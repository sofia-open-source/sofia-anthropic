# Analytics - Organization Balance

Balance analytics per bank account and rolled up to organization total. GET endpoints return historical balance series, current per-account balances, and organization-wide total. Used for treasury views and balance-over-time charts. Derived from reconciled movements and account metadata; read-only.

## Operations

| Method | Path | Summary | Details |
|--------|------|---------|----------|
| GET | `/analytics/organization-balance/per-account/history` | Get organization balance history per account | [View](../operations/analyticsGetOrganizationBalanceHistoryPerAccount.md) |
| GET | `/analytics/organization-balance/per-account` | Get organization balance per account | [View](../operations/analyticsGetOrganizationBalancePerAccount.md) |
| GET | `/analytics/organization-balance/total` | Get organization total balance | [View](../operations/analyticsGetOrganizationTotalBalance.md) |
