# Analytics - Cash Flow Reports

Cash-flow analytics: full-period report, current-month snapshot, and projected cash flow. All endpoints are GET under /analytics/cash-flow with date and filter params. Projections extrapolate from scheduled and recurring inflows/outflows. No write operations; purely analytical read models.

## Operations

| Method | Path | Summary | Details |
|--------|------|---------|----------|
| GET | `/analytics/cash-flow/report` | Generate a cash flow report. | [View](../operations/analyticsGenerateCashFlowReport.md) |
| GET | `/analytics/cash-flow/current-month` | Get current month cash flow by direction. | [View](../operations/analyticsGetCurrentMonthCashFlow.md) |
| GET | `/analytics/cash-flow/projected` | Get projected cash flow from D-3 to D+8. | [View](../operations/analyticsGetProjectedCashFlow.md) |
