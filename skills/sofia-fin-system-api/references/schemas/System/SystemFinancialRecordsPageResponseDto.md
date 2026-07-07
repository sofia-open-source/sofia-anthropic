# SystemFinancialRecordsPageResponseDto

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `items` | object[] | Yes |  |
| `pageInfo` | object | Yes |  |
| `exportedExcelFile` | object | No | Arquivo Excel exportado. É gerado se generateExcelExport=true. Contém os primeiros 2000 lançamentos financeiros para o filtro em questão. |
| `exportedPdfTableFile` | object | No | Arquivo PDF exportado com layout em tabela. É gerado se generatePdfTableExport=true. Contém os primeiros 2000 lançamentos financeiros para o filtro em questão. |
| `exportedPdfListFile` | object | No | Arquivo PDF exportado com layout em lista. É gerado se generatePdfListExport=true. Contém os primeiros 2000 lançamentos financeiros para o filtro em questão. |
| `exportedFilesObservations` | string | No | Observações sobre os arquivos exportados. |
| `aggregatedResultReport` | object | Yes | Relatório agregado de resultados. Considera TODOS os lançamentos financeiros para o filtro em questão e não apenas os da página ou os primeiros 2000. |

## Nested Fields

### `items`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes | Identificador do lançamento financeiro. |
| `ownerOrganization` | string | Yes | Identificador da organização dona do lançamento. |
| `direction` | enum: IN, OUT | Yes | Direção do lançamento (entrada/saída). |
| `dueDate` | string | No |  |
| `dueDateVariations` | string | No | Variações da data de vencimento. |
| `contact` | string | Yes | Identificador do contato relacionado. |
| `description` | string | Yes | Descrição do lançamento. |
| `subcategory` | string | Yes | Identificador da subcategoria. |
| `amount` | string | Yes |  |
| `amountVariations` | string | No | Variações do valor do lançamento. |
| `tags` | string[] | Yes | Tags relacionadas. |
| `competenceDate` | string | No |  |
| `competenceDateVariations` | string | No | Variações da data de competência. |
| `files` | string[] | Yes | Arquivos anexados. |
| `radarItems` | string[] | Yes | Ids de itens no radar relacionados. |
| `pixKey` | string | No | Chave PIX. |
| `boletoCode` | string | No | Código do boleto. |
| `pixCode` | string | No | Código PIX para pagamento/recebimento. |
| `invoiceNumber` | string | No | Número da nota fiscal. |
| `completed` | boolean | Yes | Indica se o lançamento foi concluído. |
| `cashDate` | string | No |  |
| `cashDateVariations` | string | No | Variações da data de pagamento. |
| `account` | string | No | Identificador da conta. |
| `discount` | string | No |  |
| `finesAndInterest` | string | No |  |
| `finalAmount` | string | Yes |  |
| `finalAmountVariations` | string | No | Variações do valor final do lançamento. |
| `contactHints` | string | No | Dicas de busca com nomes de contatos para facilitar buscas textuais. |
| `subcategoryHints` | string | No | Dicas de busca com nomes de subcategorias/categorias para facilitar buscas textuais. |
| `bankAccountHints` | string | No | Dicas de busca com nomes e números de contas bancárias para facilitar buscas textuais. |
| `tagsHints` | string | No | Dicas de busca com nomes de tags para facilitar buscas textuais. |
| `reconciled` | boolean | Yes | Indica se foi reconciliado com uma transação bancária. |
| `bankTransaction` | string | No | Identificador da transação bancária vinculada. |
| `installmentFinancialRecord` | string | No | Identificador do lançamento financeiro parcelado. |
| `installmentNumber` | number | No | Índice da parcela (1, 2, 3, etc.). |
| `recurringFinancialRecord` | string | No | Identificador do lançamento financeiro recorrente. |
| `recurringOccurrenceNumber` | integer | No | Occurrence index within the recurring template (0 = first occurrence). |
| `createdAt` | string | Yes | Creation date of the financial record. |
| `updatedAt` | string | Yes | Last update date of the financial record. |
| `populatedFiles` | object[] | No | Arquivos anexados. |
| `populatedSubcategory` | object | No | Subcategoria do lançamento. |
| `populatedContact` | object | No | Contato relacionado. |
| `populatedTags` | object[] | No | Tags relacionadas. |
| `populatedAccount` | object | No | Conta relacionada. |
| `populatedGroups` | object[] | No | Grupos de lançamentos financeiros relacionados. |
| `searchScore` | number | No | Pontuação de busca do lançamento. |
| `observations` | string | No | Observações do lançamento. |
| `importedAt` | string | No | Financial record import date. |
| `importedBy` | string | No | Origem da importação do lançamento. |
| `importGlobalIndex` | number | No | Índice global do lançamento financeiro no arquivo de importação. |
| `externalId` | string | No | Identificador externo do lançamento financeiro. |

#### `items.populatedFiles`

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

#### `items.populatedSubcategory`

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

#### `items.populatedContact`

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

#### `items.populatedTags`

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

#### `items.populatedAccount`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes | Identificador da conta bancária. |
| `ownerOrganization` | string | Yes | Identificador da organização dona da conta bancária. |
| `name` | string | Yes | Nome da conta bancária. |
| `type` | enum: MONEY, CHECKING, SAVINGS... | Yes | Tipo da conta bancária. |
| `number` | string | Yes | Número da conta ou cartão. |
| `considerInCashFlow` | boolean | Yes | Indica se a conta deve ser considerada nos cálculos de fluxo de caixa. |
| `isAutomatic` | boolean | Yes | Indica se a conta é automática ou manual. |
| `isDefault` | boolean | Yes | Indica se a conta é a padrão. |
| `initialBalanceDate` | any | No | Data do saldo inicial da conta bancária. |
| `initialBalanceAmount` | any | No | Valor do saldo inicial. |
| `institution` | string | No | Instituição financeira. |
| `institutionName` | string | No | Nome da instituição financeira. |
| `active` | boolean | Yes | Indica se a conta está ativa. |
| `provider` | enum: PLUGGY, OFX, OTHER | No | Fornecedor da conta bancária. |
| `providerAccountId` | string | No | Identificador da conta bancária no fornecedor. |
| `providerItemId` | string | No | Identificador do item de conexão do fornecedor. |
| `searchScore` | number | No | Pontuação de busca. |
| `createdAt` | any | Yes | Data de criação da conta bancária. |
| `updatedAt` | any | Yes | Data de atualização da conta bancária. |
| `populatedInstitution` | object | No | Instituição financeira populada. |
| `populatedAutomaticStatus` | object | No | Status se conta bancária automática. |
| `importedAt` | any | No | Data de importação da conta bancária. |
| `importedBy` | string | No | Origem da importação da conta bancária. |
| `externalId` | string | No | Identificador externo da conta bancária. |

#### `items.populatedGroups`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes |  |
| `ownerOrganization` | string | Yes |  |
| `type` | enum: INTERNAL_TRANSFER, OTHER | Yes |  |
| `description` | string | Yes |  |
| `financialRecords` | string[] | No | Ids de lançamentos financeiros relacionados. |

### `pageInfo`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `pageIndex` | number | Yes |  |
| `pageSize` | number | Yes |  |
| `totalPages` | number | Yes |  |
| `totalItems` | number | Yes |  |

### `exportedExcelFile`

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
| `createdAt` | string | Yes | File creation date. |
| `updatedAt` | string | Yes | File last update date. |
| `deletedAt` | string | Yes | File deletion date. |
| `url` | string | Yes | URL do arquivo. |
| `signedUrl` | string | Yes | URL assinada do arquivo. |

### `exportedPdfTableFile`

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
| `createdAt` | string | Yes | File creation date. |
| `updatedAt` | string | Yes | File last update date. |
| `deletedAt` | string | Yes | File deletion date. |
| `url` | string | Yes | URL do arquivo. |
| `signedUrl` | string | Yes | URL assinada do arquivo. |

### `exportedPdfListFile`

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
| `createdAt` | string | Yes | File creation date. |
| `updatedAt` | string | Yes | File last update date. |
| `deletedAt` | string | Yes | File deletion date. |
| `url` | string | Yes | URL do arquivo. |
| `signedUrl` | string | Yes | URL assinada do arquivo. |

### `aggregatedResultReport`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `income` | string | Yes | Soma total dos valores de entrada em centavos. |
| `outcome` | string | Yes | Soma total dos valores de saída em centavos |
| `resultAbsoluteValue` | string | Yes | Valor absoluto da diferença entre entrada e saída em centavos. |
| `resultDirection` | enum: IN, OUT | Yes | Direção do resultado (entrada/saída). |

