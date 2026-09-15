# DELETE /core/financial-records/{id}

**Resource:** [Core - Financial Records](../resources/Core-Financial-Records.md)
**Remove um lançamento financeiro.**
**Operation ID:** `coreRemoveFinancialRecord`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `id` | path | string | Yes | Financial record identifier. |

## Request Body

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [RemoveFinancialRecordRequestBodyDto](../schemas/Remove/RemoveFinancialRecordRequestBodyDto.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

