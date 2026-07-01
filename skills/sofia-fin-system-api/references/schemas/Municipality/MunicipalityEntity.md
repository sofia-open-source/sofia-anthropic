# MunicipalityEntity

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `municipalityCode` | string | Yes | Código IBGE do município (7 dígitos). |
| `municipalityName` | string | Yes | Nome completo do município segundo o IBGE. |
| `stateAbbreviation` | string | Yes | Sigla do estado do município (2 caracteres). |
| `stateName` | string | Yes | Nome completo do estado onde se encontra o município. |
| `nfseEnabled` | boolean | Yes | Verdadeiro se já implementamos a NFSe para este município. |
| `requiresCertificateNfse` | boolean | No | Indica se o município precisa de um certificado digital. |
| `hasHomologationEnvironmentNfse` | boolean | No | Indica se existe ambiente de homologação neste município. |
| `hasCancellationNfse` | boolean | No | Indica se é possível o cancelamento de NFSe via API. |
| `providerNfse` | string | No | Nome do provedor do município. |
| `addressRequiredNfse` | boolean | No | Indica obrigatoriedade de endereço. |
| `cpfCnpjRequiredNfse` | boolean | No | Indica obrigatoriedade de CPF/CNPJ. |
| `cnaeCodeRequiredNfse` | boolean | No | Indica obrigatoriedade do código CNAE. |
| `serviceListItemRequiredNfse` | boolean | No | Indica obrigatoriedade do item da lista de serviço. |
| `municipalTaxCodeRequiredNfse` | boolean | No | Indica obrigatoriedade do código tributário municipal. |
| `statusNfse` | enum: ativo, fora_do_ar, pausado... | Yes | Status operacional da emissão de NFSe no município. |
| `reimplementationForecastDateNfse` | string | No | Data prevista para reimplementação (formato ISO 8601 YYYY-MM-DD). |
| `lastNfseIssuance` | string | No | Data e hora da última emissão de NFSe via API (formato ISO 8601). |

