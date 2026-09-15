# FinancialRecordRadarItemAutoExecuteSettingEntity

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes | Identificador único das configurações. |
| `ownerOrganization` | string | Yes | Identificador da organização. |
| `enabledRules` | object[] | No | Regras de auto-execute habilitadas. Se não estiver listado, está desabilitado. |
| `createdAt` |  | Yes | Data de criação. |
| `updatedAt` |  | Yes | Data de atualização. |

## Nested Fields

### `enabledRules`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `origin` | enum: WHATSAPP_AGENT, EMAIL_FORWARDING_INTEGRATION, ANY | Yes | Origem do registro. |
| `nature` | enum: WHATSAPP_MESSAGE, EMAIL_MESSAGE, ANY | Yes | Natureza do registro. |
| `operation` | enum: CREATE, CREATE_MANY, LINK_TO_THIS_RADAR_ITEM... | Yes | Operação a ser executada. |

