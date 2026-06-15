# FUZE Wallet-Based Privacy and Eligibility

## Executive Summary

FUZE can use wallet addresses and public blockchain evidence without publishing the personal identity behind each address. Public records can show functional labels, snapshot references, eligibility statuses, claim states, report hashes, and corrections while identity, account, jurisdiction, and verification evidence remain permissioned.

Eligibility is a decision for a defined process and period. It depends on the active rules, wallet or beneficial ownership evidence, snapshot method, custody type, wallet category, jurisdiction, required verification, duplicate controls, and current system status. A FUZE balance can be one input, but it is not a complete eligibility decision.

This paper defines the privacy and data controls around that decision: field classification, evidence collection, wallet-person separation, status reasons, access control, retention, disclosure, disputes, corrections, and incidents.

The participation mechanism itself remains in the protected [FUZE Wallet-Based Participation Model](07-FUZE_WALLET_BASED_PARTICIPATION_MODEL_PUBLIC.md). Exchange and omnibus custody treatment is maintained in its dedicated custody paper.

---

## 1. Policy Objective

The policy should let FUZE determine and report wallet status while answering:

1. Which public evidence supports the wallet record?
2. Which private evidence supports control or beneficial ownership?
3. Which active eligibility rules were applied?
4. Why did the wallet receive its current status?
5. Who can inspect or change the record?
6. How long is supporting data retained?
7. How can an error or dispute be corrected?

The objective is verifiable status with minimum identity exposure.

---

## 2. Core Privacy Model

FUZE separates three layers.

### Public wallet layer

Contains blockchain identifiers, public transactions, functional labels, public status fields, report references, and approved aggregate information.

### Permissioned eligibility layer

Contains wallet-control evidence, account or custody evidence, jurisdiction status, verification results, reason codes, reviewer actions, and dispute records.

### Restricted identity layer

Contains personal or entity identity, contact details, documents, source records, legal or compliance evidence, and sensitive ownership mappings where required.

The layers can be linked through controlled identifiers. The public layer should not expose the private linkage.

---

## 3. Field Classification

| Field | Normal treatment |
|---|---|
| Wallet address | Public where needed for transparency or direct status |
| Functional wallet label | Public when approved |
| Snapshot block or timestamp | Public |
| Aggregate balance or category | Public or public summary |
| Eligibility status | Public, pseudonymous, or aggregate according to the active process |
| Status reason | Public category or permissioned detail |
| Claim or release status | Public-safe where the process is active |
| Wallet-control proof | Permissioned |
| Exchange or custodian statement | Permissioned |
| Personal or entity identity | Restricted |
| Contact information | Restricted |
| Identity and verification documents | Restricted |
| Jurisdiction evidence | Restricted or permissioned result |
| Legal, tax, or account records | Restricted |
| Support and dispute evidence | Permissioned or restricted |

Classification should be set before collection and reviewed before publication.

---

## 4. Wallet-Person Separation

A wallet address identifies a blockchain account, not necessarily one natural person.

A wallet can represent:

- one self-custody user;
- a multisignature group;
- a company or institution;
- an exchange or custodian;
- a smart contract;
- a treasury, reserve, vesting, or program function;
- multiple beneficial users through an omnibus structure.

FUZE should avoid publishing a person's name beside an address unless the association is already authorized and necessary for the public purpose.

Internally, a controlled mapping can connect an applicant or account reference to one or more wallets. Access to that mapping should be limited and logged.

---

## 5. Eligibility Record

Each decision should use a versioned eligibility record.

| Field | Required content |
|---|---|
| Record ID | Stable internal identifier |
| Process and period | Framework, program, snapshot, or claim scope |
| Rule version | Eligibility method applied |
| Wallet or custody reference | Address, account, contract, or custodian record |
| Wallet category | Self-custody, exchange, contract, treasury, vesting, partner, or another approved category |
| Holding evidence | Balance and timing under the active method |
| Control or ownership result | Verified, pending, unsupported, disputed, or exempt under rules |
| Jurisdiction result | Supported, restricted, pending, or unavailable |
| Verification result | Required checks completed or outstanding |
| Status | Eligible, in review, restricted, ineligible, expired, paused, or corrected |
| Reason code | Standard explanation for the status |
| Reviewer and time | Accountable decision evidence |
| Public treatment | Public, pseudonymous, aggregate, or private |

The record should preserve the rule version because later policies can differ.

---

## 6. Eligibility Criteria

An active process can require:

- a defined FUZE balance or holding condition;
- inclusion at a stated snapshot;
- proof of wallet control or beneficial ownership;
- supported custody;
- an eligible wallet category;
- supported jurisdiction;
- completion of required private verification;
- compliance with lock, vesting, transfer, or program rules;
- absence of duplicate or abusive claims;
- an active framework and claim period.

Each criterion should have a source, test, result, and reason code.

Token ownership alone cannot establish beneficial ownership behind an exchange wallet, supported jurisdiction, wallet category, duplicate status, or framework activation.

---

## 7. Proof Methods

### Wallet signature

Demonstrates control of a supported self-custody address at the verification time. The signed message should include domain, purpose, nonce, network, and expiration.

### On-chain evidence

Can establish balance, transaction, contract position, lock, vesting, or snapshot state under a stated method.

### Custodian or exchange evidence

Can support beneficial position, account history, deposit or withdrawal, and applicable timing. Authenticity and account linkage require review.

### Contract evidence

Can support ownership or authority in a multisignature, smart-contract wallet, staking position, liquidity position, or vault.

### Private identity or entity evidence

Can support jurisdiction, account ownership, qualification, or another required rule. FUZE should record the minimum necessary result rather than publishing the source documents.

One proof method can be insufficient for a particular process. The active rule should define acceptable combinations.

---

## 8. Snapshot Privacy

A snapshot can contain wallet addresses and balances that are already observable on-chain. FUZE should still define why it creates, enriches, and publishes the snapshot.

The snapshot method should state:

- contract and network;
- block or timestamp;
- included and excluded balance types;
- wallet-category treatment;
- custody treatment;
- correction window;
- public fields;
- retention and archive.

Adding eligibility, jurisdiction, identity, or claim information to a public address can increase privacy risk beyond the original blockchain data. Those enriched fields should be minimized and published only at the level needed for review.

A Merkle root, report hash, aggregate count, or status endpoint can sometimes provide evidence without publishing the full enriched dataset.

---

## 9. Status and Reason Codes

Standard statuses make decisions understandable.

| Status | Meaning |
|---|---|
| Eligible | All required criteria pass for the defined process |
| In review | Evidence or specialist review remains open |
| Restricted | A rule currently prevents access but the record remains active |
| Ineligible | One or more final criteria fail |
| Unsupported custody | Required user-level records or interaction cannot be supported |
| Duplicate | The same position or right appears in another record |
| Expired | The applicable period or action window ended |
| Paused | Processing is temporarily suspended |
| Corrected | A prior decision has been superseded |

Reason codes should explain the category without exposing sensitive facts. Detailed reviewer notes remain permissioned.

---

## 10. Wallet Categories

Wallet categories can affect eligibility because balances have different purposes.

Possible categories include:

- ordinary self-custody holder;
- exchange or omnibus custody;
- institutional custody;
- contract wallet or multisignature;
- treasury or reserve;
- team, advisor, partner, or vesting;
- liquidity or market operations;
- migration;
- claim or distribution contract;
- bridge or represented supply;
- disputed or recovery wallet.

Category assignment should be evidence-based and correctable. A label should never be used to identify a private person publicly.

---

## 11. Transfers and Status

Eligibility attaches to the active rules rather than permanently following tokens.

A transfer can affect:

- snapshot balance;
- holding-period condition;
- beneficial ownership;
- lock or vesting;
- duplicate status;
- jurisdiction;
- custody support;
- claim completion;
- private contractual rights.

The policy should state whether status depends only on the snapshot, requires continued holding, can move to a replacement wallet, or expires after transfer.

OTC receipt of FUZE does not automatically transfer a seller's historical snapshot, private agreement, migration status, or prior eligibility.

---

## 12. Custody Boundary

Self-custody can support direct signatures and address-level evidence. Exchange, institutional, or omnibus custody can require account records and intermediary cooperation.

The eligibility system should record:

- who controls the on-chain wallet;
- who is the claimed beneficial holder;
- which evidence connects them;
- whether the custody provider supports the process;
- whether direct contract interaction is possible;
- how deposits, withdrawals, and cutoffs are treated.

Detailed exchange and custodian scenarios belong in [FUZE Exchange Custody and Wallet Participation](27-FUZE_EXCHANGE_CUSTODY_AND_WALLET_PARTICIPATION_PUBLIC.md).

---

## 13. Data Minimization

FUZE should collect only information required for the stated eligibility purpose.

Before adding a field, the owner should ask:

1. Which rule requires it?
2. Can a yes/no result replace the source document?
3. Can an aggregate or hash support public reporting?
4. Who needs access?
5. When can the data be deleted or de-identified?
6. What happens if the field is wrong or exposed?

Documents should not be collected merely because they might become useful later.

---

## 14. Access Control and Logging

Permissioned and restricted records should use role-based access.

Roles can include:

- eligibility operator;
- support reviewer;
- legal or compliance reviewer;
- treasury or accounting reviewer;
- privacy or security administrator;
- auditor or independent reviewer where required.

Access logs should record user, record, action, time, and purpose. Export, bulk search, and identity-wallet mapping should receive stronger controls than ordinary status review.

Access should be removed when a role ends or the purpose expires.

---

## 15. Retention

Retention should reflect the process, legal requirements, dispute period, audit need, security exposure, and data class.

The retention record should define:

- source documents retained;
- derived status retained;
- public snapshot or hash retained;
- start and end event;
- archive or deletion method;
- holds for disputes or investigations;
- owner and review cadence.

Where source evidence can be deleted, FUZE may retain a decision result, reason, method version, and audit reference. Public blockchain records themselves remain outside FUZE's deletion control.

---

## 16. User Notice and Consent

Where FUZE collects private evidence, the user-facing notice should explain:

- purpose of collection;
- required and optional fields;
- public and private treatment;
- reviewers and service providers where applicable;
- retention;
- correction and dispute route;
- effect of declining required evidence;
- security and incident contact route.

Consent should not be used as a substitute for another required legal basis, and public wallet activity should not be presented as consent to publish personal identity.

---

## 17. Disputes and Corrections

A user can dispute wallet category, balance, custody, control, jurisdiction, duplicate status, or another eligibility result through the approved support route.

The case record should contain:

1. disputed decision and reason code;
2. original evidence and rule version;
3. new evidence;
4. reviewer findings;
5. revised status;
6. approval and effective time;
7. affected claim, allocation, or report;
8. public correction reference where needed.

Corrections should preserve the previous decision and explain the change without publishing the private evidence.

---

## 18. Privacy Incidents

A privacy incident can involve unauthorized access, disclosure, incorrect wallet-person mapping, public identity exposure, document loss, or compromised verification data.

The response should:

- contain access and preserve evidence;
- identify affected fields and people;
- correct public labels or records;
- revoke credentials or links;
- assess notification and legal requirements;
- monitor downstream misuse;
- document remediation and prevention.

Where on-chain publication cannot be removed, FUZE should avoid adding further identifying context and use correction or replacement records where appropriate.

---

## 19. Public Reporting

Public eligibility reporting can include:

- process and rule version;
- snapshot block or cutoff;
- wallet and custody categories;
- aggregate eligible, restricted, ineligible, disputed, and corrected counts;
- claim or participation status where active;
- report hash and methodology;
- pause and correction notices.

Address-level status should be published only where the active process requires it and privacy review supports it.

Reports must keep names, contact details, identity documents, exchange account records, jurisdiction evidence, private agreements, and wallet-person mappings private.

---

## 20. Boundaries

This policy governs privacy and eligibility records. It does not activate participation, approve distributable value, open a claim, or guarantee that any custody type will be supported.

Eligibility is specific to a process and period. It can change with rules, evidence, transfers, custody, jurisdiction, or system status.

Detailed privacy, eligibility, custody, and participation risks are consolidated in [FUZE Token Risk Boundaries](29-FUZE_TOKEN_RISK_BOUNDARIES_PUBLIC.md).

---

## Conclusion

FUZE wallet transparency can remain useful without turning addresses into public identity records.

Layered data classification, minimum evidence, controlled wallet-person mappings, versioned eligibility decisions, reason codes, access logs, retention, dispute handling, and privacy incident response allow FUZE to publish reviewable status while keeping personal and account information permissioned.
