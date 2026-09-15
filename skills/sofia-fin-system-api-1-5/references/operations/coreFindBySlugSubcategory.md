# GET /core/subcategories/slug/{slug}

**Resource:** [Core - Subcategories](../resources/Core-Subcategories.md)
**Busca uma subcategoria pelo slug.**
**Operation ID:** `coreFindBySlugSubcategory`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `slug` | path | string | Yes | Slug da subcategoria. |
| `populate` | query | string | No |  |

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

**Success Response Schema:**

[SubcategoryResponseDto](../schemas/Subcategory/SubcategoryResponseDto.md)

