# GET /core/recurring-financial-records

**Resource:** [Core - Recurring Financial Records](../resources/Core-Recurring-Financial-Records.md)
**Busca todos os lançamentos financeiros recorrentes.**
**Operation ID:** `coreFindAllRecurringFinancialRecords`

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

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

**Success Response Schema:**

[RecurringFinancialRecordsPageResponseDto](../schemas/Recurring/RecurringFinancialRecordsPageResponseDto.md)

