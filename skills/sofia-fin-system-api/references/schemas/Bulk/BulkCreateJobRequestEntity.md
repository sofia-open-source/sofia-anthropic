# BulkCreateJobRequestEntity

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes | Identificador da solicitação de criação. |
| `resource` | enum: core_FinancialRecords, core_Contacts, core_BankAccounts... | Yes | Recurso a ser criado. |
| `nRows` | number | Yes | Número de linhas a serem criadas. |
| `fileId` | string | Yes | Identificador do arquivo com dados para criação. |
| `requesterUserId` | string | Yes | Identificador do usuário que solicitou a criação. |
| `radarItem` | string | No | Identificador do registro de radar que originou a criação em massa. |
| `createdAt` |  | Yes | Data de criação da solicitação de criação. |
| `updatedAt` |  | Yes | Data de atualização da solicitação de criação. |
| `deletedAt` | any | Yes | Data de exclusão da solicitação de criação. |

