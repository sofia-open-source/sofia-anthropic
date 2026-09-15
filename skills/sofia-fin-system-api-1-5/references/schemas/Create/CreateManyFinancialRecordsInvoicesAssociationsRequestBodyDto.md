# CreateManyFinancialRecordsInvoicesAssociationsRequestBodyDto

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `channel` | enum: WEB_APP, WHATSAPP, SYSTEM... | No | Operation channel. |
| `invoiceId` | string | Yes | Invoice id. |
| `financialRecordIds` | string[] | Yes | Financial record ids to link. |

