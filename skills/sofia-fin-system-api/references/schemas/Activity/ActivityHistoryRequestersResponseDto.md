# ActivityHistoryRequestersResponseDto

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `requesters` | object[] | Yes |  |

## Nested Fields

### `requesters`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes | Identifier of the user who performed activities. |
| `primaryEmail` | string | No | Primary email of the user, when known. |
| `firstName` | string | No | First name of the user, when known. |
| `lastName` | string | No | Last name of the user, when known. |

