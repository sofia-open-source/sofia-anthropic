# PATCH /core/subcategories/{id}

**Resource:** [Core - Subcategories](../resources/Core-Subcategories.md)
**Atualiza parcialmente uma subcategoria.**
**Operation ID:** `corePartialUpdateSubcategory`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `id` | path | string | Yes | Identificador da subcategoria. |
| `populate` | query | string | No |  |

## Request Body

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [PartialUpdateSubcategoryRequestBodyDto](../schemas/Partial/PartialUpdateSubcategoryRequestBodyDto.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

**Success Response Schema:**

[SubcategoryResponseDto](../schemas/Subcategory/SubcategoryResponseDto.md)

