# FinancialMeasuresReportEntity

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
| `filters` | object | Yes | Filtros aplicados |
| `data` | object | Yes | Medidas financeiras calculadas |

#### `data.filters`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `account` | string[] | No | Lista de IDs de contas bancárias para filtrar. |
| `amountFrom` | any | No | Valor do lançamento mínimo. |
| `amountTo` | any | No | Valor do lançamento máximo. |
| `amountType` | enum: base, final | No |  |
| `cashDateFrom` | string | No |  |
| `cashDateTo` | string | No |  |
| `competenceDateFrom` | string | No |  |
| `competenceDateTo` | string | No |  |
| `completed` | boolean | No |  |
| `contact` | string[] | No | Lista de IDs de contatos para filtrar. |
| `createdAtFrom` | any | No |  |
| `createdAtTo` | any | No |  |
| `direction` | enum: IN, OUT | No |  |
| `dueDateFrom` | string | No |  |
| `dueDateTo` | string | No |  |
| `queryId` | string | No | ID da query a ser aplicada à consulta. |
| `finalAmountFrom` | any | No | Valor final do lançamento mínimo. |
| `finalAmountTo` | any | No | Valor final do lançamento máximo. |
| `installmentFinancialRecord` | string[] | No | Lista de IDs de parcelas para filtrar. |
| `recurringFinancialRecord` | string[] | No | Lista de IDs de recorrências para filtrar. |
| `reconciled` | boolean | No |  |
| `subcategory` | string[] | No | Lista de IDs de subcategorias para filtrar. |
| `tags` | string[] | No | Lista de IDs de tags para filtrar. |
| `includeNoAccount` | boolean | No | When true, also matches financial records with no linked bank account (null or missing). With account IDs, matches selected accounts OR no account; with no account IDs, matches only records without a linked account. |
| `includeNoTags` | boolean | No | When true, also matches financial records with no tags (empty or missing). With tag IDs, matches selected tags OR no tags; with no tag IDs, matches only records without tags. |
| `considerInternalTransfers` | boolean | No | Se deve considerar transferências internas nos relatórios. |

#### `data.data`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `contributionMargin` | string | Yes | Margem de contribuição em formato string |
| `ebitda` | string | Yes | EBITDA (Earnings Before Interest, Taxes, Depreciation and Amortization) em formato string |
| `netIncome` | string | Yes | Lucro líquido em formato string |
| `breakEvenPoint` | string | Yes | Ponto de equilíbrio em formato string |
| `averageTicket` | string | Yes | Ticket médio em formato string |

