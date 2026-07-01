# BulkRemoveJobRequestResponseDto

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `resource` | enum: core_FinancialRecords, core_Contacts, core_BankAccounts... | Yes |  |
| `ids` | string[] | Yes |  |
| `channel` | enum: WEB_APP, WHATSAPP, SYSTEM... | Yes | Canal de origem da operação |

