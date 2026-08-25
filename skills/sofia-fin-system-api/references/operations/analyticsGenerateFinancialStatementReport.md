# GET /analytics/financial-statements/report

**Resource:** [Analytics - Financial Statements Reports](../resources/Analytics-Financial-Statements-Reports.md)
**Generate financial statement report with grouping and filter options.**
**Operation ID:** `analyticsGenerateFinancialStatementReport`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `grouping` | query | enum: daily, monthly, yearly | No | Tipo de agrupamento temporal. Valores possíveis: daily, monthly, yearly |
| `referenceDate` | query | enum: dueDate, cashDate, competenceDate | No | Campo de data a ser utilizado para filtros |
| `completed` | query | boolean | No | Status de conclusão dos lançamentos |
| `includeNoTags` | query | boolean | No | When true with tag IDs, matches selected tags OR records with no tags; when true alone, only records without tags. |
| `queryId` | query | string | No | ID da query a ser aplicada à consulta. |
| `considerInternalTransfers` | query | boolean | No | Se deve considerar transferências internas nos relatórios |
| `periodFrom` | query | string | No | Data inicial do período |
| `periodTo` | query | string | No | Data final do período |
| `tags` | query | string[] | No | IDs das tags para filtrar |

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

**Success Response Schema:**

[FinancialStatementReportEntity](../schemas/Financial/FinancialStatementReportEntity.md)

