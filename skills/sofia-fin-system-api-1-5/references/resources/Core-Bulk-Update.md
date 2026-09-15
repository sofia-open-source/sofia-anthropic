# Core - Bulk Update

Async mass update of fields on a resource type. POST /core/bulk/update schedules a job describing target ids and patch payload; the queue worker applies changes in batch. Supports the same core resource set as other bulk operations. Use for spreadsheet-driven corrections or integration sync-back.

## Operations

| Method | Path | Summary | Details |
|--------|------|---------|----------|
| POST | `/core/bulk/update` | Schedules updating of multiple resources | [View](../operations/coreScheduleBulkUpdate.md) |
