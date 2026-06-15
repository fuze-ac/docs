# FUZE Exchange Custody and Wallet Participation

## Executive Summary

Exchange and institutional custody separate the on-chain wallet from the customer who holds a beneficial account balance. A public exchange address can represent many users, while the exchange controls signing, deposits, withdrawals, internal transfers, and account records.

This structure affects any FUZE process that relies on wallet control, snapshots, beneficial ownership, direct contract interaction, or user-level claims. Support therefore depends on an approved custody mode, exchange cooperation, account evidence, cutoff rules, jurisdiction treatment, reconciliation, and participant communication.

FUZE can support self-custody directly where the active rules permit wallet signatures and address-level evidence. Exchange-held or omnibus balances can require withdrawal before a cutoff, exchange-provided records, an intermediary distribution process, or an unsupported status.

This paper defines those custody modes and operating records. Listing or custody availability alone does not establish participation support.

---

## 1. Custody Objective

The custody framework should answer:

1. Who controls the on-chain address?
2. Who is the beneficial holder?
3. Which record establishes the user-level balance?
4. Can the holder sign or interact directly?
5. How are snapshot cutoffs and transfers handled?
6. Who submits or receives a claim?
7. How are aggregate and user records reconciled?
8. What happens if the custodian cannot support the process?

The objective is accurate user-level treatment where the custody model can support it.

---

## 2. Custody Types

| Type | Control and record model |
|---|---|
| Self-custody | User controls the address and can usually sign directly |
| User multisignature | A defined signer group controls a contract or wallet |
| Smart-contract wallet | Programmable wallet controls execution under its code and signers |
| Exchange custody | Exchange controls wallets and maintains internal customer balances |
| Omnibus custody | One or more on-chain addresses represent many beneficial accounts |
| Institutional custody | Custodian maintains accounts and authority for clients |
| Staking or protocol custody | Tokens sit in a contract with a receipt, share, or position record |
| Vesting custody | Tokens remain under a vesting contract or controlled grant record |
| Treasury or program custody | FUZE or an approved operator controls assets for a defined mandate |

The active process should define which types it supports and what evidence each requires.

---

## 3. Control and Beneficial Ownership

On-chain control and beneficial ownership can differ.

For self-custody, a valid signature can demonstrate address control. It does not by itself establish every legal, jurisdictional, or account fact.

For exchange or omnibus custody:

- the custodian signs transactions;
- the public address can aggregate many users;
- customer balances exist in an internal ledger;
- deposit and withdrawal times can differ from internal trade times;
- the customer may lack direct contract access;
- public chain data cannot allocate the omnibus balance among customers.

Eligibility systems should record both custody control and the claimed beneficial position where relevant.

---

## 4. Custody Support Modes

### Direct self-custody

The participant uses a supported address, signs the required message, appears in the applicable snapshot, and interacts directly with the approved process.

### Withdraw-before-cutoff

An exchange user withdraws FUZE to a supported self-custody wallet before the stated snapshot or registration cutoff.

### Evidence-supported account

FUZE reviews exchange or custodian records that establish the user's eligible balance under the active method.

### Custodian-assisted

The custodian supplies user-level data, submits an aggregate record, or supports claims and internal distribution under an approved arrangement.

### Omnibus representative

The custodian or another authorized representative participates for the omnibus position and remains responsible for user allocation under documented controls.

### Unsupported

The custody method lacks sufficient user-level evidence, cooperation, technical compatibility, jurisdiction support, or reconciliation capability.

The active notice should identify the supported modes rather than asking users to infer them.

---

## 5. Exchange Cooperation Record

Where exchange support is used, the record should define:

| Field | Required content |
|---|---|
| Venue and account model | Exchange, network, wallet, and omnibus structure |
| Supported process | Snapshot, eligibility, migration, claim, or another defined route |
| Customer evidence | Fields and statement or API method supplied |
| Cutoff | Trade, ledger, deposit, withdrawal, or snapshot time |
| Jurisdiction | Supported customer locations and restrictions |
| Data transfer | Format, security, minimization, and retention |
| Claim model | Direct customer, exchange aggregate, or internal distribution |
| Reconciliation | On-chain, omnibus, and customer-ledger matching |
| Exceptions | Frozen accounts, pending withdrawals, disputes, or unsupported balances |
| Communication | Responsibilities for customer notices and support |

Exchange cooperation should be confirmed before public claims of support.

---

## 6. Snapshot Cutoffs

Custody systems can produce several relevant times:

- on-chain block time;
- exchange trade time;
- internal ledger cutoff;
- deposit credit time;
- withdrawal debit time;
- blockchain withdrawal completion;
- statement generation time.

The active method should select the controlling time and explain pending transactions.

For example, a withdrawal requested before the snapshot but completed afterward can appear both as an internal debit and an on-chain exchange balance at the block. Reconciliation rules should prevent double counting or omission.

Cutoffs should use an explicit timezone or block number and a consistent treatment across participants.

---

## 7. User-Level Evidence

Potential evidence includes:

- official account statement;
- transaction and trade history;
- deposit or withdrawal record;
- exchange-signed or custodian-signed confirmation;
- authenticated API record;
- account identifier and beneficial-owner verification;
- custodian allocation file;
- proof of a later self-custody withdrawal.

Screenshots alone can be altered or omit relevant context. The method should define authenticity, required fields, date range, and acceptable combinations.

Evidence should remain permissioned. Public reports can show aggregate custody categories without exposing account identity.

---

## 8. Self-Custody Proof

A self-custody process can require:

1. supported chain and verified FUZE contract;
2. wallet connection or address submission;
3. unique signed message;
4. snapshot or balance check;
5. wallet-category and duplicate review;
6. jurisdiction or private verification where required;
7. destination compatibility;
8. eligibility status.

The signed message should contain the FUZE domain or process, nonce, purpose, network, and expiration to reduce replay and phishing risk.

Lost keys, compromised wallets, contract wallets, and multisignatures require their own support route where available.

---

## 9. Exchange Deposits and Withdrawals

Deposits and withdrawals can affect both evidence and status.

The method should define:

- latest withdrawal time for self-custody treatment;
- pending deposit and withdrawal treatment;
- internal transfer treatment;
- withdrawal fees and net quantity;
- wrong-network or unsupported-asset cases;
- frozen or restricted account cases;
- replacement destination verification.

Users should receive enough notice to understand operational lead times. FUZE cannot control an exchange's processing speed, maintenance, fees, account restrictions, or withdrawal availability.

---

## 10. Claim Models

### Direct wallet claim

An eligible self-custody or compatible contract wallet interacts with the approved claim process.

### Account-evidence claim

The user provides supported custody evidence and receives an approved destination status after review.

### Custodian aggregate claim

The custodian claims or receives an aggregate amount and distributes internally according to the approved user-level ledger.

### Custodian attest-and-direct

The custodian attests eligible customer amounts while users receive directly to verified destination wallets.

### Manual controlled distribution

An operator executes approved user-level records through a permissioned process when direct contract interaction is unsuitable.

Each model should identify liability, custody, data, fees, unclaimed amounts, correction, and user-support responsibilities.

---

## 11. Omnibus Reconciliation

An intermediary process should reconcile three levels:

```text
Verified omnibus or custody position
= eligible customer balances
+ excluded or unsupported balances
+ pending and exception balances
```

For a distribution:

```text
Aggregate amount received
= customer amounts completed
+ pending customer amounts
+ returned or unclaimed amount
+/- corrections
```

The custodian and FUZE should agree on identifiers, periods, precision, and exception ownership. Aggregate on-chain movement is insufficient evidence of customer-level completion.

---

## 12. Eligibility Status

Custody-related statuses can include:

| Status | Meaning |
|---|---|
| Directly supported | Address-level proof and interaction are supported |
| Evidence review | Account or beneficial-position evidence is under review |
| Custodian supported | Approved intermediary process exists |
| Withdrawal required | Self-custody is required before the cutoff |
| Pending transfer | Deposit or withdrawal prevents final classification |
| Unsupported custody | Required records or interaction are unavailable |
| Restricted | Jurisdiction, account, lock, or policy condition prevents access |
| Disputed | Ownership, balance, cutoff, or duplicate issue remains open |

Status should be process-specific. An exchange can support trading but remain unsupported for a particular snapshot or claim.

---

## 13. OTC and Private Transfers

An OTC transaction transfers FUZE under a private settlement, but related statuses may remain with the original record.

Review can include:

- source and destination transaction;
- trade or agreement time;
- beneficial ownership;
- lock or vesting;
- snapshot cutoff;
- prior claim or migration status;
- jurisdiction and verification;
- duplicate or related-party concerns.

The recipient's token balance is evidence of current ownership, not proof that historical eligibility, investor terms, contribution rights, or claim status transferred.

---

## 14. Contract and Protocol Custody

Tokens in staking, liquidity, bridge, lending, vault, or other protocol contracts can be represented by:

- receipt tokens;
- pool shares;
- internal accounting;
- claimable balances;
- underlying contract state.

The method should define which representation controls, how underlying FUZE is calculated, and how duplicate counting is prevented.

Technical compatibility also matters. A contract can hold an eligible economic position while being unable to sign or call the claim interface directly.

---

## 15. Privacy and Data Sharing

Custody records can contain identity, account balances, transaction history, jurisdiction, tax information, and verification data.

FUZE and any cooperating custodian should define:

- minimum fields;
- purpose and authority;
- secure transfer;
- permitted reviewers;
- retention and deletion;
- correction;
- incident responsibilities;
- public aggregation.

Public reporting should keep beneficial-owner identity and exchange account records private.

The broader data model is defined in [FUZE Wallet-Based Privacy and Eligibility](26-FUZE_WALLET_BASED_PRIVACY_AND_ELIGIBILITY_PUBLIC.md).

---

## 16. Custody Incidents

Relevant incidents include:

- exchange suspension or insolvency concern;
- compromised account or wallet;
- incorrect customer allocation;
- delayed or failed withdrawal;
- missing or corrupted custody records;
- chain or network mismatch;
- duplicate claim;
- unauthorized data disclosure;
- frozen account or legal restriction.

The response should preserve records, pause affected processing, identify balances and users, coordinate with the custodian, communicate status, and document recovery or correction.

An exchange incident can affect support even when the FUZE contract and self-custody process remain healthy.

---

## 17. Disputes and Corrections

A custody dispute can concern:

- beneficial ownership;
- eligible balance;
- trade or transfer timing;
- account authenticity;
- omnibus allocation;
- duplicate records;
- supported jurisdiction;
- completed distribution.

The case should preserve original records, active method, new evidence, reviewer decision, corrected amount or status, approval, and downstream report effect.

Corrections should update both customer-level and aggregate reconciliation where applicable.

---

## 18. Public Reporting

Public custody reporting can include:

- supported custody modes;
- participating exchange or custodian where authorized;
- snapshot and cutoff method;
- aggregate self-custody and intermediary amounts;
- eligible, pending, unsupported, disputed, and completed categories;
- claim model;
- reconciliation status;
- incidents, pauses, and corrections at an appropriate level.

Public wallet labels should identify exchange, custodian, treasury, contract, or program function without identifying individual customers.

---

## 19. Boundaries

Exchange listing, trading support, token custody, snapshot support, and participation support are separate capabilities.

FUZE can define its active rules and direct processes, but third-party custodians control their own accounts, systems, timing, customer records, and cooperation.

Detailed custody and participation risks are maintained in [FUZE Token Risk Boundaries](29-FUZE_TOKEN_RISK_BOUNDARIES_PUBLIC.md).

---

## Conclusion

Custody determines which wallet records FUZE can verify and which party can act.

Direct self-custody, evidence-supported accounts, custodian-assisted claims, omnibus distribution, and unsupported custody each require explicit rules. Cutoff discipline, user-level evidence, aggregate reconciliation, privacy controls, incident handling, and accurate public status prevent exchange-held balances from being mistaken for direct wallet records.
