# CreatedFinancialRecordRadarItemResultEntity

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `radarItem` | object | Yes |  |
| `appendedAsSubsequentRadarItem` | boolean | Yes | Indica se a criação foi anexada como um registro subsequente ao invés de criar um novo registro principal. |
| `autoExecute` | object | No |  |

## Nested Fields

### `radarItem`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes | Identificador do registro do radar. |
| `ownerOrganization` | string | Yes | Identificador da organização dona do registro. |
| `origin` | enum: WHATSAPP_AGENT, EMAIL_FORWARDING_INTEGRATION | Yes | Origem do registro. |
| `nature` | enum: WHATSAPP_MESSAGE, EMAIL_MESSAGE | Yes | Natureza do registro. |
| `status` | enum: PENDING, LINKED, ARCHIVED | Yes | Status do registro. |
| `folder` | enum: MAIN, SPAM | Yes | Pasta do registro. |
| `links` | string[] | Yes | Ids dos registros financeiros vinculados. |
| `bestSuggestedAction` | object | No | Melhor ação sugerida. |
| `finalBestSuggestedAction` | object | No | Ação sugerida final processada. |
| `extractedFinancialRecordData` | object | No | Dados extraídos do registro financeiro. |
| `subsequentRadarItems` | object[] | No | Registros subsequentes relacionados. |
| `whatsappMessageData` | object | No | Dados da mensagem WhatsApp. |
| `emailMessageData` | object | No | Dados da mensagem de email. |
| `autoExecute` | object | No | Auto-execute do registro. |
| `asyncActions` | object | No | Ações assíncronas do registro. |
| `createdAt` | any | Yes | Data de criação do registro. |
| `updatedAt` | any | Yes | Data de atualização do registro. |

#### `radarItem.bestSuggestedAction`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `operation` | enum: CREATE, CREATE_MANY, LINK_TO_THIS_RADAR_ITEM... | Yes | Operação sugerida. |
| `financialRecordRadarRawCreateFinancialRecordRequest` | object | No | Dados para criar registro financeiro. |
| `financialRecordRadarRawCreateManyFinancialRecordsRequest` | object | No | Dados para criar múltiplos registros financeiros. |
| `financialRecordRadarRawPartialUpdateFinancialRecordRequest` | object | No | Dados para atualizar parcialmente registro financeiro. |
| `financialRecordRadarRawLinkFinancialRecordToThisRadarItemRequest` | object | No | Dados para vincular registro financeiro ao registro do radar. |

#### `radarItem.finalBestSuggestedAction`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `operation` | enum: CREATE, CREATE_MANY, LINK_TO_THIS_RADAR_ITEM... | Yes | Operação sugerida. |
| `financialRecordRadarProcessedCreateFinancialRecordRequest` | object | No | Dados finais para criar registro financeiro. |
| `financialRecordRadarProcessedCreateManyFinancialRecordsRequest` | object | No | Dados finais para criar múltiplos registros financeiros. |
| `financialRecordRadarProcessedPartialUpdateFinancialRecordRequest` | object | No | Dados finais para atualizar parcialmente registro financeiro. |
| `financialRecordRadarProcessedLinkFinancialRecordToThisRadarItemRequest` | object | No | Dados finais para vincular registro financeiro ao registro do radar. |

#### `radarItem.extractedFinancialRecordData`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `direction` | enum: IN, OUT | No | Direção do lançamento (entrada/saída). |
| `dueDate` | any | No | Data de vencimento. |
| `contact` | string | No | Identificador do contato relacionado. |
| `description` | string | No | Descrição do lançamento. |
| `subcategory` | string | No | Identificador da subcategoria. |
| `amount` | string | No |  |
| `tags` | any[] | No | Tags relacionadas. |
| `competenceDate` | any | No | Data de competência. |
| `files` | string[] | No | Arquivos anexados. |
| `pixKey` | string | No | Chave PIX. |
| `boletoCode` | string | No | Código do boleto. |
| `pixCode` | string | No | Código PIX para pagamento/recebimento. |
| `invoiceNumber` | string | No | Número da nota fiscal. |
| `completed` | boolean | No | Indica se o lançamento foi concluído. |
| `cashDate` | any | No | Data de pagamento. |
| `account` | string | No | Identificador da conta. |
| `discount` | string | No |  |
| `finesAndInterest` | string | No |  |
| `contactHints` | string | No | Dicas de busca com nomes de contatos para facilitar buscas textuais. |
| `subcategoryHints` | string | No | Dicas de busca com nomes de subcategorias/categorias para facilitar buscas textuais. |
| `bankAccountHints` | string | No | Dicas de busca com nomes e números de contas bancárias para facilitar buscas textuais. |
| `tagsHints` | string | No | Dicas de busca com nomes de tags para facilitar buscas textuais. |
| `bankTransaction` | string | No | Identificador da transação bancária vinculada. |
| `installmentFinancialRecord` | string | No | Identificador do lançamento financeiro parcelado. |
| `installmentNumber` | number | No | Índice da parcela (1, 2, 3, etc.). |
| `recurringFinancialRecord` | string | No | Identificador do lançamento financeiro recorrente. |
| `recurringOccurrenceNumber` | integer | No | Occurrence index within the recurring template (0 = first occurrence). |
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
| `finalAmount` | any | No | Valor final do lançamento (calculado automaticamente). |
| `radarItem` | string | No | Identificador do item no radar que originou o lançamento. |
| `radarItems` | string[] | No | Ids de itens no radar relacionados. |

#### `radarItem.subsequentRadarItems`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `origin` | enum: WHATSAPP_AGENT, EMAIL_FORWARDING_INTEGRATION | Yes | Origem do registro subsequente. |
| `nature` | enum: WHATSAPP_MESSAGE, EMAIL_MESSAGE | Yes | Natureza do registro subsequente. |
| `bestSuggestedAction` | object | Yes | Melhor ação sugerida. |
| `whatsappMessageData` | object | No | Dados da mensagem WhatsApp. |
| `emailMessageData` | object | No | Dados da mensagem de email. |
| `createdAt` | any | Yes | Data de criação. |

#### `radarItem.whatsappMessageData`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `currentMessage` | object | Yes | Mensagem atual. |
| `lastMessages` | object[] | Yes | Últimas mensagens. |

#### `radarItem.emailMessageData`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `subject` | string | Yes | Assunto do email. |
| `currentMessage` | object | Yes | Mensagem atual. |
| `lastMessages` | object[] | Yes | Últimas mensagens. |

#### `radarItem.autoExecute`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `finalBestSuggestedAction` | object | No | Ação sugerida final processada. |
| `executionStatus` | enum: SUCCESS, FAILED | Yes | Status da execução do auto-execute. |
| `executionErrorMessage` | string | No | Mensagem de erro da execução do auto-execute. |
| `executedAt` | any | Yes | Data de execução do auto-execute. |
| `createdFinancialRecord` | object | No | Registro financeiro criado pelo auto-execute. |
| `partialUpdatedFinancialRecord` | object | No | Registro financeiro atualizado pelo auto-execute. |
| `bulkCreateJobRequest` | object | No | Solicitação de criação em massa criada pelo auto-execute. |
| `linkedFinancialRecord` | object | No | Registro financeiro vinculado pelo auto-execute. |

#### `radarItem.asyncActions`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `bulkCreateInProgress` | boolean | Yes | Indica se a criação em massa está em andamento. |

### `autoExecute`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `finalBestSuggestedAction` | object | No | Ação sugerida final processada. |
| `executionStatus` | enum: SUCCESS, FAILED | Yes | Status da execução do auto-execute. |
| `executionErrorMessage` | string | No | Mensagem de erro da execução do auto-execute. |
| `executedAt` | any | Yes | Data de execução do auto-execute. |
| `createdFinancialRecord` | object | No | Registro financeiro criado pelo auto-execute. |
| `partialUpdatedFinancialRecord` | object | No | Registro financeiro atualizado pelo auto-execute. |
| `bulkCreateJobRequest` | object | No | Solicitação de criação em massa criada pelo auto-execute. |
| `linkedFinancialRecord` | object | No | Registro financeiro vinculado pelo auto-execute. |

#### `autoExecute.finalBestSuggestedAction`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `operation` | enum: CREATE, CREATE_MANY, LINK_TO_THIS_RADAR_ITEM... | Yes | Operação sugerida. |
| `financialRecordRadarProcessedCreateFinancialRecordRequest` | object | No | Dados finais para criar registro financeiro. |
| `financialRecordRadarProcessedCreateManyFinancialRecordsRequest` | object | No | Dados finais para criar múltiplos registros financeiros. |
| `financialRecordRadarProcessedPartialUpdateFinancialRecordRequest` | object | No | Dados finais para atualizar parcialmente registro financeiro. |
| `financialRecordRadarProcessedLinkFinancialRecordToThisRadarItemRequest` | object | No | Dados finais para vincular registro financeiro ao registro do radar. |

#### `autoExecute.createdFinancialRecord`

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

#### `autoExecute.partialUpdatedFinancialRecord`

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

#### `autoExecute.bulkCreateJobRequest`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes | Identificador da solicitação de criação. |
| `resource` | enum: core_FinancialRecords, core_Contacts, core_BankAccounts... | Yes | Recurso a ser criado. |
| `nRows` | number | Yes | Número de linhas a serem criadas. |
| `fileId` | string | Yes | Identificador do arquivo com dados para criação. |
| `requesterUserId` | string | Yes | Identificador do usuário que solicitou a criação. |
| `radarItem` | string | No | Identificador do registro de radar que originou a criação em massa. |
| `createdAt` | any | Yes | Data de criação da solicitação de criação. |
| `updatedAt` | any | Yes | Data de atualização da solicitação de criação. |
| `deletedAt` | any | Yes | Data de exclusão da solicitação de criação. |

#### `autoExecute.linkedFinancialRecord`

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

