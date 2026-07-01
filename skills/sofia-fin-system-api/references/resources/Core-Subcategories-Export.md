# Core - Subcategories Export

Export subcategories in csv or xlsx format. POST /core/subcategories/export for async jobs; POST …/export/sync for immediate download. Exports respect list filters and sort options. Handy for chart-of-accounts reviews and migrations.

## Operations

| Method | Path | Summary | Details |
|--------|------|---------|----------|
| POST | `/core/subcategories/export` | Solicita a exportação das subcategorias. | [View](../operations/coreExportSubcategories.md) |
| POST | `/core/subcategories/export/sync` | Solicita a exportação das subcategorias de forma síncrona. | [View](../operations/coreSyncExportSubcategories.md) |
