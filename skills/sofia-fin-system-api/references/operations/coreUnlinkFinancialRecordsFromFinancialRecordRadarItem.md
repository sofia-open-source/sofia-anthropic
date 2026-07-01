# POST /core/financial-records/radar/items/{radarItemId}/unlink

**Resource:** [Core - Financial Record Radar Items](../resources/Core-Financial-Record-Radar-Items.md)
**Desvincula registros financeiros de um registro de radar**
**Operation ID:** `coreUnlinkFinancialRecordsFromFinancialRecordRadarItem`

Remove vínculos entre um registro de radar e registros financeiros, atualizando ambos os lados da relação.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `radarItemId` | path | string | Yes | Identificador do registro de radar |

## Request Body

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [UnlinkFinancialRecordsRequestBodyDto](../schemas/Unlink/UnlinkFinancialRecordsRequestBodyDto.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | Radar record updated after unlinking |
| default |  |

**Success Response Schema:**

[FinancialRecordRadarItemEntity](../schemas/Financial/FinancialRecordRadarItemEntity.md)

