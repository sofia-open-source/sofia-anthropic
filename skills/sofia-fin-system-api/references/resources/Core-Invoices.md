# Core - Invoices

Fiscal invoice (NFSe) lifecycle for the organization: issue municipal (default) or national service invoices, cancel, list, and find by id. Invoice events expose status history; Focus NFe webhooks and scheduler/queue jobs sync state with the external provider. Creation and cancellation are the primary mutations; there is no generic partial-update endpoint.

## Operations

| Method | Path | Summary | Details |
|--------|------|---------|----------|
| POST | `/core/invoices/default` | Creates a default (municipal) NFSe via Focus NFe and stores it. | [View](../operations/coreCreateDefaultInvoice.md) |
| POST | `/core/invoices/national` | Creates a national NFSe via Focus NFe and stores it. | [View](../operations/coreCreateNationalInvoice.md) |
| POST | `/core/invoices/{invoiceId}/cancel` | Requests NFSe cancellation at Focus NFe and marks the invoice as cancel requested. | [View](../operations/coreCancelInvoice.md) |
| GET | `/core/invoices` | Lists invoices for the organization. | [View](../operations/coreFindAllInvoices.md) |
| GET | `/core/invoices/{invoiceId}/events` | Lists audit events for an invoice (NFSe lifecycle and financial-record associations). | [View](../operations/coreFindInvoiceEventsByInvoiceId.md) |
| GET | `/core/invoices/{id}` | Gets an invoice by id. | [View](../operations/coreFindInvoiceById.md) |
| POST | `/core/invoices/{id}/send-email` | Sends an e-mail with the NFSe to the contact. | [View](../operations/coreSendNfEmail.md) |
