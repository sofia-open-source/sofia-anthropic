# POST /core/invoices/bulk

**Resource:** [Core - Bulk Invoices](../resources/Core-Bulk-Invoices.md)
**Schedules asynchronous creation of multiple NFSe invoices (municipal default or national). Each item sets kind to default or national.**
**Operation ID:** `coreScheduleBulkInvoices`

## Request Body

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [CreateBulkInvoicesJobRequestBodyDto](../schemas/Create/CreateBulkInvoicesJobRequestBodyDto.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 |  |
| default |  |

**Success Response Schema:**

[BulkInvoicesJobRequestEntity](../schemas/Bulk/BulkInvoicesJobRequestEntity.md)

