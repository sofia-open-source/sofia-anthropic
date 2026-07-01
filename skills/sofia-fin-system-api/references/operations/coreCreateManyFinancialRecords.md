# POST /core/financial-records/many

**Resource:** [Core - Financial Records](../resources/Core-Financial-Records.md)
**Cria múltiplos lançamentos financeiros.**
**Operation ID:** `coreCreateManyFinancialRecords`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `populate` | query | string | No |  |

## Request Body

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [CreateManyFinancialRecordsRequestBodyDto](../schemas/Create/CreateManyFinancialRecordsRequestBodyDto.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

**Success Response Schema:**

Array of [FinancialRecordResponseDto](../schemas/Financial/FinancialRecordResponseDto.md)

