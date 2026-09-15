# GET /core/financial-records/radar/items/{radarItemId}/preview-bulk-create-file

**Resource:** [Core - Financial Record Radar Items](../resources/Core-Financial-Record-Radar-Items.md)
**Obtém o preview de um arquivo .csv para criação em lote.**
**Operation ID:** `corePreviewBulkCreateFile`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `radarItemId` | path | string | Yes | Identificador do registro de radar |
| `limit` | query | number | Yes |  |

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

**Success Response Schema:**

[FinancialRecordsBulkCreateFilePreviewEntity](../schemas/Financial/FinancialRecordsBulkCreateFilePreviewEntity.md)

