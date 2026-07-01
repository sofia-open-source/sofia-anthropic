# GET /analytics/financial-statements/financial-measures-report

**Resource:** [Analytics - Financial Statements Reports](../resources/Analytics-Financial-Statements-Reports.md)
**Generate financial measures report.**
**Operation ID:** `analyticsGenerateFinancialMeasuresReport`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `account` | query | string[] | No | Lista de IDs de contas bancárias para filtrar. |
| `amountFrom` | query | any | No | Valor do lançamento mínimo. |
| `amountTo` | query | any | No | Valor do lançamento máximo. |
| `amountType` | query | enum: base, final | No |  |
| `cashDateFrom` | query | string | No |  |
| `cashDateTo` | query | string | No |  |
| `competenceDateFrom` | query | string | No |  |
| `competenceDateTo` | query | string | No |  |
| `completed` | query | boolean | No |  |
| `contact` | query | string[] | No | Lista de IDs de contatos para filtrar. |
| `createdAtFrom` | query | any | No |  |
| `createdAtTo` | query | any | No |  |
| `direction` | query | enum: IN, OUT | No |  |
| `dueDateFrom` | query | string | No |  |
| `dueDateTo` | query | string | No |  |
| `queryId` | query | string | No | ID da query a ser aplicada à consulta. |
| `finalAmountFrom` | query | any | No | Valor final do lançamento mínimo. |
| `finalAmountTo` | query | any | No | Valor final do lançamento máximo. |
| `installmentFinancialRecord` | query | string[] | No | Lista de IDs de parcelas para filtrar. |
| `recurringFinancialRecord` | query | string[] | No | Lista de IDs de recorrências para filtrar. |
| `reconciled` | query | boolean | No |  |
| `subcategory` | query | string[] | No | Lista de IDs de subcategorias para filtrar. |
| `tags` | query | string[] | No | Lista de IDs de tags para filtrar. |
| `includeNoAccount` | query | boolean | No | When true, also matches financial records with no linked bank account (null or missing). With account IDs, matches selected accounts OR no account; with no account IDs, matches only records without a linked account. |
| `includeNoTags` | query | boolean | No | When true, also matches financial records with no tags (empty or missing). With tag IDs, matches selected tags OR no tags; with no tag IDs, matches only records without tags. |
| `considerInternalTransfers` | query | boolean | No | Se deve considerar transferências internas nos relatórios. |

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

**Success Response Schema:**

[FinancialMeasuresReportEntity](../schemas/Financial/FinancialMeasuresReportEntity.md)

