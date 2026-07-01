# GET /core/recurring-financial-records/{id}

**Resource:** [Core - Recurring Financial Records](../resources/Core-Recurring-Financial-Records.md)
**Busca um lançamento financeiro recorrente pelo ID.**
**Operation ID:** `coreFindByIdRecurringFinancialRecord`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `id` | path | string | Yes | Recurring financial record ID. |
| `populate` | query | string | No |  |

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

**Success Response Schema:**

[RecurringFinancialRecordResponseDto](../schemas/Recurring/RecurringFinancialRecordResponseDto.md)

