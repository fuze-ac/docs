# FUZE Public Vault Visibility System

## Executive Summary

The FUZE Public Vault Visibility System is the public information layer for approved vault, reserve, allocation, and token-movement records. It gives readers a structured way to see what a published record represents, when it was measured, which methodology applies, and where supporting evidence can be inspected.

Visibility is contextual rather than absolute. A wallet address or balance alone cannot explain purpose, restrictions, commitments, custody, release status, or circulation treatment. FUZE therefore pairs approved identifiers with functional labels, status fields, timestamps, evidence references, and correction history.

The system publishes operational meaning while protecting personal identity, credentials, private agreements, customer information, and security-sensitive details. Public visibility creates an inspection surface; it creates no authority over a vault and no automatic access to its assets.

Vault establishment and administration are defined in the [FUZE Vault and Reserve Policy](14-FUZE_VAULT_AND_RESERVE_POLICY_PUBLIC.md). This paper focuses only on publication and interpretation.

---

## 1. Visibility Objective

The system should help a reader answer:

1. Which vault, wallet, contract, account, or registry is shown?
2. What function and asset class does it represent?
3. What balance or event is being reported?
4. Which restrictions or commitments affect interpretation?
5. How current is the record?
6. What evidence and methodology support it?
7. Has the record been corrected or superseded?

The objective is public reviewability. Published data should be understandable without exposing the private operating layer behind it.

---

## 2. Visibility and Access

Visibility and access are different system states.

| Visibility | Access |
|---|---|
| Shows approved information about a structure | Allows an eligible party to participate in an approved process |
| Can exist for inactive or restricted assets | Requires an active route and current authorization |
| Uses labels, balances, statuses, and evidence | Uses eligibility, limits, timing, pricing, claim, or release controls |
| Supports inspection | Supports a controlled action |

A visible community, migration, treasury, reserve, vesting, or liquidity-related vault remains governed by its own mandate. Any public access process is addressed in [FUZE Public Vault Access Windows](17-FUZE_PUBLIC_VAULT_ACCESS_WINDOWS_PUBLIC.md).

---

## 3. Publication Classes

Each record should be assigned a publication class.

### Public

Suitable for unrestricted publication. Examples can include an approved functional label, public contract address, aggregate balance, report timestamp, or governance reference.

### Public summary

Published at an aggregate or categorized level. This class is useful when details contain personal, commercial, custody, or security information.

### Permissioned

Available only to authorized reviewers, counterparties, auditors, service providers, or operators. Permissioned records can support a public summary without becoming public themselves.

### Restricted

Limited to essential roles because the material includes credentials, key-management information, investigation details, protected identity, or another sensitive control.

Publication class applies to each field, not only to the whole vault. An address can be public while signer identity and operating procedures remain restricted.

---

## 4. Record Types

The visibility system can publish several record types.

| Record type | Public purpose |
|---|---|
| Vault profile | Explains a structure's function, asset class, authority model, and status |
| Balance snapshot | Shows a measured balance at a stated time or block |
| Movement event | Describes an inflow, outflow, return, claim, deployment, or reclassification |
| Allocation summary | Reconciles balances and movement to an approved token category |
| Reserve summary | Shows designated, committed, used, and remaining reserve capacity |
| Restriction status | Summarizes lock, vesting, claim, custody, program, or policy conditions |
| Governance event | Links an approved proposal, decision, timelock, or multisignature action |
| Evidence reference | Points to a transaction, contract, report hash, attestation, or review record |
| Methodology notice | Defines calculation, inclusion, exclusion, and classification rules |
| Correction notice | Preserves a prior value and explains the revised record |

Different record types can appear together on one vault page, but each should retain its own timestamp and source.

---

## 5. Vault Profile

An approved vault profile should contain enough context to prevent address-only interpretation.

| Field | Description |
|---|---|
| Public identifier | Stable vault name or registry identifier |
| Functional label | Treasury, reserve, community, migration, team, partner, market operation, or other approved role |
| Asset class | FUZE token, stablecoin, fiat-equivalent account, evidence registry, or another supported class |
| Network or system | Chain, custodian, account system, or internal registry |
| Address or reference | Public identifier where approved |
| Controlling mandate | Allocation, reserve, treasury, program, or reporting purpose |
| Status | Proposed, active, paused, closing, closed, replaced, or archived |
| Authority summary | Public-safe description of contract, custodian, multisignature, or role controls |
| Methodology version | Rules used for balance and state interpretation |
| Last reviewed | Time of the latest ownership and classification review |

When an address is replaced, both profiles should show the relationship and effective time. Historical identifiers remain useful for interpreting prior transactions.

---

## 6. Labels

Labels should describe function and current status.

Good labels are:

- specific enough to distinguish allocation or operating purpose;
- stable across reports;
- mapped to an authoritative internal record;
- updated when function or control changes;
- independent of a private person's name.

A label such as `Treasury Reserve - Primary Custody` conveys more than `Wallet 1`. A label should still avoid implying availability, ownership rights, or circulating status unless those fields have separate support.

Abbreviated dashboard labels should map back to the approved category or vault name. The controlling allocation names remain in the [FUZE Token Allocation Table](02-FUZE_TOKEN_ALLOCATION_TABLE_PUBLIC.md).

---

## 7. Balance Presentation

Every displayed balance should include:

- unit and asset;
- network or source system;
- timestamp and timezone;
- block number or data cutoff where applicable;
- balance type;
- methodology version;
- freshness status.

### Balance types

| Type | Interpretation |
|---|---|
| Custodied | Held at the identified address, account, contract, or custodian |
| Allocated | Assigned to an approved token purpose |
| Reserved | Retained for a stated future use |
| Committed | Connected to an approved obligation or program |
| Claimable | Available through an active claim process for eligible recipients |
| Deployed | Placed into an approved operating mechanism |
| Circulating | Classified under the published circulation methodology |

These types can overlap unless the display explicitly uses mutually exclusive buckets. The interface should say whether a field is a state bucket, attribute, period flow, or point-in-time balance.

FUZE token quantities, stablecoin amounts, accounting values, and Platform Credit usage records should use separate units and visual treatment.

---

## 8. Event Presentation

A public movement event should identify:

1. event identifier and time;
2. source and destination labels;
3. asset and amount;
4. event class;
5. allocation or mandate;
6. prior and resulting status;
7. transaction or custody reference;
8. approval or governance reference where public;
9. report effect.

Event classes can include deposit, custody transfer, release, vest, claim, deployment, return, burn, bridge, reclassification, and correction.

The interface should describe the event rather than rely on raw transaction direction. A transfer out of one address can remain within controlled custody, while a transfer into a contract can represent deployment rather than unrestricted circulation.

---

## 9. Evidence and Provenance

Each material public figure should point to an evidence chain appropriate to its source.

### On-chain evidence

Can include network, contract, transaction hash, block, event log, and verified address label.

### Custodian evidence

Can include a public-safe statement reference, attestation, account identifier, reporting period, and reconciliation status.

### Internal ledger evidence

Can include report identifier, methodology, review time, source-system cutoff, and an approved hash of the underlying record.

### Governance evidence

Can include proposal, vote, approval, multisignature transaction, timelock operation, or policy reference.

A hash can demonstrate that a record existed in a particular form. Its meaning depends on access to the source material and the process that produced it.

---

## 10. Freshness and Status

Readers should be able to tell whether data is current enough for its purpose.

| Freshness state | Meaning |
|---|---|
| Live | Updated directly from a supported source with current health checks |
| Recent | Updated within the published normal reporting interval |
| Delayed | Source or review timing is outside the normal interval |
| Pending reconciliation | New data exists but review is incomplete |
| Stale | The record exceeds the stated freshness threshold |
| Archived | Preserved for history after replacement or closure |

The public surface should show the last successful source update and the last review separately. Automated collection can be current while human classification remains pending.

Source outages, chain reorganization, custodian delays, and reconciliation exceptions should produce an explicit status instead of silently displaying an old value as current.

---

## 11. Privacy and Identity

Wallet-level transparency should identify purpose, not the natural person behind an address.

Public records can show:

- functional wallet or vault labels;
- aggregate participant or recipient classes;
- token and status totals;
- public transactions and contracts;
- approved governance and methodology references.

Permissioned or restricted treatment applies to:

- customer, employee, investor, contributor, or claimant identity;
- account credentials and recovery material;
- private compensation and commercial terms;
- verification documents and support evidence;
- security architecture and incident details.

Where self-custody evidence is needed, FUZE can retain the verification result while publishing an aggregate status. Exchange or institutional custody can likewise be reported by category without exposing a customer's account.

---

## 12. Interface Structure

A public vault page can use four layers.

### Summary

Shows label, purpose, asset, status, balance, timestamp, and a concise interpretation.

### State detail

Shows allocation, reserve, restriction, commitment, release, deployment, and circulation fields relevant to the structure.

### Activity

Shows material events with filters for period, class, and status.

### Evidence and history

Shows methodology, transaction references, governance references, report hashes, corrections, and prior profile versions.

The summary should remain readable for a first-time visitor. Detailed fields should be available without forcing every reader through raw transaction data.

---

## 13. Quality Controls

Before publication, the reporting owner should verify:

- the identifier maps to the intended structure;
- the label matches the approved mandate;
- units and timestamps are explicit;
- balance and flow fields are separated;
- source data reconciles to the reported figure;
- links and evidence references resolve;
- privacy classification has been applied;
- superseded records are visibly marked.

Automated validation can detect stale data, broken references, missing fields, arithmetic differences, duplicate events, and unexpected asset types. Material interpretation still requires an accountable reviewer.

---

## 14. Corrections

Corrections should preserve history.

A correction notice should show:

| Field | Content |
|---|---|
| Affected record | Vault, report, event, field, and period |
| Prior value | Previously published information |
| Revised value | Corrected information |
| Reason | Source error, classification issue, timing difference, or methodology change |
| Effective time | When the correction applies |
| Downstream effect | Other reports, totals, or dashboards affected |
| Review status | Owner and approval state |

A methodology change should be distinguished from a data error. Historical reports can remain available when clearly marked as superseded.

---

## 15. Availability and Continuity

The public interface should degrade clearly when a source is unavailable.

Continuity measures can include:

- cached last-known values with a visible timestamp;
- independent source health indicators;
- queued event processing;
- manual publication of a reviewed snapshot;
- archived reports and downloadable records;
- incident notices for material interruptions.

Public data should retain provenance across interface migrations. A new dashboard or API should preserve identifiers, methodology versions, and historical correction links.

---

## 16. Boundaries

The visibility system reports approved information; it does not operate the underlying vault. A displayed balance creates neither participant eligibility nor a release instruction.

Public fields can lag final custody or accounting records during reconciliation. Each page should therefore show its source, cutoff, and review status.

Supply and circulation terminology follows [FUZE Token Release and Circulation Clarity](13-FUZE_TOKEN_RELEASE_AND_CIRCULATION_CLARITY_PUBLIC.md). Consolidated risk treatment remains in [FUZE Token Risk Boundaries](29-FUZE_TOKEN_RISK_BOUNDARIES_PUBLIC.md).

---

## Conclusion

FUZE Public Vault Visibility turns isolated addresses and balances into records that can be interpreted.

Functional labels, explicit units, state definitions, timestamps, evidence, freshness indicators, privacy tiers, and correction history give readers a useful inspection surface. The system can increase transparency while keeping access authority and personal identity outside the public display.
