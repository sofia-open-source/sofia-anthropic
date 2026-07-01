# PATCH /core/legal-entities/{id}

**Resource:** [Core - Legal entities](../resources/Core-Legal-entities.md)
**Atualiza uma entidade legal.**
**Operation ID:** `coreUpdateLegalEntity`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `id` | path | string | Yes | Identificador da entidade legal. |

## Request Body

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [UpdateLegalEntityRequestBodyDto](../schemas/Update/UpdateLegalEntityRequestBodyDto.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

**Success Response Schema:**

[LegalEntityResponseDto](../schemas/Legal/LegalEntityResponseDto.md)

