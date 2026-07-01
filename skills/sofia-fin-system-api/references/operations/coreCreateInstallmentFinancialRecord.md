# POST /core/installment-financial-records

**Resource:** [Core - Installment Financial Records](../resources/Core-Installment-Financial-Records.md)
**Create a new installment financial record.**
**Operation ID:** `coreCreateInstallmentFinancialRecord`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `populate` | query | string | No |  |

## Request Body

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [CreateInstallmentFinancialRecordRequestBodyDto](../schemas/Create/CreateInstallmentFinancialRecordRequestBodyDto.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 |  |
| default |  |

**Success Response Schema:**

[InstallmentFinancialRecordResponseDto](../schemas/Installment/InstallmentFinancialRecordResponseDto.md)

