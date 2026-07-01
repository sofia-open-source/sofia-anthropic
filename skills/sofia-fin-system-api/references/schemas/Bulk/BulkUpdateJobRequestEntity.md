# BulkUpdateJobRequestEntity

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes | Bulk update job request identifier. |
| `resource` | enum: core_FinancialRecords, core_Contacts, core_BankAccounts... | Yes | Resource to be updated. |
| `ids` | string[] | Yes | Identifiers of the records to be updated. |
| `payload` | object | Yes | Values to be updated. |
| `requesterUserId` | string | Yes | Identifier of the user who requested the update. |
| `radarItem` | string | No | Identifier of the radar item that originated the bulk update. |
| `createdAt` |  | Yes | Creation date of the bulk update job request. |
| `updatedAt` |  | Yes | Last update date of the bulk update job request. |
| `deletedAt` | any | Yes | Deletion date of the bulk update job request. |

