# FinancialRecordsInvoicesAssociationEntity

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes |  |
| `ownerOrganization` | string | Yes |  |
| `financialRecordId` | string | Yes |  |
| `invoiceId` | string | Yes |  |
| `createdAt` |  | Yes |  |
| `updatedAt` |  | Yes |  |
| `populatedFinancialRecord` | object | No | Loaded when populate includes financialRecord. |
| `populatedInvoice` | object | No | Loaded when populate includes invoice. |

## Nested Fields

### `populatedFinancialRecord`

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

#### `populatedFinancialRecord.populatedFiles`

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

#### `populatedFinancialRecord.populatedSubcategory`

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

#### `populatedFinancialRecord.populatedContact`

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

#### `populatedFinancialRecord.populatedTags`

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

#### `populatedFinancialRecord.populatedAccount`

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

#### `populatedFinancialRecord.populatedGroups`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes |  |
| `ownerOrganization` | string | Yes |  |
| `type` | enum: INTERNAL_TRANSFER, OTHER | Yes |  |
| `description` | string | Yes |  |
| `financialRecords` | string[] | No | Ids de lançamentos financeiros relacionados. |

### `populatedInvoice`

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

#### `populatedInvoice.nfseErrors`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `codigo` | string | No | Prefeitura error code (Focus erros[].codigo). |
| `mensagem` | string | No | Prefeitura error message (Focus erros[].mensagem). |
| `correcao` | string | No | How to fix (Focus erros[].correcao). |

#### `populatedInvoice.defaultTypeSpecific`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `natureOfOperation` | enum: TRIBUTACAO_NO_MUNICIPIO, TRIBUTACAO_FORA_DO_MUNICIPIO, ISENCAO... | No |  |
| `specialTaxRegime` | enum: MICROEMPRESA_MUNICIPAL, ESTIMATIVA, SOCIEDADE_DE_PROFISSIONAIS... | No |  |
| `municipalTaxCode` | string | No |  |
| `aliquota` | number | No |  |
| `issAmount` | number | No |  |
| `deductionsAmount` | number | No |  |
| `pisAmount` | number | No |  |
| `cofinsAmount` | number | No |  |
| `inssAmount` | number | No |  |
| `irAmount` | number | No |  |
| `csllAmount` | number | No |  |
| `unconditionalDiscount` | number | No |  |
| `conditionalDiscount` | number | No |  |
| `otherRetentions` | number | No |  |
| `baseCalculo` | number | No |  |
| `cnaeCode` | string | No |  |
| `nbsCode` | string | No | NBS code override (9 digits). |
| `operationIndicatorCode` | string | No | Operation indicator code override (cIndOp, 6 digits). |
| `ibsCbsTaxClassificationCode` | string | No | IBS/CBS tax classification override (cClassTrib, 6 digits). |
| `serviceCountryCode` | string | No | BACEN country code for service provision abroad (codigo_pais_prestacao). |
| `tomadorAddress` | object | No |  |

#### `populatedInvoice.nationalTypeSpecific`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `competenceDate` | string | Yes | YYYY-MM-DD. |
| `dpsSeriesNumber` | integer | No |  |
| `dpsNumber` | integer | No |  |
| `dpsIssuer` | enum: PRESTADOR, TOMADOR, INTERMEDIARIO | No |  |
| `simplesNacionalOption` | enum: NAO_OPTANTE, MEI, ME_EPP | No |  |
| `simplesNacionalTaxRegime` | enum: APURACAO_FEDERAL_E_MUNICIPAL_PELO_SN, APURACAO_FEDERAL_PELO_SN_ISS_FORA, APURACAO_FEDERAL_E_MUNICIPAL_FORA_DO_SN | No |  |
| `specialTaxRegime` | enum: NENHUM, ATO_COOPERADO, ESTIMATIVA... | No |  |
| `issTaxation` | enum: OPERACAO_TRIBUTAVEL, IMUNIDADE, EXPORTACAO_DE_SERVICO... | No |  |
| `issRetentionType` | enum: NAO_RETIDO, RETIDO_PELO_TOMADOR, RETIDO_PELO_INTERMEDIARIO | No |  |
| `relativeAliquotaPercentage` | number | No |  |
| `complementaryInfo` | string | No |  |
| `tomadorStreet` | string | No |  |
| `tomadorNumber` | string | No |  |
| `tomadorComplement` | string | No |  |
| `tomadorNeighborhood` | string | No |  |
| `tomadorMunicipalityCode` | string | No |  |
| `tomadorPostalCode` | string | No |  |
| `tomadorPhone` | string | No |  |
| `cstPisCofins` | enum: 00, 01, 07... | No |  |
| `basePisCofins` | number | No |  |
| `aliquotaPis` | number | No |  |
| `aliquotaCofins` | number | No |  |
| `valorPis` | number | No |  |
| `valorCofins` | number | No |  |
| `pisCofinsRetentionType` | enum: PIS_COFINS_CSLL_NAO_RETIDOS, PIS_COFINS_RETIDOS, PIS_COFINS_NAO_RETIDOS... | No |  |
| `valorIrrfRetido` | number | No |  |
| `valorCsllRetido` | number | No |  |
| `valorCpRetido` | number | No |  |
| `indicadorTotalTributos` | enum: INFORMA_ESTIMATIVA, NAO_INFORMA_ESTIMATIVA | No |  |
| `valorTotalTributosFederais` | number | No |  |
| `valorTotalTributosEstaduais` | number | No |  |
| `valorTotalTributosMunicipais` | number | No |  |
| `percentualTotalTributosSimplesNacional` | number | No |  |

