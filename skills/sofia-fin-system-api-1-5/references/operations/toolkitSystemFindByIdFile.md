# GET /toolkit/organizations/{organizationId}/files/{fileId}

**Resource:** [Toolkit - Files](../resources/Toolkit-Files.md)
**Finds a file by id**
**Operation ID:** `toolkitSystemFindByIdFile`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `fileId` | path | string | Yes | The id of the file to get |
| `organizationId` | path | string | Yes | The id of the organization to get the file from |

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

**Success Response Schema:**

[FileEntity](../schemas/File/FileEntity.md)

