# GET /core/bank-transactions/ofx/job-requests

**Resource:** [Core - Bank Transactions](../resources/Core-Bank-Transactions.md)
**Lista todas as solicitações de importação de arquivos OFX com suas execuções.**
**Operation ID:** `coreFindAllOfxImportJobRequests`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `pageIndex` | query | number | No |  |
| `pageSize` | query | number | No |  |
| `sortBy` | query | enum: createdAt, fileName, bankAccountName | No | Sort field. Possible values: 'createdAt', 'fileName', 'bankAccountName'. |
| `sortOrder` | query | enum: asc, desc | No | Sort order. Possible values: 'asc', 'desc'. |
| `textSearchTerm` | query | string | No | Text search term to filter by file name or bank account name. |
| `bankAccountIds` | query | string[] | No | Comma-separated bank account IDs to filter by. |
| `ids` | query | string[] | No | Comma-separated OFX import job request identifiers to search for. |

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

**Success Response Schema:**

[OfxImportJobRequestsPageResponseDto](../schemas/Ofx/OfxImportJobRequestsPageResponseDto.md)

