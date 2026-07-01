# GET /core/contacts/{id}

**Resource:** [Core - Contacts](../resources/Core-Contacts.md)
**Busca um contato pelo identificador.**
**Operation ID:** `coreFindByIdContact`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `id` | path | string | Yes | Identificador do contato. |
| `populate` | query | string | No |  |

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

**Success Response Schema:**

[ContactResponseDto](../schemas/Contact/ContactResponseDto.md)

