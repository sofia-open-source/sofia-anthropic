# GET /core/financial-records-invoices-associations

**Resource:** [Core - Financial records invoices associations](../resources/Core-Financial-records-invoices-associations.md)
**Lists invoice–financial record associations for the organization.**
**Operation ID:** `coreFindAllFinancialRecordsInvoicesAssociations`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `pageIndex` | query | number | No |  |
| `pageSize` | query | number | No |  |
| `financialRecordId` | query | string | No |  |
| `invoiceId` | query | string | No |  |
| `populate` | query | string | No | Comma-separated paths: financialRecord, invoice. |

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

**Success Response Schema:**

[FinancialRecordsInvoicesAssociationsPageEntity](../schemas/Financial/FinancialRecordsInvoicesAssociationsPageEntity.md)

