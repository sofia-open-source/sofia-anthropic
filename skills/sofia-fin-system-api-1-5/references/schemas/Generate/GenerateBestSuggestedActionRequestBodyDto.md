# GenerateBestSuggestedActionRequestBodyDto

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `organizationId` | string | Yes |  |
| `files` | object[] | Yes |  |
| `messageContext` | object | No |  |

## Nested Fields

### `files`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `url` | string | Yes |  |
| `mimeType` | string | Yes |  |
| `fileName` | string | Yes |  |

### `messageContext`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `chatId` | string | Yes | ID do chat. |
| `chatTitle` | string | No | Título do chat. |
| `channel` | enum: whatsapp, email | Yes | Canal da mensagem. |
| `currentMessage` | object | Yes |  |
| `lastMessages` | object[] | Yes |  |

#### `messageContext.currentMessage`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes | ID da mensagem. |
| `from` | object | Yes |  |
| `timestamp` | string | Yes | Timestamp da mensagem. |
| `content` | string | Yes | Conteúdo da mensagem. |
| `files` | object[] | Yes | Arquivos da mensagem. |
| `quoted` | object | No | Mensagem citada. |
| `toolCalls` | object[] | No | As chamadas de ferramentas feitas pela Sofia para gerar a mensagem. |

#### `messageContext.lastMessages`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes | ID da mensagem. |
| `from` | object | Yes |  |
| `timestamp` | string | Yes | Timestamp da mensagem. |
| `content` | string | Yes | Conteúdo da mensagem. |
| `files` | object[] | Yes | Arquivos da mensagem. |
| `quoted` | object | No | Mensagem citada. |
| `toolCalls` | object[] | No | As chamadas de ferramentas feitas pela Sofia para gerar a mensagem. |

