# FinancialResultCompositionReportEntity

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
| `data` | object[] | Yes | Composição do resultado financeiro |
| `totalRevenue` | string | Yes | Receita operacional total em formato string |
| `filters` | object | Yes | Filtros aplicados |

#### `data.data`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `label` | string | Yes | Nome da categoria |
| `amount` | string | Yes | Valor da categoria em formato string |
| `percentage` | number | Yes | Percentual relativo à receita operacional |
| `direction` | enum: IN, OUT | Yes | Direção do valor (entrada ou saída) |

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

