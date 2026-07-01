# PATCH /core/recurring-financial-records/{id}

**Resource:** [Core - Recurring Financial Records](../resources/Core-Recurring-Financial-Records.md)
**Atualiza parcialmente um lançamento financeiro recorrente.**
**Operation ID:** `corePartialUpdateRecurringFinancialRecord`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `id` | path | string | Yes | Recurring financial record ID. |
| `populate` | query | string | No |  |

## Request Body

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [PartialUpdateRecurringFinancialRecordRequestBodyDto](../schemas/Partial/PartialUpdateRecurringFinancialRecordRequestBodyDto.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

**Success Response Schema:**

[RecurringFinancialRecordResponseDto](../schemas/Recurring/RecurringFinancialRecordResponseDto.md)

