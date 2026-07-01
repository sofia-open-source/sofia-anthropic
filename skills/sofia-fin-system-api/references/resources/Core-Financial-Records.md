# Core - Financial Records

The main resource of the system, represents an amount (paid/received/to be payed/to be received) for the organization on the system. It is used in the majority of all reports and is linked to many other resources like contacts, tags, bank transactions, radar items etc.

## Operations

| Method | Path | Summary | Details |
|--------|------|---------|----------|
| GET | `/core/financial-records` | Busca todos os lançamentos financeiros. | [View](../operations/coreFindAllFinancialRecords.md) |
| POST | `/core/financial-records` | Cria um novo lançamento financeiro. | [View](../operations/coreCreateFinancialRecord.md) |
| POST | `/core/financial-records/internal-transfer` | Cria uma transferência interna entre contas. | [View](../operations/coreCreateInternalTransfer.md) |
| POST | `/core/financial-records/many` | Cria múltiplos lançamentos financeiros. | [View](../operations/coreCreateManyFinancialRecords.md) |
| PATCH | `/core/financial-records/many` | Atualiza parcialmente múltiplos lançamentos financeiros. | [View](../operations/corePartialUpdateManyFinancialRecords.md) |
| GET | `/core/financial-records/{id}` | Busca um lançamento financeiro pelo identificador. | [View](../operations/coreFindByIdFinancialRecord.md) |
| DELETE | `/core/financial-records/{id}` | Remove um lançamento financeiro. | [View](../operations/coreRemoveFinancialRecord.md) |
| PATCH | `/core/financial-records/{id}` | Atualiza parcialmente um lançamento financeiro. | [View](../operations/corePartialUpdateFinancialRecord.md) |
| POST | `/core/financial-records/{id}/unlink-all-radar-items` | Desvincula todos os radar items de um lançamento financeiro | [View](../operations/coreUnlinkAllRadarItemsFromFinancialRecord.md) |
| GET | `/core/financial-records/reports/pdf/table` | Gera exportação em PDF dos lançamentos financeiros no formato de tabela. | [View](../operations/coreGeneratePdfTableExportFinancialRecords.md) |
| GET | `/core/financial-records/reports/pdf/list` | Gera exportação em PDF dos lançamentos financeiros no formato de lista. | [View](../operations/coreGeneratePdfListExportFinancialRecords.md) |
