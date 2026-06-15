# FUZE Participation Activation Gates

## Executive Summary

FUZE participation activation gates are the documented conditions that must be satisfied before wallet-based participation can move from design or readiness into an active operating state.

The gates cover legal, accounting, treasury, audit, reporting, technical, eligibility, privacy, operating, product-revenue, approved-value, and jurisdiction readiness. Each gate requires an owner, evidence, status, dependencies, decision, review date, and conditions for continued approval.

Readiness is not activation. Policies, calculations, contracts, vaults, snapshots, reports, and support processes can be prepared or tested while the mechanism remains unavailable. Activation requires a separate authorized decision that identifies the exact scope, effective time, eligible population, value period, contracts or systems, and public notice.

This paper owns the gate register and decision process. It does not repeat the detailed wallet workflow, approved distributable value calculation, smart-contract design, or privacy model maintained in their primary papers.

---

## 1. Gate Objective

The gate system exists to prevent a sensitive mechanism from becoming active because one technical component is ready while other required controls remain unresolved.

It provides:

- a complete inventory of activation conditions;
- accountable owners and reviewers;
- consistent status terminology;
- evidence requirements for each decision;
- dependency and exception tracking;
- a formal activation record;
- pause, remediation, and reactivation procedures;
- public-safe status reporting.

No single contract deployment, treasury balance, product-revenue report, wallet snapshot, audit activity, or policy document constitutes activation.

---

## 2. Scope of Activation

An activation decision must define its scope precisely.

| Scope element | Required definition |
|---|---|
| Mechanism | The participation function being activated |
| Product-revenue pool | The defined source period and product scope, where applicable |
| Approved value | The reviewed amount and approval reference |
| Eligible population | Supported wallet, custody, participant, and jurisdiction classes |
| Record date | Snapshot or qualification period |
| Claim or participation period | Opening, closing, and relevant cutoff times |
| Technical systems | Contracts, networks, vaults, registries, and interfaces |
| Operator | Responsible operating and support roles |
| Public notice | Approved status, instructions, and boundaries |
| Review period | Date or event that triggers reassessment |

A gate can be ready for one limited scope and unresolved for another. For example, a self-custody pilot in one supported context does not establish readiness for exchange custody or every jurisdiction.

---

## 3. Gate Register

FUZE should maintain a controlled gate register.

Each entry includes:

1. gate identifier and name;
2. accountable owner;
3. required evidence;
4. pass criteria;
5. current status;
6. dependencies and blocking issues;
7. reviewer and decision;
8. effective and expiry or review dates;
9. conditions or limitations;
10. linked remediation and change records.

The register should preserve prior decisions. A changed status should identify what changed, who approved it, and whether the activation scope is affected.

---

## 4. Status Vocabulary

| Status | Meaning |
|---|---|
| Not started | No accepted evidence package exists |
| In preparation | Owner is developing policy, process, system, or records |
| Under review | Evidence has been submitted to the responsible reviewer |
| Remediation required | Review found issues that must be resolved |
| Conditionally ready | Pass criteria are met subject to stated limits or pre-activation actions |
| Ready | Evidence satisfies the gate for the defined scope |
| Expired | Prior readiness requires renewal or updated evidence |
| Suspended | A material issue temporarily invalidates readiness |
| Not applicable | The gate does not apply to the stated scope, with documented rationale |

“Not applicable” requires approval. It should not be used merely because evidence is difficult to obtain.

The overall mechanism remains pre-activation until every required gate is `Ready` or `Conditionally ready` with all pre-activation conditions completed.

---

## 5. Required Gates

### 5.1 Legal gate

**Objective:** Confirm that the proposed operating structure, rights, communication, eligibility, restrictions, and user process have received appropriate legal review for the defined scope.

Evidence can include a current issue list, approved public language, participant terms, jurisdiction treatment, rights analysis, transfer and claim treatment, dispute provisions, and required private advice.

**Pass condition:** Material legal questions have an approved treatment, required restrictions are implementable, and public materials match the reviewed structure.

### 5.2 Accounting gate

**Objective:** Establish consistent recognition, classification, deduction, reserve, period, and reconciliation methods for the product-revenue pool and approved value.

Evidence can include accounting memos, source-system mappings, revenue and cost definitions, Platform Credit treatment, stablecoin and fiat treatment, refund and chargeback handling, period-close procedures, and reviewer signoff.

**Pass condition:** The source records and calculation can be reproduced, reconciled, reviewed, corrected, and reported.

### 5.3 Treasury gate

**Objective:** Confirm that custody, reserves, approvals, settlement assets, transaction execution, and reconciliation are controlled.

Evidence can include vault mapping, signer and authority records, multisig or equivalent controls, transaction limits, emergency procedures, settlement workflow, balance reconciliation, and segregation from operating funds.

**Pass condition:** An authorized movement can be executed and reconciled without relying on one person or mixing unrelated balances.

### 5.4 Audit and assurance gate

**Objective:** Provide independent or appropriately separated review of the records, calculations, controls, and exceptions relevant to activation.

Evidence can include review procedures, test samples, findings, correction logs, contract-review references, report hashes, and an open-issues register.

**Pass condition:** Material findings are resolved or formally accepted within the defined scope, and evidence remains available for later review.

### 5.5 Reporting gate

**Objective:** Ensure that participants and public readers can understand current status, scope, calculation period, eligibility, activity, corrections, and limitations.

Evidence can include report templates, data mappings, metric definitions, publication workflow, correction history, and privacy review.

**Pass condition:** FUZE can publish accurate, timely, public-safe reports that distinguish readiness, activation, approval, claim, and completion states.

### 5.6 Smart-contract and technical gate

**Objective:** Confirm that the required contracts, applications, data sources, wallet flows, monitoring, pause controls, and support systems behave as approved.

Evidence can include specifications, deployment status, tests, security review, role configuration, network and wallet support, failure handling, monitoring, incident exercises, and verified interfaces.

**Pass condition:** The active configuration matches the reviewed specification, critical findings are addressed, privileged actions are controlled, and the system can be paused or corrected where designed.

Detailed contract readiness belongs in [FUZE Smart Contract Readiness and Activation Gates](25-FUZE_SMART_CONTRACT_READINESS_AND_ACTIVATION_GATES_PUBLIC.md).

### 5.7 Eligibility gate

**Objective:** Define who qualifies and how the decision is evidenced.

Evidence can include wallet requirements, holding or record rules, supported custody, snapshot logic, exclusions, transfer treatment, duplicate controls, verification needs, dispute routes, and test cases.

**Pass condition:** The same facts produce consistent eligibility results, unsupported cases are identified, and corrections can be processed without arbitrary decisions.

### 5.8 Privacy gate

**Objective:** Preserve public wallet transparency without exposing personal identity or unnecessary private records.

Evidence can include data inventory, purpose and retention rules, access roles, identity-wallet separation, public report fields, deletion and correction procedures, security controls, and vendor treatment.

**Pass condition:** Public outputs reveal only approved address-level or aggregate information, while permissioned identity and support records remain protected.

### 5.9 Operator and governance gate

**Objective:** Confirm that FUZE has the people, authority, procedures, support capacity, and change controls required to run the mechanism.

Evidence can include role assignments, approval matrix, operating runbook, training, support procedures, escalation paths, incident response, change control, pause authority, and succession coverage.

**Pass condition:** Named operators can execute the full workflow, reviewers remain separated from sensitive execution where required, and no critical action depends on an undocumented individual.

### 5.10 Product-revenue gate

**Objective:** Confirm that the defined product-revenue pool is supported by settled, classified, and reconcilable product records.

Evidence can include invoices, payment and settlement records, Platform Credit mappings, refunds, chargebacks, taxes, fees, product costs, partner shares, period cutoffs, and source ownership.

**Pass condition:** Included revenue can be traced to the defined products and period, excluded receipts remain separated, and material uncertainty is resolved or reflected in the calculation.

### 5.11 Approved-distributable-value gate

**Objective:** Confirm that value proposed for the activated mechanism has passed the required deductions, reserves, reviews, and approvals.

Evidence can include the approved-value calculation, reserve rationale, treasury availability, legal and accounting reviews, governance approval, version history, and public reporting record.

**Pass condition:** The amount is final for the stated period and scope, authorized for the mechanism, and reconciled to the relevant treasury records.

The detailed calculation model is maintained in [FUZE Approved Distributable Value Model](09-FUZE_APPROVED_DISTRIBUTABLE_VALUE_MODEL_PUBLIC.md).

### 5.12 Jurisdiction gate

**Objective:** Define where and for whom the mechanism can operate under the approved legal, tax, payment, custody, data, and communication treatment.

Evidence can include supported and restricted scope, participant representations, screening requirements, local advice, custody limitations, tax communication, and change-monitoring procedures.

**Pass condition:** The system and user process can enforce the approved scope, and changes can trigger timely restriction, pause, or review.

---

## 6. Gate Dependencies

Gates are related but not interchangeable.

| Dependency | Why it matters |
|---|---|
| Product revenue before approved value | Value cannot be approved from an undefined or unreconciled source pool |
| Legal treatment before public notice | User rights and restrictions must match the reviewed structure |
| Eligibility before snapshot finalization | The record method must reflect the rules it is meant to test |
| Privacy before public reporting | Report fields must be designed before sensitive data is published |
| Treasury before technical activation | Contracts and interfaces need an approved source and execution authority |
| Technical readiness before operator signoff | Operators must train against the actual system |
| Reporting before activation | Status and corrections need a usable publication route |
| Audit after source records and calculation | Review requires stable evidence and a reproducible method |

A gate owner should record upstream dependencies and avoid issuing final readiness based on assumed completion elsewhere.

---

## 7. Evidence Pack

The activation evidence pack consolidates the current gate records.

It should contain:

- activation scope statement;
- gate register and status summary;
- evidence index with owners and dates;
- unresolved issue and remediation log;
- approved-value and treasury references;
- technical deployment and configuration references;
- eligibility and privacy specifications;
- operating runbook and support route;
- public notice draft;
- activation, pause, and rollback checklist;
- decision record.

Evidence can be public, permissioned, or restricted according to sensitivity. A public paper or dashboard should not imply that restricted evidence has been independently verified unless that review occurred.

---

## 8. Activation Review

The activation review should occur after gate owners submit their final status.

The reviewer or authorized body should:

1. confirm the exact activation scope;
2. verify all required gates and conditions;
3. examine unresolved issues and accepted limitations;
4. test consistency between legal, accounting, treasury, eligibility, technical, privacy, and public materials;
5. confirm operator and support readiness;
6. approve, reject, defer, or narrow the proposed scope;
7. set the effective time and next review trigger;
8. authorize the public notice and activation checklist.

The decision should be recorded before live operation begins.

---

## 9. Conditional Readiness and Exceptions

A gate can be conditionally ready when the remaining action is specific, low enough risk for the proposed scope, and capable of completion before activation or within an approved operating condition.

The condition record should identify:

- outstanding action;
- responsible owner;
- deadline or trigger;
- affected scope;
- interim control;
- consequence if incomplete.

An exception cannot override a fundamental absence of legal authority, source-value reconciliation, treasury control, eligibility definition, privacy protection, or safe technical operation.

Repeated exceptions should trigger redesign rather than becoming the normal operating model.

---

## 10. Activation Checklist

Immediately before activation, FUZE should confirm:

- gate statuses remain current;
- approved value and treasury balances remain reconciled;
- contract addresses, network, roles, and limits match the decision;
- snapshot or eligibility records are finalized as approved;
- public notice and user instructions are published;
- support, monitoring, and incident channels are staffed;
- pause authority is available;
- reporting and correction processes are operational;
- the effective time is recorded consistently across systems.

If a material item differs from the approved evidence pack, activation should return to review.

---

## 11. Pause Triggers

An active mechanism should pause or enter urgent review when a material issue affects:

- legal or jurisdiction support;
- source revenue or approved-value accuracy;
- treasury custody or reconciliation;
- contract security, availability, or privileged roles;
- eligibility or snapshot integrity;
- privacy or identity protection;
- operator authority or support capacity;
- public reporting accuracy;
- sanctions, fraud, abuse, or duplicate claims;
- third-party custody, network, oracle, or infrastructure reliability.

The pause record should state the affected scope, effective time, known impact, temporary controls, investigation owner, communication plan, and conditions for resumption.

A pause should preserve evidence and avoid exposing private participant details.

---

## 12. Remediation and Reactivation

Reactivation is a new decision, not an automatic consequence of fixing one issue.

FUZE should:

1. identify root cause and affected records;
2. correct systems, calculations, eligibility, communications, or controls;
3. assess participant and treasury impact;
4. retest the relevant workflow;
5. obtain renewed gate decisions where evidence changed;
6. update reports and correction history;
7. authorize a revised scope and effective time.

Material changes to rights, eligibility, value, custody, contracts, jurisdictions, or public language may require the full gate review.

---

## 13. Ongoing Gate Review

Readiness can expire as products, laws, contracts, operators, data, custody models, or market infrastructure change.

Gate owners should define review triggers such as:

- a new product-revenue pool or calculation period;
- material change in approved-value policy;
- contract upgrade or network migration;
- expanded custody or jurisdiction scope;
- new data collection or identity process;
- operator or signer change;
- material incident or correction;
- changed legal, accounting, tax, or audit advice;
- prolonged inactivity before activation.

The register should show the next review date or event for every ready gate.

---

## 14. Public Status Reporting

FUZE can publish a concise activation status without exposing private advice, personal identity, security-sensitive details, or confidential workpapers.

| Public field | Example treatment |
|---|---|
| Mechanism status | Design, preparation, under review, gate-ready, active, paused, or retired |
| Scope | Supported product pool, custody class, network, period, or jurisdiction summary |
| Gate summary | Ready, conditional, under review, or blocked counts with definitions |
| Effective record | Activation, pause, or retirement date and version |
| Approved value | Status and period where publication is appropriate |
| Reports | Links to public-safe calculation, activity, correction, or audit references |
| Changes | Material scope, rule, contract, or status updates |

Gate-ready should not be described as active. A public dashboard should identify the authoritative decision record and latest update.

---

## 15. Relationship to the Participation Model

The [FUZE Wallet-Based Participation Model](07-FUZE_WALLET_BASED_PARTICIPATION_MODEL_PUBLIC.md) explains eligible FUZE-holding wallets, custody treatment, snapshots, approved value, claims, privacy, and corrections where activated.

This paper answers a narrower question: **what evidence and approvals must exist before that workflow can operate?**

Community Participation Round access, product use, Platform Credit activity, stablecoin payments, token holding, or appearance in a draft snapshot do not satisfy the activation gates.

---

## 16. Public Boundary

This gate framework is a readiness and governance model. It does not announce activation, create eligibility, approve value, open a claim period, or publish transaction instructions.

Future activation depends on the evidence and decision for a defined scope. A gate can be delayed, restricted, suspended, or closed when requirements change.

For consolidated risk treatment, use [FUZE Token Risk Boundaries](29-FUZE_TOKEN_RISK_BOUNDARIES_PUBLIC.md) and the [FUZE Risk and Disclosure Appendix](../WHITEPAPER-PAPERS/05-FUZE_RISK_AND_DISCLOSURE_APPENDIX_PUBLIC.md).

---

## Conclusion

FUZE participation activation requires coordinated readiness across twelve gates and a separate authorized decision.

The gate register turns broad readiness statements into accountable evidence, pass criteria, dependencies, conditions, and review dates. The activation, pause, and reactivation processes then ensure that live status follows the approved scope rather than technical preparation alone.
