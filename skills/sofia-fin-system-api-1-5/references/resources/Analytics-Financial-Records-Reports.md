# Analytics - Financial Records Reports

Read-only GET analytics built on financial records: aggregated totals, grouped aggregations, and monthly breakdowns. Supports saved-query filters via queryId and standard date or dimension params. Used for dashboards, KPI tiles, and drill-down charts. Deprecated system variants exist for internal cross-service use and are excluded from public skill docs.

## Operations

| Method | Path | Summary | Details |
|--------|------|---------|----------|
| GET | `/analytics/financial-records/aggregated-result/report` | Get aggregated result report for financial records | [View](../operations/analyticsGetAggregatedResultReport.md) |
| GET | `/analytics/financial-records/aggregated/report` | Generate aggregated financial records report by category, contact or tag. | [View](../operations/analyticsGenerateAggregatedFinancialRecordsReport.md) |
| GET | `/analytics/financial-records/aggregated-monthly/report` | Generate monthly financial report for the last 12 months. | [View](../operations/analyticsGenerateMonthlyFinancialReport.md) |
