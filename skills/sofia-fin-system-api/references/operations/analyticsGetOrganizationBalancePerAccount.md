# GET /analytics/organization-balance/per-account

**Resource:** [Analytics - Organization Balance](../resources/Analytics-Organization-Balance.md)
**Get organization balance per account**
**Operation ID:** `analyticsGetOrganizationBalancePerAccount`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `includeNotConsideredInCashFlow` | query | boolean | No | Include accounts with `considerInCashFlow=false` (e.g. credit cards, by default) in the response. Defaults to false: those accounts are hidden from balance summaries. |

## Responses

| Status | Description |
|--------|-------------|
| 200 | Organization balance per account |

**Success Response Schema:**

Array of [OrganizationBalancePerAccountEntity](../schemas/Organization/OrganizationBalancePerAccountEntity.md)

