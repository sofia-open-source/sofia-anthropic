# ReplaceFinancialStatementStructureRequestBodyDto

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `expectedRevision` | string | Yes | Structure revision from the last GET. Must match the current structure or the replace is rejected with 409. |
| `lines` | object[] | Yes | Full ordered list of financial statement lines. |
| `channel` | enum: WEB_APP, WHATSAPP, SYSTEM... | Yes | Canal de origem da operação |

## Nested Fields

### `lines`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | No | Line identifier. Required to update an existing RESULT line. |
| `type` | enum: IN, OUT, RESULT | Yes | Financial statement line type. |
| `categoryId` | string | No | Identifier of the referenced category. Required for IN/OUT, must be omitted/null for RESULT. |
| `label` | string | No | Display label. Required for RESULT, ignored for IN/OUT. |

