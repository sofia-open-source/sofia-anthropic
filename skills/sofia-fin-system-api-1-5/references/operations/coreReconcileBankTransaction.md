# POST /core/bank-transactions/{bankTransactionId}/reconcile

**Resource:** [Core - Bank Transactions](../resources/Core-Bank-Transactions.md)
**Reconcilia uma transação bancária com múltiplos lançamentos financeiros.**
**Operation ID:** `coreReconcileBankTransaction`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `bankTransactionId` | path | string | Yes | Bank transaction ID to reconcile. |

## Request Body

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [ReconcileBankTransactionRequestBodyDto](../schemas/Reconcile/ReconcileBankTransactionRequestBodyDto.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 | The reconciled bank transaction. |
| default |  |

**Success Response Schema:**

[BankTransactionEntity](../schemas/Bank/BankTransactionEntity.md)

