# PartialUpdateOrganizationRequestBodyDto

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `name` | string | No | Nome da organização. |
| `slug` | string | No | Slug da organização. |
| `document` | string | No | Documento da organização. Geralmente CNPJ. |
| `description` | string | No | Descrição da organização. |
| `populatedSubscription` | any | No | Subscription populada (deprecated, use admin-api). |
| `imageInBase64` | string | No | Imagem do logo em base64. |
| `channel` | enum: WEB_APP, WHATSAPP, SYSTEM... | Yes | Canal de origem da operação |

