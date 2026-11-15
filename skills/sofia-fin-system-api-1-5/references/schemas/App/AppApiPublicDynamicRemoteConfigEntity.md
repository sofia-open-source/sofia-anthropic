# AppApiPublicDynamicRemoteConfigEntity

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `nfsen` | object | Yes |  |
| `aiDeny` | object[] | No |  |
| `txAiSuggestion` | object | No |  |

## Nested Fields

### `nfsen`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `nationalForcedMunicipalityCodes` | string[] | No |  |
| `policies` | object | No |  |

#### `nfsen.policies`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `percentageRateMunicipalitySpecificDepreceated` | object | No |  |
| `totalTaxationIndicatorDepreceated` | object | No |  |
| `taxReformRequired` | object | No |  |
| `totalTributesPercentageRequired` | object | No |  |

### `aiDeny`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `organizationId` | string | Yes |  |
| `denyAgentNames` | any | Yes |  |

### `txAiSuggestion`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `ttlInMinutesToBeConsideredOnQueueOrProcessing` | number | No |  |
| `minTimeInMinutesBetweenSuggestionRequests` | number | No |  |

