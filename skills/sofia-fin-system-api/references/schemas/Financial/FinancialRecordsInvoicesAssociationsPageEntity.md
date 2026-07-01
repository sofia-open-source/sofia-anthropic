# FinancialRecordsInvoicesAssociationsPageEntity

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
| `id` | string | Yes |  |
| `ownerOrganization` | string | Yes |  |
| `financialRecordId` | string | Yes |  |
| `invoiceId` | string | Yes |  |
| `createdAt` | any | Yes |  |
| `updatedAt` | any | Yes |  |
| `populatedFinancialRecord` | object | No | Loaded when populate includes financialRecord. |
| `populatedInvoice` | object | No | Loaded when populate includes invoice. |

#### `items.populatedFinancialRecord`

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

#### `items.populatedInvoice`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes | Invoice id. |
| `ownerOrganization` | string | Yes | Organization id. |
| `type` | enum: DEFAULT, NATIONAL | Yes | NFSe layout type. |
| `providerRef` | string | Yes | Internal reference sent to Focus NFe. |
| `providerStatus` | string | Yes | Focus NFe status after emission request. |
| `rpsNumber` | string | No | Focus NFe numero_rps (municipal NFSe). |
| `rpsSeries` | string | No | Focus NFe serie_rps (municipal NFSe). |
| `fiscalNoteNumber` | string | No | Focus NFe numero (issued NF number). |
| `verificationCode` | string | No | Focus NFe codigo_verificacao. |
| `nfseEmissionDate` | any | No | Focus NFe data_emissao (NFSe fiscal issuance). |
| `nfsePortalUrl` | string | No | Focus NFe url (prefeitura portal). |
| `nfseDanfseUrl` | string | No | Focus NFe url_danfse (DANFSe PDF). |
| `nfseProtocol` | string | No | Focus NFe protocolo (national DPS receipt protocol while processing). |
| `nfseXmlPath` | string | No | Focus NFe caminho_xml_nota_fiscal. |
| `nfseCancellationXmlPath` | string | No | Focus NFe caminho_xml_cancelamento when status is cancelado. |
| `nfseErrors` | object[] | No | Focus NFe erros[] (emission errors). |
| `legalEntityId` | string | Yes | Legal entity id. |
| `serviceCodeId` | string | Yes | Legal entity service code id. |
| `issueDate` | any | Yes | Issue datetime. |
| `serviceAmount` | number | Yes | Service amount. |
| `serviceDescription` | string | Yes | Service description / discrimination. |
| `issWithheld` | boolean | Yes | Whether ISS is withheld. |
| `serviceListItemCode` | string | No | LC116 item or national ISS code. |
| `serviceMunicipalityCode` | string | Yes | IBGE code where service is provided. |
| `tomadorCnpj` | string | No |  |
| `tomadorCpf` | string | No |  |
| `tomadorName` | string | No |  |
| `tomadorEmail` | string | No |  |
| `tomadorContactId` | string | No | Contact id used when issuing the invoice (search only; tomador fields are the snapshot). |
| `linkedToFinancialRecords` | boolean | Yes | Whether linked to financial records. |
| `cancelRequested` | boolean | No | Whether cancellation was requested at the fiscal provider. |
| `lastSyncAt` | any | No | Last Focus NFe consult sync attempt (used for sync queue prioritization). |
| `defaultTypeSpecific` | object | No |  |
| `nationalTypeSpecific` | object | No |  |
| `createdAt` | any | Yes |  |
| `updatedAt` | any | Yes |  |

### `pageInfo`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `pageIndex` | number | Yes |  |
| `pageSize` | number | Yes |  |
| `totalPages` | number | Yes |  |
| `totalItems` | number | Yes |  |

