# GET /core/invoices/{id}

**Resource:** [Core - Invoices](../resources/Core-Invoices.md)
**Gets an invoice by id.**
**Operation ID:** `coreFindInvoiceById`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `id` | path | string | Yes |  |
| `populate` | query | string | Yes |  |

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

**Success Response Schema:**

[InvoiceResponseDto](../schemas/Invoice/InvoiceResponseDto.md)

