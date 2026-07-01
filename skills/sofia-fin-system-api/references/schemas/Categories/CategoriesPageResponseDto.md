# CategoriesPageResponseDto

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
| `id` | string | Yes | Category identifier. |
| `direction` | enum: IN, OUT | Yes | Category direction (IN or OUT). |
| `index` | number | Yes | Category index. |
| `name` | string | Yes | Category name. |
| `slug` | string | Yes | Category slug. |
| `createdAt` | string | Yes | Creation date of the category. |
| `updatedAt` | string | Yes | Last update date of the category. |

### `pageInfo`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `pageIndex` | number | Yes |  |
| `pageSize` | number | Yes |  |
| `totalPages` | number | Yes |  |
| `totalItems` | number | Yes |  |

