# SubgroupsPageResponseDto

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
| `id` | string | Yes | Subgroup identifier. |
| `ownerOrganization` | string | Yes | Identifier of the organization that owns the subgroup. |
| `group` | string | Yes | Identifier of the parent group (Category) this subgroup belongs to. |
| `name` | string | Yes | Subgroup name. |
| `slug` | string | Yes | Subgroup slug. |
| `position` | number | Yes | Subgroup position, used for ordering within its parent group. |
| `createdAt` | string | Yes | Creation date of the subgroup. |
| `updatedAt` | string | Yes | Last update date of the subgroup. |

### `pageInfo`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `pageIndex` | number | Yes |  |
| `pageSize` | number | Yes |  |
| `totalPages` | number | Yes |  |
| `totalItems` | number | Yes |  |

