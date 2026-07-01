# UnlinkFinancialRecordsRequestBodyDto

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `unlinkType` | enum: ALL, SPECIFIC | Yes | Tipo de desvinculação. |
| `financialRecordIds` | string[] | No | IDs dos registros financeiros a serem desvinculados (obrigatório se unlinkType for SPECIFIC). |
| `channel` | enum: WEB_APP, WHATSAPP, SYSTEM... | Yes | Canal de origem da operação |

