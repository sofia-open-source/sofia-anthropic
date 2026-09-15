# Core - Bulk Remove

Async bulk deletion across supported core resources. POST /core/bulk/remove accepts resource type and ids, schedules a job, and returns a job id; a queue worker performs the deletes. Supported types include financial records, contacts, bank accounts, bank transactions, installments, recurrences, tags, subcategories, and invoices. Use for mass cleanup from UI selections or integrations.

## Operations

| Method | Path | Summary | Details |
|--------|------|---------|----------|
| POST | `/core/bulk/remove` | Schedules removal of multiple resources | [View](../operations/coreScheduleBulkRemove.md) |
