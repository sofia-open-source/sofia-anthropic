# GET /core/contacts

**Resource:** [Core - Contacts](../resources/Core-Contacts.md)
**Busca todos os contatos.**
**Operation ID:** `coreFindAllContacts`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `pageIndex` | query | number | No |  |
| `pageSize` | query | number | No |  |
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

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

**Success Response Schema:**

[ContactsPageResponseDto](../schemas/Contacts/ContactsPageResponseDto.md)

