# CepLookupEntity

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `cep` | string | Yes | Postal code (CEP), digits only. |
| `tipo` | string | No | CEP type (localidade, logradouro, etc.). |
| `uf` | string | Yes | State abbreviation (UF). |
| `nomeLocalidade` | string | Yes | Municipality or locality name. |
| `codigoIbge` | string | No | IBGE municipality code (7 digits). |
| `tipoLogradouro` | string | No | Street type (Rua, Avenida, etc.). |
| `nomeLogradouro` | string | No | Street name. |
| `nomeBairroInicial` | string | No | Starting neighborhood of the CEP range. |
| `descricao` | string | No | Human-readable address description. |

