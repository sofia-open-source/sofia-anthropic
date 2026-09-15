# POST /core/tags/export

**Resource:** [Core - Tags Export](../resources/Core-Tags-Export.md)
**Solicita a exportação das tags.**
**Operation ID:** `coreExportTags`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `textSearchTerm` | query | string | No |  |
| `sortBy` | query | enum: name, createdAt | No |  |
| `sortOrder` | query | enum: asc, desc | No |  |
| `populate` | query | string | No |  |
| `ids` | query | string[] | No | Lista de IDs de tags para filtrar. |
| `ownerOrganizationId` | query | string | No |  |
| `format` | query | enum: csv, xlsx | Yes |  |

## Responses

| Status | Description |
|--------|-------------|
| 200 | The id of the pending resource job. |
| default |  |

**Success Response Schema:**

[ExportTagsResponseDto](../schemas/Export/ExportTagsResponseDto.md)

