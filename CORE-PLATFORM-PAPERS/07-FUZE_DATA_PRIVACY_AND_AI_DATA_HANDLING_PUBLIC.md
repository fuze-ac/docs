# FUZE Data Privacy and AI Data Handling

## Executive Summary

FUZE products may process business, shop, community, training, game, event, market-research, wallet, payment, usage, and AI-workflow data.

This paper defines the public platform model for handling that information:

- classify the data;
- collect only what the workflow needs;
- confirm authority and purpose;
- restrict access by role and context;
- control what may be sent to AI providers or tools;
- preserve human review for sensitive outputs and actions;
- retain records only for their approved purpose and required obligations;
- support correction, export, deletion, and incident response where applicable; and
- publish only reviewed public-safe records or aggregates.

Public transparency does not require publishing personal identity, customer content, private prompts, credentials, agreements, tax or accounting records, wallet-to-person mappings, or security-sensitive operational material.

A wallet address may appear in a public-safe record while any identity verification, custody review, support history, or eligibility evidence associated with it remains permissioned.

The controls described here are platform expectations. Product-specific notices, agreements, implementation details, security measures, provider terms, and jurisdictional requirements must describe the actual operating model where applicable.

## Purpose of This Paper

This paper explains:

- the principles governing FUZE data use;
- the public data-classification model;
- the lifecycle from collection through deletion;
- purpose-based permissions;
- AI prompt, context, provider, tool, output, and review controls;
- product-specific handling examples;
- wallet and public-identity separation;
- public-safe reporting and de-identification;
- logging, incidents, and correction; and
- the limits of this public framework.

The [FUZE Core Platform Rails](./04-FUZE_CORE_PLATFORM_RAILS_PUBLIC.md) defines the shared service boundaries. The investor and partner view appears in [FUZE Data Privacy and Permission Model](../INVESTOR-PARTNER-PAPERS/08-FUZE_DATA_PRIVACY_AND_PERMISSION_MODEL_PUBLIC.md). AI assurance is addressed in [FUZE AI Safety and Reliability](../INVESTOR-PARTNER-PAPERS/07-FUZE_AI_SAFETY_AND_RELIABILITY_PUBLIC.md).

## Data Handling Principles

FUZE applies the following principles across products and shared services.

| Principle | Practical meaning |
|---|---|
| Purpose limitation | Use information only for the stated product, support, security, financial, reporting, or operating purpose |
| Data minimization | Request and process only the fields, records, range, and period needed for the workflow |
| Authority | Confirm that the user, workspace, partner, product, or operator may provide and use the information |
| Least privilege | Give each person, service, model, and tool only the access needed for the approved task |
| Context separation | Keep unrelated products, workspaces, customers, public reports, diligence rooms, and private reviews separate |
| Human authority | Preserve required human judgment before sensitive AI output drives action, publication, payment, moderation, eligibility, or market operations |
| Traceability | Record important access, model, tool, permission, export, publication, correction, and administrative events |
| Retention discipline | Keep records only for their approved operating, security, contractual, financial, legal, or support need |
| Correction and accountability | Preserve reviewable records when information, access, output, or publication is corrected |
| Public-safe reporting | Publish only information suitable for the stated transparency purpose and audience |
| Status discipline | A policy paper does not prove that every control is implemented, tested, certified, or live |

These principles should shape product design, provider selection, system architecture, operations, support, and public reporting. They should not exist only as disclosure text.

## Data Classification

Classification determines collection, access, AI use, storage, sharing, reporting, retention, and deletion treatment.

| Class | Examples | Default handling |
|---|---|---|
| Public | Approved product pages, public documentation, approved reports, public event details, verified public wallet or contract references | Available only for the approved public purpose |
| Workspace | Drafts, prompts, reports, settings, internal content, task history, product activity | Limited to authorized workspace roles and services |
| Customer or participant | Orders, support messages, community activity, learner records, event registrations, player support history | Product-specific access and disclosure controls |
| Financial and usage | Payments, Platform Credit events, invoices, refunds, reconciliation, compensation, treasury classifications | Restricted operational, support, finance, and audit access |
| Sensitive identity | Names linked to verification, contact details, identity documents, addresses, recovery evidence | Strongly permissioned and excluded from public records by default |
| Partner or investor confidential | Negotiated terms, private agreements, diligence evidence, private metrics, implementation records | Qualified access under the applicable relationship |
| Security and credentials | API keys, tokens, private keys, access logs, vulnerability details, incident evidence, infrastructure access | Strict specialist access and dedicated retention |
| Wallet-public | Address, supported network, transaction, contract, vault, snapshot, claim, or public mechanism status suitable for publication | Public only where the mechanism and publication purpose justify it |
| Wallet-private context | Identity link, custody review, eligibility evidence, support history, account recovery, tax or compliance records | Permissioned separately from public wallet evidence |
| Derived or inferred | AI classifications, risk flags, summaries, profiles, predictions, correlations, or behavioral inferences | Treated according to source sensitivity, impact, accuracy, and approved use |

Data may change class only through an approved process.

A reviewed aggregate, redacted example, or public-safe status record may become public even when the underlying source records remain private.

Public availability of one field does not make every related field, inference, identity link, or cross-product use public.

## Data Lifecycle

### 1. Define the Purpose

Before collection, the product should identify:

- the user or operator;
- the task;
- the information required;
- the product or operating purpose;
- whether AI, a partner, or an external provider is involved;
- the expected output;
- the retention and reporting need; and
- the responsible product or service owner.

A broad statement such as “improve AI” is not a sufficient operational purpose for unrestricted collection or reuse.

### 2. Collect the Minimum Necessary Data

A product should distinguish required information from optional information.

Where data comes from a:

- spreadsheet;
- shop system;
- community;
- training workspace;
- game;
- event;
- partner;
- wallet;
- uploaded file;
- external API; or
- connected service,

the product should identify the source and the authority to use it.

Bulk access should be avoided when a specific workbook, tab, range, record type, field set, wallet period, or time window is sufficient.

### 3. Validate Authority and Permission

Before access or processing, the system should consider:

- actor;
- role;
- workspace or organization;
- product;
- data class;
- requested action;
- purpose;
- device or service context;
- sensitivity;
- time or session; and
- policy version.

The permission question is:

```text
Can this actor or service perform this action
on this data
inside this product or workspace
for this stated purpose
at this time?
```

Possession of data does not authorize every use.

### 4. Process Within the Approved Scope

Processing should remain within the permitted purpose and context.

Access to a record does not automatically authorize:

- AI processing;
- model training or evaluation use;
- partner sharing;
- public reporting;
- marketing;
- cross-product profiling;
- financial classification;
- wallet eligibility;
- governance decisions;
- moderation or enforcement; or
- automated consequential action.

Each additional use requires the appropriate authority and control.

### 5. Store According to Sensitivity

Records should be stored in systems appropriate to their class and operating need.

Relevant considerations may include:

- access control;
- encryption;
- credential separation;
- backup and recovery;
- data location;
- provider and subcontractor access;
- tenant or workspace isolation;
- logging;
- retention; and
- deletion capability.

Public blockchains should contain only information appropriate for permanent public visibility.

Personal identity, customer content, private agreements, full prompts, credentials, tax records, private account evidence, signer identities, and detailed security evidence should not be placed on-chain.

### 6. Share or Export Under Controlled Scope

Exports and integrations should preserve classification and purpose.

A partner or provider receives only the fields required for its approved role, not broad access to unrelated products, workspaces, customers, wallets, or platform records.

Exports should identify, where appropriate:

- requester;
- workspace;
- scope;
- purpose;
- format;
- time;
- destination;
- approval; and
- resulting access or retention responsibility.

Public reporting uses reviewed aggregates, references, labels, ranges, or redacted examples.

Qualified investor, partner, auditor, legal, finance, or security review may use permissioned material that is not suitable for public publication.

### 7. Retain Only for the Required Purpose

Retention may differ by record type.

Examples include:

- product content and drafts;
- prompts and model outputs;
- support cases;
- account and role records;
- security logs;
- Platform Credit usage;
- payments and refunds;
- tax or accounting evidence;
- partner agreements;
- incident records;
- wallet references; and
- public reports.

A single platform-wide retention period may be inappropriate because operating, contractual, security, financial, legal, and user needs differ.

Retention should be documented in the relevant product or operational process.

### 8. Correct, Delete, or De-Identify Where Applicable

Users or authorized operators may be able to request correction, deletion, export, disconnection, or workspace closure according to the product and applicable rules.

Deletion applies to systems FUZE controls, subject to:

- valid retention requirements;
- active disputes;
- security investigations;
- financial or contractual obligations;
- technical limitations; and
- immutable public records.

An immutable public-chain record cannot be erased by an off-chain product.

Interfaces, labels, internal associations, publication references, access, or private records may still be corrected, restricted, removed, or superseded where appropriate.

De-identification should be evaluated for re-identification risk, especially where small groups, unique events, timestamps, wallet activity, or combined fields remain distinctive.

## Permission Model

Permissions combine identity, role, product, workspace, data class, action, purpose, and context.

Common actions include:

- view;
- create;
- edit;
- generate;
- connect;
- approve;
- publish;
- export;
- share;
- delete;
- administer; and
- execute a tool action.

### Role Examples

| Context | Possible separation |
|---|---|
| Shop | Owner manages settings; staff perform assigned operations; customers see their own transaction context |
| Spreadsheet workspace | Owner controls sources and integrations; editor runs approved tasks; viewer reviews outputs |
| Community | Administrator configures policy; moderator reviews queues; member uses permitted features |
| Training | Author creates material; reviewer approves it; learner accesses assigned content |
| Event | Organizer manages the workspace; partner receives scoped access; participant sees relevant registration context |
| Game | Operator manages product systems; moderator manages community tools; player accesses their product context |
| QTB | Authorized analyst uses approved sources; reviewer verifies material outputs |
| AIMM | Authorized operator accesses approved operational data; governance or risk roles review sensitive activity |
| ToolGrid AI | Sponsor manager controls campaign material; public users see approved listing and sponsorship labels |
| Botmad | User defines task, files, tools, credentials, and approval scope; reviewer approves consequential output |
| Partner integration | Partner service receives scoped fields; FUZE operator monitors access, quality, and lifecycle |

Administrative access should be limited, logged, reviewed, and used for defined support, security, maintenance, finance, or operational purposes.

Emergency access should be time-limited, attributable, and reviewed after use where the implementation supports it.

## AI Data Flow

An AI task should use a bounded and reviewable data path.

```text
Approved task -> permission check -> context minimization
-> provider and model policy -> execution -> validation or review
-> output and usage record -> retention or deletion treatment
```

### AI Task Definition

An AI task should identify, where relevant:

- product and task class;
- actor and workspace;
- source records;
- purpose;
- data class;
- permitted model or provider;
- tools or connectors;
- usage or cost limit;
- output format;
- safety and quality checks;
- human-review requirement;
- retention; and
- fallback behavior.

### Prompt Handling

Prompts may contain sensitive information even when the user does not recognize or label it.

Products should provide controls appropriate to their audience, such as:

- input guidance;
- source selection;
- field or range restriction;
- warnings;
- redaction;
- blocked categories;
- approval requirements; or
- provider-routing restrictions.

Prompt logging should be proportionate and should not create an uncontrolled duplicate of sensitive content.

### Context Minimization

Before sending information to a model or tool, the product should consider whether it can:

- remove unrelated fields;
- use a limited time period;
- replace direct identifiers;
- summarize locally;
- send a reference instead of a full record;
- separate private instructions from public source material; or
- avoid the external provider entirely.

### Output Handling

AI outputs inherit sensitivity from their sources and content until reviewed and reclassified.

A generated file should retain the source workspace's permission model unless an authorized action changes it.

An AI-generated public summary should not expose private source material merely because the output is newly written.

Outputs should preserve, where appropriate:

- source references;
- uncertainty;
- review status;
- correction history;
- model or policy version suitable for operations; and
- restrictions on publication or downstream action.

## AI Provider and Tool Boundaries

When an external model, API, connector, storage service, or tool is used, FUZE should evaluate:

- data sent;
- purpose;
- retention;
- model-training or service-improvement settings;
- processing location where relevant;
- subcontractors;
- connected tools;
- authentication and credential handling;
- encryption and access;
- logging;
- availability;
- incident handling;
- deletion capability;
- portability and exit; and
- contractual and security terms appropriate to the task.

Products should not send sensitive data to a provider whose controls do not fit the intended use.

A fallback provider should not silently weaken:

- privacy;
- retention;
- security;
- quality;
- model-use restrictions;
- geographic restrictions;
- human-review requirements; or
- user-facing expectations.

Provider status, certification, or contractual claims should be verified before publication and should not be generalized beyond the actual service and scope.

## Human Review and Automated Actions

Review strength should match impact.

| Output or action | Typical treatment |
|---|---|
| Low-impact draft or idea | User review before use |
| Business report or customer message | Authorized operator review |
| Generated formula, mapping, or data transformation | Source and result validation before reliance |
| Training content or quiz | Author or reviewer approval |
| Moderation or safety recommendation | Moderator decision and escalation path |
| Market interpretation | Source and analyst review; no automatic financial conclusion |
| Liquidity-operations observation | Authorized operator and applicable governance or risk review |
| Payment, treasury, refund, or accounting classification | Qualified operational or finance approval |
| Wallet eligibility or claim decision | Defined rule, evidence, authorization, and correction path |
| Legal, tax, compliance, or public-policy language | Specialist review |
| Tool action affecting files, systems, messages, or credentials | Explicit permission, logging, bounded scope, and reversibility where possible |
| Public report or disclosure | Evidence review, privacy review, approval, versioning, and correction path |

Automation should preserve an audit trail and provide a way to stop, correct, reverse, or roll back actions where the product supports that capability.

High-impact actions should not rely only on an AI confidence score or unreviewed model output.

## Product Context Examples

### SheetLayer AI

SheetLayer AI should limit access to the selected:

- workbook;
- tab;
- range;
- field set;
- connected data source; or
- approved reporting period.

Generated formulas, mappings, dashboards, and reports remain within the source workspace's permissions.

Customer, employee, payment, or sensitive business data should not enter AI context unless the approved task needs it and the provider, permission, retention, and review controls support that use.

### ShopOS AI

ShopOS AI may process:

- menu;
- order;
- queue;
- staff;
- stock;
- loyalty;
- device;
- customer;
- payment; and
- reporting information.

Staff should see only what their role requires.

Customer and payment records should not enter AI context merely because they are available inside the product.

Public business reports should use reviewed aggregates rather than expose customer identity, transaction history, phone numbers, addresses, or private staff records.

### SpeakShop AI

SpeakShop AI may process approved scripts, business details, voice settings, sound assets, and promotional content.

The product should distinguish:

- source content supplied by the workspace;
- provider-generated audio;
- licensed or approved voice and sound assets;
- private campaign drafts; and
- public final outputs.

A generated voice file should not become public without an authorized publication action.

### TrainLayer AI

TrainLayer AI may transform authorized source material into guides, quizzes, onboarding modules, and support content.

Learner responses, assessment results, personal progress, and private feedback should remain limited to the appropriate learner, trainer, reviewer, or workspace roles.

Training content derived from private company material should not be reused outside the approved workspace without authority.

### CommunityLayer AI

CommunityLayer AI may process approved community content for moderation assistance, support, verification workflows, summaries, and reporting.

Private messages, identity evidence, appeals, safety reports, sensitive moderator notes, and enforcement history require separate access and retention treatment.

Public community reports should use approved aggregates, categories, or redacted examples.

AI assistance should not replace required moderator judgment for sensitive actions.

### ZAGA Arena and ZAGA Districts

ZAGA Arena and ZAGA Districts are separate products and may process different combinations of:

- account or player identifiers;
- session records;
- gameplay telemetry;
- progression;
- community activity;
- support records;
- device data;
- game economy records; and
- selected wallet-aware references.

Gameplay data, Platform Credits, in-game value representations, FUZE token utility, wallet activity, and any future activated participation mechanism should retain separate classifications and records.

Public leaderboards or community reports should avoid exposing private account, identity, support, or security data.

### QTB

QTB may process approved public and private market-research sources, watchlists, notes, reports, and analyst workflows.

Private positions, account details, venue communications, credentials, unpublished strategy, customer records, and restricted sources require explicit access controls.

QTB output remains research and decision support. It should preserve source traceability and human review rather than be treated as an autonomous trading instruction.

### AIMM

AIMM may process authorized market, venue, treasury, liquidity-operations, monitoring, incident, and reporting data.

Access should be limited to approved operators and reviewers.

Private positions, credentials, venue communications, operational instructions, and exploitable market or security details should remain restricted.

Public reporting should use only reviewed public-safe information and should not expose sensitive operating strategy or imply guaranteed price, spread, depth, or liquidity.

### AIE

AIE should separate:

- public event information;
- organizer workspaces;
- participant registration;
- sponsor records;
- partner terms;
- operational notes;
- media or content assets; and
- public reports.

Participant and sponsor data should be used only for the approved event or relationship purpose.

### ToolGrid AI

ToolGrid AI should separate:

- public listing content;
- neutral discovery information;
- sponsored-placement content;
- sponsor-management records;
- campaign performance records;
- destination review evidence; and
- internal trust or safety notes.

Public sponsorship labels should not expose private commercial terms.

### Botmad

Botmad requires explicit permission for:

- files;
- folders;
- applications;
- tools;
- connectors;
- messages;
- credentials;
- destinations;
- task duration;
- spending or usage limits; and
- final consequential actions.

Botmad should operate within a bounded task and should not infer unrestricted authority from access to one file, application, account, or workspace.

Sensitive credentials should be handled through approved access methods and should not be inserted into prompts or logs unnecessarily.

## Wallet Records and Identity

A public wallet record may include:

- address;
- network;
- transaction;
- contract;
- vault;
- snapshot;
- report period;
- claim status;
- governance reference; or
- mechanism status

when that information is suitable and necessary for the approved public purpose.

Private systems may separately hold information needed for:

- support;
- custody treatment;
- account recovery;
- eligibility review;
- claim review;
- tax or accounting treatment;
- fraud or security review;
- legal or compliance review; or
- user verification.

Public reporting should not join those records to a person's identity unless an authorized and appropriate process specifically requires publication.

Self-custody and exchange custody may produce different evidence.

A public exchange address does not expose each customer's identity, balance, entitlement, or transaction history.

Public availability of a wallet transaction does not make every inferred identity, behavioral profile, financial conclusion, or cross-product use appropriate.

Wallet data used by AI remains subject to purpose, permission, provider, retention, and review controls.

A wallet record does not automatically establish eligibility, approved distributable value, a claim, payment, income, yield, or investment rights.

## Public-Safe Reporting and De-Identification

Public-safe reporting may use:

- counts;
- ranges;
- percentages;
- aggregated usage;
- status categories;
- reporting periods;
- report hashes or version references;
- verified wallet, vault, transaction, or contract references appropriate to the mechanism;
- redacted examples;
- correction records; and
- incident categories without exploitable detail.

Before publication, reviewers should consider whether:

- a small group can identify a person;
- timestamps reveal private activity;
- a unique event or transaction reveals identity;
- several harmless fields become identifying when combined;
- a wallet address can be linked to private records;
- a redacted example still exposes confidential terms;
- an incident summary reveals an attack path; or
- an aggregate exposes commercial strategy.

A public report should identify:

- scope;
- period;
- source category;
- aggregation or calculation basis;
- review status;
- version; and
- correction route.

Corrections should replace, annotate, or supersede the public version without exposing the private source material used to investigate the issue.

## Logging and Audit Records

Logs may record:

- authentication;
- failed access;
- role or permission changes;
- administrative access;
- exports;
- AI tasks;
- model or provider routes;
- tool actions;
- Platform Credit events;
- payment or refund events;
- wallet references;
- publication actions;
- corrections; and
- incidents.

Logging should be proportionate.

Logs should avoid unnecessary copies of:

- full prompts;
- private documents;
- credentials;
- customer messages;
- identity documents;
- payment details; or
- sensitive outputs.

Audit access should itself be permissioned and logged where appropriate.

## Incident Response

A data or AI incident process may include:

1. contain the affected account, role, integration, model route, tool, provider, report, or publication;
2. preserve evidence under restricted access;
3. identify affected data, users, workspaces, systems, partners, and jurisdictions;
4. assess whether unauthorized access, disclosure, processing, loss, corruption, or harmful output occurred;
5. correct permissions, records, outputs, or publication;
6. notify affected parties, partners, providers, or authorities where required;
7. restore or replace affected services where safe;
8. document root cause, lessons, and control changes; and
9. publish a public-safe update when appropriate.

Security-sensitive details remain restricted when publication would increase risk.

A public incident update should distinguish confirmed facts, current impact, actions taken, unresolved questions, and next update conditions.

## User and Workspace Controls

Depending on the product and applicable rules, users or workspace owners may be able to:

- review account and role settings;
- manage workspace members;
- connect or disconnect an integration;
- select approved data sources;
- manage AI or sharing permissions;
- review provider-related settings where exposed;
- export supported records;
- correct product information;
- request deletion or workspace closure;
- review Platform Credit and usage histories;
- review wallet references appropriate to their account;
- report an unexpected output or access event; and
- contact support for a restricted or retained record.

The product should explain:

- which actions are self-service;
- which require another workspace role;
- which require support or specialist review;
- which records must be retained;
- what deletion or correction can and cannot change; and
- what happens after workspace closure.

## Retention and Deletion Decision Model

A retention decision should consider:

| Question | Example consideration |
|---|---|
| Why is the record needed? | Product delivery, support, security, dispute, finance, contract, reporting, or legal obligation |
| Who owns the record? | User, workspace, product, platform service, finance, security, or partner function |
| Who may access it? | Defined roles and service accounts |
| How long is it needed? | Product term, support period, contractual period, security need, or required obligation |
| Can it be minimized? | Remove fields, aggregate, redact, or retain only a reference |
| Can it be deleted? | Depends on system control, obligation, investigation, and technical constraint |
| Is it immutable? | Public-chain records may remain permanent |
| What is the correction path? | Update, annotate, supersede, restrict, or remove internal association |

Deletion claims should not exceed the actual technical and legal capability of the product.

## AI Training and Evaluation Boundary

Product use does not automatically authorize customer or workspace data for model training, provider training, broad product evaluation, or unrelated service improvement.

Where training or evaluation use is proposed, the relevant implementation should define:

- the data source;
- purpose;
- authority;
- provider;
- retention;
- de-identification where applicable;
- access;
- review;
- opt-in or opt-out treatment where applicable; and
- deletion or withdrawal behavior where technically and legally possible.

Synthetic, public, licensed, permissioned, or specifically prepared evaluation data may have different treatment from private customer or workspace data.

A public statement should not claim that data is never used for training unless the actual product, provider, configuration, and contractual evidence support that statement.

## Children, Vulnerable Users, and Sensitive Contexts

Where a product may involve children, learners, vulnerable users, safety reports, health-related content, identity verification, or other sensitive contexts, additional controls may be required.

These may include:

- age-appropriate design;
- guardian or institutional authority where applicable;
- stronger minimization;
- restricted sharing;
- heightened human review;
- shorter retention;
- specialist policy review; and
- clearer escalation and support.

This public paper does not establish that every FUZE product is intended for children or another regulated audience.

Product-specific notices and access rules must control the actual implementation.

## Status and Evidence

This paper defines a public policy and design direction.

It does not independently prove that every product has implemented:

- all classifications;
- every permission control;
- deletion automation;
- provider isolation;
- geographic restrictions;
- encryption configuration;
- formal privacy certification;
- security certification;
- incident exercises; or
- live user controls.

Stronger status evidence may include:

- implemented access controls;
- tested role separation;
- data maps;
- provider configuration;
- retention schedules;
- deletion and export tests;
- incident procedures;
- audit records;
- product notices;
- monitoring; and
- operating evidence.

Current product and platform status should be checked in the [FUZE Public Status and Roadmap Matrix](../PUBLIC-INDEX/02-FUZE_PUBLIC_STATUS_AND_ROADMAP_MATRIX.md).

## Public Boundary

This paper describes FUZE's platform direction. It is not:

- a universal privacy notice;
- a universal consent form;
- a statement that every product uses the same data;
- a statement that every product uses the same provider;
- a promise of one retention period;
- a legal conclusion for every jurisdiction;
- a certification of compliance;
- a security guarantee; or
- proof that every described control is implemented or live.

Product notices, agreements, interfaces, provider disclosures, and operating procedures should describe the actual implementation.

Security, privacy, and governance controls reduce exposure but cannot eliminate every human, software, provider, integration, account, model, data-quality, or adversarial risk.

Public transparency does not require disclosure of:

- personal identity;
- customer content;
- private prompts;
- partner or investor terms;
- private financial records;
- tax or accounting records;
- wallet-to-person mappings;
- credentials;
- private keys;
- signer identities;
- restricted infrastructure;
- exploitable vulnerabilities; or
- detailed incident-response procedures.

Consolidated limitations appear in the [FUZE Risk and Disclosure Appendix](../WHITEPAPER-PAPERS/05-FUZE_RISK_AND_DISCLOSURE_APPENDIX_PUBLIC.md).

## Key Takeaways

- FUZE data handling begins with a defined product purpose.
- Classification determines access, AI use, storage, reporting, retention, and deletion treatment.
- Possession of data does not authorize every use.
- AI tasks should use bounded context, approved providers and tools, and review appropriate to impact.
- AI outputs inherit sensitivity from their sources until reviewed and reclassified.
- Product, workspace, customer, financial, wallet-public, and wallet-private records remain distinct.
- Public wallet evidence can support transparency without exposing personal identity.
- Public reports should use reviewed, purpose-appropriate, and de-identified information.
- Logging and incidents should preserve accountability without creating uncontrolled copies of sensitive data.
- Product-specific notices and evidence must describe the actual implementation.
