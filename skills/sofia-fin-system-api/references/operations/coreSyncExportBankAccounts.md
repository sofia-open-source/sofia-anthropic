# POST /core/bank-accounts/export/sync

**Resource:** [Core - Bank Accounts Export](../resources/Core-Bank-Accounts-Export.md)
**Solicita a exportação das contas bancárias de forma síncrona.**
**Operation ID:** `coreSyncExportBankAccounts`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
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
| `format` | query | enum: csv, xlsx | Yes |  |

## Responses

| Status | Description |
|--------|-------------|
| 200 | The id of the job and the file generated. |
| default |  |

**Success Response Schema:**

[SyncExportResourceResponseDto](../schemas/Sync/SyncExportResourceResponseDto.md)

