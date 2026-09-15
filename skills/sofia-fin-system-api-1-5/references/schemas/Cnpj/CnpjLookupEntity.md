# CnpjLookupEntity

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `razaoSocial` | string | Yes | Company registered corporate name (razão social). |
| `nomeFantasia` | string | No | Company trade name (nome fantasia). |
| `cnpj` | string | Yes | CNPJ number, digits only. |
| `situacaoCadastral` | string | No | Registration status at Receita Federal. |
| `cnaePrincipal` | string | No | Primary CNAE code. |
| `optanteSimplesNacional` | boolean | No | Indicates whether the company is enrolled in Simples Nacional. |
| `optanteMei` | boolean | No | Indicates whether the company is enrolled as MEI. |
| `endereco` | object | Yes | Registered address information. |

## Nested Fields

### `endereco`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `codigoMunicipio` | string | No | SIAFI/IBGE municipality code returned by Focus NFe. |
| `codigoSiafi` | string | No | SIAFI municipality code. |
| `codigoIbge` | string | No | IBGE municipality code (7 digits). |
| `nomeMunicipio` | string | No | Municipality name. |
| `logradouro` | string | No | Street (logradouro). |
| `complemento` | string | No | Address complement, if any. |
| `numero` | string | No | Street number, if any. |
| `bairro` | string | No | Neighborhood. |
| `cep` | string | No | Postal code (CEP), digits only. |
| `uf` | string | No | State abbreviation (UF). |

