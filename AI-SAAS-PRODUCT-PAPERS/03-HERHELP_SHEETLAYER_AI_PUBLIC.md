# HerHelp SheetLayer AI

## Executive Summary

SheetLayer AI helps people understand and operate the spreadsheets they already use for business. It can map workbook structure, explain formulas and fields, prepare clearer views, turn selected records into follow-up work, support controlled updates, and identify information that needs restricted handling.

The product is organized into five focused layers. SheetMap interprets workbook structure and business meaning. SheetView prepares readable summaries and dashboards. SheetFlow converts reviewed records into actions. SheetSync supports controlled imports, exports, and change review. SheetGuard applies permission and sensitive-field checks.

SheetLayer AI assists with spreadsheet work; it does not make the underlying records authoritative or automatically correct. Users remain responsible for source quality, access rights, review, and decisions based on the outputs.

---

## 1. Product Purpose

Spreadsheets are often the working system behind a shop, project, community, training program, or small business. They are familiar and flexible, but that flexibility can leave important logic scattered across tabs, formulas, notes, and naming conventions.

SheetLayer AI gives users a structured way to answer questions such as:

- What does this workbook contain?
- Which tabs and fields are related?
- Where are records missing, inconsistent, or duplicated?
- What does a formula appear to calculate?
- Which rows require action?
- Which information can be summarized for another audience?
- Which columns contain personal, financial, or confidential data?
- What changed between two reviewed versions?

The product is intended to improve comprehension and workflow around a spreadsheet, not force a business to replace its existing records with a new operating system.

---

## 2. Intended Users

SheetLayer AI may support:

| User | Typical need |
|---|---|
| Shop owner | Review product, stock, sales, staff, or expense records |
| Small-business operator | Turn manual trackers into clearer summaries and follow-up lists |
| Founder or project lead | Organize roadmap, evidence, budget, or contact workbooks |
| Community manager | Separate member records from shareable activity reporting |
| Trainer | Review progress, quiz, attendance, and onboarding data |
| Product team | Map issue, test, feedback, and release records |
| Analyst or reviewer | Understand a supplied workbook without changing its source structure |

Users can work with one workbook or a selected portion of it. Access should be limited to the tabs, ranges, and fields required for the task.

---

## 3. The Five SheetLayer Functions

### 3.1 SheetMap

SheetMap interprets the structure of a workbook. It can identify tabs, headings, likely field types, relationships, formulas, and repeated patterns. The resulting map helps a user understand how the file is organized before requesting changes or reports.

Possible outputs include:

- a workbook inventory;
- field and tab descriptions;
- a formula explanation;
- likely key-field identification;
- a list of incomplete or inconsistent columns;
- duplicate-record candidates; and
- a proposed data dictionary.

The map is an interpretation of the supplied file. Ambiguous business meaning should be confirmed by someone who understands the source process.

### 3.2 SheetView

SheetView prepares selected records for easier reading. It can organize filtered tables, summary cards, management views, and dashboard drafts without changing the meaning of the source data.

A user might request:

- a low-stock view for a shop;
- a weekly sales and expense summary;
- an onboarding completion view;
- a campaign status table;
- a roadmap progress summary; or
- a mobile-friendly view of selected fields.

Each view should identify its source range, filters, reporting period, and known limitations. A presentation layer does not become the source of record merely because it is easier to read.

### 3.3 SheetFlow

SheetFlow turns reviewed rows into defined follow-up work. It can group records by status, prepare checklists, identify exceptions, and route selected items into supported HerHelp workflows.

Examples include:

- converting overdue rows into an action list;
- grouping stock exceptions for review;
- preparing follow-up tasks from approved customer records;
- identifying incomplete training modules;
- organizing product issues by owner or priority; and
- creating a review queue from flagged entries.

The user determines whether an identified item becomes a task and who is permitted to receive it.

### 3.4 SheetSync

SheetSync supports controlled movement between a workbook and another approved system or file. Its role is to make changes visible and reviewable rather than silently treating every source as interchangeable.

Depending on available connections, the process may include:

- selecting the source and destination;
- matching fields;
- comparing versions;
- previewing additions, edits, and conflicts;
- approving an import or export;
- recording rejected rows; and
- preparing an exception summary.

Integration availability depends on the product configuration. Where a live connection is unavailable, SheetLayer AI can still help prepare a mapping or reviewed export for manual use.

### 3.5 SheetGuard

SheetGuard helps users inspect permissions and sensitive fields before data is processed, shared, or exported. It can flag likely personal details, payment information, private notes, credentials, or other fields that warrant additional care.

SheetGuard may support:

- role-based view planning;
- hidden-tab review;
- redaction suggestions;
- public-summary preparation;
- destination checks;
- field-level exclusion; and
- confirmation that a proposed output contains only the necessary records.

Automated detection can miss context. A user with appropriate authority should review sensitive-data decisions.

---

## 4. Standard Workflow

### Step 1: Select the source

The user chooses a workbook, file, tab, range, or export that they are authorized to use. The task description should state the intended outcome and audience.

### Step 2: Inspect before acting

SheetMap prepares an initial structure and quality review. The user confirms headings, relationships, and any business terms that cannot be inferred reliably.

### Step 3: Choose an output

The user requests a view, action list, transformation, sync plan, or permission review. The selected operation determines which records are needed.

### Step 4: Preview the result

SheetLayer AI presents a draft with relevant assumptions, filters, or exceptions. Changes to data should be distinguishable from explanatory notes and presentation choices.

### Step 5: Review and approve

An authorized user checks the result. Material errors, outdated records, or unsuitable fields can be corrected or removed before the output is used.

### Step 6: Export or hand off

Approved results can be downloaded, returned to a workbook, or passed to another supported workflow. A handoff should preserve the purpose and permission limits established for the task.

### Step 7: Retain an operational record

Where configured, SheetLayer AI can retain task status, usage, approval, and exception information. Retention settings should reflect the sensitivity and continuing value of the record.

---

## 5. Practical Workflows

### Shop stock review

A shop owner selects current product and inventory tabs. SheetMap confirms the product identifier and stock fields. SheetView prepares low-stock and missing-price views, while SheetFlow creates a review list for the owner. After approval, selected records may support a [ShopOS AI](./04-HERHELP_SHOPOS_AI_PUBLIC.md) workflow.

### Staff onboarding tracker

A manager provides a training workbook containing staff roles, assigned modules, and completion status. SheetGuard excludes unnecessary personal fields. SheetView summarizes progress, and SheetFlow prepares follow-up items. Approved source material can then support [TrainLayer AI](./06-HERHELP_TRAINLAYER_AI_PUBLIC.md).

### Community activity report

A community team uses a workbook for event attendance, moderator actions, and campaign tasks. SheetGuard separates member details from reporting fields. SheetView creates an aggregated activity summary, while [CommunityLayer AI](./07-HERHELP_COMMUNITYLAYER_AI_PUBLIC.md) can use authorized items for the related operating workflow.

### Product readiness review

A product lead selects issue, test, and release tabs. SheetMap documents status fields and dependencies. SheetFlow groups unresolved items by owner, and SheetView prepares a readiness summary that clearly distinguishes completed evidence from planned work.

### Version comparison

An operator receives a revised supplier or catalog file. SheetSync maps identifiers and previews added, removed, and changed rows. The operator resolves conflicts before approving an updated export.

---

## 6. Product Connections

SheetLayer AI is a specialist module within [HerHelp AI SaaS](./02-HERHELP_AI_SAAS_PUBLIC.md). It can provide structured, reviewed information to another HerHelp module when the user authorizes the transfer.

Useful connections may include:

- ShopOS AI for catalog and operating records;
- TrainLayer AI for approved learning and progress data;
- CommunityLayer AI for permissioned activity workflows;
- SpeakShop AI for selected campaign or product fields; and
- FUZE reporting rails for suitable operational summaries.

A connection should move the minimum information required for the destination task. It should not make the full workbook visible to every connected product.

---

## 7. Platform Credit Use

SheetLayer tasks may consume Platform Credits when they use metered processing. Examples can include:

- mapping a workbook or selected range;
- explaining a set of formulas;
- checking records for inconsistencies;
- generating a dashboard draft;
- preparing a workflow queue;
- comparing file versions;
- reviewing likely sensitive fields; or
- producing an approved summary or export.

The applicable amount can vary with the size and complexity of the task. Users should receive the relevant usage information before confirming a chargeable operation.

Credits meter product activity inside SheetLayer AI. They remain separate from the FUZE token and do not provide ownership or market rights.

---

## 8. Data and Permission Controls

Spreadsheets can combine ordinary operating records with highly sensitive material. A single workbook may contain customer contact details, staff schedules, commercial terms, payment notes, wallet addresses, or internal comments.

SheetLayer AI should therefore apply controls appropriate to the selected data and task, including:

- authorization to connect or upload the source;
- selection of only the required workbook area;
- workspace and role separation;
- review of hidden tabs and columns;
- output and export permissions;
- redaction or exclusion of unnecessary fields;
- retention and deletion settings;
- connection revocation; and
- activity records for significant changes.

Public or partner-facing summaries should use aggregated or non-identifying information unless there is a valid reason and authority to disclose more. Wallet-level records, where present in a source, should not be used to reveal a person's private identity.

Further data-handling principles are described in [FUZE Data, Privacy and AI Data Handling](../CORE-PLATFORM-PAPERS/07-FUZE_DATA_PRIVACY_AND_AI_DATA_HANDLING_PUBLIC.md).

---

## 9. Reporting

SheetLayer reporting can help a user understand both the source workbook and the processing performed around it. Depending on the task and configuration, reports may show:

- source and reporting period;
- tabs, ranges, or files reviewed;
- records processed or excluded;
- quality and exception findings;
- views or workflow items generated;
- approved imports and exports;
- unresolved sync conflicts;
- Platform Credit usage; and
- reviewer or approval status.

Reports should distinguish observed source data from AI interpretation and user-supplied assumptions. Corrections should be traceable to the relevant task or source version.

---

## 10. Product Boundary

SheetLayer AI can explain, organize, transform, and route spreadsheet information. It cannot establish that supplied records are complete, current, lawful, or suitable for a particular accounting, tax, financial, employment, or regulatory purpose.

Users are responsible for validating important formulas, figures, classifications, and outputs with appropriate subject-matter review. Automated suggestions should be treated as working assistance, especially when a workbook influences payments, legal obligations, personnel decisions, or public reporting.

The product does not require wallet participation to perform its spreadsheet role. Detailed ecosystem participation and token mechanisms are covered in their dedicated FUZE papers rather than this product guide.

---

## 11. Conclusion

SheetLayer AI adds structure around the spreadsheet rather than obscuring it. SheetMap explains the file, SheetView makes selected records easier to read, SheetFlow prepares follow-up work, SheetSync exposes proposed changes, and SheetGuard helps control sensitive information.

Together, these functions give spreadsheet-based users a clearer route from raw records to reviewed business action while preserving human approval and source-level accountability.
