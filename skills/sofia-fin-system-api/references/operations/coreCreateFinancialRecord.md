# POST /core/financial-records

**Resource:** [Core - Financial Records](../resources/Core-Financial-Records.md)
**Cria um novo lançamento financeiro.**
**Operation ID:** `coreCreateFinancialRecord`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `populate` | query | string | No |  |

## Request Body

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [CreateFinancialRecordRequestBodyDto](../schemas/Create/CreateFinancialRecordRequestBodyDto.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 |  |
| default |  |

**Success Response Schema:**

[FinancialRecordResponseDto](../schemas/Financial/FinancialRecordResponseDto.md)

