# BankTransactionsBestSuggestedActionEntity

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `operation` | enum: CREATE, LINK | Yes |  |
| `linkData` | object | No |  |
| `createData` | object | Yes |  |

## Nested Fields

### `linkData`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `financialRecordId` | string | Yes |  |

### `createData`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `financialRecord` | object | Yes |  |

#### `createData.financialRecord`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `direction` | enum: IN, OUT | Yes |  |
| `amount` | string | Yes |  |
| `dueDate` | string | Yes |  |
| `description` | string | Yes |  |
| `contact` | string | Yes |  |
| `subcategory` | string | Yes |  |
| `account` | string | No |  |
| `concluded` | boolean | Yes |  |
| `cashDate` | string | No |  |
| `competenceDate` | string | No |  |
| `discount` | string | No |  |
| `finesAndInterests` | string | No |  |
| `boletoCode` | string | No |  |
| `pixCode` | string | No |  |
| `pixKey` | string | No |  |
| `contactHint` | string | No |  |
| `subcategoryHint` | string | No |  |
| `reason` | string | No |  |

