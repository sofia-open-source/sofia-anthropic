# OfxImportJobRequestEntity

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes | Identificador da solicitação de importação OFX. |
| `bankAccountId` | string | Yes | Identificador da conta bancária. |
| `bankAccountName` | string | Yes | Nome da conta bancária. |
| `fileName` | string | Yes | Nome do arquivo OFX. |
| `signedUrl` | string | Yes | URL assinada do arquivo OFX. |
| `maxTransactionsForAiSuggestionOnImport` | integer | No | Número máximo de transações para sugestão de AI na importação. |
| `requesterUserId` | string | Yes | Identificador do usuário que solicitou a importação. |
| `totalTransactions` | integer | No | Número total de transações no arquivo OFX. |
| `periodStartDate` | any | No | Data da transação mais antiga no arquivo OFX. |
| `periodEndDate` | any | No | Data da transação mais recente no arquivo OFX. |
| `createdAt` |  | Yes | Data de criação da solicitação de importação. |
| `updatedAt` |  | Yes | Data de atualização da solicitação de importação. |
| `deletedAt` | any | Yes | Data de exclusão da solicitação de importação. |
| `searchScore` | number | No | Pontuação de busca da solicitação de importação. |

