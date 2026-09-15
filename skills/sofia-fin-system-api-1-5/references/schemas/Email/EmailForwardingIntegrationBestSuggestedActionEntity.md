# EmailForwardingIntegrationBestSuggestedActionEntity

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `operation` | enum: CREATE, UPDATE, CREATE_MANY... | No |  |
| `createData` | object | No |  |
| `updateData` | object | No |  |
| `createManyData` | object | No |  |
| `linkData` | object | No |  |

## Nested Fields

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

### `updateData`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes | Id do lançamento financeiro a ser atualizado. |
| `updateFields` | object | Yes |  |
| `extractedFields` | object | Yes |  |

#### `updateData.updateFields`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `direction` | enum: IN, OUT | No |  |
| `amount` | string | No |  |
| `dueDate` | string | No |  |
| `description` | string | No |  |
| `contact` | string | No |  |
| `subcategory` | string | No |  |
| `account` | string | No |  |
| `concluded` | boolean | No |  |
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

#### `updateData.extractedFields`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `direction` | enum: IN, OUT | No |  |
| `amount` | string | No |  |
| `dueDate` | string | No |  |
| `description` | string | No |  |
| `contact` | string | No |  |
| `subcategory` | string | No |  |
| `account` | string | No |  |
| `concluded` | boolean | No |  |
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

### `createManyData`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `fileId` | string | Yes |  |
| `nRows` | number | Yes |  |

### `linkData`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `financialRecordId` | string | Yes | Id do lançamento financeiro a ser vinculado. |
| `extractedFields` | object | Yes |  |

#### `linkData.extractedFields`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `direction` | enum: IN, OUT | No |  |
| `amount` | string | No |  |
| `dueDate` | string | No |  |
| `description` | string | No |  |
| `contact` | string | No |  |
| `subcategory` | string | No |  |
| `account` | string | No |  |
| `concluded` | boolean | No |  |
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

