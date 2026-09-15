# Core - Bank Accounts

Organization bank accounts: checking, savings, and credit card. CRUD, paginated list, find-by-id, org-scoped list, and account-type reference data. Supports open-finance lookup by Pluggy item id for linked accounts. Accounts anchor bank transactions and balance analytics.

## Operations

| Method | Path | Summary | Details |
|--------|------|---------|----------|
| GET | `/core/bank-accounts` | Busca todas as contas bancárias. | [View](../operations/coreFindAllBankAccounts.md) |
| POST | `/core/bank-accounts` | Cria uma nova conta bancária. | [View](../operations/coreCreateBankAccount.md) |
| GET | `/core/bank-accounts/{id}` | Busca uma conta bancária pelo identificador. | [View](../operations/coreFindByIdBankAccount.md) |
| DELETE | `/core/bank-accounts/{id}` | Remove uma conta bancária. | [View](../operations/coreRemoveBankAccount.md) |
| PATCH | `/core/bank-accounts/{id}` | Atualiza parcialmente uma conta bancária. | [View](../operations/corePartialUpdateBankAccount.md) |
| GET | `/core/bank-accounts/types` | Busca todos os tipos de conta bancária. | [View](../operations/coreFindAllBankAccountTypes.md) |
| GET | `/core/bank-accounts/pluggy/{itemId}` | Busca contas bancárias pelo identificador do item do Pluggy. | [View](../operations/coreFindAllByPluggyItem.md) |
