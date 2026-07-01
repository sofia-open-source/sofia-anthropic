# DELETE /core/bank-accounts/{id}

**Resource:** [Core - Bank Accounts](../resources/Core-Bank-Accounts.md)
**Remove uma conta bancária.**
**Operation ID:** `coreRemoveBankAccount`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `id` | path | string | Yes | Bank account identifier. |

## Request Body

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [RemoveBankAccountRequestBodyDto](../schemas/Remove/RemoveBankAccountRequestBodyDto.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

