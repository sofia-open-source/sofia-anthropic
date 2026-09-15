# POST /core/bank-transactions/{bankTransactionId}/unreconcile

**Resource:** [Core - Bank Transactions](../resources/Core-Bank-Transactions.md)
**Desfaz a reconciliação de uma transação bancária.**
**Operation ID:** `coreUnreconcileBankTransaction`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `bankTransactionId` | path | string | Yes | Bank transaction ID to undo reconciliation. |

## Responses

| Status | Description |
|--------|-------------|
| 200 | The bank transaction with reconciliation undone. |
| default |  |

**Success Response Schema:**

[BankTransactionEntity](../schemas/Bank/BankTransactionEntity.md)

