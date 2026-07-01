# CreateMessageFromWhatsappRequestBodyDto

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `channel` | enum: WHATSAPP, EMAIL | Yes | Message channel (WHATSAPP or EMAIL). |
| `channelMessageId` | string | Yes | Message ID in the source channel. |
| `chatId` | string | Yes | Conversation ID in the source channel. |
| `chatTitle` | string | No | Conversation title (e.g. email subject). |
| `from` | object | Yes | Sender information. |
| `to` | object | Yes | Recipient information. |
| `content` | string | Yes | Message content. |
| `files` | string[] | No | List of attached file IDs (optional). |
| `channelCreatedAt` |  | Yes | Message creation date in the source channel. |

## Nested Fields

### `from`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `mainUserId` | string | No | Sender user ID (optional). |
| `email` | string (email) | No | Sender email. |
| `phone` | string | No | Sender phone. |
| `name` | string | No | Sender name. |

### `to`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `email` | string (email) | No | Recipient email. |
| `phone` | string | No | Recipient phone. |

