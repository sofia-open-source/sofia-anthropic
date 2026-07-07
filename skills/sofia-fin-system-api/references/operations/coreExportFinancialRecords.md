# POST /core/financial-records/export

**Resource:** [Core - Financial Records Export](../resources/Core-Financial-Records-Export.md)
**Solicita a exportação dos lançamentos financeiros de forma assíncrona.**
**Operation ID:** `coreExportFinancialRecords`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `textSearchTerm` | query | string | No |  |
| `readPreference` | query | enum: primary, primaryPreferred, secondary... | No |  |
| `semanticSearchTermInBase64` | query | string | No |  |
| `sortBy` | query | enum: direction, dueDate, contact... | No |  |
| `sortOrder` | query | enum: asc, desc | No |  |
| `populate` | query | string | No |  |
| `ids` | query | string[] | No | Lista de IDs de lançamentos financeiros para filtrar. |
| `amountFrom` | query | any | No | Valor do lançamento (mínimo). |
| `amountTo` | query | any | No | Valor do lançamento (máximo). |
| `finalAmountFrom` | query | any | No | Valor final do lançamento (mínimo). |
| `finalAmountTo` | query | any | No | Valor final do lançamento (máximo). |
| `direction` | query | enum: IN, OUT | No |  |
| `dueDateFrom` | query | string | No |  |
| `dueDateTo` | query | string | No |  |
| `contact` | query | string[] | No | Lista de IDs de contatos para filtrar. |
| `subcategory` | query | string[] | No | Lista de IDs de subcategorias para filtrar. |
| `competenceDateFrom` | query | string | No |  |
| `competenceDateTo` | query | string | No |  |
| `cashDateFrom` | query | string | No |  |
| `cashDateTo` | query | string | No |  |
| `cashFlowDateFrom` | query | string | No | Start of the cash-flow date range. Matches completed records by cashDate and open records by dueDate (OR semantics). Ignored when combined with cashDateFrom/To or dueDateFrom/To. |
| `cashFlowDateTo` | query | string | No | End of the cash-flow date range. Matches completed records by cashDate and open records by dueDate (OR semantics). Ignored when combined with cashDateFrom/To or dueDateFrom/To. |
| `createdAtFrom` | query | any | No |  |
| `createdAtTo` | query | any | No |  |
| `tags` | query | string[] | No | Lista de IDs de tags para filtrar. |
| `completed` | query | boolean | No |  |
| `reconciled` | query | boolean | No |  |
| `account` | query | string[] | No | Lista de IDs de contas bancárias para filtrar. |
| `includeNoAccount` | query | boolean | No | When true, also matches financial records with no linked bank account (null or missing). With account IDs, matches selected accounts OR no account; with no account IDs, matches only records without a linked account. |
| `includeNoTags` | query | boolean | No | When true, also matches financial records with no tags (empty or missing). With tag IDs, matches selected tags OR no tags; with no tag IDs, matches only records without tags. |
| `installmentFinancialRecord` | query | string[] | No | Lista de IDs de parcelas para filtrar. |
| `recurringFinancialRecord` | query | string[] | No | Lista de IDs de recorrências para filtrar. |
| `recurringOccurrenceNumber` | query | integer | No |  |
| `queryId` | query | string | No | ID da consulta a ser aplicada. |
| `hiddenColumnsForPdfReport` | query | string[] | No | Lista de colunas para esconder no PDF separadas por vírgula (contact, category). |
| `format` | query | enum: csv, xlsx | Yes |  |

## Responses

| Status | Description |
|--------|-------------|
| 200 | The id of the pending resource job. |
| default |  |

**Success Response Schema:**

[ExportFinancialRecordsResponseDto](../schemas/Export/ExportFinancialRecordsResponseDto.md)

