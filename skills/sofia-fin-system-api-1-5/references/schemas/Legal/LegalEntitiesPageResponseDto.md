# LegalEntitiesPageResponseDto

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `items` | object[] | Yes | Lista de entidades legais. |
| `pageInfo` | object | Yes | Informações de paginação. |

## Nested Fields

### `items`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes | Identificador único da entidade legal. |
| `ownerOrganization` | string | Yes | Identificador da organização dona. |
| `provider` | enum: FOCUS_NFE | Yes | Provedor de serviços fiscais. |
| `providerId` | string | Yes | Identificador da entidade no provedor fiscal. |
| `name` | string | Yes | Razão social da empresa. |
| `tradeName` | string | Yes | Nome fantasia. |
| `stateRegistration` | string | No | Inscrição estadual. |
| `municipalRegistration` | string | No | Inscrição municipal. |
| `cnpj` | string | No | CNPJ da empresa. |
| `cpf` | string | No | CPF do prestador. |
| `taxRegime` | enum: SIMPLES_NACIONAL, SIMPLES_NACIONAL_EXCESS, NORMAL... | Yes | Regime tributário. |
| `simplesNacionalTaxRegime` | enum: APURACAO_FEDERAL_E_MUNICIPAL_PELO_SN, APURACAO_FEDERAL_PELO_SN_ISS_FORA, APURACAO_FEDERAL_E_MUNICIPAL_FORA_DO_SN | No | NFSe nacional SN tax apuration regime (regApTribSN). Optional; when omitted at emission, ME/EPP defaults to federal and municipal via SN. |
| `email` | string | Yes | Email de contato da empresa. |
| `phone` | string | No | Telefone da empresa. |
| `street` | string | Yes | Endereço: logradouro. |
| `number` | string | Yes | Endereço: número. |
| `complement` | string | No | Endereço: complemento. |
| `neighborhood` | string | Yes | Endereço: bairro. |
| `postalCode` | string | Yes | Endereço: CEP completo. |
| `municipality` | string | Yes | Endereço: nome do município sem abreviações. |
| `municipalityCode` | string | No | IBGE municipality code (7 digits). |
| `stateAbbreviation` | string | Yes | Endereço: UF com 2 caracteres. |
| `nfseDefaultEnabled` | boolean | Yes | Whether municipal (default / prefeitura) NFSe is enabled on the Focus empresa for this entity. |
| `nfseNationalProdEnabled` | boolean | Yes | Whether NFS-e Nacional production is enabled on the Focus empresa for this entity. |
| `nfseNationHomologEnabled` | boolean | Yes | Whether NFS-e Nacional homologation is enabled on the Focus empresa for this entity. |
| `municipalityNfseUnavailable` | boolean | Yes | True when the IBGE municipality is not served by Focus for NFSe (stored at create or municipality update). |
| `nfseSendMunicipalRegistration` | boolean | Yes | Whether to include municipal registration in NFSe emission payloads. |
| `isDefault` | boolean | Yes | Whether this legal entity is the default for the organization. |
| `automaticSendNfEmail` | boolean | No | Whether to automatically send NF email. |
| `createdAt` | string | Yes | Creation date of the legal entity. |
| `updatedAt` | string | Yes | Last update date of the legal entity. |

### `pageInfo`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `pageIndex` | number | Yes |  |
| `pageSize` | number | Yes |  |
| `totalPages` | number | Yes |  |
| `totalItems` | number | Yes |  |

