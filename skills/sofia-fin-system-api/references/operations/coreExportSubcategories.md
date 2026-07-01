# POST /core/subcategories/export

**Resource:** [Core - Subcategories Export](../resources/Core-Subcategories-Export.md)
**Solicita a exportação das subcategorias.**
**Operation ID:** `coreExportSubcategories`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `readPreference` | query | enum: primary, primaryPreferred, secondary... | No |  |
| `sortBy` | query | enum: name, createdAt, index | No |  |
| `sortOrder` | query | enum: asc, desc | No |  |
| `populate` | query | string | No |  |
| `category` | query | string | No |  |
| `direction` | query | enum: IN, OUT | No |  |
| `active` | query | boolean | No |  |
| `textSearchTerm` | query | string | No |  |
| `semanticSearchTermInBase64` | query | string | No |  |
| `ids` | query | string[] | No | Lista de IDs de subcategorias para filtrar. |
| `hideInternalTransfers` | query | boolean | No | Se verdadeiro, esconde subcategorias de transferência interna. |
| `ownerOrganizationId` | query | string | No |  |
| `format` | query | enum: csv, xlsx | Yes |  |

## Responses

| Status | Description |
|--------|-------------|
| 200 | The id of the pending resource job. |
| default |  |

**Success Response Schema:**

[ExportSubcategoriesResponseDto](../schemas/Export/ExportSubcategoriesResponseDto.md)

