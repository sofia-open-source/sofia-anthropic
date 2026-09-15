# ContactResponseDto

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes | Contact identifier. |
| `ownerOrganization` | string | Yes | Identifier of the organization that owns the contact. |
| `name` | string | Yes | Contact name. |
| `types` | string[] | Yes | Contact types. |
| `documentType` | enum: CNPJ, CPF | No | Contact document type. |
| `document` | string | No | Contact document. |
| `email` | string | No | Contact email. |
| `phone` | string | No | Contact phone. |
| `pixKeys` | string[] | Yes | Contact PIX keys. |
| `birthDate` | string | No | Contact birth date. |
| `origin` | enum: INDICATION, ADS, ORGANIC_SEARCH... | No | Contact origin. |
| `address` | object | No | Contact address. |
| `isNotIdentified` | boolean | Yes | Whether the contact is the unidentified contact. |
| `searchScore` | number | No | Contact search score. |
| `createdAt` | string | Yes | Creation date of the contact. |
| `updatedAt` | string | Yes | Last update date of the contact. |
| `importedAt` | string | No | Contact import date. |
| `importedBy` | string | No | Contact import source. |
| `externalId` | string | No | External identifier of the contact. |
| `observations` | string | No | Contact observations. |

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

