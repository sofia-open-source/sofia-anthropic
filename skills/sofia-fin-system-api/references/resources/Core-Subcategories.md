# Core - Subcategories

Expense and revenue subcategories under system-managed categories. Org-owned CRUD, paginated list, find-by-id or slug, and org-scoped listing. Subcategories classify financial records in reports and budgets. Categories themselves are not mutated via this API.

## Operations

| Method | Path | Summary | Details |
|--------|------|---------|----------|
| GET | `/core/subcategories` | Busca todas as subcategorias. | [View](../operations/coreFindAllSubcategories.md) |
| POST | `/core/subcategories` | Cria uma nova subcategoria. | [View](../operations/coreCreateSubcategory.md) |
| GET | `/core/subcategories/slug/{slug}` | Busca uma subcategoria pelo slug. | [View](../operations/coreFindBySlugSubcategory.md) |
| GET | `/core/subcategories/{id}` | Busca uma subcategoria pelo identificador. | [View](../operations/coreFindByIdSubcategory.md) |
| DELETE | `/core/subcategories/{id}` | Remove uma subcategoria. | [View](../operations/coreRemoveSubcategory.md) |
| PATCH | `/core/subcategories/{id}` | Atualiza parcialmente uma subcategoria. | [View](../operations/corePartialUpdateSubcategory.md) |
