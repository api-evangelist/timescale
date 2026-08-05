---
name: Fork a Tiger Cloud service to get a disposable copy of production data
description: Use zero-copy forks (including point-in-time) as Tiger Data's substitute for a sandbox, then resize or tear the fork down.
api: openapi/timescale-tiger-cloud-openapi-original.yml
operations: [getServices, getService, forkService, resizeService, stopService, startService]
generated: '2026-08-05'
method: generated
source: openapi/timescale-tiger-cloud-openapi-original.yml
---

# Fork a Tiger Cloud service to get a disposable copy of production data

Tiger Data publishes **no test-mode credentials and no magic test values**. A fork is the
provider's actual answer to "give me somewhere safe to test."

## Steps

1. `getServices` (`GET /projects/{project_id}/services`) — find the source
   `service_id` and confirm its `status` is `READY`.

2. `forkService` (`POST /projects/{project_id}/services/{service_id}/forkService`) with a
   `ForkServiceCreate` body:
   - `name` — name the fork so it is obviously disposable.
   - `fork_strategy` — one of `LAST_SNAPSHOT`, `NOW`, `PITR`.
   - `target_time` — required with `PITR`; reconstructs the service as of that instant.
   - `cpu_millis` / `memory_gbs` — size the fork **down**; it does not need production
     resources and it bills like any other service.
   - `environment_tag: DEV`.

3. The response is `202 Accepted` with the new `Service`. Poll `getService` on the new
   `service_id` until `status` is `READY`. The fork's `forked_from` field (`ForkSpec`:
   `project_id`, `service_id`, `is_standby`) carries its lineage back to the parent — read
   it to prove you are pointed at the fork and not the original.

4. Capture `initial_password` from the create response. It is returned once.

5. Test against the fork's `endpoint`.

6. Between runs, call `stopService` to stop paying for idle compute and `startService` to
   bring it back; both are `202` and require polling `getService` for `PAUSED` / `READY`.
   `resizeService` changes `cpu_millis` / `memory_gbs` on a running fork.

## Rules

- **No idempotency key exists.** A retried `forkService` creates a second fork and a second
  bill. On an ambiguous failure, call `getServices` and look for the fork by name before
  retrying.
- A fork is a full, billable service, not a free sandbox. Tear it down deliberately.
- `environment_tag` is a label, not an isolation boundary — a `DEV` fork sits on the same
  API surface with the same credentials as production.
