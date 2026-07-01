# OnBankAccountCreatedRequestBodyDto

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `requester` | object | Yes |  |
| `bankAccount` | object | Yes |  |

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

### `bankAccount`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes | Identificador da conta bancária. |
| `ownerOrganization` | string | Yes | Identificador da organização dona da conta bancária. |
| `name` | string | Yes | Nome da conta bancária. |
| `type` | enum: MONEY, CHECKING, SAVINGS... | Yes | Tipo da conta bancária. |
| `number` | string | Yes | Número da conta ou cartão. |
| `isAutomatic` | boolean | Yes | Indica se a conta é automática ou manual. |
| `isDefault` | boolean | Yes | Indica se a conta é a padrão. |
| `initialBalanceDate` | any | No | Data do saldo inicial. |
| `initialBalanceAmount` | any | No | Valor do saldo inicial. |
| `institution` | string | No | Instituição financeira. |
| `active` | boolean | Yes | Indica se a conta está ativa. |
| `provider` | enum: PLUGGY, OFX, OTHER | No | Fornecedor da conta bancária. |
| `providerAccountId` | string | No | Identificador da conta bancária no fornecedor. |
| `providerItemId` | string | No | Identificador do item de conexão do fornecedor. |
| `createdAt` | any | Yes | Data de criação da conta bancária. |
| `updatedAt` | any | Yes | Data de atualização da conta bancária. |

