# PartialUpdateTagRequestBodyDto

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `name` | string | No | Tag name. |
| `searchScore` | number | No | Text search score. |
| `importedAt` | any | No | Tag import date. |
| `importedBy` | string | No | Tag import source. |
| `externalId` | string | No | External identifier of the tag. |
| `channel` | enum: WEB_APP, WHATSAPP, SYSTEM... | Yes | Canal de origem da operação |

