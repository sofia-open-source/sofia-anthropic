# GET /analytics/organization-balance/per-account/history

**Resource:** [Analytics - Organization Balance](../resources/Analytics-Organization-Balance.md)
**Get organization balance history per account**
**Operation ID:** `analyticsGetOrganizationBalanceHistoryPerAccount`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `periodType` | query | enum: day, month, year | Yes |  |
| `periodAmount` | query | integer | Yes |  |

## Responses

| Status | Description |
|--------|-------------|
| 200 | Organization balance history |

**Success Response Schema:**

Array of [OrganizationBalanceHistoryPerAccountEntity](../schemas/Organization/OrganizationBalanceHistoryPerAccountEntity.md)

