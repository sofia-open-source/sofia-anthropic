# FinancialRecordRadarItemsPageResponseDto

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `items` | object[] | Yes |  |
| `pageInfo` | object | Yes |  |

## Nested Fields

### `items`

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
| `createdAt` | string | Yes | Creation date of the radar item. |
| `updatedAt` | string | Yes | Last update date of the radar item. |

#### `items.bestSuggestedAction`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `operation` | enum: CREATE, CREATE_MANY, LINK_TO_THIS_RADAR_ITEM... | Yes | Operação sugerida. |
| `financialRecordRadarRawCreateFinancialRecordRequest` | object | No | Dados para criar registro financeiro. |
| `financialRecordRadarRawCreateManyFinancialRecordsRequest` | object | No | Dados para criar múltiplos registros financeiros. |
| `financialRecordRadarRawPartialUpdateFinancialRecordRequest` | object | No | Dados para atualizar parcialmente registro financeiro. |
| `financialRecordRadarRawLinkFinancialRecordToThisRadarItemRequest` | object | No | Dados para vincular registro financeiro ao registro do radar. |

#### `items.finalBestSuggestedAction`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `operation` | enum: CREATE, CREATE_MANY, LINK_TO_THIS_RADAR_ITEM... | Yes | Operação sugerida. |
| `financialRecordRadarProcessedCreateFinancialRecordRequest` | object | No | Dados finais para criar registro financeiro. |
| `financialRecordRadarProcessedCreateManyFinancialRecordsRequest` | object | No | Dados finais para criar múltiplos registros financeiros. |
| `financialRecordRadarProcessedPartialUpdateFinancialRecordRequest` | object | No | Dados finais para atualizar parcialmente registro financeiro. |
| `financialRecordRadarProcessedLinkFinancialRecordToThisRadarItemRequest` | object | No | Dados finais para vincular registro financeiro ao registro do radar. |

#### `items.extractedFinancialRecordData`

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

#### `items.subsequentRadarItems`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `origin` | enum: WHATSAPP_AGENT, EMAIL_FORWARDING_INTEGRATION | Yes | Origem do registro subsequente. |
| `nature` | enum: WHATSAPP_MESSAGE, EMAIL_MESSAGE | Yes | Natureza do registro subsequente. |
| `bestSuggestedAction` | object | Yes | Melhor ação sugerida. |
| `whatsappMessageData` | object | No | Dados da mensagem WhatsApp. |
| `emailMessageData` | object | No | Dados da mensagem de email. |
| `createdAt` | any | Yes | Data de criação. |

#### `items.whatsappMessageData`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `currentMessage` | object | Yes | Mensagem atual. |
| `lastMessages` | object[] | Yes | Últimas mensagens. |

#### `items.emailMessageData`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `subject` | string | Yes | Assunto do email. |
| `currentMessage` | object | Yes | Mensagem atual. |
| `lastMessages` | object[] | Yes | Últimas mensagens. |

#### `items.autoExecute`

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

#### `items.asyncActions`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `bulkCreateInProgress` | boolean | Yes | Indica se a criação em massa está em andamento. |

### `pageInfo`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `pageIndex` | number | Yes |  |
| `pageSize` | number | Yes |  |
| `totalPages` | number | Yes |  |
| `totalItems` | number | Yes |  |

