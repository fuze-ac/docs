# FUZE Vault-by-Vault Release Rules

## Executive Summary

FUZE assigns its fixed **500,000,000 FUZE** supply to ten approved allocation categories.

Each category has a distinct mandate and therefore requires a distinct release basis.

This paper defines the evidence, authority, custody, destination, restriction, execution, reconciliation, and reporting conditions required before token units can move from each allocation vault or controlled category balance.

The common release sequence is:

```text
approved allocation and vault mandate
-> category-consistent release trigger
-> complete release packet
-> available and uncommitted balance check
-> beneficiary, destination, contract, program, partner, or venue verification
-> vesting, eligibility, claim, milestone, agreement, reserve, or market-condition review
-> required approvals
-> final pre-execution review
-> transaction or system execution
-> confirmation and finality
-> post-release custody and state classification
-> allocation, vault, program, and circulation reconciliation
-> public-safe reporting
-> return, cancellation, correction, suspension, closure, or archive
```

Each state is separate.

An approved allocation does not itself create:

- a beneficiary right;
- a grant;
- a commitment;
- a vesting schedule;
- eligibility;
- a claim;
- a release;
- circulation;
- liquidity;
- listing;
- income;
- revenue share;
- or financial return.

A release request does not become executable until its category-specific conditions are satisfied.

Approval does not equal execution.

Execution does not automatically equal circulation.

A token transfer can result in:

- controlled custody;
- locked custody;
- vesting custody;
- claim funding;
- participant custody;
- partner custody;
- program deployment;
- reserve utilization;
- liquidity or market-operation inventory;
- return custody;
- or another approved state.

Every material release should identify:

- release identifier;
- source allocation;
- source vault or custody;
- opening state;
- permitted purpose;
- release trigger;
- amount;
- recipient or destination class;
- eligibility, vesting, claim, milestone, agreement, program, reserve, or market condition;
- continuing restrictions;
- authority;
- execution evidence;
- final custody;
- final token state;
- circulation effect;
- return and correction treatment;
- public-reporting treatment;
- and current-as-of date.

This paper owns the category-specific release gates for:

1. Community Participation Allocation;
2. BOARD / Surfboard Migration;
3. Team Allocation;
4. Foundation Reserve;
5. Treasury Reserve;
6. Holder Incentives;
7. Ecosystem Growth & Partnerships;
8. Liquidity & Market Operations;
9. Advisors / Strategic Contributors; and
10. Transparency / Stability Reserve.

The allocation names, amounts, percentages, and mandates remain controlled by [FUZE Token Allocation Table](02-FUZE_TOKEN_ALLOCATION_TABLE_PUBLIC.md).

Common custody and reserve administration remain controlled by [FUZE Vault and Reserve Policy](14-FUZE_VAULT_AND_RESERVE_POLICY_PUBLIC.md).

Movement authorization and post-release classification remain controlled by [FUZE Controlled Circulation Policy](12-FUZE_CONTROLLED_CIRCULATION_POLICY_PUBLIC.md) and [FUZE Token Release and Circulation Clarity](13-FUZE_TOKEN_RELEASE_AND_CIRCULATION_CLARITY_PUBLIC.md).

## Purpose of This Paper

This paper explains:

- the public vault-by-vault release position;
- common release states;
- the release packet;
- common release gates;
- the approved allocation matrix;
- category-specific triggers and evidence;
- destination and custody treatment;
- vesting, claim, milestone, reserve, and market-operation boundaries;
- batch and program releases;
- final pre-execution review;
- execution and post-release classification;
- unused, cancelled, expired, returned, and recovered amounts;
- exceptions, amendments, and reclassification;
- suspension and incident treatment;
- allocation and vault reconciliation;
- public reporting;
- closure and archive;
- status and evidence requirements; and
- public limitations.

This paper does not replace:

- the token allocation table;
- vault-establishment records;
- individual grant agreements;
- vesting schedules;
- community-round terms;
- migration terms;
- incentive-program rules;
- partner or grant agreements;
- claim instructions;
- reserve-utilization decisions;
- liquidity or market-operation procedures;
- exchange-listing procedures;
- legal, accounting, tax, or compliance review;
- smart-contract specifications;
- private signer procedures;
- or the token risk register.

## Public Position

Vault balances are controlled capacity, not automatic distribution authority.

Release rules exist to preserve the purpose of each allocation and prevent one category from becoming a general-purpose token pool.

FUZE should not release token units from an allocation merely because:

- the vault holds a balance;
- the allocation appears in tokenomics;
- a recipient requests tokens;
- a partnership is announced;
- a contributor performed informal work;
- a wallet is connected;
- a holder owns tokens;
- a market opportunity exists;
- a listing is discussed;
- a product launches;
- or token price changes.

Every release requires a category-consistent purpose, current evidence, valid authority, available balance, verified destination, enforceable or recordable restrictions, execution evidence, and reconciliation.

These rules do not promise that the full amount of any allocation will be released, committed, claimed, vested, deployed, or circulated.

## Common Release States

| State | Evidence-backed meaning | What it does not establish |
|---|---|---|
| Allocated | Units belong to an approved fixed-supply category. | Commitment or release |
| Custodied | Units are held in an approved vault, wallet, contract, custodian, or account. | Availability or release authority |
| Available within allocation | Units remain uncommitted and usable only for an approved category purpose. | Approved movement |
| Proposed | A release request is being prepared. | Approval or recipient right |
| Under review | Evidence and conditions are being assessed. | Approval |
| Approved | Release conditions and decision authority are satisfied for the stated scope. | Execution |
| Committed | Units are reserved for an approved recipient, agreement, program, claim, reserve use, or market operation. | Transfer or circulation |
| Locked | Units remain subject to an enforceable restriction. | Vesting completion or release |
| Vesting | Units progress under an approved schedule or condition. | Vested or released status |
| Vested | The vesting condition is satisfied. | Transfer or circulation |
| Eligible | A recipient or wallet satisfies qualification rules. | Claimability or receipt |
| Claimable | An active process permits an eligible recipient to claim. | Claimed or transferred status |
| Claimed | The required claim action is complete. | Final transfer, unrestricted custody, or circulation |
| Approved for execution | Exact transaction parameters are authorized. | Submission |
| Submitted | Transaction or system instruction has been sent. | Confirmation or finality |
| Released | Units moved from the prior controlled state under an approved instruction. | Unrestricted circulation |
| Operationally deployed | Units entered an approved program, partner, reserve, liquidity, or market mechanism. | Ordinary holder circulation |
| Returned | Units moved back to approved category custody. | Immediate reuse |
| Recovered | Units were restored after error, cancellation, dispute, expiry, or incident. | Final availability |
| Suspended | Further activity is paused. | Cancellation or correction |
| Corrected | A later authorized record changes a prior amount or state while preserving history. | Erasure of the original event |
| Cancelled | The proposed or approved release no longer proceeds. | Removal of historical records |
| Closed | The release and remaining obligations are complete or controlled. | Future release authority |
| Archived | Historical records remain retained but are not current. | Active status |

`Approved`, `committed`, `claimable`, `vested`, `released`, `deployed`, and `circulating` are different states.

## Common Release Packet

Every material release should use a complete packet proportionate to the amount, purpose, destination, restrictions, irreversibility, and public impact.

### Core Fields

1. release identifier;
2. allocation category;
3. source vault or custody reference;
4. opening allocation and vault balance;
5. available and uncommitted balance;
6. purpose;
7. release trigger;
8. movement class;
9. recipient or destination class;
10. recipient, wallet, contract, partner, program, custodian, or venue verification;
11. amount;
12. calculation method where applicable;
13. applicable agreement, grant, migration, vesting, claim, incentive, reserve, or market reference;
14. conditions already satisfied;
15. conditions continuing after release;
16. lock, vesting, claim, transfer, use, sale, return, or disclosure restrictions;
17. jurisdiction and eligibility treatment where applicable;
18. duplicate, prior-release, prior-claim, prior-grant, or prior-deployment check;
19. legal, accounting, tax, compliance, security, treasury, or market review where applicable;
20. approval authority;
21. source and destination technical details;
22. expected final custody;
23. expected final token state;
24. expected circulation effect;
25. execution deadline or timelock;
26. return, cancellation, revocation, recovery, and correction treatment;
27. public and permissioned reporting treatment;
28. owner;
29. reviewer;
30. current status; and
31. current-as-of date.

### Core Decision Tests

The reviewer should confirm that:

- the request fits the allocation mandate;
- the source vault and allocation mapping are current;
- sufficient uncommitted balance exists;
- the amount is not already committed, released, claim-funded, deployed, or otherwise used;
- the trigger is active and supported;
- required evidence is complete and current;
- the recipient or destination is verified;
- restrictions are enforceable or reliably recorded;
- the movement does not bypass another allocation or process;
- the resulting custody and token state can be classified;
- the circulation effect can be reported under the current methodology;
- return and correction routes are defined;
- and the required authority is valid.

A release that fails a material test remains pending, enters remediation, or is rejected.

## Common Release Gates

### Gate 1: Allocation Integrity

The release must use the exact approved allocation category and purpose.

### Gate 2: Vault and Custody Integrity

The source vault, token, network, balance, authority, and status must be verified.

### Gate 3: Available-Balance Integrity

The release amount must not exceed:

```text
closing vault balance
- existing commitments
- active restrictions
- approved pending releases
- disputed or quarantined amounts
= available category balance
```

### Gate 4: Trigger Validity

The category-specific event must be active and satisfied.

### Gate 5: Recipient or Destination Validity

The recipient, wallet, contract, partner, program, venue, pool, custodian, or recovery destination must be verified for the stated purpose.

### Gate 6: Condition and Restriction Validity

Vesting, service, milestone, eligibility, claim, lock, transfer, use, return, and reporting conditions must be defined.

### Gate 7: Duplicate and Conflict Review

The release must not duplicate or conflict with:

- prior releases;
- prior claims;
- token grants;
- stablecoin compensation;
- Platform Credit grants;
- partner payments;
- migration claims;
- incentive awards;
- market inventory;
- or another program.

### Gate 8: Specialist Review

The required treasury, legal, accounting, tax, compliance, security, technical, partner, product, migration, community, or market review must be complete.

### Gate 9: Execution Readiness

The exact source, destination, token, network, amount, decimals, restrictions, transaction method, signer threshold, and timelock must match the approval.

### Gate 10: Reporting Readiness

The owner must be able to update allocation, vault, program, beneficiary or destination, controlled-circulation, and public-reporting records after execution.

## Approved Allocation Matrix

| Allocation vault | Approved amount | Share | Primary release basis |
|---|---:|---:|---|
| Community Participation Allocation | 110,000,000 FUZE | 22.00% | Approved community round, product-user route, contributor route, or community program |
| BOARD / Surfboard Migration | 25,000,000 FUZE | 5.00% | Verified legacy continuity under an active migration process |
| Team Allocation | 45,000,000 FUZE | 9.00% | Approved team grant under vesting, service, milestone, or role conditions |
| Foundation Reserve | 35,000,000 FUZE | 7.00% | Approved long-horizon stewardship, mission, governance, or continuity need |
| Treasury Reserve | 120,000,000 FUZE | 24.00% | Approved strategic treasury, infrastructure, platform, ecosystem, or operating deployment |
| Holder Incentives | 55,000,000 FUZE | 11.00% | Qualified outcome under an approved incentive program |
| Ecosystem Growth & Partnerships | 40,000,000 FUZE | 8.00% | Approved partner, integration, grant, distribution, or ecosystem milestone |
| Liquidity & Market Operations | 30,000,000 FUZE | 6.00% | Approved DEX, liquidity, custody, venue, market-making, or market-structure operation |
| Advisors / Strategic Contributors | 15,000,000 FUZE | 3.00% | Approved contribution, service period, milestone, or vesting event |
| Transparency / Stability Reserve | 25,000,000 FUZE | 5.00% | Exceptional trust, transparency, security, reporting, recovery, or stability action |
| **Total fixed supply** | **500,000,000 FUZE** | **100.00%** | **Ten purpose-specific release paths** |

An active program may impose stricter conditions while remaining inside the approved allocation mandate.

No program may weaken the common release gates without an approved exception and compensating controls.

## Community Participation Allocation

**Allocation:** 110,000,000 FUZE — 22.00% of fixed supply.

### Mandate

Supports approved community, product-user, contributor, participation, education, ecosystem-access, or similar public-participation routes.

### Valid Release Triggers

A release review may open when:

- an approved Community Participation Round becomes active;
- an approved product-user route opens;
- an approved contributor or community route opens;
- a participant satisfies an active program condition;
- an approved claim window opens;
- or another community program receives explicit authority.

### Required Evidence

- active program identifier and version;
- approved budget from this allocation;
- eligible participant class;
- qualification method;
- account, product-use, contribution, identity, wallet, or other route evidence required by the program;
- snapshot or measurement record where applicable;
- jurisdiction and participation treatment where applicable;
- duplicate, multi-account, abuse, fraud, and prior-allocation review;
- participant amount or calculation method;
- claim, lock, vesting, expiry, transfer, and cancellation rules;
- distribution or claim contract status where applicable;
- and reporting method.

### Destination Classes

Possible destinations include:

- controlled claim-funding vault;
- approved distribution contract;
- vesting contract;
- verified participant wallet;
- approved custodian;
- program account;
- or another approved community mechanism.

### Release and Circulation Treatment

Reports should distinguish:

- program budget;
- committed amount;
- eligible amount;
- claim-funded amount;
- claimable amount;
- claimed amount;
- released amount;
- locked or vesting amount;
- returned amount;
- expired amount;
- corrected amount;
- and circulating classification.

### Prohibited Shortcuts

The following do not independently authorize release:

- community membership;
- social-media activity;
- token holding;
- wallet connection;
- product registration;
- a referral;
- an informal contribution;
- or an announcement.

### Exception and Return Treatment

Rejected, duplicate, abusive, expired, cancelled, unclaimed, or invalid assignments remain in or return to category custody unless another treatment is formally approved.

The round workflow remains controlled by [FUZE Community Participation Round](06-FUZE_COMMUNITY_PARTICIPATION_ROUND_PUBLIC.md).

## BOARD / Surfboard Migration

**Allocation:** 25,000,000 FUZE — 5.00% of fixed supply.

### Mandate

Supports continuity treatment for eligible legacy BOARD / Surfboard positions under an approved migration process.

### Valid Release Triggers

A release review may open when:

- the migration process is active;
- the applicant submits required evidence;
- the legacy position is supportable under the current method;
- the conversion or allocation calculation is approved;
- and the destination and claim route are verified.

### Required Evidence

- migration program identifier and version;
- legacy asset, contract, network, pool, staking, custody, exchange, or position evidence;
- source snapshot or measurement date;
- self-custody, exchange-custody, staking, pool, intermediary, lost-access, or other approved treatment;
- claimant authority;
- destination-wallet or custodian verification;
- duplicate, prior-claim, prior-migration, and conflicting-ownership review;
- conversion or allocation formula;
- approved amount;
- lock, vesting, claim, expiry, and transfer rules;
- unresolved-evidence treatment;
- and reporting method.

### Destination Classes

Possible destinations include:

- migration claim contract;
- controlled migration vault;
- vesting contract;
- verified destination wallet;
- approved custodian;
- or another approved migration route.

### Release and Circulation Treatment

Reports should distinguish:

- submitted positions;
- verified positions;
- approved amount;
- disputed amount;
- claim-funded amount;
- claimable amount;
- claimed amount;
- released amount;
- locked amount;
- returned amount;
- and remaining allocation.

### Prohibited Shortcuts

The following do not independently authorize release:

- a wallet screenshot;
- a token balance without ownership evidence;
- an exchange screenshot without account authority;
- an unsupported intermediary record;
- a prior community statement;
- or a claimed legacy relationship.

### Exception and Return Treatment

Conflicting ownership, incomplete evidence, duplicate claims, unsupported calculations, wrong destinations, or disputed records enter suspension or correction.

Unused migration supply retains the migration mandate unless formally reclassified.

Detailed migration handling remains controlled by [FUZE BOARD / Surfboard Migration](20-FUZE_BOARD_SURFBOARD_MIGRATION_PUBLIC.md).

## Team Allocation

**Allocation:** 45,000,000 FUZE — 9.00% of fixed supply.

### Mandate

Supports approved long-term alignment of team members and operators through documented token grants.

Stablecoin salary, fees, expenses, bonuses, and other compensation remain separate.

### Valid Release Triggers

A release review may open when:

- an approved grant exists;
- the vesting start and schedule are effective;
- the applicable time, service, role, milestone, or performance condition is satisfied;
- no active suspension, termination, cancellation, or dispute blocks release;
- and the releasable calculation is approved.

### Required Evidence

- grant identifier;
- recipient class;
- approved grant amount;
- allocation source;
- grant date and effective date;
- cliff;
- vesting schedule;
- service, role, milestone, or performance conditions;
- vested-to-date calculation;
- previously released amount;
- cancelled, forfeited, or returned amount;
- current releasable amount;
- continuing lock or transfer restrictions;
- destination verification;
- termination and change-of-role treatment;
- approval;
- and reporting classification.

### Destination Classes

Possible destinations include:

- team vesting contract;
- controlled beneficiary sub-account;
- verified recipient wallet;
- approved custodian;
- or another approved grant structure.

### Release and Circulation Treatment

Reports should distinguish:

- granted;
- unvested;
- vesting;
- vested-unreleased;
- approved for release;
- released;
- recipient-custodied;
- continuing restricted;
- cancelled;
- returned;
- and circulating classification.

### Prohibited Shortcuts

Employment, title, work history, or informal promise alone does not authorize release.

A stablecoin compensation record does not substitute for a token grant and vesting record.

### Exception and Return Treatment

Unearned, unvested, cancelled, forfeited, or recovered amounts return to category control under the grant terms.

Corrections should preserve prior calculations and effective dates.

Detailed vesting treatment remains controlled by [FUZE Team Advisor Partner Vesting](19-FUZE_TEAM_ADVISOR_PARTNER_VESTING_PUBLIC.md).

## Foundation Reserve

**Allocation:** 35,000,000 FUZE — 7.00% of fixed supply.

### Mandate

Supports long-horizon stewardship, mission continuity, governance development, institutional continuity, ecosystem trust, and foundation-level responsibilities.

### Valid Release Triggers

A release review may open when:

- a foundation-level purpose is documented;
- other allocations are unsuitable or insufficient for that exact purpose;
- the amount and duration are proportionate;
- governance and custody authority approve the action;
- and the expected long-term effect and remaining capacity are documented.

### Required Evidence

- stewardship or continuity objective;
- category-fit explanation;
- alternatives considered;
- amount and sizing basis;
- destination and duration;
- restrictions;
- return, sunset, or closure treatment;
- governance, treasury, legal, accounting, tax, compliance, security, or specialist review where applicable;
- effect on remaining reserve capacity;
- and public-reporting treatment.

### Destination Classes

Possible destinations include:

- controlled stewardship vault;
- governance or mission program;
- approved contract;
- partner or institutional arrangement;
- vesting or restricted grant structure;
- recovery or continuity structure;
- or another approved foundation mechanism.

### Release and Circulation Treatment

Foundation-vault withdrawal, operational deployment, external custody, recipient release, and circulation should be reported separately.

### Prohibited Shortcuts

The Foundation Reserve should not become a default source for:

- ordinary operating expenses;
- routine compensation;
- community allocations;
- holder incentives;
- ordinary partner grants;
- or market operations

when another category is the appropriate source.

### Exception and Return Treatment

Cancelled initiatives, unused balances, recovered assets, and expired commitments should return to foundation or recovery custody.

A purpose outside the mandate requires formal reclassification.

## Treasury Reserve

**Allocation:** 120,000,000 FUZE — 24.00% of fixed supply.

### Mandate

Supports approved strategic treasury, infrastructure, platform, ecosystem, financing, continuity, acquisition, integration, reserve, or other treasury actions consistent with the allocation mandate.

It is strategic capacity, not an unrestricted general distribution pool.

### Valid Release Triggers

A release review may open when:

- a treasury proposal is complete;
- the action fits the reserve mandate;
- alternatives and source options are considered;
- sufficient uncommitted capacity exists;
- counterparty, contract, provider, program, or destination due diligence is complete;
- and required governance and specialist reviews approve the action.

### Required Evidence

- treasury proposal;
- use classification;
- amount and sizing basis;
- timing and duration;
- destination;
- alternatives considered;
- source balance and commitments;
- conversion, custody, lock, vesting, repayment, return, or counterparty terms;
- legal, accounting, tax, compliance, security, technical, or financial review where applicable;
- expected final token state;
- expected circulation effect;
- risk and incident treatment;
- and reporting method.

### Destination Classes

Possible destinations include:

- another controlled treasury vault;
- approved reserve vault;
- strategic contract;
- provider or custodian;
- partner or institutional structure;
- product or ecosystem program;
- acquisition or financing structure;
- recovery vault;
- or another approved treasury destination.

### Release and Circulation Treatment

The packet should identify whether the event is:

- custody transfer;
- reserve designation;
- commitment;
- conversion;
- collateralization;
- operational deployment;
- external release;
- return;
- recovery;
- or reclassification.

Not every treasury withdrawal increases circulation.

### Prohibited Shortcuts

Treasury Reserve should not be treated as a standing source for:

- community participation;
- migration;
- holder incentives;
- team or advisor grants;
- routine partner allocations;
- or approved distributable value

without the proper category or formal reclassification.

### Exception and Return Treatment

Failed, cancelled, excess, expired, recovered, or repaid amounts return to treasury or recovery custody and require renewed classification before reuse.

## Holder Incentives

**Allocation:** 55,000,000 FUZE — 11.00% of fixed supply.

### Mandate

Supports approved loyalty, product-use, referral, campaign, recognition, contribution, holding, engagement, or other measurable incentive programs.

### Valid Release Triggers

A release review may open when:

- an approved incentive program is active;
- the measurement period or qualifying event is complete;
- the participant satisfies the published rules;
- the amount is calculated under the approved method;
- abuse and duplicate checks pass;
- and the claim or delivery route is active.

### Required Evidence

- program identifier and version;
- objective;
- duration and measurement period;
- approved budget;
- eligible participant class;
- measurable behavior or qualification;
- calculation method;
- snapshot or event data;
- participant or wallet qualification;
- duplicate, sybil, bot, fraud, reversal, refund, and manipulation controls;
- earned amount;
- claim or delivery route;
- expiry, lock, vesting, transfer, and cancellation rules;
- and reporting method.

### Destination Classes

Possible destinations include:

- incentive claim contract;
- controlled program vault;
- vesting or lock contract;
- verified recipient wallet;
- approved custodian;
- or another approved incentive route.

### Release and Circulation Treatment

Reports should distinguish:

- approved budget;
- committed budget;
- measured or provisional amount;
- qualified or earned amount;
- claim-funded amount;
- claimable amount;
- distributed amount;
- locked amount;
- expired amount;
- reversed or recovered amount;
- remaining amount;
- and circulating classification.

### Prohibited Shortcuts

Token holding, wallet connection, social activity, referral submission, or product use does not create an incentive right unless an active program expressly defines it.

### Exception and Return Treatment

Invalid, refunded, reversed, duplicate, abusive, fraudulent, expired, or unclaimed qualifications are cancelled, corrected, or recovered under the program rules.

A new campaign requires its own budget, qualification method, and release packet.

## Ecosystem Growth & Partnerships

**Allocation:** 40,000,000 FUZE — 8.00% of fixed supply.

### Mandate

Supports approved partnerships, integrations, grants, ecosystem growth, distribution, developer support, market access preparation, product collaboration, education, events, or other category-consistent initiatives.

### Valid Release Triggers

A release review may open when:

- an approved agreement or grant exists;
- the relationship and counterparty are verified;
- the applicable milestone, service period, deliverable, activation, or vesting condition is satisfied;
- the amount and schedule are approved;
- and continuing obligations and return rights are documented.

### Required Evidence

- partner, grantee, or program identifier;
- agreement or authority;
- purpose and category fit;
- deliverable, milestone, service period, or activation condition;
- acceptance evidence;
- approved amount and schedule;
- vesting, lock, transfer, onward-use, sale, disclosure, and return restrictions;
- counterparty and destination verification;
- conflict and related-party review where applicable;
- legal, accounting, tax, compliance, security, technical, or market review where applicable;
- termination and clawback treatment;
- and reporting classification.

### Destination Classes

Possible destinations include:

- partner vesting contract;
- grant contract;
- controlled partner sub-account;
- verified partner wallet;
- approved custodian;
- integration or program contract;
- or another approved ecosystem destination.

### Release and Circulation Treatment

Reports should distinguish:

- approved grant or partner amount;
- committed amount;
- milestone-earned amount;
- vesting amount;
- released amount;
- partner-custodied amount;
- restricted amount;
- returned or recovered amount;
- and circulating classification.

### Prohibited Shortcuts

A partnership discussion, memorandum, announcement, event appearance, logo placement, introduction, or non-binding proposal does not authorize release.

### Exception and Return Treatment

Incomplete milestones, terminated relationships, unused grants, material breach, invalid destination, or failed integration follow the agreement's cancellation, vesting, return, recovery, or correction treatment.

## Liquidity & Market Operations

**Allocation:** 30,000,000 FUZE — 6.00% of fixed supply.

### Mandate

Supports approved DEX liquidity, market-making, custody, venue preparation, inventory, market-structure, listing-support preparation, and related operational activity.

It does not guarantee listing, liquidity, spread, depth, volume, demand, price, or financial return.

### Valid Release Triggers

A release review may open when:

- an approved market-structure purpose exists;
- the DEX, pool, venue, custodian, market maker, provider, or counterparty is verified;
- the operating plan and inventory limits are approved;
- custody and execution routes are ready;
- monitoring and return controls exist;
- and legal, treasury, security, accounting, compliance, and market reviews are complete where applicable.

### Required Evidence

- operation identifier;
- market purpose;
- DEX, venue, pool, custodian, provider, or counterparty class;
- FUZE amount;
- paired asset and amount where applicable;
- source and destination custody;
- pricing range, inventory, term, fee, withdrawal, and service parameters where applicable;
- market-maker or provider agreement where applicable;
- authority and transaction limits;
- monitoring owner;
- reconciliation method;
- pause and incident controls;
- return and recovery rights;
- circulating-supply methodology treatment;
- and public-reporting treatment.

### Destination Classes

Possible destinations include:

- market-operation vault;
- multisig operating wallet;
- DEX pool or position manager;
- market-maker wallet;
- approved custodian;
- venue account;
- smart contract;
- bridge custody;
- or another approved market-structure destination.

### Release and Circulation Treatment

Reports should distinguish:

- approved budget;
- committed inventory;
- transferred inventory;
- paired amount;
- deposited amount;
- active-position amount;
- market-maker inventory;
- venue custody;
- withdrawn amount;
- returned amount;
- current position balance;
- and circulating classification.

### Prohibited Shortcuts

The following do not independently authorize release:

- a listing discussion;
- a market-maker proposal;
- a venue account;
- a pool deployment draft;
- token price movement;
- community demand;
- or a desire to support price.

### Exception and Return Treatment

Unused inventory, failed transactions, withdrawn positions, terminated arrangements, unsupported venues, provider incidents, excess inventory, and recovered balances return to controlled category or recovery custody.

DEX-first and possible CEX-later treatment remains controlled by [FUZE Liquidity and Listing Policy](21-FUZE_LIQUIDITY_AND_LISTING_POLICY_PUBLIC.md).

## Advisors / Strategic Contributors

**Allocation:** 15,000,000 FUZE — 3.00% of fixed supply.

### Mandate

Supports approved long-term alignment for advisors and strategic contributors through documented grants tied to service, contribution, milestone, role, or vesting conditions.

Short-term work compensation remains separate.

### Valid Release Triggers

A release review may open when:

- an approved grant exists;
- the role or contribution scope is current;
- the applicable service period, milestone, contribution, or vesting condition is satisfied;
- no active conflict, termination, suspension, cancellation, or dispute blocks release;
- and the releasable calculation is approved.

### Required Evidence

- grant identifier;
- recipient class;
- role and contribution scope;
- grant amount;
- effective date;
- cliff and vesting schedule;
- service, milestone, contribution, or performance condition;
- accepted work or contribution evidence;
- vested-to-date calculation;
- previously released amount;
- cancelled, forfeited, or returned amount;
- current releasable amount;
- conflict, related-party, confidentiality, and termination treatment;
- continuing restrictions;
- destination verification;
- approval;
- and reporting classification.

### Destination Classes

Possible destinations include:

- advisor or contributor vesting contract;
- controlled beneficiary sub-account;
- verified recipient wallet;
- approved custodian;
- or another approved grant structure.

### Release and Circulation Treatment

Reports should distinguish:

- granted;
- unvested;
- vested-unreleased;
- approved for release;
- released;
- continuing restricted;
- cancelled;
- returned;
- and circulating classification.

### Prohibited Shortcuts

An introduction, recommendation, public support, meeting, informal advice, title, announcement, or stablecoin service payment does not establish a token-grant release.

### Exception and Return Treatment

Unearned, unvested, cancelled, forfeited, disputed, or recovered amounts return to category control under the grant terms.

A changed scope requires an amended grant decision before later release.

Detailed treatment remains controlled by [FUZE Team Advisor Partner Vesting](19-FUZE_TEAM_ADVISOR_PARTNER_VESTING_PUBLIC.md).

## Transparency / Stability Reserve

**Allocation:** 25,000,000 FUZE — 5.00% of fixed supply.

### Mandate

Supports exceptional trust, transparency, evidence, assurance, security, recovery, reporting, custody, continuity, or ecosystem-stability actions that fit this reserve better than another allocation.

It is not an automatic market-support or price-stabilization pool.

### Valid Release Triggers

A release review may open when:

- a material trust, transparency, security, reporting, recovery, custody, continuity, or ecosystem-stability event exists;
- the event and response objective are documented;
- another allocation is not the more appropriate source;
- the amount and safeguards are proportionate;
- monitoring and closure criteria exist;
- and the required governance and specialist reviews approve the action.

### Required Evidence

- event or objective;
- category-fit explanation;
- alternatives considered;
- proposed amount and sizing basis;
- destination;
- restriction and safeguard model;
- governance, treasury, legal, accounting, tax, compliance, security, technical, or market review as applicable;
- monitoring period;
- success or closure criteria;
- return or recovery route;
- circulation effect;
- public explanation;
- and reporting method.

### Destination Classes

Possible destinations include:

- controlled assurance structure;
- recovery vault;
- security or remediation contract;
- evidence or transparency program;
- restricted partner or provider arrangement;
- continuity mechanism;
- or another approved exceptional-response structure.

### Release and Circulation Treatment

Reports should distinguish:

- designated reserve amount;
- committed amount;
- approved response amount;
- deployed amount;
- restricted amount;
- returned or recovered amount;
- closed amount;
- and circulating classification.

### Prohibited Shortcuts

Recurring ordinary expenses, routine compensation, routine partner grants, general community programs, ordinary liquidity inventory, or discretionary price support should use their proper allocation or process.

### Exception and Return Treatment

Unused, recovered, expired, cancelled, or excess amounts return to reserve or recovery custody.

A recurring or materially different use requires a new decision or reclassification.

## Batch and Program Releases

A batch release requires both program-level and item-level controls.

### Program Record

The program record should identify:

- program identifier;
- allocation category;
- purpose;
- approved budget;
- eligibility, vesting, milestone, claim, partner, incentive, migration, or market method;
- period;
- owner;
- authority;
- destination classes;
- restrictions;
- reporting method;
- return treatment;
- and closure trigger.

### Batch Manifest

Each item should identify:

- item identifier;
- beneficiary or destination private reference;
- verified destination;
- amount;
- calculation or entitlement basis;
- duplicate-check status;
- restriction;
- intended final state;
- circulation effect;
- validation status;
- and exception status.

### Batch Totals

The batch record should identify:

- item count;
- total approved amount;
- total prepared amount;
- total submitted amount;
- total confirmed amount;
- failed amount;
- returned amount;
- corrected amount;
- and closing program balance.

A batch total alone is not sufficient evidence for individual recipients or destinations.

### Partial Completion

A batch may complete partially.

Failed or unresolved items should remain separately classified and should not be represented as released or distributed.

## Final Pre-Execution Review

Immediately before execution, FUZE should confirm:

- canonical FUZE token and network;
- source allocation and vault;
- source balance and commitments;
- release identifier and approval version;
- destination address, contract, custodian, program, partner, venue, or pool;
- destination control class;
- amount and decimals;
- batch total where applicable;
- lock, vesting, claim, milestone, agreement, reserve, or market condition;
- duplicate release and prior-payment checks;
- signer, role, multisig, timelock, and contract configuration;
- sanctions, restriction, incident, or pause status where applicable;
- expected final custody;
- expected final state;
- expected circulation effect;
- return and recovery route;
- and approval validity.

A material discrepancy should stop execution and return the release to review.

## Execution and Post-Release Classification

### Execution Record

The execution record should include:

- release identifier;
- approved request version;
- source address or account;
- destination address or account;
- network;
- canonical FUZE contract;
- amount;
- transaction hash or system reference;
- block or confirmation context;
- fee amount and asset where applicable;
- executor or signer roles;
- execution time;
- timelock or governance reference;
- confirmation and finality status;
- batch manifest where applicable;
- exception notes;
- and current status.

### Post-Release Classification

After confirmation, FUZE should record:

- source allocation effect;
- source vault effect;
- destination custody;
- recipient, program, partner, contract, reserve, or market state;
- continuing lock or restriction;
- vesting state;
- eligibility and claim state;
- operational deployment state;
- circulating-supply effect;
- return or recovery rights;
- and public-reporting treatment.

Technical execution alone does not establish the final classification.

## Unused, Cancelled, Expired, Returned, and Recovered Amounts

### Return Record

A return or recovery record should identify:

1. original release or commitment;
2. original allocation;
3. original vault;
4. original recipient, program, partner, contract, reserve, venue, or destination class;
5. reason;
6. amount;
7. source and destination;
8. transaction or system evidence;
9. continuing obligations or disputes;
10. revised program balance;
11. revised allocation balance;
12. revised custody and token state;
13. revised circulation effect;
14. reviewer;
15. approval;
16. public-report effect;
17. current status; and
18. closure.

### Reuse After Return

Returned or recovered units should not be reused automatically when:

- the original program remains open or disputed;
- ownership or allocation is unclear;
- legal, accounting, tax, compliance, or security review is pending;
- the units came from a partner, bridge, venue, liquidity, or market context;
- a claim or participant correction remains open;
- or public reporting requires restatement.

## Exceptions, Amendments, and Reclassification

### Execution Exception

An execution exception may change:

- destination;
- transaction route;
- custody provider;
- claim contract;
- timing;
- batch composition;
- or technical method

while preserving the allocation mandate and approved economic purpose.

The exception should receive appropriate renewed verification and approval.

### Program Amendment

A program amendment may change:

- eligibility;
- milestone;
- vesting schedule;
- claim period;
- lock;
- budget use;
- partner deliverable;
- incentive calculation;
- or reporting method.

The amendment should identify affected prior and future records.

### Reclassification

A change of allocation purpose requires formal reclassification.

The reclassification record should identify:

- source category;
- destination category;
- amount;
- reason;
- alternatives;
- existing commitments;
- affected recipients, programs, partners, or market operations;
- governance and specialist review;
- updated allocation table;
- updated vault and custody treatment;
- updated circulation treatment;
- effective date;
- and public communication.

After reclassification:

```text
sum of all approved allocation categories = 500,000,000 FUZE
```

## Suspension and Incident Handling

A release, batch, program, vault, contract, partner, claim route, or movement class should be suspended when a material issue affects:

- source authority;
- vault balance;
- signer or multisig integrity;
- destination validity;
- contract behavior;
- eligibility;
- vesting calculation;
- claim integrity;
- milestone evidence;
- batch manifest;
- partner conduct;
- market-operation controls;
- bridge or custody provider;
- legal or jurisdiction support;
- sanctions or restriction status;
- reconciliation;
- or public-reporting accuracy.

### Incident Record

The incident record should identify:

- incident identifier;
- affected allocation and vault;
- affected release requests, batches, programs, or transactions;
- affected amount;
- detection time;
- actual onchain or system state;
- known impact;
- containment;
- suspension scope;
- beneficiary, partner, venue, contract, provider, signer, or custody actions;
- recovery options;
- allocation and circulation effect;
- public communication;
- root cause;
- remediation;
- reviewer;
- reactivation conditions;
- status;
- and closure.

### Reactivation

Reactivation should require:

- issue containment;
- corrected authority, configuration, evidence, or calculation;
- affected-balance reconciliation;
- renewed approval;
- testing where applicable;
- and updated public status.

## Allocation and Vault Reconciliation

For each allocation category:

```text
opening allocation balance
+ approved inward reclassification
+ verified returns and recoveries
- approved outward reclassification
- confirmed releases, deployments, or burns
+/- corrections
= closing allocation balance
```

For each source vault:

```text
opening vault balance
+ verified inflows
- verified outflows
+/- corrections
= closing vault balance
```

Available category capacity should reconcile as:

```text
closing allocation or vault balance
- active commitments
- locked or restricted amount
- approved pending releases
- disputed or quarantined amount
= available uncommitted category capacity
```

Program reconciliation should distinguish:

- approved budget;
- committed amount;
- eligible or earned amount;
- claim-funded amount;
- claimable amount;
- released amount;
- deployed amount;
- returned amount;
- cancelled amount;
- corrected amount;
- and remaining amount.

The same units should not appear more than once across mutually exclusive states.

## Public Reporting

A public release report may include:

- report identifier and version;
- reporting period;
- allocation category;
- approved allocation amount;
- opening and closing category balance;
- opening and closing source-vault balance;
- release or movement class;
- amount;
- recipient or destination class;
- aggregate eligibility, vesting, milestone, claim, program, reserve, or market state;
- continuing restrictions;
- transaction, governance, contract, or report references;
- released, deployed, returned, cancelled, disputed, suspended, and corrected amounts;
- circulation-methodology treatment;
- limitations;
- review date;
- status;
- and current-as-of date.

### Reporting Separation

Reports should distinguish:

- proposed;
- approved;
- committed;
- claim-funded;
- claimable;
- vested;
- approved for release;
- submitted;
- confirmed;
- released;
- deployed;
- returned;
- and circulating.

### Public Privacy and Security Boundary

Public reporting should not expose:

- personal identity linked to a wallet;
- private beneficiary records;
- private grant or vesting terms;
- private migration evidence;
- private partner terms;
- private market strategy;
- signer identities where not approved;
- credentials;
- private keys;
- recovery material;
- exact security procedures;
- or exploitable treasury patterns.

Public display behavior remains governed by [FUZE Public Vault Visibility System](16-FUZE_PUBLIC_VAULT_VISIBILITY_SYSTEM_PUBLIC.md).

## Closure and Archive

A release, batch, or program may close when:

- execution is complete;
- all intended items are completed, cancelled, returned, or controlled;
- claims expire or close;
- vesting obligations are transferred or completed;
- partner or grant obligations conclude;
- market positions close;
- reserve use concludes;
- incidents and corrections are resolved or carried forward under documented treatment;
- and allocation, vault, program, and circulation records reconcile.

### Closure Record

The closure record should identify:

- release, batch, or program identifier;
- source allocation;
- approved amount;
- released amount;
- deployed amount;
- returned or recovered amount;
- cancelled or expired amount;
- disputed or unresolved amount;
- corrected amount;
- remaining commitment;
- closing allocation balance;
- closing vault balance;
- final token-state and circulation treatment;
- evidence retention;
- public-report status;
- closure authority;
- and current-as-of date.

Closed records should not be silently rewritten.

Later changes should use correction or restatement records.

## Separation from Adjacent Systems

| System or process | Primary role | Why it remains separate |
|---|---|---|
| Token allocation table | Defines fixed category amounts and mandates | Allocation does not authorize release |
| Vault and reserve policy | Defines custody, reserve, authority, segregation, and lifecycle | A funded vault does not authorize movement |
| Vault-by-vault release rules | Defines category-specific release gates | Each allocation uses a distinct purpose and evidence basis |
| Controlled circulation | Governs movement execution, state transition, and circulation classification | Release approval is one stage in a larger process |
| Vesting | Defines time, service, milestone, or hybrid progression | Vested does not equal released or circulating |
| Claim process | Defines eligibility and recipient action | Claimable, claimed, transferred, and circulating remain separate |
| Stablecoin compensation | Settles approved business obligations | Does not authorize FUZE token grants or releases |
| Platform Credits | Product-consumption units | Outside FUZE allocation balances |
| Approved distributable value | Reviewed value from defined product-revenue pools | Does not create token-release authority |
| Wallet-based participation | Activation-gated eligibility, claim, and payout process | Does not create FUZE token release unless a separate token allocation is used |
| Liquidity and listing policy | Governs market structure and venue processes | Liquidity allocation release does not establish listing or price outcome |

## Status and Evidence

This paper defines category-specific release requirements.

It does not independently prove that any current program, grant, migration, vesting event, claim window, partner milestone, reserve action, liquidity deployment, or token release is active or approved.

| Status claim | Evidence direction |
|---|---|
| Allocation available | Approved allocation, current vault balance, commitments, restrictions, pending releases, disputes, and calculation |
| Release proposed | Release packet, category fit, amount, destination, conditions, owner, and status |
| Release approved | Complete gates, reviewers, authority, amount, source, destination, conditions, and approval version |
| Tokens committed | Approved obligation, program, grant, claim, partner, reserve, or market use and ledger entry |
| Tokens vesting | Grant, schedule, condition, beneficiary class, custody, calculation, and status |
| Tokens vested | Satisfied condition, amount, calculation, reviewer, continuing restrictions, and state |
| Participant eligible | Active program, route, criteria, evidence, duplicate review, decision, and status |
| Tokens claimable | Active claim process, funded amount, eligible recipient class, window, and route |
| Tokens claimed | Claim action, amount, recipient or wallet reference, time, transfer status, and restrictions |
| Milestone satisfied | Agreement, milestone definition, evidence, acceptance, reviewer, and status |
| Release submitted | Approved instruction, source, destination, amount, transaction or system reference, and time |
| Release confirmed | Required confirmation or provider finality and exception treatment |
| Tokens released | Transaction evidence, allocation effect, vault effect, destination custody, restrictions, and state classification |
| Tokens deployed | Program, partner, reserve, contract, liquidity, market, or other approved destination and restrictions |
| Tokens returned | Original release, reason, amount, transaction, destination custody, revised allocation, and state |
| Release corrected | Original record, error, evidence, revised amount or state, authority, and report update |
| Program closed | Final budget, releases, returns, cancellations, disputes, corrections, balances, reports, and closure authority |

The following do not independently establish release authority or completed release:

- this paper;
- an allocation balance;
- a vault address;
- a wallet screenshot;
- a token transfer;
- an internal spreadsheet;
- a grant discussion;
- a partnership announcement;
- a vesting draft;
- a claim announcement;
- a community post;
- a listing discussion;
- a market-maker proposal;
- code;
- a repository;
- or token price activity.

## Allocation, Release, Circulation, Market, and Outcome Separation

The following remain separate:

- fixed supply;
- allocation;
- vault custody;
- available category balance;
- proposal;
- approval;
- commitment;
- lock;
- vesting;
- vested status;
- eligibility;
- claim funding;
- claimability;
- claim action;
- release approval;
- transaction submission;
- confirmation;
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

A token release does not guarantee:

- recipient sale;
- exchange access;
- listing;
- active liquidity;
- market depth;
- narrow spread;
- trading volume;
- demand;
- price support;
- price appreciation;
- income;
- revenue share;
- or financial return.

## Public Boundary

This paper publishes the category-specific release triggers, evidence requirements, destination classes, state treatment, exception routes, reconciliation methods, reporting requirements, and public boundaries for the ten approved FUZE allocations.

It does not publish or establish current:

- vault addresses;
- signer identities;
- beneficiary identities;
- grant amounts;
- vesting schedules;
- claim windows;
- participant allocations;
- migration approvals;
- partner allocations;
- incentive awards;
- reserve-use amounts;
- liquidity deployments;
- market-maker inventory;
- exchange deposits;
- token-release amounts;
- circulating supply;
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

unless those details are separately approved and supported by current evidence in an allocation record, release packet, grant, vesting record, migration decision, participation process, claim report, partner record, reserve decision, market-operation report, transaction record, specialist paper, or public status report.

Every actual release remains subject to its controlling allocation, vault, grant, vesting, migration, community, incentive, partner, reserve, liquidity, market, governance, treasury, legal, accounting, tax, compliance, technical, security, privacy, and reporting requirements.

## Key Takeaways

- FUZE has ten allocation categories, and each category has a distinct release mandate and evidence path.
- A vault balance or approved allocation does not create a recipient right, claim, vesting event, release, deployment, circulation, or market outcome.
- Every material release should pass common allocation, custody, balance, trigger, destination, condition, duplicate, specialist, execution, and reporting gates.
- Community, migration, team, foundation, treasury, incentive, partner, liquidity, advisor, and stability releases must remain distinct.
- Approved, committed, vested, eligible, claimable, claimed, released, deployed, returned, and circulating are separate states.
- Batch and program releases require item-level manifests, program ledgers, partial-completion treatment, and closing reconciliation.
- Unused, cancelled, expired, invalid, disputed, returned, or recovered units should map back to the correct allocation and vault before reuse.
- Changing execution details may use an approved exception, but changing allocation purpose requires formal reclassification.
- Every completed release should reconcile the allocation, source vault, program or obligation, destination, final token state, and circulation effect.
- Token release does not guarantee listing, liquidity, depth, spread, volume, demand, price support, income, revenue share, or financial return.
