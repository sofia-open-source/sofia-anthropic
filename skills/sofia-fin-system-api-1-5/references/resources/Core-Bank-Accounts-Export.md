# Core - Bank Accounts Export

Export bank accounts in csv or xlsx format. POST /core/bank-accounts/export enqueues async export; POST …/export/sync returns the generated file in one response. Optional id filters narrow the export set. Useful for account registers and external treasury tools.

## Operations

| Method | Path | Summary | Details |
|--------|------|---------|----------|
| POST | `/core/bank-accounts/export` | Solicita a exportação das contas bancárias. | [View](../operations/coreExportBankAccounts.md) |
| POST | `/core/bank-accounts/export/sync` | Solicita a exportação das contas bancárias de forma síncrona. | [View](../operations/coreSyncExportBankAccounts.md) |
