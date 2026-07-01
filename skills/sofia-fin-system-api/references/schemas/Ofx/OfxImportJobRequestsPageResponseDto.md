# OfxImportJobRequestsPageResponseDto

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `items` | object[] | Yes |  |
| `pageInfo` | object | Yes |  |

## Nested Fields

### `items`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes | Identificador da solicitação de importação OFX. |
| `bankAccountId` | string | Yes | Identificador da conta bancária. |
| `bankAccountName` | string | Yes | Nome da conta bancária. |
| `fileName` | string | Yes | Nome do arquivo OFX. |
| `requesterUserId` | string | Yes | Identificador do usuário que solicitou a importação. |
| `totalTransactions` | integer | No | Número total de transações no arquivo OFX. |
| `periodStartDate` | string | No | Oldest transaction date in the OFX file. |
| `periodEndDate` | string | No | Newest transaction date in the OFX file. |
| `createdAt` | string | Yes | Creation date of the OFX import request. |
| `updatedAt` | string | Yes | Last update date of the OFX import request. |
| `signedUrl` | string | Yes | URL assinada do arquivo OFX. |
| `searchScore` | number | No | Pontuação de busca da solicitação de importação. |
| `executions` | object[] | Yes | List of executions for this import request. |
| `nSuccessImportedTransactions` | integer | No | Maximum number of successfully imported transactions in a single execution. |
| `user` | object | Yes | User who requested the import. |
| `status` | enum: PENDING, PROCESSING, FINISHED | Yes | OFX import job request status. |
| `populatedBankAccount` | object | Yes | Populated bank account. |

#### `items.executions`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes | Identificador da execução da importação OFX. |
| `status` | enum: PROCESSING, FINISHED | Yes | Status da execução da importação OFX. |
| `nTotalItems` | integer | No | Número total de itens a serem processados. |
| `nSuccessItems` | integer | No | Número de itens processados com sucesso. |
| `nFailedItems` | integer | No | Número de itens que falharam ao processar. |
| `startedAt` | string | No | Execution start date. |
| `finishedAt` | string | No | Execution end date. |
| `createdAt` | string | Yes | Creation date of the OFX import execution. |
| `updatedAt` | string | Yes | Last update date of the OFX import execution. |

#### `items.user`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes |  |
| `primaryEmail` | string (email) | Yes |  |
| `primaryPhoneNumber` | string | Yes |  |
| `firstName` | string | Yes |  |
| `lastName` | string | Yes |  |
| `organization` | object | No |  |

#### `items.populatedBankAccount`

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

### `pageInfo`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `pageIndex` | number | Yes |  |
| `pageSize` | number | Yes |  |
| `totalPages` | number | Yes |  |
| `totalItems` | number | Yes |  |

