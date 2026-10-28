# RecurringFinancialRecordsAggregatedResultResponseDto

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `data` | object | Yes |  |

## Nested Fields

### `data`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `income` | string | Yes | Sum of IN recurring template amounts, in cents. |
| `outcome` | string | Yes | Sum of OUT recurring template amounts, in cents. |
| `resultAbsoluteValue` | string | Yes | Absolute difference between income and outcome, in cents. |
| `resultDirection` | enum: IN, OUT | Yes | IN when income is greater than or equal to outcome, otherwise OUT. |

