# PATCH /core/legal-entities/{id}/focus-nfse-rps-settings

**Resource:** [Core - Legal entities](../resources/Core-Legal-entities.md)
**Atualiza série e/ou próximo RPS de NFSe municipal em produção na Focus NFe.**
**Operation ID:** `coreUpdateLegalEntityFocusNfseRpsSettings`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `id` | path | string | Yes | Identificador da entidade legal. |

## Request Body

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [UpdateLegalEntityFocusNfseRpsSettingsRequestBodyDto](../schemas/Update/UpdateLegalEntityFocusNfseRpsSettingsRequestBodyDto.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

**Success Response Schema:**

[LegalEntityFocusNfseRpsSettingsResponseDto](../schemas/Legal/LegalEntityFocusNfseRpsSettingsResponseDto.md)

