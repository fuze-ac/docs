
# FUZE Participation Activation Gates

## Executive Summary

FUZE Participation Activation Gates are the controlling readiness and authorization system that must be completed before wallet-based participation can move from design, preparation, testing, or technical deployment into active operation for a defined scope.

The gate system exists because no single component is sufficient by itself.

The following do not independently activate participation:

- a policy paper;
- a token balance;
- a product revenue figure;
- an approved-value calculation draft;
- a treasury balance;
- a deployed contract;
- a configured vault;
- a snapshot;
- a dashboard;
- an audit activity;
- a legal review;
- an internal test;
- a public announcement;
- or a target date.

Activation requires coordinated readiness across the applicable:

- legal and jurisdiction gate;
- accounting gate;
- product-revenue gate;
- approved-distributable-value gate;
- treasury and custody gate;
- governance and authority gate;
- audit and assurance gate;
- smart-contract and technical gate;
- eligibility gate;
- privacy and data gate;
- operator and support gate;
- reporting and public-communication gate; and
- incident, pause, correction, and continuity gate.

Each gate must have:

- a stable identifier;
- a defined scope;
- an accountable owner;
- required evidence;
- pass criteria;
- a reviewer;
- a current status;
- dependencies;
- blocking issues;
- limitations;
- an effective date;
- an expiry or reassessment trigger;
- and a decision record.

Readiness is not activation.

A gate can be ready for one limited configuration and unresolved for another.

For example, a self-custody pilot on one supported network may be ready while exchange custody, institutional custody, another jurisdiction, another product revenue pool, or another payout route remains unsupported.

The overall mechanism remains inactive until:

1. every required gate is `Ready` or `Conditionally ready` for the exact proposed scope;
2. all pre-activation conditions are completed;
3. the evidence pack is current;
4. cross-gate inconsistencies are resolved;
5. an authorized activation decision is recorded;
6. the public notice and operating systems match the approved scope; and
7. the effective activation event occurs.

The gate system also governs:

- narrowing;
- pause;
- suspension;
- remediation;
- reactivation;
- expansion;
- material change;
- closure; and
- retirement.

This paper owns the gate register, gate status vocabulary, evidence package, activation review, conditional-readiness rules, pre-activation checklist, pause triggers, remediation, reactivation, expiry, and public gate reporting.

The operating participation model appears in [FUZE Wallet-Based Participation Model](07-FUZE_WALLET_BASED_PARTICIPATION_MODEL_PUBLIC.md).

The approved-value calculation and approval model appears in [FUZE Approved Distributable Value Model](09-FUZE_APPROVED_DISTRIBUTABLE_VALUE_MODEL_PUBLIC.md).

## Purpose of This Paper

This paper explains:

- why a gate system is required;
- how activation scope is defined;
- how the gate register is maintained;
- the status vocabulary;
- all required gates;
- ownership, review, and separation of duties;
- evidence standards;
- gate dependencies;
- conditional readiness and exceptions;
- the activation evidence pack;
- the activation review and decision;
- the pre-activation checklist;
- material-change review;
- pause and suspension triggers;
- remediation and reactivation;
- gate expiry and ongoing review;
- closure and retirement;
- public gate reporting;
- status and evidence requirements; and
- public limitations.

This paper does not replace:

- legal advice;
- tax advice;
- accounting policy;
- treasury policy;
- custody agreements;
- smart-contract specifications;
- product-revenue-pool definitions;
- approved distributable value records;
- wallet eligibility rules;
- snapshot specifications;
- participant terms;
- claim instructions;
- payout instructions;
- incident runbooks;
- audit workpapers;
- or the token risk register.

## Gate Principles

### Scope Before Readiness

No gate should be marked ready without a precise scope.

Readiness should identify the exact:

- mechanism;
- framework version;
- product revenue pool;
- accounting period;
- approved-value period;
- payout asset;
- payout network;
- FUZE token network and contract;
- wallet categories;
- custody classes;
- participant classes;
- jurisdictions;
- snapshot or eligibility method;
- claim or participation method;
- contracts and systems;
- operators;
- support route;
- reporting method;
- and review period.

### Evidence Before Status

Gate status should be based on current, reviewable evidence.

A meeting, intention, plan, draft, or verbal assurance is not sufficient when the gate requires documented proof.

### Independent Gates, Integrated Decision

Gates remain separate because each controls a different risk.

They are integrated because the final mechanism must be internally consistent.

For example:

- legal wording must match eligibility behavior;
- accounting treatment must match the approved-value calculation;
- treasury custody must match the payout flow;
- privacy treatment must match public reporting;
- operator procedures must match the deployed technical system;
- and the public notice must match the activated scope.

### Readiness Before Activation

A gate may be ready while the mechanism remains inactive.

Activation requires a separate decision and effective event.

### Least-Broad Scope

Where evidence supports only a limited scope, activation should be limited to that scope.

FUZE should prefer:

- one product pool over an undefined portfolio pool;
- one reviewed period over an open-ended period;
- one supported wallet class over unsupported custody assumptions;
- one supported jurisdiction set over global language;
- one tested claim route over multiple untested routes;
- and one controlled payout method over broad optionality.

### No Silent Inheritance

Readiness should not be inherited automatically by:

- another period;
- another product;
- another product revenue pool;
- another network;
- another contract;
- another wallet or custody class;
- another jurisdiction;
- another payout asset;
- another provider;
- another operator;
- or another framework version.

### Reversibility

Activation should not occur unless the mechanism can be:

- paused;
- narrowed;
- corrected;
- reconciled;
- rolled back where technically possible;
- migrated;
- closed;
- or retired.

### Public Status Must Match Evidence

`Ready`, `approved for activation`, `active`, `paused`, and `retired` are different states.

A technical deployment should not be described as activation.

### Market Outcomes Remain Separate

Gate readiness or activation does not establish:

- DEX access;
- CEX application;
- CEX approval;
- listing;
- liquidity;
- depth;
- spread;
- volume;
- token demand;
- price support;
- price appreciation;
- revenue growth;
- income;
- or financial return.

## Activation Scope Record

Every proposed activation should have a versioned scope record.

| Scope field | Required definition |
|---|---|
| Activation identifier | Stable reference for the proposed or approved activation |
| Framework version | Exact participation-model version |
| Mechanism | Wallet-based participation function being activated |
| Product revenue pool | Included products, transaction types, and accounting period |
| Approved-value record | Approved amount, asset denomination, period, and approval reference |
| FUZE token identity | Network, canonical contract, decimals, and status |
| Token condition | Balance, holding period, snapshot, average, continued holding, or other approved rule |
| Snapshot or eligibility period | Block, time, method, source, finality, and correction window |
| Wallet categories | Included, excluded, restricted, and separately treated categories |
| Custody classes | Self-custody, smart account, multisig, exchange, institutional, omnibus, contract, or other supported classes |
| Participant scope | Eligible participant types and verification requirements |
| Jurisdiction scope | Supported and restricted locations or participant categories |
| Claim or participation process | Portal, contract, custody, manual, or other approved route |
| Payout or settlement | Asset, network, custody, batch, timing, fees, and failure treatment |
| Technical systems | Contracts, vaults, registries, indexers, portals, APIs, providers, and monitoring |
| Operators | Product, treasury, eligibility, claim, payout, support, security, privacy, reporting, and incident roles |
| Public notice | Approved notice version and authoritative publication source |
| Effective event | Date, time, block, governance action, deployment event, or other controlling activation event |
| Review trigger | Date, period close, incident, material change, or other reassessment trigger |
| Limitations | Known exclusions, unsupported cases, and open conditions |
| Current status | Proposed, under review, approved for activation, active, paused, closed, or retired |
| Current-as-of date | Time to which the status applies |

A gate can be ready only for the scope stated in this record.

## Gate Register

FUZE should maintain a controlled gate register.

Each gate entry should include:

1. gate identifier;
2. gate name;
3. activation identifier;
4. framework version;
5. scope summary;
6. accountable owner;
7. contributing owners;
8. required evidence;
9. evidence references;
10. evidence date;
11. pass criteria;
12. current status;
13. reviewer;
14. reviewer decision;
15. decision date;
16. effective date;
17. expiry or reassessment trigger;
18. upstream dependencies;
19. downstream dependencies;
20. blocking issues;
21. conditions;
22. limitations;
23. remediation actions;
24. exception references;
25. material-change references;
26. pause or suspension effect;
27. public-reporting status;
28. correction history;
29. latest review date;
30. next review date or event;
31. current-as-of date; and
32. archival state.

The register should preserve prior versions and decisions.

A changed status should identify:

- what changed;
- why it changed;
- who approved the change;
- which evidence changed;
- whether activation scope is affected;
- whether public communication must change;
- and whether reactivation or renewed approval is required.

## Gate Status Vocabulary

| Status | Evidence-backed meaning | What it does not establish |
|---|---|---|
| Not started | No accepted evidence package exists. | Preparation or readiness |
| In preparation | The owner is developing policy, process, system, records, or controls. | Review or pass |
| Evidence submitted | The owner has submitted a defined package for review. | Reviewer acceptance |
| Under review | The responsible reviewer is evaluating the evidence. | Readiness |
| Remediation required | Material issues must be corrected before readiness. | Conditional approval |
| Conditionally ready | Pass criteria are satisfied subject to documented limits or pre-activation conditions. | Activation while conditions remain incomplete |
| Ready | Current evidence satisfies the gate for the exact defined scope. | Overall mechanism activation |
| Expiring | The gate remains usable temporarily but renewal or updated evidence is required by the stated trigger. | Indefinite readiness |
| Expired | Prior readiness is no longer current. | Continued use without review |
| Suspended | A material issue temporarily invalidates readiness. | Closure or retirement |
| Failed | The gate does not satisfy the pass criteria for the proposed scope. | Permanent rejection of every narrower scope |
| Not applicable | The gate does not apply to the exact scope, with approved rationale and no hidden dependency. | Permission to ignore difficult evidence |
| Closed | The gate is no longer active because the activation scope has ended. | Historical erasure |
| Archived | Historical evidence and decisions are retained but not current. | Readiness or active status |

`Not applicable` requires reviewer approval.

The overall mechanism remains pre-activation until every required gate is `Ready` or `Conditionally ready` and every pre-activation condition is complete.

## Ownership and Separation of Duties

The gate system should assign accountable roles without concentrating incompatible authority in one undocumented individual.

Possible roles include:

- framework owner;
- product revenue owner;
- accounting owner;
- treasury owner;
- custody owner;
- governance owner;
- legal and compliance reviewer;
- tax reviewer;
- audit or assurance reviewer;
- smart-contract owner;
- security reviewer;
- eligibility owner;
- privacy owner;
- operations owner;
- support owner;
- reporting owner;
- incident commander;
- activation approver;
- pause authority;
- and reactivation approver.

### Minimum Separation Expectations

Where proportionate to scope:

- the person calculating approved value should not unilaterally approve it;
- the person approving eligibility logic should not unilaterally change production data;
- the person preparing a payout batch should not unilaterally execute and reconcile it;
- the person operating a contract should not unilaterally approve its security status;
- the person publishing a public report should not silently alter source records;
- and the person requesting an exception should not be the only approver of the exception.

When staffing limits require combined roles, the evidence pack should document:

- combined responsibilities;
- compensating controls;
- independent review points;
- limits;
- and approval authority.

## Required Gates

### Gate 1: Legal and Jurisdiction

**Objective:** Confirm that the proposed mechanism, participant rights, restrictions, claims, payouts, custody, data treatment, communication, and dispute process have an approved treatment for the defined scope.

#### Required Evidence

Evidence may include:

- issue list;
- structure summary;
- participant terms;
- public wording review;
- supported and restricted jurisdiction analysis;
- eligibility and verification requirements;
- claim and payout characterization;
- custody and beneficial-ownership treatment;
- consumer and financial-promotion treatment;
- gaming, payment, sanctions, securities, privacy, and other relevant analysis;
- dispute and governing-law treatment;
- tax communication boundaries;
- escalation requirements;
- and current advice references.

#### Pass Criteria

- material legal and jurisdiction questions have approved treatment;
- required restrictions can be enforced operationally and technically;
- participant terms match the mechanism;
- public language matches the reviewed structure;
- unsupported jurisdictions and participant classes are identifiable;
- claim and payout processes do not exceed the reviewed rights;
- and unresolved limitations are documented in the activation scope.

#### Blocking Conditions

- unclear operating authority;
- unenforceable restrictions;
- inconsistent public language;
- unresolved material participant-rights issues;
- unsupported jurisdictional scope;
- or inability to implement required controls.

### Gate 2: Accounting

**Objective:** Establish reproducible recognition, classification, period, deduction, reserve, currency, correction, and reconciliation methods.

#### Required Evidence

Evidence may include:

- accounting policy or memo;
- source-system mapping;
- product revenue definitions;
- Platform Credit treatment;
- fiat, stablecoin, and other payment-asset treatment;
- revenue-recognition timing;
- refunds and chargebacks;
- payment, network, and provider fees;
- taxes and liabilities;
- partner shares;
- operating and support costs;
- reserves;
- currency conversion;
- period-close procedure;
- correction and restatement method;
- account mapping;
- reconciliation examples;
- and reviewer signoff.

#### Pass Criteria

- included and excluded records are defined;
- calculations can be reproduced from source records;
- period treatment is consistent;
- Platform Credit activity is not confused with recognized revenue;
- deductions and reserves are classified;
- source, treasury, claim, payout, and reporting records reconcile;
- corrections preserve history;
- and the method supports period close and review.

#### Blocking Conditions

- unreconciled source systems;
- unclear revenue-recognition basis;
- undefined Platform Credit treatment;
- material unclassified balances;
- or inability to reproduce the approved-value calculation.

### Gate 3: Product Revenue

**Objective:** Confirm that the product revenue pool is defined, settled, attributable, complete for the period, and separated from excluded receipts.

#### Required Evidence

Evidence may include:

- pool identifier;
- included products;
- included transaction types;
- excluded products and receipts;
- invoice records;
- payment and settlement records;
- delivery or consumption evidence where relevant;
- Platform Credit mappings;
- refunds and chargebacks;
- taxes;
- fees;
- partner shares;
- period cutoff;
- source ownership;
- unresolved-item register;
- and product-owner confirmation.

#### Pass Criteria

- included revenue can be traced to defined products and transactions;
- excluded receipts remain separate;
- settlement and timing are known;
- refunds, chargebacks, and partner shares are reflected;
- the period is closed or controlled under documented open-item treatment;
- material uncertainty is resolved or reflected in reserves;
- and the pool can support approved-value review.

#### Blocking Conditions

- undefined pool scope;
- unsupported revenue estimates;
- material unsettled receipts without treatment;
- mixed operating, fundraising, customer, or treasury inflows;
- or missing product-owner confirmation.

### Gate 4: Approved Distributable Value

**Objective:** Confirm that candidate value has passed all required deductions, reserves, reconciliations, reviews, and approvals.

#### Required Evidence

Evidence may include:

- approved-value calculation;
- source pool references;
- gross amount;
- deductions;
- reserves;
- currency conversion;
- accounting review;
- legal and compliance review;
- treasury availability;
- audit or assurance review;
- governance approval;
- version history;
- correction state;
- payout-asset treatment;
- custody reference;
- and public-reporting record.

#### Pass Criteria

- the amount is final or explicitly controlled for the stated period;
- source and deductions reconcile;
- reserves are approved;
- treasury availability is confirmed;
- the amount is authorized for the mechanism;
- claim and payout availability states are defined separately;
- and the public and permissioned records are ready.

#### Blocking Conditions

- candidate value treated as approved value;
- unresolved reconciliation differences;
- unavailable treasury balance;
- missing governance approval;
- or unsupported payout-asset assumptions.

The detailed model appears in [FUZE Approved Distributable Value Model](09-FUZE_APPROVED_DISTRIBUTABLE_VALUE_MODEL_PUBLIC.md).

### Gate 5: Treasury and Custody

**Objective:** Confirm that value custody, movement authority, payout assets, reserves, settlement, and reconciliation are controlled.

#### Required Evidence

Evidence may include:

- custody and vault map;
- account and subledger map;
- source and destination controls;
- signer and authority registry;
- multisig or equivalent policy;
- timelock treatment where applicable;
- transaction limits;
- payout-asset inventory;
- network and destination controls;
- batch process;
- simulation and approval process;
- fee treatment;
- emergency pause;
- key-compromise procedure;
- provider-failure procedure;
- segregation from operating funds;
- reconciliation runbook;
- and test evidence.

#### Pass Criteria

- value is identifiable and available under approved custody;
- unrelated balances are segregated or reliably subledgered;
- no critical movement depends on one undocumented individual;
- payout preparation, approval, execution, confirmation, and reconciliation are distinguishable;
- limits and emergency controls are active;
- failed or returned payouts can be handled;
- and balances reconcile to accounting and approved-value records.

#### Blocking Conditions

- unclear source custody;
- unrestricted single-person movement;
- mixed balances without reliable reconciliation;
- missing payout-asset availability;
- or untested emergency controls.

### Gate 6: Governance and Authority

**Objective:** Confirm that every material decision and emergency action has a defined, reviewable authority.

#### Required Evidence

Evidence may include:

- authority matrix;
- activation authority;
- value-approval authority;
- snapshot and eligibility authority;
- claim and payout authority;
- contract-admin authority;
- pause and reactivation authority;
- material-change authority;
- exception authority;
- conflict-of-interest controls;
- quorum or threshold where applicable;
- multisig and timelock configuration;
- succession and backup coverage;
- decision-record format;
- and governance calendar or trigger list.

#### Pass Criteria

- each material action has an accountable authority;
- decision scope and limits are documented;
- conflicts and recusals are controlled;
- emergency powers are bounded;
- authority survives ordinary staff absence;
- governance records are retained;
- and technical roles match approved authority.

#### Blocking Conditions

- ambiguous activation authority;
- undocumented emergency power;
- signer configuration inconsistent with policy;
- unresolved conflicts;
- or inability to record and verify decisions.

### Gate 7: Audit and Assurance

**Objective:** Provide independent or appropriately separated review of source records, calculations, controls, technical evidence, exceptions, and reporting.

#### Required Evidence

Evidence may include:

- review scope;
- reviewer qualifications or independence;
- source samples;
- calculation reperformance;
- custody and treasury testing;
- eligibility testing;
- contract and configuration review references;
- control walkthroughs;
- exception and finding register;
- remediation evidence;
- report hashes;
- management representations where appropriate;
- and conclusion record.

#### Pass Criteria

- review scope matches the activation scope;
- material calculations and records can be reproduced;
- key controls have been tested;
- material findings are resolved or formally accepted within a bounded scope;
- open findings are visible to the activation authority;
- evidence remains retained;
- and public statements do not overstate the review performed.

#### Blocking Conditions

- unresolved critical finding;
- inability to reproduce material calculations;
- unavailable source evidence;
- review scope narrower than public claims;
- or claimed independence that does not exist.

### Gate 8: Smart Contract and Technical

**Objective:** Confirm that contracts, applications, data sources, wallets, registries, claim flows, payout systems, monitoring, pause controls, and recovery procedures behave as approved.

#### Required Evidence

Evidence may include:

- technical specification;
- architecture;
- threat model;
- contract source and deployment records;
- network and canonical contract references;
- role configuration;
- upgrade and admin-power treatment;
- tests;
- security review;
- wallet and custody compatibility;
- snapshot and eligibility implementation;
- indexer and node behavior;
- claim and payout implementation;
- replay protection;
- finality and reorg treatment;
- provider-failure handling;
- monitoring;
- alerting;
- incident exercises;
- pause, correction, migration, and rollback tests;
- and verified interfaces.

#### Pass Criteria

- active configuration matches the reviewed specification;
- canonical addresses and networks are verified;
- privileged actions are controlled;
- critical findings are resolved;
- wallet, custody, snapshot, eligibility, claim, and payout flows work within scope;
- failures are observable and supportable;
- monitoring and alerts are active;
- and the mechanism can be paused or corrected where designed.

#### Blocking Conditions

- critical security finding;
- unverified contract or configuration;
- uncontrolled admin power;
- unsupported wallet or custody behavior;
- untested claim or payout path;
- or missing pause capability.

Detailed contract treatment appears in [FUZE Smart Contract Readiness and Activation Gates](25-FUZE_SMART_CONTRACT_READINESS_AND_ACTIVATION_GATES_PUBLIC.md).

### Gate 9: Eligibility

**Objective:** Define who qualifies, which facts determine status, how custody is handled, and how consistent decisions and corrections are produced.

#### Required Evidence

Evidence may include:

- framework and period identifier;
- FUZE token rule;
- balance or holding-period method;
- snapshot specification;
- included and excluded wallet categories;
- self-custody proof method;
- smart-account and multisig treatment;
- exchange and omnibus custody treatment;
- institutional custody treatment;
- beneficial-ownership evidence;
- multiple-wallet treatment;
- continued-holding rule;
- transfer treatment;
- jurisdiction and verification requirements;
- duplicate and abuse controls;
- reason codes;
- dispute and appeal process;
- correction process;
- and test cases.

#### Pass Criteria

- the same facts produce consistent results;
- unsupported cases are identified;
- wallet categories are controlled;
- custody-specific evidence is defined;
- duplicate and abuse rules are testable;
- reason codes support review;
- corrections preserve history;
- and eligibility can be reproduced for the stated period.

#### Blocking Conditions

- ambiguous token rule;
- undefined custody treatment;
- inconsistent snapshot method;
- unsupported beneficial-ownership assumptions;
- arbitrary decisions;
- or no correction route.

### Gate 10: Privacy and Data

**Objective:** Preserve public wallet transparency while protecting private identity, account, custody, tax, support, and wallet-person mapping records.

#### Required Evidence

Evidence may include:

- data inventory;
- data-flow map;
- purpose and lawful-basis treatment where applicable;
- collection minimization;
- consent or notice;
- public and permissioned field classification;
- wallet-person mapping controls;
- access roles;
- retention and deletion rules;
- correction and export processes;
- vendor and cross-border treatment;
- logging;
- security controls;
- public-report template;
- privacy impact review;
- and incident response.

#### Pass Criteria

- only necessary data is collected;
- public outputs expose only approved wallet-level or aggregate information;
- private identity and account evidence remains permissioned;
- wallet-person mappings are restricted;
- access is logged and reviewable;
- retention and deletion are enforceable;
- vendors meet the required controls;
- and privacy incidents can be contained and reported appropriately.

#### Blocking Conditions

- unnecessary identity collection;
- public exposure of private participant data;
- uncontrolled wallet-person mapping;
- missing retention or deletion treatment;
- or unsupported vendor data handling.

### Gate 11: Operator and Support

**Objective:** Confirm that named operators can run the complete mechanism safely, consistently, and continuously.

#### Required Evidence

Evidence may include:

- operating model;
- role assignments;
- runbook;
- period calendar;
- training records;
- service expectations;
- eligibility-review process;
- claim and payout support;
- provider escalation;
- correction and dispute handling;
- incident response;
- pause procedure;
- change control;
- business continuity;
- backup and succession coverage;
- workload and capacity assessment;
- and test exercises.

#### Pass Criteria

- named operators understand their roles;
- the full workflow can be executed from source records through closure;
- support channels are active;
- escalation routes are current;
- sensitive actions use appropriate separation;
- staff absence does not create uncontrolled failure;
- incidents and corrections can be managed;
- and operating capacity matches the proposed scope.

#### Blocking Conditions

- no accountable operator;
- unsupported workload;
- undocumented manual steps;
- missing support route;
- single-person dependency without compensating control;
- or untested incident and continuity procedures.

### Gate 12: Reporting and Public Communication

**Objective:** Ensure that participants and public readers can understand current status, scope, method, approved value, eligibility, claims, payouts, corrections, limitations, and closure without exposing private records.

#### Required Evidence

Evidence may include:

- public notice;
- report templates;
- metric definitions;
- source mappings;
- methodology;
- period and timezone definitions;
- status vocabulary;
- public and permissioned field classification;
- publication workflow;
- review and approval workflow;
- report hashes or references;
- correction and restatement process;
- archive process;
- support links;
- and privacy review.

#### Pass Criteria

- the public notice matches the activated mechanism;
- reports distinguish readiness, activation, snapshot, eligibility, claim, payout, settlement, correction, and closure;
- counts and amounts use defined denominators;
- current-as-of dates are visible;
- corrections preserve prior versions;
- private identity is not exposed;
- and FUZE can publish accurate, timely, public-safe status updates.

#### Blocking Conditions

- public wording inconsistent with the mechanism;
- undefined metrics;
- inability to correct reports;
- privacy conflict;
- or use of stronger status language than the evidence supports.

### Gate 13: Incident, Pause, Correction, and Continuity

**Objective:** Confirm that material errors, attacks, failures, provider outages, discrepancies, and legal or privacy issues can be contained without losing evidence or abandoning valid obligations.

#### Required Evidence

Evidence may include:

- incident taxonomy;
- severity levels;
- incident commander;
- detection and alerting;
- pause authority;
- contract and operational pause methods;
- affected-scope controls;
- communication plan;
- participant support plan;
- evidence preservation;
- correction and restatement process;
- payout hold and recovery procedures;
- provider-failure procedures;
- compromised-wallet treatment;
- treasury discrepancy treatment;
- reactivation checklist;
- business continuity plan;
- and exercise results.

#### Pass Criteria

- material failures can be detected;
- the affected scope can be paused or isolated;
- evidence is preserved;
- claims and payouts can be held or corrected safely;
- participant and public communication routes are ready;
- valid obligations remain tracked;
- continuity and recovery are tested;
- and reactivation requires renewed authority.

#### Blocking Conditions

- no pause authority;
- no way to isolate affected processing;
- no correction or restatement method;
- missing evidence preservation;
- or untested continuity for critical providers or operators.

## Gate Dependencies

Gates are related but not interchangeable.

| Dependency | Why it matters |
|---|---|
| Product revenue before approved value | Value cannot be approved from an undefined or unreconciled source pool |
| Accounting before approved-value approval | Deductions, reserves, period treatment, and corrections require a reproducible method |
| Legal and jurisdiction before public notice | Participant rights, restrictions, and wording must match the reviewed structure |
| Eligibility before final snapshot execution | The snapshot method must reflect the rule it is intended to test |
| Privacy before public reporting | Public fields must be designed before wallet and participant data are published |
| Governance before treasury and technical operation | Signers, admins, operators, and emergency roles need approved authority |
| Treasury before payout activation | Claims cannot settle safely without approved custody, asset, movement, and reconciliation controls |
| Technical readiness before operator signoff | Operators must train against the actual configuration and failure states |
| Audit after stable source records and calculations | Assurance requires reproducible evidence and a defined method |
| Reporting before activation | Status, corrections, incidents, and closure require an operational publication route |
| Incident readiness before activation | A mechanism should not go active before it can be paused, corrected, and recovered |

A gate owner should record upstream and downstream dependencies.

A reviewer should not issue final readiness based on assumed completion elsewhere.

## Evidence Standards

### Evidence Quality

Evidence should be:

- current;
- attributable;
- complete for the stated scope;
- reproducible where applicable;
- reviewable;
- versioned;
- protected according to sensitivity;
- and linked to the gate decision.

### Evidence Classes

Evidence may be:

- public;
- permissioned;
- restricted;
- confidential professional advice;
- security-sensitive;
- or operationally sensitive.

A public report may state that a review occurred without publishing protected workpapers.

It should not imply independent assurance beyond the review actually performed.

### Evidence Freshness

Each gate should define whether evidence expires because of:

- time;
- a new participation period;
- a new product revenue pool;
- a new approved-value calculation;
- a network or contract change;
- a custody-provider change;
- a jurisdiction change;
- a key operator or signer change;
- a material incident;
- a legal, accounting, tax, or audit update;
- or prolonged inactivity before activation.

### Evidence Gaps

An evidence gap should be recorded as:

- blocking;
- remediable before activation;
- conditionally acceptable for a limited scope;
- not applicable with approved rationale;
- or requiring redesign.

Unknown should not be converted into `Ready`.

## Conditional Readiness

A gate may be `Conditionally ready` only when:

- the remaining action is specific;
- the risk is bounded for the exact scope;
- the interim control is documented;
- the owner and deadline or trigger are defined;
- the activation authority understands the limitation;
- the public notice can state the limitation accurately;
- and failure to complete the condition has a defined consequence.

A conditional-readiness record should identify:

1. gate;
2. scope;
3. outstanding action;
4. risk;
5. interim control;
6. owner;
7. deadline or trigger;
8. evidence required for closure;
9. effect on activation;
10. effect on participants;
11. effect on public reporting;
12. pause or expiry condition;
13. reviewer;
14. approver; and
15. current status.

### Conditions That Must Be Complete Before Activation

A gate may be conditionally ready while a pre-activation action remains open, but the mechanism cannot activate until that action is complete.

Examples may include:

- publishing the approved notice;
- loading the final allowed-wallet category list;
- confirming final treasury balance;
- completing final role transfer;
- setting final transaction limits;
- recording the snapshot block;
- or completing a final operational exercise.

### Conditions That May Continue During Limited Operation

A condition may continue during a limited pilot only when:

- the pilot scope is narrow;
- the condition does not remove a fundamental control;
- participants are not misled;
- the interim control is effective;
- monitoring is active;
- and pause criteria are defined.

## Exceptions

An exception is a documented, time-bounded deviation from a normal gate requirement.

An exception record should identify:

- requirement;
- reason;
- proposed deviation;
- affected scope;
- risk;
- compensating control;
- owner;
- reviewer;
- approver;
- effective period;
- expiry;
- monitoring;
- participant effect;
- public-reporting effect;
- and closure.

An exception cannot override the fundamental absence of:

- legal authority;
- defined participant rights;
- source-value reconciliation;
- approved distributable value;
- treasury control;
- governance authority;
- eligibility definition;
- privacy protection;
- safe technical operation;
- pause capability;
- or public status accuracy.

Repeated exceptions should trigger redesign rather than becoming the default operating model.

## Activation Evidence Pack

The activation evidence pack consolidates the current decision basis.

It should contain:

- activation scope record;
- framework version;
- gate register;
- gate-status summary;
- evidence index;
- owner and reviewer list;
- unresolved issue register;
- remediation register;
- conditional-readiness register;
- exception register;
- product revenue pool reference;
- approved distributable value reference;
- accounting and treasury references;
- custody and payout references;
- governance and authority references;
- technical deployment and configuration references;
- security-review references;
- snapshot and eligibility specifications;
- privacy and data references;
- operating runbook;
- support and incident routes;
- public notice;
- report templates;
- activation checklist;
- pause and rollback checklist;
- closure and retirement checklist;
- activation decision template;
- and current-as-of date.

The pack should identify which evidence is:

- public;
- permissioned;
- restricted;
- confidential;
- or security-sensitive.

## Activation Review

The activation review should occur only after gate owners submit their final statuses for the proposed scope.

The authorized reviewer or decision body should:

1. confirm the activation identifier and framework version;
2. confirm the exact scope;
3. verify every required gate;
4. inspect all conditional-readiness items;
5. inspect all exceptions;
6. confirm all pre-activation actions;
7. examine unresolved issues;
8. test consistency across legal, accounting, product revenue, approved value, treasury, governance, technical, eligibility, privacy, operations, incident, and public materials;
9. confirm operator and support capacity;
10. confirm approved-value and treasury reconciliation;
11. confirm contracts, networks, wallet categories, claim routes, payout assets, and systems;
12. confirm the public notice;
13. confirm monitoring and pause readiness;
14. decide whether to approve, reject, defer, narrow, or return the proposal for remediation;
15. set the effective event;
16. set the review and expiry triggers;
17. authorize the public status; and
18. record the decision before operation begins.

## Activation Decision Record

The decision record should include:

- activation identifier;
- framework version;
- decision status;
- approved scope;
- excluded scope;
- gate summary;
- conditional items;
- exceptions;
- accepted limitations;
- effective event;
- effective time;
- activation authority;
- decision participants;
- recusals or conflicts;
- approved public notice;
- monitoring requirements;
- pause authority;
- review triggers;
- expiry;
- closure conditions;
- and current-as-of date.

Possible decisions are:

- approved for activation;
- approved for a narrower scope;
- deferred;
- remediation required;
- rejected;
- withdrawn;
- or cancelled.

`Approved for activation` is not the same as `Active`.

## Pre-Activation Checklist

Immediately before the effective activation event, FUZE should confirm:

- the activation decision remains valid;
- gate statuses remain current;
- no gate has expired or been suspended;
- all pre-activation conditions are complete;
- the product revenue pool is unchanged or approved;
- approved distributable value remains valid;
- treasury and custody balances reconcile;
- payout assets and networks are available;
- contract addresses and network settings match the approved record;
- contract roles, signers, limits, and pause controls match the decision;
- snapshot or eligibility parameters are finalized;
- wallet and custody category rules are loaded correctly;
- claim or participation routes are active only for the approved scope;
- public notice and user instructions are published;
- support and escalation channels are staffed;
- monitoring and alerts are active;
- incident and pause authority are available;
- reporting and correction routes are operational;
- the effective event is recorded consistently across systems;
- and a final preflight receipt is retained.

If a material item differs from the approved evidence pack, activation should return to review.

## Activation States

| State | Meaning |
|---|---|
| Pre-design | No approved framework or scope exists |
| Design | Framework and scope are being developed |
| Gate preparation | Owners are preparing required evidence |
| Gate review | Evidence is under review |
| Remediation | One or more gates require correction |
| Gate-ready | Every required gate is ready or conditionally ready for the proposed scope |
| Approved for activation | Authorized decision exists, but the effective event has not occurred |
| Active for stated scope | The effective event occurred and the approved mechanism is operating |
| Narrowed | Active scope has been reduced |
| Paused | Some or all operation is temporarily stopped |
| Suspended | Readiness or operation is invalidated pending material review |
| Closing | No new participation is accepted while obligations are being completed |
| Closed | The defined activation period is complete |
| Retired | No new activation periods are intended under the framework version |
| Archived | Historical evidence and decisions remain retained but are not current |

`Gate-ready` should never be described as `Active`.

## Material Change Review

A material change should return the affected gates to review.

Material changes may include:

- a new product revenue pool;
- a new accounting period;
- a changed revenue-recognition method;
- a changed approved-value formula;
- a changed reserve policy;
- a changed payout asset;
- a new payout network;
- a new custody provider;
- a new wallet category;
- exchange or institutional custody support;
- a changed token condition;
- a changed snapshot method;
- a new contract;
- a contract upgrade;
- a network migration;
- a new jurisdiction;
- changed participant rights;
- changed claim or payout method;
- changed privacy or identity collection;
- changed operators or signers;
- changed audit or reporting method;
- a material incident;
- or a stronger public claim.

The change record should identify:

- previous scope;
- proposed scope;
- affected gates;
- new evidence;
- user and participant impact;
- claim and payout impact;
- public-reporting impact;
- required remediation;
- decision;
- effective time;
- and current status.

A prior activation decision should not be treated as blanket approval for materially different operation.

## Pause and Suspension Triggers

An active mechanism should pause or enter urgent review when a material issue affects:

- legal or jurisdiction support;
- participant rights or public terms;
- source revenue accuracy;
- approved distributable value;
- accounting or period-close integrity;
- treasury custody or reconciliation;
- payout-asset availability;
- contract security;
- privileged roles;
- network or provider reliability;
- snapshot integrity;
- eligibility logic;
- wallet or custody evidence;
- duplicate or abusive claims;
- privacy or identity protection;
- operator authority or support capacity;
- public-report accuracy;
- audit findings;
- sanctions or restricted-party controls;
- fraud;
- compromised wallets;
- payout failure;
- or continuity.

### Pause Scope

A pause record should identify whether it affects:

- new participation periods;
- snapshot execution;
- eligibility decisions;
- wallet verification;
- claim submission;
- claim review;
- payout authorization;
- payout execution;
- one product revenue pool;
- one wallet or custody class;
- one jurisdiction;
- one provider;
- one contract;
- one payout asset;
- the whole period;
- or the whole framework.

### Pause Record

The record should include:

- identifier;
- affected activation and framework version;
- trigger;
- effective time;
- affected scope;
- known impact;
- affected participants or wallets;
- affected value;
- temporary controls;
- evidence-preservation actions;
- claim and payout treatment;
- treasury and custody treatment;
- public communication;
- support route;
- investigation owner;
- remediation owner;
- reactivation conditions;
- reviewer;
- and current status.

A pause should preserve valid obligations and historical evidence.

## Remediation

Remediation should identify:

- root cause;
- affected gates;
- affected records;
- participant and treasury impact;
- corrective actions;
- preventive actions;
- responsible owners;
- deadlines or triggers;
- testing;
- reviewer;
- public correction;
- and closure evidence.

Possible remediation may include:

- recalculation;
- source-record correction;
- reserve adjustment;
- payout hold;
- transaction reversal where possible;
- corrected claim or eligibility status;
- contract patch or migration;
- role change;
- provider replacement;
- notice correction;
- participant outreach;
- support escalation;
- report restatement;
- or scope reduction.

A corrected component does not automatically reactivate the mechanism.

## Reactivation

Reactivation is a new authorized decision.

FUZE should:

1. identify the cause and affected scope;
2. complete remediation;
3. reconcile affected product revenue, approved value, treasury, eligibility, claims, payouts, and reports;
4. retest the affected workflow;
5. renew the affected gate decisions;
6. confirm unaffected gates remain current;
7. update the evidence pack;
8. update public status and correction history;
9. confirm operator and support readiness;
10. confirm pause and continuity controls;
11. authorize the revised scope;
12. set the effective event; and
13. retain the reactivation decision.

Material changes to rights, value, custody, contracts, jurisdictions, eligibility, claims, payouts, or public wording may require full gate review.

## Ongoing Gate Review and Expiry

Readiness can expire as products, laws, accounting treatment, contracts, operators, data, custody models, providers, jurisdictions, and market infrastructure change.

Review triggers may include:

- a new product revenue pool;
- a new accounting period;
- a new approved-value period;
- a new participation period;
- a contract upgrade;
- a network migration;
- a new custody class;
- a new provider;
- a new jurisdiction;
- a new participant type;
- a changed identity or tax process;
- a changed payout asset;
- a changed reserve policy;
- an operator or signer change;
- a material incident;
- a correction or report restatement;
- changed legal, accounting, tax, audit, privacy, or security advice;
- prolonged inactivity before activation;
- or the scheduled review date.

Every ready gate should show:

- effective date;
- next review date or trigger;
- expiry treatment;
- owner;
- and status if the review is not completed.

An expired gate should not remain represented as ready.

## Closure and Retirement

A participation period may close while some obligations remain under controlled treatment.

Closure review should confirm:

- no new eligible claims are accepted beyond the approved rules;
- product revenue and approved value are finalized or controlled;
- eligibility records are closed;
- claims are resolved or documented;
- payouts are completed or reserved;
- failed, returned, disputed, or unclaimed value has approved treatment;
- treasury and accounting records reconcile;
- corrections and appeals are resolved or controlled;
- final public reporting is published;
- records are retained appropriately;
- support for remaining obligations exists;
- and final gate statuses are closed or archived.

Framework retirement should additionally confirm:

- no new activation scope will use the retired version;
- contracts, portals, and providers are deprecated safely;
- custody and treasury treatment is complete;
- outstanding claims and payouts remain controlled;
- data retention and deletion are addressed;
- public communication is updated;
- historical evidence remains traceable;
- and the retirement decision is recorded.

## Public Gate Reporting

FUZE may publish a concise gate-status view without exposing private advice, personal identity, confidential workpapers, credentials, or exploitable security details.

| Public field | Example treatment |
|---|---|
| Activation identifier | Stable public-safe reference |
| Framework version | Current reviewed version |
| Mechanism status | Design, preparation, gate review, gate-ready, approved for activation, active, paused, closed, or retired |
| Scope | Product pool, period, wallet classes, network, claim route, payout route, and jurisdiction summary |
| Gate summary | Counts by ready, conditional, under review, remediation, suspended, expired, or not applicable |
| Blocking areas | Public-safe description of unresolved gates |
| Conditional areas | Public-safe limitations and deadlines or triggers |
| Approved-value status | Pending, approved, deferred, unavailable, or closed for the stated period |
| Effective record | Activation, pause, reactivation, closure, or retirement date and version |
| Reports | Links to public-safe value, eligibility, claim, payout, correction, or audit references |
| Changes | Material scope, rule, provider, contract, or status changes |
| Current-as-of date | Time to which the status applies |

Public reporting should distinguish:

- gate-ready;
- approved for activation;
- active;
- paused;
- closed;
- and retired.

A dashboard should identify the authoritative decision record and latest update.

### Gate Summary Limitations

A gate summary should not imply that:

- all underlying evidence is public;
- every review was independent;
- readiness applies beyond the named scope;
- approved value is claimable;
- a claim is payable;
- a payout is settled;
- or market access exists.

## Status and Evidence

This paper defines the activation-gate system.

It does not independently prove that any gate is ready or that participation is approved, active, claimable, payable, or settled.

| Status claim | Evidence direction |
|---|---|
| Gate register created | Versioned register, activation identifier, owners, scope, fields, and current entries |
| Gate in preparation | Assigned owner, evidence plan, dependencies, and current work record |
| Gate under review | Submitted evidence package, reviewer, review scope, and current status |
| Gate remediation required | Finding, affected scope, required action, owner, deadline or trigger, and review state |
| Gate conditionally ready | Pass criteria, outstanding condition, interim control, limitation, owner, deadline or trigger, and approval |
| Gate ready | Current evidence, exact scope, reviewer, decision, effective date, limitations, and expiry trigger |
| Gate expired | Prior decision, expiry trigger, affected scope, and renewal requirement |
| Gate suspended | Material issue, affected scope, temporary controls, remediation, and current status |
| Gate-ready mechanism | Every required gate ready or conditionally ready and every pre-activation condition complete |
| Approved for activation | Authorized decision, exact scope, effective event, notice, monitoring, pause, and review conditions |
| Active for stated scope | Effective event occurred, operating systems and notice match the decision, support and monitoring active, and public status current |
| Mechanism paused | Approved pause, affected scope, participant and value treatment, support, remediation, and communication |
| Mechanism reactivated | Completed remediation, renewed gates, updated evidence pack, authorized decision, and effective event |
| Activation closed | Final value, eligibility, claim, payout, correction, reporting, support, and archive treatment |
| Framework retired | No new activation, outstanding obligations controlled, systems deprecated, final governance decision, and public status |

The following do not independently establish gate readiness or activation:

- this paper;
- a gate name;
- a checklist;
- a policy draft;
- a legal discussion;
- an accounting spreadsheet;
- a treasury balance;
- an audit activity;
- a contract deployment;
- a snapshot;
- a dashboard;
- code;
- a repository;
- an internal test;
- a public announcement;
- a token balance;
- product use;
- Platform Credit activity;
- stablecoin payment;
- or token price activity.

## Readiness, Activation, Claim, Payout, Market, and Outcome Separation

The following remain separate:

- design;
- preparation;
- evidence submission;
- gate review;
- remediation;
- conditional readiness;
- readiness;
- gate-ready status;
- approval for activation;
- effective activation;
- active operation;
- product revenue;
- candidate distributable value;
- approved distributable value;
- snapshot completion;
- wallet control;
- eligibility;
- claim availability;
- claim submission;
- claim approval;
- payout authorization;
- payout submission;
- payout confirmation;
- payout settlement;
- product adoption;
- product revenue growth;
- DEX access;
- CEX access;
- liquidity;
- market price;
- and financial return.

Ready gates do not guarantee:

- activation;
- approved distributable value;
- wallet eligibility;
- an open claim;
- a payout;
- continued operation;
- exchange access;
- liquidity;
- price support;
- income;
- revenue share;
- or financial return.

## Public Boundary

This paper publishes the gate taxonomy, register model, status vocabulary, evidence standards, decision process, pre-activation controls, pause triggers, remediation, reactivation, expiry, closure, and public-reporting boundaries.

It does not publish or establish current:

- gate readiness;
- gate-ready status;
- activation approval;
- framework activation;
- product revenue pools;
- approved distributable value;
- wallet eligibility;
- snapshot block or time;
- supported jurisdictions;
- supported custody providers;
- claim availability;
- claim amount;
- payout asset;
- payout date;
- contract address;
- vault address;
- DEX activation;
- CEX application;
- CEX approval;
- liquidity;
- token demand;
- token price;
- income;
- revenue share;
- profitability;
- or financial return

unless those details are separately approved and supported by current evidence in the gate register, activation decision, activated notice, approved-value record, snapshot report, claim process, payout report, specialist paper, or public status record.

A gate can be narrowed, remediated, expired, suspended, closed, or retired as requirements and evidence change.

## Key Takeaways

- Participation activation requires a coordinated gate system and a separate authorized activation decision.
- Readiness is specific to the exact framework version, product pool, period, token rule, wallet and custody scope, jurisdiction, claim route, payout route, systems, operators, and public notice.
- A policy, calculation, treasury balance, deployed contract, vault, snapshot, audit activity, dashboard, announcement, or target date does not independently activate participation.
- Required gates cover legal and jurisdiction, accounting, product revenue, approved distributable value, treasury and custody, governance, audit, technical, eligibility, privacy, operations, reporting, and incident readiness.
- Each gate requires an owner, evidence, pass criteria, reviewer, status, dependencies, limitations, effective date, and expiry or reassessment trigger.
- `Gate-ready`, `approved for activation`, and `active for stated scope` are different states.
- Conditional readiness is allowed only with bounded risk, explicit controls, named ownership, deadlines or triggers, and clear consequences.
- Exceptions cannot replace fundamental legal authority, value reconciliation, treasury control, eligibility definition, privacy protection, safe technical operation, pause capability, or accurate public status.
- Material changes should return the affected gates to review rather than inherit approval automatically.
- Pause, remediation, reactivation, closure, and retirement require new records and accountable decisions while preserving valid obligations and historical evidence.
