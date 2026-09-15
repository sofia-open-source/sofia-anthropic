# GET /core/bank-transactions/{id}

**Resource:** [Core - Bank Transactions](../resources/Core-Bank-Transactions.md)
**Busca uma movimentação financeira por ID.**
**Operation ID:** `coreFindBankTransactionById`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `id` | path | string | Yes | Bank transaction ID. |
| `populate` | query | string | No |  |

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

**Success Response Schema:**

[BankTransactionEntity](../schemas/Bank/BankTransactionEntity.md)

