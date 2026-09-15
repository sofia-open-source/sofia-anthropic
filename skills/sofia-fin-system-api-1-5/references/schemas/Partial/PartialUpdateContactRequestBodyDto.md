# PartialUpdateContactRequestBodyDto

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `name` | string | No | Contact name. |
| `types` | string[] | No | Contact types. |
| `documentType` | enum: CNPJ, CPF | No | Contact document type. |
| `document` | string | No | Contact document. |
| `email` | string | No | Contact email. |
| `phone` | string | No | Contact phone. |
| `pixKeys` | string[] | No | Contact PIX keys. |
| `birthDate` | string | No | Contact birth date. |
| `origin` | enum: INDICATION, ADS, ORGANIC_SEARCH... | No | Contact origin. |
| `address` | object | No | Contact address. |
| `searchScore` | number | No | Contact search score. |
| `importedAt` | any | No | Contact import date. |
| `importedBy` | string | No | Contact import source. |
| `externalId` | string | No | External identifier of the contact. |
| `observations` | string | No | Contact observations. |
| `channel` | enum: WEB_APP, WHATSAPP, SYSTEM... | Yes | Canal de origem da operação |

## Nested Fields

### `address`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `cep` | string | No | Contact address ZIP code (CEP). |
| `street` | string | No | Contact address street. |
| `number` | string | No | Contact address number. |
| `complement` | string | No | Contact address complement. |
| `neighborhood` | string | No | Contact address neighborhood. |
| `city` | string | No | Contact address city. |
| `state` | string | No | Contact address state. |
| `country` | string | No | Contact address country. |

