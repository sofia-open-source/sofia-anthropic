# GET /core/tags/{id}

**Resource:** [Core - Tags](../resources/Core-Tags.md)
**Busca uma tag pelo identificador.**
**Operation ID:** `coreFindByIdTag`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `id` | path | string | Yes | Identificador da tag. |
| `populate` | query | string | No |  |

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

**Success Response Schema:**

[TagResponseDto](../schemas/Tag/TagResponseDto.md)

