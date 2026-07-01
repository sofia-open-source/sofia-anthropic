# PATCH /core/contacts/{id}

**Resource:** [Core - Contacts](../resources/Core-Contacts.md)
**Atualiza parcialmente um contato.**
**Operation ID:** `corePartialUpdateContact`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `id` | path | string | Yes | Identificador do contato. |
| `populate` | query | string | No |  |

## Request Body

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [PartialUpdateContactRequestBodyDto](../schemas/Partial/PartialUpdateContactRequestBodyDto.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

**Success Response Schema:**

[ContactResponseDto](../schemas/Contact/ContactResponseDto.md)

