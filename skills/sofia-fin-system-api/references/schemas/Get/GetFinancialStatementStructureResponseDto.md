# GetFinancialStatementStructureResponseDto

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `revision` | string | Yes | Deterministic content revision of the ordered structure. Required as expectedRevision on replace. |
| `lines` | object[] | Yes | Financial statement lines, ordered by position. |

## Nested Fields

### `lines`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes | Financial statement line identifier. |
| `ownerOrganization` | string | Yes | Identifier of the organization that owns the financial statement line. |
| `type` | enum: IN, OUT, RESULT | Yes | Financial statement line type. |
| `position` | number | Yes | Dense 0-based position, used for ordering the financial statement structure. |
| `categoryId` | string | Yes | Identifier of the referenced category. Required for IN/OUT, null for RESULT. |
| `label` | string | Yes | Display label. Required for RESULT, null for IN/OUT (label comes live from the category). |
| `createdAt` | string | Yes | Creation date of the financial statement line. |
| `updatedAt` | string | Yes | Last update date of the financial statement line. |
| `category` | object | Yes |  |

#### `lines.category`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes | Category identifier. |
| `name` | string | Yes | Category name. |
| `slug` | string | Yes | Category slug. |
| `direction` | enum: IN, OUT | Yes | Category direction (IN or OUT). |

