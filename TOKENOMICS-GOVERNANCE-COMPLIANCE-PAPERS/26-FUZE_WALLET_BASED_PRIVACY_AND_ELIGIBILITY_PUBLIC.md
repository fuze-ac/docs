
# FUZE Wallet-Based Privacy and Eligibility

## Executive Summary

FUZE can use wallet addresses and public blockchain evidence without publishing the personal identity behind each address. Public-safe records may show functional wallet labels, snapshot references, eligibility status, claim status where an activated process exists, report hashes, and corrections. Identity, account, jurisdiction, tax, legal, and verification evidence remains permissioned or restricted.

Eligibility is a decision for one defined process and period. A FUZE token balance may be one input, but it does not by itself establish wallet control, beneficial ownership, supported custody, jurisdiction, wallet category, duplicate treatment, private verification, framework activation, or an entitlement.

This paper defines the privacy and eligibility control model: data classification, wallet-person separation, proof methods, versioned decisions, custody treatment, access control, retention, user notice, disputes, corrections, incident handling, and public-safe reporting.

The wallet-based participation framework remains activation-gated under the [FUZE Wallet-Based Participation Model](07-FUZE_WALLET_BASED_PARTICIPATION_MODEL_PUBLIC.md). Exchange, institutional, and omnibus custody treatment is controlled by [FUZE Exchange Custody and Wallet Participation](27-FUZE_EXCHANGE_CUSTODY_AND_WALLET_PARTICIPATION_PUBLIC.md).

## 1. Purpose and Primary Readers

This paper is written primarily for eligibility operators, privacy and security reviewers, legal and compliance reviewers, product and technical teams, support operators, auditors, custody partners, and participants who need to understand how FUZE separates public wallet evidence from private identity evidence.

The policy should answer:

1. Which public evidence supports a wallet record?
2. Which permissioned evidence supports control or beneficial ownership?
3. Which rule version and process were applied?
4. Why did the wallet receive its current status?
5. Who can inspect, export, or change the record?
6. How long is supporting data retained?
7. How can an error, dispute, or privacy incident be handled?

The objective is reviewable eligibility with minimum identity exposure.

## 2. Current Public Status

Wallet-based participation is an activation-gated public model. Current documentation defines the intended privacy, eligibility, custody, reporting, and correction controls. It does not by itself prove that:

- an eligibility process is active;
- a snapshot has been approved or completed;
- any wallet is currently eligible;
- a claim period is open;
- approved distributable value exists for a period;
- a contract or registry is active;
- an exchange or custodian supports participation; or
- any wallet has a current payment or participation right.

A stronger status requires current evidence for the exact process, rule version, period, jurisdiction, custody mode, activation approval, and operating route.

## 3. Privacy Architecture

FUZE separates wallet-based records into three layers.

### Public wallet layer

May contain:

- blockchain addresses;
- public transactions;
- approved functional wallet labels;
- snapshot block or timestamp;
- public-safe status fields;
- report hashes or audit references;
- correction or pause notices; and
- approved aggregate information.

### Permissioned eligibility layer

May contain:

- wallet-control evidence;
- beneficial-ownership or custody evidence;
- jurisdiction result;
- verification result;
- wallet category;
- reason codes;
- reviewer actions;
- dispute records; and
- process-specific account references.

### Restricted identity layer

May contain:

- personal or entity identity;
- contact information;
- identity documents;
- legal, tax, or compliance evidence;
- private agreements;
- exchange or custodian account records; and
- wallet-to-person mappings.

The layers may be linked through controlled identifiers. The public layer should not expose the private linkage.

## 4. Data Classification

| Field | Normal treatment |
|---|---|
| Wallet address | Public only where needed for transparency or direct status |
| Functional wallet label | Public when approved and non-identifying |
| Snapshot block or timestamp | Public |
| Aggregate balance or category | Public or public-safe summary |
| Eligibility status | Public, pseudonymous, aggregate, or private according to the active process |
| Public reason category | Public-safe where needed |
| Detailed reviewer reason | Permissioned |
| Claim or participation status | Public-safe only where an activated process exists |
| Wallet-control proof | Permissioned |
| Exchange or custodian evidence | Permissioned or restricted |
| Personal or entity identity | Restricted |
| Contact information | Restricted |
| Identity and verification documents | Restricted |
| Jurisdiction evidence | Restricted; a derived result may be permissioned |
| Legal, tax, or account records | Restricted |
| Support and dispute evidence | Permissioned or restricted |

Classification should be assigned before collection and reviewed again before publication, export, or third-party sharing.

## 5. Wallet-Person Separation

A wallet address identifies a blockchain account. It does not necessarily identify one natural person.

A wallet may represent:

- one self-custody user;
- a multisignature group;
- a company or institution;
- an exchange or custodian;
- an omnibus structure representing many users;
- a smart contract;
- a treasury, reserve, vesting, liquidity, migration, or program function; or
- a protocol position represented by another record.

FUZE should not publish a person's name beside an address unless the association is already authorized, necessary for the public purpose, and approved for disclosure.

Internally, a controlled mapping may connect a participant or account reference to one or more wallets. Access to that mapping should be role-limited, logged, reviewable, and removed when no longer required.

## 6. Eligibility Is Process-Specific

Eligibility applies to a named process, rule version, and period. It does not permanently attach to a token or wallet.

An active process may require:

- a defined FUZE balance or holding condition;
- inclusion at a stated snapshot;
- proof of wallet control or beneficial ownership;
- a supported custody method;
- an eligible wallet category;
- a supported jurisdiction;
- required permissioned verification;
- compliance with lock, vesting, transfer, or program rules;
- duplicate and abuse controls;
- an active framework and participation period; and
- completion of all applicable activation gates.

Each criterion should have a source, test, result, and reason code.

Holding FUZE token alone cannot establish beneficial ownership behind an exchange wallet, supported jurisdiction, custody compatibility, category treatment, duplicate status, private verification, or framework activation.

## 7. Versioned Eligibility Record

Each decision should use a versioned record.

| Field | Required content |
|---|---|
| Record ID | Stable internal identifier |
| Process and period | Framework, program, snapshot, claim, or review scope |
| Rule version | Eligibility method applied |
| Wallet or custody reference | Address, account, contract, or custodian reference |
| Wallet category | Self-custody, exchange, contract, treasury, vesting, liquidity, partner, or another approved category |
| Holding evidence | Balance and timing under the active method |
| Control or ownership result | Verified, pending, unsupported, disputed, or exempt under the rules |
| Jurisdiction result | Supported, restricted, pending, or unavailable |
| Verification result | Required checks completed, failed, waived, or outstanding |
| Eligibility status | Eligible, in review, restricted, ineligible, expired, paused, or corrected |
| Reason code | Standard explanation for the status |
| Reviewer and time | Accountable decision evidence |
| Public treatment | Public, pseudonymous, aggregate, or private |
| Supersession reference | Prior record replaced by a correction where applicable |

The rule version must be preserved because a later policy may use different evidence, exclusions, or treatment.

## 8. Proof Methods

### Wallet signature

A valid signature can demonstrate control of a supported self-custody address at the verification time. The signed message should identify the FUZE domain or process, purpose, nonce, network, and expiration.

A signature does not by itself prove beneficial ownership, identity, jurisdiction, source of funds, or every other eligibility condition.

### On-chain evidence

On-chain records can establish a balance, transfer, contract position, lock, vesting state, or snapshot state under a defined method.

The evidence should identify the verified contract, network, block or timestamp, included balance types, and calculation method.

### Custodian or exchange evidence

Custodian records may support a beneficial position, account history, deposit, withdrawal, or cutoff status. Authenticity, account linkage, timing, and reconciliation require review.

### Contract evidence

Contract records may support authority or economic position in a multisignature wallet, smart-contract wallet, staking position, liquidity position, bridge, vesting contract, or vault.

### Private identity or entity evidence

Private evidence may support jurisdiction, account ownership, qualification, tax treatment, or another required rule. FUZE should retain the minimum necessary result and should not publish source documents.

One proof method may be insufficient. The active process should define acceptable evidence combinations, freshness, verification steps, and exception handling.

## 9. Snapshot Privacy

A snapshot may contain wallet addresses and balances already visible on-chain. FUZE should still define why it creates, enriches, retains, and publishes the dataset.

The snapshot method should state:

- verified FUZE contract and network;
- controlling block or timestamp;
- included and excluded balance types;
- wallet-category treatment;
- custody and protocol treatment;
- duplicate prevention;
- correction window;
- public fields;
- retention and archive; and
- report hash or verification method where used.

Adding eligibility, jurisdiction, identity, custody, or claim information to a public address can increase privacy risk beyond the original blockchain record. Enriched fields should be minimized and disclosed only at the level required for the active process.

A Merkle root, report hash, aggregate count, pseudonymous status endpoint, or permissioned verification route may provide useful evidence without publishing the full enriched dataset.

## 10. Eligibility Status and Reason Codes

| Status | Meaning |
|---|---|
| Eligible | All required criteria pass for the defined process and period |
| In review | Evidence or specialist review remains open |
| Restricted | A current rule prevents access while the record remains active |
| Ineligible | One or more final criteria fail |
| Unsupported custody | Required user-level evidence or interaction cannot be supported |
| Duplicate | The same position, balance, or right appears in another record |
| Disputed | Ownership, balance, custody, timing, or another result is contested |
| Expired | The applicable period or action window ended |
| Paused | Processing is temporarily suspended |
| Corrected | A previous decision was superseded by a reviewed correction |

Public reason codes should explain the category without exposing identity, jurisdiction details, account information, private agreements, or sensitive reviewer findings.

Detailed notes remain permissioned.

## 11. Wallet Categories

Wallet category matters because equal balances can have different purposes and controls.

Possible categories include:

- ordinary self-custody holder;
- user multisignature or smart-contract wallet;
- exchange or omnibus custody;
- institutional custody;
- staking, bridge, liquidity, or protocol custody;
- treasury or reserve;
- team, advisor, partner, or vesting;
- liquidity and market operations;
- migration;
- claim or distribution contract;
- disputed or recovery wallet; and
- another approved process-specific category.

Category assignment should be evidence-based, versioned, and correctable. A public category label should describe function without identifying a private person.

## 12. Transfers and Eligibility

Eligibility follows the active rules rather than permanently following transferred tokens.

A transfer may affect:

- snapshot balance;
- holding-period conditions;
- beneficial ownership;
- wallet control;
- lock or vesting status;
- duplicate treatment;
- jurisdiction;
- custody support;
- claim completion; and
- private contractual rights.

The active process should state whether status:

- depends only on a completed snapshot;
- requires continued holding;
- can move to a verified replacement wallet;
- can be affected by custody changes; or
- expires after a transfer or cutoff.

A private or OTC transfer of FUZE token does not automatically transfer a seller's historical snapshot, private agreement, migration status, prior claim, or eligibility record.

## 13. Custody Boundary

Self-custody can support direct signatures and address-level evidence. Exchange, institutional, omnibus, and protocol custody may require account records, intermediary cooperation, reconciliation, and a supported interaction route.

The eligibility record should distinguish:

- who controls the on-chain address;
- who claims beneficial ownership;
- which evidence connects the two;
- whether the custodian supports the process;
- whether direct contract interaction is possible;
- which cutoff controls; and
- how deposits, withdrawals, internal transfers, and pending transactions are treated.

Exchange listing, token custody, wallet visibility, snapshot support, and participation support are separate capabilities.

Detailed custody modes and reconciliation requirements are maintained in [FUZE Exchange Custody and Wallet Participation](27-FUZE_EXCHANGE_CUSTODY_AND_WALLET_PARTICIPATION_PUBLIC.md).

## 14. Data Minimization

FUZE should collect only the information required for the stated process.

Before collecting a field or document, the process owner should ask:

1. Which active rule requires it?
2. Can a yes/no, category, or verification result replace the source document?
3. Can aggregation, hashing, or pseudonymization support the reporting purpose?
4. Who needs access and for how long?
5. Which third parties receive it?
6. When can it be deleted or de-identified?
7. How will an error or disclosure be corrected?

Documents should not be collected merely because they may become useful later.

## 15. Access Control and Audit Logging

Permissioned and restricted records should use role-based and purpose-limited access.

Possible roles include:

- eligibility operator;
- support reviewer;
- legal or compliance reviewer;
- treasury or accounting reviewer;
- privacy or security administrator;
- technical operator; and
- auditor or independent reviewer where required.

Access logs should record the user, role, record, action, time, and purpose. Export, bulk search, identity-wallet mapping, source-document access, and rule changes should receive stronger controls than ordinary status review.

Access should be reviewed periodically and removed when a role, process, legal basis, or retention need ends.

## 16. Retention and Deletion

Retention should reflect the process, legal requirements, dispute period, audit need, security exposure, and data class.

A retention record should define:

- source documents retained;
- derived results retained;
- public snapshot, report, or hash retained;
- start and end event;
- archive, deletion, or de-identification method;
- holds for disputes, investigations, or legal requirements;
- responsible owner; and
- review cadence.

Where source evidence can be deleted, FUZE may retain a decision result, rule version, reason code, approval reference, and audit record.

Public blockchain records remain outside FUZE's deletion control. FUZE should avoid adding unnecessary identifying context to permanent public records.

## 17. User Notice and Permissioned Evidence

Where FUZE collects private evidence, the user-facing notice should explain:

- the process and purpose;
- required and optional information;
- public, permissioned, and restricted treatment;
- reviewers and service providers where applicable;
- retention and deletion;
- correction and dispute routes;
- the effect of declining required evidence; and
- security and incident contact routes.

Public wallet activity should not be treated as consent to publish personal identity.

Consent should not be used as a substitute for another required legal basis where that basis is necessary.

## 18. Third-Party Data Sharing

Where a custodian, identity provider, auditor, service provider, or other approved party handles eligibility data, the arrangement should define:

- the exact purpose;
- minimum fields;
- authority and responsibilities;
- secure transfer method;
- permitted users and onward sharing;
- retention and deletion;
- correction obligations;
- incident responsibilities;
- audit or assurance rights; and
- public reporting boundaries.

Third-party involvement does not make protected records public.

## 19. Disputes and Corrections

A participant may dispute wallet category, balance, custody, control, beneficial ownership, jurisdiction result, duplicate status, cutoff treatment, or another eligibility decision through the approved support route.

The case record should contain:

1. the disputed decision and reason code;
2. the original evidence and rule version;
3. the new evidence submitted;
4. reviewer findings;
5. the revised or confirmed status;
6. approval and effective time;
7. affected claim, participation, allocation, or report; and
8. a public-safe correction reference where required.

Corrections should preserve the previous decision, identify the superseding record, and explain the public change without exposing protected evidence.

## 20. Privacy and Data Incidents

A relevant incident may involve:

- unauthorized access or export;
- disclosure of identity or account records;
- an incorrect wallet-person mapping;
- public identity exposure;
- compromised verification data;
- document loss;
- incorrect eligibility publication; or
- unauthorized third-party sharing.

The response should:

- contain access and preserve evidence;
- identify affected records and people;
- pause affected processing where necessary;
- correct public labels or statuses;
- revoke credentials, links, or integrations;
- assess notification and legal requirements;
- coordinate with affected providers;
- monitor downstream misuse; and
- document remediation and prevention.

Where an on-chain record cannot be removed, FUZE should avoid adding further identifying context and should use correction or replacement records where appropriate.

## 21. Public Reporting

Public eligibility reporting may include:

- process and rule version;
- framework status;
- snapshot block, timestamp, or cutoff;
- supported wallet and custody categories;
- aggregate eligible, restricted, ineligible, disputed, pending, and corrected counts;
- claim or participation status where an activated process exists;
- methodology and report hash;
- pause, incident, and correction notices; and
- reporting period and freshness.

Address-level status should be published only where the active process requires it and privacy review supports it.

Public reports should exclude:

- names and contact details;
- identity documents;
- wallet-to-person mappings;
- exchange and custodian account records;
- jurisdiction source evidence;
- tax and legal records;
- private agreements;
- sensitive reviewer notes; and
- credentials or security procedures.

## 22. Public Boundary

This paper governs privacy and eligibility records. It does not activate wallet-based participation, approve distributable value, open a claim, confirm a snapshot, establish current wallet eligibility, or guarantee support for any custody type.

Eligibility remains specific to one process and period. It may change with rule versions, evidence, transfers, custody, jurisdiction, verification, corrections, or framework status.

Wallet-level transparency does not require public personal identity.

Detailed participation mechanics are maintained in the [FUZE Wallet-Based Participation Model](07-FUZE_WALLET_BASED_PARTICIPATION_MODEL_PUBLIC.md). Detailed custody treatment is maintained in [FUZE Exchange Custody and Wallet Participation](27-FUZE_EXCHANGE_CUSTODY_AND_WALLET_PARTICIPATION_PUBLIC.md). Consolidated risks are maintained in [FUZE Token Risk Boundaries](29-FUZE_TOKEN_RISK_BOUNDARIES_PUBLIC.md).

## Key Takeaways

- A wallet address is a blockchain account identifier, not automatically a public identity record.
- FUZE separates public wallet evidence, permissioned eligibility evidence, and restricted identity evidence.
- Holding FUZE token can be one eligibility condition but is not a complete eligibility decision.
- Eligibility is process-specific, period-specific, rule-versioned, and activation-dependent.
- Self-custody, exchange custody, omnibus custody, contract wallets, and protocol positions require different evidence and treatment.
- Public reporting should use the minimum information needed for verification and should protect wallet-to-person mappings.
- Disputes, corrections, retention, access logs, and incident handling are part of the eligibility system rather than optional administrative steps.