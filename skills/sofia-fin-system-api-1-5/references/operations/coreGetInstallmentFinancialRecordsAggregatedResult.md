# GET /core/installment-financial-records/aggregated-result

**Resource:** [Core - Installment Financial Records](../resources/Core-Installment-Financial-Records.md)
**Sum installment financial records for the current filters.**
**Operation ID:** `coreGetInstallmentFinancialRecordsAggregatedResult`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `pageIndex` | query | number | No |  |
| `pageSize` | query | number | No |  |
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

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

**Success Response Schema:**

[InstallmentFinancialRecordsAggregatedResultResponseDto](../schemas/Installment/InstallmentFinancialRecordsAggregatedResultResponseDto.md)

