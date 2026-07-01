# POST /core/financial-record-groups

**Resource:** [Core - Financial Record Groups](../resources/Core-Financial-Record-Groups.md)
**Cria um grupo de lançamentos financeiros.**
**Operation ID:** `coreCreateFinancialRecordGroup`

Cria um grupo vinculando dois lançamentos financeiros (um de entrada e outro de saída) após validar todas as condições necessárias.

## Request Body

Data for creating the financial record group.

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [CreateFinancialRecordGroupRequestBodyDto](../schemas/Create/CreateFinancialRecordGroupRequestBodyDto.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | Grupo criado com sucesso. |
| default |  |

**Success Response Schema:**

[FinancialRecordGroupResponseDto](../schemas/Financial/FinancialRecordGroupResponseDto.md)

