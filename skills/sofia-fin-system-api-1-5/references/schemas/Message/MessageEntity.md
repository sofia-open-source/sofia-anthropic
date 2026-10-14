# MessageEntity

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes | User message ID. |
| `replyTo` | string | No | Database ID of the message being replied to (for AI messages only). |
| `replyToChannelMessageId` | string | No | Channel message ID of the message being replied to (for AI messages only). |
| `enableLinkPreview` | boolean | No | Whether the message should have link preview. |
| `role` | enum: USER, AI | Yes | Message role (user or ai). |
| `channel` | enum: WHATSAPP, EMAIL | Yes | Message channel (WHATSAPP or EMAIL). |
| `channelMessageId` | string | Yes | Message ID in the source channel. |
| `chatId` | string | Yes | Conversation ID in the source channel. |
| `chatTitle` | string | No | Conversation title (e.g. email subject). |
| `from` | object | Yes | Sender information. |
| `status` | enum: PENDING, PROCESSING, PROCESSED... | No | Message status. |
| `content` | string | Yes | Message content. |
| `quotedChannelMessageId` | string | No | ID of the quoted message. |
| `files` | string[] | No | Attached file IDs. |
| `toolCalls` | object[] | No | Tool calls made by Sofia to generate the message. |
| `channelCreatedAt` |  | Yes | Message creation date in the source channel. |
| `createdAt` |  | Yes | Record creation date in the fin-system. |
| `startProcessingAt` | any | No | Processing start date. |
| `processedAt` | any | No | Processing completion date. |
| `processingDurationInMilliseconds` | integer | No | Processing duration in milliseconds. |
| `updatedAt` |  | Yes | Last record update date. |
| `markMessage` | boolean | No | Whether to mark the source message in the response. |

## Nested Fields

### `from`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `mainUserId` | string | No | Sender user ID (optional). |
| `email` | string (email) | No | Sender email. |
| `phone` | string | No | Sender phone. |
| `name` | string | No | Sender name. |

### `toolCalls`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `toolCallId` | string | Yes | Tool call ID. |
| `toolName` | string | Yes | Tool name. |
| `input` | any | No | Tool input. |

