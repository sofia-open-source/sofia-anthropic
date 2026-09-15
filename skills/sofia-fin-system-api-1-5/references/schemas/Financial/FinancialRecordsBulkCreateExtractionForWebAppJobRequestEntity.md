# FinancialRecordsBulkCreateExtractionForWebAppJobRequestEntity

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes |  |
| `userId` | string | Yes |  |
| `organizationId` | string | Yes |  |
| `file` | object | Yes |  |
| `createdAt` | string | Yes |  |
| `updatedAt` | string | Yes |  |
| `extractionNotificationDeliveredAt` | string | No |  |

## Nested Fields

### `file`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `url` | string | Yes |  |
| `mimeType` | string | Yes |  |
| `fileName` | string | Yes |  |

