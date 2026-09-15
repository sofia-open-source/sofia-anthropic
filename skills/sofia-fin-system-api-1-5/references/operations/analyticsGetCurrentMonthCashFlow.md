# GET /analytics/cash-flow/current-month

**Resource:** [Analytics - Cash Flow Reports](../resources/Analytics-Cash-Flow-Reports.md)
**Get current month cash flow by direction.**
**Operation ID:** `analyticsGetCurrentMonthCashFlow`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `direction` | query | enum: IN, OUT | Yes | Record direction (IN or OUT) |

## Responses

| Status | Description |
|--------|-------------|
| 200 | Current month cash flow retrieved successfully |

**Success Response Schema:**

[CurrentMonthCashFlowEntity](../schemas/Current/CurrentMonthCashFlowEntity.md)

