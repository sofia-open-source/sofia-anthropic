# GET /core/subcategories/{id}

**Resource:** [Core - Subcategories](../resources/Core-Subcategories.md)
**Busca uma subcategoria pelo identificador.**
**Operation ID:** `coreFindByIdSubcategory`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `id` | path | string | Yes | Identificador da subcategoria. |
| `populate` | query | string | No |  |

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

**Success Response Schema:**

[SubcategoryResponseDto](../schemas/Subcategory/SubcategoryResponseDto.md)

