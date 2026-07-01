# PATCH /core/financial-records/many

**Resource:** [Core - Financial Records](../resources/Core-Financial-Records.md)
**Atualiza parcialmente múltiplos lançamentos financeiros.**
**Operation ID:** `corePartialUpdateManyFinancialRecords`

## Request Body

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [PartialUpdateManyFinancialRecordsRequestBodyDto](../schemas/Partial/PartialUpdateManyFinancialRecordsRequestBodyDto.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

**Success Response Schema:**

Array of [FinancialRecordResponseDto](../schemas/Financial/FinancialRecordResponseDto.md)

