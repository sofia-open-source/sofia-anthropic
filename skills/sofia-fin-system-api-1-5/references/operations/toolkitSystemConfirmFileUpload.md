# POST /toolkit/organizations/{organizationId}/files/upload/confirm

**Resource:** [Toolkit - Files upload](../resources/Toolkit-Files-upload.md)
**Confirms a file upload**
**Operation ID:** `toolkitSystemConfirmFileUpload`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `organizationId` | path | string | Yes | The id of the organization to confirm the file upload |

## Request Body

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [ConfirmFileUploadRequestBodyDto](../schemas/Confirm/ConfirmFileUploadRequestBodyDto.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 |  |
| default |  |

**Success Response Schema:**

[FileEntity](../schemas/File/FileEntity.md)

