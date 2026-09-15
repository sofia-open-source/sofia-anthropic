# UserVersionChangelogResponseDto

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes |  |
| `userId` | string | Yes |  |
| `version` | string | Yes |  |
| `viewed` | boolean | Yes |  |
| `populatedChangelog` | object | No |  |
| `createdAt` | string | Yes | Creation date of the tag. |
| `updatedAt` | string | Yes | Last update date of the tag. |
| `deletedAt` | string | No | When the resource was removed |

## Nested Fields

### `populatedChangelog`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `version` | string | Yes |  |
| `date` | any | No |  |
| `summary` | string | No |  |
| `content` | string | No |  |

