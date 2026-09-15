# Core - Financial Records Export

Contains endpoints to export the financial records of the organization synchronously or asynchronously in csv or xlsx format. You can export all records or filter them.

## Operations

| Method | Path | Summary | Details |
|--------|------|---------|----------|
| POST | `/core/financial-records/export` | Solicita a exportação dos lançamentos financeiros de forma assíncrona. | [View](../operations/coreExportFinancialRecords.md) |
| POST | `/core/financial-records/export/sync` | Solicita a exportação dos lançamentos financeiros de forma síncrona. | [View](../operations/coreSyncExportFinancialRecords.md) |
