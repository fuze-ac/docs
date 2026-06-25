# FUZE Exchange Custody and Wallet Participation

## Executive Summary

Holding FUZE through an exchange or institutional custodian is operationally different from holding it in a self-custody wallet. In self-custody, the holder can usually prove control of a specific address and interact directly with an approved wallet-based process. In exchange or omnibus custody, the custodian controls the on-chain address while individual customer balances exist in a private internal ledger.

This distinction matters whenever a FUZE process uses wallet signatures, snapshots, eligibility checks, contract interactions, migrations, claims, or other activation-gated participation. An exchange listing, deposit service, withdrawal service, or custody relationship does not by itself establish support for any such process.

This paper defines the public framework for classifying custody, determining which evidence may be required, handling exchange-held balances, protecting customer identity, and communicating supported and unsupported routes. It describes an operating policy, not evidence that any exchange, custodian, claim process, or wallet-based participation mechanism is currently active.

## 1. Purpose and Primary Readers

This paper is written primarily for FUZE holders, exchanges, custodians, and operators who need to understand how custody affects wallet-based processes.

It answers five practical questions:

1. Who controls the on-chain wallet?
2. Who holds the beneficial account balance?
3. Which evidence can connect the beneficial holder to the custody record?
4. Can the holder interact directly with the applicable FUZE process?
5. What happens when the custodian cannot support the required evidence or action?

The objective is consistent treatment across self-custody, exchange custody, institutional custody, omnibus accounts, smart-contract wallets, and other controlled structures.

## 2. Current Public Position

FUZE may use wallet-level records for eligibility, access, reporting, governance direction, or other ecosystem participation where a specific framework has been approved and activated.

At the public-documentation level, this paper defines the custody treatment that such a framework could apply. It does not establish that:

- a FUZE token contract is deployed or activated;
- a snapshot or claim window is open;
- an exchange or custodian supports FUZE participation;
- exchange-held balances are eligible for a specific process;
- a listing, liquidity venue, or withdrawal route is available;
- token holding alone creates a payment, distribution, or participation right.

Any active process must publish its own dated rules, supported networks, custody modes, evidence requirements, cutoffs, privacy treatment, and support route.

## 3. Why Custody Changes the Evidence

A blockchain address proves where tokens are recorded on-chain. It does not always identify the person or entity with the economic interest in those tokens.

With self-custody, the user normally controls the private signing authority and can demonstrate control through a wallet signature. With exchange or omnibus custody:

- the exchange or custodian controls the address;
- one address may represent many customers;
- customer balances are maintained in an internal ledger;
- internal trades may not create on-chain transfers;
- deposit and withdrawal timing may differ from trade timing;
- the customer may be unable to sign from the custody address;
- public chain data cannot allocate the omnibus balance among customers.

For that reason, on-chain balance, wallet control, beneficial ownership, account eligibility, and direct interaction must remain separate concepts.

## 4. Custody Categories

| Custody category | Control and record model | Typical participation implication |
|---|---|---|
| Self-custody wallet | User controls the address and signing authority | Can support direct address proof where the active rules permit it |
| User multisignature | A defined signer group controls the wallet | Requires compatible signing and authority evidence |
| Smart-contract wallet | Contract code and authorized signers control execution | Requires technical compatibility with the active process |
| Exchange custody | Exchange controls wallets and records customer balances internally | Usually requires withdrawal or exchange-supported evidence |
| Omnibus custody | One or more addresses represent many beneficial accounts | Requires user-level allocation and aggregate reconciliation |
| Institutional custody | Regulated or professional custodian acts for clients | Requires custodian records, authority, and process support |
| Protocol custody | Tokens are held in staking, liquidity, bridge, vault, or other contracts | Requires a defined method for the underlying position |
| Vesting custody | Tokens remain subject to a vesting contract or grant record | Requires treatment of locks, release conditions, and ownership |
| Treasury or program custody | FUZE or an approved operator controls assets for a defined purpose | Must remain separate from ordinary participant balances |

An active FUZE process should state which categories it supports rather than leaving users to infer support from token visibility alone.

## 5. Supported Custody Modes

A specific FUZE process may use one or more of the following modes.

### 5.1 Direct self-custody

The participant uses a supported wallet, provides the required address-level evidence, and interacts directly with the approved process.

### 5.2 Withdrawal before cutoff

A customer moves FUZE from an exchange or custodian to a supported self-custody wallet before the published registration, snapshot, or action cutoff.

### 5.3 Evidence-supported custody account

The customer provides approved exchange or custodian evidence showing the beneficial balance under the active method. Review remains subject to authenticity, timing, jurisdiction, duplicate, and privacy controls.

### 5.4 Custodian-assisted participation

The custodian supplies approved user-level records, supports verification, submits an aggregate position, facilitates direct delivery, or performs an internal allocation under a documented arrangement.

### 5.5 Authorized omnibus representation

The custodian or another approved representative acts for an omnibus position and remains responsible for the underlying customer allocation, reconciliation, communication, and exception handling.

### 5.6 Unsupported custody

A custody route is unsupported when the process lacks sufficient evidence, cooperation, technical compatibility, jurisdiction coverage, data protection, or reconciliation capability.

A custody provider can be supported for one FUZE process and unsupported for another.

## 6. Process-Specific Support Record

Before publicly describing an exchange or custodian as supported, the applicable record should define:

| Record field | Required treatment |
|---|---|
| Process scope | Exact snapshot, migration, eligibility, claim, access, or reporting process |
| Venue and network | Custodian, exchange, chain, contract, and address model |
| Custody structure | Individual, omnibus, institutional, protocol, or another approved category |
| Evidence method | Statement, authenticated record, signed confirmation, API record, or allocation file |
| Controlling cutoff | Block number, timestamp, ledger time, trade time, deposit time, or withdrawal time |
| Customer coverage | Supported account types, locations, and restrictions |
| Interaction model | Direct wallet, reviewed destination, aggregate action, or internal allocation |
| Reconciliation | On-chain position, custodian ledger, customer balances, and exceptions |
| Data treatment | Minimum fields, secure transfer, reviewers, retention, and deletion |
| Support ownership | Customer communication, disputes, corrections, and incident response |
| Approval status | Owner, reviewer, effective date, and current status |

Support should not be announced before the cooperation and operating record is approved.

## 7. Snapshot and Cutoff Rules

Custody systems can produce several different times:

- blockchain block time;
- exchange trade time;
- internal ledger cutoff;
- deposit credit time;
- withdrawal debit time;
- on-chain withdrawal completion time;
- account-statement generation time.

An active process must select the controlling event and explain how pending transfers are treated.

For example, a withdrawal requested before a snapshot but completed afterward can appear as an internal account debit while the tokens remain inside the exchange's on-chain balance at the snapshot block. Without a reconciliation rule, the position could be counted twice or omitted.

Cutoffs should therefore use an explicit block number or a timestamp with timezone, together with documented treatment for pending deposits, pending withdrawals, internal transfers, reversals, and corrections.

## 8. Evidence for Exchange-Held Balances

Depending on the active process, acceptable evidence may include:

- an official account statement;
- authenticated balance history;
- trade history relevant to the cutoff;
- deposit or withdrawal records;
- an exchange-signed or custodian-signed confirmation;
- an authenticated API record;
- a custodian allocation file;
- an approved account identifier and ownership result;
- later proof of withdrawal to a supported self-custody wallet.

Screenshots alone may omit context or be altered. Where they are accepted as supporting material, the process should define the required fields, period, authenticity checks, and additional corroboration.

Customer evidence must remain permissioned. Public reporting may use aggregate custody categories, counts, balances, status totals, hashes, or methodology without publishing customer identity or account records.

## 9. Self-Custody Proof

A direct self-custody route may require:

1. a supported network and verified FUZE contract reference;
2. wallet connection or address submission;
3. a unique signed message;
4. a balance or snapshot check;
5. wallet-category and duplicate review;
6. jurisdiction or private verification where required;
7. destination and contract compatibility;
8. a final process-specific status.

A signed message should identify the FUZE domain or process, purpose, network, nonce, and expiration. This reduces replay and phishing risk while demonstrating address control.

A signature proves control of the relevant address at the verification time. It does not by itself prove beneficial ownership, legal identity, jurisdiction, eligibility, or activation of a participation right.

## 10. Deposits, Withdrawals, and Internal Transfers

An active custody method should state how it treats:

- the latest withdrawal time for self-custody treatment;
- deposits not yet credited internally;
- withdrawals not yet completed on-chain;
- internal exchange transfers;
- subaccounts and institutional accounts;
- withdrawal fees and the resulting net quantity;
- wrong-network or unsupported-contract cases;
- frozen, restricted, or disputed accounts;
- replacement destination wallets;
- exchange maintenance or withdrawal suspension.

Users should receive enough notice to account for third-party processing time. FUZE cannot control an exchange's maintenance, fees, account restrictions, processing speed, internal records, or withdrawal availability.

## 11. Interaction and Delivery Models

Where an approved process requires an action or delivery, the operating model may be one of the following.

### Direct wallet interaction

A supported self-custody or compatible contract wallet completes the action directly.

### Reviewed destination model

A custody customer submits approved account evidence and, after review, provides a supported destination wallet for the applicable process.

### Custodian aggregate model

The custodian acts for an approved aggregate position and performs customer-level allocation through its own controlled ledger.

### Custodian attest-and-direct model

The custodian confirms approved user-level amounts while eligible customers use verified destination wallets directly.

### Controlled manual model

An authorized operator processes approved user-level records where direct contract interaction is unsuitable, subject to permission, approval, reconciliation, and audit controls.

Each model should identify responsibility for custody, data, fees, corrections, disputes, uncompleted actions, customer support, and final reconciliation.

## 12. Omnibus Reconciliation

An omnibus process should reconcile the on-chain or custody position to the underlying customer ledger.

    Verified omnibus position
    = eligible customer balances
    + excluded or unsupported balances
    + pending and exception balances

Where an aggregate amount is processed:

    Aggregate amount processed
    = completed customer amounts
    + pending customer amounts
    + returned or uncompleted amounts
    +/- approved corrections

The custodian and FUZE should agree on identifiers, precision, timing, exception ownership, and completion evidence. An aggregate on-chain movement does not prove completion for each underlying customer.

## 13. Process Statuses

| Status | Meaning |
|---|---|
| Directly supported | The process supports address-level proof and direct interaction |
| Evidence review | Custody or beneficial-position evidence remains under review |
| Custodian supported | An approved intermediary process exists for the stated scope |
| Withdrawal required | The user must move to supported self-custody before the cutoff |
| Pending transfer | A deposit, withdrawal, or internal movement prevents final classification |
| Unsupported custody | Required records, cooperation, or interaction are unavailable |
| Restricted | A jurisdiction, account, lock, legal, or process condition prevents access |
| Disputed | Ownership, balance, timing, allocation, or duplicate treatment remains unresolved |
| Paused | Processing is temporarily suspended while an issue is reviewed |
| Corrected | A previous custody decision has been superseded by an approved correction |

These statuses are process-specific and time-sensitive. Trading support does not establish snapshot, migration, claim, governance, or participation support.

## 14. Transfers, Private Transactions, and Historical Status

Receiving FUZE through a private or off-market transaction can establish a current token position where the transfer is valid. It does not automatically transfer every historical or contractual status connected to the seller.

A review may need to consider:

- source and destination transactions;
- transfer or agreement time;
- beneficial ownership;
- lock or vesting conditions;
- snapshot rules;
- prior migration or claim status;
- duplicate treatment;
- jurisdiction and required verification;
- private rights that do not travel with the token.

A current wallet balance is therefore not proof that an earlier snapshot position, private agreement, contribution status, or completed action also transferred.

## 15. Smart-Contract and Protocol Custody

FUZE held in staking, liquidity, bridge, lending, vault, multisignature, or other contract structures may be represented through:

- receipt tokens;
- pool shares;
- internal accounting;
- claimable balances;
- underlying contract state;
- signer or role authority.

The active process should define which representation controls, how underlying FUZE is calculated, how duplicate counting is prevented, and whether the contract can perform the required signature or transaction.

A contract can represent an economic position while remaining technically unable to interact with a particular wallet interface or claim contract.

## 16. Privacy and Identity Protection

Custody evidence can contain personal identity, account identifiers, balances, transaction history, jurisdiction, tax information, verification results, and support records.

FUZE and any cooperating custodian should define:

- the minimum required fields;
- the purpose and authority for collection;
- secure transfer and storage;
- permitted reviewers;
- access logging;
- retention and deletion;
- correction and dispute handling;
- incident responsibilities;
- approved public aggregation.

Public wallet labels may identify a function such as exchange, custodian, treasury, contract, or program where approved. They should not expose the identity of individual customers or publish wallet-to-person mappings.

The broader privacy and eligibility model is defined in [FUZE Wallet-Based Privacy and Eligibility](26-FUZE_WALLET_BASED_PRIVACY_AND_ELIGIBILITY_PUBLIC.md).

## 17. Incidents, Pauses, and Corrections

Custody-related incidents may include:

- exchange suspension or insolvency concern;
- compromised account or wallet;
- incorrect customer allocation;
- delayed or failed withdrawal;
- missing or corrupted records;
- unsupported network or contract use;
- duplicate processing;
- unauthorized data disclosure;
- frozen account or legal restriction.

The response should preserve records, pause affected processing where necessary, identify impacted balances and accounts, coordinate with the custodian, communicate the public-safe status, and document recovery or correction.

A correction should update both the customer-level record and aggregate reconciliation where applicable while preserving the earlier decision and its reason.

## 18. Public Reporting

Where a custody-supported process is active, public reporting may include:

- supported custody modes;
- authorized participating custodians or exchanges;
- applicable network, snapshot, and cutoff method;
- aggregate self-custody and intermediary categories;
- directly supported, pending, restricted, unsupported, disputed, and completed totals;
- interaction or delivery model;
- reconciliation status;
- public-safe incident, pause, and correction notices;
- report hashes or methodology references.

Publication should remain proportional to the public purpose. Identity, contact details, account statements, jurisdiction evidence, private agreements, and customer-level custody records remain permissioned or restricted.

## 19. Market-Access and Participation Boundary

Exchange listing, trading support, custody support, deposits, withdrawals, liquidity, snapshots, claims, and wallet-based participation are separate capabilities.

FUZE's public market-access direction is DEX-first, subject to readiness, approval, deployment, liquidity, legal, operational, and disclosure requirements. Possible later CEX access must move through distinct preparation, application, review, approval, and live-access stages. None of those stages should be inferred from this custody framework.

FUZE can define the rules for its own approved processes, but third-party venues control their own accounts, customer ledgers, timing, fees, restrictions, technical support, and cooperation.

Detailed token and custody-related risks are maintained in [FUZE Token Risk Boundaries](29-FUZE_TOKEN_RISK_BOUNDARIES_PUBLIC.md). Market-access treatment is maintained in [FUZE Liquidity and Listing Policy](21-FUZE_LIQUIDITY_AND_LISTING_POLICY_PUBLIC.md).

## Key Takeaways

- Self-custody and exchange custody produce different evidence and interaction capabilities.
- An exchange address can represent many beneficial holders and cannot establish customer-level balances by itself.
- Every active FUZE process must publish its own supported custody modes, evidence requirements, cutoffs, privacy treatment, and status.
- Listing, trading, custody, withdrawal, snapshot, and participation support are separate capabilities.
- Exchange-held balances may require withdrawal, approved account evidence, custodian cooperation, or an unsupported classification.
- Customer identity and account records remain permissioned even when aggregate wallet or custody reporting is public.
- This paper defines a controlled framework and does not establish that any exchange-supported participation process is currently active.
