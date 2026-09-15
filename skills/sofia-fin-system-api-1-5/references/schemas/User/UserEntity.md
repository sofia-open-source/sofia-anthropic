# UserEntity

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes | Identificador do usuário no banco de dados. |
| `mainId` | string | Yes | Identificador do usuário no clerk. |
| `firstName` | string | Yes | Nome do usuário. |
| `lastName` | string | Yes | Sobrenome do usuário. |
| `email` | string | No | Email do usuário. |
| `phone` | string | No | Telefone do usuário. |
| `avatarUrl` | string | No | URL do avatar do usuário. |
| `availableOrganizations` | object[] | Yes | Organizações disponíveis para o usuário. |
| `whatsAppSelectedOrganizationId` | string | No | Organization id selected by the user for WhatsApp (Clerk public metadata). |

## Nested Fields

### `availableOrganizations`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `mainId` | string | Yes | Identificador da organização no clerk. |
| `name` | string | Yes | Nome da organização. |

