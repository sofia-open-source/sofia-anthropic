# POST /core/invoices/{invoiceId}/cancel

**Resource:** [Core - Invoices](../resources/Core-Invoices.md)
**Requests NFSe cancellation at Focus NFe and marks the invoice as cancel requested.**
**Operation ID:** `coreCancelInvoice`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `invoiceId` | path | string | Yes |  |

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

**Success Response Schema:**

[InvoiceResponseDto](../schemas/Invoice/InvoiceResponseDto.md)

