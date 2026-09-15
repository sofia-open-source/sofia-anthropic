# GET /core/subcategories

**Resource:** [Core - Subcategories](../resources/Core-Subcategories.md)
**Busca todas as subcategorias.**
**Operation ID:** `coreFindAllSubcategories`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `pageIndex` | query | number | No |  |
| `pageSize` | query | number | No |  |
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

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

**Success Response Schema:**

[SubcategoriesPageResponseDto](../schemas/Subcategories/SubcategoriesPageResponseDto.md)

