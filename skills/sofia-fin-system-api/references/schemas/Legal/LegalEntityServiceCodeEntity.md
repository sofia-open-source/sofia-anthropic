# LegalEntityServiceCodeEntity

**Type:** object

## Fields

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
| `createdAt` |  | Yes | Creation timestamp. |
| `updatedAt` |  | Yes | Last update timestamp. |

