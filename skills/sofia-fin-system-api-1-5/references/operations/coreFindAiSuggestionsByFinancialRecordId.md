# GET /core/financial-records/{financialRecordId}/ai-suggestions

**Resource:** [Core - Bank Transactions](../resources/Core-Bank-Transactions.md)
**Busca sugestões de AI por ID do lançamento financeiro.**
**Operation ID:** `coreFindAiSuggestionsByFinancialRecordId`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `financialRecordId` | path | string | Yes | Financial record ID. |

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

**Success Response Schema:**

Array of [BankTransactionEntity](../schemas/Bank/BankTransactionEntity.md)

