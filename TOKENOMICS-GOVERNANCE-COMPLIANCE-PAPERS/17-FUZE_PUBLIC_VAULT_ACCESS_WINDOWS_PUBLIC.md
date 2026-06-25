
# FUZE Public Vault Access Windows

## Executive Summary

A FUZE Public Vault Access Window is a formally approved, time-bounded or condition-bounded process through which a defined participant class may apply, qualify, provide approved consideration where applicable, receive an allocation decision, and enter a controlled claim, lock, vesting, custody, or token-release route from a named FUZE allocation vault.

A window is not created by publishing a vault, balance, allocation, roadmap, or community announcement.

It exists only when its complete operating record has been approved, its activation gates have passed, and its public notice states that the window is active.

The controlling lifecycle is:

```text
approved purpose and source allocation
-> complete window proposal
-> legal, treasury, product, technical, security, custody, reporting, and jurisdiction review
-> approval of one version
-> activation-gate verification
-> public notice
-> opening
-> application or qualification capture
-> eligibility, duplicate, abuse, payment, and limit review
-> allocation decision
-> settlement or qualifying-condition confirmation
-> claim, lock, vesting, custody, or release processing
-> token, consideration, proceeds, refund, and exception reconciliation
-> final public-safe report
-> closure and archive
```

A window can also enter:

- delayed;
- paused;
- capacity reached;
- processing;
- partially settled;
- partially released;
- cancelled;
- corrected;
- superseded;
- or terminated status.

Each state is separate.

Public visibility does not create access.

Access does not create eligibility.

Eligibility does not create an allocation.

An allocation decision does not equal settlement.

Settlement does not automatically equal token release.

Release does not automatically equal circulation.

Circulation does not establish:

- DEX access;
- CEX application;
- CEX approval;
- listing;
- deposits or withdrawals;
- active trading;
- liquidity;
- market depth;
- narrow spread;
- token demand;
- price support;
- income;
- revenue share;
- or financial return.

Every active window should identify:

- stable window identifier and version;
- purpose;
- source allocation and source vault;
- approved maximum FUZE capacity;
- participant class;
- eligibility rules;
- supported and restricted jurisdictions where applicable;
- opening and closing boundaries;
- application or qualification method;
- allocation method;
- participant limits;
- pricing or non-payment consideration method;
- supported payment asset and network where applicable;
- proceeds route;
- release, claim, lock, vesting, or custody treatment;
- pause, cancellation, refund, return, correction, and dispute treatment;
- support and complaint route;
- evidence and reporting method;
- current status;
- and current-as-of date.

The window record should distinguish:

- maximum approved capacity;
- capacity reserved for tiers or classes;
- applications received;
- eligible applications;
- approved allocations;
- pending allocations;
- rejected or cancelled allocations;
- verified consideration received;
- refunds and reversals;
- settled allocations;
- claim-funded amounts;
- claimable amounts;
- released amounts;
- locked or vesting amounts;
- returned amounts;
- unused closing capacity;
- and circulation classification.

This paper defines the process for creating and operating an access window.

It does not announce an active window, token sale, solicitation, entitlement, investment product, exchange listing, liquidity commitment, or financial outcome.

The pricing methodology for any approved payment-based window remains governed by [FUZE Vault Access Pricing Mechanism](18-FUZE_VAULT_ACCESS_PRICING_MECHANISM_PUBLIC.md).

Public display remains governed by [FUZE Public Vault Visibility System](16-FUZE_PUBLIC_VAULT_VISIBILITY_SYSTEM_PUBLIC.md).

Source-vault release authority remains governed by [FUZE Vault-by-Vault Release Rules](15-FUZE_VAULT_BY_VAULT_RELEASE_RULES_PUBLIC.md).

## Purpose of This Paper

This paper explains:

- the public access-window position;
- visibility, access, eligibility, allocation, settlement, and release separation;
- eligible source categories;
- window types;
- the complete window record;
- lifecycle and status vocabulary;
- activation gates;
- public notice requirements;
- participant classes and eligibility;
- application and qualification workflows;
- allocation methods;
- capacity and participant limits;
- pricing and consideration boundaries;
- payment, proceeds, refund, and settlement controls;
- claim, lock, vesting, custody, and release treatment;
- duplicate, abuse, fraud, sanctions, and restricted-activity controls;
- pause, cancellation, amendment, extension, and supersession;
- complaints, disputes, and corrections;
- reconciliation and final reporting;
- privacy, evidence, and record retention;
- closure and archive;
- status and evidence requirements; and
- public limitations.

This paper does not replace:

- an active window notice;
- the token allocation table;
- vault-establishment records;
- vault-specific release rules;
- community-round terms;
- migration terms;
- partner agreements;
- grant terms;
- incentive-program terms;
- pricing records;
- payment-provider terms;
- stablecoin issuer terms;
- claim instructions;
- vesting schedules;
- legal, accounting, tax, compliance, sanctions, or jurisdiction review;
- smart-contract specifications;
- private identity or verification procedures;
- private signer procedures;
- liquidity or listing procedures;
- or the token risk register.

## Public Position

An access window is a controlled participation process, not an open path from a public treasury or vault balance.

FUZE should not describe access as active unless:

- the exact window version is approved;
- the source allocation and source vault are verified;
- sufficient uncommitted capacity exists;
- participant rules are complete;
- pricing or qualifying consideration is reproducible;
- payment, proceeds, claim, lock, vesting, custody, release, refund, and correction routes are ready where applicable;
- required legal, treasury, product, technical, security, privacy, compliance, accounting, tax, and jurisdiction reviews are complete;
- public notice and support routes are published;
- monitoring is active;
- and the current status is `Active`.

The following do not independently open a window:

- a visible vault;
- an allocation balance;
- a product launch;
- a community post;
- a wallet connection;
- token ownership;
- prior participation;
- a partnership announcement;
- a pricing example;
- a roadmap date;
- an internal approval draft;
- or a listing discussion.

A window should use neutral, evidence-based language and should not imply guaranteed access, allocation, token delivery, liquidity, resale, market value, or financial return.

## Visibility, Access, Eligibility, Allocation, Settlement, and Release

| State | Evidence-backed meaning | What it does not establish |
|---|---|---|
| Visible | Approved public information about a vault, balance, record, or window can be inspected. | Active access, eligibility, or authority |
| Proposed | A window design is being prepared. | Approval or public offer |
| Approved | A specific window version has received required authority. | Activation or opening |
| Announced | An approved notice has been published. | Active participation unless the notice says `Active` |
| Accessible | The supported application or qualification route is open. | Eligibility or allocation |
| Applied | A submission was received. | Completeness, eligibility, or allocation |
| Eligible | The submission satisfies the active rules. | Allocation or settlement |
| Waitlisted | The submission may be considered if capacity becomes available. | Allocation right |
| Allocated | FUZE records an approved participant amount. | Settlement, claimability, release, or circulation |
| Payment pending | Consideration is due but not fully verified. | Settlement |
| Payment verified | Required consideration was received through the approved route. | Final settlement if other conditions remain |
| Settled | Allocation and required consideration or qualifying basis reconcile under the window terms. | Token release |
| Claimable | The approved amount is available through an active claim route. | Claim completion or receipt |
| Claimed | The participant completed the required claim action. | Final transfer or unrestricted custody |
| Released | FUZE moved or assigned the amount under the approved release route. | Unrestricted circulation |
| Locked or vesting | Released or assigned FUZE remains subject to continuing conditions. | Current transferability |
| Closed | New access has ended and final processing is controlled. | Completion of every pending item |
| Archived | Historical notice, methodology, report, and corrections remain available. | Current access |

## Eligible Source Categories

Source selection begins with the approved allocation mandate.

### Community Participation Allocation

May support an approved:

- community participation round;
- product-user route;
- contributor route;
- education or ecosystem-access route;
- or another published community program.

The source must remain within the Community Participation Allocation mandate and the applicable release rules.

### Ecosystem Growth & Partnerships

May support a bounded:

- partner participation route;
- ecosystem grant route;
- integration route;
- developer or distribution route;
- or another approved relationship-based process

when the participant class, agreement, milestone, limits, and purpose fit the allocation mandate.

### Treasury Reserve

May serve as a source only when a specific strategic treasury decision expressly approves:

- purpose;
- amount;
- participant class;
- destination;
- pricing or consideration treatment;
- release treatment;
- treasury impact;
- and reporting.

Treasury Reserve is not a default substitute for Community Participation or Ecosystem Growth & Partnerships.

### Categories Using Dedicated Routes

The following generally use their dedicated release processes rather than a public access window:

- BOARD / Surfboard Migration;
- Team Allocation;
- Foundation Reserve;
- Holder Incentives;
- Liquidity & Market Operations;
- Advisors / Strategic Contributors;
- and Transparency / Stability Reserve.

A different route requires a documented category-fit review or formal allocation reclassification.

### Source Approval Does Not Create a New Allocation

A window uses capacity from an existing source category.

It does not create a new allocation category or alter the fixed **500,000,000 FUZE** supply.

Unused capacity remains with the source allocation unless another action receives separate authority.

## Window Types

### Community Round Window

Supports a defined community participation process with published eligibility, limits, pricing or qualifying basis, release conditions, and reporting.

### Product-User Window

Supports a defined route for qualified users of an approved FUZE or ecosystem product.

Product registration or use alone does not create eligibility unless the active rules expressly say so.

### Contributor Window

Supports a bounded route for verified contributors under published contribution evidence, review, and allocation criteria.

### Partner or Ecosystem Window

Supports a defined class of partners, developers, integrators, grantees, or ecosystem participants under approved relationship and milestone conditions.

### Strategic Treasury Window

Supports a specifically approved strategic process from Treasury Reserve where the purpose cannot be appropriately handled by another allocation or ordinary treasury transaction.

### Payment-Based Window

Requires an approved payment asset, pricing method, payment route, settlement process, and refund treatment.

### Non-Payment Window

Uses an approved qualifying basis such as:

- product usage;
- contribution;
- milestone;
- grant decision;
- partner condition;
- or another measurable non-payment basis.

A non-payment window still requires a reproducible allocation method and evidence.

### Hybrid Window

Combines payment and non-payment qualification.

The window record should explain the order in which eligibility, non-payment conditions, pricing, payment, and allocation are applied.

## Complete Window Record

No window should activate while a material field remains undecided.

### Identity and Authority

1. window identifier;
2. public title;
3. version;
4. sponsor;
5. operating owner;
6. approval authority;
7. reviewers;
8. effective date;
9. expiry or closing trigger;
10. current status; and
11. current-as-of date.

### Purpose and Source

12. purpose;
13. source allocation;
14. source vault;
15. source-vault status;
16. approved maximum FUZE capacity;
17. existing source commitments;
18. reserved capacity by class or tier;
19. available capacity calculation;
20. category-fit explanation; and
21. unused-capacity treatment.

### Participant Rules

22. participant class;
23. eligibility criteria;
24. exclusion criteria;
25. supported and restricted jurisdictions where applicable;
26. age, entity, account, product, contribution, partner, wallet, or other requirements;
27. identity or verification level where applicable;
28. related-party treatment;
29. duplicate and linked-account treatment;
30. acknowledgements and disclosures;
31. support route;
32. complaint route; and
33. appeal or reconsideration treatment where applicable.

### Window Boundary

34. announcement time;
35. opening time;
36. closing time or closing condition;
37. timezone;
38. capacity-reached treatment;
39. late-submission treatment;
40. extension authority;
41. pause authority;
42. cancellation authority; and
43. processing period after close.

### Application and Allocation

44. application or qualification method;
45. required fields and evidence;
46. completeness rules;
47. eligibility workflow;
48. allocation method;
49. minimum participant amount where applicable;
50. maximum participant amount;
51. tier rules;
52. queue rules;
53. pro-rata rules where applicable;
54. waitlist rules;
55. rounding and residual treatment;
56. decision reason codes;
57. notification method; and
58. allocation-expiry treatment.

### Pricing or Qualifying Consideration

59. payment-based, non-payment, or hybrid classification;
60. pricing methodology where applicable;
61. calculation currency;
62. reference source;
63. observation time or period;
64. floor, cap, premium, discount, or adjustment treatment where approved;
65. supported payment assets;
66. supported networks;
67. payment address or provider route;
68. payment deadline;
69. fees and conversion treatment;
70. overpayment and underpayment treatment;
71. failed-payment treatment;
72. non-payment qualifying basis where applicable; and
73. evidence required for the qualifying basis.

### Settlement and Proceeds

74. consideration-receipt owner;
75. payment-verification method;
76. settlement rule;
77. proceeds destination;
78. proceeds custody and classification;
79. treasury and accounting owner;
80. tax treatment owner;
81. refund source and route;
82. reversal treatment;
83. chargeback or payment-provider risk treatment;
84. stablecoin depeg, freeze, bridge, or network-risk treatment where applicable; and
85. settlement cutoff.

### Release and Claim

86. release route;
87. direct, claim, staged, locked, vesting, or program-custody treatment;
88. claim contract or destination where applicable;
89. claim opening and closing conditions;
90. lock or vesting schedule;
91. participant destination verification;
92. release deadline;
93. unclaimed treatment;
94. failed-transfer treatment;
95. return and recovery route;
96. circulating-supply treatment; and
97. public reporting treatment.

### Controls and Reporting

98. legal, compliance, jurisdiction, treasury, accounting, tax, product, technical, security, privacy, custody, and reporting reviews;
99. fraud, abuse, sanctions, restricted-activity, and duplicate controls where applicable;
100. monitoring and alerts;
101. incident process;
102. pause and reactivation process;
103. correction and restatement process;
104. public notice fields;
105. status-reporting cadence;
106. final-report owner;
107. evidence-retention requirements;
108. privacy classification;
109. closure requirements; and
110. archive location.

## Lifecycle and Status Vocabulary

### Proposed

The sponsor documents the purpose, source category, participant class, expected capacity, dependencies, and intended outcome.

### Under Review

Applicable owners assess category fit, legal and jurisdiction support, treasury exposure, product readiness, pricing, payments, custody, technical implementation, security, privacy, accounting, tax, reporting, and support.

### Approved

The required authority approves one exact window version.

Approval may include conditions that must be satisfied before announcement or opening.

### Activation Pending

The window is approved but one or more activation gates remain incomplete.

### Announced

FUZE publishes the approved notice and clearly labels the window as:

- upcoming;
- conditional;
- activation pending;
- or active.

Announcement alone does not create active access.

### Active

The supported application or qualification route is open within the approved boundary.

### Capacity Reached

The maximum available capacity has been reserved or allocated under the published method.

The system should state whether:

- new applications close;
- a waitlist opens;
- applications continue for possible cancellations;
- or the window enters processing.

### Paused

New or continuing activity is temporarily restricted because a material issue requires review.

### Processing

Submissions undergo completeness, eligibility, duplicate, abuse, payment, qualification, allocation, and exception checks.

Processing can continue after the application boundary closes.

### Allocation Pending

The participant passed initial review, but capacity, payment, final calculation, or another condition remains unresolved.

### Allocated

An approved participant amount is recorded.

### Settlement Pending

Payment, qualifying consideration, custody, or reconciliation remains incomplete.

### Settled

The approved allocation and required consideration or qualifying basis reconcile.

### Claim Funding

FUZE places the required amount into an approved claim or distribution structure.

Claim funding does not establish individual claim completion.

### Claimable

An eligible participant can complete the active claim process for the approved amount.

### Released

FUZE transfers or assigns the approved amount under the stated release treatment.

### Closing

New participation has ended and remaining applications, allocations, payments, refunds, claims, releases, disputes, and reconciliations are being finalized.

### Closed

New access and ordinary processing have ended, with remaining exceptions controlled under the closure record.

### Cancelled

The window will not proceed or is terminated before ordinary completion.

### Corrected

A later authorized record changes a prior data point, calculation, decision, allocation, payment, release, or report while preserving history.

### Superseded

A later approved window version replaces the prior version for current operation.

### Archived

The notice, methodology, status history, reports, and correction records remain available for later review.

## Activation Gates

A window can become `Active` only after all applicable gates pass.

### 1. Source Mandate Gate

The purpose fits the source allocation and source-vault mandate.

### 2. Capacity Gate

The source has sufficient uncommitted and unrestricted capacity after accounting for:

- existing commitments;
- pending releases;
- reserved tiers;
- disputes;
- quarantine;
- and other active windows.

### 3. Program Readiness Gate

The associated product, community route, contributor process, partnership, grant, or strategic program is ready for the stated purpose.

### 4. Legal and Jurisdiction Gate

Participant classes, jurisdictions, communications, consideration, contracts, disclosures, exclusions, and support routes have received required review.

### 5. Treasury and Custody Gate

The source vault, proceeds route, payment route, refund source, release route, signer model, custodian, claim contract, and reconciliation owners are confirmed.

### 6. Pricing or Qualifying-Basis Gate

The pricing method or non-payment qualifying basis is approved, reproducible, testable, and published at the required level.

### 7. Payment and Settlement Gate

Where payment applies, supported assets, networks, addresses, provider routes, deadlines, fees, failed-payment rules, refund routes, and settlement records are ready.

### 8. Eligibility and Abuse-Control Gate

Eligibility, duplicate, linked-account, fraud, bot, sanctions, restricted-activity, manual-review, and override processes are ready where applicable.

### 9. Technical and Security Gate

Application, pricing, payment, allocation, claim, vesting, release, monitoring, alerting, pause, correction, and data-retention systems are tested for the intended scope.

### 10. Privacy and Data Gate

Data collection is necessary, proportionate, classified, retained, and protected under the approved process.

### 11. Reporting Gate

Public notice, status vocabulary, evidence references, methodology, source-vault profile, support route, correction route, and final-report owner are ready.

### 12. Operational Support Gate

Staffing, escalation, incident response, participant communication, complaints, refunds, and closure support are ready.

The broader participation gate framework remains controlled by [FUZE Participation Activation Gates](08-FUZE_PARTICIPATION_ACTIVATION_GATES_PUBLIC.md).

## Public Notice Requirements

The opening notice should identify:

- window title, identifier, and version;
- current status;
- purpose;
- source allocation;
- source-vault public profile where available;
- participant class;
- eligibility and exclusion summary;
- supported and restricted jurisdictions where applicable;
- opening and closing boundaries;
- approved maximum capacity;
- reserved capacity or tiers where relevant;
- minimum and maximum participant limits;
- allocation method;
- pricing or qualifying-consideration method;
- supported payment assets and networks where applicable;
- payment deadline and settlement treatment;
- release, claim, lock, vesting, or custody treatment;
- pause, cancellation, refund, expiry, and correction treatment;
- support and complaint route;
- privacy summary;
- risk and interpretation boundaries;
- methodology and evidence references;
- and current-as-of date.

### Notice Status

The notice should clearly say whether the window is:

- proposed;
- activation pending;
- upcoming;
- active;
- capacity reached;
- paused;
- processing;
- closing;
- closed;
- cancelled;
- corrected;
- superseded;
- or archived.

### No Implied Continuation

A prior window does not imply a future window.

A recurring program should publish each operating period, capacity, rules, and current status unless the approved framework expressly supports continuous operation.

### Material Changes

A material change to eligibility, capacity, pricing, payment, limits, release, dates, refund treatment, or risk should be published before it applies, except where immediate suspension is required for safety or compliance.

## Participant Classes and Eligibility

Eligibility should connect directly to the purpose of the active window.

Possible participant classes include:

- qualified community participants;
- approved product users;
- verified contributors;
- approved ecosystem developers;
- approved partners or integrators;
- approved grantees;
- or another defined class supported by the source mandate.

### Possible Eligibility Factors

- account status;
- product-use evidence;
- contribution evidence;
- partner or grant relationship;
- supported jurisdiction;
- age or entity requirements where applicable;
- wallet capability;
- destination verification;
- required acknowledgements;
- absence of duplicate, fraudulent, abusive, sanctioned, or restricted activity;
- and completion before the deadline.

### Eligibility Decision Record

The decision record should include:

- private participant reference;
- window identifier and version;
- application or qualification time;
- evidence received;
- completeness status;
- applicable criteria;
- checks performed;
- decision;
- reason code;
- reviewer or automated rule version;
- override status;
- appeal or reconsideration status where applicable;
- and current status.

### Wallet Boundaries

Wallet ownership or control can support:

- destination verification;
- duplicate review;
- claim security;
- or another active rule.

A wallet balance alone does not create eligibility unless the published window expressly uses a balance-based rule and defines:

- asset;
- network;
- snapshot time;
- custody treatment;
- delegated or exchange custody treatment;
- related-wallet treatment;
- and anti-manipulation controls.

### Public Reporting

Public reporting may show aggregate:

- applications;
- completed submissions;
- eligible submissions;
- rejected submissions;
- waitlisted submissions;
- and reason-code categories.

Personal identity and supporting evidence remain permissioned or restricted.

## Application and Qualification Workflow

### Submission

The system should capture:

- window version;
- participant class;
- required information;
- required evidence;
- acknowledgements;
- wallet or destination where applicable;
- payment intent where applicable;
- submission time;
- and consent or notice records where required.

### Completeness Review

Incomplete submissions should receive:

- missing-field status;
- remediation route;
- deadline;
- and closure treatment.

### Verification

Applicable checks may include:

- account or product status;
- contribution or milestone evidence;
- partner or entity authority;
- jurisdiction;
- identity or verification level;
- wallet control;
- duplicate or linked account;
- prior allocation;
- payment route;
- sanctions or restricted activity;
- fraud or abuse;
- and manual-review triggers.

### Decision

Possible decisions include:

- eligible;
- eligible subject to capacity;
- waitlisted;
- remediation required;
- payment pending;
- manual review;
- rejected;
- withdrawn;
- cancelled;
- or suspended.

### Decision Consistency

The same active rules should apply to similarly situated participants.

An override should identify:

- original rule result;
- reason;
- authority;
- scope;
- effective time;
- and audit record.

## Allocation Methods

### First Completed and Verified

Capacity is assigned in order of completed, eligible, and verified submissions.

The notice should define:

- timestamp source;
- completeness threshold;
- payment requirement;
- queue treatment;
- simultaneous submissions;
- and cancellation reallocation.

### Pro Rata

Approved demand is scaled against available capacity.

The method should define:

- numerator and denominator;
- excluded demand;
- minimum allocation;
- maximum allocation;
- rounding;
- residual amount;
- and treatment of declined or unpaid allocations.

### Tiered Allocation

Participant classes receive separate capacity or limits under published criteria.

The method should define:

- tier eligibility;
- tier capacity;
- participant limits;
- movement between tiers;
- and unused-tier treatment.

### Reviewed Allocation

FUZE applies stated qualitative and quantitative criteria.

The process should include:

- scoring or decision factors;
- reviewer roles;
- conflict controls;
- reason codes;
- and consistency review.

### Earned or Contribution-Based Allocation

The amount depends on verified activity, deliverables, product use, or another measurable outcome.

The method should define:

- measurement period;
- source data;
- calculation;
- caps;
- reversals;
- abuse controls;
- and dispute route.

### Lottery or Randomized Allocation

Where legally and operationally supported, a randomized method should define:

- eligible pool;
- random source;
- reproducibility or assurance;
- exclusions;
- participant limits;
- and jurisdiction treatment.

A randomized method should not be used where the legal or program framework does not support it.

### Combined Method

A combined method should state the exact order of:

- eligibility;
- tiering;
- review;
- payment;
- pro-rata scaling;
- queueing;
- randomization;
- and residual assignment.

## Capacity and Participant Limits

### Capacity States

The window should distinguish:

- approved maximum capacity;
- capacity reserved for tiers;
- unreserved capacity;
- capacity requested;
- capacity associated with complete submissions;
- capacity associated with eligible submissions;
- capacity provisionally allocated;
- capacity finally allocated;
- capacity settled;
- capacity claim-funded;
- capacity released;
- cancelled or expired capacity;
- returned capacity;
- and unused closing capacity.

### Participant Limits

Limits may apply per:

- person;
- entity;
- account;
- wallet;
- linked group;
- partner;
- jurisdiction;
- tier;
- period;
- or lifetime under the stated program.

The controlling limit dimension should be published.

### Linked Participants

The record should define treatment of:

- related entities;
- common beneficial ownership;
- shared devices;
- shared payment accounts;
- shared wallets;
- delegated wallets;
- custodial accounts;
- and household or organizational relationships where applicable and legally supported.

### Capacity Reuse

Cancelled, rejected, unpaid, expired, or returned capacity may be:

- reallocated to the queue;
- offered to a waitlist;
- returned to general window capacity;
- held for correction;
- or returned to the source allocation.

The active notice should state the method.

## Pricing and Consideration

Where payment applies, the window should use the approved pricing mechanism.

### Required Pricing Fields

- calculation currency;
- price unit;
- reference source or sources;
- observation time or period;
- source-failure treatment;
- floor, cap, premium, discount, or adjustment rule where approved;
- rounding;
- precision;
- fee treatment;
- conversion treatment;
- payment deadline;
- stale-price treatment;
- and correction method.

Detailed rules remain controlled by [FUZE Vault Access Pricing Mechanism](18-FUZE_VAULT_ACCESS_PRICING_MECHANISM_PUBLIC.md).

### Price Is Not a Forecast

A window price is an input to a bounded allocation process.

It does not predict or guarantee:

- future token price;
- market value;
- liquidity;
- resale;
- exchange listing;
- or financial return.

### Supported Consideration

Consideration may include an approved:

- stablecoin payment;
- fiat payment route;
- product-use condition;
- verified contribution;
- partner milestone;
- grant basis;
- or another legally and operationally supported condition.

### Unit Separation

The process should keep separate:

- FUZE allocated;
- stablecoin paid;
- fiat paid;
- fees;
- refunds;
- Platform Credits;
- product-use metrics;
- contribution scores;
- and accounting values.

## Payment, Proceeds, Refund, and Settlement Controls

### Payment Instruction

Where payment applies, the participant should receive an instruction identifying:

- payment asset;
- network;
- canonical contract or native-asset status;
- amount;
- destination;
- memo or reference where required;
- deadline;
- fee responsibility;
- required confirmation;
- and support route.

### Payment Verification

Verification should confirm:

- sender or participant linkage where required;
- asset;
- network;
- amount;
- destination;
- transaction or provider reference;
- confirmation or finality;
- payment deadline;
- and duplicate-use status.

### Stablecoin Treatment

Stablecoin use should account for:

- issuer;
- depeg risk;
- freeze or blacklist risk;
- network congestion;
- fees;
- unsupported bridge or wrapped assets;
- custody support;
- and wrong-network risk.

Stablecoin payment remains a settlement rail and does not merge with the FUZE allocation ledger.

### Overpayment

The notice should define whether overpayment is:

- refunded;
- applied up to the participant limit with the remainder refunded;
- held pending instruction;
- or rejected.

### Underpayment

The notice should define whether underpayment causes:

- remediation within a deadline;
- proportional allocation;
- reduced allocation;
- rejection;
- or refund.

### Late Payment

Late payment should follow the published rule and should not receive discretionary acceptance without authorized exception treatment.

### Proceeds Route

The proceeds record should identify:

- receiving vault or provider;
- asset;
- amount;
- fees;
- conversions;
- refunds;
- accounting classification;
- tax owner;
- reconciliation owner;
- and current status.

### Refunds and Reversals

A refund record should identify:

- participant private reference;
- original payment;
- reason;
- refundable amount;
- non-refundable fees where legally supported and disclosed;
- refund asset and network;
- verified return destination;
- transaction or provider reference;
- confirmation;
- accounting effect;
- allocation effect;
- and closure status.

Refunds should use a verified route and should not be redirected solely through an informal message.

### Settlement

Settlement should require agreement among:

```text
approved participant allocation
<-> verified consideration or qualifying basis
<-> source-vault commitment
<-> proceeds or evidence record
<-> release or claim instruction
```

A payment alone does not establish settlement when eligibility, allocation, or another condition remains incomplete.

## Release, Claim, Lock, Vesting, and Custody Treatment

### Direct Release

Approved FUZE transfers after settlement and final checks.

The record should identify continuing restrictions and circulation treatment.

### Claim Release

Approved FUZE becomes claimable through an active claim route.

The process should define:

- claim opening;
- claim closing;
- destination verification;
- claim security;
- unclaimed treatment;
- failed-claim treatment;
- and correction route.

### Staged Release

Approved FUZE becomes available in defined portions.

Each stage should identify:

- amount or percentage;
- timing or condition;
- continuing restrictions;
- prior released amount;
- and next stage.

### Time Lock

Transfer remains restricted until a stated time or condition.

Unlock does not automatically establish circulation or liquidity.

### Vesting

Release follows a defined time, service, milestone, contribution, or hybrid schedule.

The participant record should distinguish:

- allocated;
- unvested;
- vested;
- vested-unreleased;
- released;
- cancelled;
- and returned amounts.

### Program Custody

FUZE remains in a contract or controlled account for an approved program purpose.

Program custody should identify:

- participant rights;
- withdrawal conditions;
- transfer restrictions;
- return rights;
- and circulation treatment.

### Participant Record

The participant record should identify:

- approved allocation;
- settled amount;
- claim-funded amount;
- claimable amount;
- claimed amount;
- released amount;
- locked or unvested amount;
- next condition;
- expired amount;
- returned amount;
- correction status;
- and current status.

Release classification remains governed by [FUZE Vault-by-Vault Release Rules](15-FUZE_VAULT_BY_VAULT_RELEASE_RULES_PUBLIC.md) and [FUZE Controlled Circulation Policy](12-FUZE_CONTROLLED_CIRCULATION_POLICY_PUBLIC.md).

## Duplicate, Abuse, Fraud, and Restricted-Activity Controls

Controls should be proportionate to the participant class, jurisdiction, consideration, capacity, and risk.

Possible controls include:

- person, entity, account, wallet, or linked-group limits;
- repeated-submission detection;
- device, session, or behavioral signals where legally supported;
- payment-source verification;
- wallet-control verification;
- prior-allocation checks;
- sanctions or restricted-activity screening where required;
- bot and automation defenses;
- manual-review thresholds;
- unusual-payment review;
- referral or contribution verification;
- document-integrity checks;
- and conflict or related-party review.

### False Positives

Automated controls can be wrong.

The process should provide:

- manual review;
- reason codes;
- evidence correction;
- and reconsideration where appropriate.

### Fraud or Abuse Finding

Possible outcomes include:

- rejection;
- allocation cancellation;
- payment refund under the terms;
- claim suspension;
- release suspension;
- recovery where possible;
- account restriction;
- incident escalation;
- or legal or compliance referral.

Public reporting should use aggregate categories and should not expose private allegations without authority.

## Pause, Cancellation, Amendment, Extension, and Supersession

### Pause Triggers

A window may pause when a material issue affects:

- legal or jurisdiction support;
- source allocation or vault authority;
- available capacity;
- pricing or market-data integrity;
- payment route;
- proceeds route;
- eligibility rules;
- duplicate or abuse controls;
- application system;
- allocation calculation;
- claim, vesting, lock, or release system;
- custody or signer integrity;
- security or privacy;
- reconciliation;
- public notice accuracy;
- or participant support.

### Pause Record

The record should identify:

- affected stage;
- effective time;
- reason at a public-safe level;
- submissions affected;
- payments affected;
- allocations affected;
- claims or releases affected;
- interim participant treatment;
- refund treatment;
- reactivation conditions;
- review owner;
- and current status.

### Reactivation

Reactivation should require:

- issue containment;
- corrected rules, systems, data, or authority;
- testing where applicable;
- affected-record reconciliation;
- renewed approval;
- revised notice where material;
- and participant communication.

### Cancellation

Cancellation requires a plan for:

- applications;
- eligibility decisions;
- waitlists;
- allocations;
- received consideration;
- refunds;
- fees;
- committed FUZE;
- claim funding;
- released FUZE;
- records;
- support;
- public communication;
- and final reconciliation.

Cancellation cannot reverse an irreversible token transfer automatically.

### Amendment

A material amendment should identify:

- prior version;
- new version;
- changed fields;
- reason;
- affected participants;
- effective time;
- opt-out or refund treatment where applicable;
- renewed reviews;
- approval;
- and public notice.

A material amendment should not be applied retroactively without a documented basis and participant treatment.

### Extension

An extension should identify:

- original closing boundary;
- new closing boundary;
- reason;
- capacity effect;
- pricing or source-data effect;
- participant treatment;
- approvals;
- and publication time.

### Supersession

A new window version should link to the prior version and explain whether prior:

- applications;
- eligibility decisions;
- allocations;
- payments;
- claims;
- releases;
- and disputes

continue, migrate, close, or require new action.

## Complaints, Disputes, and Corrections

### Complaint Route

The public notice should identify a support or complaint route for:

- submission problems;
- eligibility decisions;
- allocation calculations;
- payment recognition;
- refunds;
- claim or release problems;
- account or wallet verification;
- and incorrect public records.

### Dispute Record

A dispute record should identify:

- private participant reference;
- window version;
- affected application, allocation, payment, claim, or release;
- issue class;
- evidence;
- status;
- reviewer;
- interim treatment;
- decision;
- correction or refund effect;
- and closure.

### Correction

A correction may address:

- incorrect eligibility;
- duplicate allocation;
- wrong amount;
- wrong price;
- wrong payment classification;
- missing payment;
- wrong destination;
- failed refund;
- claim error;
- release error;
- stale status;
- or public-report error.

The correction should preserve the original record and link to the revised record.

### No Hidden Manual Adjustment

Manual adjustments should identify:

- original result;
- revised result;
- reason;
- authority;
- evidence;
- participant effect;
- capacity effect;
- treasury effect;
- and reporting effect.

## Reconciliation

### FUZE Capacity Reconciliation

```text
opening approved FUZE capacity
- final approved allocations
- active reserved or pending allocations
+ cancelled, expired, rejected, or returned allocations
+/- approved corrections
= unused closing capacity
```

### Source-Vault Reconciliation

```text
opening source-vault balance
- confirmed releases or claim-funding transfers
+ verified returns and recoveries
+/- approved corrections
= closing source-vault balance
```

### Consideration Reconciliation

Where payment applies:

```text
verified consideration received
- refunds
- reversals or chargebacks
- approved fees
- approved conversions or transfers
+/- corrections
= reconciled net proceeds or closing proceeds balance
```

### Participant-State Reconciliation

```text
approved participant allocation
= payment-pending or qualifying-basis-pending amount
+ settled amount
+ cancelled or expired amount
+/- corrections
```

For settled allocations:

```text
settled amount
= awaiting claim funding
+ claimable
+ claimed pending transfer
+ released
+ locked or vesting under the stated method
+ returned or cancelled after settlement
+/- corrections
```

The exact categories should be mutually exclusive under the window methodology.

### Program Reconciliation

The final report should reconcile:

- applications;
- complete applications;
- eligible applications;
- waitlisted applications;
- rejected or withdrawn applications;
- approved allocations;
- payment-pending allocations;
- settled allocations;
- claim-funded amounts;
- claimable amounts;
- released amounts;
- locked or vesting amounts;
- refunded amounts;
- returned amounts;
- disputes;
- corrections;
- and unused capacity.

### Unit Separation

FUZE quantities, stablecoin amounts, fiat amounts, Platform Credits, contribution measurements, application counts, participant counts, and accounting values should remain separately labeled.

## Public Status and Final Reporting

### Status Updates

Public status may show:

- proposed;
- activation pending;
- upcoming;
- active;
- capacity reached;
- paused;
- processing;
- allocation pending;
- allocated;
- settlement pending;
- settled;
- claim funding;
- claimable;
- releasing;
- closing;
- closed;
- cancelled;
- corrected;
- superseded;
- and archived.

### Aggregate Progress Fields

Where approved, a public progress view may show:

- approved maximum capacity;
- applications received;
- eligible applications;
- approved allocations;
- settled allocation amount;
- claim-funded amount;
- released amount;
- returned amount;
- unused capacity;
- and freshness status.

These fields should identify whether they are:

- point-in-time;
- period flow;
- cumulative;
- estimated;
- provisional;
- reviewed;
- or final.

### Final Report

The final report may include:

- window identifier and version;
- source allocation;
- source-vault opening and closing balances;
- approved capacity;
- opening and closing times;
- participant class;
- application totals;
- eligibility totals;
- allocation method;
- pricing or qualifying-basis method;
- approved allocation amount;
- verified consideration;
- refunds and reversals;
- net proceeds where applicable;
- settled amount;
- claim-funded amount;
- claimable amount;
- released amount;
- locked or vesting amount;
- returned amount;
- unused capacity;
- exceptions and disputes;
- corrections;
- circulation treatment;
- evidence references;
- methodology;
- limitations;
- review and approval;
- and current-as-of date.

### Privacy

Public reporting should not expose:

- participant identity;
- private account data;
- private wallet-person mappings;
- verification documents;
- private payment details;
- private tax information;
- private complaints or allegations;
- credentials;
- private keys;
- recovery material;
- or security-sensitive procedures.

## Evidence and Record Retention

The window evidence package should retain, as applicable:

- proposal;
- approved window record;
- all versions;
- activation-gate evidence;
- public notices;
- applications;
- eligibility evidence;
- decision records;
- allocation calculations;
- pricing records;
- payment instructions;
- payment and refund records;
- proceeds records;
- claim-funding records;
- claim and release records;
- source-vault transactions;
- participant communications;
- complaints and disputes;
- incidents;
- corrections;
- reconciliation;
- final report;
- and archive references.

Retention should follow the applicable privacy, legal, accounting, tax, compliance, security, and operational requirements.

Public evidence may use:

- transaction hashes;
- contract references;
- governance references;
- methodology versions;
- report identifiers;
- aggregate status;
- and approved hashes or attestations.

A public hash does not replace the underlying accountable process.

## Closure and Archive

A window can close when:

- new applications have ended;
- capacity allocation is complete;
- payments and refunds are reconciled;
- claims and releases are complete or controlled;
- unresolved items have owners and treatment;
- source-vault and proceeds balances reconcile;
- final reporting is approved;
- and archive materials are ready.

### Closure Record

The closure record should identify:

1. window identifier and version;
2. closing reason;
3. final status;
4. approved capacity;
5. allocated amount;
6. settled amount;
7. released amount;
8. locked or vesting amount;
9. refunded amount;
10. returned amount;
11. unused capacity;
12. unresolved disputes or claims;
13. source-vault closing balance;
14. proceeds closing status;
15. corrections;
16. final report;
17. evidence-retention owner;
18. closure authority;
19. archive location; and
20. current-as-of date.

### Archive

The archive should preserve:

- original notice;
- all material amendments;
- status history;
- pricing or qualifying methodology;
- allocation method;
- final report;
- corrections;
- supersession links;
- and public evidence.

Archived records should be clearly marked as historical and should not imply current access.

## Separation from Adjacent Systems

| System or process | Primary role | Why it remains separate |
|---|---|---|
| Public vault visibility | Publishes approved vault, balance, state, event, and evidence information | Visibility does not create access |
| Public vault access window | Defines a bounded participation, allocation, settlement, and release process | Does not itself determine market price or listing |
| Vault access pricing | Defines reproducible pricing inputs and calculations | Pricing does not create eligibility or allocation |
| Community Participation Round | Defines one community participation framework | Not every access window is a community round |
| Participation Activation Gates | Defines broader activation readiness | Window-specific gates remain in the operating record |
| Vault-by-vault release rules | Defines allocation-specific release authority | Window allocation does not equal token release |
| Controlled circulation | Governs movement and final token-state classification | Release does not equal circulation |
| Stablecoin compensation | Settles approved business obligations | Window payments are participant consideration, not compensation |
| Platform Credits | Product-consumption units | Platform Credits are not FUZE token allocation or payment unless separately supported |
| Approved distributable value | Reviewed value from defined product-revenue pools | Window capacity and proceeds are not approved distributable value |
| Wallet-based participation | Activation-gated eligibility, claim, and payout process | It does not automatically create a public vault access window |
| Liquidity and listing policy | Governs market structure and venue processes | Access and release do not establish listing or liquidity |

## Status and Evidence

This paper defines the public vault access-window process.

It does not independently prove that any current window, sale, participant route, pricing method, payment route, claim process, token release, liquidity deployment, or listing is active.

| Status claim | Evidence direction |
|---|---|
| Window proposed | Proposal, purpose, source, participant class, capacity, dependencies, owner, and status |
| Window approved | Complete record, exact version, gate conditions, reviewers, authority, and decision |
| Window announced | Public notice, version, publication time, status, support route, and current-as-of date |
| Window active | Completed activation gates, active systems, opening time, source capacity, monitoring, and notice |
| Application received | Window version, participant private reference, submission time, required fields, and status |
| Participant eligible | Active criteria, evidence, checks, decision, reason code, reviewer or rule version, and status |
| Participant allocated | Eligible decision, allocation method, amount, capacity effect, notice, and expiry treatment |
| Payment verified | Approved asset and network, amount, destination, transaction or provider reference, finality, and participant linkage |
| Allocation settled | Approved allocation, verified payment or qualifying basis, source commitment, reconciliation, and status |
| Tokens claimable | Claim funding, active claim route, participant allocation, claim period, and current status |
| Tokens released | Release instruction, source allocation, destination, amount, transaction, confirmation, restrictions, and classification |
| Window paused | Trigger, affected stage, effective time, participant treatment, authority, and reactivation conditions |
| Window cancelled | Decision, scope, application treatment, payment and refund treatment, token treatment, reporting, and closure plan |
| Window closed | Final allocations, payments, refunds, releases, returns, balances, exceptions, report, and closure authority |
| Window corrected | Original record, issue, revised data or decision, evidence, authority, participant effect, and public update |
| Window archived | Final status, archive location, methodology, reports, corrections, and historical notice |

The following do not independently establish an active access window or participant right:

- this paper;
- a visible vault;
- an allocation balance;
- a wallet connection;
- a product account;
- token ownership;
- a community post;
- a pricing example;
- an application form draft;
- a payment address;
- an internal spreadsheet;
- a transaction hash;
- code;
- a repository;
- a partnership announcement;
- or a listing discussion.

## Access, Release, Circulation, Market, and Outcome Separation

The following remain separate:

- public visibility;
- window proposal;
- approval;
- announcement;
- activation;
- access;
- application;
- completeness;
- eligibility;
- waitlisting;
- allocation;
- payment instruction;
- payment verification;
- settlement;
- claim funding;
- claimability;
- claim completion;
- release approval;
- transaction execution;
- release;
- lock or vesting;
- circulation;
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

An active window, approved allocation, participant payment, settlement, claim, or release does not guarantee:

- full participant allocation;
- immediate token transfer;
- unrestricted transferability;
- resale;
- DEX access;
- CEX listing;
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

This paper publishes the access-window purpose, source, record, lifecycle, activation, notice, eligibility, application, allocation, capacity, pricing-boundary, payment, settlement, release, pause, refund, reconciliation, reporting, privacy, closure, and archive framework.

It does not publish or establish current:

- active window;
- token sale;
- solicitation;
- source-vault address;
- payment address;
- supported payment asset;
- pricing source;
- opening or closing date;
- participant eligibility;
- participant identity;
- allocation amount;
- claim window;
- release amount;
- vesting schedule;
- stablecoin proceeds;
- refund obligation;
- token circulation;
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

unless those details are separately approved and supported by a current active-window notice, source-vault record, pricing record, payment instruction, allocation decision, claim record, release report, transaction record, specialist paper, or public status report.

Every actual window remains subject to its controlling allocation, vault, pricing, treasury, product, community, partner, legal, accounting, tax, compliance, sanctions, jurisdiction, technical, security, privacy, custody, claim, release, circulation, reporting, and support requirements.

## Key Takeaways

- A FUZE Public Vault Access Window is a bounded, versioned process, not an automatic consequence of publishing a vault or allocation balance.
- Visibility, access, application, eligibility, allocation, payment, settlement, claimability, release, lock, vesting, and circulation are separate states.
- Only allocation categories whose mandates support the stated purpose may fund a window; unused capacity remains with the source allocation unless separately authorized.
- A complete window record should define source, capacity, participant class, eligibility, timing, allocation, pricing or qualifying basis, payment, proceeds, release, refunds, controls, reporting, and closure before activation.
- A window should not become active until all applicable source, capacity, legal, treasury, pricing, payment, eligibility, technical, security, privacy, reporting, and support gates pass.
- Public notices should state the exact status and should not describe an upcoming or conditional process as active.
- Allocation methods, participant limits, queue treatment, reserved tiers, rounding, and residual capacity should be reproducible.
- Payment, proceeds, refunds, and token allocation should use separate ledgers and reconcile before settlement.
- Direct release, claim release, staged release, time lock, vesting, and program custody require distinct participant and reporting states.
- Pauses, cancellations, amendments, extensions, disputes, and corrections should preserve participant treatment and historical evidence.
- Final reporting should reconcile applications, eligibility, allocations, consideration, refunds, settlement, claims, releases, returns, unused capacity, and source-vault balances.
- This framework announces no current window and creates no sale, entitlement, listing, liquidity, price support, income, revenue share, or financial return.
