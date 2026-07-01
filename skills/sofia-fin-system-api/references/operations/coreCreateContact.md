# POST /core/contacts

**Resource:** [Core - Contacts](../resources/Core-Contacts.md)
**Cria um novo contato.**
**Operation ID:** `coreCreateContact`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `populate` | query | string | No |  |

## Request Body

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [CreateContactRequestBodyDto](../schemas/Create/CreateContactRequestBodyDto.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 |  |
| default |  |

**Success Response Schema:**

[ContactResponseDto](../schemas/Contact/ContactResponseDto.md)

