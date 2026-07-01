# PATCH /core/tags/{id}

**Resource:** [Core - Tags](../resources/Core-Tags.md)
**Atualiza parcialmente uma tag.**
**Operation ID:** `corePartialUpdateTag`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `id` | path | string | Yes | Identificador da tag. |
| `populate` | query | string | No |  |

## Request Body

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [PartialUpdateTagRequestBodyDto](../schemas/Partial/PartialUpdateTagRequestBodyDto.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

**Success Response Schema:**

[TagResponseDto](../schemas/Tag/TagResponseDto.md)

