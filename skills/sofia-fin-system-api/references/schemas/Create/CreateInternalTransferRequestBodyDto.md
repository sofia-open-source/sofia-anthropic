# CreateInternalTransferRequestBodyDto

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `channel` | enum: WEB_APP, WHATSAPP, SYSTEM... | Yes | Canal de origem da operação |
| `amount` | string | Yes | Valor da transferência em centavos. |
| `dueDate` | string | No | Data de vencimento. |
| `competenceDate` | string | No | Data de competência. |
| `cashDate` | string | No | Data de efetivação da transferência. |
| `completed` | boolean | No | Indica se a transferência foi concluída. |
| `description` | string | Yes | Descrição da transferência. |
| `tags` | string[] | No | Tags relacionadas. |
| `files` | string[] | No | Arquivos anexados. |
| `observations` | string | No | Observações. |
| `originBankAccountId` | string | Yes | Conta de origem (saída). |
| `destinationBankAccountId` | string | Yes | Conta de destino (entrada). |
| `originSubcategoryId` | string | Yes | Subcategoria de origem (saída). |
| `destinationSubcategoryId` | string | Yes | Subcategoria de destino (entrada). |

