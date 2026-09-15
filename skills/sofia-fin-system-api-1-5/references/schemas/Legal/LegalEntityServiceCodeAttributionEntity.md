# LegalEntityServiceCodeAttributionEntity

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes | Identificador único da atribuição. |
| `ownerOrganization` | string | Yes | Identificador da organização dona. |
| `legalEntityId` | string | Yes | Identificador da entidade legal. |
| `serviceCodeId` | string | Yes | Identificador do código de serviço. |
| `isDefault` | boolean | Yes | Whether this attribution is the default for the legal entity. |
| `createdAt` |  | Yes | Data de criação. |
| `updatedAt` |  | Yes | Data de atualização. |
| `populatedServiceCode` | object | No | Service code loaded when the request `populate` query includes `serviceCode`. |

## Nested Fields

### `populatedServiceCode`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes | Unique identifier of the service code. |
| `code` | string | Yes | Code of the service. |
| `type` | enum: MUNICIPAL_SPECIFIC, MUNICIPAL_COMPLEMENTAL_LAW_116_2003, NATIONAL | Yes | Service code type. |
| `nationalServiceCode` | string | No | National service code. |
| `municipalSpecificServiceCode` | string | No | Municipality-specific service code. |
| `municipalSpecificServiceTaxRate` | number | No | Municipality-specific tax rate. |
| `municipalCode` | string | No | IBGE municipality code (required when type is MUNICIPAL_SPECIFIC). |
| `municipalComplementalLaw116_2003ServiceCode` | string | No | Service code under Complementary Law 116/2003. |
| `nbsCode` | string | No | NBS code (9 digits) for municipal NFSe reform (Anexo VIII). |
| `operationIndicatorCode` | string | No | Operation indicator code (cIndOp, 6 digits) for municipal NFSe reform. |
| `ibsCbsTaxClassificationCode` | string | No | IBS/CBS tax classification code (cClassTrib, 6 digits) for municipal NFSe reform. |
| `description` | string | Yes | Service description. |
| `createdAt` | any | Yes | Creation timestamp. |
| `updatedAt` | any | Yes | Last update timestamp. |

