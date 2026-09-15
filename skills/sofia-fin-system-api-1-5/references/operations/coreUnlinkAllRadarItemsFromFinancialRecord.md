# POST /core/financial-records/{id}/unlink-all-radar-items

**Resource:** [Core - Financial Records](../resources/Core-Financial-Records.md)
**Desvincula todos os radar items de um lançamento financeiro**
**Operation ID:** `coreUnlinkAllRadarItemsFromFinancialRecord`

Remove o vínculo entre um lançamento financeiro e todos os radar items que estão associados a ele.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `id` | path | string | Yes | Financial record identifier. |

## Request Body

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [UnlinkAllRadarItemsRequestBodyDto](../schemas/Unlink/UnlinkAllRadarItemsRequestBodyDto.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | Financial record with unlinked radar items |
| default |  |

**Success Response Schema:**

[UnlinkAllRadarItemsResponseDto](../schemas/Unlink/UnlinkAllRadarItemsResponseDto.md)

