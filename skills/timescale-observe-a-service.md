---
name: Read Tiger Cloud service logs and metrics
description: Page through service logs with the cursor contract and pull metric series, including which operations are preview-gated.
api: openapi/timescale-tiger-cloud-openapi-original.yml
operations: [getService, getServiceLogs, getServiceMetricsAvailableSeries, getServiceMetricsSeries]
generated: '2026-08-05'
method: generated
source: openapi/timescale-tiger-cloud-openapi-original.yml
---

# Read Tiger Cloud service logs and metrics

## Logs

`getServiceLogs` (`GET /projects/{project_id}/services/{service_id}/logs`) is the **only**
paginated operation in the whole Tiger Cloud API.

Query parameters:
- `cursor` — opaque cursor. Pass back the `last_cursor` from the previous response to get
  the next page of **older** entries. Absent `last_cursor` means there are no more results.
- `since` / `until` — RFC 3339 timestamps bounding the window.
- `node` — a specific node, for multi-node services.
- `page` — **deprecated**. Do not use it; use `cursor`.

Response is `ServiceLogs`: `logs`, `entries` (`ServiceLogEntry`: `timestamp`, `message`,
`severity`), and `lastCursor`. Entries come back in reverse-chronological order.

Loop: call with no cursor, read `entries`, then re-call with `cursor: <lastCursor>` until
`lastCursor` is absent.

## Metrics

Both metrics operations are marked `x-preview: true` in the spec, and the Tiger CLI/MCP
surface only registers them when an experimental flag is set at startup. Treat them as
unstable and do not build a hard dependency on their shape.

1. `getServiceMetricsAvailableSeries`
   (`GET /projects/{project_id}/services/{service_id}/metrics/available-series`) — discover
   which series names exist before asking for data. Never guess a series name.

2. `getServiceMetricsSeries`
   (`POST /projects/{project_id}/services/{service_id}/metrics/series`) with a
   `MetricsSeriesRequest`: `name`, `from`, `to`, `bucket_seconds`, `fn`, and `filters`
   (`MetricLabelFilter`: `key`, `value`). Response is `MetricSeries` (`labels`, `data`),
   where each `MetricDataPoint` is `{time, value}`.

## Rules

- No rate limit, `Retry-After`, or 429 semantics are documented anywhere. Poll gently and
  back off on any `4XX`.
- No request-id or correlation-id header is declared, so there is nothing to quote to
  support when an operation misbehaves — capture the full `{code, message, details}` body
  instead.
- Both operations are reads and are safe to retry.
