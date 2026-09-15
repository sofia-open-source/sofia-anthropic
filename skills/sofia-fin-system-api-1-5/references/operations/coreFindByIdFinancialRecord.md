# GET /core/financial-records/{id}

**Resource:** [Core - Financial Records](../resources/Core-Financial-Records.md)
**Busca um lançamento financeiro pelo identificador.**
**Operation ID:** `coreFindByIdFinancialRecord`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `id` | path | string | Yes | Financial record identifier. |
| `populate` | query | string | No |  |

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

**Success Response Schema:**

[FinancialRecordResponseDto](../schemas/Financial/FinancialRecordResponseDto.md)

