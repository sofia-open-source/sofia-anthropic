# POST /core/bank-transactions/ofx

**Resource:** [Core - Bank Transactions](../resources/Core-Bank-Transactions.md)
**Dispara a importação assíncrona de um arquivo OFX.**
**Operation ID:** `coreDispatchOfxImport`

## Request Body

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [OfxImportRequestBodyDto](../schemas/Ofx/OfxImportRequestBodyDto.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 |  |
| default |  |

**Success Response Schema:**

[OfxImportJobRequestEntity](../schemas/Ofx/OfxImportJobRequestEntity.md)

