# FUZE Token Release and Circulation Clarity

## Executive Summary

FUZE token reporting uses distinct terms for fixed supply, allocation, custody, restriction, vesting, eligibility, claimability, release, deployment, external custody, circulation, return, recovery, reclassification, and burn.

These terms are not synonyms.

A token unit can change one status without changing every other status.

For example:

- an allocation can be approved without any token movement;
- a treasury transfer can change custody without changing circulation;
- an unlock can end one restriction while other restrictions remain;
- vesting can complete without release;
- a claim can open without any recipient claiming;
- a claim can complete while a continuing lock remains;
- tokens can enter a liquidity or market-operation system without becoming ordinary holder circulation;
- and a return can reduce deployed or circulating classification while preserving the original allocation purpose.

The fixed FUZE token supply is **500,000,000 FUZE** under the approved allocation model.

That figure remains separate from:

- allocated supply;
- custodied supply;
- available allocation balance;
- planned or committed supply;
- locked or vesting supply;
- vested supply;
- eligible or claimable supply;
- claimed supply;
- approved-for-release supply;
- released supply;
- operationally deployed supply;
- externally custodied supply;
- liquidity or market-operation inventory;
- and circulating supply.

The authoritative reporting sequence is:

```text
verified token and network
-> fixed total supply
-> approved allocation categories
-> custody and control classification
-> restriction and commitment classification
-> release, claim, deployment, return, recovery, or burn events
-> mutually exclusive point-in-time state buckets
-> period movement reconciliation
-> circulating-supply calculation under a versioned methodology
-> public report
-> correction or restatement where required
```

A public supply figure should identify:

- report identifier and version;
- network and canonical token contract;
- measurement timestamp and block where applicable;
- total-supply source;
- allocation-table version;
- controlled-wallet and contract registry version;
- circulation-methodology version;
- custody and control assumptions;
- treatment of locks, vesting, claims, exchanges, liquidity, market makers, bridges, burns, and pending classifications;
- opening and closing figures;
- event movements;
- corrections;
- limitations;
- reviewer;
- and current-as-of date.

The same token units should not be counted more than once across mutually exclusive supply buckets.

Descriptive attributes can overlap, but additive report categories cannot.

For example, team tokens may be both treasury-custodied and unvested. Those are two attributes of the same units, not two separate supply amounts to add together.

This paper owns FUZE's public supply vocabulary, event vocabulary, classification tests, circulating-supply methodology structure, reporting schema, reconciliation rules, examples, third-party comparison process, corrections, restatements, and public interpretation boundaries.

The operating controls for token movement are defined in [FUZE Controlled Circulation Policy](12-FUZE_CONTROLLED_CIRCULATION_POLICY_PUBLIC.md).

Allocation purpose and amounts are defined in [FUZE Token Allocation Table](02-FUZE_TOKEN_ALLOCATION_TABLE_PUBLIC.md).

Vault custody and category-specific release controls are defined in [FUZE Vault and Reserve Policy](14-FUZE_VAULT_AND_RESERVE_POLICY_PUBLIC.md) and [FUZE Vault-by-Vault Release Rules](15-FUZE_VAULT_BY_VAULT_RELEASE_RULES_PUBLIC.md).

## Purpose of This Paper

This paper explains:

- the public supply-reporting position;
- the controlling fixed supply;
- supply terminology;
- event terminology;
- point-in-time states versus period movements;
- mutually exclusive categories versus overlapping attributes;
- custody, control, restriction, availability, and return-right tests;
- circulating-supply methodology;
- exchange, custodian, bridge, contract, liquidity, and market-maker treatment;
- allocation and wallet labels;
- unlock and release calendars;
- reporting schemas;
- reconciliation equations;
- interpretation examples;
- third-party data-provider differences;
- corrections and restatements;
- methodology changes;
- public reporting and privacy boundaries;
- status and evidence requirements; and
- public limitations.

This paper does not replace:

- the token allocation table;
- controlled-circulation authorization;
- vault-specific custody rules;
- vault-specific release rules;
- vesting agreements;
- migration or community-round terms;
- claim instructions;
- partner agreements;
- incentive-program rules;
- liquidity or market-making procedures;
- exchange-listing procedures;
- legal or accounting advice;
- smart-contract specifications;
- or the token risk register.

## Public Position

Supply reporting should explain what changed and what did not change.

FUZE should not use broad words such as:

- unlocked;
- released;
- distributed;
- available;
- deployed;
- circulating;
- liquid;
- listed;
- or burned

without a defined status and supporting evidence.

A release report should not imply exchange access.

A circulation report should not imply liquidity.

A liquidity deployment should not imply stable depth or spread.

A listing discussion or application should not be described as approval or live trading.

A supply event should not be represented as a price-support action or financial outcome.

## Controlling Supply

The approved FUZE token supply is:

| Field | Value |
|---|---:|
| Fixed total supply | 500,000,000 FUZE |
| Approved allocation categories | 10 |
| Allocation reconciliation | 100.00% |

The [FUZE Token Allocation Table](02-FUZE_TOKEN_ALLOCATION_TABLE_PUBLIC.md) controls the approved category names, amounts, percentages, and mandates.

A public supply report should identify the current verified:

- network;
- canonical FUZE token contract;
- decimals;
- total-supply source;
- block or timestamp;
- and contract status

when those details are approved for publication.

This paper does not announce a contract address.

### Fixed Supply Versus Reported Supply States

The fixed total supply contains all approved allocation categories whether the units are:

- held in controlled custody;
- locked;
- vesting;
- claimable;
- released;
- externally custodied;
- operationally deployed;
- circulating;
- returned;
- pending classification;
- or verifiably burned.

If a technically valid and approved burn changes onchain total supply, the report should distinguish:

- original fixed allocation model;
- cumulative burned amount;
- current onchain total supply;
- and revised reconciliation treatment.

No burn is established by this paper.

## Supply Vocabulary

### Fixed Total Supply

The complete approved token quantity under the FUZE token model before any separately approved and verifiable supply-reduction event.

### Onchain Total Supply

The total-supply value returned by the verified token contract at the stated block or time.

Onchain total supply should reconcile to the fixed model and any approved burn or supply-changing event.

### Allocated Supply

Tokens assigned to an approved fixed-supply category.

Allocation defines purpose and mandate.

It does not establish custody, commitment, release, or circulation.

### Custodied Supply

Tokens held in an identified wallet, vault, contract, custodian, exchange, bridge, provider, or account.

Custody is a location and control concept, not a complete circulation conclusion.

### Treasury-Controlled Supply

Tokens subject to direct or governed FUZE treasury, reserve, foundation, program, signer, contract-admin, or equivalent operating authority.

### Available Allocation Balance

Tokens within an allocation category that remain uncommitted and available only for an approved category-consistent purpose.

Available within an allocation does not mean available to the market or public.

### Planned Supply

Tokens included in a proposal, forecast, budget, or intended use that has not created a binding commitment or recipient right.

### Committed Supply

Tokens reserved for an approved obligation, recipient class, program, grant, partner, claim process, incentive, vesting arrangement, liquidity purpose, or other authorized use.

Commitment does not equal release or circulation.

### Reserved Supply

Tokens retained for a defined future purpose, contingency, program, obligation, or risk treatment outside ordinary circulation.

### Locked Supply

Tokens restricted by:

- smart contract;
- vesting contract;
- lockup;
- policy;
- agreement;
- jurisdiction;
- claim condition;
- program rule;
- custody rule;
- or another enforceable limitation.

### Unlocked Supply

Tokens for which a specified lock has ended.

Unlocked tokens can remain:

- unvested under another condition;
- unreleased;
- in controlled custody;
- contractually restricted;
- committed;
- or outside circulation.

### Vesting Supply

Tokens progressing under an approved time, service, milestone, performance, or hybrid vesting schedule.

### Vested Supply

Tokens that have satisfied the applicable vesting condition.

Vested tokens can remain unreleased, unclaimed, custodied, restricted, or non-circulating.

### Unvested Supply

Tokens that have not yet satisfied the applicable vesting condition.

### Eligible Supply

Tokens assigned to recipients or wallets that satisfy the approved eligibility criteria for a stated process.

Eligibility does not equal claimability, claim completion, receipt, or circulation.

### Claimable Supply

Tokens available for eligible recipients to claim under an active process and current claim window.

The methodology should state whether unclaimed claimable units remain outside circulating supply.

### Claimed Supply

Tokens for which the required claim action has been completed.

Claimed status does not by itself establish:

- transfer confirmation;
- recipient custody;
- absence of continuing lock;
- or circulating status.

### Approved-for-Release Supply

Tokens for which all required release conditions and authority are complete, while execution remains pending.

### Released Supply

Tokens moved from a prior controlled state under an approved release instruction.

Released supply is a cumulative or event measure unless the report expressly uses another definition.

Released does not automatically mean circulating.

### Operationally Deployed Supply

Tokens placed into an approved:

- product mechanism;
- grant;
- partner arrangement;
- incentive program;
- claim system;
- treasury use;
- liquidity position;
- market-making arrangement;
- venue account;
- bridge;
- or another operating mechanism.

Operational deployment requires a specific classification.

### Externally Custodied Supply

Tokens held by a recipient, partner, exchange, custodian, market maker, bridge, contract, provider, or other party outside direct FUZE custody.

External custody does not automatically prove unrestricted beneficial availability or circulation.

### Circulating Supply

Tokens reasonably available in user or market circulation under the published methodology at the stated block or time.

The methodology should define the treatment of:

- controlled treasury wallets;
- allocation vaults;
- team and advisor wallets;
- vesting contracts;
- claim contracts;
- unclaimed balances;
- recipient wallets;
- exchanges;
- omnibus custodians;
- liquidity pools;
- market-maker inventory;
- bridges;
- wrapped or represented tokens;
- partner wallets;
- restricted program wallets;
- returned balances;
- burns;
- and pending classifications.

### Non-Circulating Supply

The mutually exclusive remainder after circulating supply is subtracted from current total supply under the same methodology and measurement point.

```text
current total supply = circulating supply + non-circulating supply
```

### Liquidity-Committed Supply

Tokens contractually or operationally committed to an approved liquidity or market-structure purpose but not necessarily transferred or externally available.

### Liquidity-Deployed Supply

Tokens placed into an approved liquidity position, venue, pool, or market-structure operation.

Reports should distinguish:

- committed;
- transferred;
- paired;
- deposited;
- externally available;
- withdrawn;
- returned;
- and currently held inventory.

### Market-Maker Inventory

Tokens held or controlled for an approved market-making or liquidity-management purpose.

Market-maker inventory should not automatically be classified as ordinary holder circulation.

### Bridged or Represented Supply

A token representation backed by locked or custodied canonical FUZE on another network or system.

Backed representations should reconcile to underlying canonical units and should not be counted as newly issued economic supply.

### Returned Supply

Tokens moved back to approved controlled custody after unused, cancelled, expired, failed, disputed, recovered, or completed use.

### Recovered Supply

Tokens restored to approved control after an error, incident, cancellation, compromise, or other recovery event.

Recovered units require renewed state classification before reuse.

### Pending-Classification Supply

Tokens for which current evidence is insufficient to assign a stronger final classification.

Pending-classification amounts should be disclosed, assigned an owner, and resolved rather than hidden inside another category.

### Reclassified Supply

Tokens whose approved allocation purpose changed through formal authority and updated fixed-supply reconciliation.

### Retired or Inaccessible Supply

Tokens treated as operationally unavailable under an approved method but not necessarily provably burned.

### Burned Supply

Tokens provably removed from usable supply through an approved irreversible mechanism.

A transfer to an unknown, inactive, or inaccessible address should not be labeled a burn without sufficient proof.

## Event Vocabulary

| Event | Required interpretation | What it does not establish by itself |
|---|---|---|
| Allocation | Assigns token purpose within fixed supply | Custody, commitment, release, or circulation |
| Custody deposit | Places tokens into a wallet, vault, contract, custodian, or provider | Economic availability |
| Custody withdrawal | Removes tokens from one custody location | Final destination state or circulation |
| Custody transfer | Moves tokens between controlled locations | Circulation change |
| Commitment | Reserves tokens for an approved obligation or program | Release or recipient receipt |
| Lock | Applies an enforceable restriction | Vesting or release |
| Unlock | Ends a specified restriction | Unrestricted transferability or circulation |
| Vesting start | Begins an approved vesting schedule | Vested amount |
| Vest | Satisfies a vesting condition for stated units | Release or circulation |
| Eligibility approval | Confirms recipient or wallet qualification | Claim completion or receipt |
| Claim opens | Makes an amount claimable under an active process | Claim completion |
| Claim | Records the recipient's required claim action | Confirmed transfer or circulation |
| Release approval | Authorizes a defined release | Execution |
| Release | Moves units from the prior controlled state | Unrestricted circulation |
| Program funding | Places units into an operating program or claim mechanism | Individual recipient availability |
| Partner deployment | Places units under an approved partner arrangement | Unrestricted partner resale or circulation |
| Liquidity commitment | Reserves units for market-structure activity | Pool deposit or active liquidity |
| Liquidity deployment | Places units into a pool, venue, or market operation | Stable depth, spread, volume, or price support |
| Exchange deposit | Transfers units into exchange custody | Listing, trading availability, beneficial ownership, or circulation classification without further evidence |
| Bridge lock | Locks canonical FUZE to support another representation | New economic supply |
| Bridge mint | Creates a backed representation | Increase in total economic supply |
| Return | Restores unused or recovered units to approved control | Immediate availability for reuse |
| Recovery | Restores units after an error or incident | Final correction or reuse authority |
| Reclassification | Changes allocation purpose | Ordinary custody transfer |
| Burn | Permanently removes units where technically verified | Reclassification or ordinary transfer |
| Correction | Repairs an erroneous record or classification | Erasure of the original evidence |
| Restatement | Revises a prior public figure or method materially | Deletion of the prior report |

Public updates should name the actual event instead of relying on the vague phrase “tokens moved.”

## Point-in-Time States and Period Movements

### Point-in-Time State

A point-in-time report answers:

> What is the evidence-backed state of the supply at a specific timestamp or block?

It should use mutually exclusive buckets that reconcile to current total supply.

### Period Movement

A period report answers:

> What events changed custody, restriction, commitment, deployment, or circulation between the opening and closing measurement points?

Period movements include:

- allocation changes;
- commitments;
- locks;
- unlocks;
- vesting;
- claims;
- releases;
- deployments;
- returns;
- recoveries;
- reclassifications;
- burns;
- and corrections.

### Cumulative Measures

Cumulative measures may include:

- cumulative vested;
- cumulative claimed;
- cumulative released;
- cumulative deployed;
- cumulative returned;
- or cumulative burned.

A cumulative event total should not be represented as a current balance without reconciliation.

For example:

- cumulative released can exceed current circulating supply if released units were later returned, locked, bridged, or otherwise reclassified;
- cumulative deployed can exceed current deployed balance if positions were withdrawn or closed;
- and cumulative claimed can differ from current recipient-held supply.

## Mutually Exclusive Buckets and Overlapping Attributes

A supply report can use either:

1. mutually exclusive state buckets that add to total supply; or
2. overlapping descriptive attributes that are clearly labeled as non-additive.

It should not mix the two without explanation.

### Mutually Exclusive Example

```text
controlled non-circulating custody
+ restricted external custody
+ operational deployment outside ordinary circulation
+ ordinary circulating supply
+ pending classification
+ verifiably burned supply
= current total supply
```

The exact categories depend on the approved methodology.

### Overlapping Attribute Example

The same 10,000,000 FUZE could be:

- Team Allocation;
- treasury-custodied;
- locked;
- unvested;
- and non-circulating.

Those labels describe the same units and should not be summed.

### Reporting Requirement

Every table should identify whether categories are:

- mutually exclusive and additive;
- subsets;
- overlapping attributes;
- cumulative events;
- or period flows.

## Classification Tests

Before assigning a supply state, the reporting owner should assess the following tests.

### 1. Canonical Token Test

Are the units canonical FUZE under the verified network and token contract, or are they:

- bridged;
- wrapped;
- represented;
- synthetic;
- pending migration;
- or unsupported?

### 2. Allocation Test

Which approved allocation category owns the units?

Is the category mapping current and reconciled?

### 3. Control Test

Who can move, withdraw, redirect, freeze, upgrade, or recover the units?

Relevant control can include:

- FUZE treasury;
- multisig;
- contract admin;
- custodian;
- partner;
- recipient;
- exchange;
- market maker;
- bridge;
- or shared authority.

### 4. Beneficial-Control Test

Who has the economic right to the units, distinct from operational custody?

### 5. Transferability Test

Can the controlling holder transfer the units without:

- lock;
- vesting;
- contract restriction;
- legal restriction;
- custody approval;
- claim condition;
- program limitation;
- return obligation;
- or another material constraint?

### 6. Availability Test

Are the units available to users or markets now, or merely:

- planned;
- committed;
- funded;
- prepared;
- claimable;
- or awaiting release?

### 7. Restriction Test

Do any continuing restrictions remain after an unlock, vesting event, claim, release, or transfer?

### 8. Custody Test

Where are the units held?

Possible classes include:

- FUZE treasury;
- allocation vault;
- vesting contract;
- claim contract;
- self-custody recipient;
- smart account;
- multisig;
- partner wallet;
- exchange hot wallet;
- exchange cold wallet;
- omnibus custodian;
- liquidity pool;
- market-maker wallet;
- bridge contract;
- protocol contract;
- or unsupported location.

### 9. Return and Recovery Test

Can unused, cancelled, disputed, expired, or improperly used tokens return to FUZE-controlled allocation custody?

### 10. Market-Availability Test

Are the units actually available for market transfer or trading, or held as:

- venue inventory;
- market-maker inventory;
- one-sided liquidity;
- locked liquidity;
- controlled collateral;
- or operational reserves?

### 11. Finality Test

Has the relevant transaction, claim, bridge, provider, or custody event reached the required confirmation or finality state?

### 12. Evidence-Freshness Test

Does the classification use current:

- wallet labels;
- contract states;
- custody records;
- restrictions;
- partner terms;
- venue data;
- and reporting methods?

### 13. Method-Consistency Test

Does the classification follow the same published methodology as prior periods?

If the method changed, is the change disclosed and are prior figures restated where necessary?

No single test determines every case.

Material judgment should be documented.

## Circulating-Supply Methodology

FUZE should publish a versioned circulating-supply methodology.

### Required Methodology Fields

| Field | Required definition |
|---|---|
| Methodology identifier | Stable name and version |
| Effective date | Date or block from which the method applies |
| Network and token | Canonical chain and verified contract |
| Measurement point | Timestamp, block, and source cutoff |
| Total-supply source | Contract, ledger, or other authoritative source |
| Allocation source | Approved allocation-table version |
| Controlled-wallet registry | Included treasury, vault, contract, partner, program, venue, and custody records |
| Inclusion rule | Conditions under which units count as circulating |
| Exclusion rule | Conditions under which units remain non-circulating |
| Lock and vesting treatment | Locked, unlocked, vesting, vested, and released classification |
| Claim treatment | Eligible, claimable, claimed, unclaimed, transferred, and restricted treatment |
| Partner treatment | Partner custody, lock, use, onward transfer, and return rights |
| Exchange treatment | Hot, cold, omnibus, deposit, withdrawal, beneficial ownership, and listing-state treatment |
| Liquidity treatment | Committed, deposited, paired, active, withdrawn, and returned treatment |
| Market-maker treatment | Inventory, venue custody, authority, return rights, and ordinary-circulation treatment |
| Bridge treatment | Canonical lock, representation mint, burn, release, and duplicate-supply prevention |
| Contract treatment | Product, staking, claim, vesting, utility, market, and unsupported contracts |
| Burn treatment | Technical and governance evidence required |
| Pending treatment | Unresolved classification and disclosure method |
| Correction method | Error correction and restatement process |
| Reviewer | Responsible preparer and reviewer |
| Limitations | Known gaps, third-party dependencies, and assumptions |
| Current-as-of date | Time to which the method and data apply |

### Inclusion Principle

A unit should count as circulating only when the approved methodology finds it reasonably available in user or market circulation and not subject to a material continuing exclusion.

### Exclusion Principle

A unit may remain non-circulating when it is:

- controlled by FUZE;
- held in an allocation vault;
- locked;
- unvested;
- unreleased;
- only planned or committed;
- claim-funded but unclaimed;
- subject to a material partner restriction;
- recoverable under continuing return rights;
- held as controlled market inventory;
- represented by another backed token already counted elsewhere;
- pending classification;
- or otherwise unavailable under the published method.

### Methodology Judgment

Reasonable methodologies can differ, especially for:

- unclaimed but claimable tokens;
- exchange omnibus wallets;
- partner custody;
- market-maker inventory;
- liquidity-pool balances;
- bridge representations;
- and contract-held tokens.

FUZE should publish its method and explain material differences from third-party methods.

## Exchange and Custodian Treatment

### Exchange Deposit Does Not Equal Listing

A token transfer to an exchange-associated wallet does not independently establish:

- formal application;
- approval;
- listing;
- deposits enabled;
- withdrawals enabled;
- trading live;
- liquidity;
- or beneficial ownership.

### Exchange Custody Classes

A report may distinguish:

- FUZE-controlled exchange account;
- market-maker exchange account;
- partner exchange account;
- user deposit balance;
- exchange hot wallet;
- exchange cold wallet;
- omnibus exchange wallet;
- and unidentified exchange-associated balance.

### Beneficial Ownership

An exchange wallet can contain balances belonging to multiple parties.

Address ownership alone may not identify beneficial ownership or circulation status.

### Custodian Treatment

Institutional or omnibus custody requires evidence of:

- beneficial owner or account class;
- transfer restrictions;
- withdrawal authority;
- lock or agreement status;
- return rights;
- and reporting scope.

## Liquidity and Market-Operation Treatment

Liquidity-related supply should use specialist classifications.

### Distinct States

Reports should distinguish:

- liquidity budget approved;
- liquidity committed;
- tokens transferred to market-operation custody;
- tokens paired;
- tokens deposited into a pool;
- tokens deposited to a venue;
- tokens held as market-maker inventory;
- tokens active in a position;
- tokens withdrawn;
- tokens returned;
- and current position balance.

### No Automatic Circulation Assumption

A liquidity-pool or market-maker balance can have different circulation treatment depending on:

- position structure;
- control;
- transferability;
- venue;
- lock;
- return rights;
- beneficial availability;
- and methodology.

### Market Outcome Separation

Liquidity deployment does not guarantee:

- active trading;
- stable depth;
- narrow spread;
- volume;
- demand;
- listing;
- price support;
- price appreciation;
- or financial return.

## Bridge and Represented-Supply Treatment

A bridge can create a representation of canonical FUZE on another network.

The reporting method should identify:

- canonical source network;
- canonical token contract;
- bridge or representation contract;
- locked canonical amount;
- minted represented amount;
- burned represented amount;
- released canonical amount;
- fees and rounding;
- operator and admin controls;
- paused or compromised state;
- and reconciliation status.

### One-to-One Reconciliation

Where the representation is fully backed:

```text
represented FUZE outstanding
<= canonical FUZE locked or otherwise verifiably backing the representation
```

Canonical and represented units should not be counted twice as new economic supply.

### Unsupported Representations

An unsupported token using FUZE branding or ticker should not enter FUZE supply reporting without verification.

## Reconciliation Equations

### Total Supply

```text
current total supply
= circulating supply
+ non-circulating supply
```

### Exclusive State Reconciliation

```text
opening state balance
+ inbound state transitions
- outbound state transitions
+ returns and recoveries
+/- corrections
= closing state balance
```

### Circulating-Supply Movement

```text
opening circulating supply
+ newly classified circulating
- returned or reclassified out of circulation
- verifiably burned circulating units
+/- corrections and restatements
= closing circulating supply
```

### Allocation Reconciliation

For each allocation category:

```text
opening category balance
+ approved inward reclassification
+ returned or recovered category units
- approved outward reclassification
- category releases, deployments, or burns
+/- corrections
= closing category balance
```

### Fixed-Supply Reconciliation

```text
sum of all mutually exclusive allocation-category balances
= 500,000,000 FUZE
```

unless a separately approved and technically valid supply-changing event is reflected in the governing model.

### Bridge Reconciliation

```text
canonical circulating and non-circulating units
+ represented units not already counted through canonical backing
= no more than the approved economic supply under the methodology
```

The report should explain the exact bridge accounting rather than relying on this simplified expression.

### Pending Classification

```text
current total supply
= classified circulating
+ classified non-circulating
+ pending classification
+ verifiably burned or removed amount where applicable
```

Pending classification should not be hidden inside a stronger category.

## Point-in-Time Report

A point-in-time report should include:

- report identifier and version;
- measurement timestamp and timezone;
- block number where applicable;
- network and canonical token contract;
- total supply;
- circulating supply;
- non-circulating supply;
- pending-classification amount;
- mutually exclusive state buckets;
- allocation summary;
- custody and contract summary;
- methodology version;
- source cutoff;
- corrections and limitations;
- preparer and reviewer;
- and current status.

## Period Movement Report

A period movement report should include:

- opening measurement point;
- closing measurement point;
- opening balances;
- allocation events;
- custody transfers;
- commitments;
- locks and unlocks;
- vesting events;
- eligibility and claim events;
- releases;
- program and partner deployments;
- liquidity and market-operation movements;
- bridge events;
- returns and recoveries;
- reclassifications;
- burns;
- corrections;
- unresolved items;
- closing balances;
- and transaction, governance, contract, or report references.

## Public Reporting Schema

| Field | Description |
|---|---|
| Report identifier | Stable public reference |
| Report type | Point-in-time, period movement, event, correction, or restatement |
| Version | Report version |
| Scope | Network, token contract, allocations, wallets, contracts, custodians, bridges, venues, and systems included |
| Measurement point | Timestamp, timezone, block, and data cutoff |
| Total supply | Current authoritative total-supply figure |
| Allocation-table version | Controlling fixed-supply model |
| Methodology version | Circulating-supply classification method |
| Circulating supply | Amount under the published method |
| Non-circulating supply | Mutually exclusive reconciled remainder |
| Pending classification | Amount awaiting final evidence-backed classification |
| State detail | Exclusive balances and separately labeled overlapping attributes |
| Period events | Vesting, claims, releases, deployments, returns, burns, and corrections |
| Allocation detail | Source category for material movements |
| Custody detail | Public-safe wallet, vault, contract, venue, or custody classes |
| Evidence | Transactions, contracts, governance, vaults, reports, or other public-safe references |
| Exceptions | Unresolved, estimated, delayed, disputed, or unsupported items |
| Prior-period change | Corrections, restatements, and methodology changes |
| Owner and review | Responsible preparer and reviewer roles |
| Limitations | Known data, classification, provider, bridge, exchange, privacy, or timing limitations |
| Current status | Draft, under review, published, corrected, superseded, or archived |
| Current-as-of date | Time to which the report applies |

Human-readable summaries and machine-readable exports should use the same definitions and totals.

## Interpretation Examples

### Controlled Treasury Transfer

FUZE moves tokens from one approved treasury wallet to another after a custody update.

**Likely report treatment:**

- source custody decreases;
- destination custody increases;
- allocation remains unchanged;
- restriction remains unchanged;
- circulating supply remains unchanged when control and availability remain equivalent.

### Vault Deposit

Tokens move from a treasury wallet into an approved allocation vault.

**Likely report treatment:**

- custody changes;
- controlled or locked classification may strengthen;
- circulation does not increase.

### Team Vesting Event

A scheduled amount satisfies vesting but remains in a controlled vesting contract.

**Likely report treatment:**

- unvested decreases;
- vested-unreleased increases;
- circulation may remain unchanged.

### Vesting Release to Recipient

A vested amount transfers to the recipient's self-custody wallet with no continuing material restriction.

**Likely report treatment:**

- vested-unreleased decreases;
- released increases;
- recipient custody increases;
- circulating supply may increase under the methodology.

### Community Approval Pending Release

A participant receives an approved allocation record while claim, lock, or release conditions remain incomplete.

**Likely report treatment:**

- planned or committed state;
- no release;
- no circulation increase.

### Claim Process Funded

Tokens move into a claim contract before the claim window opens.

**Likely report treatment:**

- controlled claim funding or operational deployment;
- not automatically claimable;
- not automatically circulating.

### Claim Opens

Eligible recipients can now claim.

**Likely report treatment:**

- eligible or funded amount may become claimable;
- no automatic transfer;
- circulation treatment follows the published method.

### Migration Claim

An eligible legacy holder completes a claim and receives tokens subject to a continuing lock.

**Likely report treatment:**

- claimable decreases;
- claimed and recipient-custodied increases;
- circulating supply may remain unchanged while the lock continues.

### Partner Deployment

Tokens transfer to a partner wallet subject to milestone, onward-transfer, and return restrictions.

**Likely report treatment:**

- partner-deployed or externally custodied;
- not automatically ordinary circulation.

### Liquidity-Pool Deployment

Tokens move from a controlled market-operations wallet into an approved liquidity pool.

**Likely report treatment:**

- liquidity-deployed amount increases;
- source market inventory decreases;
- circulating classification follows the methodology and position structure;
- no conclusion about depth, spread, volume, or price.

### Exchange Deposit

Tokens move into an exchange-associated address.

**Likely report treatment:**

- exchange or venue custody pending beneficial-owner and availability analysis;
- no automatic statement that listing or trading is live.

### Bridge Mint

Canonical FUZE is locked and an equivalent representation is minted elsewhere.

**Likely report treatment:**

- canonical bridge-locked amount increases;
- represented amount increases;
- no increase in approved economic supply when fully backed;
- circulation treatment follows the methodology across both networks.

### Program Return

Unused incentive tokens return to the original allocation vault.

**Likely report treatment:**

- deployed or committed balance decreases;
- returned controlled balance increases;
- circulating supply may decrease if the units had previously been classified as circulating.

### Burn

Tokens enter an approved irreversible burn mechanism and the result is technically verified.

**Likely report treatment:**

- burned amount increases;
- current onchain total supply or usable-supply calculation changes according to the token design and methodology;
- prior allocation and circulation figures are reconciled.

## Allocation, Wallet, Contract, and Custody Labels

Public labels can support interpretation but do not replace the underlying methodology.

A label should identify, where appropriate:

- allocation category;
- function;
- custody class;
- network;
- contract or wallet type;
- active, replaced, deprecated, paused, or closed status;
- effective date;
- authoritative source;
- and current-as-of date.

### Mixed-Purpose Addresses

If one address holds multiple allocation categories or states, the public label should not imply one uniform purpose.

A supporting subledger and public-safe explanation are required.

### Address Ownership Versus Identity

An address label can identify a custody or operating role.

It does not establish the personal identity behind the address without separate evidence.

Public reporting should protect wallet-person mappings.

### Replaced and Deprecated Addresses

A replaced address should identify:

- replacement date;
- successor address or authoritative source where public-safe;
- remaining balance treatment;
- migration status;
- and whether the old address remains monitored.

## Unlock, Vesting, Claim, and Release Calendar

A public calendar may show scheduled, earliest, estimated, conditional, or completed events.

Each entry should identify:

- allocation category;
- event type;
- amount or calculation method;
- scheduled or earliest time;
- timezone or block basis;
- condition;
- current status;
- custody source;
- expected resulting state;
- expected circulation effect;
- authority or report reference;
- and current-as-of date.

### Calendar Statuses

Possible statuses include:

- proposed;
- scheduled;
- conditional;
- awaiting evidence;
- approved;
- delayed;
- partially completed;
- completed;
- cancelled;
- corrected;
- or superseded.

A calendar entry is not evidence that an event occurred.

Completed events require transaction or system evidence and post-event reconciliation.

## Third-Party Data Providers

Exchanges, explorers, market-data services, analytics providers, partners, and community dashboards can use different supply methodologies.

FUZE should publish:

- its authoritative methodology;
- verified current figures;
- network and token-contract references;
- public wallet and contract labels;
- report history;
- correction history;
- methodology-change history;
- and a route for material discrepancy reports.

### Common Sources of Difference

Differences may arise from:

- measurement time or block;
- outdated wallet labels;
- unknown controlled wallets;
- exchange omnibus treatment;
- unclaimed claim balances;
- vesting-contract treatment;
- partner restrictions;
- liquidity-pool classification;
- market-maker inventory;
- bridge representations;
- burns;
- returned balances;
- pending classifications;
- or methodology differences.

### Discrepancy Record

A discrepancy record should identify:

1. provider or report;
2. provider figure;
3. FUZE figure;
4. measurement point;
5. methodology difference;
6. affected wallets, contracts, or categories where public-safe;
7. evidence;
8. owner;
9. communication status;
10. correction or explanation;
11. current status; and
12. closure.

A difference does not by itself prove intentional misreporting.

It should be investigated and explained.

## Corrections and Restatements

### Correction

A correction fixes an error while retaining the same core methodology.

Examples include:

- wrong amount;
- duplicate transaction;
- omitted wallet;
- incorrect address label;
- wrong allocation mapping;
- wrong event date;
- incorrect claim count;
- missed return;
- or arithmetic error.

### Restatement

A restatement revises a prior published figure because of:

- a material error;
- newly available evidence;
- a methodology change;
- a bridge or exchange classification change;
- a custody or beneficial-control correction;
- or another material re-evaluation.

### Correction or Restatement Record

The record should identify:

1. affected report;
2. affected period and measurement point;
3. prior figure;
4. revised figure;
5. amount of change;
6. affected categories;
7. reason;
8. source evidence;
9. methodology version before and after;
10. reviewer;
11. approval;
12. effective date;
13. linked downstream reports or providers;
14. public explanation;
15. current status; and
16. archive reference.

Prior versions should remain accessible and visibly marked as corrected or superseded.

## Methodology Changes

A methodology change should be approved and disclosed before or with publication.

The change record should identify:

- prior method;
- new method;
- reason;
- affected categories;
- affected current figure;
- affected historical figures;
- whether history is restated;
- implementation date;
- reviewer;
- approval;
- third-party notification;
- and limitations.

A methodology change should not be used silently to produce a preferred supply number.

## Reporting Governance

### Roles

Possible roles include:

- data owner;
- allocation owner;
- custody-registry owner;
- contract and onchain-data owner;
- vesting and claim owner;
- market-operation owner;
- bridge owner;
- methodology owner;
- preparer;
- reviewer;
- approver;
- and publisher.

### Separation of Duties

Where proportionate:

- the preparer should not be the only approver;
- the movement executor should not unilaterally classify the circulation effect;
- the market-operation owner should not silently change the public supply methodology;
- and the publisher should not alter source figures outside the correction process.

### Evidence Retention

The reporting package should retain:

- data extracts;
- wallet and contract registry version;
- allocation table;
- movement ledger;
- vesting and claim records;
- bridge and exchange evidence;
- liquidity and market-operation records;
- methodology;
- calculations;
- review notes;
- approvals;
- published report;
- and correction history.

## Public Privacy and Security Boundary

Supply transparency should not expose:

- private identity behind a wallet;
- personal wallet-person mappings;
- private beneficiary records;
- private employment or advisor agreements;
- private partner terms;
- exchange-account credentials;
- custodian credentials;
- signer identities where not approved;
- private keys;
- recovery material;
- exact security procedures;
- private market strategy;
- or exploitable treasury patterns.

Public transparency can use:

- approved wallet and contract labels;
- transaction hashes;
- aggregate allocation and state figures;
- methodology;
- governance references;
- report hashes;
- and correction history

where disclosure is accurate, approved, and safe.

## Relationship to Adjacent Systems

| System or process | Primary role | Why it remains separate |
|---|---|---|
| Controlled circulation | Governs movement authorization, custody, state transitions, and reconciliation | Operating control framework |
| Release and circulation clarity | Defines terminology, methodology, interpretation, and public reporting | Reporting and communication standard |
| Token allocation table | Defines fixed category amounts and mandates | Allocation does not establish release or circulation |
| Vault and reserve policy | Defines custody, reserve purpose, and control | Custody does not equal release |
| Vault-by-vault release rules | Defines category-specific release conditions | Release conditions differ by category |
| Vesting | Defines time, service, milestone, or hybrid progression | Vested does not equal released or circulating |
| Claim process | Defines eligibility and recipient action | Claimable, claimed, transferred, and circulating remain separate |
| Platform Credits | Product-consumption units | Outside FUZE token supply calculations |
| Stablecoin compensation | Business-payment settlement | Outside FUZE token supply calculations |
| Approved distributable value | Reviewed value from product-revenue pools | Separate unit, ledger, and process |
| Wallet-based participation | Activation-gated eligibility, claim, and payout system | Does not alter FUZE token circulation unless FUZE token is separately used |
| Liquidity and listing policy | Governs market structure and venue process | Supply availability does not establish listing or liquidity |

## Status and Evidence

This paper defines FUZE token release and circulation terminology and reporting methodology.

It does not independently prove that any current unlock, vesting event, claim window, release, bridge, liquidity deployment, exchange deposit, burn, or circulating-supply amount exists.

| Status claim | Evidence direction |
|---|---|
| Fixed total supply verified | Canonical token contract, network, block or time, total-supply call, allocation model, and review record |
| Allocation verified | Approved allocation table, category amounts, authority, version, and fixed-supply reconciliation |
| Custody verified | Wallet, contract, custodian, control class, allocation mapping, balance, and current status |
| Tokens locked | Amount, custody, contract or policy, restriction, effective period, and evidence |
| Tokens unlocked | Specific restriction ended, amount, effective time, continuing restrictions, and custody state |
| Tokens vesting | Schedule, amount, beneficiary class, custody, calculation, and current status |
| Tokens vested | Satisfied condition, amount, calculation, reviewer, and continuing state |
| Tokens claimable | Active process, eligibility, amount, claim window, funding, and current status |
| Tokens claimed | Claim action, amount, recipient or wallet reference, time, transfer status, and continuing restrictions |
| Tokens approved for release | Release condition, authority, amount, source, destination, and instruction |
| Tokens released | Transaction or system evidence, confirmation, custody effect, allocation effect, and final state |
| Tokens operationally deployed | Program, partner, contract, incentive, liquidity, market, or other approved reference and restrictions |
| Tokens externally custodied | Custodian or recipient class, beneficial-control evidence, restrictions, and current state |
| Tokens circulating | Published methodology, measurement point, registry version, inclusion and exclusion treatment, calculation, and report |
| Tokens returned | Original movement, reason, amount, transaction, destination custody, allocation, and revised state |
| Tokens burned | Approved irreversible mechanism, canonical token evidence, amount, authority, and supply reconciliation |
| Bridge representation verified | Canonical lock, representation contract, minted and burned amounts, backing reconciliation, and current status |
| Report corrected | Original report, error, evidence, revised figure, reviewer, approval, and current version |
| Methodology changed | Prior and new methods, reason, impact, approval, effective date, and restatement treatment |

The following do not independently establish release or circulation status:

- this paper;
- a wallet label;
- a token transfer;
- a wallet screenshot;
- a vesting schedule draft;
- a calendar entry;
- a claim announcement;
- a contract deployment;
- an exchange-associated address;
- a liquidity-pool balance;
- a bridge token;
- code;
- a repository;
- a partner discussion;
- a listing discussion;
- or token price activity.

## Allocation, Release, Circulation, Market, and Outcome Separation

The following remain separate:

- fixed total supply;
- onchain total supply;
- allocation;
- custody;
- available allocation balance;
- planning;
- commitment;
- reservation;
- lock;
- unlock;
- vesting;
- vested status;
- eligibility;
- claimability;
- claim action;
- release approval;
- transaction execution;
- release;
- operational deployment;
- external custody;
- circulating-supply classification;
- exchange deposit;
- DEX access;
- CEX discussion;
- CEX application;
- CEX approval;
- listing;
- deposits enabled;
- withdrawals enabled;
- trading live;
- liquidity;
- depth;
- spread;
- volume;
- token demand;
- market price;
- income;
- revenue share;
- and financial return.

A release or circulation increase does not guarantee:

- listing;
- deposits or withdrawals;
- trading access;
- active liquidity;
- market depth;
- narrow spread;
- trading volume;
- token demand;
- price support;
- price appreciation;
- income;
- revenue share;
- or financial return.

## Public Boundary

This paper publishes FUZE token supply terminology, classification tests, methodology requirements, reporting schemas, reconciliation rules, event interpretation, correction processes, and public disclosure boundaries.

It does not publish or establish current:

- token contract address;
- wallet or vault addresses;
- signer identities;
- unlock dates;
- vesting schedules;
- beneficiary identities;
- claim windows;
- release amounts;
- partner allocations;
- incentive budgets;
- bridge contracts;
- liquidity deployments;
- market-maker inventory;
- exchange deposits;
- circulating-supply amount;
- DEX activation;
- CEX application;
- CEX approval;
- listing;
- deposits or withdrawals;
- trading status;
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

unless those details are separately approved and supported by current evidence in a token contract record, allocation report, custody registry, vault report, vesting record, claim report, controlled-circulation ledger, bridge report, market-operation report, specialist paper, or public status record.

Circulation figures require current contract, wallet, custody, control, restriction, claim, exchange, bridge, liquidity, market-operation, return, burn, and event evidence.

## Key Takeaways

- FUZE supply reporting uses distinct terms for allocation, custody, lock, vesting, claimability, release, deployment, external custody, return, burn, and circulation.
- The fixed supply is 500,000,000 FUZE under the approved allocation model.
- An onchain transfer, unlock, vesting event, claim opening, exchange deposit, bridge mint, or liquidity deployment does not automatically create ordinary circulating supply.
- Point-in-time state balances, period movements, and cumulative events are different report types.
- Mutually exclusive buckets may be added; overlapping attributes must not be double counted.
- Circulating supply requires a versioned methodology covering control, transferability, restrictions, custody, claims, exchanges, liquidity, market makers, bridges, returns, burns, and pending classifications.
- Exchange custody, liquidity positions, market-maker inventory, and bridge representations require specialist treatment rather than simple wallet-label assumptions.
- Reports should reconcile to total supply and identify their timestamp, block, registry version, allocation version, methodology version, evidence, limitations, and corrections.
- Third-party supply figures can differ because of timing, data, wallet labels, custody assumptions, or methodology; differences should be investigated and explained.
- Release, circulation, exchange access, listing, liquidity, demand, price support, income, revenue share, and financial return remain separate states and outcomes.
