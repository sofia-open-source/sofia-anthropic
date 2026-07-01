# BulkUpdateJobRequestResponseDto

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `ids` | string[] | Yes |  |
| `payload` | object | Yes |  |
| `resource` | enum: core_FinancialRecords, core_Contacts, core_BankAccounts... | Yes |  |
| `channel` | enum: WEB_APP, WHATSAPP, SYSTEM... | Yes | Canal de origem da operação |
| `radarItem` | string | No |  |

