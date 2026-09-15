# POST /core/invoices/default

**Resource:** [Core - Invoices](../resources/Core-Invoices.md)
**Creates a default (municipal) NFSe via Focus NFe and stores it.**
**Operation ID:** `coreCreateDefaultInvoice`

## Request Body

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [CreateDefaultInvoiceRequestBodyDto](../schemas/Create/CreateDefaultInvoiceRequestBodyDto.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 |  |
| default |  |

**Success Response Schema:**

[InvoiceResponseDto](../schemas/Invoice/InvoiceResponseDto.md)

