# Core - Legal entities

Legal entities (CNPJ) and fiscal registration data for the organization. CRUD, set default entity for invoicing, and get/patch Focus NFSe RPS settings per entity. Required for NFSe issuance and provider configuration. One organization may hold multiple entities but typically invoices from the default.

## Operations

| Method | Path | Summary | Details |
|--------|------|---------|----------|
| GET | `/core/legal-entities` | Lista todas as entidades legais da organização. | [View](../operations/coreFindAllLegalEntities.md) |
| POST | `/core/legal-entities` | Cria uma nova entidade legal. | [View](../operations/coreCreateLegalEntity.md) |
| GET | `/core/legal-entities/{id}` | Busca uma entidade legal pelo identificador. | [View](../operations/coreFindLegalEntityById.md) |
| DELETE | `/core/legal-entities/{id}` | Remove uma entidade legal. | [View](../operations/coreRemoveLegalEntity.md) |
| PATCH | `/core/legal-entities/{id}` | Atualiza uma entidade legal. | [View](../operations/coreUpdateLegalEntity.md) |
| POST | `/core/legal-entities/{id}/set-as-default` | Define uma entidade legal como padrão da organização. | [View](../operations/coreSetDefaultLegalEntity.md) |
| GET | `/core/legal-entities/{id}/focus-nfse-rps-settings` | Consulta série e próximo RPS de NFSe municipal em produção na Focus NFe. | [View](../operations/coreFindLegalEntityFocusNfseRpsSettings.md) |
| PATCH | `/core/legal-entities/{id}/focus-nfse-rps-settings` | Atualiza série e/ou próximo RPS de NFSe municipal em produção na Focus NFe. | [View](../operations/coreUpdateLegalEntityFocusNfseRpsSettings.md) |
