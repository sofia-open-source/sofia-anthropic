# GET /analytics/financial-statements/data

**Resource:** [Analytics - Financial Statements Reports](../resources/Analytics-Financial-Statements-Reports.md)
**Calculate customizable financial statement data with hierarchy and vertical or horizontal analysis.**
**Operation ID:** `analyticsGetFinancialStatementData`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `startDate` | query | string (date) | Yes | Inclusive requested range start date in UTC (YYYY-MM-DD). |
| `endDate` | query | string (date) | Yes | Inclusive requested range end date in UTC (YYYY-MM-DD). |
| `groupBy` | query | enum: daily, weekly, monthly... | Yes | Calendar period used to group values. |
| `includeAV` | query | boolean | No | Whether to include vertical analysis percentages. |
| `includeAH` | query | boolean | No | Whether to include horizontal analysis percentages. |
| `referenceDate` | query | enum: dueDate, cashDate, competenceDate | No | Financial record date field used to filter the requested range. Defaults to cashDate. |
| `completed` | query | boolean | No | Financial record completion status filter. |
| `tags` | query | string[] | No | Comma-separated tag identifiers to filter. |
| `includeNoTags` | query | boolean | No | When true with tag identifiers, includes matching tagged records and untagged records; when true alone, includes only untagged records. |
| `queryId` | query | string | No | Saved query identifier to apply. |

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

**Success Response Schema:**

[GetFinancialStatementDataV2ResponseDto](../schemas/Get/GetFinancialStatementDataV2ResponseDto.md)

