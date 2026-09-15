# Core - Recurring Financial Records

Recurrence templates that define rules for seeding future financial records (frequency, amounts, contacts, categories, etc.). Full CRUD plus POST /many for batch creation of templates. Internal scheduler and queue workers activate templates and materialize due occurrences into financial records. Active templates drive automated bookkeeping without manual entry for each period.

## Operations

| Method | Path | Summary | Details |
|--------|------|---------|----------|
| GET | `/core/recurring-financial-records` | Busca todos os lançamentos financeiros recorrentes. | [View](../operations/coreFindAllRecurringFinancialRecords.md) |
| POST | `/core/recurring-financial-records` | Cria um novo lançamento financeiro recorrente. | [View](../operations/coreCreateRecurringFinancialRecord.md) |
| POST | `/core/recurring-financial-records/many` | Cria múltiplos lançamentos financeiros recorrentes. | [View](../operations/coreCreateManyRecurringFinancialRecords.md) |
| GET | `/core/recurring-financial-records/{id}` | Busca um lançamento financeiro recorrente pelo ID. | [View](../operations/coreFindByIdRecurringFinancialRecord.md) |
| DELETE | `/core/recurring-financial-records/{id}` | Remove um lançamento financeiro recorrente. | [View](../operations/coreRemoveRecurringFinancialRecord.md) |
| PATCH | `/core/recurring-financial-records/{id}` | Atualiza parcialmente um lançamento financeiro recorrente. | [View](../operations/corePartialUpdateRecurringFinancialRecord.md) |
