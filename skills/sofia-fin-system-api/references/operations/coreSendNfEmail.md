# POST /core/invoices/{id}/send-email

**Resource:** [Core - Invoices](../resources/Core-Invoices.md)
**Sends an e-mail with the NFSe to the contact.**
**Operation ID:** `coreSendNfEmail`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `id` | path | string | Yes |  |

## Request Body

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [SendNfEmailRequestBodyDto](../schemas/Send/SendNfEmailRequestBodyDto.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

