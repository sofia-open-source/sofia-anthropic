---
name: sofia-fin-system-api
description: Sofia API for financial management of bussiness. Provides management of bank accounts, financial records (in/out/paid/to be paid), invoices, contacts etc. Provides reports and bank reconciliation. Use when working with the Sofia Fin System API or when the user needs to interact with this API.
metadata:
  api-version: "1.4.36"
  openapi-version: "3.0.0"
---

# Sofia Fin System API

Sofia API for financial management of bussiness. Provides management of bank accounts, financial records (in/out/paid/to be paid), invoices, contacts etc. Provides reports and bank reconciliation.

## How to Use This Skill

This API documentation is split into multiple files for on-demand loading.

**Directory structure:**
```
references/
├── resources/      # 33 resource index files
├── operations/     # 134 operation detail files
├── schemas/        # 73 schema groups, 199 schema files
├── business-rules.md
├── write-safety-protocol.md
└── workflows/      # Guided multi-step API workflows
```

**Navigation flow:**
1. Find the resource you need in the list below
2. Read `references/resources/<resource>.md` to see available operations
3. Read `references/operations/<operation>.md` for full details
4. If an operation references a schema, read `references/schemas/<prefix>/<schema>.md`

**Additional references:**
- [Backend business rules](references/business-rules.md): important runtime invariants that are not fully represented in OpenAPI, such as reconciliation, financial record locks, categories, contacts, bank accounts, and permissions.
- [Safe write protocol](references/write-safety-protocol.md): required flow for create, update, delete, reconcile, and bulk operations, including organization display, dry-run, confirmation, snapshots, filter transparency, and undo guidance.

**Workflow guides:**
- [Apply category tree template](references/workflows/category-tree.md): reorganizes subcategories from a user-provided template while preserving historical records and avoiding orphaned reports.
- [Financial diagnostic dashboard](references/workflows/diagnostic-dashboards.md): turns financial reports into diagnostic dashboards with indicators, benchmarks, traffic-light status, health score, and actionable insights.

## Base URL

https://app-proxy-public-prod.sofia-fin-system.com

## Authentication

Supported methods: bearer token on header. See `references/authentication.md` for details.

## Resources

- **Core - Bank Transactions** → `references/resources/Core-Bank-Transactions.md` (14 ops) - Imported bank statement lines from OFX manual import or open finance (Pluggy), used to reconcile against financial records. CRUD-style read/update/delete, reconcile and unreconcile, bulk archive/unarchive/reconcile, and AI-suggested actions for matching. OFX import flows schedule jobs, list executions, retry failures, and download failure reports. System endpoints support provider-driven create-or-update for integrated feeds.
- **Core - Financial Records** → `references/resources/Core-Financial-Records.md` (11 ops) - The main resource of the system, represents an amount (paid/received/to be payed/to be received) for the organization on the system. It is used in the majority of all reports and is linked to many other resources like contacts, tags, bank transactions, radar items etc.
- **Core - Legal entities** → `references/resources/Core-Legal-entities.md` (8 ops) - Legal entities (CNPJ) and fiscal registration data for the organization. CRUD, set default entity for invoicing, and get/patch Focus NFSe RPS settings per entity. Required for NFSe issuance and provider configuration. One organization may hold multiple entities but typically invoices from the default.
- **Core - Contacts** → `references/resources/Core-Contacts.md` (8 ops) - People and companies (customers, suppliers, employees) linked to financial records. Full CRUD plus paginated list, find-by-id, and org-scoped lookups. Reference endpoints expose contact types and origins. Includes lookup of the special not-identified contact used when no counterparty is known.
- **Core - Invoices** → `references/resources/Core-Invoices.md` (7 ops) - Fiscal invoice (NFSe) lifecycle for the organization: issue municipal (default) or national service invoices, cancel, list, and find by id. Invoice events expose status history; Focus NFe webhooks and scheduler/queue jobs sync state with the external provider. Creation and cancellation are the primary mutations; there is no generic partial-update endpoint.
- **Core - Financial Record Radar Items** → `references/resources/Core-Financial-Record-Radar-Items.md` (7 ops) - Represents the intent to create(one or many)/update financial records on the system based on a WhatsApp message or email.
- **Core - Bank Accounts** → `references/resources/Core-Bank-Accounts.md` (7 ops) - Organization bank accounts: checking, savings, and credit card. CRUD, paginated list, find-by-id, org-scoped list, and account-type reference data. Supports open-finance lookup by Pluggy item id for linked accounts. Accounts anchor bank transactions and balance analytics.
- **Core - Subcategories** → `references/resources/Core-Subcategories.md` (6 ops) - Expense and revenue subcategories under system-managed categories. Org-owned CRUD, paginated list, find-by-id or slug, and org-scoped listing. Subcategories classify financial records in reports and budgets. Categories themselves are not mutated via this API.
- **Core - Recurring Financial Records** → `references/resources/Core-Recurring-Financial-Records.md` (6 ops) - Recurrence templates that define rules for seeding future financial records (frequency, amounts, contacts, categories, etc.). Full CRUD plus POST /many for batch creation of templates. Internal scheduler and queue workers activate templates and materialize due occurrences into financial records. Active templates drive automated bookkeeping without manual entry for each period.
- **Core - Tags** → `references/resources/Core-Tags.md` (5 ops) - Free-form classification tags attached to financial records. CRUD, paginated list, find-by-id, and org-scoped tag list. Tags enable flexible filtering and reporting dimensions beyond categories. Scoped to the leaf organization.
- **Core - Financial records invoices associations** → `references/resources/Core-Financial-records-invoices-associations.md` (5 ops) - Explicit links between financial records and issued invoices (NFSe). Create one association, create many in batch, paginated list with filters, find-by-id, and delete. There is no update endpoint; remove and recreate to change a link. Associations support reporting and audit trails where a payment or revenue line ties to a fiscal document.
- **Core - Installment Financial Records** → `references/resources/Core-Installment-Financial-Records.md` (5 ops) - Parent financial records split into installments, each with its own due date and amount. Supports create, paginated list, find-by-id, partial update, and delete on /core/installment-financial-records. List endpoints accept filters and populate related data. Installments are the template from which individual financial-record lines can be generated over time.
- **Toolkit - Files upload** → `references/resources/Toolkit-Files-upload.md` (4 ops) - Two-step upload to Google Cloud Storage. Create upload request returns fileId and a signed PUT URL; after the client uploads bytes, confirm upload marks the file complete. User routes live under /toolkit/files/upload; system routes under /toolkit/organizations/:organizationId/files/upload for cross-service uploads. Used by bulk import, attachments, and export download prep.
- **Toolkit - Files** → `references/resources/Toolkit-Files.md` (4 ops) - File metadata and access after upload. Find by id, delete, and generate signed download URLs from stored object URLs. System find-by-id accepts an organization id for internal callers. Files are owned by an organization and referenced by exports, bulk jobs, and attachments.
- **Analytics - Financial Records Reports** → `references/resources/Analytics-Financial-Records-Reports.md` (3 ops) - Read-only GET analytics built on financial records: aggregated totals, grouped aggregations, and monthly breakdowns. Supports saved-query filters via queryId and standard date or dimension params. Used for dashboards, KPI tiles, and drill-down charts. Deprecated system variants exist for internal cross-service use and are excluded from public skill docs.
- **Analytics - Financial Statements Reports** → `references/resources/Analytics-Financial-Statements-Reports.md` (3 ops) - DRE (income statement) and related financial-statement reports for a period. Endpoints return the main statement, financial measures, and result-composition breakdowns. All are GET-only and filterable by period and saved queries. Outputs feed P&L views and management reporting; no mutation endpoints.
- **Core - Financial Record Groups** → `references/resources/Core-Financial-Record-Groups.md` (3 ops) - Groups that tie related financial records together (e.g. split payments or linked entries). Create a group, find the group containing a given financial-record id, and delete a group. No list-all or partial-update endpoints. Groups help the UI and analytics treat multiple records as one logical transaction.
- **Analytics - Cash Flow Reports** → `references/resources/Analytics-Cash-Flow-Reports.md` (3 ops) - Cash-flow analytics: full-period report, current-month snapshot, and projected cash flow. All endpoints are GET under /analytics/cash-flow with date and filter params. Projections extrapolate from scheduled and recurring inflows/outflows. No write operations; purely analytical read models.
- **Analytics - Organization Balance** → `references/resources/Analytics-Organization-Balance.md` (3 ops) - Balance analytics per bank account and rolled up to organization total. GET endpoints return historical balance series, current per-account balances, and organization-wide total. Used for treasury views and balance-over-time charts. Derived from reconciled movements and account metadata; read-only.
- **Core - Contacts Export** → `references/resources/Core-Contacts-Export.md` (2 ops) - Export contacts in csv or xlsx format. POST /core/contacts/export schedules async export; POST …/export/sync returns the file immediately. List filters (types, sort, search, etc.) apply to exports. Use for CRM-style extracts and spreadsheet workflows.
- **Core - Subcategories Export** → `references/resources/Core-Subcategories-Export.md` (2 ops) - Export subcategories in csv or xlsx format. POST /core/subcategories/export for async jobs; POST …/export/sync for immediate download. Exports respect list filters and sort options. Handy for chart-of-accounts reviews and migrations.
- **Core - Tags Export** → `references/resources/Core-Tags-Export.md` (2 ops) - Export tags in csv or xlsx format. POST /core/tags/export schedules async export; POST …/export/sync returns the file synchronously. Same scope as the organization tag list. Use for backup or bulk review of labeling conventions.
- **Core - Financial Records Export** → `references/resources/Core-Financial-Records-Export.md` (2 ops) - Contains endpoints to export the financial records of the organization synchronously or asynchronously in csv or xlsx format. You can export all records or filter them.
- **Core - Bank Accounts Export** → `references/resources/Core-Bank-Accounts-Export.md` (2 ops) - Export bank accounts in csv or xlsx format. POST /core/bank-accounts/export enqueues async export; POST …/export/sync returns the generated file in one response. Optional id filters narrow the export set. Useful for account registers and external treasury tools.
- **Core - Bank Transactions Export** → `references/resources/Core-Bank-Transactions-Export.md` (2 ops) - Export endpoints for bank transactions in csv or xlsx format. POST /core/bank-transactions/export schedules async export; POST …/export/sync produces the file synchronously. Query params match list filters (bank account, date range, type, reconciled status, origin, etc.). Useful for reconciliation audits and spreadsheet analysis outside the app.
- **Core - Recurring Financial Records Export** → `references/resources/Core-Recurring-Financial-Records-Export.md` (2 ops) - Export endpoints for recurring financial record templates in csv or xlsx format. POST /core/recurring-financial-records/export enqueues async export; POST …/export/sync returns the file in the same request. Filters mirror the list API so exports can be scoped by organization and template attributes. Prefer async export for large template sets.
- **Core - Installment Financial Records Export** → `references/resources/Core-Installment-Financial-Records-Export.md` (2 ops) - Export endpoints for installment financial records in csv or xlsx format. POST /core/installment-financial-records/export schedules an async job and returns a pending job id; POST …/export/sync runs immediately and returns the job id plus the generated file. Both accept the same query filters as the list endpoint. Use async export for large datasets; use sync when the caller needs the file in the same response.
- **Core - Bulk Invoices** → `references/resources/Core-Bulk-Invoices.md` (1 ops) - Batch NFSe issuance for many invoices in one operation. POST /core/invoices/bulk schedules an async job with the payload of invoices to create (default or national). A queue worker processes each item and records successes and failures. Use when issuing a large set of service invoices from a single user action or integration.
- **Core - Bank Institutions** → `references/resources/Core-Bank-Institutions.md` (1 ops) - Read-only reference catalog of Brazilian banking institutions (codes, names, and metadata). Single list endpoint GET /core/bank-institutions; no create, update, or delete. Consumed when registering bank accounts and interpreting open-finance institution identifiers. Data is system-managed and shared across all organizations.
- **Core - Bulk Remove** → `references/resources/Core-Bulk-Remove.md` (1 ops) - Async bulk deletion across supported core resources. POST /core/bulk/remove accepts resource type and ids, schedules a job, and returns a job id; a queue worker performs the deletes. Supported types include financial records, contacts, bank accounts, bank transactions, installments, recurrences, tags, subcategories, and invoices. Use for mass cleanup from UI selections or integrations.
- **Core - Bulk Create** → `references/resources/Core-Bulk-Create.md` (1 ops) - Async bulk creation from uploaded spreadsheet files. POST /core/bulk/create schedules a job with resource type, fileId, and optional radar-item context; the worker parses rows and creates entities. Financial-record imports can leverage AI/file-extraction flows. Same resource families as bulk remove where creation applies.
- **Core - Bulk Update** → `references/resources/Core-Bulk-Update.md` (1 ops) - Async mass update of fields on a resource type. POST /core/bulk/update schedules a job describing target ids and patch payload; the queue worker applies changes in batch. Supports the same core resource set as other bulk operations. Use for spreadsheet-driven corrections or integration sync-back.
- **Core - Users** → `references/resources/Core-Users.md` (1 ops) - Provide one endpoint to list all organizations that the authencticated user has access.
