# BankAccountResponseDto

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes | Identificador da conta bancária. |
| `ownerOrganization` | string | Yes | Identificador da organização dona da conta bancária. |
| `name` | string | Yes | Nome da conta bancária. |
| `type` | enum: MONEY, CHECKING, SAVINGS... | Yes | Tipo da conta bancária. |
| `number` | string | Yes | Número da conta ou cartão. |
| `considerInCashFlow` | boolean | Yes | Indica se a conta deve ser considerada nos cálculos de fluxo de caixa. |
| `isAutomatic` | boolean | Yes | Indica se a conta é automática ou manual. |
| `isDefault` | boolean | Yes | Indica se a conta é a padrão. |
| `initialBalanceDate` | string | No | Data do saldo inicial da conta bancária. |
| `initialBalanceAmount` | string | No |  |
| `institution` | string | No | Instituição financeira. |
| `institutionName` | string | No | Nome da instituição financeira. |
| `active` | boolean | Yes | Indica se a conta está ativa. |
| `provider` | enum: PLUGGY, OFX, OTHER | No | Fornecedor da conta bancária. |
| `providerAccountId` | string | No | Identificador da conta bancária no fornecedor. |
| `providerItemId` | string | No | Identificador do item de conexão do fornecedor. |
| `searchScore` | number | No | Pontuação de busca. |
| `createdAt` | string | Yes | Creation date of the bank account. |
| `updatedAt` | string | Yes | Last update date of the bank account. |
| `populatedInstitution` | object | No | Instituição financeira populada. |
| `populatedAutomaticStatus` | object | No | Status se conta bancária automática. |
| `importedAt` | string | No | Bank account import date. |
| `importedBy` | string | No | Origem da importação da conta bancária. |
| `externalId` | string | No | Identificador externo da conta bancária. |

## Nested Fields

### `populatedInstitution`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `sofiaId` | string | Yes | Sofia identifier for the bank institution |
| `pluggyIds` | string[] | Yes | Pluggy identifiers for the bank institution |
| `name` | string | Yes | Name of the bank institution |
| `imageUrl` | string | Yes | URL of the bank institution image |

### `populatedAutomaticStatus`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `isSyncing` | boolean | Yes | Indica se a conta bancária está sincronizando. |
| `error` | object | No | Erro da sincronização da conta bancária. |
| `lastSyncAt` | any | No | Data da última sincronização da conta bancária. |
| `nextSyncAt` | any | No | Data da próxima sincronização da conta bancária. |

#### `populatedAutomaticStatus.error`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `code` | string | No | Código de erro da sincronização da conta bancária. |
| `message` | string | No | Mensagem de erro da sincronização da conta bancária. |

