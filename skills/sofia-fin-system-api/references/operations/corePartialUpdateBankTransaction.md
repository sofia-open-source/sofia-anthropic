# PATCH /core/bank-transactions/{id}

**Resource:** [Core - Bank Transactions](../resources/Core-Bank-Transactions.md)
**Atualiza parcialmente uma movimentação financeira.**
**Operation ID:** `corePartialUpdateBankTransaction`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `id` | path | string | Yes | Bank transaction ID. |
| `populate` | query | string | No |  |

## Request Body

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [PartialUpdateBankTransactionRequestBodyDto](../schemas/Partial/PartialUpdateBankTransactionRequestBodyDto.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

**Success Response Schema:**

[BankTransactionEntity](../schemas/Bank/BankTransactionEntity.md)

