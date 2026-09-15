# ExecuteOfxImportJobRequestBodyDto

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `requester` | object | Yes |  |
| `ofxImportJobRequestId` | string | Yes |  |

## Nested Fields

### `requester`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes |  |
| `primaryEmail` | string (email) | Yes |  |
| `primaryPhoneNumber` | string | Yes |  |
| `firstName` | string | Yes |  |
| `lastName` | string | Yes |  |
| `organization` | object | No |  |

#### `requester.organization`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes |  |
| `name` | string | Yes |  |
| `type` | enum: LEAF, GROUP | Yes |  |
| `role` | enum: org:admin, org:member | Yes |  |
| `onFinSystem` | boolean | No |  |
| `parent` | object | No |  |
| `children` | object[] | No |  |

