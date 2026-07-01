# ProspectInstallmentFinancialRecordRequestBodyDto

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `frequency` | enum: MONTHLY, WEEKLY, YEARLY | Yes | Record frequency. |
| `firstInstallmentDate` | string | No | First installment due date. |
| `amount` | string | Yes | Record amount. |
| `numberOfInstallments` | number | Yes | Number of installments. |

