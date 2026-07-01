# UpdateLegalEntityRequestBodyDto

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `name` | any | No | Razão social da empresa. |
| `tradeName` | any | No | Nome fantasia. |
| `stateRegistration` | string | No | Inscrição estadual. |
| `municipalRegistration` | string | No | Inscrição municipal. |
| `taxRegime` | enum: SIMPLES_NACIONAL, SIMPLES_NACIONAL_EXCESS, NORMAL... | No | Regime tributário. |
| `simplesNacionalTaxRegime` | enum: APURACAO_FEDERAL_E_MUNICIPAL_PELO_SN, APURACAO_FEDERAL_PELO_SN_ISS_FORA, APURACAO_FEDERAL_E_MUNICIPAL_FORA_DO_SN | No | NFSe nacional SN tax apuration regime (regApTribSN). Send null to clear. |
| `email` | any | No | Email de contato da empresa. |
| `phone` | string | No | Telefone da empresa. |
| `street` | any | No | Endereço: logradouro. |
| `number` | any | No | Endereço: número. |
| `complement` | string | No | Endereço: complemento. |
| `neighborhood` | any | No | Endereço: bairro. |
| `postalCode` | any | No | Endereço: CEP completo. |
| `municipality` | any | No | Endereço: nome do município sem abreviações. |
| `municipalityCode` | any | No | IBGE municipality code (7 digits). |
| `stateAbbreviation` | any | No | Endereço: UF com 2 caracteres. |
| `certificateBase64` | any | No | Arquivo do certificado digital em formato PFX ou P12 (base64). |
| `certificatePassword` | any | No | Senha do certificado digital. |
| `responsibleName` | any | No | Nome do responsável pela empresa. |
| `responsibleCpf` | any | No | CPF do responsável pela empresa. |
| `responsibleLogin` | any | No | Login para acesso da prefeitura. |
| `responsiblePassword` | any | No | Senha para acesso da prefeitura. |
| `nfseSendMunicipalRegistration` | boolean | No | Whether to include municipal registration in NFSe emission payloads. |
| `automaticSendNfEmail` | boolean | No | Whether to automatically send NF email. |

