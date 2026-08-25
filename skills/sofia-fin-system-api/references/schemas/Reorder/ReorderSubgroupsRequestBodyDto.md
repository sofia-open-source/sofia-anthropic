# ReorderSubgroupsRequestBodyDto

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `group` | string | Yes | Identifier of the parent group whose subgroups are being reordered. |
| `orderedIds` | string[] | Yes | Subgroup identifiers in their new order (0-based position). |
| `channel` | enum: WEB_APP, WHATSAPP, SYSTEM... | Yes | Canal de origem da operação |

