# FUZE Vault and Reserve Policy

## Executive Summary

FUZE uses vaults to place assets and records under a defined purpose, control model, and reporting treatment. It uses reserves to designate resources for future obligations, continuity, risk response, or approved strategic needs.

This paper establishes the policy applied before a vault or reserve becomes operational. It covers classification, ownership, authorization, custody, segregation, reconciliation, review, incident handling, public reporting, and closure.

A vault balance is meaningful only with its purpose and status. A reserve designation is meaningful only with its intended use, approval conditions, and review record. These controls help FUZE distinguish custody from availability and planned use from completed deployment.

Allocation-specific release conditions are maintained in the [FUZE Vault-by-Vault Release Rules](15-FUZE_VAULT_BY_VAULT_RELEASE_RULES_PUBLIC.md). Public display and access-window mechanics remain in their dedicated papers.

---

## 1. Policy Objective

The policy gives FUZE a consistent method for answering five questions:

1. Why does this vault or reserve exist?
2. What asset, allocation, or record belongs within it?
3. Who can propose, approve, execute, and review activity?
4. How are balances and movements reconciled?
5. What information can be reported publicly?

The objective is controlled stewardship. Each structure should have enough documentation for an authorized reviewer to understand its mandate, current state, responsible roles, and evidence trail.

---

## 2. Scope

This policy applies to purpose-specific structures used to hold or track:

- FUZE token allocations;
- stablecoin and treasury assets;
- operational or contingency reserves;
- approved program balances;
- custody and transaction evidence;
- public reporting references.

The word **vault** describes a controlled wallet, contract, account, sub-account, or ledger structure. The word **reserve** describes an approved designation of resources for a future purpose. A reserve may sit inside a vault, but the terms describe different attributes.

Platform Credit ledgers remain product-usage systems. They may use account controls and reconciliation procedures, but they are outside FUZE token vault balances.

---

## 3. Control Principles

### Purpose before movement

Every vault requires a documented mandate before funding or use. The mandate identifies the asset class, source, intended activity, restrictions, approval path, reporting category, and end condition.

### Segregation by meaning

Assets with materially different purposes should use separate wallets, contracts, accounts, or reliable sub-ledgers. Segregation should make allocation, ownership, restriction, and reporting differences reviewable.

### Least necessary authority

Access is assigned according to role. Proposal, approval, execution, reconciliation, and review responsibilities should be separated where the operating model permits.

### Evidence-linked activity

Each material movement should connect to an instruction, approval, transaction record, accounting entry, and resulting classification. The evidence should support reconstruction of the event.

### Reversible administration

Administrative mistakes should have a defined correction route. Emergency controls may pause activity, replace authority, quarantine a destination, or require enhanced review.

### Public-safe transparency

Public reporting should explain function and status while keeping personal identity, credentials, security procedures, negotiations, and confidential records private.

---

## 4. Vault Classification

FUZE can classify a vault by both asset and function.

| Classification | Primary function | Required context |
|---|---|---|
| Allocation vault | Custodies FUZE assigned to an approved allocation | Allocation name, mandate, balance, restriction, and release authority |
| Treasury vault | Holds assets available for approved treasury operations | Asset type, treasury purpose, approval class, and reconciliation owner |
| Reserve vault | Protects resources designated for a future need | Reserve purpose, utilization trigger, review date, and release authority |
| Program vault | Supports a defined product, community, partner, incentive, or migration program | Program owner, eligibility or milestone basis, budget, and end condition |
| Operational vault | Supports execution such as settlement, compensation, or controlled market operations | Counterparty or venue class, transaction limits, and operating controls |
| Recovery vault | Receives returned, quarantined, disputed, or corrected assets | Source event, custody status, investigation owner, and final disposition |
| Evidence registry | Stores hashes, identifiers, labels, or references rather than economic assets | Source system, publication scope, retention, and correction method |

A vault can have more than one operational attribute, but its controlling classification should remain clear. Where mixed use is unavoidable, the owner must maintain a sub-ledger that preserves the same distinctions.

---

## 5. Reserve Classification

A reserve should be described by the event or obligation it is intended to address.

### Continuity reserve

Protects product, infrastructure, security, staffing, or essential operating continuity.

### Obligation reserve

Supports a recorded obligation such as tax, refund, chargeback, vendor settlement, or approved compensation.

### Program reserve

Sets aside capacity for an approved ecosystem, partner, community, migration, or incentive program before deployment.

### Strategic reserve

Preserves resources for a future initiative that requires treasury or governance approval at the time of use.

### Stability reserve

Supports an exceptional response to a documented security, operational, reporting, or ecosystem-stability event.

A reserve label does not itself authorize spending or token release. Utilization follows the applicable approval, custody, accounting, and reporting route.

---

## 6. Establishment Record

Before activation, the responsible owner prepares a vault or reserve record containing:

| Field | Required content |
|---|---|
| Identifier | Unique internal name and public label where approved |
| Classification | Vault type, reserve type, asset class, and reporting category |
| Mandate | Purpose, permitted uses, exclusions, and end condition |
| Source | Allocation, treasury source, program budget, return, or transfer origin |
| Authority | Proposer, approver, executor, reconciler, reviewer, and emergency role |
| Custody | Wallet, contract, custodian, account, or ledger arrangement |
| Controls | Signer threshold, timelock, limits, allowlists, review gates, or equivalent safeguards |
| Evidence | Approval references, transaction identifiers, agreements, and supporting records |
| Reporting | Internal cadence, public fields, confidentiality class, and methodology |
| Lifecycle | Activation date, review schedule, suspension triggers, and closure route |

The record should be approved before the structure receives material assets. Technical setup can occur earlier for testing when test assets and production authority remain clearly separated.

---

## 7. Custody and Access

Custody design should reflect the value, purpose, transaction frequency, and risk of the vault.

Possible arrangements include:

- multisignature wallets;
- timelocked contracts;
- role-controlled smart contracts;
- institutional or exchange custody;
- treasury bank or payment accounts;
- internal ledgers tied to external custody evidence.

The selected arrangement should identify who can:

- initiate an instruction;
- approve it;
- execute or sign;
- inspect balances and records;
- reconcile the result;
- invoke emergency controls.

Self-custody and third-party custody require different evidence. Self-custody records should document authorized control and signer changes. Third-party custody records should document account ownership, permissions, statements, transfers, and material service constraints.

Credentials, recovery materials, private keys, and detailed security procedures remain restricted.

---

## 8. Segregation Rules

Segregation is based on economic and reporting meaning rather than convenience.

FUZE should separate:

- distinct token allocations where their mandates or release rules differ;
- FUZE token custody from stablecoin treasury balances;
- operating assets from protected reserves;
- participant or program inventory from treasury inventory;
- returned or disputed assets from active program balances;
- test environments from production custody.

Commingling requires an approved exception and a reliable method to identify each beneficial purpose. The exception record should explain why physical separation is impractical, how the sub-ledger works, and how reviewers can reconcile it.

The controlling token allocation amounts and percentages remain in the [FUZE Token Allocation Table](02-FUZE_TOKEN_ALLOCATION_TABLE_PUBLIC.md). This policy governs how related custody and reserve structures are administered.

---

## 9. Funding and Movement Controls

### Initial funding

The first transfer should verify the destination, asset, network, amount, authority, and expected classification. A small validation transfer may precede a material movement when operationally appropriate.

### Internal transfer

Movement between controlled structures should identify both source and destination mandates. Continued FUZE control can leave circulation unchanged even though custody changes.

### External deployment

Movement to a recipient, contract, custodian, partner, program, or venue requires the approval and evidence specified for that activity. The resulting status should be recorded after execution.

### Return

Unused, cancelled, recovered, or excess assets should return to the source structure or an approved recovery vault. Their next use requires a new instruction.

### Reclassification

A mandate change requires approval at least as strong as the original establishment decision. The record should preserve the former classification, effective time, reason, and resulting reporting treatment.

The [FUZE Controlled Circulation Policy](12-FUZE_CONTROLLED_CIRCULATION_POLICY_PUBLIC.md) governs movement discipline. The [FUZE Token Release and Circulation Clarity](13-FUZE_TOKEN_RELEASE_AND_CIRCULATION_CLARITY_PUBLIC.md) paper provides the state vocabulary used in reports.

---

## 10. Reserve Utilization

A reserve-use request should state:

1. the reserve and current balance;
2. the event, obligation, or program being addressed;
3. the requested amount and destination;
4. the basis for timing and sizing;
5. the approving authority;
6. the expected remaining reserve;
7. the reporting and follow-up requirements.

Utilization should be limited to the approved purpose. A material purpose change returns the request for reclassification or separate approval.

After execution, the owner records the amount used, resulting balance, evidence, and any replenishment decision. Replenishment is a new treasury or allocation action rather than an automatic entitlement.

---

## 11. Reconciliation

Each asset-holding vault should reconcile custody evidence to its internal record.

```text
Opening balance
+ verified inflows
- verified outflows
+/- corrections
= closing balance
```

The reviewer should investigate:

- transactions missing from the internal ledger;
- ledger entries missing from custody evidence;
- unexpected assets, networks, or destinations;
- stale pending instructions;
- differences caused by fees, conversions, bridges, or custodians.

Reconciliation frequency should reflect transaction volume, asset exposure, and reporting commitments. Material exceptions remain open until resolved, approved as a timing item, or escalated.

Reserve reporting adds a second reconciliation:

```text
Custodied balance
- committed amount
- approved pending use
= uncommitted reserve capacity
```

These fields should retain their units. FUZE token quantities, stablecoin amounts, and accounting values require separate presentation.

---

## 12. Review and Monitoring

The owner should review each active structure on a defined cadence and after a material event.

The review covers:

- continuing business need;
- mandate and classification accuracy;
- authorized roles and signer status;
- custody health and service changes;
- balance and transaction reconciliation;
- open commitments and reserve adequacy;
- reporting accuracy;
- incidents, exceptions, and corrective actions.

Dormant structures still require ownership and status review. A structure with an expired mandate should move to suspension or closure instead of remaining ambiguously available.

Governance, multisignature, and timelock design is addressed in the [FUZE Governance, Multisig, and Timelock Model](24-FUZE_GOVERNANCE_MULTISIG_TIMELOCK_MODEL_PUBLIC.md).

---

## 13. Suspension and Incident Handling

Activity can be suspended when FUZE identifies:

- unauthorized or unexplained movement;
- compromised authority or custody access;
- a material reconciliation difference;
- conflicting instructions or an expired mandate;
- a legal, compliance, security, or counterparty concern.

The incident owner should preserve evidence, identify affected assets and instructions, restrict further movement where feasible, notify the required reviewers, and document the recovery decision.

Possible outcomes include restoring normal operation, replacing authority, returning assets, moving to a recovery vault, correcting records, reclassifying the structure, or closing it.

Public communication should describe a material event at the level appropriate for affected users and reporting commitments while protecting investigation and security details.

---

## 14. Public Reporting

An approved public vault record can include:

| Public field | Purpose |
|---|---|
| Vault label | Identifies the structure without exposing a private person |
| Mandate | Explains the approved function |
| Asset or allocation class | Shows what the structure controls |
| Status | Proposed, active, suspended, closing, or closed |
| Balance or capacity | Provides an amount with unit, timestamp, and methodology |
| Restriction | Summarizes reserve, vesting, lock, program, or custody conditions |
| Movement summary | Describes material inflow, outflow, return, or reclassification |
| Evidence reference | Links to an approved transaction, report, or governance record |
| Review time | Shows when the record was last assessed |

The [FUZE Public Vault Visibility System](16-FUZE_PUBLIC_VAULT_VISIBILITY_SYSTEM_PUBLIC.md) defines presentation and publication behavior.

Wallet labels should describe function rather than personal identity. Public records must keep customer data, participant identity, partner terms, signer details, credentials, and confidential treasury information private.

---

## 15. Closure

A vault or reserve can close when its mandate ends, assets are exhausted or transferred, a program concludes, custody is replaced, or governance retires the structure.

Closure requires:

1. a final balance and reconciliation;
2. disposition of remaining assets;
3. cancellation or transfer of authority;
4. status updates in dependent systems;
5. retention of approvals and evidence;
6. a final internal and public report where applicable.

Closed identifiers should remain traceable. Reuse of an address, account, or label for a different purpose can obscure history and should undergo a new classification review.

---

## 16. Policy Boundaries

Vaults and reserves organize control; they do not make every balance available for use. Custody, allocation, release, circulation, and market availability are separate states.

This policy does not activate a participation window, authorize a token release, publish private custody details, or promise a financial outcome. Those actions require their dedicated approvals and papers.

Detailed category release conditions are in the [FUZE Vault-by-Vault Release Rules](15-FUZE_VAULT_BY_VAULT_RELEASE_RULES_PUBLIC.md). Consolidated token risk treatment is in [FUZE Token Risk Boundaries](29-FUZE_TOKEN_RISK_BOUNDARIES_PUBLIC.md).

---

## Conclusion

FUZE vault and reserve governance begins with a documented purpose and ends with a reconciled, reviewable record.

Classification, segregation, controlled authority, evidence-linked movement, reserve utilization, monitoring, and closure give each structure a clear operational meaning. Public reporting can then communicate that meaning without confusing a balance with availability or exposing private control information.
