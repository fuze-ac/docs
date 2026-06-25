# FUZE Core Platform Rails

## Executive Summary

FUZE Core Platform Rails are reusable, governed services that products may integrate instead of rebuilding common capabilities independently.

The rails cover:

- identity and access;
- product usage and Platform Credits;
- payment and settlement;
- AI orchestration;
- data and permission controls;
- wallet-aware records;
- reporting and evidence; and
- governance and platform operations.

A rail is more than shared code. It has an accountable owner, a defined service boundary, authoritative records, access rules, monitoring, versioning, failure behavior, reconciliation, correction paths, and support expectations.

Products remain responsible for their own user experience, domain logic, product status, and product-specific risks. The rail supplies a consistent shared capability only where a proven product need justifies that dependency.

This paper defines the public rail model and integration expectations. It does not prescribe a specific vendor, network, model provider, database, wallet, payment processor, or smart-contract deployment. It also does not establish that every described rail is implemented or live.

## Purpose of This Paper

This paper explains:

- what qualifies as a platform rail;
- which service domains belong in the rail catalogue;
- what each rail owns;
- how products should integrate with a rail;
- how records, permissions, reconciliation, and corrections should work;
- how reliability, incidents, and version changes should be handled;
- when a capability should remain product-specific;
- how Platform Credits, stablecoins, wallets, and FUZE token remain distinct; and
- what evidence is required before stronger public status claims are made.

The [FUZE Platform Overview](./01-FUZE_PLATFORM_OVERVIEW_PUBLIC.md) explains the wider platform model. The [FUZE Product-First Execution Model](./03-FUZE_PRODUCT_FIRST_EXECUTION_MODEL_PUBLIC.md) explains when repeated product needs should become shared infrastructure.

## What Qualifies as a Rail

A capability becomes a platform rail when one governed service boundary can support multiple credible workflows or one critical control that several products should not implement inconsistently.

A rail should define:

- the request, command, or event it accepts;
- the decision, result, or state it returns;
- the authoritative record it owns;
- the products, operators, and service roles allowed to use it;
- its availability and response expectations;
- its security and privacy controls;
- monitoring, reconciliation, correction, and incident behavior;
- versioning and migration rules;
- failure and fallback behavior;
- support ownership; and
- evidence supporting its current status.

This prevents the platform from becoming a loosely connected set of utilities without clear authority.

A product team should know which system owns:

- account or role status;
- Platform Credit balance;
- payment classification;
- AI task state;
- permission decision;
- wallet reference;
- report version;
- configuration approval; and
- incident status.

A shared helper does not automatically qualify as a rail. The capability should remain product-specific when centralization would add complexity, weaken domain behavior, increase risk, or lack a credible reuse case.

## Rail Design Principles

| Principle | Public meaning |
|---|---|
| Product need first | A rail exists to support proven product workflows or required common controls |
| Clear authority | One service owns each authoritative record or decision |
| Least privilege | Products and operators receive only the access required for the task |
| Idempotent state change | Retries must not duplicate credits, payments, claims, or other state changes |
| Evidence by default | Important decisions and state transitions create reviewable records |
| Failure is explicit | Delayed, degraded, denied, failed, and corrected states remain distinguishable |
| Versioned change | Interfaces, policies, and schemas change through controlled versions |
| Privacy by purpose | Data use follows the approved purpose, authority, and minimum necessary scope |
| Human authority | Sensitive AI, finance, market, identity, safety, and governance actions retain required human control |
| Public-safe reporting | Transparency exposes the evidence needed for the claim without exposing protected information |
| Status discipline | Design documentation does not imply implementation, deployment, activation, or live availability |

## Rail Catalogue

| Rail | Authoritative responsibility | Typical product interaction | Main boundary |
|---|---|---|---|
| Identity and Access | Accounts, organizations, workspaces, roles, sessions, and access decisions | Authenticate an actor and authorize an action | A wallet address alone does not establish private authority |
| Product Usage and Platform Credits | Defined usage events, balances, reservations, consumption, reversals, and corrections | Quote, reserve, consume, reverse, or display usage | Platform Credits remain separate from FUZE token |
| Payment and Settlement | Payment intent, route, status, classification, reconciliation, refund, and exception references | Initiate or check a supported commercial transaction | Payment capability does not itself prove revenue |
| AI Orchestration | Approved task, context policy, model route, execution state, validation, and review metadata | Submit a governed AI task and receive a reviewable result | AI output does not replace required human judgment |
| Data and Permission | Data classification, authority, consent, use policy, retention, correction, and deletion state | Check whether data may be collected, used, shared, retained, or removed | Possession of data does not authorize every use |
| Wallet-Aware Records | Address, network, transaction, vault, snapshot, eligibility, claim, and public-safe status references | Associate a wallet record with an approved product or ecosystem action | Wallet transparency must not expose personal identity |
| Reporting and Evidence | Metric definitions, source ownership, report versions, evidence references, corrections, and publication state | Produce internal, permissioned, investor, partner, community, or public-safe reports | A dashboard is not automatically the authoritative source |
| Governance and Operations | Configuration approvals, releases, exceptions, incidents, service ownership, and controlled changes | Request, approve, execute, delay, reject, or roll back a platform change | Sensitive changes require impact-appropriate approval |

FUZE token utility may call relevant rails where a defined mechanism requires them. FUZE token is not a general-purpose replacement for identity, product usage, payment, data, or reporting services.

## Identity and Access Rail

The Identity and Access Rail answers:

1. who or what is requesting an action;
2. which organization, workspace, product, device, or service context applies;
3. which role or policy governs the request; and
4. whether the requested action is allowed.

### Identity Contexts

The rail may support:

- individual accounts;
- shop or SME accounts;
- teams and organizations;
- product workspaces;
- partners and contributors;
- service accounts;
- devices and terminals;
- sessions and recovery events; and
- optional wallet association where a defined workflow requires it.

### Authorization Request

A product may send:

- actor reference;
- workspace or organization;
- product and requested action;
- resource or record scope;
- device or session context;
- risk or sensitivity indicator; and
- relevant policy version.

The rail returns:

- allowed, denied, or additional-review-required status;
- the controlling role or policy reference;
- scope and expiry where relevant; and
- a decision record suitable for audit.

### Identity Boundaries

Products should not infer staff authority, customer permissions, partner authority, administrative rights, eligibility, or verified identity from a public wallet address alone.

A wallet may provide an address-based context. Private verification, customer identity, employment role, account recovery, signer authority, and administrative permissions remain governed by their appropriate systems.

### Failure Behavior

When identity services are unavailable:

- privileged, financial, destructive, or security-sensitive actions should fail closed;
- low-risk read-only or offline functionality may continue only under an approved cached policy;
- products should explain the temporary limitation without exposing sensitive policy details; and
- deferred actions should be revalidated before execution.

## Product Usage and Platform Credits Rail

The Product Usage and Platform Credits Rail records supported product consumption.

It may support:

- usage quotations;
- reservations;
- completed consumption;
- reversals;
- corrections;
- promotional grants;
- expiry rules;
- balance presentation; and
- usage history.

### Authoritative Usage Event

| Field | Purpose |
|---|---|
| Product and action | Identifies the service requested |
| Actor, organization, or workspace | Identifies the permitted consuming context |
| Quantity and unit | Defines measurable usage |
| Credit rule or pricing version | Preserves how the action was evaluated |
| Reservation reference | Links authorization to later completion or release |
| Idempotency reference | Prevents duplicate consumption during retries |
| Outcome | Records completion, failure, cancellation, reversal, or correction |
| Timestamp and source | Supports reconciliation and investigation |
| Related product result | Connects consumption to the delivered output where appropriate |

### Consumption Lifecycle

A common flow is:

`quote -> reserve -> perform action -> confirm consumption -> display result and balance`

Where the action fails before the product's defined completion condition, the rail should release or reverse the reservation according to the governing rule.

### Credit Boundaries

Platform Credits apply to supported product actions.

They are not:

- FUZE token;
- a transferable investment asset;
- a wallet-based participation right;
- a guaranteed refund right outside the product terms; or
- proof of product revenue.

Each product should clearly state:

- what consumes credits;
- how much is consumed;
- when consumption becomes final;
- what happens on failure;
- whether expiry or promotional conditions apply; and
- how corrections are handled.

### Failure Behavior

If the rail cannot confirm balance, reservation, or final consumption, the product should not silently create an unrecorded billable action.

An approved grace, offline, or retry policy may be used only when eventual reconciliation is guaranteed and the user-facing behavior remains clear.

See [FUZE Platform Credits Usage Examples](./06-FUZE_PLATFORM_CREDITS_USAGE_EXAMPLES_PUBLIC.md).

## Payment and Settlement Rail

The Payment and Settlement Rail coordinates supported commercial or operational movement of value without assuming one route for every product, country, partner, or participant.

### Responsibilities

The rail may:

- create a payment or settlement intent;
- select an approved route;
- preserve provider, bank, processor, network, or wallet references;
- track pending, completed, failed, expired, refunded, disputed, reversed, or corrected states;
- prevent duplicate fulfillment;
- classify funds by operational purpose;
- connect transactions to invoices, orders, partner records, treasury records, or compensation records; and
- produce reconciliation and exception records.

### Value Classification

A transaction should identify its actual purpose, such as:

- product payment;
- subscription or usage payment;
- settlement;
- refund;
- treasury movement;
- partner payment;
- contributor compensation; or
- another approved operational category.

Stablecoins may be used within approved payment, settlement, treasury, or compensation workflows.

Stablecoin records remain separate from:

- Platform Credit balances;
- FUZE token utility;
- wallet-based participation;
- token rewards; and
- public payout promises.

### External-State Handling

External processors, banks, wallets, marketplaces, or networks may return delayed, conflicting, duplicated, or reversed states.

The rail should:

- preserve the external reference;
- maintain one authoritative internal state;
- avoid duplicate fulfillment;
- show pending rather than final status while confirmation is incomplete;
- support manual review for exceptions; and
- record corrections without erasing the prior state.

### Revenue Boundary

A payment intent, deposit, transfer, or successful processor event does not independently prove reconciled revenue.

Revenue claims require the commercial or accounting evidence that connects payment to delivered product or service under the applicable recognition process.

## AI Orchestration Rail

The AI Orchestration Rail gives products a controlled way to request generation, analysis, interpretation, moderation assistance, summarization, classification, transformation, or another approved model task.

### AI Task Definition

An AI task may include:

- product and task class;
- actor and permission context;
- authorized input and source references;
- data classification and retention policy;
- model or provider policy;
- tool access;
- cost or usage limit;
- output format;
- validation rules;
- human-review requirement;
- confidence or quality controls;
- safety and escalation rules; and
- fallback behavior.

### Rail Result

The rail may return:

- queued, running, completed, failed, blocked, or review-required status;
- output or error;
- route and model metadata appropriate for operations;
- usage and cost record;
- validation results;
- safety or policy flags; and
- review state.

The product remains responsible for deciding:

- how the output is presented;
- whether it may trigger another action;
- whether a human must approve it;
- how the user corrects it; and
- how the result is stored or reported.

### AI Boundaries

Sensitive prompts, customer records, identity data, credentials, private partner material, regulated data, or restricted business information require the corresponding permission, provider, retention, and review controls.

Market, legal, financial, safety, identity, moderation, and high-impact operational outputs should not bypass required human review.

QTB outputs remain market research and decision support. AIMM outputs remain authorized liquidity-operations intelligence and reporting. Botmad actions remain permission-controlled and subject to human authority.

### Fallback Behavior

Fallback may:

- route to another approved model;
- reduce functionality;
- queue the task;
- return a partial result clearly labeled as such; or
- ask the user to retry.

Fallback must not silently weaken privacy, data handling, quality, permission, or review requirements.

## Data and Permission Rail

The Data and Permission Rail applies policy to information as it moves through products and shared services.

### Policy Areas

It may maintain:

- data categories and sensitivity labels;
- collection purpose;
- legal or operational authority;
- consent where applicable;
- workspace, user, partner, and service access rules;
- AI-use permissions;
- sharing restrictions;
- geographic or contractual restrictions;
- retention and deletion schedules;
- export and correction rights;
- audit events; and
- public/private classification.

### Purpose-Based Permission

Permission is evaluated for the requested use, not merely for possession of the data.

For example, information collected to complete a shop order should not automatically become:

- AI training material;
- public reporting content;
- partner data;
- marketing data;
- token eligibility evidence; or
- unrestricted cross-product context.

### Data Minimization

Products should:

- transfer only the fields required for the task;
- prefer references over full records where possible;
- separate operational logs from public reports;
- redact or aggregate where appropriate;
- limit retention to the defined need; and
- preserve correction and deletion behavior where required.

Logs, support records, prompts, model outputs, exports, and reports each require their own access and retention treatment.

The [FUZE Data Privacy and AI Data Handling](./07-FUZE_DATA_PRIVACY_AND_AI_DATA_HANDLING_PUBLIC.md) provides the deeper public policy.

## Wallet-Aware Record Rail

The Wallet-Aware Record Rail supports address-based records when a product or ecosystem mechanism has a defined reason to use them.

### Possible Records

The rail may support:

- supported network and wallet-address references;
- transaction references;
- contract references;
- product-connected access status;
- token-holding references;
- snapshot or vault references;
- eligibility status;
- claim status;
- governance references;
- correction state; and
- public report references.

### Record Validation

Wallet-related records should validate:

- network;
- address format;
- contract or asset reference where relevant;
- transaction status;
- confirmation requirements;
- custody context where required;
- snapshot or reporting period; and
- source and correction history.

Unsupported networks, malformed addresses, conflicting custody records, incomplete confirmations, or mismatched contracts should create explicit exceptions rather than assumed matches.

### Public and Private Separation

Public-safe systems may show:

- wallet address;
- network;
- transaction or vault reference;
- status;
- report period; and
- correction state.

They should not publish personal names, contact details, identity documents, customer history, tax records, private custody evidence, or wallet-to-person mappings unless specifically authorized.

### Participation Boundary

The rail defines shared record capability only.

Detailed token-related eligibility, approved distributable value, claims, custody, activation, and participation rules belong in the dedicated wallet and tokenomics papers.

A wallet record does not by itself establish eligibility, payment, income, yield, distribution, or investment rights.

See [FUZE Wallet-Based Platform Model](./08-FUZE_WALLET_BASED_PLATFORM_MODEL_PUBLIC.md).

## Reporting and Evidence Rail

The Reporting and Evidence Rail converts governed source events into reviewable information.

### Responsibilities

It may manage:

- metric definitions;
- source ownership;
- source periods;
- aggregation rules;
- privacy and redaction rules;
- reporting frequency;
- draft, reviewed, published, superseded, and corrected states;
- source references or hashes;
- approval records; and
- audience-specific access.

### Report Audiences

Reports may be:

- internal operational reports;
- partner reports;
- qualified investor reports;
- governance reports;
- community reports; or
- public-safe reports.

The same source event may support different reports with different access and aggregation rules.

### Evidence Discipline

A public metric should be traceable to:

- a definition;
- a source owner;
- a period;
- a calculation or aggregation rule;
- a review state; and
- a correction history where applicable.

Reports should distinguish:

- observed results;
- targets;
- examples;
- projections;
- estimates;
- roadmap direction; and
- unverified claims.

A dashboard is a presentation surface. It is not automatically the authoritative source unless the reporting model explicitly assigns that role.

Corrections should preserve:

- the earlier version;
- the reason for correction;
- reviewer or approving function;
- effective replacement; and
- publication state.

See [FUZE Transparency and Reporting Rails](./09-FUZE_TRANSPARENCY_AND_REPORTING_RAILS_PUBLIC.md).

## Governance and Operations Rail

Shared services require controlled change because one change can affect several products, users, records, or mechanisms.

### Governance Scope

The rail may cover:

- service ownership;
- configuration and policy approval;
- release review;
- staged rollout;
- rollback;
- access exceptions;
- incident declaration and response;
- vendor and dependency review;
- schema and interface versioning;
- data migrations;
- service deprecation;
- security review;
- privacy review;
- finance review;
- legal or compliance review where required; and
- public-status changes.

### Approval by Impact

Low-risk operational changes may use delegated authority.

Sensitive changes involving:

- funds;
- Platform Credit balances;
- permissions;
- customer data;
- wallet logic;
- token utility;
- contracts;
- eligibility;
- claims;
- public status;
- disclosures; or
- market access

require approvals appropriate to their impact.

### Operational Visibility

Each rail should have:

- accountable owner;
- support and escalation route;
- health indicators;
- dependency status;
- current version;
- known limitation handling;
- incident process; and
- change history.

Public materials may summarize this model without exposing restricted infrastructure, credentials, vulnerabilities, signer identities, or exploitable operational details.

## Authoritative Record Model

A shared platform depends on clear record authority.

| Record | Authoritative rail or function |
|---|---|
| Account and role status | Identity and Access |
| Platform Credit balance and consumption | Product Usage and Platform Credits |
| Payment or settlement state | Payment and Settlement |
| AI task execution and review metadata | AI Orchestration |
| Data-use permission and retention state | Data and Permission |
| Wallet, network, transaction, vault, or snapshot reference | Wallet-Aware Records |
| Report version and publication state | Reporting and Evidence |
| Configuration approval, incident, and release state | Governance and Operations |

A product may cache or present these records, but it should not create a conflicting source of truth.

Where eventual consistency is necessary, the interface should expose:

- pending state;
- last confirmed version;
- source timestamp;
- reconciliation status; and
- correction path.

## Integration Pattern

A product integration follows a controlled lifecycle.

### 1. Define the Workflow

Identify the user action, product outcome, and reason the rail is required.

### 2. Define the Service Contract

Agree on:

- request;
- response;
- authoritative record;
- permissions;
- data fields;
- error states;
- timeout and retry behavior;
- idempotency; and
- version.

### 3. Map Controls

Map:

- roles;
- data sensitivity;
- AI review;
- payment or credit rules;
- wallet context;
- evidence requirements;
- support ownership; and
- escalation.

### 4. Test Normal and Failure Paths

Test:

- successful request;
- duplicate request;
- denied request;
- invalid input;
- delayed dependency;
- unavailable service;
- partial completion;
- reversal or correction;
- stale version; and
- reconciliation mismatch.

### 5. Establish Operations

Define:

- monitoring;
- alerts;
- support;
- incident ownership;
- reconciliation;
- rollback;
- status communication; and
- service review.

### 6. Release to Approved Scope

Release according to the product's current stage, permissions, support capacity, and evidence.

### 7. Review and Migrate Deliberately

Review service quality and migrate versions through controlled change rather than silent interface drift.

The product should retain enough local context to explain the user experience. The rail remains authoritative for its domain record.

## Practical Integration Examples

### AI-Assisted Shop Report

ShopOS AI may:

1. confirm the operator's workspace and report permission through Identity and Access;
2. request approved shop records under the Data and Permission policy;
3. submit a bounded task to AI Orchestration;
4. reserve and confirm applicable Platform Credit consumption;
5. allow operator review and correction;
6. store the approved result; and
7. make the completed report available through the product's reporting history.

If the model request fails:

- the product preserves the input state;
- the task may be retried or completed manually;
- completed-action consumption should not be finalized unless the usage rule's completion condition is met; and
- the failure creates an operational record.

Token or wallet logic is unnecessary unless a separate defined ecosystem function requires it.

### Community Moderation Assistance

CommunityLayer AI may:

1. verify the moderator role;
2. retrieve only the permitted report and conversation context;
3. submit a summarization or triage task;
4. return the output as a reviewable recommendation;
5. preserve human moderator authority; and
6. record the decision and correction history.

The AI rail should not autonomously impose a high-impact moderation action unless the approved product policy explicitly permits it.

### QTB Research Task

QTB may:

1. verify analyst access;
2. retrieve approved market sources;
3. submit a structured interpretation task;
4. preserve source references and confidence limits;
5. require analyst review; and
6. produce a report record.

The rail should support research traceability rather than imply autonomous trading or assured financial performance.

### AIMM Monitoring Task

AIMM may:

1. verify authorized operator access;
2. retrieve approved venue or market-operation data;
3. evaluate defined monitoring conditions;
4. record alerts, observations, and operator decisions; and
5. publish the appropriate internal or public-safe report.

The workflow should not imply price control, guaranteed spread, guaranteed depth, guaranteed liquidity, or venue control.

## Reliability and Failure Model

Rails should expose clear operational states.

| State | Product response |
|---|---|
| Healthy | Process normally and record the authoritative result |
| Degraded | Limit affected functionality and communicate the constraint |
| Delayed | Show pending state and reconcile asynchronously |
| Denied | Explain the applicable access or policy decision where safe |
| Failed | Preserve the request reference, avoid duplicate side effects, and offer recovery |
| Review required | Pause final action until the authorized reviewer decides |
| Reversed | Restore or adjust state according to the authoritative reversal record |
| Corrected | Link the replacement record and retain the audit trail |
| Version unsupported | Prevent unsafe execution and route the product to migration or fallback |

### Reliability Controls

State-changing operations should support:

- idempotency;
- correlation identifiers;
- durable request references;
- timeout behavior;
- retry limits;
- duplicate detection;
- reconciliation;
- rollback or compensation where appropriate; and
- audit history.

Monitoring should detect:

- elevated failure rates;
- stale or missing records;
- reconciliation gaps;
- unusual permission denials;
- model cost spikes;
- payment exceptions;
- duplicate events;
- report delays;
- version mismatches; and
- dependency outages.

No shared rail removes the need for product-level quality, support, and user communication. It provides a consistent place to operate the common dependency.

## Versioning and Migration

Rails should use explicit version control for:

- interfaces;
- schemas;
- policies;
- pricing or credit rules;
- model-routing policies;
- permission rules;
- metric definitions; and
- public-report formats.

A version change should identify:

- reason;
- affected products;
- compatibility;
- migration path;
- rollout scope;
- fallback;
- owner;
- effective date where approved; and
- evidence required for completion.

Breaking changes should not be introduced silently.

A retired version should remain traceable for historical records and corrections where appropriate.

## Rail Status and Evidence

This paper describes the intended service architecture and operating model.

A rail may progress through:

- concept;
- design;
- prototype;
- internal testing;
- limited release;
- public beta where applicable;
- live operation;
- under review;
- paused; or
- retired.

Evidence should match the status.

| Status claim | Evidence direction |
|---|---|
| Designed | Defined service boundary, records, permissions, and failure model |
| Prototype | Reviewable bounded implementation |
| Internal testing | Test records for normal and failure behavior |
| Limited release | Approved product integration, monitoring, support, and access scope |
| Live | Production integration, service ownership, current terms, support, monitoring, and operating evidence |
| Reliable | Measured service behavior over a defined period and scope |
| Reconciled | Completed reconciliation records and resolved exceptions |

A document, interface diagram, or code repository does not independently prove deployment, adoption, reliability, security, or live service.

Current public status should be checked in the [FUZE Public Status and Roadmap Matrix](../PUBLIC-INDEX/02-FUZE_PUBLIC_STATUS_AND_ROADMAP_MATRIX.md).

## Security and Privacy Boundary

Public rail documentation may explain service responsibilities and controls.

It should not expose:

- credentials;
- API keys;
- private keys;
- seed phrases;
- signer identities;
- restricted endpoints;
- exploitable vulnerabilities;
- detailed incident-response secrets;
- private customer or partner data;
- internal security topology; or
- sensitive treasury procedures.

Public wallet, transaction, report, or contract references may be included only when verified, approved, relevant, and linked to the correct status.

Public transparency should reveal enough evidence for the claim without creating a public identity directory or operational attack surface.

## Public Boundary

This paper describes a service architecture direction. It does not confirm that every rail, integration, vendor route, network, wallet function, token mechanism, contract, payment route, or reporting surface is deployed or active.

Platform services may experience downtime, integration errors, incorrect records, security incidents, external-provider failures, delayed reconciliation, model failures, and version conflicts.

Platform Credits remain separate from FUZE token. Stablecoins remain operational rails. Wallet records do not automatically create participation rights. FUZE token utility requires its own defined mechanism, implementation, controls, activation status, and evidence.

A payment route does not prove revenue. A deployed contract does not prove activation. A dashboard does not prove the accuracy or authority of the underlying source. Shared architecture does not prove that every product uses every rail.

The [FUZE Technical Architecture Public](../WHITEPAPER-PAPERS/03-FUZE_TECHNICAL_ARCHITECTURE_PUBLIC.md) provides the broader system view. The [FUZE Risk and Disclosure Appendix](../WHITEPAPER-PAPERS/05-FUZE_RISK_AND_DISCLOSURE_APPENDIX_PUBLIC.md) provides consolidated limitations.

## Key Takeaways

- FUZE Core Platform Rails turn repeated product needs into governed shared services.
- A rail has an owner, service boundary, authoritative record, permissions, monitoring, versioning, reconciliation, and failure behavior.
- Products retain responsibility for their user experience and domain logic.
- Platform Credits, stablecoins, wallet records, and FUZE token have separate roles.
- Sensitive AI, financial, market, identity, wallet, and governance actions retain required human and specialist review.
- State-changing actions require idempotency, reconciliation, correction, and auditability.
- Public transparency should expose the evidence needed for the claim without exposing protected identity or security-sensitive information.
- Rail status must advance only when implementation and operating evidence support the stronger claim.
- Products should adopt only the rails they genuinely need and only when the dependency is operationally justified.