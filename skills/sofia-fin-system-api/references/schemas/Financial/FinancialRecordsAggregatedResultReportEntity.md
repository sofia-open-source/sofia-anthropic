# FinancialRecordsAggregatedResultReportEntity

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `type` | enum: FINANCIAL_RECORDS_AGGREGATE_RESULT_REPORT, FINANCIAL_RECORDS_BY_CONTACTS_REPORT, BANK_ACCOUNTS_CURRENT_BALANCE_REPORT... | Yes |  |
| `generatedAt` |  | Yes |  |
| `data` | object | Yes |  |

## Nested Fields

### `data`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `income` | string | Yes | Sum of all INCOME financial records for the given filter in string format |
| `outcome` | string | Yes | Sum of all OUTCOME financial records for the given filter in string format |
| `resultAbsoluteValue` | string | Yes | Absolute value of the difference between income and outcome |
| `resultDirection` | enum: IN, OUT | Yes | Direction of the result (INCOME if income > outcome, OUTCOME otherwise) |

