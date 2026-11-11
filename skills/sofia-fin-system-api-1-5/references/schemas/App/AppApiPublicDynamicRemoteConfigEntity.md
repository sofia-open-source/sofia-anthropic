# AppApiPublicDynamicRemoteConfigEntity

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `nfsen` | object | Yes |  |
| `aiDeny` | object[] | No |  |

## Nested Fields

### `nfsen`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `nationalForcedMunicipalityCodes` | string[] | No |  |
| `policies` | object | Yes |  |

#### `nfsen.policies`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `percentageRateMunicipalitySpecificDepreceated` | object | Yes |  |
| `totalTaxationIndicatorDepreceated` | object | Yes |  |
| `taxReformRequired` | object | Yes |  |
| `totalTributesPercentageRequired` | object | Yes |  |

### `aiDeny`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `organizationId` | string | Yes |  |
| `denyAgentNames` | any | Yes |  |

