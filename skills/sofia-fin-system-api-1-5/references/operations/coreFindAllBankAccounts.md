# GET /core/bank-accounts

**Resource:** [Core - Bank Accounts](../resources/Core-Bank-Accounts.md)
**Busca todas as contas bancárias.**
**Operation ID:** `coreFindAllBankAccounts`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `pageIndex` | query | number | No |  |
| `pageSize` | query | number | No |  |
| `textSearchTerm` | query | string | No |  |
| `readPreference` | query | enum: primary, primaryPreferred, secondary... | No |  |
| `semanticSearchTermInBase64` | query | string | No |  |
| `type` | query | enum: MONEY, CHECKING, SAVINGS... | No |  |
| `isAutomatic` | query | boolean | No |  |
| `isDefault` | query | boolean | No |  |
| `ids` | query | string[] | No | Lista de IDs de contas bancárias para filtrar. |
| `active` | query | boolean | No |  |
| `provider` | query | enum: PLUGGY, OFX, OTHER | No |  |
| `providerItemId` | query | string | No |  |
| `sortBy` | query | enum: name, type, institution... | No |  |
| `sortOrder` | query | enum: asc, desc | No |  |
| `populate` | query | string | No |  |
| `ownerOrganizationId` | query | string | No |  |

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

**Success Response Schema:**

[BankAccountsPageResponseDto](../schemas/Bank/BankAccountsPageResponseDto.md)

