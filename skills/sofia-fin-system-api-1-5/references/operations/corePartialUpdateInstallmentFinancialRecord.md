# PATCH /core/installment-financial-records/{id}

**Resource:** [Core - Installment Financial Records](../resources/Core-Installment-Financial-Records.md)
**Partially update an installment financial record.**
**Operation ID:** `corePartialUpdateInstallmentFinancialRecord`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `id` | path | string | Yes | Installment financial record ID. |
| `populate` | query | string | No |  |

## Request Body

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [PartialUpdateInstallmentFinancialRecordRequestBodyDto](../schemas/Partial/PartialUpdateInstallmentFinancialRecordRequestBodyDto.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

**Success Response Schema:**

[InstallmentFinancialRecordResponseDto](../schemas/Installment/InstallmentFinancialRecordResponseDto.md)

