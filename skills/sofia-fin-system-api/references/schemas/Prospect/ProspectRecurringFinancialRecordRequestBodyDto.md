# ProspectRecurringFinancialRecordRequestBodyDto

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `direction` | enum: IN, OUT | Yes | Direção do lançamento (entrada/saída). |
| `firstOccurrenceDate` |  | No | Data da primeira ocorrência. |
| `description` | string | Yes | Descrição do lançamento. |
| `contact` | string | No | Identificador do contato relacionado. |
| `subcategory` | string | Yes | Identificador da subcategoria. |
| `amount` | any | No | Valor do lançamento. |
| `tags` | string[] | No | Tags relacionadas. |
| `files` | string[] | No | Arquivos anexados. |
| `frequency` | enum: WEEKLY, MONTHLY, YEARLY | Yes | Frequência de repetição do lançamento. |
| `repetitionDay` | number | Yes | Dia de repetição do lançamento. |
| `repetitionMonth` | number | No | Mês de repetição do lançamento. |
| `onlyBusinessDays` | boolean | No | Indica se o lançamento será apenas em dias úteis. |
| `automaticCompletion` | boolean | No | Indica se o lançamento será completado automaticamente. |
| `isActive` | boolean | No | Indica se o lançamento recorrente está ativo. |
| `populatedContact` | object | No | Contato relacionado. |
| `populatedTags` | object[] | No | Tags relacionadas. |
| `populatedSubcategory` | object | No | Subcategoria relacionada. |
| `populatedFiles` | object[] | No | Arquivos anexados. |
| `observations` | string | No | Observações do lançamento recorrente. |
| `searchScore` | number | No |  |
| `externalId` | string | No | Identificador externo do lançamento recorrente. |
| `channel` | enum: WEB_APP, WHATSAPP, SYSTEM... | Yes | Canal de origem da operação |
| `numberOfRepetitions` | integer | Yes | Número de repetições. |

## Nested Fields

### `populatedContact`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes | Contact identifier. |
| `ownerOrganization` | string | Yes | Identifier of the organization that owns the contact. |
| `name` | string | Yes | Contact name. |
| `types` | string[] | Yes | Contact types. |
| `documentType` | enum: CNPJ, CPF | No | Contact document type. |
| `document` | string | No | Contact document. |
| `email` | string | No | Contact email. |
| `phone` | string | No | Contact phone. |
| `pixKeys` | string[] | Yes | Contact PIX keys. |
| `birthDate` | any | No | Contact birth date. |
| `origin` | enum: INDICATION, ADS, ORGANIC_SEARCH... | No | Contact origin. |
| `address` | object | No | Contact address. |
| `isNotIdentified` | boolean | Yes | Whether the contact is the unidentified contact. |
| `searchScore` | number | No | Contact search score. |
| `createdAt` | any | Yes | Creation date of the contact. |
| `updatedAt` | any | Yes | Last update date of the contact. |
| `importedAt` | any | No | Contact import date. |
| `importedBy` | string | No | Contact import source. |
| `externalId` | string | No | External identifier of the contact. |
| `observations` | string | No | Contact observations. |

#### `populatedContact.address`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `cep` | string | No | Contact address ZIP code (CEP). |
| `street` | string | No | Contact address street. |
| `number` | string | No | Contact address number. |
| `complement` | string | No | Contact address complement. |
| `neighborhood` | string | No | Contact address neighborhood. |
| `city` | string | No | Contact address city. |
| `state` | string | No | Contact address state. |
| `country` | string | No | Contact address country. |

### `populatedTags`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes | Tag identifier. |
| `ownerOrganization` | string | Yes | Identifier of the organization that owns the tag. |
| `name` | string | Yes | Tag name. |
| `createdAt` | any | Yes | Creation date of the tag. |
| `updatedAt` | any | Yes | Last update date of the tag. |
| `searchScore` | number | No | Text search score. |
| `importedAt` | any | No | Tag import date. |
| `importedBy` | string | No | Tag import source. |
| `externalId` | string | No | External identifier of the tag. |

### `populatedSubcategory`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes | Identificador da subcategoria. |
| `ownerOrganization` | string | Yes | Identificador da organização dona da subcategoria. |
| `name` | string | Yes | Nome da subcategoria. |
| `slug` | string | Yes | Slug da subcategoria. |
| `index` | number | Yes | Índice da subcategoria. |
| `category` | string | Yes | Identificador da categoria. |
| `populatedCategory` | object | No | Categoria da subcategoria. |
| `normalizedSubcategory` | string | No | Identificador da subcategoria normalizada. |
| `populatedNormalizedSubcategory` | object | No | Subcategoria normalizada. |
| `considerInDre` | boolean | Yes | Indica se a subcategoria deve ser exibida no DRE. |
| `isInternalTransfer` | boolean | No | Indica se a subcategoria representa uma transferência interna. |
| `description` | string | Yes | Descrição da subcategoria. |
| `active` | boolean | No | Indica se a subcategoria está ativa. |
| `searchScore` | number | No | Pontuação de busca da subcategoria. |
| `createdAt` | any | Yes | Data de criação da subcategoria. |
| `updatedAt` | any | Yes | Data de atualização da subcategoria. |
| `importedAt` | any | No | Data de importação da subcategoria. |
| `importedBy` | string | No | Origem da importação da subcategoria. |
| `externalId` | string | No | Identificador externo da subcategoria. |

#### `populatedSubcategory.populatedCategory`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes | Category identifier. |
| `direction` | enum: IN, OUT | Yes | Category direction (IN or OUT). |
| `index` | number | Yes | Category index. |
| `name` | string | Yes | Category name. |
| `slug` | string | Yes | Category slug. |
| `createdAt` | any | Yes | Creation date of the category. |
| `updatedAt` | any | Yes | Last update date of the category. |

#### `populatedSubcategory.populatedNormalizedSubcategory`

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

### `populatedFiles`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes | Identificador do arquivo. |
| `ownerOrganization` | string | Yes | Identificador da organização dona do arquivo. |
| `originalFileName` | string | Yes | Nome original do arquivo. |
| `mimeType` | string | Yes | Tipo MIME do arquivo. |
| `size` | number | Yes | Tamanho do arquivo em bytes. |
| `fileType` | enum: DEFAULT, FINANCIAL_RECORD, EXPORT... | Yes | Tipo do arquivo. |
| `objectName` | string | Yes | Nome do objeto no storage. |
| `status` | enum: PENDING, COMPLETED, FAILED... | Yes | Status do arquivo. |
| `caption` | string | No | Legenda do arquivo. |
| `createdAt` | any | Yes | Data de criação do arquivo. |
| `updatedAt` | any | Yes | Data de atualização do arquivo. |
| `deletedAt` | any | No | Data de exclusão do arquivo. |
| `url` | string | Yes | URL do arquivo. |
| `signedUrl` | string | Yes | URL assinada do arquivo. |

