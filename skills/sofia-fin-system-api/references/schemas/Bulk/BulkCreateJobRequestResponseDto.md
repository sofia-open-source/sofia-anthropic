# BulkCreateJobRequestResponseDto

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `fileId` | string | Yes |  |
| `resource` | enum: core_FinancialRecords, core_Contacts, core_BankAccounts... | Yes |  |
| `nRows` | number | Yes |  |
| `channel` | enum: WEB_APP, WHATSAPP, SYSTEM... | Yes | Canal de origem da operação |
| `radarItem` | string | No |  |

