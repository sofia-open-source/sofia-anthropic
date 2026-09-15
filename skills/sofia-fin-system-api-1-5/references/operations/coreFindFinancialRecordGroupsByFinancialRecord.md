# GET /core/financial-record-groups/by-financial-record/{financialRecordId}

**Resource:** [Core - Financial Record Groups](../resources/Core-Financial-Record-Groups.md)
**Busca grupos de lançamentos financeiros pelo ID do lançamento.**
**Operation ID:** `coreFindFinancialRecordGroupsByFinancialRecord`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `financialRecordId` | path | string | Yes | Financial record identifier. |

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

**Success Response Schema:**

Array of [FinancialRecordGroupResponseDto](../schemas/Financial/FinancialRecordGroupResponseDto.md)

