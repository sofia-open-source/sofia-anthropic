# GET /core/financial-records/radar/items/{radarItemId}

**Resource:** [Core - Financial Record Radar Items](../resources/Core-Financial-Record-Radar-Items.md)
**Busca um registro de radar pelo identificador.**
**Operation ID:** `coreFindByIdFinancialRecordRadarItem`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `radarItemId` | path | string | Yes | Identificador do registro de radar |
| `populate` | query | string | Yes |  |

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

**Success Response Schema:**

[FinancialRecordRadarItemEntity](../schemas/Financial/FinancialRecordRadarItemEntity.md)

