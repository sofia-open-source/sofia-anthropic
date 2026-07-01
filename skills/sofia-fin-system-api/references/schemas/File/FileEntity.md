# FileEntity

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes | Identificador do arquivo. |
| `ownerOrganization` | string | Yes | Identificador da organização dona do arquivo. |
| `originalFileName` | string | Yes | Nome original do arquivo. |
| `mimeType` | string | Yes | Tipo MIME do arquivo. |
| `size` | number | Yes | Tamanho do arquivo em bytes. |
| `fileType` | enum: DEFAULT, FINANCIAL_RECORD, EXPORT... | Yes | Tipo do arquivo. |
| `objectName` | string | Yes | Nome do objeto no storage. |
| `status` | enum: PENDING, COMPLETED, FAILED... | Yes | Status do arquivo. |
| `caption` | string | No | Legenda do arquivo. |
| `createdAt` |  | Yes | Data de criação do arquivo. |
| `updatedAt` |  | Yes | Data de atualização do arquivo. |
| `deletedAt` | any | No | Data de exclusão do arquivo. |
| `url` | string | Yes | URL do arquivo. |
| `signedUrl` | string | Yes | URL assinada do arquivo. |

