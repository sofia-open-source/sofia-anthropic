# ShouldAiSuggestActionRequestBodyDto

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `requester` | object | Yes | User making the request. |
| `transactionData` | object | Yes | Bank transaction data. |

## Nested Fields

### `requester`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes |  |
| `primaryEmail` | string (email) | Yes |  |
| `primaryPhoneNumber` | string | Yes |  |
| `firstName` | string | Yes |  |
| `lastName` | string | Yes |  |
| `organization` | object | No |  |

#### `requester.organization`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes |  |
| `name` | string | Yes |  |
| `type` | enum: LEAF, GROUP | Yes |  |
| `role` | enum: org:admin, org:member | Yes |  |
| `onFinSystem` | boolean | No |  |
| `parent` | object | No |  |
| `children` | object[] | No |  |

### `transactionData`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `bankAccount` | string | Yes | Bank account identifier of the transaction. |
| `provider` | enum: PLUGGY, OFX, OTHER | Yes | Bank transaction provider. |
| `providerTransactionId` | string | Yes | Bank transaction identifier in the provider. |
| `amountInBrl` | string | Yes | Transaction amount in cents (BRL). |
| `date` | any | Yes | Bank transaction date. |
| `type` | enum: DEBIT, CREDIT | Yes | Bank transaction type (credit or debit). |
| `description` | string | No | Bank transaction description. |
| `status` | enum: PENDING, POSTED | Yes | Bank transaction status. |
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
| `importedAt` | any | No | Data de importação da movimentação financeira. |
| `importedBy` | string | No | Origem da importação da movimentação financeira. |
| `importGlobalIndex` | number | No | Índice global da movimentação financeira no arquivo de importação. |

#### `transactionData.populatedFinancialRecords`

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
| `recurringOccurrenceNumber` | integer | No | Occurrence index within the recurring template (0 = first occurrence). |
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

#### `transactionData.aiSuggestion`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `operation` | enum: CREATE, LINK | Yes |  |
| `linkData` | object | No |  |
| `createData` | object | Yes |  |

#### `transactionData.paymentData`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `payer` | object | No |  |
| `receiver` | object | No |  |
| `receiverReferenceId` | string | No |  |
| `paymentMethod` | string | No |  |
| `referenceNumber` | string | No |  |
| `reason` | string | No |  |
| `boletoMetadata` | object | No |  |

#### `transactionData.creditCardMetadata`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `installmentNumber` | number | No |  |
| `totalInstallments` | number | No |  |
| `totalAmount` | number | No |  |
| `payeeMCC` | number | No |  |
| `purchaseDate` | any | No |  |

#### `transactionData.merchant`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `name` | string | No |  |
| `businessName` | string | No |  |
| `cnpj` | string | No |  |
| `cnae` | string | No |  |
| `category` | string | No |  |

