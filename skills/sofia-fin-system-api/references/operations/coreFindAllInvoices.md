# GET /core/invoices

**Resource:** [Core - Invoices](../resources/Core-Invoices.md)
**Lists invoices for the organization.**
**Operation ID:** `coreFindAllInvoices`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `pageIndex` | query | integer | No |  |
| `pageSize` | query | integer | No |  |
| `types` | query | string[] | No | Comma-separated invoice types (InvoiceType enum values). |
| `legalEntitiesIds` | query | string[] | No | Comma-separated legal entity ids to filter by. |
| `issueDateFrom` | query | any | No |  |
| `issueDateTo` | query | any | No |  |
| `tomadorContactId` | query | string | No | Filter by contact id linked as invoice tomador. |
| `providerStatuses` | query | string[] | No | Comma-separated Focus NFe providerStatus values to filter by. |
| `textSearchTerm` | query | string | No | Search tomador, description, amount, fiscal note number (prefeitura), RPS, verification code, provider ref. |
| `populate` | query | string | No |  |

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

**Success Response Schema:**

[InvoicesPageResponseDto](../schemas/Invoices/InvoicesPageResponseDto.md)

