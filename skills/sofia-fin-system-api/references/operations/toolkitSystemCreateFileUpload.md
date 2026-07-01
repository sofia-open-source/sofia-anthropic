# POST /toolkit/organizations/{organizationId}/files/upload

**Resource:** [Toolkit - Files upload](../resources/Toolkit-Files-upload.md)
**Cria uma nova solicitação de upload de arquivo**
**Operation ID:** `toolkitSystemCreateFileUpload`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `organizationId` | path | string | Yes | The id of the organization to confirm the file upload |

## Request Body

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [CreateFileUploadRequestBodyDto](../schemas/Create/CreateFileUploadRequestBodyDto.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

