# POST /core/financial-records/radar/items/{radarItemId}/links

**Resource:** [Core - Financial Record Radar Items](../resources/Core-Financial-Record-Radar-Items.md)
**Vincula registros financeiros a um registro de radar**
**Operation ID:** `coreLinkFinancialRecordsToFinancialRecordRadarItem`

Adiciona vínculos entre um registro de radar e múltiplos registros financeiros, atualizando ambos os lados da relação.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `radarItemId` | path | string | Yes | Identificador do registro de radar |

## Request Body

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [LinkFinancialRecordsRequestBodyDto](../schemas/Link/LinkFinancialRecordsRequestBodyDto.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 | Radar record updated with links |
| default |  |

**Success Response Schema:**

[FinancialRecordRadarItemEntity](../schemas/Financial/FinancialRecordRadarItemEntity.md)

