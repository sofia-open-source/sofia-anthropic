# Core - Bulk Invoices

Batch NFSe issuance for many invoices in one operation. POST /core/invoices/bulk schedules an async job with the payload of invoices to create (default or national). A queue worker processes each item and records successes and failures. Use when issuing a large set of service invoices from a single user action or integration.

## Operations

| Method | Path | Summary | Details |
|--------|------|---------|----------|
| POST | `/core/invoices/bulk` | Schedules asynchronous creation of multiple NFSe invoices (municipal default or national). Each item sets kind to default or national. | [View](../operations/coreScheduleBulkInvoices.md) |
