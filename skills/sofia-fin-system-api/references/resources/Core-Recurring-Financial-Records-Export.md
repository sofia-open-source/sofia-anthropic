# Core - Recurring Financial Records Export

Export endpoints for recurring financial record templates in csv or xlsx format. POST /core/recurring-financial-records/export enqueues async export; POST …/export/sync returns the file in the same request. Filters mirror the list API so exports can be scoped by organization and template attributes. Prefer async export for large template sets.

## Operations

| Method | Path | Summary | Details |
|--------|------|---------|----------|
| POST | `/core/recurring-financial-records/export` | Solicita a exportação dos lançamentos recorrentes. | [View](../operations/coreExportRecurringFinancialRecords.md) |
| POST | `/core/recurring-financial-records/export/sync` | Solicita a exportação dos lançamentos recorrentes de forma síncrona. | [View](../operations/coreSyncExportRecurringFinancialRecords.md) |
