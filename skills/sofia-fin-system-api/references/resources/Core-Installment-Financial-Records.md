# Core - Installment Financial Records

Parent financial records split into installments, each with its own due date and amount. Supports create, paginated list, find-by-id, partial update, and delete on /core/installment-financial-records. List endpoints accept filters and populate related data. Installments are the template from which individual financial-record lines can be generated over time.

## Operations

| Method | Path | Summary | Details |
|--------|------|---------|----------|
| GET | `/core/installment-financial-records` | Find all installment financial records. | [View](../operations/coreFindAllInstallmentFinancialRecords.md) |
| POST | `/core/installment-financial-records` | Create a new installment financial record. | [View](../operations/coreCreateInstallmentFinancialRecord.md) |
| GET | `/core/installment-financial-records/{id}` | Find an installment financial record by ID. | [View](../operations/coreFindByIdInstallmentFinancialRecord.md) |
| DELETE | `/core/installment-financial-records/{id}` | Remove an installment financial record. | [View](../operations/coreRemoveInstallmentFinancialRecord.md) |
| PATCH | `/core/installment-financial-records/{id}` | Partially update an installment financial record. | [View](../operations/corePartialUpdateInstallmentFinancialRecord.md) |
