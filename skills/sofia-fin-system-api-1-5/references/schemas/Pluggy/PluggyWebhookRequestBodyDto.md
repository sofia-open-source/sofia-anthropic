# PluggyWebhookRequestBodyDto

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `event` | enum: item/created, item/updated, item/deleted... | Yes | Event type. |
| `eventId` | string | Yes | Unique identifier for the event. |
| `itemId` | string | No | Item identifier. |
| `accountId` | string | No | Pluggy account id for transaction events. |
| `transactionIds` | string[] | No | Transaction ids removed by Pluggy (transactions/deleted). |
| `triggeredBy` | enum: USER, CLIENT, SYNC... | No | Who or what triggered the event. |
| `error` | object | No | Error details in case of item/error event. |

## Nested Fields

### `error`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `code` | string | Yes |  |
| `message` | string | Yes |  |
| `parameter` | string | No |  |

