# POST /core/installment-financial-records/export/sync

**Resource:** [Core - Installment Financial Records Export](../resources/Core-Installment-Financial-Records-Export.md)
**Request synchronous export of installment financial records.**
**Operation ID:** `coreSyncExportInstallmentFinancialRecords`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `textSearchTerm` | query | string | No |  |
| `sortBy` | query | enum: direction, firstInstallmentDate, contact... | No |  |
| `sortOrder` | query | enum: asc, desc | No |  |
| `populate` | query | string | No |  |
| `direction` | query | enum: IN, OUT | No |  |
| `firstInstallmentDateFrom` | query | string | No |  |
| `firstInstallmentDateTo` | query | string | No |  |
| `contact` | query | string | No |  |
| `subcategory` | query | string | No |  |
| `tags` | query | string[] | No |  |
| `competenceDateFrom` | query | string | No |  |
| `competenceDateTo` | query | string | No |  |
| `frequency` | query | enum: MONTHLY, WEEKLY, YEARLY | No |  |
| `completed` | query | boolean | No |  |
| `format` | query | enum: csv, xlsx | No |  |

## Responses

| Status | Description |
|--------|-------------|
| 200 | The id of the job and the file generated. |
| default |  |

**Success Response Schema:**

[SyncExportResourceResponseDto](../schemas/Sync/SyncExportResourceResponseDto.md)

