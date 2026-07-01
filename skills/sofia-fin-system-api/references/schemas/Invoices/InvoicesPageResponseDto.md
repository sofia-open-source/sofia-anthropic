# InvoicesPageResponseDto

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
| `issueDate` | string | Yes | Issue datetime. |
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
| `createdAt` | string | Yes | Creation timestamp. |
| `updatedAt` | string | Yes | Last update timestamp. |

#### `items.nfseErrors`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `codigo` | string | No | Prefeitura error code (Focus erros[].codigo). |
| `mensagem` | string | No | Prefeitura error message (Focus erros[].mensagem). |
| `correcao` | string | No | How to fix (Focus erros[].correcao). |

#### `items.defaultTypeSpecific`

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

#### `items.nationalTypeSpecific`

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

### `pageInfo`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `pageIndex` | number | Yes |  |
| `pageSize` | number | Yes |  |
| `totalPages` | number | Yes |  |
| `totalItems` | number | Yes |  |

