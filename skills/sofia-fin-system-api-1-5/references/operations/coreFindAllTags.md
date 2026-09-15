# GET /core/tags

**Resource:** [Core - Tags](../resources/Core-Tags.md)
**Busca todas as tags.**
**Operation ID:** `coreFindAllTags`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `pageIndex` | query | number | No |  |
| `pageSize` | query | number | No |  |
| `textSearchTerm` | query | string | No |  |
| `sortBy` | query | enum: name, createdAt | No |  |
| `sortOrder` | query | enum: asc, desc | No |  |
| `populate` | query | string | No |  |
| `ids` | query | string[] | No | Lista de IDs de tags para filtrar. |
| `ownerOrganizationId` | query | string | No |  |

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

**Success Response Schema:**

[TagsPageResponseDto](../schemas/Tags/TagsPageResponseDto.md)

