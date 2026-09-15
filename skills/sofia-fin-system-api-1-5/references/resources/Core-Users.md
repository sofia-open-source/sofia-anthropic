# Core - Users

Provide one endpoint to list all organizations that the authencticated user has access.

## Operations

| Method | Path | Summary | Details |
|--------|------|---------|----------|
| GET | `/core/users/me/organizations` | Busca todas as organizações de usuário. | [View](../operations/coreListMyOrganizations.md) |
| GET | `/core/users/me/last-changelog` | Obtêm o último changelog. | [View](../operations/coreGetLastChangelog.md) |
| POST | `/core/users/me/changelog/{version}/mark-as-viewed` | Marca o changelog especificado como já visto pelo usuário. | [View](../operations/coreMarkChangelogAsViewed.md) |
