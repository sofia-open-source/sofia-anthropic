# Core - Tags

Free-form classification tags attached to financial records. CRUD, paginated list, find-by-id, and org-scoped tag list. Tags enable flexible filtering and reporting dimensions beyond categories. Scoped to the leaf organization.

## Operations

| Method | Path | Summary | Details |
|--------|------|---------|----------|
| GET | `/core/tags` | Busca todas as tags. | [View](../operations/coreFindAllTags.md) |
| POST | `/core/tags` | Cria uma nova tag. | [View](../operations/coreCreateTag.md) |
| GET | `/core/tags/{id}` | Busca uma tag pelo identificador. | [View](../operations/coreFindByIdTag.md) |
| DELETE | `/core/tags/{id}` | Remove uma tag. | [View](../operations/coreRemoveTag.md) |
| PATCH | `/core/tags/{id}` | Atualiza parcialmente uma tag. | [View](../operations/corePartialUpdateTag.md) |
