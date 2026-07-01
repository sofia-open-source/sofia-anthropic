# PATCH /core/financial-records/{id}

**Resource:** [Core - Financial Records](../resources/Core-Financial-Records.md)
**Atualiza parcialmente um lançamento financeiro.**
**Operation ID:** `corePartialUpdateFinancialRecord`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `id` | path | string | Yes | Financial record identifier. |
| `populate` | query | string | No |  |

## Request Body

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [PartialUpdateFinancialRecordRequestBodyDto](../schemas/Partial/PartialUpdateFinancialRecordRequestBodyDto.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

**Success Response Schema:**

[FinancialRecordResponseDto](../schemas/Financial/FinancialRecordResponseDto.md)

