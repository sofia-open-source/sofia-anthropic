# GET /core/bank-accounts/pluggy/{itemId}

**Resource:** [Core - Bank Accounts](../resources/Core-Bank-Accounts.md)
**Busca contas bancárias pelo identificador do item do Pluggy.**
**Operation ID:** `coreFindAllByPluggyItem`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `itemId` | path | string | Yes | Pluggy connection item identifier. |
| `populate` | query | string | No |  |

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

**Success Response Schema:**

Array of [BankAccountResponseDto](../schemas/Bank/BankAccountResponseDto.md)

