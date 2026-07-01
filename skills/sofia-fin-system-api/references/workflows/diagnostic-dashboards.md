# Workflow: financial diagnostic dashboard

Raises reports from "show numbers" to "diagnose": indicators, industry benchmarks,
traffic-light status (green/yellow/red), health score, and insights. Use original text based on
standard financial analysis and cash-flow practices; do not copy third-party content.

## Data
Use **actuals** (`completed=true`, grouped by `cashDate`), separate from projections. Pull data from
`coreFindAllFinancialRecords` (period filters) or from the analytics endpoints
(`analyticsGenerateCashFlowReport`, `analyticsGetOrganizationTotalBalance`,
`analyticsGenerateAggregatedFinancialRecordsReport`, `analyticsGenerateFinancialStatementReport`).
Map indicators to the real top-level categories (operating revenue; personnel expenses; direct costs
and expenses; income taxes; investments; financial expenses/revenue, etc.).

## Indicators (minimum 8)
Operating cash margin; burn rate (outflows/inflows, lower is better); personnel commitment
(personnel/revenue); fixed-cost coverage; rent/revenue (lower is better); effective tax burden (lower is better);
cash growth in the period; break-even point/revenue (lower is better).

## Traffic-light status
Green = within/above the ideal range; yellow = up to 20% below the lower bound; red = more
than 20% below. For indicators where **lower is better**, invert the logic.

## Industry benchmarks (DEFAULTS - calibrate with Sofia data)
| Indicator (ideal = green) | Services | Healthcare | Retail | Food service | SaaS |
|---|---|---|---|---|---|
| Operating cash margin | >20% | >20% | >8% | >10% | >25% |
| Burn rate (lower is better) | <70% | <72% | <88% | <85% | <75% |
| Personnel/revenue | 30-50% | 25-40% | 15-30% | 25-35% | 30-55% |
| Fixed-cost coverage | >2.0x | >2.0x | >1.5x | >1.5x | >2.0x |
| Rent/revenue (lower is better) | <10% | <12% | <8% | <10% | <5% |
| Tax burden (lower is better) | <8% | <8% | <10% | <8% | <8% |
| Cash growth | >3%/month | >3%/month | >2%/month | >3%/month | >5%/month |
| Break-even point/revenue (lower is better) | <60% | <65% | <80% | <75% | <60% |

Ask for the industry; if it is not provided, use "Services". Calibrate with Sofia's real dataset as a product advantage.

## Dashboard structure
Sections: summary (inflows/outflows/balance + score) | cash flow (monthly) | indicators | traffic-light status |
insights (2-4 actionable sentences). Score = weighted average (green=2, yellow=1, red=0) -> 0-100.

## Honest limitations to disclose
- **Fixed vs variable** is not native: "fixed-cost coverage" and "break-even point" depend on
  subcategory classification; until then, approximate and disclose it, or ask which subcategories are fixed.
- Benchmarks are defaults to calibrate.
- This is a point-in-time snapshot (read-only); recurring diagnostics require scheduled automation.
