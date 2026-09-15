# POST /core/bank-accounts

**Resource:** [Core - Bank Accounts](../resources/Core-Bank-Accounts.md)
**Cria uma nova conta bancária.**
**Operation ID:** `coreCreateBankAccount`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `populate` | query | string | No |  |

## Request Body

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [CreateBankAccountRequestBodyDto](../schemas/Create/CreateBankAccountRequestBodyDto.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 |  |
| default |  |

**Success Response Schema:**

[BankAccountResponseDto](../schemas/Bank/BankAccountResponseDto.md)

