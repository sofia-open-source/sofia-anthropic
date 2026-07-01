# POST /core/recurring-financial-records/export

**Resource:** [Core - Recurring Financial Records Export](../resources/Core-Recurring-Financial-Records-Export.md)
**Solicita a exportação dos lançamentos recorrentes.**
**Operation ID:** `coreExportRecurringFinancialRecords`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `textSearchTerm` | query | string | No |  |
| `sortBy` | query | enum: direction, firstOccurrenceDate, contact... | No |  |
| `sortOrder` | query | enum: asc, desc | No |  |
| `populate` | query | string | No |  |
| `direction` | query | enum: IN, OUT | No |  |
| `firstOccurrenceDateFrom` | query | string | No |  |
| `firstOccurrenceDateTo` | query | string | No |  |
| `contact` | query | string | No |  |
| `subcategory` | query | string | No |  |
| `amountFrom` | query | any | No |  |
| `amountTo` | query | any | No |  |
| `tags` | query | any | No |  |
| `repetitionDay` | query | number | No |  |
| `repetitionMonth` | query | number | No |  |
| `onlyBusinessDays` | query | boolean | No |  |
| `automaticCompletion` | query | boolean | No |  |
| `isActive` | query | boolean | No |  |
| `format` | query | enum: csv, xlsx | Yes |  |

## Responses

| Status | Description |
|--------|-------------|
| 200 | The id of the pending resource job. |
| default |  |

**Success Response Schema:**

[ExportRecurringFinancialRecordsResponseDto](../schemas/Export/ExportRecurringFinancialRecordsResponseDto.md)

