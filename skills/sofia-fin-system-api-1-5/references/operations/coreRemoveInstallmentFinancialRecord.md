# DELETE /core/installment-financial-records/{id}

**Resource:** [Core - Installment Financial Records](../resources/Core-Installment-Financial-Records.md)
**Remove an installment financial record.**
**Operation ID:** `coreRemoveInstallmentFinancialRecord`

Remove an installment financial record. Optionally, remove all related non-completed financial records via the query parameter "removeNotCompletedFinancialRecords=true".

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `id` | path | string | Yes | Installment financial record ID. |

## Request Body

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [RemoveInstallmentFinancialRecordRequestBodyDto](../schemas/Remove/RemoveInstallmentFinancialRecordRequestBodyDto.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

