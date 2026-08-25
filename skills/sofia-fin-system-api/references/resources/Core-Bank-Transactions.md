# Core - Bank Transactions

Imported bank statement lines from OFX manual import or open finance (Pluggy), used to reconcile against financial records. CRUD-style read/update/delete, reconcile and unreconcile, bulk archive/unarchive/reconcile, and AI-suggested actions for matching. OFX import flows schedule jobs, list executions, retry failures, and download failure reports. System endpoints support provider-driven create-or-update for integrated feeds.

## Operations

| Method | Path | Summary | Details |
|--------|------|---------|----------|
| GET | `/core/bank-transactions` | Busca todas as movimentações financeiras. | [View](../operations/coreFindAllBankTransactions.md) |
| PUT | `/core/bank-transactions` | Cria ou atualiza uma movimentação financeira. | [View](../operations/coreCreateOrUpdateBankTransaction.md) |
| GET | `/core/bank-transactions/{id}` | Busca uma movimentação financeira por ID. | [View](../operations/coreFindBankTransactionById.md) |
| PATCH | `/core/bank-transactions/{id}` | Atualiza parcialmente uma movimentação financeira. | [View](../operations/corePartialUpdateBankTransaction.md) |
| POST | `/core/bank-transactions/ofx` | Dispara a importação assíncrona de um arquivo OFX. | [View](../operations/coreDispatchOfxImport.md) |
| POST | `/core/bank-transactions/{bankTransactionId}/reconcile` | Reconcilia uma transação bancária com múltiplos lançamentos financeiros. | [View](../operations/coreReconcileBankTransaction.md) |
| POST | `/core/bank-transactions/{bankTransactionId}/unreconcile` | Desfaz a reconciliação de uma transação bancária. | [View](../operations/coreUnreconcileBankTransaction.md) |
| GET | `/core/bank-transactions/ofx/job-requests` | Lista todas as solicitações de importação de arquivos OFX com suas execuções. | [View](../operations/coreFindAllOfxImportJobRequests.md) |
| PUT | `/core/bank-transactions/{bankTransactionId}/best-suggested-action` | Cria ou atualiza uma sugestão de melhor ação para uma transação bancária. | [View](../operations/coreCreateOrUpdateBankTransactionBestSuggestedAction.md) |
| POST | `/core/bank-transactions/should-ai-suggest-action` | Verifica se a AI deve sugerir uma ação para uma transação bancária. | [View](../operations/coreShouldAiSuggestAction.md) |
| POST | `/core/bank-transactions/bulk-operations` | Agenda uma operação em lote para transações bancárias. | [View](../operations/coreScheduleBulkBankTransactionsOperation.md) |
| GET | `/core/financial-records/{financialRecordId}/ai-suggestions` | Busca sugestões de AI por ID do lançamento financeiro. | [View](../operations/coreFindAiSuggestionsByFinancialRecordId.md) |
| POST | `/core/bank-transactions/ofx/job-requests/{id}/retry` | Reexecuta a importação de um job request de OFX. | [View](../operations/coreRetryOfxImport.md) |
| GET | `/core/bank-transactions/ofx/job-executions/{id}/failures/download` | Baixa as falhas de uma execução de importação OFX em Excel. | [View](../operations/coreDownloadOfxImportFailures.md) |
