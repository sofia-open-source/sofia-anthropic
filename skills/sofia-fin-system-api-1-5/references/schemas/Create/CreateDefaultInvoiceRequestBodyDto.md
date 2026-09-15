# CreateDefaultInvoiceRequestBodyDto

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
| `serviceDescription` | string | Yes | Service description / discrimination. |
| `issWithheld` | boolean | Yes | Whether ISS is withheld. |
| `serviceListItemCode` | string | No | LC116 item or national list code when omitted. |
| `serviceMunicipalityCode` | string | Yes | IBGE code where service is provided. |
| `tomador` | object | No | Service taker. |
| `defaultTypeSpecific` | object | No | Default NFSe-specific fields. |

## Nested Fields

### `tomador`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `cnpj` | string | No |  |
| `cpf` | string | No |  |
| `name` | string | No |  |
| `email` | string (email) | No |  |

### `defaultTypeSpecific`

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

#### `defaultTypeSpecific.tomadorAddress`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `street` | string | No | Logradouro. |
| `number` | string | No | Número. |
| `complement` | string | No | Complemento. |
| `neighborhood` | string | No | Bairro. |
| `municipalityCode` | string | No | IBGE municipality code. |
| `stateAbbreviation` | string | No | UF. |
| `postalCode` | string | No | CEP. |

