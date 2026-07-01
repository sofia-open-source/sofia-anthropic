# DELETE /core/financial-record-groups/{financialRecordGroupId}

**Resource:** [Core - Financial Record Groups](../resources/Core-Financial-Record-Groups.md)
**Remove um grupo de lançamentos financeiros.**
**Operation ID:** `coreRemoveFinancialRecordGroup`

Remove only the grouping, keeping the original financial records.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `financialRecordGroupId` | path | string | Yes | Financial record group identifier. |

## Responses

| Status | Description |
|--------|-------------|
| 200 | Grupo removido com sucesso. |
| default |  |

