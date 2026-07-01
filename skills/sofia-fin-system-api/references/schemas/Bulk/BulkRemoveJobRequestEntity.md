# BulkRemoveJobRequestEntity

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes | Bulk remove job request identifier. |
| `resource` | enum: core_FinancialRecords, core_Contacts, core_BankAccounts... | Yes | Resource to be removed. |
| `ids` | string[] | Yes | Identifiers of the resources to be removed. |
| `requesterUserId` | string | Yes | Identifier of the user who requested the removal. |
| `createdAt` |  | Yes | Creation date of the bulk remove job request. |
| `updatedAt` |  | Yes | Last update date of the bulk remove job request. |
| `deletedAt` | any | Yes | Deletion date of the bulk remove job request. |

