# BankTransactionEntity

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes | Bank transaction identifier. |
| `ownerOrganization` | string | Yes | Identifier of the organization that owns the bank transaction. |
| `bankAccount` | string | Yes | Bank account identifier of the transaction. |
| `bankAccountName` | string | Yes | Bank account name of the transaction. |
| `bankAccountNumber` | string | Yes | Bank account number of the transaction. |
| `bankAccountInstitutionName` | string | No | Bank institution name of the transaction. |
| `populatedBankAccount` | object | No | Populated bank account of the transaction. |
| `provider` | enum: PLUGGY, OFX, OTHER | Yes | Bank transaction provider. |
| `providerTransactionId` | string | Yes | Bank transaction identifier in the provider. |
| `amountInBrl` | any | No | Transaction amount in cents (BRL). |
| `amountInBrlVariations` | string | Yes | Amount variations of the bank transaction in cents. |
| `date` |  | Yes | Bank transaction date. |
| `dateVariations` | string | Yes | Date variations of the bank transaction. |
| `type` | enum: DEBIT, CREDIT | Yes | Bank transaction type (credit or debit). |
| `typeVariations` | string | Yes | Type variations of the bank transaction. |
| `description` | string | No | Bank transaction description. |
| `status` | enum: PENDING, POSTED | Yes | Bank transaction status. |
| `ignored` | boolean | Yes | Whether the bank transaction should be ignored. |
| `reconciled` | boolean | No | Whether the transaction has been reconciled with financial records. |
| `financialRecords` | string[] | No | IDs of financial records linked to this bank transaction. |
| `populatedFinancialRecords` | object[] | No | Populated financial records linked to this bank transaction (present when populate includes financialRecords). |
| `aiSuggestion` | object | No | AI-generated best action suggestion for this bank transaction. |
| `ofxJobRequestId` | string | No | Identificador da solicitação de importação OFX relacionada. |
| `ofxJobExecutionId` | string | No | Identificador da execução de importação OFX relacionada. |
| `pluggyJobRequestId` | string | No | Identificador da solicitação de importação Pluggy relacionada. |
| `pluggyJobExecutionId` | string | No | Identificador da execução de importação Pluggy relacionada. |
| `externalId` | string | No | Identificador externo da movimentação financeira. |
| `amount` | number | No | Valor da movimentação financeira. |
| `amountInAccountCurrency` | number | No | Valor da movimentação financeira na moeda da conta. |
| `balance` | number | No | Saldo após a movimentação financeira. |
| `currencyCode` | string | No | Código da moeda da movimentação financeira. |
| `category` | string | No | Categoria da movimentação financeira. |
| `providerCode` | string | No | Código do provedor da movimentação financeira. |
| `paymentData` | object | No | Dados de pagamento da movimentação financeira. |
| `creditCardMetadata` | object | No | Metadados de cartão de crédito da movimentação financeira. |
| `merchant` | object | No | Dados do comerciante da movimentação financeira. |
| `categoryId` | string | No | Identificador da categoria da movimentação financeira. |
| `operationType` | string | No | Tipo de operação da movimentação financeira. |
| `searchScore` | number | No | Pontuação de busca da movimentação financeira. |
| `createdAt` |  | Yes | Data de criação da movimentação financeira. |
| `updatedAt` |  | Yes | Data de atualização da movimentação financeira. |
| `importedAt` | any | No | Data de importação da movimentação financeira. |
| `importedBy` | string | No | Origem da importação da movimentação financeira. |
| `importGlobalIndex` | number | No | Índice global da movimentação financeira no arquivo de importação. |

## Nested Fields

### `populatedBankAccount`

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

#### `populatedBankAccount.populatedInstitution`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `sofiaId` | string | Yes | Sofia identifier for the bank institution |
| `pluggyIds` | string[] | Yes | Pluggy identifiers for the bank institution |
| `name` | string | Yes | Name of the bank institution |
| `imageUrl` | string | Yes | URL of the bank institution image |

#### `populatedBankAccount.populatedAutomaticStatus`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `isSyncing` | boolean | Yes | Indica se a conta bancária está sincronizando. |
| `error` | object | No | Erro da sincronização da conta bancária. |
| `lastSyncAt` | any | No | Data da última sincronização da conta bancária. |
| `nextSyncAt` | any | No | Data da próxima sincronização da conta bancária. |

### `populatedFinancialRecords`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes | Identificador do lançamento financeiro. |
| `ownerOrganization` | string | Yes | Identificador da organização dona do lançamento. |
| `direction` | enum: IN, OUT | Yes | Direção do lançamento (entrada/saída). |
| `dueDate` | any | No | Data de vencimento. |
| `dueDateVariations` | string | No | Variações da data de vencimento. |
| `contact` | string | Yes | Identificador do contato relacionado. |
| `description` | string | Yes | Descrição do lançamento. |
| `subcategory` | string | Yes | Identificador da subcategoria. |
| `amount` | any | No | Valor do lançamento. É o valor em centavos. Exemplo: 10032 para R$ 100,32 |
| `amountVariations` | string | No | Variações do valor do lançamento. |
| `tags` | string[] | Yes | Tags relacionadas. |
| `competenceDate` | any | No | Data de competência. |
| `competenceDateVariations` | string | No | Variações da data de competência. |
| `files` | string[] | Yes | Arquivos anexados. |
| `radarItems` | string[] | Yes | Ids de itens no radar relacionados. |
| `pixKey` | string | No | Chave PIX. |
| `boletoCode` | string | No | Código do boleto. |
| `pixCode` | string | No | Código PIX para pagamento/recebimento. |
| `invoiceNumber` | string | No | Número da nota fiscal. |
| `completed` | boolean | Yes | Indica se o lançamento foi concluído. |
| `cashDate` | any | No | Data de pagamento. |
| `cashDateVariations` | string | No | Variações da data de pagamento. |
| `account` | string | No | Identificador da conta. |
| `discount` | any | No | Valor do desconto. É o valor em centavos. Exemplo: 1000 para R$ 10,00 |
| `finesAndInterest` | any | No | Valor de multas e juros. É o valor em centavos. Exemplo: 1000 para R$ 10,00 |
| `finalAmount` | any | No | Valor final do lançamento. É o valor em centavos. Exemplo: 10000 para R$ 100,00 |
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
| `createdAt` | any | No | Data de criação do lançamento. |
| `updatedAt` | any | No | Data de atualização do lançamento. |
| `populatedFiles` | object[] | No | Arquivos anexados. |
| `populatedSubcategory` | object | No | Subcategoria do lançamento. |
| `populatedContact` | object | No | Contato relacionado. |
| `populatedTags` | object[] | No | Tags relacionadas. |
| `populatedAccount` | object | No | Conta relacionada. |
| `populatedGroups` | object[] | No | Grupos de lançamentos financeiros relacionados. |
| `searchScore` | number | No | Pontuação de busca do lançamento. |
| `observations` | string | No | Observações do lançamento. |
| `importedAt` | any | No | Data de importação do lançamento. |
| `importedBy` | string | No | Origem da importação do lançamento. |
| `importGlobalIndex` | number | No | Índice global do lançamento financeiro no arquivo de importação. |
| `externalId` | string | No | Identificador externo do lançamento financeiro. |

#### `populatedFinancialRecords.populatedFiles`

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

#### `populatedFinancialRecords.populatedSubcategory`

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

#### `populatedFinancialRecords.populatedContact`

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

#### `populatedFinancialRecords.populatedTags`

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

#### `populatedFinancialRecords.populatedAccount`

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

#### `populatedFinancialRecords.populatedGroups`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes |  |
| `ownerOrganization` | string | Yes |  |
| `type` | enum: INTERNAL_TRANSFER, OTHER | Yes |  |
| `description` | string | Yes |  |
| `financialRecords` | string[] | No | Ids de lançamentos financeiros relacionados. |

### `aiSuggestion`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `operation` | enum: CREATE, LINK | Yes |  |
| `linkData` | object | No |  |
| `createData` | object | Yes |  |

#### `aiSuggestion.linkData`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `financialRecordId` | string | Yes |  |
| `populatedFinancialRecord` | object | No | Populated financial record for the LINK suggestion (present when populate includes aiSuggestion.linkedFinancialRecord). |

#### `aiSuggestion.createData`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `financialRecord` | object | Yes |  |
| `populatedContact` | object | No | Populated contact for the CREATE suggestion (present when populate includes aiSuggestion.contact). |
| `populatedSubcategory` | object | No | Populated subcategory for the CREATE suggestion (present when populate includes aiSuggestion.subcategory). |

### `paymentData`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `payer` | object | No |  |
| `receiver` | object | No |  |
| `receiverReferenceId` | string | No |  |
| `paymentMethod` | string | No |  |
| `referenceNumber` | string | No |  |
| `reason` | string | No |  |
| `boletoMetadata` | object | No |  |

#### `paymentData.payer`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `documentNumber` | object | No |  |
| `name` | string | No |  |
| `accountNumber` | string | No |  |
| `branchNumber` | string | No |  |
| `routingNumber` | string | No |  |

#### `paymentData.receiver`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `documentNumber` | object | No |  |
| `name` | string | No |  |
| `accountNumber` | string | No |  |
| `branchNumber` | string | No |  |
| `routingNumber` | string | No |  |

#### `paymentData.boletoMetadata`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `digitableLine` | string | No |  |
| `barcode` | string | No |  |
| `baseAmount` | number | No |  |
| `penaltyAmount` | number | No |  |
| `interestAmount` | number | No |  |
| `discountAmount` | number | No |  |

### `creditCardMetadata`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `installmentNumber` | number | No |  |
| `totalInstallments` | number | No |  |
| `totalAmount` | number | No |  |
| `payeeMCC` | number | No |  |
| `purchaseDate` | any | No |  |

### `merchant`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `name` | string | No |  |
| `businessName` | string | No |  |
| `cnpj` | string | No |  |
| `cnae` | string | No |  |
| `category` | string | No |  |

