# FUZE Core Platform Rails

## Executive Summary

FUZE Core Platform Rails are reusable services that products can integrate instead of implementing common functions independently. They cover access, product usage, payments, AI orchestration, data permissions, wallet-aware records, reporting, and operational governance.

A rail is more than shared code. It has an owner, an interface, authoritative records, access rules, monitoring, and defined behavior when a dependency fails. Products remain responsible for their user experience and domain logic while the rail supplies a consistent platform capability.

This paper defines the public service model and integration expectations. It does not prescribe a specific vendor, network, database, model provider, or contract deployment.

---

## 1. What Qualifies as a Rail

A capability becomes a platform rail when multiple credible workflows benefit from one governed service boundary.

Each rail should define:

- the request or event it accepts;
- the decision or result it returns;
- the record for which it is authoritative;
- the product and operator roles allowed to use it;
- its availability and response expectations;
- monitoring, reconciliation, correction, and incident behavior;
- versioning and migration rules.

This prevents the platform from becoming a loosely connected set of helpers. A product team should know which system owns an account status, credit balance, payment classification, AI task record, permission decision, wallet reference, or published report version.

---

## 2. Rail Catalogue

| Rail | Authoritative responsibility | Typical product interaction |
|---|---|---|
| Identity and Access | Accounts, workspaces, roles, sessions, and access decisions | Authenticate a user and authorize an action |
| Product Usage and Credits | Defined usage events, Platform Credit balances, consumption, and corrections | Quote, reserve, consume, reverse, or display usage |
| Payment and Settlement | Payment intent, route, status, classification, and reconciliation reference | Initiate or check a supported commercial transaction |
| AI Orchestration | Approved task, context policy, model route, execution status, and review metadata | Submit an AI task and receive a governed result |
| Data and Permission | Data classification, consent or authority, access policy, retention, and deletion state | Check whether data can be collected, used, shared, or removed |
| Wallet-Aware Records | Address references, supported network context, transaction evidence, and public-safe status | Associate a wallet record with an approved product or ecosystem action |
| Reporting and Evidence | Metric definitions, report versions, source references, corrections, and publication state | Produce an internal, qualified, or public-safe report |
| Governance and Operations | Configuration approval, release control, exceptions, incidents, and service ownership | Request or execute a controlled platform change |

Token utility can call relevant rails where a defined mechanism requires them. The token itself is not a general-purpose replacement for identity, product usage, payment, or reporting services.

---

## 3. Identity and Access Rail

The identity rail answers who or what is requesting an action and whether the action is allowed in the current context.

Its model can include:

- individual, team, organization, partner, contributor, and service accounts;
- product workspaces and memberships;
- roles and scoped permissions;
- session and device context;
- account recovery and security events;
- optional wallet association where a workflow supports it.

A product sends the actor, workspace, requested action, and relevant context. The rail returns an access decision and the policy or role reference that supports it.

Products should not infer sensitive authority from a public wallet address alone. A wallet may provide an address-based context, while staff roles, customer permissions, private verification, and administrative authority remain governed by their appropriate systems.

When identity services are unavailable, products should fail closed for privileged or destructive actions. Limited low-risk functionality may continue only where an approved offline or cached policy permits it.

---

## 4. Product Usage and Platform Credits Rail

The usage rail records defined product consumption. It can support usage quotes, reservations, completed consumption, reversals, corrections, bonuses, expiry rules, and balance presentation.

A reliable usage event identifies:

| Field | Purpose |
|---|---|
| Product and action | States what service was requested |
| Actor or workspace | Identifies the permitted consuming context |
| Quantity and unit | Defines the measurable usage |
| Credit or pricing rule version | Preserves how the action was evaluated |
| Idempotency reference | Prevents duplicate consumption during retries |
| Outcome | Records completion, failure, cancellation, or correction |
| Timestamp and source | Supports reconciliation and investigation |

Platform Credits apply to supported product actions. The rail should make balances and consumption understandable to the user and maintain separation from FUZE token records.

If the usage rail cannot confirm a balance or reservation, the product should avoid silently delivering an unrecorded billable action. A product may use an approved grace or retry policy, but the eventual result must reconcile to one authoritative record.

See [FUZE Platform Credits Usage Examples](06-FUZE_PLATFORM_CREDITS_USAGE_EXAMPLES_PUBLIC.md) for product-facing scenarios.

---

## 5. Payment and Settlement Rail

The payment rail coordinates supported commercial movement without assuming one route for every product or region.

Its responsibilities include:

- creating a payment or settlement intent;
- selecting an approved route;
- recording provider, network, or processor references;
- tracking pending, completed, failed, refunded, disputed, or corrected states;
- classifying funds for product, treasury, settlement, or compensation purposes;
- connecting the transaction to reconciliation records.

Stablecoins may be used within payment, settlement, treasury, or compensation operations. Their records should identify the actual purpose and remain distinct from Platform Credit balances and FUZE token utility.

External processors, networks, wallets, marketplaces, and banks can introduce delayed or conflicting states. The rail should preserve the external reference, avoid duplicate fulfillment, and expose a review path for exceptions. A user-facing product should show a pending state instead of treating an unconfirmed event as final.

---

## 6. AI Orchestration Rail

The AI rail gives products a controlled way to request generation, analysis, interpretation, moderation assistance, summarization, or other approved model tasks.

An AI task can include:

- product and task class;
- authorized input and context references;
- data sensitivity and retention policy;
- model or provider policy;
- cost or usage limit;
- output format and validation;
- human-review requirement;
- safety, quality, and escalation rules.

The rail returns the task status, output or error, model-route metadata appropriate for operations, usage record, and review state. Product teams remain responsible for deciding how the result is presented and what human action follows.

Sensitive prompts, customer records, credentials, private partner material, or regulated data require the corresponding permission and provider controls. Market, legal, financial, safety, identity, and high-impact operational outputs should not bypass required human review.

Fallback behavior may route to another approved model, reduce functionality, queue the task, or ask the user to retry. It should not change data handling or quality claims without notice.

---

## 7. Data and Permission Rail

The data rail applies policy to information as it moves through products and shared services.

It can maintain:

- data categories and sensitivity labels;
- collection purpose and authority;
- workspace, user, and partner access rules;
- AI-use permissions;
- geographic or contractual restrictions where applicable;
- retention and deletion schedules;
- export, correction, and audit events.

Permission is evaluated for the requested use, not merely for possession of the data. Information collected to complete a shop order, for example, should not automatically become AI training context, public reporting material, or partner data.

Products should minimize transferred data and prefer references or scoped fields over complete records. Logs and reports need their own redaction and retention treatment.

The [FUZE Data Privacy and AI Data Handling](07-FUZE_DATA_PRIVACY_AND_AI_DATA_HANDLING_PUBLIC.md) paper provides the deeper public policy.

---

## 8. Wallet-Aware Record Rail

The wallet rail supports address-based records when a product or ecosystem mechanism has a defined reason to use them.

Possible records include:

- supported network and wallet address references;
- transaction or contract references;
- product-connected access status;
- snapshots or vault references for an approved mechanism;
- public report links and correction states;
- eligibility or claim status where an activated framework requires them.

The rail should separate public-safe evidence from private verification. Public systems may show an address and status without publishing the person's name, contact data, documents, customer history, or other sensitive records.

Network, contract, and transaction references require validation. Unsupported networks, malformed addresses, conflicting custody records, or incomplete confirmations should produce an explicit exception rather than an assumed match.

Detailed token-related eligibility and participation mechanics belong in the dedicated wallet papers. This rail only defines the shared record capability.

---

## 9. Reporting and Evidence Rail

The reporting rail converts governed source events into reviewable information.

It manages:

- metric definitions and source ownership;
- aggregation and privacy rules;
- reporting periods;
- draft, reviewed, published, superseded, and corrected versions;
- source references or hashes where useful;
- access levels for internal, partner, investor, community, or public reports.

A public metric should be traceable to a definition and source period. Corrections should preserve the earlier version, reason, reviewer, and effective replacement where appropriate.

Reporting should distinguish observed results from targets, examples, projections, and roadmap direction. A dashboard is a presentation surface; it is not the authoritative source unless the reporting model explicitly makes it one.

See [FUZE Transparency and Reporting Rails](09-FUZE_TRANSPARENCY_AND_REPORTING_RAILS_PUBLIC.md).

---

## 10. Governance and Operations Rail

Shared services require controlled change because one modification can affect several products.

The governance rail can cover:

- service ownership and escalation;
- configuration and policy approval;
- release review and rollback;
- access exceptions;
- incident declaration and response;
- dependency and vendor review;
- schema or interface versioning;
- security, privacy, finance, and legal sign-off where required.

Low-risk operational changes may use delegated authority. Sensitive changes involving funds, permissions, public status, wallet logic, contracts, or disclosures need the approvals appropriate to their impact.

Every rail should publish an operational contact, health indicators, known dependency status, and a process for product teams to report issues.

---

## 11. Integration Pattern

A product integration follows a controlled lifecycle:

1. Define the workflow and identify the rail dependency.
2. Agree on request, response, record ownership, and error states.
3. Map roles, permissions, data, and reporting requirements.
4. Test normal, duplicate, delayed, denied, and failed requests.
5. Establish monitoring, reconciliation, support, and incident ownership.
6. Release to an approved scope.
7. Review service quality and migrate versions deliberately.

The product should retain enough local context to explain the user experience, while the rail remains authoritative for its domain record.

### Example: AI-Assisted Shop Report

ShopOS AI confirms the operator's workspace and report permission through identity services. It requests approved shop data under the data policy, sends a bounded task to AI orchestration, records any supported credit consumption, and stores the reviewed result. Reporting services can then include the completed report in the appropriate history.

If the model request fails, the product preserves the input state and provides retry or manual completion. It should not consume a completed-action charge until the usage policy's completion condition is met.

---

## 12. Reliability and Failure Model

Rails should expose clear health and failure states:

| State | Product response |
|---|---|
| Healthy | Process normally and record the authoritative result |
| Degraded | Limit affected functionality and communicate the constraint |
| Delayed | Show pending status and reconcile asynchronously |
| Denied | Explain the applicable access or policy decision where safe |
| Failed | Preserve the request reference, avoid duplicate side effects, and offer recovery |
| Corrected | Link the replacement record and retain an audit trail |

Retries require idempotency for credit, payment, wallet, and other state-changing actions. Monitoring should detect unusual failure rates, reconciliation gaps, permission denials, model cost spikes, and stale reports.

No shared rail removes the need for product-level quality and support. It provides a consistent place to operate the common dependency.

---

## 13. Public Boundary

This paper describes a service architecture direction. It does not confirm that every rail, integration, vendor route, network, wallet function, token mechanism, or reporting surface is deployed or active.

Platform services can experience downtime, integration errors, incorrect records, security incidents, external-provider failures, or delayed reconciliation. Sensitive identity and operational information remains permissioned even when a wallet or report reference is public.

Current status is tracked through the [FUZE Public Status and Roadmap Matrix](../PUBLIC-INDEX/02-FUZE_PUBLIC_STATUS_AND_ROADMAP_MATRIX.md). The [FUZE Technical Architecture Public](../WHITEPAPER-PAPERS/03-FUZE_TECHNICAL_ARCHITECTURE_PUBLIC.md) provides the broader system view.

---

## Conclusion

FUZE Core Platform Rails turn repeated product needs into governed services. Clear interfaces, record ownership, permissions, monitoring, and failure behavior allow products to share capabilities without losing their domain focus.

The rail model supports gradual integration: products can adopt the services they need, when evidence and operational readiness justify the dependency.
