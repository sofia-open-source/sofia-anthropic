# Core - Bulk Create

Async bulk creation from uploaded spreadsheet files. POST /core/bulk/create schedules a job with resource type, fileId, and optional radar-item context; the worker parses rows and creates entities. Financial-record imports can leverage AI/file-extraction flows. Same resource families as bulk remove where creation applies.

## Operations

| Method | Path | Summary | Details |
|--------|------|---------|----------|
| POST | `/core/bulk/create` | Schedules creation of multiple resources from a file | [View](../operations/coreScheduleBulkCreate.md) |
