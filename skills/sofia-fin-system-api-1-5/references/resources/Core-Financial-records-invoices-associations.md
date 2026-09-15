# Core - Financial records invoices associations

Explicit links between financial records and issued invoices (NFSe). Create one association, create many in batch, paginated list with filters, find-by-id, and delete. There is no update endpoint; remove and recreate to change a link. Associations support reporting and audit trails where a payment or revenue line ties to a fiscal document.

## Operations

| Method | Path | Summary | Details |
|--------|------|---------|----------|
| GET | `/core/financial-records-invoices-associations` | Lists invoice–financial record associations for the organization. | [View](../operations/coreFindAllFinancialRecordsInvoicesAssociations.md) |
| POST | `/core/financial-records-invoices-associations` | Links a financial record to an invoice. | [View](../operations/coreCreateFinancialRecordsInvoicesAssociation.md) |
| POST | `/core/financial-records-invoices-associations/many` | Links multiple financial records to a single invoice. | [View](../operations/coreCreateManyFinancialRecordsInvoicesAssociations.md) |
| GET | `/core/financial-records-invoices-associations/{id}` | Gets an association by id. | [View](../operations/coreFindFinancialRecordsInvoicesAssociationById.md) |
| DELETE | `/core/financial-records-invoices-associations/{id}` | Removes an association between a financial record and an invoice. | [View](../operations/coreRemoveFinancialRecordsInvoicesAssociation.md) |
