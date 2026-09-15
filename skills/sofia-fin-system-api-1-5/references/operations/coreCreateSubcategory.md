# POST /core/subcategories

**Resource:** [Core - Subcategories](../resources/Core-Subcategories.md)
**Cria uma nova subcategoria.**
**Operation ID:** `coreCreateSubcategory`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `populate` | query | string | No |  |

## Request Body

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [ExternalCreateSubcategoryRequestBodyDto](../schemas/External/ExternalCreateSubcategoryRequestBodyDto.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 |  |
| default |  |

**Success Response Schema:**

[SubcategoryResponseDto](../schemas/Subcategory/SubcategoryResponseDto.md)

