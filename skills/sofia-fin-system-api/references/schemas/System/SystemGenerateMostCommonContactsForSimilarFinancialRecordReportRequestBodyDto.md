# SystemGenerateMostCommonContactsForSimilarFinancialRecordReportRequestBodyDto

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `amount` | string | Yes | Valor do lançamento financeiro |
| `direction` | enum: IN, OUT | Yes | Direção do lançamento financeiro |
| `description` | string | Yes | Descrição do lançamento financeiro |
| `dueDate` | string | Yes | Data de vencimento |
| `concluded` | boolean | Yes |  |
| `cashDate` | string | No | Data de pagamento |
| `discount` | string | No | Valor do desconto |
| `finesAndInterests` | string | No | Valor de multas e juros |
| `boletoCode` | string | No | Código do boleto |
| `pixCode` | string | No | Código PIX |
| `pixKey` | string | No | Chave PIX |
| `contactHint` | string | No | Breve descrição do contato relacionado ao lançamento financeiro (sem ser a empresa em questão), como nome, email, telefone, etc. |
| `subcategoryHint` | string | No | Breve descrição da subcategoria relacionada ao lançamento financeiro como nome, descrição, etc. |
| `channel` | enum: WEB_APP, WHATSAPP, SYSTEM... | Yes | Canal de origem da operação |

