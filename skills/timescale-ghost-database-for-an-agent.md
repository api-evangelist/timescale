---
name: Give an agent its own Ghost Postgres database
description: Create a Ghost space, mint a scoped API key, provision and fork a database, and check usage — the agent-native path on api.ghost.build.
api: openapi/timescale-ghost-openapi-original.yml
operations: [authInfo, getPricing, createSpace, createApiKey, createDatabase, getDatabase, listDatabases, forkDatabase, pauseDatabase, resumeDatabase, shareDatabase, spaceUsage]
generated: '2026-08-05'
method: generated
source: openapi/timescale-ghost-openapi-original.yml + https://ghost.build/agents.txt
---

# Give an agent its own Ghost Postgres database

Base URL: `https://api.ghost.build/v0`. Auth is
`Authorization: Bearer <JWT or gt_-prefixed API key>` on every operation except
`GET /health`, which is anonymous and is the liveness probe.

## Understand the bill before provisioning

1. `getPricing` (`GET /pricing`) is callable and returns `Pricing` →
   `standard` / `dedicated`, with `included_compute_hours_per_month` and
   `included_gib_per_database`. Read it before creating anything; Ghost databases are
   billable beyond the included tier.

2. `authInfo` (`GET /auth/info`) confirms who you are — `type`, plus `api_key`
   (`ApiKeyInfo`: `prefix`, `name`, `space_id`, `space_name`, ...) or `user` (`UserInfo`).

## Set up a space and a scoped key

3. `createSpace` (`POST /spaces`) with `{name}`. The space is the tenancy boundary — every
   database, member, invite, key and invoice hangs off `space_id`.

4. `createApiKey` (`POST /spaces/{space_id}/api_keys`) with `{name}`. The response is
   `ApiKeyCredentials` (`api_key`, `access_key`, `secret_key`) — **capture it now**;
   `listApiKeys` afterwards returns only `prefix`, `name`, `created_at`. Keys are revoked
   by prefix with `deleteApiKey`, never by full value.

   Give the agent its own named key so it can be revoked independently. Note that key
   minting has deliberately **no MCP tool** — do this out-of-band, not from inside an
   agent loop.

## Provision the database

5. `createDatabase` (`POST /spaces/{space_id}/databases`) with a `CreateDatabaseRequest`:
   `name`, `type` (`standard` | `dedicated`), `size` (`1x` | `2x` | `4x` | `8x`), optional
   `share_token`. Returns `202 Accepted`.

   **Not idempotent** — no idempotency key exists on any Ghost operation. On an ambiguous
   failure call `listDatabases` and check by name before retrying.

6. Poll `getDatabase` (`GET /spaces/{space_id}/databases/{database_ref}`) — `database_ref`
   accepts the id **or** the name — until `status` is `running`. `DatabaseStatus`:
   `queued`, `configuring`, `running`, `pausing`, `paused`, `resuming`, `deleting`,
   `deleted`, `upgrading`, `unstable`, `unknown`.

7. Connect with `host`, `port` and `password` from the `Database` object.

## Operate

- `forkDatabase` — zero-copy branch for an experiment.
- `pauseDatabase` / `resumeDatabase` — stop paying for idle compute between agent runs.
- `shareDatabase` → returns a share token; `listShares` / `revokeShare` manage them.
  Treat a share token as a credential.
- `spaceUsage` (`GET /spaces/{space_id}/usage`) — `storage_mib`, `compute_minutes`,
  `cost_to_date`, `estimated_total_cost`, `overages_enabled`. Check this on a schedule; it
  is the only guardrail against an agent running up a bill.

## Rules

- Errors are `{message, code}` on a `default` response, not RFC 9457. The published
  `ErrorCode` enum is `no_payment_method` and `compute_limit_exceeded` — handle both
  explicitly, because both mean "stop provisioning", not "retry".
- No list operation paginates. Every collection returns an unbounded array.
- Not one of the 48 operations carries a tag, so do not rely on tag grouping to navigate
  the spec.
