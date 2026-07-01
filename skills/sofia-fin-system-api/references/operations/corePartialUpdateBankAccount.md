# PATCH /core/bank-accounts/{id}

**Resource:** [Core - Bank Accounts](../resources/Core-Bank-Accounts.md)
**Atualiza parcialmente uma conta bancária.**
**Operation ID:** `corePartialUpdateBankAccount`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `id` | path | string | Yes | Bank account identifier. |
| `populate` | query | string | No |  |

## Request Body

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [PartialUpdateBankAccountRequestBodyDto](../schemas/Partial/PartialUpdateBankAccountRequestBodyDto.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

**Success Response Schema:**

[BankAccountResponseDto](../schemas/Bank/BankAccountResponseDto.md)

