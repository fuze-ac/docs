# FUZE Vault and Reserve Policy

## Executive Summary

FUZE vaults are controlled custody, account, contract, wallet, sub-account, or ledger structures established for a defined asset, allocation, obligation, program, operating function, recovery purpose, or evidence function.

FUZE reserves are approved designations of resources retained for a defined future obligation, continuity need, risk response, program, or strategic purpose.

A vault and a reserve are related but different concepts.

A vault describes where and how assets or records are controlled.

A reserve describes why resources are being retained and what conditions govern their use.

The controlling lifecycle is:

```text
approved purpose and classification
-> establishment record
-> custody and authority design
-> technical or provider setup
-> verification and activation
-> funding or designation
-> ongoing custody, commitment, and reserve tracking
-> approved movement or utilization
-> reconciliation and review
-> suspension, recovery, reclassification, replenishment, or closure
-> public-safe reporting and archive
```

Each state is separate.

A vault address does not by itself establish:

- allocation purpose;
- beneficial ownership;
- reserve status;
- available balance;
- release authority;
- circulation status;
- claimability;
- participant eligibility;
- liquidity;
- or market availability.

A reserve label does not itself authorize:

- spending;
- token release;
- stablecoin payment;
- partner deployment;
- claim funding;
- liquidity deployment;
- reclassification;
- or market activity.

Every active vault or reserve should identify:

- stable identifier;
- classification;
- asset, token, allocation, or record scope;
- mandate;
- permitted uses;
- prohibited uses;
- legal or beneficial-control context;
- custody model;
- authority and signer model;
- funding source;
- opening balance or capacity;
- commitments;
- restrictions;
- movement and utilization controls;
- reconciliation method;
- incident and emergency controls;
- review cadence;
- public-reporting treatment;
- closure conditions;
- status;
- and current-as-of date.

The same vault may contain more than one asset, allocation, token lot, commitment, or reserve only when an approved subledger preserves those distinctions without double counting.

The same reserve may be physically held across more than one vault only when custody, amount, obligation, and utilization records remain reconciled.

This paper owns FUZE's common policy for vault establishment, reserve designation, classification, custody, authority, segregation, funding, movement, utilization, reconciliation, monitoring, provider and signer changes, incidents, recovery, replenishment, reclassification, public visibility, closure, and archive.

Allocation-specific release conditions remain governed by [FUZE Vault-by-Vault Release Rules](15-FUZE_VAULT_BY_VAULT_RELEASE_RULES_PUBLIC.md).

Token-state and circulation treatment remain governed by [FUZE Controlled Circulation Policy](12-FUZE_CONTROLLED_CIRCULATION_POLICY_PUBLIC.md) and [FUZE Token Release and Circulation Clarity](13-FUZE_TOKEN_RELEASE_AND_CIRCULATION_CLARITY_PUBLIC.md).

## Purpose of This Paper

This paper explains:

- the public vault-and-reserve position;
- vault and reserve definitions;
- classification models;
- establishment records;
- custody and authority design;
- segregation and subledger requirements;
- funding and designation;
- commitments and availability;
- movement and utilization controls;
- stablecoin, token, fiat, provider, and record treatment;
- vault and reserve status vocabulary;
- reconciliation and review;
- signer, authority, address, contract, and provider changes;
- suspension, incident, recovery, and emergency treatment;
- replenishment and reclassification;
- public reporting and visibility;
- closure and archive;
- status and evidence requirements; and
- public limitations.

This paper does not replace:

- the token allocation table;
- vault-specific release rules;
- controlled-circulation approvals;
- vesting agreements;
- claim instructions;
- reserve-use approvals;
- treasury policy;
- bank, payment-provider, custodian, or exchange agreements;
- stablecoin issuer terms;
- smart-contract specifications;
- private signer and key-management procedures;
- employment, vendor, partner, or grant agreements;
- accounting or tax policy;
- legal advice;
- liquidity or listing procedures;
- or the token risk register.

## Public Position

Vaults and reserves organize custody, authority, purpose, and evidence.

They do not make every balance available for use.

FUZE should distinguish:

- asset ownership;
- custody location;
- operational control;
- beneficial purpose;
- allocation category;
- reserve designation;
- commitment;
- lock or restriction;
- release authority;
- deployment;
- circulation;
- and market availability.

A public vault balance should always state:

- asset or unit;
- measurement time or block;
- vault function;
- status;
- restrictions;
- and methodology.

A public reserve amount should always state:

- reserve purpose;
- unit;
- current status;
- commitment treatment;
- utilization authority;
- and review date.

Vault and reserve reporting should not imply:

- guaranteed funding;
- guaranteed token release;
- guaranteed compensation;
- guaranteed participant payout;
- guaranteed liquidity;
- price support;
- income;
- revenue share;
- or financial return.

## Core Definitions

### Vault

A vault is an approved structure used to hold, control, segregate, administer, or evidence assets or records.

A vault may be implemented through:

- multisignature wallet;
- smart contract;
- timelocked contract;
- role-controlled contract;
- self-custody wallet;
- institutional custodian;
- exchange or provider account;
- bank or payment account;
- segregated sub-account;
- restricted internal ledger;
- or another approved custody or record system.

### Reserve

A reserve is an approved designation of assets, value, capacity, or token units retained for a defined future need.

A reserve should identify:

- purpose;
- basis;
- amount or sizing method;
- custody;
- owner;
- restrictions;
- utilization trigger;
- approval path;
- review cadence;
- release or closure treatment;
- and reporting treatment.

### Vault Balance

The asset quantity or record amount held in the vault at the stated measurement point.

A vault balance can contain:

- available amount;
- committed amount;
- locked amount;
- reserved amount;
- pending movement;
- disputed amount;
- returned amount;
- or another controlled substate.

### Available Balance

The amount not currently committed, restricted, disputed, pending, suspended, or otherwise unavailable under the vault mandate.

Available does not mean approved for movement.

### Committed Balance

The amount reserved for an approved obligation, program, recipient class, contract, claim process, partner, expense, release, or deployment.

Committed does not mean executed or released.

### Restricted Balance

The amount subject to lock, vesting, contract, policy, legal, custody, jurisdiction, security, incident, provider, or other material restriction.

### Reserve Capacity

The amount still available within the approved reserve after current commitments and approved pending uses.

```text
custodied reserve balance
- committed reserve amount
- approved pending utilization
= uncommitted reserve capacity
```

### Recovery Vault

A vault used to isolate returned, disputed, compromised, erroneous, recovered, unsupported, or otherwise quarantined assets pending final disposition.

### Evidence Registry

A controlled record structure holding hashes, references, labels, approvals, report identifiers, or proof records rather than economic assets.

## Core Principles

### Purpose Before Funding

A vault or reserve requires an approved mandate before receiving material production assets or being represented as active.

### Segregation by Meaning

Assets or records with materially different allocation, ownership, restriction, obligation, release, participant, market, or reporting treatment should be physically or logically segregated.

### Least Necessary Authority

Authority should be limited by:

- role;
- asset;
- purpose;
- amount;
- destination;
- time;
- transaction class;
- and emergency condition.

### Separation of Duties

Where proportionate, proposal, approval, preparation, signing, execution, reconciliation, classification, and reporting should not be controlled by one person.

### Evidence-Linked Activity

Every material establishment, funding, designation, commitment, movement, use, return, correction, reclassification, replenishment, or closure should connect to durable evidence.

### No Double Counting

The same assets should not be counted simultaneously as:

- available;
- committed;
- reserve capacity;
- deployed;
- released;
- claim-funded;
- circulating;
- returned;
- or another mutually exclusive active state.

### Reversible Administration Where Possible

Administrative mistakes should have defined pause, replacement, return, quarantine, correction, or recovery routes.

Blockchain finality can make recovery impossible, so pre-execution controls remain essential.

### Public-Safe Transparency

Public reporting should explain purpose, status, balance, restrictions, movements, and review while protecting personal identity, private agreements, credentials, security design, and exploitable treasury information.

## Vault Classification

A vault may be classified by asset, allocation, custody, and function.

| Vault class | Primary function | Required context |
|---|---|---|
| Token allocation vault | Holds FUZE assigned to an approved allocation category | Allocation, mandate, token amount, restriction, authority, release rule, and circulation treatment |
| Token vesting vault | Holds FUZE under approved vesting or lock conditions | Beneficiary class, schedule, cliff, condition, release route, termination, and reconciliation |
| Claim-funding vault | Funds an approved migration, community, incentive, grant, or other claim process | Program, eligibility, claim window, claimable amount, unclaimed treatment, and return route |
| Token treasury vault | Holds FUZE available only for approved treasury or category-consistent actions | Allocation source, authority, limits, permitted movement classes, and reporting |
| Stablecoin treasury vault | Holds approved stablecoins for treasury, compensation, vendor, refund, product, or operating use | Asset, network, issuer, custody, obligations, payment controls, and accounting treatment |
| Fiat or payment account | Holds fiat or provider balances for approved operations | Entity, institution, account ownership, permissions, reconciliation, and legal treatment |
| Reserve vault | Holds assets designated for continuity, obligations, risk, strategic needs, or another reserve purpose | Reserve class, basis, trigger, utilization authority, and review cadence |
| Program vault | Supports a defined product, community, partner, migration, incentive, grant, or ecosystem program | Program owner, budget, eligibility or milestone, restrictions, end condition, and return treatment |
| Operational vault | Supports recurring settlement, compensation, product payment, treasury, or another controlled execution function | Transaction classes, limits, counterparties, allowlists, and reconciliation |
| Liquidity or market-operation vault | Holds assets for an approved liquidity, market-making, venue, or market-structure purpose | Venue or counterparty, inventory limits, custody, risk controls, return rights, and specialist reporting |
| Partner custody vault | Holds or administers assets under a partner agreement | Partner authority, purpose, milestone, restrictions, onward transfer, return rights, and reporting |
| Recovery or quarantine vault | Isolates returned, disputed, compromised, unsupported, or erroneous assets | Source event, investigation owner, restrictions, final disposition, and closure |
| Bridge custody vault | Holds canonical assets supporting a represented token or cross-network process | Canonical asset, representation, backing, bridge controls, reconciliation, and incident treatment |
| Evidence registry | Holds public or permissioned proof references rather than economic assets | Source, retention, access, correction, publication, and archive |

A vault may have multiple attributes, but it should have one controlling mandate and a reliable subledger where more than one purpose exists.

## Reserve Classification

### Continuity Reserve

Supports essential product, infrastructure, security, staffing, data, provider, or operating continuity.

### Obligation Reserve

Supports a recorded liability or expected obligation such as:

- tax;
- refund;
- chargeback;
- vendor settlement;
- compensation;
- professional service;
- partner obligation;
- claim correction;
- or another approved payable.

### Product and Service Reserve

Supports approved product delivery, Platform Credit obligations, AI usage, provider costs, customer support, infrastructure, moderation, or service continuity.

### Program Reserve

Sets aside resources for an approved:

- community program;
- migration;
- holder incentive;
- grant;
- partner program;
- event;
- education initiative;
- product launch;
- or ecosystem program.

### Security and Incident Reserve

Supports response, recovery, audit, remediation, notification, replacement, or continuity after a security, privacy, custody, contract, provider, or operational incident.

### Legal, Compliance, Tax, and Audit Reserve

Supports professional review, filings, tax, audit, assurance, compliance, dispute, or regulatory obligations.

### Strategic Reserve

Preserves resources for a future initiative that requires a separate use decision at the time of activation.

### Liquidity and Market-Structure Reserve

Preserves approved capacity for future liquidity or market-structure needs without implying deployment, listing, price support, or trading activity.

### Stability Reserve

Supports an exceptional documented response to ecosystem, operational, reporting, custody, or continuity risk.

A stability reserve is not a price-stabilization promise.

### Recovery Reserve

Holds recovered or returned assets pending final classification, reuse, reallocation, repayment, or closure.

## Vault and Reserve Status Vocabulary

| Status | Meaning |
|---|---|
| Proposed | Purpose and design are being prepared |
| Under review | Establishment, custody, authority, or policy is being reviewed |
| Approved for setup | Establishment is authorized, but production activation remains pending |
| Testing | Technical or provider setup uses test or controlled limited assets |
| Verified | Address, contract, account, roles, and configuration have been checked |
| Active | Structure may operate within its approved mandate |
| Funded | Assets or records have entered the structure |
| Designated | A reserve amount and purpose are approved |
| Partially committed | Part of the balance is committed |
| Fully committed | All available capacity is committed |
| Restricted | Movement or utilization is limited by a current condition |
| Suspended | New activity is paused pending review |
| Quarantined | Assets are isolated pending investigation or disposition |
| Under reconciliation | Balance, ledger, custody, or commitment differences are being resolved |
| Closing | Remaining assets, authority, records, and obligations are being finalized |
| Closed | Mandate and remaining actions are complete or controlled |
| Deprecated | Structure is no longer used for new activity but remains monitored or retained |
| Replaced | A successor structure exists and migration treatment is recorded |
| Corrected | Later authorization changes a prior record while preserving history |
| Archived | Historical records remain retained but are not current |

`Approved`, `active`, `funded`, `available`, `committed`, and `released` are different statuses.

## Establishment Record

Before activation, the responsible owner should prepare a complete establishment record.

### Required Fields

1. structure identifier;
2. public label where approved;
3. vault class;
4. reserve class where applicable;
5. asset, token, allocation, currency, or record scope;
6. network, institution, provider, or system;
7. mandate;
8. permitted uses;
9. prohibited uses;
10. source of assets or records;
11. legal or beneficial-control context;
12. custody arrangement;
13. authority model;
14. signer, approver, or role model;
15. transaction or movement classes;
16. limits and thresholds;
17. allowlist or destination controls;
18. timelock or delay controls;
19. emergency and pause controls;
20. reconciliation method;
21. review cadence;
22. commitment and reserve accounting method;
23. public and permissioned reporting fields;
24. privacy and confidentiality class;
25. incident and recovery process;
26. provider, address, contract, or signer change process;
27. activation conditions;
28. closure conditions;
29. owners and reviewers;
30. effective date;
31. expiry or reassessment trigger;
32. current status; and
33. current-as-of date.

### Establishment Evidence

Evidence may include:

- governance decision;
- treasury approval;
- allocation authority;
- reserve policy;
- agreement;
- contract deployment and verification;
- custodian or provider account evidence;
- bank or payment account evidence;
- signer and role confirmation;
- test transaction;
- security review;
- legal, accounting, tax, or compliance review;
- and public-label approval.

### Testing Before Activation

Technical setup may occur before production activation only when:

- test and production assets remain clearly separated;
- production authority is not assumed;
- test records are labeled;
- test balances are excluded from production reports;
- and activation requires a separate verified decision.

## Mandate and Permitted Use

The mandate should answer:

1. Why does the structure exist?
2. Which assets, allocations, obligations, programs, or records belong in it?
3. Which uses are permitted?
4. Which uses are prohibited?
5. Which authority can approve activity?
6. Which conditions must be satisfied before movement or utilization?
7. Which evidence is required?
8. How are balances, commitments, and restrictions reported?
9. What event causes suspension, reclassification, replacement, or closure?

### Prohibited Use Examples

A vault should not be used for:

- another allocation category without reclassification;
- personal transactions;
- undocumented compensation;
- unapproved token grants;
- unsupported stablecoins or networks;
- customer funds outside the approved product process;
- mixing Platform Credits with external assets;
- market operations outside approved authority;
- hidden partner commitments;
- price support promises;
- or any use inconsistent with the mandate.

## Custody Models

### Self-Custody

Self-custody records should define:

- wallet or contract;
- network;
- ownership and authority;
- signer threshold;
- signer roles;
- key or recovery governance at a restricted level;
- transaction preparation;
- approval;
- execution;
- monitoring;
- and replacement.

### Multisignature Custody

Multisig design should define:

- signer count;
- approval threshold;
- signer roles;
- role conflicts;
- signer replacement;
- quorum loss;
- emergency actions;
- module and guard configuration where applicable;
- transaction review;
- and public-safe disclosure.

### Timelocked Custody

Timelock design should define:

- applicable movement classes;
- delay;
- queueing;
- cancellation;
- emergency bypass if any;
- notice;
- and execution authority.

### Smart-Contract Custody

Contract custody should define:

- contract purpose;
- token or asset support;
- admin and upgrade powers;
- pause powers;
- withdrawal and recovery rights;
- role assignments;
- event records;
- verification status;
- testing;
- audit or assurance state where applicable;
- and incident treatment.

### Third-Party Custody

Third-party custody should define:

- provider or institution;
- legal account owner;
- beneficial owner;
- authorized users;
- approval and withdrawal controls;
- sub-account treatment;
- statements and evidence;
- service limits;
- insolvency and access risk;
- freeze or restriction risk;
- provider change;
- and exit plan.

### Exchange Custody

Exchange custody requires clear separation among:

- FUZE treasury account;
- market-maker account;
- partner account;
- user deposit balances;
- hot and cold wallets;
- and omnibus balances.

An exchange-associated address does not establish listing, trading, beneficial ownership, or circulation status by itself.

### Bank and Payment Accounts

Bank or payment accounts should identify:

- legal owner;
- institution;
- currency;
- authorized users;
- transaction limits;
- approval process;
- statements;
- reconciliation;
- freezes or service limits;
- and closure or migration treatment.

## Authority Model

### Roles

Possible roles include:

- establishment proposer;
- mandate owner;
- allocation or reserve owner;
- budget owner;
- custody administrator;
- transaction requester;
- transaction preparer;
- reviewer;
- approver;
- signer or executor;
- reconciler;
- security reviewer;
- legal, accounting, tax, compliance, or specialist reviewer;
- incident owner;
- reporter;
- and closure authority.

### Delegated Authority

Delegated authority should identify:

- scope;
- asset;
- vault;
- amount threshold;
- transaction class;
- destination class;
- duration;
- review requirement;
- and revocation process.

### Combined Roles

When staffing limits require combined roles, the record should identify:

- combined responsibilities;
- risk;
- compensating review;
- transaction limits;
- logging;
- and decision authority.

### Authority Expiry

Authority should be reviewed after:

- role change;
- departure;
- incident;
- provider change;
- mandate change;
- extended inactivity;
- governance change;
- or scheduled review.

## Segregation Rules

FUZE should separate, physically or through a reliable subledger:

- distinct FUZE token allocations;
- FUZE token from stablecoins;
- fiat from digital assets;
- operating balances from protected reserves;
- participant or claim funding from treasury balances;
- product receipts from compensation funds;
- approved distributable value from unrestricted operating value;
- partner or grant inventory from treasury inventory;
- market-operation inventory from ordinary treasury inventory;
- returned or disputed assets from active program assets;
- bridge backing from unencumbered treasury assets;
- test assets from production assets;
- and public evidence records from private operational records.

### Commingling Exception

A commingling exception should identify:

- reason physical segregation is impractical;
- affected assets and purposes;
- subledger method;
- ownership and commitment records;
- movement allocation method;
- reconciliation method;
- reviewer;
- duration;
- risk controls;
- and exit plan.

### Mixed-Allocation Token Vault

Where one token vault contains multiple allocation categories, the subledger should preserve:

- category opening balance;
- category inflows and outflows;
- commitments;
- locks;
- releases;
- deployments;
- returns;
- corrections;
- and closing balance.

Public reporting should not label the entire wallet as one allocation when the ledger shows more than one.

## Funding and Reserve Designation

### Initial Funding

The initial funding process should confirm:

- source;
- source authority;
- destination;
- asset;
- network;
- native or contract reference;
- amount;
- expected classification;
- circulation effect where applicable;
- custody and signer readiness;
- test-transfer requirement;
- transaction evidence;
- and post-funding reconciliation.

### Reserve Designation

A reserve designation should identify:

1. reserve identifier;
2. reserve class;
3. purpose;
4. source;
5. amount or sizing method;
6. unit;
7. custody;
8. effective date;
9. obligations or risk addressed;
10. commitment treatment;
11. utilization trigger;
12. approval authority;
13. review cadence;
14. replenishment treatment;
15. release or closure treatment;
16. public-reporting treatment;
17. status; and
18. current-as-of date.

### Designation Does Not Move Assets Automatically

A reserve can be designated within an existing vault or moved into a dedicated vault.

The designation decision and custody movement should be recorded separately.

### Funding Source Boundaries

A reserve can be funded from an approved:

- token allocation;
- treasury balance;
- product-revenue pool after proper treatment;
- operating budget;
- returned program balance;
- recovered asset;
- financing source under an approved plan;
- or another authorized source.

The funding source does not automatically determine the reserve's accounting, tax, release, or circulation treatment.

## Commitment and Availability

Every vault or reserve should distinguish:

- total custodied balance;
- unrestricted available balance within the mandate;
- committed balance;
- restricted balance;
- approved pending movement;
- disputed or quarantined balance;
- returned or recovered balance;
- and uncommitted capacity.

### Commitment Record

A commitment should identify:

- commitment identifier;
- vault or reserve;
- asset and amount;
- purpose;
- obligation, program, recipient class, partner, claim, release, or deployment reference;
- approval;
- effective date;
- expiry;
- cancellation treatment;
- utilization method;
- return treatment;
- status;
- and current-as-of date.

### Commitment Expiry

Expired or cancelled commitments should not automatically restore availability when:

- a dispute remains;
- a legal or accounting obligation remains;
- a transaction is pending;
- a partner or claim process remains open;
- a security incident exists;
- or classification is unresolved.

## Movement Controls

### Internal Custody Transfer

A transfer between controlled structures should identify:

- source and destination mandates;
- allocation or reserve purpose;
- asset and amount;
- authority;
- expected state;
- expected circulation effect;
- transaction evidence;
- and post-transfer reconciliation.

Continued control can leave economic availability and circulation unchanged.

### External Deployment

Movement to a recipient, contract, custodian, partner, claim process, venue, pool, market maker, or provider requires the specialist approval applicable to that activity.

### Stablecoin Payment

Stablecoin movement for compensation, vendors, reimbursements, or operating obligations should follow [FUZE Stablecoin Compensation Policy](11-FUZE_STABLECOIN_COMPENSATION_POLICY_PUBLIC.md) or the applicable product-payment process.

### Token Release

FUZE token release should follow:

- source allocation;
- vault-specific release conditions;
- vesting, eligibility, claim, partner, incentive, migration, or market requirements;
- controlled-circulation approval;
- and post-release classification.

### Return

Unused, cancelled, failed, excess, recovered, or disputed assets should return to:

- the original vault;
- another approved category vault;
- or a recovery vault

under a documented instruction.

### Reclassification

A mandate or allocation-purpose change requires approval at least as strong as the original establishment and allocation decision.

Reclassification should preserve:

- former purpose;
- new purpose;
- amount;
- authority;
- effective time;
- updated custody and subledger;
- updated public reporting;
- and fixed-supply reconciliation where FUZE token is affected.

## Reserve Utilization

A reserve-use request should identify:

1. reserve identifier and class;
2. current custodied balance;
3. committed balance;
4. uncommitted capacity;
5. event, obligation, program, or risk addressed;
6. requested amount;
7. asset and unit;
8. destination;
9. timing and urgency;
10. sizing basis;
11. permitted-use basis;
12. budget, legal, accounting, tax, compliance, security, or specialist review where applicable;
13. approving authority;
14. expected remaining reserve;
15. replenishment proposal if any;
16. reporting treatment;
17. follow-up evidence;
18. return or recovery treatment; and
19. closure trigger.

### Reserve Utilization States

| Status | Meaning |
|---|---|
| Requested | A proposed use exists |
| Under review | Evidence, purpose, amount, and authority are being reviewed |
| Approved | The use is approved but not executed |
| Committed | Capacity is reserved for the approved use |
| Submitted | Movement or payment instruction is sent |
| Confirmed | Required technical or provider confirmation exists |
| Utilized | The reserve value entered its approved use |
| Partially utilized | Only part of the approved amount was used |
| Returned | Unused or recovered amount returned |
| Replenishment proposed | A new funding proposal exists |
| Closed | Use and remaining obligations are reconciled |

### Purpose Limitation

Reserve value should be used only for the approved purpose.

A materially different use requires:

- a new utilization decision;
- reserve reclassification;
- or another authorized funding source.

### Replenishment

Replenishment is not automatic.

A replenishment proposal should identify:

- reason;
- source;
- amount;
- target reserve level;
- prior utilization;
- current obligation or risk;
- treasury impact;
- approval;
- and reporting treatment.

## Asset-Specific Treatment

### FUZE Token

FUZE-token vault records should identify:

- allocation category;
- canonical token and network;
- token amount;
- lock, vesting, claim, partner, incentive, migration, reserve, or market state;
- release authority;
- circulation effect;
- and supply-reporting treatment.

### Stablecoins

Stablecoin vault records should identify:

- issuer;
- network;
- native or contract reference;
- decimals;
- bridge or wrapped status;
- custody support;
- freeze or blacklist risk;
- depegging risk;
- obligations;
- conversion treatment;
- and accounting unit.

### Fiat and Provider Balances

Fiat and provider records should identify:

- currency;
- institution or provider;
- legal owner;
- account or sub-account;
- available, pending, restricted, and held balances;
- settlement timing;
- fees;
- reconciliation;
- and service restrictions.

### Platform Credits

Platform Credits remain product-consumption units under [FUZE Platform Credits Relationship](10-FUZE_PLATFORM_CREDITS_RELATIONSHIP_PUBLIC.md).

A Platform Credit ledger is not a FUZE-token or stablecoin vault.

Product-credit obligations may inform a product or continuity reserve, but the units and ledgers must remain separate.

### Approved Distributable Value

Approved distributable value is a reviewed value status under [FUZE Approved Distributable Value Model](09-FUZE_APPROVED_DISTRIBUTABLE_VALUE_MODEL_PUBLIC.md).

A treasury or vault balance does not become approved distributable value without the required pool, period, calculation, review, and decision record.

## Reconciliation

### Custody Reconciliation

For each asset-holding vault:

```text
opening custody balance
+ verified inflows
- verified outflows
+/- approved corrections
= closing custody balance
```

### Commitment Reconciliation

```text
closing custody balance
- committed amount
- restricted amount
- approved pending movements
- disputed or quarantined amount
= currently uncommitted balance within the mandate
```

### Reserve Reconciliation

```text
opening reserve designation
+ approved additions and replenishment
- approved utilization
- approved release from reserve designation
+ returned or recovered amount
+/- corrections
= closing reserve designation
```

### Token Allocation Reconciliation

For a FUZE-token allocation vault:

```text
opening allocation-vault balance
+ approved allocation inflows and returns
- approved releases, deployments, reclassifications, or burns
+/- corrections
= closing allocation-vault balance
```

### Multi-Asset Presentation

FUZE token quantities, stablecoin amounts, fiat balances, accounting values, Platform Credits, and other units should not be added together without an approved valuation method and measurement time.

### Reconciliation Differences

Differences may include:

- missing transaction;
- duplicate transaction;
- wrong asset;
- wrong network;
- unsupported token;
- fee difference;
- conversion difference;
- bridge difference;
- provider timing;
- pending settlement;
- incorrect allocation mapping;
- incorrect commitment;
- stale subledger;
- unauthorized movement;
- or compromised custody.

A material unresolved difference should trigger:

- investigation;
- restricted activity;
- suspension;
- quarantine;
- correction;
- or escalation.

## Monitoring and Review

Each active structure should have a defined monitoring and review cadence.

### Ongoing Monitoring

Monitoring may cover:

- balances;
- transactions;
- asset and network changes;
- contract events;
- signer and role changes;
- provider notices;
- allowlist changes;
- commitments;
- reserve adequacy;
- pending instructions;
- failed transactions;
- bridge backing;
- exchange or custodian status;
- security alerts;
- and public-reporting differences.

### Scheduled Review

The review should confirm:

- continuing business need;
- correct classification;
- mandate accuracy;
- asset and allocation scope;
- custody health;
- signer and authority validity;
- balance and commitment reconciliation;
- reserve adequacy;
- public-label accuracy;
- open incidents and exceptions;
- provider and contract support;
- and closure or replacement need.

### Event-Driven Review

Review should occur after:

- material movement;
- large commitment;
- reserve utilization;
- signer change;
- role change;
- provider change;
- contract upgrade;
- network migration;
- bridge event;
- security incident;
- reconciliation difference;
- legal or jurisdiction change;
- mandate change;
- extended dormancy;
- or public-report correction.

## Signer, Authority, Address, Contract, and Provider Changes

### Signer or Role Change

The change record should identify:

- prior role or signer;
- new role or signer;
- reason;
- effective time;
- approval;
- credential or authority revocation status;
- multisig or contract configuration change;
- testing;
- public-report effect;
- and current status.

### Vault Address Change

A new address should be treated as a new custody destination requiring:

- purpose confirmation;
- network and asset verification;
- control verification;
- signer or admin verification;
- test transaction where proportionate;
- migration plan;
- old-address treatment;
- balance reconciliation;
- label update;
- and public notice where applicable.

### Contract Upgrade or Replacement

The record should identify:

- old and new contracts;
- reason;
- asset migration;
- admin and upgrade powers;
- testing and assurance;
- pause and rollback;
- remaining old-contract balance;
- deprecated status;
- and reporting effect.

### Custodian or Provider Change

The change should address:

- legal account ownership;
- asset and network support;
- migration;
- pending transactions;
- statements and evidence;
- fees;
- access revocation;
- old-provider closure;
- new-provider controls;
- and reconciliation.

## Suspension, Quarantine, and Incident Handling

### Suspension Triggers

Activity may be suspended for:

- unauthorized or unexplained movement;
- compromised signer, key, account, or provider;
- contract vulnerability;
- material reconciliation difference;
- incorrect allocation or reserve classification;
- conflicting instructions;
- expired mandate;
- unsupported asset or network;
- provider insolvency or access restriction;
- sanctions, legal, tax, accounting, or compliance concern;
- bridge or exchange incident;
- market-operation incident;
- public-reporting error;
- or another material risk.

### Suspension Scope

A suspension may apply to:

- one transaction;
- one movement class;
- one asset;
- one network;
- one signer;
- one vault;
- one reserve;
- one provider;
- one partner;
- one program;
- one contract;
- or all activity.

### Quarantine

Assets may move to a recovery or quarantine vault when:

- return is required;
- ownership or classification is uncertain;
- unsupported assets were received;
- fraud or compromise is suspected;
- an erroneous transfer was recovered;
- a dispute remains;
- or a provider or contract incident requires isolation.

### Incident Record

The incident record should identify:

1. incident identifier;
2. affected vaults and reserves;
3. assets and amounts;
4. affected authority, signer, contract, provider, partner, or program;
5. detection time;
6. known transaction or balance impact;
7. containment;
8. suspension or quarantine scope;
9. evidence;
10. recovery options;
11. accounting, tax, legal, security, allocation, and circulation effects;
12. public-communication treatment;
13. root cause;
14. remediation;
15. reviewer;
16. reactivation conditions;
17. current status; and
18. closure.

### Recovery and Reactivation

Reactivation should require:

- containment;
- authority or configuration repair;
- custody verification;
- affected-balance reconciliation;
- corrected records;
- testing where applicable;
- renewed approval;
- and updated public status.

Technical recovery alone does not automatically restore reserve capacity or movement authority.

## Recovery, Returns, and Final Disposition

Recovered or returned assets should not be reused until their:

- source;
- ownership;
- allocation;
- reserve purpose;
- restrictions;
- accounting treatment;
- legal treatment;
- tax treatment;
- circulation treatment;
- and final destination

are resolved.

### Final Disposition Options

Possible outcomes include:

- return to original vault;
- return to original allocation;
- restoration to reserve;
- repayment to counterparty;
- use under the original approved purpose;
- transfer to another approved vault;
- reclassification;
- continued quarantine;
- write-off or loss treatment;
- burn where separately approved and technically valid;
- or closure.

## Public Reporting

A public vault or reserve report may include:

- report identifier and version;
- vault or reserve label;
- classification;
- mandate;
- asset, allocation, or record class;
- network or institution at an approved level;
- status;
- opening and closing balance or capacity;
- available, committed, restricted, utilized, returned, and corrected amounts;
- reserve designation and utilization summary;
- material inflow, outflow, transfer, return, reclassification, or closure events;
- transaction, governance, contract, or report references;
- methodology;
- review date;
- limitations;
- and current-as-of date.

### Public Vault Visibility

Presentation and publication behavior are governed by [FUZE Public Vault Visibility System](16-FUZE_PUBLIC_VAULT_VISIBILITY_SYSTEM_PUBLIC.md).

### Reporting Methodology

The report should identify:

- asset and unit;
- measurement point;
- source system;
- wallet, contract, provider, or custody scope;
- allocation and reserve classification;
- commitment and availability method;
- pending and disputed treatment;
- conversion method where values are aggregated;
- corrections;
- and limitations.

### Public-Safe Labels

Labels should describe function rather than personal identity.

Examples include:

- Team Allocation Vault;
- Community Participation Vault;
- Stablecoin Operating Treasury;
- Security Incident Reserve;
- Claim Funding Contract;
- Liquidity Operations Vault;
- or Recovery Vault.

### Private Information

Public reporting should not expose:

- personal identity linked to a wallet;
- private beneficiary records;
- private partner or vendor terms;
- private compensation details;
- bank account details;
- provider credentials;
- signer identities where not approved;
- private keys;
- recovery materials;
- exact security procedures;
- confidential legal, accounting, tax, audit, or compliance records;
- or exploitable treasury patterns.

## Closure

A vault or reserve may close when:

- its mandate ends;
- the program concludes;
- all obligations are settled;
- assets are exhausted;
- remaining assets are transferred;
- custody is replaced;
- the reserve is released or retired;
- a contract is deprecated;
- a provider is closed;
- or governance retires the structure.

### Closure Requirements

1. final mandate review;
2. final custody balance;
3. final subledger and commitment reconciliation;
4. final reserve designation and utilization reconciliation;
5. disposition of remaining assets;
6. cancellation, revocation, or transfer of authority;
7. pending transaction resolution;
8. incident and dispute resolution or controlled carry-forward;
9. public-label update;
10. dependent-system update;
11. evidence retention;
12. final public and private report where applicable;
13. closure authority; and
14. current-as-of date.

### Deprecated and Replaced Structures

A deprecated or replaced structure should identify:

- successor;
- migration date;
- remaining balance;
- pending obligations;
- monitoring status;
- access status;
- label status;
- and final closure trigger.

Closed identifiers should remain traceable.

Reuse of an address, account, contract, or label for a materially different purpose should undergo a new establishment and classification review.

## Separation from Adjacent Systems

| System or process | Primary role | Why it remains separate |
|---|---|---|
| Vault policy | Defines custody, authority, segregation, reconciliation, lifecycle, and reporting | Does not itself authorize release or use |
| Reserve policy | Defines why value is retained and the conditions for utilization | Reserve designation does not equal spending authority |
| Token allocation table | Defines fixed FUZE category amounts and mandates | Allocation does not establish custody or release |
| Vault-by-vault release rules | Defines category-specific release conditions | Release conditions differ by allocation and purpose |
| Controlled circulation | Governs token movement, state transition, and circulation classification | Vault custody is only one input |
| Platform Credits | Product-consumption units | Separate ledger and unit from external assets |
| Stablecoin compensation | Settles approved business obligations | Requires separate engagement, payee, payment, and tax controls |
| Approved distributable value | Reviewed value from defined product-revenue pools | A vault balance is not automatically approved value |
| Wallet-based participation | Activation-gated eligibility, claim, and payout process | Vault funding does not create participant rights |
| Liquidity and listing policy | Governs market-structure and venue processes | Market vaults do not establish listing, liquidity, or price outcome |

## Status and Evidence

This paper defines the vault-and-reserve governance model.

It does not independently prove that any vault, reserve, wallet, contract, bank account, provider, balance, release authority, or reserve capacity is currently active.

| Status claim | Evidence direction |
|---|---|
| Vault proposed | Proposal, classification, mandate, asset scope, owner, and status |
| Vault approved for setup | Establishment record, authority, custody design, reviewers, and decision |
| Vault verified | Address, contract, account, roles, asset, network, configuration, and test evidence |
| Vault active | Activation decision, current authority, custody support, monitoring, and status |
| Vault funded | Source, asset, amount, transaction or statement, classification, and reconciliation |
| Reserve designated | Purpose, class, amount, source, custody, trigger, authority, and review date |
| Balance available | Custody balance, commitments, restrictions, pending movements, disputes, and calculation |
| Balance committed | Approved obligation or program, amount, expiry, authority, and ledger entry |
| Reserve use approved | Request, purpose, amount, destination, reviews, authority, and remaining capacity |
| Reserve utilized | Movement or payment evidence, confirmation, destination use, balance effect, and reconciliation |
| Assets returned | Original movement, reason, amount, transaction or statement, destination, and revised classification |
| Vault suspended | Trigger, scope, effective time, authority, interim controls, and review conditions |
| Assets quarantined | Source event, amount, custody, restrictions, investigation, and disposition status |
| Vault reconciled | Custody, ledger, commitments, restrictions, fees, corrections, and reviewer evidence |
| Vault replaced | Old and new structures, migration, balances, authority changes, labels, and status |
| Vault closed | Final balance, disposition, authority revocation, reports, retention, and closure decision |
| Report corrected | Original report, error, evidence, revised values, reviewer, approval, and current version |

The following do not independently establish an active vault, available balance, reserve, or release authority:

- this paper;
- a wallet address;
- a wallet label;
- a balance screenshot;
- a transaction hash;
- a contract deployment;
- a multisig page;
- a bank balance;
- a stablecoin balance;
- an internal spreadsheet;
- a token allocation;
- a reserve announcement;
- code;
- a repository;
- or a public statement.

## Custody, Reserve, Release, Market, and Outcome Separation

The following remain separate:

- legal ownership;
- beneficial purpose;
- custody;
- vault establishment;
- vault activation;
- funding;
- reserve designation;
- available balance;
- commitment;
- restriction;
- movement approval;
- transaction execution;
- confirmation;
- reserve utilization;
- token release;
- claim funding;
- participant eligibility;
- claimability;
- payout;
- operational deployment;
- circulation;
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

A funded vault or designated reserve does not guarantee:

- use;
- replenishment;
- token release;
- participant eligibility;
- claim availability;
- payout;
- partner deployment;
- liquidity deployment;
- listing;
- market depth;
- price support;
- income;
- revenue share;
- or financial return.

## Public Boundary

This paper publishes the vault and reserve classification, establishment, custody, authority, segregation, funding, commitment, utilization, reconciliation, monitoring, incident, recovery, reporting, and closure model.

It does not publish or establish current:

- vault addresses;
- reserve addresses;
- bank or provider account details;
- signer identities;
- private authority configurations;
- asset balances;
- reserve amounts;
- available capacity;
- commitment amounts;
- release schedules;
- beneficiary identities;
- claim windows;
- partner balances;
- market-maker inventory;
- liquidity deployment;
- token circulation;
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

unless those details are separately approved and supported by current evidence in an establishment record, custody registry, allocation report, reserve report, release decision, transaction record, market-operation report, public vault report, specialist paper, or public status record.

Specific vault and reserve actions remain subject to their controlling allocation, treasury, compensation, product, approved-value, participation, vesting, claim, partner, migration, incentive, liquidity, market, legal, accounting, tax, compliance, technical, security, and reporting requirements.

## Key Takeaways

- A vault defines controlled custody or record structure; a reserve defines why resources are retained and how their use is controlled.
- A vault balance does not automatically establish availability, release authority, circulation, claimability, or market access.
- A reserve designation does not automatically authorize utilization, replenishment, token release, stablecoin payment, or liquidity deployment.
- Every structure should have a stable identifier, mandate, asset scope, authority model, custody design, controls, reconciliation method, review cadence, incident process, reporting treatment, and closure route.
- Assets with different allocation, ownership, restriction, obligation, participant, or market meanings should be segregated physically or through a reliable subledger.
- Available, committed, restricted, pending, disputed, utilized, returned, and reserve-capacity amounts are separate states.
- Funding, reserve designation, commitment, movement approval, execution, utilization, return, recovery, reclassification, and closure require durable evidence.
- Signer, role, address, contract, provider, and custody changes require renewed verification and reconciliation.
- Incidents may require suspension, quarantine, recovery, correction, replacement, or closure before normal activity resumes.
- Vault funding and reserve capacity do not guarantee token release, participant payout, listing, liquidity, price support, income, revenue share, or financial return.
