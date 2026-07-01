# ProjectedCashFlowEntity

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `periods` | object[] | Yes | Lista de períodos com fluxo de caixa projetado |

## Nested Fields

### `periods`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `period` | object | Yes |  |
| `openingBalance` | string | Yes | Saldo inicial do período |
| `totalIncome` | string | Yes | Soma de transações de entrada no período |
| `totalOutcome` | string | Yes | Soma de transações de saída no período |
| `closingBalance` | string | Yes | Saldo final do período |
| `isProjected` | boolean | Yes | Indica se o período é projetado (futuro) ou histórico |

#### `periods.period`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `start` | string | No | Period start date |
| `end` | string | No | Period end date |

