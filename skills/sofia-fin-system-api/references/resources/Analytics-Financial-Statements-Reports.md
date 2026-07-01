# Analytics - Financial Statements Reports

DRE (income statement) and related financial-statement reports for a period. Endpoints return the main statement, financial measures, and result-composition breakdowns. All are GET-only and filterable by period and saved queries. Outputs feed P&L views and management reporting; no mutation endpoints.

## Operations

| Method | Path | Summary | Details |
|--------|------|---------|----------|
| GET | `/analytics/financial-statements/report` | Generate financial statement report with grouping and filter options. | [View](../operations/analyticsGenerateFinancialStatementReport.md) |
| GET | `/analytics/financial-statements/financial-measures-report` | Generate financial measures report. | [View](../operations/analyticsGenerateFinancialMeasuresReport.md) |
| GET | `/analytics/financial-statements/result-composition/report` | Generate financial result composition report. | [View](../operations/analyticsGenerateFinancialResultCompositionReport.md) |
