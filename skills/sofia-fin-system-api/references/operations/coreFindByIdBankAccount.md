# GET /core/bank-accounts/{id}

**Resource:** [Core - Bank Accounts](../resources/Core-Bank-Accounts.md)
**Busca uma conta bancária pelo identificador.**
**Operation ID:** `coreFindByIdBankAccount`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `id` | path | string | Yes | Bank account identifier. |
| `populate` | query | string | No |  |

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

**Success Response Schema:**

[BankAccountResponseDto](../schemas/Bank/BankAccountResponseDto.md)

