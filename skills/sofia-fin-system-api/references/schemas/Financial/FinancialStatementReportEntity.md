# FinancialStatementReportEntity

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

#### `data.filters`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `grouping` | enum: daily, monthly, yearly | Yes | Agrupamento temporal |
| `period` | object | No |  |
| `referenceDate` | enum: dueDate, cashDate, competenceDate | Yes | Campo de data a ser utilizado para filtros |
| `completed` | boolean | No | Status de conclusão dos lançamentos |
| `tags` | string[] | No | IDs das tags para filtro |
| `considerInternalTransfers` | boolean | No | Se deve considerar transferências internas nos relatórios |

#### `data.data`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `period` | object | Yes |  |
| `operationalRevenue` | object | Yes |  |
| `operatingExpenses` | object | Yes |  |
| `salesAndMarketingExpenses` | object | Yes |  |
| `administrativeExpenses` | object | Yes |  |
| `personnelExpenses` | object | Yes |  |
| `financialIncome` | object | Yes |  |
| `otherIncome` | object | Yes |  |
| `financialExpenses` | object | Yes |  |
| `investments` | object | Yes |  |
| `incomeTaxExpense` | object | Yes |  |
| `contributionMargin` | object | Yes |  |
| `netIncome` | object | Yes |  |
| `ebitda` | object | Yes |  |

