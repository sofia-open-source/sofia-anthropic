# BulkBankTransactionsJobRequestEntity

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes |  |
| `ownerOrganization` | string | Yes |  |
| `requesterUserId` | string | Yes |  |
| `operation` | enum: ARCHIVE, UNARCHIVE, UNRECONCILE... | Yes |  |
| `bankTransactionIds` | string[] | Yes |  |
| `createdAt` |  | Yes |  |
| `updatedAt` |  | Yes |  |

