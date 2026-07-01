# Workflow: apply category tree template

Reorganizes **subcategories** from a user-provided template (BPOs often have ready-made templates),
adapting to the organization's current state. Top-level categories are read-only; the reorganization happens in subcategories
(`coreCreateSubcategory`, `corePartialUpdateSubcategory`, `coreRemoveSubcategory`,
`coreFindAllSubcategories`).

## State detection
- **Empty organization** = no financial records linked to subcategories.
- **Organization with records** = there are links (check per subcategory, not only in aggregate).

## Match first to avoid orphaned history
Match template entries to existing subcategories by **normalized name**, within the same direction, and
**reuse** matches (rename/move in place). Creating a "new" subcategory with the same name and deactivating
the old one leaves historical records pointing to the dead subcategory and breaks reports.

## Decision per subcategory
| Situation | Empty organization | Organization with records |
|---|---|---|
| In the template and already exists | Reuse it (rename/move/reorder `index`). | Same, preserving history. |
| In the template and does not exist | Create it. | Create it. |
| Removed from the template and **empty** | Delete it. | **Offer deletion** (safe). |
| Removed from the template and **has records** | Does not apply. | **Deactivate it** (`active=false`); optionally **merge** by reassigning records (bulk update) to a template subcategory and then deleting it. |

## Rules (see business-rules.md)
Subcategory direction = parent category direction (IN only under an IN category). Do not delete a
subcategory with records: reassign first or deactivate it. Keep at least one IN subcategory and at least one OUT subcategory.
`isInternalTransfer` cannot change after it is set.

## Execution
Run a dry-run showing the plan (create/rename/move/deactivate/delete/merge) with the **record count**
for each affected item -> snapshot the tree -> ask for one confirmation -> execute
(reuse before creating; applying the same template again is idempotent) -> report the result.

## Template format
Accept the template in the format provided by the user (indented list, JSON, table): top-level category -> subcategories,
with optional flags (`considerInDre`, `isInternalTransfer`). Direction comes from the top-level category; ask if it is ambiguous.
