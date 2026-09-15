# RawAccountEntity

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `provider` | enum: PLUGGY, OTHER | Yes |  |
| `id` | string | Yes |  |
| `type` | enum: BANK, CREDIT | Yes |  |
| `subtype` | enum: CHECKING_ACCOUNT, SAVINGS_ACCOUNT, CREDIT_CARD | Yes |  |
| `number` | string | Yes |  |
| `name` | string | Yes |  |
| `balance` | string | Yes |  |
| `currencyCode` | enum: AED, AFN, ALL... | Yes |  |
| `connector` | object | Yes |  |

## Nested Fields

### `connector`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | number | Yes |  |
| `name` | string | Yes |  |
| `institutionUrl` | string | Yes |  |
| `imageUrl` | string | Yes |  |
| `primaryColor` | string | Yes |  |

