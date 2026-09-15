# POST /core/contacts/export

**Resource:** [Core - Contacts Export](../resources/Core-Contacts-Export.md)
**Solicita a exportação dos contatos.**
**Operation ID:** `coreExportContacts`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `textSearchTerm` | query | string | No |  |
| `readPreference` | query | enum: primary, primaryPreferred, secondary... | No |  |
| `semanticSearchTermInBase64` | query | string | No |  |
| `ids` | query | string[] | No | List of contact IDs to filter by. |
| `types` | query | any | No |  |
| `origins` | query | any | No |  |
| `birthdayFrom` | query | string | No |  |
| `birthdayTo` | query | string | No |  |
| `country` | query | string | No |  |
| `states` | query | any | No |  |
| `considerNotIdentified` | query | boolean | No |  |
| `sortBy` | query | enum: name, document, email... | No |  |
| `sortOrder` | query | enum: asc, desc | No |  |
| `populate` | query | string | No |  |
| `format` | query | enum: csv, xlsx | Yes |  |

## Responses

| Status | Description |
|--------|-------------|
| 200 | The id of the pending resource job. |
| default |  |

**Success Response Schema:**

[ExportContactsResponseDto](../schemas/Export/ExportContactsResponseDto.md)

