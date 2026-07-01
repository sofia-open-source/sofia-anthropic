# GET /core/financial-records-invoices-associations/{id}

**Resource:** [Core - Financial records invoices associations](../resources/Core-Financial-records-invoices-associations.md)
**Gets an association by id.**
**Operation ID:** `coreFindFinancialRecordsInvoicesAssociationById`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `id` | path | string | Yes |  |
| `populate` | query | string | No | Comma-separated paths: financialRecord, invoice. |

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

**Success Response Schema:**

[FinancialRecordsInvoicesAssociationEntity](../schemas/Financial/FinancialRecordsInvoicesAssociationEntity.md)

