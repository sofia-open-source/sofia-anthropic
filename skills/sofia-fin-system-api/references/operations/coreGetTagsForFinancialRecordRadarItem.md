# GET /core/financial-records/radar/items/{radarItemId}/tags

**Resource:** [Core - Financial Record Radar Items](../resources/Core-Financial-Record-Radar-Items.md)
**Obtém as tags para um registro de radar.**
**Operation ID:** `coreGetTagsForFinancialRecordRadarItem`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `radarItemId` | path | string | Yes | Identificador do registro de radar |

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

**Success Response Schema:**

Array of [FinancialRecordRadarItemTagEntity](../schemas/Financial/FinancialRecordRadarItemTagEntity.md)

