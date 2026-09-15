# Toolkit - Files upload

Two-step upload to Google Cloud Storage. Create upload request returns fileId and a signed PUT URL; after the client uploads bytes, confirm upload marks the file complete. User routes live under /toolkit/files/upload; system routes under /toolkit/organizations/:organizationId/files/upload for cross-service uploads. Used by bulk import, attachments, and export download prep.

## Operations

| Method | Path | Summary | Details |
|--------|------|---------|----------|
| POST | `/toolkit/files/upload` | Cria uma nova solicitação de upload de arquivo | [View](../operations/toolkitCreateFileUpload.md) |
| POST | `/toolkit/organizations/{organizationId}/files/upload` | Cria uma nova solicitação de upload de arquivo | [View](../operations/toolkitSystemCreateFileUpload.md) |
| POST | `/toolkit/files/upload/confirm` | Confirms a file upload | [View](../operations/toolkitConfirmFileUpload.md) |
| POST | `/toolkit/organizations/{organizationId}/files/upload/confirm` | Confirms a file upload | [View](../operations/toolkitSystemConfirmFileUpload.md) |
