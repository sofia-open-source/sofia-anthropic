# Core - Tags Export

Export tags in csv or xlsx format. POST /core/tags/export schedules async export; POST …/export/sync returns the file synchronously. Same scope as the organization tag list. Use for backup or bulk review of labeling conventions.

## Operations

| Method | Path | Summary | Details |
|--------|------|---------|----------|
| POST | `/core/tags/export` | Solicita a exportação das tags. | [View](../operations/coreExportTags.md) |
| POST | `/core/tags/export/sync` | Solicita a exportação das tags de forma síncrona. | [View](../operations/coreSyncExportTags.md) |
