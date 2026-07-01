# GET /core/installment-financial-records/{id}

**Resource:** [Core - Installment Financial Records](../resources/Core-Installment-Financial-Records.md)
**Find an installment financial record by ID.**
**Operation ID:** `coreFindByIdInstallmentFinancialRecord`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `id` | path | string | Yes | Installment financial record ID. |
| `populate` | query | string | No |  |

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

**Success Response Schema:**

[InstallmentFinancialRecordResponseDto](../schemas/Installment/InstallmentFinancialRecordResponseDto.md)

