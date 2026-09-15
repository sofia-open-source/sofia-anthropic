# CreateCategoryRequestBodyDto

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `direction` | enum: IN, OUT | Yes | Category direction (IN or OUT). |
| `index` | number | Yes | Category index. |
| `name` | string | Yes | Category name. |
| `slug` | string | Yes | Category slug. |
| `channel` | enum: WEB_APP, WHATSAPP, SYSTEM... | Yes | Canal de origem da operação |

