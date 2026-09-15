# POST /core/invoices/national

**Resource:** [Core - Invoices](../resources/Core-Invoices.md)
**Creates a national NFSe via Focus NFe and stores it.**
**Operation ID:** `coreCreateNationalInvoice`

## Request Body

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [CreateNationalInvoiceRequestBodyDto](../schemas/Create/CreateNationalInvoiceRequestBodyDto.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 |  |
| default |  |

**Success Response Schema:**

[InvoiceResponseDto](../schemas/Invoice/InvoiceResponseDto.md)

