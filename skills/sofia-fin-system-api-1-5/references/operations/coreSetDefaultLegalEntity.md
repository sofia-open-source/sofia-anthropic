# POST /core/legal-entities/{id}/set-as-default

**Resource:** [Core - Legal entities](../resources/Core-Legal-entities.md)
**Define uma entidade legal como padrão da organização.**
**Operation ID:** `coreSetDefaultLegalEntity`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `id` | path | string | Yes | Identificador da entidade legal. |

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

**Success Response Schema:**

[LegalEntityResponseDto](../schemas/Legal/LegalEntityResponseDto.md)

