---
name: Provision a Tiger Cloud PostgreSQL service
description: Create a managed TimescaleDB/PostgreSQL service on Tiger Cloud and poll it to READY before handing back a connection endpoint.
api: openapi/timescale-tiger-cloud-openapi-original.yml
operations: [getAuthInfo, getProjects, createService, getService, getServices]
generated: '2026-08-05'
method: generated
source: openapi/timescale-tiger-cloud-openapi-original.yml + https://www.tigerdata.com/docs/get-started/quickstart/rest-api
---

# Provision a Tiger Cloud PostgreSQL service

Base URL: `https://console.cloud.tigerdata.com/public/api/v1`

## Authenticate first

Tiger Cloud uses **HTTP Basic** with client credentials created in Tiger Console: the
public access key is the username, the secret key is the password.

```
curl -u "${TIGERDATA_ACCESS_KEY}:${TIGERDATA_SECRET_KEY}" ...
```

There is no OpenAPI `securitySchemes` block to read this from — it is documented in prose
only. A missing header returns `401 {"code":"UNAUTHORIZED","message":"Invalid or missing
authentication credentials","details":"missing Authorization header"}`.

1. Call `getAuthInfo` (`GET /auth/info`). The `type` field returns `apiKey` for a
   personal-access-token caller and `oauth` for an OAuth user. Confirm you are the caller
   you expect to be before doing anything mutating.
2. Call `getProjects` (`GET /projects`). A PAT caller sees exactly one project — its own
   scope. Use that `id` as `project_id` in every path below.

## Create the service

3. Call `createService` (`POST /projects/{project_id}/services`) with a `ServiceCreate`
   body: `name`, `region_code`, `cpu_millis`, `memory_gbs`, optional `replica_count`,
   `addons`, and `environment_tag` (`DEV` or `PROD` — set `DEV` for anything that is not
   production).

   **This operation is not idempotent.** Tiger Data publishes no idempotency key for any
   operation. Do not retry a `createService` on a timeout or an ambiguous failure — call
   `getServices` and check whether the service already exists before trying again.

4. The response is `202 Accepted` carrying the `Service` resource immediately, including
   `service_id` (a 10-character alphanumeric string) and `initial_password`.
   **`initial_password` is returned once.** Capture it now; there is no operation to read
   it back. `updatePassword` can rotate it later.

## Poll to READY

5. Poll `getService` (`GET /projects/{project_id}/services/{service_id}`) until
   `status` is `READY`. There is no operation/job resource and no `Location` header to
   follow — polling the service itself is the only mechanism.

   `DeployStatus` values: `QUEUED`, `CONFIGURING`, `READY`, `OPTIMIZING`, `UPGRADING`,
   `PAUSING`, `PAUSED`, `RESUMING`, `DELETING`, `DELETED`, `UNSTABLE`.

   Treat `UNSTABLE` as a terminal failure to report, not a state to keep polling through.
   Back off between polls; no rate limit is published, so be conservative.

6. When `READY`, read `endpoint` (`host` + `port`) for the direct connection, or
   `connection_pooler.endpoint` if you called `enablePooler`.

## Rules

- Every error is a flat `{code, message, details?}` envelope on `application/json`. It is
  **not** RFC 9457. Branch on `code`, not on the HTTP status — the spec declares a single
  wildcard `4XX` per operation and enumerates no concrete statuses and no 5xx at all.
- `getServices` returns an unbounded array with no pagination parameters. Do not expect a
  cursor.
- Do not call `deleteService` from an agent loop. It is the one destructive service
  operation Tiger Data deliberately did **not** expose as an MCP tool.
