# Core - Bank Transactions Export

Export endpoints for bank transactions in csv or xlsx format. POST /core/bank-transactions/export schedules async export; POST …/export/sync produces the file synchronously. Query params match list filters (bank account, date range, type, reconciled status, origin, etc.). Useful for reconciliation audits and spreadsheet analysis outside the app.

## Operations

| Method | Path | Summary | Details |
|--------|------|---------|----------|
| POST | `/core/bank-transactions/export` | Solicita a exportação das transações bancárias. | [View](../operations/coreExportBankTransactions.md) |
| POST | `/core/bank-transactions/export/sync` | Solicita a exportação das transações bancárias de forma síncrona. | [View](../operations/coreSyncExportBankTransactions.md) |
