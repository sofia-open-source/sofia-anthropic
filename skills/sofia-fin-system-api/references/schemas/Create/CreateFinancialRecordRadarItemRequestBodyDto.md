# CreateFinancialRecordRadarItemRequestBodyDto

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `ownerOrganization` | string | Yes | Identificador da organização dona do registro. |
| `origin` | enum: WHATSAPP_AGENT, EMAIL_FORWARDING_INTEGRATION | Yes | Origem do registro. |
| `nature` | enum: WHATSAPP_MESSAGE, EMAIL_MESSAGE | Yes | Natureza do registro. |
| `status` | enum: PENDING, LINKED, ARCHIVED | Yes | Status do registro. |
| `folder` | enum: MAIN, SPAM | Yes | Pasta do registro. |
| `delayedTo` |  | No | Data para a qual o registro foi adiado. |
| `bestSuggestedAction` | object | No | Melhor ação sugerida. |
| `whatsappMessageData` | object | No | Dados da mensagem WhatsApp. |
| `emailMessageData` | object | No | Dados da mensagem de email. |

## Nested Fields

### `bestSuggestedAction`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `operation` | enum: CREATE, CREATE_MANY, LINK_TO_THIS_RADAR_ITEM... | Yes | Operação sugerida. |
| `financialRecordRadarRawCreateFinancialRecordRequest` | object | No | Dados para criar registro financeiro. |
| `financialRecordRadarRawCreateManyFinancialRecordsRequest` | object | No | Dados para criar múltiplos registros financeiros. |
| `financialRecordRadarRawPartialUpdateFinancialRecordRequest` | object | No | Dados para atualizar parcialmente registro financeiro. |
| `financialRecordRadarRawLinkFinancialRecordToThisRadarItemRequest` | object | No | Dados para vincular registro financeiro ao registro do radar. |

#### `bestSuggestedAction.financialRecordRadarRawCreateFinancialRecordRequest`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `direction` | enum: IN, OUT | Yes | Direção do lançamento (entrada/saída). |
| `dueDate` | any | No | Data de vencimento. |
| `contact` | string | No | Identificador do contato relacionado. |
| `description` | string | Yes | Descrição do lançamento. |
| `subcategory` | string | Yes | Identificador da subcategoria. |
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

#### `bestSuggestedAction.financialRecordRadarRawCreateManyFinancialRecordsRequest`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `fileId` | string | Yes |  |
| `nRows` | number | Yes | Número de linhas a serem criadas. |

#### `bestSuggestedAction.financialRecordRadarRawPartialUpdateFinancialRecordRequest`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | object | Yes |  |
| `data` | object | Yes |  |
| `extractedFinancialRecordData` | object | No |  |

#### `bestSuggestedAction.financialRecordRadarRawLinkFinancialRecordToThisRadarItemRequest`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `financialRecord` | string | Yes | ID do registro financeiro a ser vinculado. |
| `extractedFinancialRecordData` | object | Yes |  |

### `whatsappMessageData`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `currentMessage` | object | Yes | Mensagem atual. |
| `lastMessages` | object[] | Yes | Últimas mensagens. |

#### `whatsappMessageData.currentMessage`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes | ID da mensagem. |
| `timestamp` | string | Yes | Timestamp da mensagem. |
| `phone` | string | Yes | Telefone do remetente. |
| `name` | string | No | Nome do remetente. |
| `content` | string | No | Conteúdo da mensagem. |
| `files` | object[] | No | Arquivos anexados. |
| `quoted` | object | No | Mensagem citada. |

#### `whatsappMessageData.lastMessages`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes | ID da mensagem. |
| `timestamp` | string | Yes | Timestamp da mensagem. |
| `phone` | string | Yes | Telefone do remetente. |
| `name` | string | No | Nome do remetente. |
| `content` | string | No | Conteúdo da mensagem. |
| `files` | object[] | No | Arquivos anexados. |
| `quoted` | object | No | Mensagem citada. |

### `emailMessageData`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `subject` | string | Yes | Assunto do email. |
| `currentMessage` | object | Yes | Mensagem atual. |
| `lastMessages` | object[] | Yes | Últimas mensagens. |

#### `emailMessageData.currentMessage`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes | ID da mensagem. |
| `timestamp` | string | Yes | Timestamp da mensagem. |
| `email` | string | Yes | Email do remetente. |
| `name` | string | No | Nome do remetente. |
| `content` | string | No | Conteúdo da mensagem. |
| `files` | object[] | No | Arquivos anexados. |

#### `emailMessageData.lastMessages`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes | ID da mensagem. |
| `timestamp` | string | Yes | Timestamp da mensagem. |
| `email` | string | Yes | Email do remetente. |
| `name` | string | No | Nome do remetente. |
| `content` | string | No | Conteúdo da mensagem. |
| `files` | object[] | No | Arquivos anexados. |

