# POST /core/tags

**Resource:** [Core - Tags](../resources/Core-Tags.md)
**Cria uma nova tag.**
**Operation ID:** `coreCreateTag`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `populate` | query | string | No |  |

## Request Body

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [CreateTagRequestBodyDto](../schemas/Create/CreateTagRequestBodyDto.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 |  |
| default |  |

**Success Response Schema:**

[TagResponseDto](../schemas/Tag/TagResponseDto.md)

