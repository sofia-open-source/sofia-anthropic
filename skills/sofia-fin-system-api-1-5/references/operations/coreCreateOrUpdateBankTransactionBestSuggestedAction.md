# PUT /core/bank-transactions/{bankTransactionId}/best-suggested-action

**Resource:** [Core - Bank Transactions](../resources/Core-Bank-Transactions.md)
**Cria ou atualiza uma sugestão de melhor ação para uma transação bancária.**
**Operation ID:** `coreCreateOrUpdateBankTransactionBestSuggestedAction`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `bankTransactionId` | path | string | Yes | Bank transaction ID to get best action suggestions. |

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

**Success Response Schema:**

[BankTransactionEntity](../schemas/Bank/BankTransactionEntity.md)

