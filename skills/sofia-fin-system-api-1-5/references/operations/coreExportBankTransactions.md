# POST /core/bank-transactions/export

**Resource:** [Core - Bank Transactions Export](../resources/Core-Bank-Transactions-Export.md)
**Solicita a exportação das transações bancárias.**
**Operation ID:** `coreExportBankTransactions`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `textSearchTerm` | query | string | No |  |
| `semanticSearchTermInBase64` | query | string | No |  |
| `bankAccount` | query | string[] | No | Comma-separated bank account IDs to filter by. |
| `dateFrom` | query | any | No |  |
| `dateTo` | query | any | No |  |
| `type` | query | enum: DEBIT, CREDIT | No |  |
| `reconciled` | query | boolean | No | Filter by reconciled transactions. |
| `origin` | query | enum: AUTOMATIC_INTEGRATION, MANUAL_OFX_IMPORT | No | Filter by transaction origin. |
| `ignored` | query | boolean | No | Filter by ignored/archived transactions. |
| `ofxImportJobRequestIds` | query | string[] | No | Comma-separated OFX import job IDs to filter by. |
| `sortBy` | query | enum: date, amountInBrl, description... | No |  |
| `sortOrder` | query | enum: asc, desc | No |  |
| `populate` | query | string | No |  |
| `queryId` | query | string | No | Query ID to apply. |
| `ownerOrganizationId` | query | string | No |  |
| `format` | query | enum: csv, xlsx | Yes |  |

## Responses

| Status | Description |
|--------|-------------|
| 200 | The id of the pending resource job. |
| default |  |

**Success Response Schema:**

[ExportBankTransactionsResponseDto](../schemas/Export/ExportBankTransactionsResponseDto.md)

