# Backend business rules not documented in OpenAPI

OpenAPI describes shapes and types, not business rules. The backend validates invariants that only
surface as runtime errors (HTTP 400/422). Validating **before** calling avoids raw errors and
half-finished operations. Endpoints are cited by the official skill `operationId`.

> Collected by reading `app-api`. It may diverge from the deployed API over time; revalidate when
> the backend changes. Monetary values are **integer cents as strings** (BRL 700.00 -> `"70000"`).

## Reconciliation (`coreReconcileBankTransaction`)

Body: `{ financialRecordIds: [...] }`: one transaction can reconcile with **N** financial records. Four rules:

1. The transaction **must not** already be reconciled.
2. **None** of the financial records can already be reconciled with another transaction.
3. **Amount:** sum `finalAmount` **with direction sign** (IN = +, OUT = -); the **absolute value**
   must be **exactly equal** to the transaction `amountInBrl`. A 1-cent difference is an error.
4. **Direction:** if the signed sum is not 0, its direction (>0 = IN) must match the transaction
   (`type == CREDIT` means IN, otherwise OUT).
   Use the transaction `amountInBrl` (cents) and `type`; **do not** use `amount` (raw provider value).
   Undo with `coreUnreconcileBankTransaction` (error if it is not reconciled).

## Financial records (`coreCreateFinancialRecord`, `corePartialUpdateFinancialRecord`)

- **Direction x category:** the financial record direction must match the category direction of the
  selected subcategory. You cannot use an OUT subcategory in an IN financial record.
- **Marking as paid/received (`completed=true`) requires** `account` **and** `cashDate`.
- **`cashDate` cannot be in the future.**
- **A reconciled financial record is locked:** you cannot change `completed`, `account`, `cashDate`,
  or the final amount (`amount`/`discount`/`finesAndInterest`). Unreconcile it first.
- **Removal (`coreRemoveFinancialRecord`)** is blocked if the financial record is reconciled, linked
  to a radar item, or part of an internal transfer. Remove the link first.
- **The synchronous batch endpoint `corePartialUpdateManyFinancialRecords` is ATOMIC** (single transaction):
  if one id fails, everything is rolled back; there is never partial state.
- **Batch creation:** maximum **100** financial records per request (`coreCreateManyFinancialRecords`).

## Async bulk operations (`coreScheduleBulkUpdate`, `coreScheduleBulkRemove`, `coreScheduleBulkCreate`)

- **Not atomic** (best effort): processes in batches of about 50, applies what succeeds, **records
  failures**, and continues. Final result is "X succeeded, Y failed". Poll the job and read the
  failures before reporting. Update/remove mainly support `FINANCIAL_RECORDS` and `CONTACTS`.

## AI-assisted reconciliation (`coreCreateOrUpdateBankTransactionBestSuggestedAction`)

The AI returns `operation`: **LINK** (link to an existing `linkData.financialRecordId`) or
**CREATE** (create `createData.financialRecord`, then reconcile). There is no single "execute suggestion"
endpoint; orchestrate it: create if `CREATE`, then call `coreReconcileBankTransaction`.

## Internal transfer (`coreCreateInternalTransfer` / `coreCreateFinancialRecordGroup`)

The two financial records must be 1 IN + 1 OUT, have the **same amount**, the same dates (due,
cash, accrual), the same completion status, both have an account, have no discount and no fines/interest,
and both subcategories must have `isInternalTransfer = true`.

## Installments (`coreCreateInstallmentFinancialRecord`)

Number of installments > 1 and equal to `numberOfInstallments`; **sum of installments = total amount**;
installments must be **ordered by due date**.

## Recurring records (`coreCreateRecurringFinancialRecord`)

Repeat day is 1-7 for weekly frequency or 1-31 for monthly frequency; repeat month is required for yearly frequency.

## Subcategories (`coreCreateSubcategory`, `corePartialUpdateSubcategory`, `coreRemoveSubcategory`)

- `isInternalTransfer` **cannot change** after it is set.
- **Do not remove** a subcategory with records (regular, installment, or recurring): reassign first,
  or deactivate it (`active=false`).
- At least one IN subcategory and at least one OUT subcategory must remain.
- Top-level categories are **read-only** (there is no create/update/delete API for them).

## Contacts (`coreCreateContact`, `corePartialUpdateContact`, `coreRemoveContact`)

- System-generated contacts (for example, "Nao identificado") cannot be updated or removed.
- Document numbers (CPF/CNPJ), when provided, are validated.

## Bank accounts (`coreCreateBankAccount`)

- Institution is required for bank accounts and forbidden for "cash" accounts.
- Initial balance (date + amount) is required for accounts that are not credit cards.
- Credit cards cannot be default accounts and cannot be included in cash flow.
- The default account cannot be removed, deactivated, or changed to non-default. Promote another account first.

## Bank transactions

- `amountInBrl` cannot be < 0. Do not archive a reconciled transaction. OFX is only for manual accounts.
- Removing a reconciled transaction unreconciles it and **notifies organization members by email** (customer-visible effect).

## NFSe / legal entities (`coreCreateDefaultInvoice`, `coreCreateLegalEntity`)

Issuance requires preconditions (valid CNPJ/CPF, municipal registration when required, recipient address
in certain municipalities, contact email, compatible service code). The default legal entity cannot be removed.

## Permissions

Administrative organization operations (updating the organization, invitations, members) require an
**administrator** role. Organization slug must be unique.
