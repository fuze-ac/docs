# FUZE Data Privacy and Permission Model

## Executive Summary

FUZE products can process business files, shop records, community content, event information, AI prompts and outputs, product-usage records, payments, Platform Credits, wallet references, and operational evidence. Privacy and permission controls determine why that data is used, who can access it, which actions are authorized, how long records remain, and what may appear in public reporting.

The model separates private product data, restricted operational evidence, public-safe reporting, and public blockchain records. A wallet address or transaction may be visible without making the person behind it public. Identity documents, customer records, private agreements, credentials, verification material, and sensitive operating evidence remain permissioned.

Access is purpose-based and role-based. Product users, workspace owners, reviewers, finance roles, partners, support staff, AI workflows, and administrators receive different authority. Sensitive actions such as publication, payment changes, data export, member sanctions, wallet eligibility decisions, permission changes, and destructive automation require explicit authorization and records.

This paper gives investors, partners, customers, and reviewers a public framework for assessing FUZE data governance. It does not replace a privacy notice, customer agreement, data-processing agreement, security policy, legal assessment, or audit.

## 1. Purpose and Primary Readers

This paper is written for investors, partners, enterprise reviewers, product owners, customers, support teams, privacy and security reviewers, and operators.

It explains:

1. which data categories FUZE products may use;
2. how records are classified;
3. how identities, workspaces, roles, resources, actions, purposes, and conditions determine access;
4. how AI workflows, support teams, and partners receive limited permissions;
5. how public blockchain records remain separate from private identity and business context;
6. how data collection, use, sharing, retention, correction, deletion, and closure are handled;
7. which evidence supports stronger privacy and permission claims;
8. which public claims remain outside this framework.

The [FUZE AI Safety and Reliability](07-FUZE_AI_SAFETY_AND_RELIABILITY_PUBLIC.md) paper governs AI evaluation, automation, and incident controls. Product-specific papers govern the exact workflow and data scope.

## 2. Current Public Position

FUZE public papers define intended privacy, workspace, permission, wallet, reporting, and access-control principles.

They do not by themselves prove:

- that a specific control is configured, tested, or operating;
- that every product uses the same data, provider, storage location, or retention period;
- that a customer, enterprise, partner, or regulator has approved a product;
- that a data-processing agreement, privacy notice, security certification, or independent audit exists;
- that every access request, deletion request, incident, or data transfer has been completed;
- that privacy, security, or human-error risk has been eliminated;
- that public blockchain transparency makes personal identity public.

Stronger status requires current evidence for the named product, workflow, environment, data set, role, provider, control, test, review period, and operating scope.

## 3. Control Objective

The objective is to use the minimum data and authority needed to deliver a defined workflow while preserving appropriate evidence, correction capability, and public transparency.

Each workflow should answer:

1. What data is involved?
2. Who controls, supplies, or originates it?
3. Why is the data needed?
4. Which users, services, AI systems, providers, or partners may access it?
5. Which actions may each role perform?
6. Where is the data stored, processed, or transmitted?
7. Which record supports review, correction, and audit?
8. How long is it retained?
9. What may be shared publicly?
10. How is access removed?
11. How is the data corrected, restricted, exported, deleted, or archived where applicable?
12. What happens when the customer, partner, user, or product closes?

These decisions should be part of product and implementation design rather than deferred until broad release.

## 4. Data Inventory

| Category | Examples | Typical sensitivity |
|---|---|---|
| Account and identity | Login, contact details, workspace membership, role | Private |
| Product content | Settings, prompts, files, templates, outputs, reports | Private or workspace-controlled |
| Business operations | Sales, stock, staff, customers, tasks, spreadsheets | Private or restricted |
| Community and event | Messages, moderation evidence, participants, sponsors, feedback | Mixed; often private |
| AI operations | Instructions, retrieved context, model output, evaluation, usage metadata | Private or restricted |
| Commercial | Offers, invoices, payments, refunds, Platform Credit activity | Restricted |
| Partner | Integration, implementation, support, campaign, and commercial records | Restricted |
| Security | Logs, credentials, alerts, incidents, vulnerabilities | Highly restricted |
| Wallet and blockchain | Addresses, transactions, contract, vault, or event references | Public at network level; context may remain private |
| Verification | Identity, eligibility, custody, jurisdiction, or professional-review evidence | Highly restricted |
| Public reporting | Approved metrics, status, hashes, summaries, and labels | Public |

Not every product uses every category. The responsible product owner should identify actual fields, systems, providers, purposes, owners, and retention requirements rather than relying only on broad labels.

## 5. Data Classification

### 5.1 Public

Material intentionally approved for public release, such as product pages, public papers, current status, public-safe metrics, wallet addresses, transaction references, report hashes, and approved labels.

### 5.2 Workspace

Records available to authorized members of a customer, team, shop, enterprise, community, event, partner deployment, or game program.

### 5.3 Restricted operational

Payment records, detailed usage, support cases, partner implementation, internal product reports, moderation evidence, market operations, and administrative logs.

### 5.4 Highly restricted

Credentials, security findings, identity documents, private verification, legal advice, tax and accounting workpapers, sensitive treasury procedures, protected personal data, and exploitable incident detail.

Classification controls access, sharing, export, retention, logging, review, and public treatment.

A public source may become sensitive when combined with private identity, customer context, location, time, role, or transaction information.

## 6. Permission Decision Model

An access decision should consider:

```text
identity + workspace + role + resource + action
+ purpose + conditions + approval state -> allow, deny, or require approval
```

### Identity

The person, service, partner, provider, or AI workflow requesting access is authenticated through a supported method.

### Workspace

The request belongs to a defined customer, product, program, or operating boundary.

### Role

The requester has assigned authority such as owner, administrator, editor, operator, reviewer, finance role, support role, partner role, viewer, or service role.

### Resource

The relevant file, data set, report, product module, workspace, payment record, wallet reference, integration, or tool is identified.

### Action

Reading, creating, editing, exporting, sharing, publishing, approving, paying, refunding, deleting, connecting, administering, and changing permissions are separate actions.

### Purpose

The action must support the approved product, support, implementation, reporting, security, or operational purpose.

### Conditions

The action may require a time limit, second approval, network, device, location, value threshold, customer consent, reviewer state, or another product rule.

Permission should default to the smallest scope that supports the task.

## 7. Workspace Roles and Separation

A workspace may represent an individual, shop, team, enterprise, community, event, partner deployment, game program, or controlled operating environment.

| Role | Typical authority |
|---|---|
| Owner | Workspace policy, billing, administrators, export, and closure |
| Administrator | Users, configuration, approved integrations, and operational reports |
| Editor or operator | Create and change product content within assigned scope |
| Reviewer | Inspect and approve selected outputs or actions |
| Finance role | View billing, credits, payments, refunds, and reconciliation records |
| Support role | Access assigned cases and diagnostic evidence |
| Partner operator | Work only within assigned customer or implementation scope |
| Viewer | Read approved records without changing state |
| AI service | Use authorized data and tools for a defined task |
| Security or audit role | Review approved logs, controls, incidents, and evidence |

Workspace separation should prevent one customer, community, partner, environment, or product program from accessing another's records.

Privileged roles require stronger authentication, logging, periodic review, and prompt removal when the role changes.

## 8. Public, Blockchain, and Private Records

Blockchain visibility is not equivalent to identity transparency.

### Public network record

A network may expose an address, amount, asset, timestamp, contract, transaction, event, or state.

### FUZE public context

FUZE may publish an approved label, purpose, status, report hash, vault category, or public-safe explanation.

### Permissioned context

The person, customer relationship, agreement, eligibility evidence, custody notes, tax information, internal approval, and support record remain in restricted systems.

Public reporting should not join these layers in a way that identifies a person without a valid purpose, authority, and approved disclosure process.

Wallet-level transparency may support review of vaults, releases, snapshots, activity, claims, or status where relevant. Detailed eligibility, custody, participation, and correction treatment remains in the dedicated wallet and token papers.

## 9. AI Access

An AI workflow receives only the sources and tools required for its task.

Controls may include:

- explicit source selection;
- workspace and folder boundaries;
- restricted-field filtering;
- retrieval limited by role and purpose;
- read-only defaults;
- tool allowlists;
- confirmation before state changes;
- output review and approval;
- prompt and result handling rules;
- retention controls;
- model and provider configuration;
- access and action records;
- stop, revoke, and recovery controls.

Examples:

- SheetLayer AI may process a selected sheet rather than every business file.
- CommunityLayer AI may review relevant community evidence without receiving billing records.
- QTB may use a bounded research source set without account-trading authority.
- AIMM may access approved operations records without exposing private credentials or strategy to public reporting.
- Botmad may prepare a document from approved files without broad publishing, deletion, or credential authority.

Data being present in a workspace does not authorize every AI workflow to use it.

## 10. Partner, Provider, and Support Access

Partners may need access for implementation, integration, training, campaign delivery, or first-line support.

Their access should identify:

- assigned customer, workspace, or program;
- product and environment;
- purpose and tasks;
- data categories;
- allowed actions;
- start and end time;
- credential owner;
- logging and review;
- subcontractor or provider treatment;
- support and incident duties;
- offboarding steps.

A support role should receive enough evidence to diagnose the assigned case without standing access to unrelated customer content.

Emergency access requires a named owner, reason, scope, duration, record, and follow-up review.

Partner, provider, support, and temporary access should be removed when the task, contract, role, incident, or approved period ends.

## 11. Commercial and Financial Records

Payment, invoice, refund, dispute, Platform Credit, stablecoin settlement, and reconciliation records receive restricted access.

Finance users may need transaction and customer context. Product users may need a simpler balance, allowance, or purchase history. Support staff may need status and correction authority without access to complete accounting records.

Stablecoin transactions visible onchain still require permissioned context such as:

- payer or customer account;
- invoice or purpose;
- product or service;
- fulfillment;
- fees and conversion;
- refund or reversal;
- treasury treatment;
- accounting classification;
- reconciliation status.

Product revenue reporting should use reconciled categories while protecting customer-level detail.

Investment proceeds, token activity, treasury transfers, liquidity movements, wallet balances, and product payments retain separate classifications.

## 12. Data Lifecycle

### 12.1 Collection

Collect or receive data for a stated product or operating purpose. Avoid requesting information the workflow does not need.

### 12.2 Use

Apply role, workspace, AI, partner, provider, and purpose restrictions. Record material actions and approvals.

### 12.3 Sharing

Share only with the intended audience or approved provider. Public release requires separate classification and review.

### 12.4 Retention

Retain records according to product need, customer agreement, security, dispute, accounting, tax, legal, professional, and jurisdictional requirements.

### 12.5 Correction

Allow authorized users or operators to correct inaccurate product, account, eligibility, permission, or reporting records while preserving necessary history.

### 12.6 Restriction, deletion, or anonymization

Delete, anonymize, restrict, or archive off-chain records according to approved policy and applicable requirements.

Some transaction, security, dispute, audit, legal, accounting, or professional records may require continued retention.

### 12.7 Closure

When a customer, partner, workspace, user role, or product closes:

1. stop new processing where applicable;
2. remove permissions;
3. disconnect integrations;
4. rotate or revoke credentials;
5. resolve exports and customer handoff;
6. apply retention, deletion, or restriction rules;
7. reconcile open support and commercial records;
8. record completion and remaining obligations.

Public blockchain records cannot be deleted by FUZE. FUZE may control its off-chain labels, interfaces, reports, cached data, and identity links.

## 13. User and Customer Requests

Requests concerning access, correction, export, restriction, deletion, consent, or objection should be authenticated and routed according to the relevant product, contract, privacy notice, policy, entity, and jurisdiction.

The process should identify:

- requester and authority;
- affected account, workspace, or record;
- request type;
- identity-verification method;
- applicable exceptions or retention duties;
- owner and response status;
- downstream providers or partners;
- completion record.

A request should not expose another person's data or weaken account security.

## 14. Public-Safe Reporting

A public report should use the minimum detail needed to explain the activity.

Useful approaches include:

- aggregation;
- category totals;
- cohort or period summaries;
- redaction;
- public wallet addresses without identity linkage;
- hashes or references;
- status labels;
- approved partner or customer case studies;
- methodology and correction notes.

Public reports should exclude:

- customer files;
- personal contact details;
- private messages;
- identity documents;
- credentials;
- payment details;
- private agreements;
- security-sensitive logs;
- non-public partner terms;
- legal, tax, accounting, or professional workpapers;
- unreconciled estimates presented as confirmed facts.

Small cohorts may create re-identification risk even when names are removed. Reviewers should consider whether combinations of location, product, time, role, wallet, or activity could identify a person or customer.

## 15. Security and Audit Evidence

Relevant control evidence may include:

- identity and access configuration;
- privileged-role reviews;
- permission tests;
- workspace-isolation tests;
- data-flow diagrams;
- integration and credential inventory;
- provider and subprocessor review;
- encryption and key-management direction;
- access and administrative logs;
- retention, export, and deletion tests;
- incident and recovery procedures;
- security findings and remediation;
- partner and support access records;
- offboarding records.

The level of public disclosure should not weaken security.

Qualified diligence may review more detailed evidence under appropriate authorization and confidentiality controls.

Reviewers should distinguish:

1. designed controls;
2. configured controls;
3. tested controls;
4. operating controls;
5. corrected controls after incidents or exceptions.

## 16. Privacy and Access Incidents

A privacy or access incident may involve:

- unauthorized viewing or sharing;
- incorrect export;
- cross-workspace exposure;
- model or provider exposure;
- partner or support misuse;
- credential compromise;
- incorrect public disclosure;
- unauthorized identity linkage;
- failure to remove access;
- improper retention or deletion;
- an AI tool acting beyond its approved data scope.

The response may include:

1. contain access or processing;
2. preserve relevant evidence;
3. identify affected systems, people, customers, and records;
4. correct permissions, records, or public material;
5. notify users, customers, partners, providers, or authorities where appropriate;
6. rotate credentials and test remediation;
7. review downstream sharing and retention;
8. restore, narrow, suspend, or retire the affected workflow;
9. record corrective action and reporting decisions.

Public incident detail should balance transparency with privacy, security, legal, contractual, and investigation requirements.

## 17. Product Control Profiles

| Product area | Sensitive data focus | Permission emphasis |
|---|---|---|
| HerHelp AI SaaS and SheetLayer AI | Files, spreadsheets, business context, generated outputs | Source selection, workspace boundaries, export review |
| ShopOS AI | Customers, staff, orders, stock, devices, payment-adjacent records | Owner and staff roles, device scope, financial separation |
| TrainLayer AI and SpeakShop AI | Source content, learners, campaigns, public outputs | Source rights, reviewer approval, audience control |
| CommunityLayer AI | Messages, moderation, verification, support evidence | Moderator authority, member privacy, escalation |
| ZAGA | Profiles, game records, community roles, optional wallet links | Game identity, operator roles, public-sharing controls |
| QTB and AIMM | Private research, watchlists, venue and operations records | Restricted workspaces, source and report sharing |
| AIE | Organizers, participants, sponsors, feedback | Consent, event roles, report redaction |
| ToolGrid AI | Providers, sponsors, campaigns, listing review | Campaign scope, moderation, sponsor labeling |
| Botmad | Files, tools, messages, tasks, credentials, and action logs | Least privilege, preview, confirmation, review, revocation |

Individual product papers define the exact workflow. This table identifies the data-control emphasis for cross-product and investor review.

## 18. Wallet, Token, and Identity Boundaries

A wallet may support access, eligibility, participation, game utility, recognition, claims, or another approved ecosystem function.

Wallet instructions should state:

- purpose;
- supported network;
- requested signature or transaction;
- eligibility method;
- resulting record;
- fees where applicable;
- correction and support route;
- privacy treatment.

A wallet address should not be treated as verified personal identity unless an authorized process establishes that relationship for a valid purpose.

Wallet status for one program does not create unrelated product access, governance authority, token rights, claims, distributions, or customer permissions.

## 19. Investor and Partner Review Questions

Reviewers should ask:

- Is there a current data inventory for each product?
- Which party controls or supplies each important data set?
- How are customer and partner workspaces isolated?
- Which roles may view, export, approve, pay, publish, delete, or change permissions?
- How is AI source and tool access bounded?
- How are providers, partners, and support staff provisioned and removed?
- Which records are public, workspace, restricted, or highly restricted?
- How are wallet records kept separate from identity?
- What retention, export, deletion, and offboarding tests exist?
- Which privacy or access incidents have occurred?
- Can public metrics be traced without exposing customers or users?
- Which controls are designed, configured, tested, operating, or corrected?
- Which customer, legal, or jurisdictional requirements remain unresolved?

These questions connect privacy and permissions to enterprise readiness, product safety, partner trust, support quality, and public reporting.

## 20. Public Reporting

Public privacy and permission reporting may include:

- product or workflow category;
- data classification summary;
- workspace and role model;
- control status;
- aggregate access-review results;
- incident category and correction status;
- retention or deletion-test summary;
- methodology and limitations.

Public reporting should not expose:

- personal information;
- private customer or partner data;
- credentials or secrets;
- exploit details;
- identity verification material;
- private legal or commercial terms;
- sensitive security procedures;
- small-cohort data that creates re-identification risk.

## 21. Public Boundary

This paper describes FUZE's public data privacy and permission model.

It is not:

- a privacy notice;
- a customer agreement;
- a data-processing agreement;
- a security certification;
- an independent audit;
- a legal, regulatory, or jurisdiction-specific conclusion;
- a guarantee that incidents, misuse, unauthorized access, or human error will not occur.

Specific rights, obligations, providers, processing locations, retention periods, transfer mechanisms, and security terms depend on the product, entity, customer, partner, jurisdiction, and current agreement.

## Key Takeaways

- FUZE data governance begins with purpose, data category, workspace, role, action, and audience.
- Access defaults to the smallest scope needed for the approved task.
- Private product and identity records remain permissioned; public reporting uses approved summaries or wallet-level evidence without unnecessary identity exposure.
- Blockchain visibility does not automatically make personal identity public.
- AI workflows, partners, providers, and support teams receive separate, bounded access.
- Platform Credit, payment, stablecoin, token, wallet, and revenue records retain distinct classifications.
- Designed, configured, tested, operating, and corrected controls are different evidence states.
- Public papers do not replace product-specific privacy notices, agreements, security review, or legal assessment.