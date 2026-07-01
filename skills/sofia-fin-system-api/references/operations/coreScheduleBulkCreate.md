# POST /core/bulk/create

**Resource:** [Core - Bulk Create](../resources/Core-Bulk-Create.md)
**Schedules creation of multiple resources from a file**
**Operation ID:** `coreScheduleBulkCreate`

## Request Body

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [BulkCreateJobRequestResponseDto](../schemas/Bulk/BulkCreateJobRequestResponseDto.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 |  |
| default |  |

**Success Response Schema:**

[BulkCreateJobRequestEntity](../schemas/Bulk/BulkCreateJobRequestEntity.md)

