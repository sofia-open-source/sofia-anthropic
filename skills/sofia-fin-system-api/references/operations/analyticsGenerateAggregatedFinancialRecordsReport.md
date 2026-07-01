# GET /analytics/financial-records/aggregated/report

**Resource:** [Analytics - Financial Records Reports](../resources/Analytics-Financial-Records-Reports.md)
**Generate aggregated financial records report by category, contact or tag.**
**Operation ID:** `analyticsGenerateAggregatedFinancialRecordsReport`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `account` | query | string | No | Account IDs separated by comma |
| `amountFrom` | query | string | No | Minimum record amount. |
| `amountTo` | query | string | No | Maximum record amount. |
| `amountType` | query | enum: base, final | No | Value type for calculations. "base" for amount, "final" for finalAmount. Default is "final". |
| `cashDateFrom` | query | string | No | Cash date start |
| `cashDateTo` | query | string | No | Cash date end |
| `competenceDateFrom` | query | string | No | Competence date start |
| `competenceDateTo` | query | string | No | Competence date end |
| `completed` | query | string | No | Record completion status |
| `contact` | query | string | No | Contact ID |
| `createdAtFrom` | query | string | No | Creation date start |
| `createdAtTo` | query | string | No | Creation date end |
| `direction` | query | enum: IN, OUT | No | Report direction |
| `dueDateFrom` | query | string | No | Due date start |
| `dueDateTo` | query | string | No | Due date end |
| `queryId` | query | string | No | Query ID to apply to the request. |
| `finalAmountFrom` | query | string | No | Minimum final record amount. |
| `finalAmountTo` | query | string | No | Maximum final record amount. |
| `installmentFinancialRecord` | query | string | No | Installment financial record ID |
| `recurringFinancialRecord` | query | string | No | Recurring financial record ID |
| `reconciled` | query | string | No | Reconciliation status |
| `subcategory` | query | string | No | Subcategory ID |
| `tags` | query | string | No | Tag IDs |
| `includeNoAccount` | query | boolean | No | When true, also matches financial records with no linked bank account (null or missing). With account IDs, matches selected accounts OR no account; with no account IDs, matches only records without a linked account. |
| `includeNoTags` | query | boolean | No | When true, also matches financial records with no tags (empty or missing). With tag IDs, matches selected tags OR no tags; with no tag IDs, matches only records without tags. |
| `considerInternalTransfers` | query | boolean | No | Se deve considerar transferências internas nos relatórios. |
| `groupBy` | query | enum: category, contact, tag | No | Campo para agrupamento dos dados |
| `sortOrder` | query | enum: asc, desc | No | Ordem de classificação |
| `aggregationDirection` | query | enum: IN, OUT | No | Direção do lançamento financeiro |

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

**Success Response Schema:**

[AggregatedFinancialRecordsReportEntity](../schemas/Aggregated/AggregatedFinancialRecordsReportEntity.md)

