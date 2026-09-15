# POST /core/recurring-financial-records

**Resource:** [Core - Recurring Financial Records](../resources/Core-Recurring-Financial-Records.md)
**Cria um novo lançamento financeiro recorrente.**
**Operation ID:** `coreCreateRecurringFinancialRecord`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `populate` | query | string | No |  |

## Request Body

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [CreateRecurringFinancialRecordRequestBodyDto](../schemas/Create/CreateRecurringFinancialRecordRequestBodyDto.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 |  |
| default |  |

**Success Response Schema:**

[RecurringFinancialRecordResponseDto](../schemas/Recurring/RecurringFinancialRecordResponseDto.md)

