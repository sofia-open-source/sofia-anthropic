# UpdateMyOrganizationUserSettingsRequestBodyDto

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `tablePagination` | object | No | Partial update for table pagination preferences. |

## Nested Fields

### `tablePagination`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `mode` | enum: INFINITE, FIXED | No | Pagination mode applied to standard tables across the app. |
| `pageSize` | any | No | Page size used when pagination mode is fixed. |

