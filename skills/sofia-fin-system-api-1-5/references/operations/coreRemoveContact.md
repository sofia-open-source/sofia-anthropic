# DELETE /core/contacts/{id}

**Resource:** [Core - Contacts](../resources/Core-Contacts.md)
**Remove um contato.**
**Operation ID:** `coreRemoveContact`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `id` | path | string | Yes | Identificador do contato. |

## Request Body

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [RemoveContactRequestBodyDto](../schemas/Remove/RemoveContactRequestBodyDto.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

