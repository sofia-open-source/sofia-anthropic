# PUT /core/bank-transactions

**Resource:** [Core - Bank Transactions](../resources/Core-Bank-Transactions.md)
**Cria ou atualiza uma movimentação financeira.**
**Operation ID:** `coreCreateOrUpdateBankTransaction`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `populate` | query | string | No |  |

## Request Body

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [CreateOrUpdateBankTransactionRequestBodyDto](../schemas/Create/CreateOrUpdateBankTransactionRequestBodyDto.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

**Success Response Schema:**

[BankTransactionEntity](../schemas/Bank/BankTransactionEntity.md)

