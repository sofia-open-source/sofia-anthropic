# GET /core/invoices/{invoiceId}/events

**Resource:** [Core - Invoices](../resources/Core-Invoices.md)
**Lists audit events for an invoice (NFSe lifecycle and financial-record associations).**
**Operation ID:** `coreFindInvoiceEventsByInvoiceId`

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

Array of [InvoiceEventResponseDto](../schemas/Invoice/InvoiceEventResponseDto.md)

