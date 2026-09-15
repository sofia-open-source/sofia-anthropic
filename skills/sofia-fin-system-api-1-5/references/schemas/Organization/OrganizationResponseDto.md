# OrganizationResponseDto

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes | Identificador da organização. |
| `name` | string | Yes | Nome da organização. |
| `slug` | string | Yes | Slug da organização. |
| `type` | enum: LEAF, GROUP | Yes | Tipo da organização. |
| `document` | string | No | Documento da organização. Geralmente CNPJ. |
| `imageUrl` | string | No | URL da imagem do logo da organização. |
| `populatedSubscription` | any | No | Subscription populada (deprecated, use admin-api). |
| `parent` | string | No | Identificador da organização pai. |
| `populatedParent` | object | No | Organização pai. |
| `children` | string[] | No | Identificadores das organizações filhas. |
| `populatedChildren` | object[] | No | Organizações filhas. |
| `createdAt` |  | Yes | Data de criação da organização. |
| `updatedAt` |  | Yes | Data de atualização da organização. |
| `description` | string | No | Descrição da organização. |
| `groupSettings` | object | No | Configurações do grupo. |
| `publicMetadata` | object | No | Metadados públicos da organização. |

## Nested Fields

### `populatedParent`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes | Identificador da organização. |
| `name` | string | Yes | Nome da organização. |
| `slug` | string | Yes | Slug da organização. |
| `type` | enum: LEAF, GROUP | Yes | Tipo da organização. |
| `document` | string | No | Documento da organização. Geralmente CNPJ. |
| `imageUrl` | string | No | URL da imagem do logo da organização. |
| `description` | string | No | Descrição da organização. |
| `createdAt` | any | Yes | Data de criação da organização. |
| `updatedAt` | any | Yes | Data de atualização da organização. |

### `populatedChildren`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes | Identificador da organização. |
| `name` | string | Yes | Nome da organização. |
| `slug` | string | Yes | Slug da organização. |
| `type` | enum: LEAF, GROUP | Yes | Tipo da organização. |
| `document` | string | No | Documento da organização. Geralmente CNPJ. |
| `imageUrl` | string | No | URL da imagem do logo da organização. |
| `description` | string | No | Descrição da organização. |
| `createdAt` | any | Yes | Data de criação da organização. |
| `updatedAt` | any | Yes | Data de atualização da organização. |

### `groupSettings`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `sharedContacts` | boolean | Yes | Compartilhamento de contatos. |
| `sharedTags` | boolean | Yes | Compartilhamento de tags. |
| `sharedSubcategories` | boolean | Yes | Compartilhamento de subcategorias. |

