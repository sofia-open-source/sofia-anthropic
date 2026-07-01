# POST /core/financial-records/internal-transfer

**Resource:** [Core - Financial Records](../resources/Core-Financial-Records.md)
**Cria uma transferência interna entre contas.**
**Operation ID:** `coreCreateInternalTransfer`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `populate` | query | string | No |  |

## Request Body

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [CreateInternalTransferRequestBodyDto](../schemas/Create/CreateInternalTransferRequestBodyDto.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 |  |
| default |  |

**Success Response Schema:**

Array of [FinancialRecordResponseDto](../schemas/Financial/FinancialRecordResponseDto.md)

