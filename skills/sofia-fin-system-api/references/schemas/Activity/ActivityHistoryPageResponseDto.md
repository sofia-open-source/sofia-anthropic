# ActivityHistoryPageResponseDto

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `items` | object[] | Yes |  |
| `pageInfo` | object | Yes |  |

## Nested Fields

### `items`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes |  |
| `createdAt` | any | Yes |  |
| `action` | enum: CREATE, UPDATE, DELETE... | Yes |  |
| `actionLabel` | string | Yes |  |
| `channel` | enum: WEB_APP, WHATSAPP, SYSTEM... | Yes |  |
| `channelLabel` | string | Yes |  |
| `resource` | enum: core_FinancialRecords, core_Contacts, core_BankAccounts... | Yes |  |
| `resourceLabel` | string | Yes |  |
| `resourceId` | string | Yes |  |
| `requester` | object | Yes |  |
| `displayFields` | object[] | Yes |  |
| `changedFields` | object[] | Yes |  |
| `isBulk` | boolean | Yes |  |
| `bulkJobRequestId` | string | No |  |
| `operation` | enum: CREATE, PARTIAL_UPDATE, REMOVE... | Yes |  |
| `primaryObjectLabel` | string | Yes |  |

#### `items.requester`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes |  |
| `primaryEmail` | string | No |  |
| `firstName` | string | No |  |
| `lastName` | string | No |  |

#### `items.displayFields`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `key` | string | Yes |  |
| `label` | string | Yes |  |
| `value` | string | Yes |  |
| `reference` | object | No |  |

#### `items.changedFields`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `key` | string | Yes |  |
| `label` | string | Yes |  |
| `previousValue` | string | Yes |  |
| `nextValue` | string | Yes |  |

### `pageInfo`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `pageIndex` | number | Yes |  |
| `pageSize` | number | Yes |  |
| `totalPages` | number | Yes |  |
| `totalItems` | number | Yes |  |

