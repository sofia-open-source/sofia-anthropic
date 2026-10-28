# POST /core/installment-financial-records/export

**Resource:** [Core - Installment Financial Records Export](../resources/Core-Installment-Financial-Records-Export.md)
**Request export of installment financial records.**
**Operation ID:** `coreExportInstallmentFinancialRecords`

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
| `contact` | query | string[] | No | Contact ids to filter by. |
| `subcategory` | query | string[] | No | Subcategory ids to filter by. |
| `amountFrom` | query | any | No | Minimum installment plan amount, in cents. |
| `amountTo` | query | any | No | Maximum installment plan amount, in cents. |
| `tags` | query | string[] | No |  |
| `competenceDateFrom` | query | string | No |  |
| `competenceDateTo` | query | string | No |  |
| `frequency` | query | enum: MONTHLY, WEEKLY, YEARLY | No |  |
| `completed` | query | boolean | No |  |
| `format` | query | enum: csv, xlsx | No |  |

## Responses

| Status | Description |
|--------|-------------|
| 200 | The id of the pending resource job. |
| default |  |

**Success Response Schema:**

[ExportInstallmentFinancialRecordsResponseDto](../schemas/Export/ExportInstallmentFinancialRecordsResponseDto.md)

