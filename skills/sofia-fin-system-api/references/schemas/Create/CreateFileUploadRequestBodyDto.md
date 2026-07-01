# CreateFileUploadRequestBodyDto

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `originalFileName` | string | Yes | Nome original do arquivo. |
| `mimeType` | string | Yes | Tipo MIME do arquivo. |
| `size` | number | Yes | Tamanho do arquivo em bytes. |
| `fileType` | enum: DEFAULT, FINANCIAL_RECORD, EXPORT... | Yes | Tipo do arquivo. |
| `caption` | string | No | Legenda do arquivo. |
| `channel` | enum: WEB_APP, WHATSAPP, SYSTEM... | Yes | Canal de origem da operação |

