# ProcessEmailForForwardingIntegrationRequestBodyDto

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `forwardedEmailId` | string | Yes | ID of the forwarded email to process. |
| `requester` | object | Yes |  |

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

