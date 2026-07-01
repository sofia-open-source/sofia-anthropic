# GET /analytics/cash-flow/report

**Resource:** [Analytics - Cash Flow Reports](../resources/Analytics-Cash-Flow-Reports.md)
**Generate a cash flow report.**
**Operation ID:** `analyticsGenerateCashFlowReport`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `grouping` | query | enum: daily, monthly, yearly | No | Período de agrupamento para o relatório de fluxo de caixa |
| `queryId` | query | string | No | Query ID to apply to the request. |
| `mode` | query | enum: REALIZED, PROJECTED, ALL | No | Unified completion filter. `REALIZED` returns only completed (by cash date), `PROJECTED` only open (by due date), `ALL` both. When omitted we fall back to `completed`/`includeProjected` (legacy). |
| `includeProjected` | query | boolean | No | DEPRECATED: use `mode`. Include projected transactions (legacy). |
| `completed` | query | boolean | No | DEPRECATED: use `mode`. Filter by completion status. `true` returns only completed, `false` returns only open (by due date), omitting returns both. |
| `includeNoAccount` | query | boolean | No | Include records without a linked bank account in income/outcome totals (does not affect opening/closing balance). |
| `includeNoTags` | query | boolean | No | When true with tag IDs, matches selected tags OR records with no tags; when true alone, only records without tags. |
| `periodFrom` | query | string | No | Period start date |
| `periodTo` | query | string | No | Period end date |
| `reconciled` | query | boolean[] | No | Reconciliation status filter. Comma-separated booleans 'true,false' |
| `tags` | query | string[] | No | Tag IDs to filter. Comma-separated IDs |
| `bankAccounts` | query | string[] | No | Bank account IDs to filter |

## Responses

| Status | Description |
|--------|-------------|
| 200 | Cash flow report generated successfully |

**Success Response Schema:**

[CashFlowReportEntity](../schemas/Cash/CashFlowReportEntity.md)

