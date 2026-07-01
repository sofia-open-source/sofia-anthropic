# Core - Contacts Export

Export contacts in csv or xlsx format. POST /core/contacts/export schedules async export; POST …/export/sync returns the file immediately. List filters (types, sort, search, etc.) apply to exports. Use for CRM-style extracts and spreadsheet workflows.

## Operations

| Method | Path | Summary | Details |
|--------|------|---------|----------|
| POST | `/core/contacts/export` | Solicita a exportação dos contatos. | [View](../operations/coreExportContacts.md) |
| POST | `/core/contacts/export/sync` | Solicita a exportação dos contatos de forma síncrona. | [View](../operations/coreSyncExportContacts.md) |
