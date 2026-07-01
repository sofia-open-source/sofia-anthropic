# Toolkit - Files

File metadata and access after upload. Find by id, delete, and generate signed download URLs from stored object URLs. System find-by-id accepts an organization id for internal callers. Files are owned by an organization and referenced by exports, bulk jobs, and attachments.

## Operations

| Method | Path | Summary | Details |
|--------|------|---------|----------|
| GET | `/toolkit/files/{id}` | Finds a file by id | [View](../operations/toolkitFindByIdFile.md) |
| DELETE | `/toolkit/files/{id}` | Deletes a file | [View](../operations/toolkitDeleteFile.md) |
| GET | `/toolkit/organizations/{organizationId}/files/{fileId}` | Finds a file by id | [View](../operations/toolkitSystemFindByIdFile.md) |
| GET | `/toolkit/files/signed-url` | Get a signed url from a url | [View](../operations/toolkitGetSignedUrlFromUrl.md) |
