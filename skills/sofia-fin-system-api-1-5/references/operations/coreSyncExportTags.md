# POST /core/tags/export/sync

**Resource:** [Core - Tags Export](../resources/Core-Tags-Export.md)
**Solicita a exportação das tags de forma síncrona.**
**Operation ID:** `coreSyncExportTags`

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
| 200 | The id of the job and the file generated. |
| default |  |

**Success Response Schema:**

[SyncExportResourceResponseDto](../schemas/Sync/SyncExportResourceResponseDto.md)

