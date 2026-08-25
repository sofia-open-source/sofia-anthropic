# InvoiceEventResponseDto

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes |  |
| `organization` | string | Yes |  |
| `ownerOrganization` | string | Yes |  |
| `resourceId` | string | Yes |  |
| `channel` | enum: WEB_APP, WHATSAPP, SYSTEM... | Yes | Canal de origem da operação |
| `resource` | enum: core_FinancialRecords, core_Contacts, core_BankAccounts... | Yes |  |
| `requester` |  | Yes |  |
| `request` |  | Yes |  |
| `previousResult` | any | No |  |
| `result` |  | No |  |
| `context` | object | No |  |
| `createdAt` |  | Yes |  |
| `updatedAt` |  | Yes |  |
| `operation` | enum: CREATE, UPDATE, CANCEL... | Yes | Invoice event operation label for the API (differs from stored EVENT_OPERATIONS where applicable). |

## Nested Fields

### `context`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `bulkJobRequestId` | string | No |  |
| `bulkOperation` | enum: CREATE, PARTIAL_UPDATE, REMOVE... | No |  |

