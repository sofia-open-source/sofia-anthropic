# POST /core/recurring-financial-records/many

**Resource:** [Core - Recurring Financial Records](../resources/Core-Recurring-Financial-Records.md)
**Cria múltiplos lançamentos financeiros recorrentes.**
**Operation ID:** `coreCreateManyRecurringFinancialRecords`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `populate` | query | string | No |  |

## Request Body

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [CreateManyRecurringFinancialRecordsRequestBodyDto](../schemas/Create/CreateManyRecurringFinancialRecordsRequestBodyDto.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

**Success Response Schema:**

Array of [RecurringFinancialRecordResponseDto](../schemas/Recurring/RecurringFinancialRecordResponseDto.md)

