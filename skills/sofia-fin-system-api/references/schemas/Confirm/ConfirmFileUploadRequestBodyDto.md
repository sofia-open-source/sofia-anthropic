# ConfirmFileUploadRequestBodyDto

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes | Identificador do arquivo. |
| `size` | number | No | Tamanho do arquivo em bytes. |
| `status` | enum: FAILED, COMPLETED | Yes |  |
| `caption` | string | No | Legenda do arquivo. |
| `deletedAt` | any | No | Data de exclusão do arquivo. |
| `channel` | enum: WEB_APP, WHATSAPP, SYSTEM... | Yes | Canal de origem da operação |

