# POST /core/bank-transactions/bulk-operations

**Resource:** [Core - Bank Transactions](../resources/Core-Bank-Transactions.md)
**Agenda uma operação em lote para transações bancárias.**
**Operation ID:** `coreScheduleBulkBankTransactionsOperation`

## Request Body

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [BulkBankTransactionsJobRequestResponseDto](../schemas/Bulk/BulkBankTransactionsJobRequestResponseDto.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 |  |
| default |  |

**Success Response Schema:**

[BulkBankTransactionsJobRequestEntity](../schemas/Bulk/BulkBankTransactionsJobRequestEntity.md)

