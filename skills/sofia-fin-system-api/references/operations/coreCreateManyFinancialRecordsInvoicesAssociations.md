# POST /core/financial-records-invoices-associations/many

**Resource:** [Core - Financial records invoices associations](../resources/Core-Financial-records-invoices-associations.md)
**Links multiple financial records to a single invoice.**
**Operation ID:** `coreCreateManyFinancialRecordsInvoicesAssociations`

## Request Body

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [CreateManyFinancialRecordsInvoicesAssociationsRequestBodyDto](../schemas/Create/CreateManyFinancialRecordsInvoicesAssociationsRequestBodyDto.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 |  |
| default |  |

**Success Response Schema:**

Array of [FinancialRecordsInvoicesAssociationEntity](../schemas/Financial/FinancialRecordsInvoicesAssociationEntity.md)

