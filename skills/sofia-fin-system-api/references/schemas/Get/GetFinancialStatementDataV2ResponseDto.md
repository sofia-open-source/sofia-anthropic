# GetFinancialStatementDataV2ResponseDto

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `generatedAt` | string | Yes | Financial statement generation timestamp. |
| `filters` | object | Yes | Filters applied to the financial statement. |
| `periods` | object[] | Yes | Shared visible periods in chronological order. |
| `lines` | object[] | Yes | Financial statement lines in configured display order. |

## Nested Fields

### `filters`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `startDate` | string (date) | Yes | Inclusive requested range start date in UTC (YYYY-MM-DD). |
| `endDate` | string (date) | Yes | Inclusive requested range end date in UTC (YYYY-MM-DD). |
| `groupBy` | enum: daily, weekly, monthly... | Yes | Calendar period used to group values. |
| `includeAV` | boolean | No | Whether to include vertical analysis percentages. |
| `includeAH` | boolean | No | Whether to include horizontal analysis percentages. |
| `referenceDate` | enum: dueDate, cashDate, competenceDate | No | Financial record date field used to filter the requested range. Defaults to cashDate. |
| `completed` | boolean | No | Financial record completion status filter. |
| `tags` | string[] | No | Comma-separated tag identifiers to filter. |
| `includeNoTags` | boolean | No | When true with tag identifiers, includes matching tagged records and untagged records; when true alone, includes only untagged records. |
| `queryId` | string | No | Saved query identifier to apply. |

### `periods`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `canonicalStartDate` | string (date) | Yes | Inclusive canonical calendar-period start date (YYYY-MM-DD). |
| `canonicalEndDate` | string (date) | Yes | Inclusive canonical calendar-period end date (YYYY-MM-DD). |
| `startDate` | string (date) | Yes | Inclusive clipped period start date (YYYY-MM-DD). |
| `endDate` | string (date) | Yes | Inclusive clipped period end date (YYYY-MM-DD). |
| `id` | string | Yes | Stable period identifier. |

### `lines`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `cells` | object[] | Yes | Values ordered to match the top-level periods array. |
| `total` | any | No | Signed total monetary value in cents, serialized as a decimal string in JSON. |
| `totalAv` | number | No | Vertical analysis percentage for the total, null when its denominator is zero. |
| `id` | string | Yes | Financial statement line identifier. |
| `type` | enum: IN, OUT, RESULT | Yes | Financial statement line type. |
| `label` | string | Yes | Financial statement line display label. |
| `groupId` | string | Yes | Referenced group identifier, or null for result lines. |
| `breakdown` | any[] | Yes | Expandable hierarchy: subgroups (by position), then direct categories (by index), matching the Categories page. |

#### `lines.cells`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `value` | any | No | Signed monetary value in cents, serialized as a decimal string in JSON. |
| `av` | number | No | Vertical analysis percentage, null when its denominator is zero. |
| `ah` | number | No | Horizontal analysis percentage, null when no prior value exists or its denominator is zero. |

