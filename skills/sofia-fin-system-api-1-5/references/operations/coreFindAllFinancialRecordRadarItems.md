# GET /core/financial-records/radar/items

**Resource:** [Core - Financial Record Radar Items](../resources/Core-Financial-Record-Radar-Items.md)
**Busca todos os registros do radar.**
**Operation ID:** `coreFindAllFinancialRecordRadarItems`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `pageIndex` | query | number | No |  |
| `pageSize` | query | number | No |  |
| `folder` | query | enum: MAIN, SPAM | No |  |
| `status` | query | enum: PENDING, LINKED, ARCHIVED | No |  |
| `origin` | query | enum: WHATSAPP_AGENT, EMAIL_FORWARDING_INTEGRATION | No |  |
| `nature` | query | enum: WHATSAPP_MESSAGE, EMAIL_MESSAGE | No |  |
| `hasAutoExecute` | query | boolean | No |  |
| `links` | query | string[] | No |  |
| `sortBy` | query | enum: createdAt | No |  |
| `sortOrder` | query | enum: asc, desc | No |  |
| `populate` | query | string | No |  |

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

**Success Response Schema:**

[FinancialRecordRadarItemsPageResponseDto](../schemas/Financial/FinancialRecordRadarItemsPageResponseDto.md)

