# DELETE /core/recurring-financial-records/{id}

**Resource:** [Core - Recurring Financial Records](../resources/Core-Recurring-Financial-Records.md)
**Remove um lançamento financeiro recorrente.**
**Operation ID:** `coreRemoveRecurringFinancialRecord`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `id` | path | string | Yes | Recurring financial record ID. |

## Request Body

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [RemoveRecurringFinancialRecordRequestBodyDto](../schemas/Remove/RemoveRecurringFinancialRecordRequestBodyDto.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

