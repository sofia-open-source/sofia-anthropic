# GET /core/legal-entities

**Resource:** [Core - Legal entities](../resources/Core-Legal-entities.md)
**Lista todas as entidades legais da organização.**
**Operation ID:** `coreFindAllLegalEntities`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `pageIndex` | query | number | No | Índice da página. |
| `pageSize` | query | number | No | Quantidade de itens por página. |
| `isDefault` | query | boolean | No | Filtrar por entidade legal padrão. |

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

**Success Response Schema:**

[LegalEntitiesPageResponseDto](../schemas/Legal/LegalEntitiesPageResponseDto.md)

