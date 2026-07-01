# OrganizationUserSettingEntity

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes | Settings identifier. |
| `ownerOrganization` | string | Yes | Organization identifier that scopes the settings. |
| `ownerUser` | string | Yes | User identifier (Clerk user id) that scopes the settings. |
| `tablePagination` | object | Yes | Preferences for standard table pagination. |
| `createdAt` |  | Yes | Creation date. |
| `updatedAt` |  | Yes | Last update date. |

## Nested Fields

### `tablePagination`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `mode` | enum: INFINITE, FIXED | Yes | Pagination mode applied to standard tables across the app. |
| `pageSize` | any | Yes | Page size used when pagination mode is fixed. |

