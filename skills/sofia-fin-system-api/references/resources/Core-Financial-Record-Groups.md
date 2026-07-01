# Core - Financial Record Groups

Groups that tie related financial records together (e.g. split payments or linked entries). Create a group, find the group containing a given financial-record id, and delete a group. No list-all or partial-update endpoints. Groups help the UI and analytics treat multiple records as one logical transaction.

## Operations

| Method | Path | Summary | Details |
|--------|------|---------|----------|
| POST | `/core/financial-record-groups` | Cria um grupo de lançamentos financeiros. | [View](../operations/coreCreateFinancialRecordGroup.md) |
| GET | `/core/financial-record-groups/by-financial-record/{financialRecordId}` | Busca grupos de lançamentos financeiros pelo ID do lançamento. | [View](../operations/coreFindFinancialRecordGroupsByFinancialRecord.md) |
| DELETE | `/core/financial-record-groups/{financialRecordGroupId}` | Remove um grupo de lançamentos financeiros. | [View](../operations/coreRemoveFinancialRecordGroup.md) |
