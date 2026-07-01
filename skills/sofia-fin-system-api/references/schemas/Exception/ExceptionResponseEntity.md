# ExceptionResponseEntity

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `statusCode` | number | Yes |  |
| `message` | string | Yes |  |
| `errors` | object[] | Yes |  |

## Nested Fields

### `errors`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `fieldPath` | string | Yes |  |
| `messages` | string[] | Yes |  |

