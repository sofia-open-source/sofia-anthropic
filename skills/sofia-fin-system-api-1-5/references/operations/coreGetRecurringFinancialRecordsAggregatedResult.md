# GET /core/recurring-financial-records/aggregated-result

**Resource:** [Core - Recurring Financial Records](../resources/Core-Recurring-Financial-Records.md)
**Sum recurring financial records for the current filters.**
**Operation ID:** `coreGetRecurringFinancialRecordsAggregatedResult`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `pageIndex` | query | number | No |  |
| `pageSize` | query | number | No |  |
| `textSearchTerm` | query | string | No |  |
| `sortBy` | query | enum: direction, firstOccurrenceDate, contact... | No |  |
| `sortOrder` | query | enum: asc, desc | No |  |
| `populate` | query | string | No |  |
| `direction` | query | enum: IN, OUT | No |  |
| `firstOccurrenceDateFrom` | query | string | No |  |
| `firstOccurrenceDateTo` | query | string | No |  |
| `contact` | query | string[] | No | Contact ids to filter by. |
| `subcategory` | query | string[] | No | Subcategory ids to filter by. |
| `amountFrom` | query | any | No |  |
| `amountTo` | query | any | No |  |
| `frequency` | query | enum: WEEKLY, MONTHLY, YEARLY | No | Recurrence frequency to filter by. |
| `tags` | query | any | No |  |
| `repetitionDay` | query | number | No |  |
| `repetitionMonth` | query | number | No |  |
| `onlyBusinessDays` | query | boolean | No |  |
| `automaticCompletion` | query | boolean | No |  |
| `isActive` | query | boolean | No |  |

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

**Success Response Schema:**

[RecurringFinancialRecordsAggregatedResultResponseDto](../schemas/Recurring/RecurringFinancialRecordsAggregatedResultResponseDto.md)

