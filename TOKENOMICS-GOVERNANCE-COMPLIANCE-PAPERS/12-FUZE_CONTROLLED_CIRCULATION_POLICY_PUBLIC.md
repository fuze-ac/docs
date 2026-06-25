# FUZE Controlled Circulation Policy

## Executive Summary

FUZE controlled circulation is the governance, custody, classification, authorization, reconciliation, and reporting system used to manage how FUZE token units move from fixed-supply allocation into controlled custody, commitment, vesting, claimability, release, operational deployment, circulation, return, correction, closure, or retirement.

The controlling sequence is:

```text
fixed supply and approved allocation
-> approved custody
-> planned use
-> authorized commitment
-> lock, vesting, eligibility, claim, release, or deployment condition
-> approved state transition
-> transaction or system execution
-> post-execution classification
-> allocation, custody, and circulation reconciliation
-> public-safe reporting
-> return, correction, pause, closure, or archive
```

Each state is separate.

An onchain transfer does not automatically create circulating supply.

A transfer between FUZE-controlled wallets may remain controlled custody.

A transfer into a vesting contract may remain locked or vesting.

A claimable allocation may remain outside circulation until claimed, depending on the approved methodology.

A transfer into a product, partner, incentive, liquidity, or market-operation system requires its own deployment classification.

A released amount does not automatically establish:

- unrestricted transferability;
- circulating-supply status;
- active liquidity;
- exchange access;
- market demand;
- price support;
- price appreciation;
- income;
- revenue share;
- or financial return.

Every controlled-circulation event should identify:

- fixed-supply category;
- allocation source;
- source custody;
- opening state;
- purpose;
- amount;
- recipient or destination class;
- applicable lock, vesting, claim, milestone, agreement, or program condition;
- authority;
- transaction or system evidence;
- resulting custody;
- resulting state;
- circulating-supply effect;
- reporting treatment;
- correction and return treatment;
- and current-as-of date.

The policy uses state-based accounting rather than wallet-only assumptions.

One wallet may contain token units belonging to different:

- allocation categories;
- commitments;
- restrictions;
- vesting schedules;
- programs;
- custody purposes;
- release states;
- and circulation classifications.

The ledger should therefore classify token lots or controlled balances by purpose and state instead of labeling an entire address with one status when the supporting records show multiple states.

This paper owns the common state machine and control framework for FUZE token circulation.

Category-specific release conditions remain governed by their primary papers, including:

- [FUZE Token Allocation Table](02-FUZE_TOKEN_ALLOCATION_TABLE_PUBLIC.md);
- [FUZE Token Release and Circulation Clarity](13-FUZE_TOKEN_RELEASE_AND_CIRCULATION_CLARITY_PUBLIC.md);
- [FUZE Vault and Reserve Policy](14-FUZE_VAULT_AND_RESERVE_POLICY_PUBLIC.md);
- [FUZE Vault-by-Vault Release Rules](15-FUZE_VAULT_BY_VAULT_RELEASE_RULES_PUBLIC.md);
- [FUZE Team Advisor Partner Vesting](19-FUZE_TEAM_ADVISOR_PARTNER_VESTING_PUBLIC.md); and
- [FUZE Liquidity and Listing Policy](21-FUZE_LIQUIDITY_AND_LISTING_POLICY_PUBLIC.md).

## Purpose of This Paper

This paper explains:

- the public controlled-circulation position;
- the token state model;
- allocation and custody integrity;
- state-transition authority;
- movement classes;
- movement requests;
- approval and pre-execution review;
- transaction execution and finality;
- circulation classification;
- batch and program controls;
- vesting, claim, partner, incentive, reserve, and market-operation boundaries;
- returns, recovery, and unused amounts;
- reclassification;
- corrections and restatements;
- pause, suspension, and incident response;
- supply and allocation reconciliation;
- public reporting;
- closure and archive;
- status and evidence requirements; and
- public limitations.

This paper does not replace:

- the fixed-supply allocation table;
- vault-specific custody rules;
- allocation-specific release rules;
- vesting agreements;
- grant or partner agreements;
- migration terms;
- community-round terms;
- incentive-program rules;
- claim instructions;
- liquidity or market-operation procedures;
- exchange-listing procedures;
- legal or tax advice;
- accounting policy;
- smart-contract specifications;
- private signer procedures;
- or the token risk register.

## Public Position

Controlled circulation is a supply-governance and evidence discipline.

Its purpose is to preserve allocation intent, prevent unauthorized or misclassified movement, distinguish custody movement from economic circulation, and support accurate public reporting.

It is not a mechanism for:

- controlling market price;
- guaranteeing liquidity;
- ensuring exchange listing;
- maintaining trading volume;
- supporting a price floor;
- creating token demand;
- guaranteeing resale;
- or producing financial return.

The complete FUZE token supply remains fixed at **500,000,000 FUZE** under the approved allocation model.

Every allocation, custody balance, committed amount, released amount, deployed amount, returned amount, corrected amount, and reported circulating amount should reconcile to that fixed supply without duplication.

## Core Principles

### Allocation Purpose Before Movement

Every movement should map to an approved allocation category and a permitted purpose.

Operational convenience is not sufficient justification for using one allocation category for another purpose.

### State Before Wallet Label

A wallet address is not a complete circulation classification.

Classification should reflect:

- beneficial and operational control;
- transfer restrictions;
- lock or vesting conditions;
- claim status;
- return rights;
- contractual restrictions;
- program purpose;
- and the approved reporting methodology.

### Authorization Before Execution

No controlled movement should rely solely on an informal message, unsigned spreadsheet, wallet screenshot, or verbal instruction.

### Execution Before Final Classification

A technically successful transaction must still be reconciled to the approved request before the resulting state is finalized.

### No Double Counting

The same token units should not be counted simultaneously as:

- available allocation balance;
- committed balance;
- released balance;
- deployed balance;
- claimable balance;
- circulating balance;
- returned balance;
- or another active state

unless the reporting model clearly treats one as a subset and prevents double counting.

### Correction Without Erasure

Corrections should preserve original transactions, decisions, and prior reports.

### Public Status Must Match Evidence

Terms such as `released`, `unlocked`, `vested`, `claimable`, `distributed`, `deployed`, and `circulating` should be used only with the exact supported meaning.

## Token State Model

| State | Evidence-backed meaning | What it does not establish |
|---|---|---|
| Allocated | Token units belong to an approved fixed-supply category. | Custody, commitment, release, or circulation |
| Custodied | Token units are held in an approved wallet, vault, contract, custodian, or account. | Allocation availability or circulation |
| Available within allocation | Units remain uncommitted and usable only for category-consistent approved purposes. | Transfer approval |
| Planned | Units appear in a proposal, forecast, or budget. | Commitment or recipient right |
| Committed | Units are reserved for an approved obligation, program, grant, partner, or process. | Vesting, claimability, release, or circulation |
| Locked | Transfer or release is restricted by contract, time, policy, agreement, or another enforceable condition. | Vesting completion or recipient control |
| Vesting | Units progress under an approved time, service, milestone, or hybrid schedule. | Release, claim, or circulation |
| Vested | The vesting condition has been satisfied for the stated units. | Automatic transfer, release, or circulation |
| Eligible | An approved recipient or wallet satisfies the stated qualification rules. | Claim completion or receipt |
| Claimable | An eligible recipient can complete an active claim process for the stated amount. | Claimed, transferred, or circulating status |
| Claimed | The recipient completed the required claim action. | Confirmed transfer or final settlement |
| Approved for release | Required release conditions and authority are complete. | Execution |
| Released | Units moved from the prior controlled state under an approved release. | Unrestricted circulation |
| Operationally deployed | Units entered an approved product, partner, incentive, liquidity, market, or ecosystem mechanism. | Ordinary holder circulation |
| Externally custodied | Units are held by a supported recipient, partner, exchange, custodian, or contract outside direct FUZE custody. | Unrestricted beneficial control or circulation |
| Circulating | Units are reasonably available in user or market circulation under the approved reporting method. | Liquidity, active trading, demand, or price support |
| Returned | Units moved back to approved category custody. | Immediate reuse or reclassification |
| Recovered | Units were recovered after error, cancellation, expiry, incident, or another approved event. | Restored availability without review |
| Suspended | Further action is paused pending review. | Cancellation or correction |
| Corrected | A later authorized record changes classification or amount while preserving history. | Erasure of the original event |
| Reclassified | Units move from one approved allocation purpose to another through formal authority. | Ordinary custody transfer |
| Closed | The relevant obligation, program, or movement is complete or controlled. | Availability for another purpose |
| Retired or inaccessible | Units are permanently or operationally unavailable under the approved treatment. | Burn unless the token contract and evidence establish destruction |
| Burned | Units are provably removed from usable supply under the approved method. | Reclassification or ordinary transfer |

A single token lot may transition through several states over time.

Not every token unit follows every state.

## State-Transition Ledger

FUZE should maintain a controlled state-transition ledger.

### Ledger Entry Fields

Each entry should include, where applicable:

1. transition identifier;
2. token and network reference;
3. allocation category;
4. token lot, commitment, program, or balance reference;
5. source custody;
6. destination custody;
7. opening state;
8. requested state;
9. final state;
10. amount;
11. purpose;
12. movement class;
13. recipient or destination class;
14. agreement, grant, migration, vesting, eligibility, claim, partner, program, or market reference;
15. lock or restriction;
16. request owner;
17. reviewers;
18. approval authority;
19. transaction or system reference;
20. execution time;
21. confirmation and finality status;
22. circulating-supply effect;
23. allocation-ledger effect;
24. custody-ledger effect;
25. program-ledger effect;
26. return or recovery treatment;
27. correction link;
28. public-report reference;
29. current status;
30. current-as-of date; and
31. closure state.

### Append-Oriented History

A state change should create a new linked entry.

The ledger should not silently overwrite:

- allocation source;
- amount;
- purpose;
- destination;
- transaction reference;
- prior state;
- or prior public classification.

## Allocation and Custody Integrity

### Allocation Record

Every controlled balance should map to:

- approved allocation category;
- total category amount;
- opening balance;
- available balance;
- planned amount;
- committed amount;
- locked amount;
- vesting amount;
- claimable amount;
- released amount;
- deployed amount;
- circulating classification;
- returned or recovered amount;
- correction amount;
- and closing balance.

### Custody Record

The custody record should identify:

- wallet, vault, contract, custodian, exchange, or provider;
- network;
- address or account reference;
- control class;
- allocation categories held;
- token lots or subledger method;
- signer or authority model;
- restrictions;
- monitoring;
- reconciliation frequency;
- and current status.

### Mixed-Purpose Wallets

Where one wallet holds more than one allocation category or token state, FUZE should use a reliable subledger.

Public reporting should not infer the entire wallet's purpose from one transaction or one label.

### Controlled Custody Transfer

A transfer remains a controlled custody movement when:

- allocation purpose remains unchanged;
- FUZE or the approved controlled entity retains control;
- restrictions remain enforceable;
- destination custody is approved;
- the transfer is fully reconciled;
- and no recipient or market availability is created.

## Permitted Movement Classes

### Custody Transfer

Moves token units between approved controlled wallets, vaults, contracts, custodians, or accounts without changing allocation purpose or economic availability.

Possible reasons include:

- wallet replacement;
- key rotation;
- multisig migration;
- custody-provider change;
- contract upgrade;
- network migration;
- segregation;
- consolidation;
- or operational restructuring.

### Lock or Vesting Deposit

Moves token units into an approved lock or vesting mechanism.

The movement may reduce available category custody while remaining non-circulating.

### Vesting Release

Recognizes or executes an amount under an approved vesting rule.

Vested, releasable, released, received, and circulating remain separate states.

### Claim Funding

Places token units into an approved migration, community, incentive, grant, or other claim process.

Funding the process does not establish individual claim completion.

### Claim or Eligibility Release

Transfers an approved amount to an eligible recipient after the active claim or release requirements are satisfied.

### Program Deployment

Moves token units into an approved:

- product utility;
- community program;
- grant;
- incentive;
- education or contributor program;
- event;
- partnership;
- ecosystem initiative;
- or another category-consistent mechanism.

### Partner Deployment

Moves token units under an approved partnership, milestone, grant, service, distribution, integration, or ecosystem agreement.

Partner custody, lock, vesting, use, transfer, return, and reporting should be defined.

### Reserve or Treasury Deployment

Uses an approved reserve or treasury category for a permitted strategic, continuity, partnership, emergency, product, or operational purpose.

### Liquidity or Market-Operation Deployment

Moves token units into an approved liquidity, venue, market-making, market-structure, or listing-support context.

These units require specialist classification and should not be treated automatically as ordinary circulating holder supply.

### Return

Moves unused, cancelled, expired, unclaimed, or otherwise returnable units back to the appropriate controlled category.

### Recovery

Moves units back after an erroneous, unauthorized, compromised, disputed, or failed event where recovery is possible.

### Reclassification

Changes the approved allocation purpose through formal governance and updated fixed-supply reporting.

### Burn or Permanent Removal

Moves units into a provably unusable state only when the approved token method and evidence support permanent removal.

A transfer to an unfamiliar or inaccessible address should not be labeled a burn without proof.

## Movement Request

Before execution, the movement request should identify:

| Request field | Required content |
|---|---|
| Movement identifier | Stable reference |
| Token identity | Network and canonical FUZE contract |
| Allocation source | Exact category and available balance |
| Source custody | Wallet, vault, contract, custodian, or account |
| Opening state | Current evidence-backed classification |
| Purpose | Approved category-consistent reason |
| Movement class | Custody, lock, vesting, claim, program, partner, reserve, market, return, recovery, reclassification, or burn |
| Destination | Address, contract, custodian, program, venue, or recipient class |
| Destination ownership or control | FUZE-controlled, recipient-controlled, shared, custodial, contractual, market, or other approved class |
| Amount | FUZE quantity, precision, and batch detail |
| Conditions | Lock, vesting, milestone, eligibility, claim, agreement, program, venue, return, or recovery rules |
| Requested final state | Intended post-movement classification |
| Circulation effect | Increase, decrease, no change, pending classification, or specialist treatment |
| Timing | Earliest execution, deadline, period, timelock, or block condition |
| Evidence | Agreement, allocation, governance, vesting, eligibility, claim, partner, treasury, market, or technical records |
| Restrictions | Jurisdiction, custody, transfer, use, sale, return, disclosure, or other controls |
| Request owner | Responsible business or program owner |
| Reporting treatment | Private, permissioned, aggregate public, or onchain public treatment |
| Return and correction treatment | Expected handling of unused, failed, cancelled, or incorrect amounts |

An incomplete request remains `Pending` and should not be executed through informal instruction.

## Movement Status Vocabulary

| Status | Meaning |
|---|---|
| Draft | Request is being prepared |
| Pending evidence | Required source, purpose, destination, amount, or condition evidence is incomplete |
| Under review | Reviewers are evaluating the request |
| Remediation required | Material issues must be corrected |
| Approved | Business and policy approval exists, but execution may remain pending |
| Treasury authorized | Exact transaction parameters and source custody are authorized |
| Timelocked | Execution is delayed by an approved timelock or notice condition |
| Ready for execution | Final pre-execution checks are complete |
| Submitted | Transaction or system instruction has been sent |
| Confirmed | Required network or provider confirmation exists |
| Reconciled | Transaction, allocation, custody, program, and supply records agree |
| Classified | Final token state and circulation effect are recorded |
| Partially completed | Only part of the approved movement completed |
| Failed | Execution did not complete as approved |
| Returned | Token units returned to approved custody |
| Suspended | Further action is paused |
| Corrected | Later authorization changes the record while preserving history |
| Cancelled | Request is withdrawn or authority ends before completion |
| Closed | Movement and remaining obligations are complete or controlled |
| Archived | Historical record is retained but not current |

`Approved`, `submitted`, `confirmed`, `reconciled`, and `circulating` are different states.

## Authorization Framework

Authorization should reflect the movement's amount, allocation, purpose, destination, irreversibility, market impact, security risk, and public significance.

### Review Areas

Applicable review may include:

- allocation-purpose confirmation;
- available and uncommitted balance;
- existing commitment and double-use check;
- vault or custody authority;
- vesting status;
- eligibility or claim status;
- milestone or agreement status;
- legal and compliance review;
- accounting and tax review;
- treasury review;
- jurisdiction review;
- technical destination review;
- smart-contract review;
- security review;
- partner or venue review;
- public communication readiness;
- and supply-reporting readiness.

### Approval Layers

The policy may use:

- individual movement approval;
- approved batch approval;
- approved program budget with per-item controls;
- threshold-based approval;
- multisig approval;
- timelock;
- governance decision;
- emergency authority;
- or another approved model.

Approval of a high-level program budget does not automatically authorize every transfer unless the operating policy expressly defines delegated limits and item-level evidence.

### Separation of Duties

Where proportionate, the following roles should be distinguishable:

- requester;
- business or program owner;
- allocation reviewer;
- treasury reviewer;
- legal, compliance, accounting, tax, or specialist reviewer;
- transaction preparer;
- signer or executor;
- reconciler;
- supply classifier;
- and public reporter.

One person should not independently request, approve, execute, classify, and reconcile a sensitive token movement.

## Pre-Execution Review

Immediately before execution, FUZE should confirm:

- canonical FUZE token and network;
- source allocation;
- source custody;
- opening state;
- available and uncommitted balance;
- existing program, grant, vesting, claim, or partner commitments;
- approved purpose;
- movement class;
- destination address and control class;
- destination contract and role configuration where applicable;
- amount and decimals;
- batch total;
- lock, vesting, claim, milestone, or agreement conditions;
- duplicate-release or duplicate-payment check;
- sanctions, restriction, incident, or pause status where applicable;
- signer, multisig, threshold, and timelock configuration;
- expected resulting custody;
- expected final state;
- expected circulation effect;
- return or correction path;
- and current approval validity.

A material difference should return the request to review.

## Execution and Technical Evidence

### Execution Record

The execution record should include:

- movement identifier;
- approved request version;
- source address or account;
- destination address or account;
- network;
- canonical FUZE contract;
- amount;
- transaction hash or system reference;
- block or confirmation context;
- fee amount and asset where relevant;
- executor or signer roles;
- execution time;
- timelock or governance reference;
- confirmation and finality status;
- batch manifest where applicable;
- exception notes;
- and current status.

### Technical Success Is Not Final Classification

A successful transaction proves that the network or system accepted the movement.

It does not independently prove:

- correct allocation source;
- correct business purpose;
- recipient eligibility;
- final vesting status;
- valid claim completion;
- correct circulating classification;
- or final reconciliation.

### Contract Deployment

Where tokens enter a contract, the record should identify:

- contract purpose;
- deployment or verification reference;
- admin and upgrade powers;
- withdrawal or return rights;
- lock and transfer behavior;
- accounting method;
- circulation methodology;
- incident controls;
- and current status.

## Circulating-Supply Classification

FUZE should use a documented and versioned methodology to determine circulating supply.

The methodology should identify:

- measurement date or block;
- network and canonical token contract;
- total supply reference;
- allocation categories;
- controlled-wallet registry;
- custody classes;
- lock and vesting treatment;
- claimable and unclaimed treatment;
- exchange and omnibus treatment;
- contract balances;
- liquidity and market-operation treatment;
- partner and program restrictions;
- bridge or wrapped treatment;
- returned and recovered amounts;
- inaccessible or burned amounts;
- pending classifications;
- corrections;
- and current-as-of date.

### Classification Factors

Factors may include:

- direct or indirect FUZE control;
- beneficial control;
- transferability;
- lock or vesting restriction;
- contractual restriction;
- recipient claim or custody status;
- return or recovery rights;
- operational deployment;
- ability to trade or transfer;
- venue custody;
- market-maker custody;
- bridge or contract mechanics;
- and the approved reporting standard.

### Illustrative Classification Examples

| Event | Likely treatment under a documented method |
|---|---|
| Treasury wallet A to treasury wallet B | Controlled custody transfer; no circulation increase |
| Vault to vesting contract | Released from vault custody but still locked or vesting; not automatically circulating |
| Vesting completion without transfer | Vested state; not automatically released or circulating |
| Claim program funded | Operational deployment or claim funding; not automatically recipient circulation |
| Claimable but unclaimed amount | Treatment depends on the published methodology |
| Claimed and transferred to self-custody recipient | May enter circulation if no continuing restriction applies |
| Partner wallet with contractual lock and return rights | Externally custodied or partner-deployed; not automatically ordinary circulation |
| Exchange hot or cold wallet | Requires exchange-custody and beneficial-availability analysis |
| Liquidity pool | Market-operation deployment requiring specialist classification |
| Market-maker inventory | Operational market inventory, not automatically ordinary holder circulation |
| Returned unused program balance | Returned to controlled category custody; may reduce deployed or circulating classification |
| Burn address with verifiable permanent inaccessibility | Burned or removed from usable supply under the approved method |

Detailed supply terminology appears in [FUZE Token Release and Circulation Clarity](13-FUZE_TOKEN_RELEASE_AND_CIRCULATION_CLARITY_PUBLIC.md).

## Allocation-Specific Boundaries

The common state machine applies across categories, but each allocation uses its own purpose and release rules.

### Team and Advisor Allocations

Team and advisor token treatment should preserve:

- agreement;
- role or contribution basis;
- allocation source;
- vesting;
- cliff;
- service or milestone treatment;
- termination;
- cancellation;
- release;
- custody;
- transfer restrictions;
- and reporting.

Stablecoin compensation remains separate.

### Community Participation Allocation

Community allocation movements should preserve:

- approved round or program;
- participant route;
- eligibility;
- decision;
- allocation;
- vesting or lock;
- claim;
- release;
- and reporting.

Community membership or product use alone does not authorize release.

### BOARD / Surfboard Migration

Migration movements should preserve:

- legacy evidence;
- eligibility;
- conversion basis;
- wallet or custody verification;
- allocation source;
- claim;
- release;
- correction;
- and closure.

### Holder Incentives

Incentive movements should preserve:

- program purpose;
- budget;
- qualification;
- measurement period;
- anti-abuse controls;
- claim or direct-delivery method;
- release;
- and reporting.

Token holding alone does not authorize an incentive release unless the active program says so.

### Ecosystem Growth and Partnerships

Partner movements should preserve:

- partner identity and authority;
- agreement;
- purpose;
- milestone;
- lock or vesting;
- custody;
- permitted use;
- onward-transfer limits;
- return rights;
- reporting;
- and termination treatment.

### Liquidity and Market-Making Allocation

Market-related movements should preserve:

- approved venue or counterparty;
- purpose;
- custody;
- inventory limits;
- strategy authority;
- spread and depth objectives where applicable;
- fees;
- risk controls;
- return and recovery rights;
- proof and reporting;
- and circulation classification.

They do not create a guaranteed price or liquidity outcome.

### Reserve Allocations

Reserve movements should preserve:

- reserve purpose;
- trigger;
- approval;
- amount;
- custody;
- temporary or permanent use;
- return treatment;
- reclassification rules;
- and reporting.

## Batch and Program Controls

### Batch Manifest

A batch release should contain item-level records for:

- destination;
- destination class;
- amount;
- allocation source;
- purpose;
- eligibility, vesting, milestone, or agreement reference;
- intended final state;
- circulation effect;
- validation status;
- and exception state.

### Batch Record

The batch record should additionally identify:

- batch identifier;
- program identifier;
- item count;
- total amount;
- source custody;
- allocation category;
- preparation time;
- reviewers;
- approvers;
- transaction or contract references;
- successful items;
- failed items;
- returned items;
- corrected items;
- closing balance;
- and reconciliation status.

A batch total alone is not sufficient evidence for individual recipients or destinations.

### Program Ledger

A program should track:

- approved budget;
- available amount;
- planned amount;
- committed amount;
- locked amount;
- claim-funded amount;
- released amount;
- deployed amount;
- circulating classification;
- failed amount;
- returned amount;
- cancelled amount;
- corrected amount;
- and remaining amount.

### Partial Use

A program may close or pause before its full approved budget is used.

Unused token units retain their original allocation purpose unless a formal reclassification is approved.

## Returns, Recovery, and Unused Amounts

Returned or recovered token units should map back to the correct:

- allocation category;
- custody;
- token lot;
- program;
- commitment;
- and state.

### Return Record

The record should identify:

1. original movement;
2. original allocation;
3. original recipient, program, contract, or venue class;
4. reason for return;
5. amount;
6. source and destination;
7. transaction or system evidence;
8. continuing obligations;
9. restrictions;
10. revised program balance;
11. revised allocation balance;
12. revised circulation classification;
13. reviewer;
14. approval;
15. public-report effect;
16. current status; and
17. closure.

### Reuse After Return

Returned units should not be reused automatically when:

- the original program remains disputed;
- legal or accounting review is pending;
- the source category is unclear;
- the units came from an exchange, partner, bridge, liquidity, or market context;
- a security incident occurred;
- or the public classification requires correction.

## Reclassification

Reclassification changes allocation purpose.

It is different from a custody transfer, return, or ordinary state transition within one category.

### Reclassification Proposal

The proposal should identify:

- source category;
- destination category;
- amount;
- percentage of each affected category;
- purpose;
- reason the destination category is required;
- alternatives considered;
- existing commitments;
- affected programs and stakeholders;
- legal, accounting, treasury, governance, and specialist reviews;
- updated vault and custody treatment;
- updated fixed-supply allocation table;
- updated circulation method if affected;
- effective date;
- public communication;
- and correction of prior references.

### Reconciliation Requirement

After reclassification:

```text
sum of all approved allocation categories = 500,000,000 FUZE
```

The reclassification should not change fixed total supply unless a separately approved and technically valid supply event occurs.

## Corrections and Restatements

Corrections may address:

- wrong allocation source;
- wrong amount;
- wrong destination;
- duplicate movement;
- missing movement;
- unauthorized movement;
- incorrect vesting state;
- incorrect eligibility or claim state;
- incorrect program balance;
- incorrect custody classification;
- incorrect circulating classification;
- wrong transaction reference;
- failed batch item;
- returned or recovered amount;
- compromised wallet or contract;
- or public-report error.

### Correction Record

A correction record should identify:

1. correction identifier;
2. original movement or report;
3. affected allocation;
4. affected token lot or balance;
5. affected amount;
6. error type;
7. evidence;
8. actual custody and state;
9. corrected custody and state;
10. allocation effect;
11. circulation effect;
12. program, partner, claim, vesting, or market effect;
13. recovery or return action;
14. reviewer;
15. approval;
16. revised ledger entries;
17. revised public report;
18. current status; and
19. closure.

### Restatement

A material supply or circulation correction may require restatement.

A restatement should:

- preserve the prior report;
- identify the incorrect method or record;
- show the revised amount;
- explain the affected period;
- identify the authority;
- and update linked public materials.

## Pause, Suspension, and Incident Response

Movement should pause or enter urgent review when a material issue affects:

- custody security;
- signer or multisig integrity;
- contract behavior;
- allocation authority;
- available balance;
- vesting or lock logic;
- eligibility or claim integrity;
- batch manifest integrity;
- partner or venue behavior;
- bridge or custody provider;
- liquidity or market operation;
- legal or jurisdiction support;
- sanctions or restriction status;
- treasury reconciliation;
- supply classification;
- or public reporting accuracy.

### Pause Scope

A pause may apply to:

- one movement;
- one batch;
- one program;
- one allocation category;
- one vault;
- one contract;
- one partner;
- one venue;
- one claim route;
- one custody provider;
- one network;
- one movement class;
- or all token movements.

### Incident Record

The record should identify:

- incident identifier;
- affected allocation and custody;
- affected movements;
- affected amount;
- detection time;
- known impact;
- actual onchain or system state;
- containment;
- pause scope;
- signer, contract, custody, or venue actions;
- recovery options;
- affected recipients or stakeholders;
- supply and circulation effect;
- public communication;
- root cause;
- remediation;
- reviewer;
- reactivation conditions;
- and closure.

### Reactivation

Reactivation should require:

- issue containment;
- corrected configuration or records;
- affected-balance reconciliation;
- renewed authority;
- testing where applicable;
- updated public status;
- and documented effective time.

Fixing one technical issue does not automatically reactivate every affected movement or program.

## Supply and Allocation Reconciliation

FUZE should reconcile controlled circulation across:

```text
fixed token supply
<-> allocation table
<-> vault and custody balances
<-> commitments and vesting records
<-> claim and program ledgers
<-> partner and market-operation balances
<-> onchain balances and transactions
<-> returns, recoveries, burns, and corrections
<-> public supply and circulation reports
```

### Core Reconciliation Identity

At a point in time:

```text
allocated controlled balances
+ externally custodied or deployed balances
+ circulating balances
+ verifiably burned or permanently removed balances
+ pending-classification balances
= fixed total supply
```

The exact categories should be mutually exclusive under the reporting method.

### Allocation Reconciliation

For each category:

```text
opening category balance
+ approved inward reclassification or return
- approved outward reclassification
- releases, deployments, or burns under the category
+ recoveries and corrections
= closing category balance
```

Substates should reconcile without double counting.

### Pending Classification

A balance should enter `Pending classification` when evidence is insufficient to determine the final state.

Pending balances should be:

- visible to authorized reviewers;
- excluded from stronger public claims;
- assigned an owner;
- given a resolution trigger;
- and corrected promptly.

## Public Reporting

A public controlled-circulation report may include:

- reporting period;
- current-as-of block or time;
- total supply;
- allocation-table version;
- methodology version;
- opening and closing balances by state;
- custody transfers excluded from circulation change;
- planned and committed amounts at an aggregate level where appropriate;
- locked, vesting, vested, eligible, claimable, claimed, released, deployed, returned, recovered, burned, and circulating classifications;
- movements by allocation and movement class;
- program and partner deployment at a public-safe level;
- liquidity and market-operation balances under specialist classifications;
- reclassifications;
- pending classifications;
- corrections and restatements;
- transaction, governance, or report references;
- limitations;
- and current status.

### Methodology Disclosure

The report should identify:

- source systems;
- network and canonical token contract;
- measurement date or block;
- wallet and custody registry treatment;
- exchange and omnibus treatment;
- lock and vesting treatment;
- claimable and unclaimed treatment;
- liquidity and market-operation treatment;
- bridge and wrapped treatment;
- return and burn treatment;
- corrections;
- methodology changes;
- and limitations.

### Point-in-Time Versus Period Movement

Reports should distinguish:

- opening balance;
- period inflow;
- period outflow;
- state transition;
- closing balance;
- and cumulative amount.

A cumulative release amount should not be presented as current circulating supply.

### Public Privacy and Security Boundary

Public reporting should not expose:

- personal identity linked to a wallet;
- private recipient agreements;
- private vesting terms where not approved;
- private partner terms;
- private market strategy;
- credentials;
- private keys;
- recovery material;
- signer identities where not approved;
- exact security procedures;
- or exploitable treasury patterns.

## Separation from Adjacent Systems

| System or process | Primary role | Why it remains separate |
|---|---|---|
| Controlled circulation | Governs FUZE token states, movements, custody, classification, and reporting | Common supply-governance framework |
| Token allocation table | Defines fixed category amounts | Does not itself authorize movement |
| Vault and reserve policy | Defines custody and reserve purposes | Custody does not equal release or circulation |
| Vault-by-vault release rules | Defines category-specific release conditions | Specialist conditions remain category-specific |
| Vesting | Defines time, service, milestone, or hybrid release progression | Vesting completion does not equal circulation |
| Claim process | Defines recipient eligibility and claim action | Claimable, claimed, transferred, and circulating remain separate |
| Stablecoin compensation | Settles approved business obligations | Does not change FUZE token supply or circulation |
| Platform Credits | Product-consumption units | Not FUZE token and not part of circulating supply |
| Wallet-based participation | Activation-gated eligibility, claim, and payout process | Stablecoin or approved-value payout does not change FUZE token circulation unless FUZE token is separately used |
| Liquidity and market operations | Supports approved market structure | Requires separate custody, venue, inventory, risk, and reporting treatment |
| DEX and CEX access | Separate market-access states | Circulation does not establish listing or active liquidity |

## Status and Evidence

This paper defines the controlled-circulation model.

It does not independently prove that any allocation, vault, vesting event, claim process, release, deployment, liquidity transfer, reclassification, burn, or circulating-supply figure is currently active or correct.

| Status claim | Evidence direction |
|---|---|
| Allocation recorded | Approved allocation table, category amount, authority, version, and fixed-supply reconciliation |
| Custody recorded | Wallet, vault, contract, custodian, control class, allocation mapping, and balance evidence |
| Tokens planned | Proposal, budget, purpose, owner, amount, and non-commitment status |
| Tokens committed | Approved obligation or program, amount, restrictions, authority, and ledger entry |
| Tokens locked | Contract, policy, agreement, amount, start, end or condition, custody, and status |
| Tokens vesting | Schedule, beneficiary class, amount, service or milestone basis, custody, and calculation |
| Tokens vested | Schedule calculation, satisfied condition, amount, reviewer, and current state |
| Tokens claimable | Active process, eligibility, amount, claim route, period, and funding evidence |
| Tokens claimed | Claim action, recipient or wallet reference, amount, time, and status |
| Tokens approved for release | Release condition, authority, amount, source, destination, and instruction |
| Tokens released | Transaction or system evidence, confirmation, allocation effect, custody effect, and state classification |
| Tokens operationally deployed | Program, partner, contract, incentive, reserve, liquidity, or market reference and restrictions |
| Tokens circulating | Approved methodology, measurement date or block, wallet and custody treatment, exclusions, and report |
| Tokens returned | Original movement, reason, amount, transaction, destination custody, allocation, and revised state |
| Tokens burned | Canonical token evidence, permanent inaccessibility or supply reduction method, authority, and report |
| Allocation reclassified | Governance decision, source and destination categories, amount, updated table, and fixed-supply reconciliation |
| Report corrected | Original report, error, corrected method or records, authority, revised values, and current version |

The following do not independently establish circulation status:

- this paper;
- a wallet label;
- a transfer hash;
- a wallet screenshot;
- a vesting schedule draft;
- a program budget;
- a claim announcement;
- a contract deployment;
- an exchange deposit;
- a liquidity-pool balance;
- code;
- a repository;
- a partner discussion;
- or token price activity.

## Allocation, Release, Circulation, Market, and Outcome Separation

The following remain separate:

- fixed supply;
- allocation;
- custody;
- available allocation balance;
- planned use;
- commitment;
- lock;
- vesting;
- vested status;
- eligibility;
- claimability;
- claim completion;
- release approval;
- transaction execution;
- release;
- operational deployment;
- external custody;
- circulating-supply classification;
- exchange deposit;
- DEX access;
- CEX application;
- CEX approval;
- listing;
- liquidity;
- depth;
- spread;
- volume;
- token demand;
- market price;
- income;
- revenue share;
- and financial return.

A token release or circulation increase does not guarantee:

- recipient sale;
- exchange access;
- listing;
- market liquidity;
- stable spread;
- trading volume;
- token demand;
- price support;
- price appreciation;
- income;
- revenue share;
- or financial return.

## Public Boundary

This paper publishes the common allocation, custody, state-transition, movement, authorization, circulation-classification, reconciliation, correction, pause, and reporting framework.

It does not publish or establish current:

- vault addresses;
- custody addresses;
- signer identities;
- release schedules;
- beneficiary identities;
- vesting terms;
- claim windows;
- partner allocations;
- incentive budgets;
- market-maker inventories;
- liquidity deployments;
- exchange deposits;
- circulating-supply amount;
- DEX activation;
- CEX application;
- CEX approval;
- listing;
- liquidity;
- depth;
- spread;
- volume;
- token demand;
- token price;
- income;
- revenue share;
- profitability;
- or financial return

unless those details are separately approved and supported by current evidence in an allocation record, vault policy, release rule, vesting record, claim process, partner record, market-operation report, circulation report, specialist paper, or public status record.

Specific token movements remain subject to their controlling allocation, custody, vesting, claim, partner, migration, community, incentive, reserve, liquidity, market, governance, legal, accounting, tax, technical, security, and reporting requirements.

## Key Takeaways

- Controlled circulation is the governance and evidence system for how FUZE token units change allocation, custody, restriction, release, deployment, and circulation states.
- An onchain transfer does not automatically create circulating supply.
- Allocation, custody, planning, commitment, lock, vesting, vested status, eligibility, claimability, release, deployment, external custody, and circulation are separate states.
- The same wallet may contain multiple allocation categories and token states, so state-based subledgers are more reliable than wallet-only labels.
- Every movement should have a category-consistent purpose, request, evidence, authority, destination, amount, execution record, final state, circulation effect, and reconciliation.
- Batch releases require item-level manifests and program-ledger reconciliation.
- Returned or recovered token units should map back to the correct allocation, custody, token lot, and state before reuse.
- Reclassification changes allocation purpose and requires formal governance plus continued reconciliation to the fixed 500,000,000 FUZE supply.
- Corrections and restatements should preserve original transactions and prior public reports.
- Token release, circulation, liquidity deployment, exchange access, market demand, price support, income, revenue share, and financial return remain separate and must not be implied from one another.
