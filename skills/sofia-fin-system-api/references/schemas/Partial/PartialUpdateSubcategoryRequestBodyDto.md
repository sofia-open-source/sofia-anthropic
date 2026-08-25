# PartialUpdateSubcategoryRequestBodyDto

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `name` | string | No | Nome da subcategoria. |
| `slug` | string | No | Slug da subcategoria. |
| `index` | number | No | Índice da subcategoria. |
| `category` | string | No |  |
| `populatedCategory` | object | No | Categoria da subcategoria. |
| `normalizedSubcategory` | string | No |  |
| `populatedNormalizedSubcategory` | object | No | Subcategoria normalizada. |
| `considerInDre` | boolean | No | Indica se a subcategoria deve ser exibida no DRE. |
| `isInternalTransfer` | boolean | No |  |
| `description` | string | No | Descrição da subcategoria. |
| `active` | boolean | No |  |
| `searchScore` | number | No | Pontuação de busca da subcategoria. |
| `importedAt` | any | No | Data de importação da subcategoria. |
| `importedBy` | string | No | Origem da importação da subcategoria. |
| `externalId` | string | No | Identificador externo da subcategoria. |
| `channel` | enum: WEB_APP, WHATSAPP, SYSTEM... | Yes | Canal de origem da operação |

## Nested Fields

### `populatedCategory`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes | Category identifier. |
| `direction` | enum: IN, OUT | Yes | Category direction (IN or OUT). |
| `index` | number | Yes | Category index. |
| `name` | string | Yes | Category name. |
| `slug` | string | Yes | Category slug. |
| `createdAt` | any | Yes | Creation date of the category. |
| `updatedAt` | any | Yes | Last update date of the category. |

### `populatedNormalizedSubcategory`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes | Identificador da subcategoria normalizada. |
| `name` | string | Yes | Nome da subcategoria. |
| `slug` | string | Yes | Slug da subcategoria. |
| `index` | number | Yes | Índice da subcategoria. |
| `category` | string | Yes | Identificador da categoria. |
| `populatedCategory` | object | No | Categoria da subcategoria. |
| `considerInDre` | boolean | Yes | Indica se a subcategoria deve ser exibida no DRE. |
| `isInternalTransfer` | boolean | No | Indica se a subcategoria representa uma transferência interna. |
| `description` | string | Yes | Descrição da subcategoria. |
| `createdAt` | any | Yes | Data de criação da subcategoria. |
| `updatedAt` | any | Yes | Data de atualização da subcategoria. |

#### `populatedNormalizedSubcategory.populatedCategory`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes | Category identifier. |
| `direction` | enum: IN, OUT | Yes | Category direction (IN or OUT). |
| `index` | number | Yes | Category index. |
| `name` | string | Yes | Category name. |
| `slug` | string | Yes | Category slug. |
| `createdAt` | any | Yes | Creation date of the category. |
| `updatedAt` | any | Yes | Last update date of the category. |

