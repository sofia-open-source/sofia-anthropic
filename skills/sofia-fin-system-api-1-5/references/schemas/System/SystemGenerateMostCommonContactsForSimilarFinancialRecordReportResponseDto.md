# SystemGenerateMostCommonContactsForSimilarFinancialRecordReportResponseDto

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `subcategories` | object | Yes | Objeto contendo três listas de subcategorias ordenadas por diferentes métricas |
| `allFinancialRecordsTotalSearchScore` | number | Yes | Soma total dos scores de todos os lançamentos encontrados |
| `nSimilarFinancialRecordsConsidered` | number | Yes | Número de lançamentos similares considerados |
| `nTotalFinancialRecords` | number | Yes | Número total de lançamentos financeiros da organização |

## Nested Fields

### `subcategories`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `topByTotalSearchScore` | object[] | Yes | Top subcategorias por soma total do search score |
| `topByMeanSearchScore` | object[] | Yes | Top subcategorias por média do search score |
| `topByRelativeFrequency` | object[] | Yes | Top subcategorias por frequência relativa |

#### `subcategories.topByTotalSearchScore`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes | Identificador da subcategoria |
| `name` | string | Yes | Nome da subcategoria |
| `description` | string | Yes | Descrição da subcategoria |
| `categoryName` | string | Yes | Nome da categoria |
| `direction` | enum: IN, OUT | Yes | Direção da categoria |
| `totalSearchScore` | number | Yes | Soma total do searchScore para aquela subcategoria |
| `meanSearchScore` | number | Yes | Valor médio do searchScore para aquela subcategoria |
| `count` | number | Yes | Número de lançamentos financeiros associados a esta subcategoria |
| `relativeFrequency` | number | Yes | Número de vezes que aquela subcategoria apareceu dividido pelo número total de lançamentos encontrados |

#### `subcategories.topByMeanSearchScore`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes | Identificador da subcategoria |
| `name` | string | Yes | Nome da subcategoria |
| `description` | string | Yes | Descrição da subcategoria |
| `categoryName` | string | Yes | Nome da categoria |
| `direction` | enum: IN, OUT | Yes | Direção da categoria |
| `totalSearchScore` | number | Yes | Soma total do searchScore para aquela subcategoria |
| `meanSearchScore` | number | Yes | Valor médio do searchScore para aquela subcategoria |
| `count` | number | Yes | Número de lançamentos financeiros associados a esta subcategoria |
| `relativeFrequency` | number | Yes | Número de vezes que aquela subcategoria apareceu dividido pelo número total de lançamentos encontrados |

#### `subcategories.topByRelativeFrequency`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes | Identificador da subcategoria |
| `name` | string | Yes | Nome da subcategoria |
| `description` | string | Yes | Descrição da subcategoria |
| `categoryName` | string | Yes | Nome da categoria |
| `direction` | enum: IN, OUT | Yes | Direção da categoria |
| `totalSearchScore` | number | Yes | Soma total do searchScore para aquela subcategoria |
| `meanSearchScore` | number | Yes | Valor médio do searchScore para aquela subcategoria |
| `count` | number | Yes | Número de lançamentos financeiros associados a esta subcategoria |
| `relativeFrequency` | number | Yes | Número de vezes que aquela subcategoria apareceu dividido pelo número total de lançamentos encontrados |

