# CreateLegalEntityServiceCodeAttributionRequestBodyDto

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `legalEntityId` | string | Yes | Identificador da entidade legal. |
| `serviceCodeId` | string | Yes | Identificador do código de serviço. |
| `isDefault` | boolean | No | Whether this attribution should be the default. |
| `customNfseRootJson` | object | No | Custom JSON deep-merged into the root of the Focus NFe NFSe payload. For municipal NFSe, a `servico` object is deep-merged into the generated `servico` block. |

