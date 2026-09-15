# CreateNationalInvoiceRequestBodyDto

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `channel` | enum: WEB_APP, WHATSAPP, SYSTEM... | No | Operation channel. |
| `contactId` | string | No | Contact id used to prefill tomador fields; stored on the invoice for search. |
| `legalEntityId` | string | Yes | Legal entity id. |
| `serviceCodeId` | string | Yes | Legal entity service code id. |
| `financialRecordIds` | string[] | No | Financial record ids to link. |
| `issueDate` |  | Yes | Issue datetime. |
| `serviceAmount` | number | Yes | Service amount. |
| `serviceDescription` | string | Yes | Service description. |
| `issWithheld` | boolean | Yes | Whether ISS is withheld (legacy; prefer issRetentionType). |
| `serviceListItemCode` | string | No | National ISS taxation code when omitted. |
| `serviceMunicipalityCode` | string | Yes | IBGE code where service is provided. |
| `tomador` | object | No | Service taker. |
| `nationalTypeSpecific` | object | Yes | National NFSe-specific fields. |

## Nested Fields

### `tomador`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `cnpj` | string | No |  |
| `cpf` | string | No |  |
| `name` | string | No |  |
| `email` | string (email) | No |  |

### `nationalTypeSpecific`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `competenceDate` | string | Yes | Competence date YYYY-MM-DD. |
| `dpsSeriesNumber` | integer | No |  |
| `dpsNumber` | integer | No |  |
| `dpsIssuer` | enum: PRESTADOR, TOMADOR, INTERMEDIARIO | No |  |
| `simplesNacionalOption` | enum: NAO_OPTANTE, MEI, ME_EPP | No |  |
| `simplesNacionalTaxRegime` | enum: APURACAO_FEDERAL_E_MUNICIPAL_PELO_SN, APURACAO_FEDERAL_PELO_SN_ISS_FORA, APURACAO_FEDERAL_E_MUNICIPAL_FORA_DO_SN | No |  |
| `specialTaxRegime` | enum: NENHUM, ATO_COOPERADO, ESTIMATIVA... | Yes |  |
| `issTaxation` | enum: OPERACAO_TRIBUTAVEL, IMUNIDADE, EXPORTACAO_DE_SERVICO... | Yes |  |
| `issRetentionType` | enum: NAO_RETIDO, RETIDO_PELO_TOMADOR, RETIDO_PELO_INTERMEDIARIO | Yes |  |
| `relativeAliquotaPercentage` | number | No |  |
| `complementaryInfo` | string | No |  |
| `tomadorStreet` | string | No |  |
| `tomadorNumber` | string | No |  |
| `tomadorComplement` | string | No |  |
| `tomadorNeighborhood` | string | No |  |
| `tomadorMunicipalityCode` | string | No |  |
| `tomadorPostalCode` | string | No |  |
| `tomadorPhone` | string | No |  |
| `cstPisCofins` | enum: 00, 01, 07... | No | PIS/COFINS CST (SPED). |
| `basePisCofins` | number | No | PIS/COFINS calculation base (BRL). |
| `aliquotaPis` | number | No | PIS rate (%) for own calculation. |
| `aliquotaCofins` | number | No | COFINS rate (%) for own calculation. |
| `valorPis` | number | No | PIS own-calculation amount (BRL). |
| `valorCofins` | number | No | COFINS own-calculation amount (BRL). |
| `pisCofinsRetentionType` | enum: PIS_COFINS_CSLL_NAO_RETIDOS, PIS_COFINS_RETIDOS, PIS_COFINS_NAO_RETIDOS... | No | PIS/COFINS withholding type (SPED tpRetPisCofins). |
| `valorIrrfRetido` | number | No | Withheld IRRF amount (BRL). |
| `valorCsllRetido` | number | No | Withheld CSLL envelope amount (BRL; post-reform SPED semantics). |
| `valorCpRetido` | number | No | Withheld CP/related federal amount (BRL). |
| `indicadorTotalTributos` | enum: INFORMA_ESTIMATIVA, NAO_INFORMA_ESTIMATIVA | No | Lei 12.741/2012: whether approximate total taxes are declared in this DPS. |
| `valorTotalTributosFederais` | number | No | Approximate total federal taxes (BRL) for transparency. |
| `valorTotalTributosEstaduais` | number | No | Approximate total state taxes (BRL) for transparency. |
| `valorTotalTributosMunicipais` | number | No | Approximate total municipal taxes (BRL) for transparency. |
| `percentualTotalTributosSimplesNacional` | number | No | Approximate Simples Nacional total tax rate (%). |

