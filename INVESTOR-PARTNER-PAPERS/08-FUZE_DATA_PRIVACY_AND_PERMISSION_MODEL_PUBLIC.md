# FUZE Data Privacy and Permission Model

## Executive Summary

FUZE products can process business files, shop records, community content, event information, AI prompts and outputs, product-usage records, payments, Platform Credits, wallet references, and operational evidence. Privacy and permission controls determine why that data is used, who can access it, which action is authorized, how long records remain, and what can appear in public reporting.

The model separates four environments: private product data, restricted operational evidence, public-safe reports, and public blockchain records. A wallet address or transaction can be visible without making the person behind it public. Identity documents, customer records, private agreements, credentials, and verification material remain permissioned.

Access is purpose-based. Product users, workspace owners, reviewers, partners, support staff, AI tools, and administrators receive different authority. Sensitive actions such as publication, payment changes, data export, member sanctions, wallet eligibility decisions, and destructive automation require explicit roles and records.

This paper gives investors and partners a framework for assessing data governance across FUZE. It does not replace product terms, a privacy notice, a data-processing agreement, or a security audit.

---

## 1. Control Objective

The objective is to use the minimum data and authority needed to deliver a defined product workflow while preserving useful evidence and public transparency.

Each workflow should answer:

1. What data is involved?
2. Who controls or supplies it?
3. Why does the product need it?
4. Which users, systems, AI tools, or partners can access it?
5. Which actions can each role perform?
6. Where is the data stored or transmitted?
7. What record supports review and correction?
8. How long is it retained?
9. What can be shared publicly?
10. How is access removed or the data deleted where applicable?

These decisions belong in product and implementation design rather than being deferred until broad release.

---

## 2. Data Inventory

| Category | Examples | Typical sensitivity |
|---|---|---|
| Account and identity | Login, workspace membership, role, contact details | Private |
| Product content | Settings, prompts, files, templates, outputs, reports | Private or workspace-controlled |
| Business operations | Sales, stock, staff, customers, tasks, spreadsheets | Private or restricted |
| Community and event | Messages, moderation evidence, participants, sponsors, feedback | Mixed; often private |
| AI operations | Instructions, retrieved context, model output, evaluation, usage metadata | Private or restricted |
| Commercial | Offers, invoices, payments, refunds, Platform Credit activity | Restricted |
| Partner | Integration, implementation, support, commercial, and campaign records | Restricted |
| Security | Logs, credentials, alerts, incidents, vulnerabilities | Highly restricted |
| Wallet and blockchain | Addresses, transactions, contract or vault references | Public at network level; contextual data can remain private |
| Verification | Identity, eligibility, custody, jurisdiction, or professional review evidence | Highly restricted |
| Public reporting | Approved metrics, status, hashes, summaries, labels | Public |

Not every product uses every category. The product owner should identify the specific fields and systems rather than rely only on broad labels.

---

## 3. Data Classification

FUZE can classify records by intended audience.

### Public

Approved product pages, public papers, current status, public-safe metrics, published wallet addresses, transaction references, report hashes, and other material intentionally released.

### Workspace

Records available to authorized members of a customer, team, shop, event, community, or project workspace.

### Restricted operational

Payment records, detailed usage, support cases, partner implementation, internal product reports, moderation evidence, market operations, and administrative logs.

### Highly restricted

Credentials, security findings, identity documents, private verification, legal advice, tax and accounting workpapers, sensitive treasury procedures, and protected personal data.

Classification controls access, sharing, retention, logging, and review. A public source can still become sensitive when combined with private identity or business context.

---

## 4. Permission Decision Model

An access decision should consider:

```text
user or service identity + workspace + role + resource
+ action + purpose + conditions -> allow, deny, or require approval
```

### Identity

The person, service, partner, or AI workflow requesting access is authenticated through the supported method.

### Workspace

The request belongs to a defined customer or operating boundary.

### Role

Owner, administrator, editor, operator, reviewer, finance role, support role, partner, viewer, or another approved role has assigned authority.

### Resource

The relevant file, report, data set, campaign, product module, payment record, wallet reference, or tool is identified.

### Action

Reading, creating, editing, exporting, publishing, approving, paying, deleting, connecting, or administering are separate permissions.

### Conditions

The action can require a time limit, second approval, network, device, value threshold, customer consent, or another product rule.

Permission should default to the smallest scope that supports the task.

---

## 5. Workspace Roles and Separation

A workspace can represent an individual, shop, team, enterprise, community, event, partner deployment, or game program.

Common role patterns include:

| Role | Typical authority |
|---|---|
| Owner | Workspace policy, billing, administrators, export, closure |
| Administrator | Users, configuration, approved integrations, operational reports |
| Editor or operator | Create and change product content within assigned scope |
| Reviewer | Inspect and approve selected outputs or actions |
| Finance role | View billing, credits, payment, refund, and reconciliation records |
| Support role | Access assigned cases and diagnostic evidence |
| Partner operator | Work only in assigned customer or implementation scope |
| Viewer | Read approved records without changing state |
| AI service | Use authorized data and tools for a defined task |

Workspace separation should prevent one customer, community, partner, or product program from accessing another’s records. Privileged roles need stronger authentication, logging, and periodic review.

---

## 6. Public, Blockchain, and Private Records

Blockchain visibility is not equivalent to identity transparency.

### Public network record

A network can expose an address, amount, asset, timestamp, contract, transaction, or event.

### FUZE public context

FUZE can publish an approved label, purpose, status, report hash, vault category, or other public-safe explanation.

### Permissioned context

The person, agreement, eligibility evidence, customer relationship, custody notes, tax information, and internal approval remain in restricted systems.

Public reporting should avoid joining these layers in a way that identifies a person without a valid purpose and approved process.

Wallet-level transparency can support review of vaults, releases, snapshots, activity, or status where relevant. Detailed eligibility, custody, participation, and claim treatment remains in the dedicated wallet papers.

---

## 7. AI Access

An AI workflow receives only the sources and tools required for its task.

Controls can include:

- explicit source selection
- workspace and folder boundaries
- restricted-field filtering
- retrieval limited by role
- read-only defaults
- tool allowlists
- confirmation before state changes
- output review
- prompt and result handling rules
- retention controls
- model and provider configuration
- access and action records

Examples:

- SheetLayer AI can process the selected sheet rather than every business file.
- CommunityLayer AI can review the relevant community evidence without receiving billing records.
- QTB can use a bounded research source set without account-trading authority.
- Botmad can prepare a document from approved files without broad credential or publishing access.

The [FUZE AI Safety and Reliability](07-FUZE_AI_SAFETY_AND_RELIABILITY_PUBLIC.md) paper covers evaluation, automation, and incident controls.

---

## 8. Partner and Support Access

Partners can need access for implementation, integration, training, campaign delivery, or first-line support. Their permissions should identify:

- assigned customer or program
- product and environment
- purpose and tasks
- data categories
- allowed actions
- start and end time
- credential owner
- logging and review
- subcontractor treatment
- offboarding steps

A support role should receive enough evidence to diagnose the case without gaining standing access to unrelated customer content.

Emergency access requires an owner, reason, duration, record, and follow-up review. Partner or support access should be removed when the task, contract, or role ends.

---

## 9. Commercial and Financial Records

Payment, invoice, refund, dispute, Platform Credit, stablecoin settlement, and reconciliation records receive restricted access.

Finance users can need transaction and customer context while product users need a simpler balance or purchase history. Support can need status and correction authority without seeing full accounting records.

Stablecoin transactions visible onchain still require permissioned business context such as payer, invoice, fulfillment, fees, conversion, refund, and accounting classification.

Product revenue reporting should use reconciled categories and protect customer-level detail. Investment proceeds, token activity, treasury transfers, and product payments retain separate classifications.

---

## 10. Data Lifecycle

### Collection

Collect or receive data for a stated product or operating purpose. Avoid requesting information that the workflow does not need.

### Use

Apply role, workspace, AI, and partner permissions. Record material actions and approvals.

### Sharing

Share within the intended audience or with an approved provider. Public release requires a separate classification and review.

### Retention

Retain records according to product need, customer agreement, security, dispute, accounting, tax, legal, and jurisdiction requirements.

### Correction

Allow authorized users or operators to correct inaccurate product, account, or reporting records while preserving necessary history.

### Deletion or restriction

Delete, anonymize, restrict, or archive off-chain records according to approved policy and applicable requirements. Some security, transaction, dispute, or professional records can require continued retention.

### Closure

When a customer, partner, workspace, or product closes, remove access, disconnect integrations, rotate credentials, resolve exports, apply retention rules, and record completion.

Public blockchain records cannot be deleted by FUZE. FUZE can control its off-chain labels, interfaces, reports, and identity links.

---

## 11. Public-Safe Reporting

A public report should use the minimum detail needed to explain the activity.

Useful approaches include:

- aggregation
- category totals
- cohort or period summaries
- redaction
- public wallet addresses without identity linkage
- hashes or references
- status labels
- approved partner or customer case studies
- methodology and correction notes

Public reports should exclude customer files, personal contact information, private messages, identity documents, credentials, payment details, private agreements, security-sensitive logs, non-public partner terms, and professional workpapers.

Small cohorts can create re-identification risk even when names are removed. Reviewers should consider whether combinations of location, product, time, role, and activity could reveal a person or customer.

---

## 12. Security and Audit Evidence

Relevant control evidence can include:

- identity and access configuration
- privileged-role reviews
- permission tests
- workspace-isolation tests
- data-flow diagrams
- integration and credential inventory
- encryption and key-management direction
- access and administrative logs
- retention and deletion tests
- provider review
- incident and recovery procedures
- security findings and remediation
- partner-access records

The level of public disclosure should not weaken security. Qualified diligence can review more detailed evidence under appropriate access and confidentiality controls.

Designed controls, configured controls, tested controls, and operating controls are distinct evidence levels.

---

## 13. Incident and Rights Handling

A privacy or access incident can involve unauthorized viewing, sharing, export, model exposure, partner misuse, credential compromise, incorrect public disclosure, or failure to remove access.

The response can include:

1. contain access or processing;
2. preserve relevant evidence;
3. identify affected systems, people, and records;
4. correct permissions or public material;
5. notify users, partners, or authorities where appropriate;
6. rotate credentials and test remediation;
7. review retention and downstream sharing;
8. record follow-up and reporting.

User or customer requests regarding access, correction, export, restriction, or deletion should be authenticated and routed according to the applicable product, contract, policy, and jurisdiction.

---

## 14. Product Control Profiles

| Product area | Sensitive data focus | Permission emphasis |
|---|---|---|
| HerHelp and SheetLayer AI | Files, spreadsheets, business context, generated outputs | Source selection, workspace boundaries, export review |
| ShopOS AI | Customers, staff, orders, stock, devices, payment-adjacent records | Owner and staff roles, device scope, financial separation |
| TrainLayer and SpeakShop AI | Source content, learners, campaigns, public outputs | Source rights, reviewer approval, audience control |
| CommunityLayer AI | Messages, moderation, verification, support evidence | Moderator authority, member privacy, escalation |
| ZAGA | Profiles, game records, community roles, optional wallet links | Game identity, public sharing, operator roles |
| QTB and AIMM | Private research, watchlists, venue and operations records | Restricted workspaces, source and report sharing |
| AIE | Organizers, participants, sponsors, feedback | Consent, event roles, report redaction |
| ToolGrid AI | Providers, sponsors, campaigns, listing review | Campaign scope, moderation, public labeling |
| Botmad | Files, tools, messages, task and action logs | Least privilege, confirmation, review, revocation |

Individual product papers define the exact workflow. This table identifies the data-control emphasis for investor review.

---

## 15. Investor and Partner Review Questions

Reviewers can ask:

- Is there a current data inventory for the product?
- Which party controls each important data set?
- How are customer workspaces isolated?
- Which roles can view, export, approve, pay, publish, or delete?
- How is AI source and tool access bounded?
- How are partners and support staff provisioned and removed?
- Which records are public, restricted, or highly restricted?
- How are wallet records separated from identity?
- What retention and deletion tests exist?
- Which incidents or access exceptions have occurred?
- Can public metrics be traced without exposing customers?
- Which controls are designed, configured, tested, and operating?

These questions connect privacy to enterprise readiness, partner trust, product safety, and reporting quality.

---

## 16. Public Boundary

This paper describes FUZE’s public data and permission model. It is not a privacy notice, customer agreement, data-processing agreement, security certification, or legal conclusion.

Specific rights, obligations, retention, processing locations, providers, and security terms depend on the product, entity, customer, jurisdiction, and current agreement. Controls reduce exposure and access risk but cannot eliminate every incident or human error.

---

## Conclusion

FUZE data governance depends on knowing the purpose, data, workspace, role, action, and audience for each workflow.

Private product and identity records remain permissioned; public reporting uses approved summaries or wallet-level evidence without exposing personal identity. Investors should expect this design to be supported by configured access, tests, logs, lifecycle procedures, incident handling, and product-specific operating evidence.
