# OfxImportRequestBodyDto

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `signedUrl` | string | Yes | URL assinada para download do arquivo OFX. |
| `fileName` | string | Yes | Nome do arquivo OFX. |
| `bankAccount` | string | Yes | ID da conta bancária. |
| `channel` | enum: WEB_APP, WHATSAPP, SYSTEM... | Yes | Canal de origem da operação |

