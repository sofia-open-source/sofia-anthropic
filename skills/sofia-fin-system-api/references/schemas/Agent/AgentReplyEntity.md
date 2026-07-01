# AgentReplyEntity

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `document` | object | No |  |
| `image` | object | No |  |
| `text` | object | No |  |
| `toolCalls` | object[] | Yes | As chamadas de ferramentas feitas pela Sofia para gerar a resposta. |
| `markMessage` | boolean | No |  |

## Nested Fields

### `document`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `signedUrl` | string | Yes |  |
| `fileName` | string | Yes |  |
| `mimeType` | string | Yes |  |
| `caption` | string | No |  |
| `fileSize` | number | Yes |  |

### `image`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `signedUrl` | string | Yes |  |
| `mimeType` | string | Yes |  |
| `caption` | string | No |  |
| `fileSize` | number | Yes |  |

### `text`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `body` | string | Yes |  |
| `enableLinkPreview` | boolean | No |  |

### `toolCalls`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `toolCallId` | string | Yes |  |
| `toolName` | string | Yes |  |
| `input` | any | Yes |  |

