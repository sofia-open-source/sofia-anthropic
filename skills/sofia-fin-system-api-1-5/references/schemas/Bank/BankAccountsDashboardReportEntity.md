# BankAccountsDashboardReportEntity

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
| `bankAccounts` | object[] | Yes |  |

#### `data.bankAccounts`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes | Bank account ID |
| `name` | string | Yes | Bank account name |
| `type` | string | Yes | Bank account type |
| `provider` | string | No | Bank account provider |
| `recordCount` | number | Yes | Total financial records |
| `totalIncome` | string | Yes | Total income |
| `totalOutcome` | string | Yes | Total outcome |
| `balance` | string | Yes | Current bank account balance |

