# Safe write protocol

For any operation that **writes** (create/update/delete, reconcile, bulk operation), follow this
flow. This is especially important for customers operating on real data.

## Standard flow

1. **Resolve names to ids** when the user refers to names (contact/account/subcategory):
   use `coreFindAllContacts`, `coreFindAllBankAccounts`, or `coreFindAllSubcategories` with text search.
2. **Show the affected organization** before anything else: always display `Organization: <name>`
   from `listMyOrganizations`. This is financial data; the user must see which organization the write will affect.
3. **Dry-run first.** List matching resources (`coreFindAllFinancialRecords`, etc.) and show:
   how many records match, a sample, the total impact in BRL, and exactly what will change,
   **including the filters used in plain text** (see "Filter transparency" below).
4. **Ask for one confirmation** for the entire batch, not item by item. For large volumes or deletions,
   confirm by typing the organization name.
5. **Snapshot before writing**: save the current state of affected ids to a file so the operation can
   be undone. For `CREATE`, store the created ids.
6. **Validate business rules first** (see `business-rules.md`) and fail with a clear message instead
   of triggering a raw 4xx response (for example, do not try to change the account of a reconciled financial record).
7. **On partial failure, stop and report.** Remember: `corePartialUpdateManyFinancialRecords` is
   atomic (there is never partial state); async bulk operations (`coreScheduleBulk*`) are best effort:
   poll the job and read the failures.

## Reuse one call vs loop

- **Same new value for all records**: one `corePartialUpdateManyFinancialRecords` call.
- **Different value per record**: loop over `corePartialUpdateFinancialRecord`, but ask for **one**
  confirmation. Partial failure is possible here, so the snapshot enables undo.

## Filter transparency (always)

Every listing/report/batch must declare filters in Portuguese and **translate relative dates
to absolute dates**. Example: "payments next week" becomes
`Direção: Saída; Data de vencimento: entre DD/MM/AAAA e DD/MM/AAAA; Concluído: Não`.
Make it clear which date field was used (due vs accrual vs cash date) and state assumptions
explicitly ("considerei só os não pagos").

## Undo

Revert using the snapshot: reapply the old values with `corePartialUpdateFinancialRecord`;
for `CREATE`, unreconcile if needed and then call `coreRemoveFinancialRecord` for the created ids.
