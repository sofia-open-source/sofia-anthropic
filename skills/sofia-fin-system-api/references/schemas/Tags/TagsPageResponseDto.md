# TagsPageResponseDto

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `items` | object[] | Yes |  |
| `pageInfo` | object | Yes |  |

## Nested Fields

### `items`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes | Tag identifier. |
| `ownerOrganization` | string | Yes | Identifier of the organization that owns the tag. |
| `name` | string | Yes | Tag name. |
| `createdAt` | string | Yes | Creation date of the tag. |
| `updatedAt` | string | Yes | Last update date of the tag. |
| `searchScore` | number | No | Text search score. |
| `importedAt` | string | No | Tag import date. |
| `importedBy` | string | No | Tag import source. |
| `externalId` | string | No | External identifier of the tag. |

### `pageInfo`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `pageIndex` | number | Yes |  |
| `pageSize` | number | Yes |  |
| `totalPages` | number | Yes |  |
| `totalItems` | number | Yes |  |

