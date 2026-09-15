# Analytics - Financial Statements Reports

Customizable Demonstrativo (DRE V2) analytics. The canonical endpoint is GET /analytics/financial-statements/data, which returns the organization's configured structure lines with hierarchy and optional AV/AH. Filterable by period, grouping, tags, and saved queries. Internal transfers are always excluded. No mutation endpoints.

## Operations

| Method | Path | Summary | Details |
|--------|------|---------|----------|
| GET | `/analytics/financial-statements/data` | Calculate customizable financial statement data with hierarchy and vertical or horizontal analysis. | [View](../operations/analyticsGetFinancialStatementData.md) |
| GET | `/analytics/financial-statements/financial-measures-report` | Generate financial measures report. | [View](../operations/analyticsGenerateFinancialMeasuresReport.md) |
| GET | `/analytics/financial-statements/result-composition/report` | Generate financial result composition report. | [View](../operations/analyticsGenerateFinancialResultCompositionReport.md) |
