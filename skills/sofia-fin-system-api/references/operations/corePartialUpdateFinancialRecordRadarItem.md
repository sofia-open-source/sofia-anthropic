# PATCH /core/financial-records/radar/items/{radarItemId}

**Resource:** [Core - Financial Record Radar Items](../resources/Core-Financial-Record-Radar-Items.md)
**Atualiza parcialmente um registro de radar**
**Operation ID:** `corePartialUpdateFinancialRecordRadarItem`

Atualiza parcialmente um registro de radar existente.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `radarItemId` | path | string | Yes | Identificador do registro de radar |

## Request Body

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [PartialUpdateFinancialRecordRadarItemRequestBodyDto](../schemas/Partial/PartialUpdateFinancialRecordRadarItemRequestBodyDto.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | Registro de radar atualizado com sucesso |
| default |  |

**Success Response Schema:**

[FinancialRecordRadarItemEntity](../schemas/Financial/FinancialRecordRadarItemEntity.md)

