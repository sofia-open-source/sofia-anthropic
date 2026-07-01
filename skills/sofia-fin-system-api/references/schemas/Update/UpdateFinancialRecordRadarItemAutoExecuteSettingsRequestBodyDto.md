# UpdateFinancialRecordRadarItemAutoExecuteSettingsRequestBodyDto

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `desiredEnabledRules` | object[] | No | Regras de auto-execute desejadas. |
| `desiredDisabledRules` | object[] | No | Regras de auto-execute desabilitadas. |

## Nested Fields

### `desiredEnabledRules`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `origin` | enum: WHATSAPP_AGENT, EMAIL_FORWARDING_INTEGRATION, ANY | Yes | Origem do registro. |
| `nature` | enum: WHATSAPP_MESSAGE, EMAIL_MESSAGE, ANY | Yes | Natureza do registro. |
| `operation` | enum: CREATE, CREATE_MANY, LINK_TO_THIS_RADAR_ITEM... | Yes | Operação a ser executada. |

### `desiredDisabledRules`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `origin` | enum: WHATSAPP_AGENT, EMAIL_FORWARDING_INTEGRATION, ANY | Yes | Origem do registro. |
| `nature` | enum: WHATSAPP_MESSAGE, EMAIL_MESSAGE, ANY | Yes | Natureza do registro. |
| `operation` | enum: CREATE, CREATE_MANY, LINK_TO_THIS_RADAR_ITEM... | Yes | Operação a ser executada. |

