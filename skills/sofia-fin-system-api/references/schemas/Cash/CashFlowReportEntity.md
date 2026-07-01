# CashFlowReportEntity

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `type` | string | Yes |  |
| `generatedAt` |  | Yes |  |
| `data` | object | Yes |  |

## Nested Fields

### `data`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `filters` | object | Yes |  |
| `data` | object[] | Yes |  |
| `summary` | object | Yes |  |

#### `data.filters`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `grouping` | enum: daily, monthly, yearly | Yes | Agrupamento temporal |
| `period` | object | No | Período para filtrar |
| `bankAccounts` | string[] | No | IDs das contas bancárias para filtrar |
| `reconciled` | boolean[] | No | Filtro de status de conciliação |
| `tags` | string[] | No | IDs das tags para filtrar |

#### `data.data`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `period` | object | Yes | Período |
| `openingBalance` | any | No | Saldo no início do período |
| `totalIncome` | any | No | Soma das transações de ENTRADA no período |
| `totalOutcome` | any | No | Soma das transações de SAÍDA no período |
| `openIncome` | any | No | Parte de totalIncome ainda em aberto (não concluído) |
| `openOutcome` | any | No | Parte de totalOutcome ainda em aberto (não concluído) |
| `closingBalance` | any | No | Saldo no fim do período |
| `isProjected` | boolean | Yes | Indica se o período é projetado (futuro) ou histórico |
| `insertedAccounts` | object[] | Yes | Contas que foram introduzidas neste período |

#### `data.summary`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `totalPeriods` | number | Yes | Número de períodos no relatório |
| `overallStartBalance` | any | No | Saldo no início do primeiro período |
| `overallEndBalance` | any | No | Saldo no fim do último período |
| `totalIncome` | any | No | Total de entradas em todos os períodos |
| `totalOutcome` | any | No | Total de saídas em todos os períodos |
| `netCashFlow` | any | No | Fluxo de caixa líquido (total de entradas - total de saídas) |
| `includeProjected` | boolean | Yes | Incluir projeções |

