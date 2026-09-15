# OrganizationBalanceHistoryPerAccountEntity

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountId` | string | Yes | ID da conta |
| `accountName` | string | Yes | Nome da conta |
| `accountType` | string | Yes | Tipo de conta |
| `accountImageUrl` | string (uri) | No | URL da imagem da conta |
| `connectionType` | string | No | Tipo de conexão da conta |
| `currentBalance` | string | Yes | Saldo atual da conta |
| `history` | object[] | Yes |  |

## Nested Fields

### `history`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `period` | object | Yes | Período |
| `openingBalance` | string | Yes | Saldo inicial |
| `totalIncome` | string | Yes | Total de receitas |
| `totalOutcome` | string | Yes | Total de despesas |
| `closingBalance` | string | Yes | Saldo final |

#### `history.period`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `start` | string | No | Period start date |
| `end` | string | No | Period end date |
| `name` | string | Yes | Period name |

