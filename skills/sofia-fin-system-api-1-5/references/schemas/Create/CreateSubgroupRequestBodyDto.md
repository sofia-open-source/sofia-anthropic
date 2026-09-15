# CreateSubgroupRequestBodyDto

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `group` | string | Yes | Identifier of the parent group (Category) this subgroup belongs to. |
| `name` | string | Yes | Subgroup name. |
| `slug` | string | Yes | Subgroup slug. |
| `channel` | enum: WEB_APP, WHATSAPP, SYSTEM... | Yes | Canal de origem da operação |

