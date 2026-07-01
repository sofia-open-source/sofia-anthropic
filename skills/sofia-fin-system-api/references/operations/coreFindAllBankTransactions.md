# GET /core/bank-transactions

**Resource:** [Core - Bank Transactions](../resources/Core-Bank-Transactions.md)
**Busca todas as movimentações financeiras.**
**Operation ID:** `coreFindAllBankTransactions`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `pageIndex` | query | number | No |  |
| `pageSize` | query | number | No |  |
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

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

**Success Response Schema:**

[BankTransactionsPageResponseDto](../schemas/Bank/BankTransactionsPageResponseDto.md)

