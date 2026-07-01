# IntegrationPreviewEntity

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes | Unique identifier for the integration. |
| `title` | string | Yes | Title of the integration. |
| `subtitle` | string | Yes | Subtitle of the integration. |
| `description` | string | Yes | Brief description of what the integration does. |
| `copy` | string | No | Copy text. Used to copy phone, email etc. |
| `content` | string | No | Content of the integration. Show on details. In HTML format. Use markdown for formatting. |
| `iconName` | string | Yes | Name of the integration icon. Lucide react. |
| `availability` | enum: AVAILABLE, SOON | Yes | Availability status of the integration. |

