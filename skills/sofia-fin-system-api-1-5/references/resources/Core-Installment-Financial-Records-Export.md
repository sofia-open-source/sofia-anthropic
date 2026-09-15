# Core - Installment Financial Records Export

Export endpoints for installment financial records in csv or xlsx format. POST /core/installment-financial-records/export schedules an async job and returns a pending job id; POST …/export/sync runs immediately and returns the job id plus the generated file. Both accept the same query filters as the list endpoint. Use async export for large datasets; use sync when the caller needs the file in the same response.

## Operations

| Method | Path | Summary | Details |
|--------|------|---------|----------|
| POST | `/core/installment-financial-records/export` | Request export of installment financial records. | [View](../operations/coreExportInstallmentFinancialRecords.md) |
| POST | `/core/installment-financial-records/export/sync` | Request synchronous export of installment financial records. | [View](../operations/coreSyncExportInstallmentFinancialRecords.md) |
