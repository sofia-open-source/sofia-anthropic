# CreateLegalEntityRequestBodyDto

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `name` | string | Yes | Razão social da empresa. |
| `tradeName` | string | Yes | Nome fantasia. |
| `stateRegistration` | string | No | Inscrição estadual. |
| `municipalRegistration` | string | No | Inscrição municipal. |
| `cnpj` | string | No | CNPJ da empresa. |
| `cpf` | string | No | CPF do prestador. |
| `taxRegime` | enum: SIMPLES_NACIONAL, SIMPLES_NACIONAL_EXCESS, NORMAL... | Yes | Regime tributário. |
| `simplesNacionalTaxRegime` | enum: APURACAO_FEDERAL_E_MUNICIPAL_PELO_SN, APURACAO_FEDERAL_PELO_SN_ISS_FORA, APURACAO_FEDERAL_E_MUNICIPAL_FORA_DO_SN | No | NFSe nacional SN tax apuration regime (regApTribSN). Optional for ME/EPP Simples Nacional. |
| `email` | string (email) | Yes | Email de contato da empresa. |
| `phone` | string | No | Telefone da empresa. |
| `street` | string | Yes | Endereço: logradouro. |
| `number` | string | Yes | Endereço: número. |
| `complement` | string | No | Endereço: complemento. |
| `neighborhood` | string | Yes | Endereço: bairro. |
| `postalCode` | string | Yes | Endereço: CEP completo. |
| `municipality` | string | Yes | Endereço: nome do município sem abreviações. |
| `municipalityCode` | string | Yes | IBGE municipality code (7 digits). |
| `stateAbbreviation` | string | Yes | Endereço: UF com 2 caracteres. |
| `isDefault` | boolean | No | Whether this legal entity should be the default for the organization. |
| `nfseSendMunicipalRegistration` | boolean | No | Whether to include municipal registration in NFSe emission payloads. |
| `certificateBase64` | string | No | Arquivo do certificado digital em formato PFX ou P12 (base64). |
| `certificatePassword` | string | No | Senha do certificado digital. |
| `responsibleName` | string | No | Nome do responsável pela empresa. |
| `responsibleCpf` | string | No | CPF do responsável pela empresa. |
| `responsibleLogin` | string | No | Login para acesso da prefeitura. |
| `responsiblePassword` | string | No | Senha para acesso da prefeitura. |
| `automaticSendNfEmail` | boolean | No | Whether to automatically send NF email. |

