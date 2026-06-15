# FUZE Controlled Circulation Policy

## Executive Summary

FUZE controlled circulation governs how tokens move from an approved allocation and custody state into a released, deployed, claimable, or circulating state.

The policy requires every movement to have a permitted purpose, source allocation, authorization, destination, amount, status classification, transaction evidence, and reconciliation. A transfer between controlled wallets does not become circulating supply merely because it appears on-chain.

Different allocation categories use different release rules, but this paper does not repeat those vault-specific rules. It establishes the common state machine and controls that every release, transfer, return, lock, vest, deployment, or correction should follow.

Controlled circulation is a supply-governance and reporting discipline. It does not control market price or assure exchange access, demand, liquidity, or resale.

---

## 1. Policy Objective

The policy is intended to:

- preserve the purpose of approved allocations;
- distinguish custody movement from economic circulation;
- prevent unauthorized or misclassified release;
- connect transactions to governance and operating evidence;
- support consistent supply reporting;
- provide pause, return, correction, and incident routes;
- make changes understandable without exposing sensitive controls.

The complete fixed supply and category amounts are maintained in [FUZE Token Allocation Table](02-FUZE_TOKEN_ALLOCATION_TABLE_PUBLIC.md).

---

## 2. Circulation States

Tokens can occupy several policy states.

| State | Meaning |
|---|---|
| Allocated | Assigned to an approved supply category |
| Custodied | Held in the approved vault, contract, wallet, or account for that category |
| Planned | Included in a proposed use or budget without commitment |
| Committed | Subject to an approved obligation or program |
| Locked | Restricted by time, contract, policy, or another enforceable condition |
| Vesting | Progressing under a time, service, or milestone schedule |
| Claimable | Available to an eligible recipient under an active process |
| Released | Moved from the prior controlled state under authorization |
| Operationally deployed | Placed into an approved contract, program, partner, or market operation |
| Circulating | Reasonably available in user or market circulation under the reporting method |
| Returned | Moved back to approved category custody |
| Suspended | Frozen from further action pending review |
| Corrected | Reclassified or adjusted through an approved correction record |

One token balance can contain portions in different states. Reports should avoid assigning one label to an entire wallet when the underlying records support multiple classifications.

---

## 3. State Transition Rule

A token state changes only through an approved transition.

Every transition record should identify:

1. source allocation and custody location;
2. opening state;
3. permitted purpose;
4. recipient or destination class;
5. amount;
6. approval authority;
7. release, vesting, eligibility, or program condition;
8. transaction or system evidence;
9. resulting state;
10. reporting and reconciliation treatment.

The basic path can be:

```text
Allocated -> custodied -> planned or committed
-> locked, vesting, claimable, or approved for release
-> released or operationally deployed
-> circulating, returned, completed, suspended, or corrected
```

Not every movement follows every state. The transition record should show the path actually used.

---

## 4. Permitted Movement Classes

### Custody transfer

Moves tokens between approved controlled addresses without changing allocation purpose or release status.

Examples can include wallet replacement, contract migration, custody restructuring, or network operations. The transfer remains non-circulating when control and restrictions continue.

### Vesting release

Changes a vested amount under an approved time, service, or milestone rule. Vesting can make tokens eligible for later release without making them circulating immediately.

### Claim or eligibility release

Makes an approved amount available to an eligible recipient under an active migration, community, incentive, or other defined process.

### Program deployment

Moves tokens into an approved product, community, partner, incentive, or ecosystem program with its own scope and records.

### Treasury deployment

Uses reserve or treasury supply for an approved strategic, operating, partnership, or other category-consistent purpose.

### Market-operation deployment

Moves tokens for approved liquidity or market-structure activity under the dedicated policy, custody, venue, and reporting controls.

### Return or recovery

Returns unused, cancelled, expired, recovered, or incorrectly delivered tokens to the appropriate controlled category.

### Correction

Repairs an erroneous classification, duplicate release, wrong amount, wrong destination, or other record problem through an approved process.

---

## 5. Movement Request

Before execution, the request should contain:

| Request field | Required content |
|---|---|
| Movement identifier | Stable reference |
| Source | Allocation, vault, address, and current state |
| Purpose | Approved reason and policy basis |
| Destination | Address, contract, custodian, program, or recipient class |
| Amount | FUZE quantity and any batch detail |
| Conditions | Vesting, lock, eligibility, milestone, agreement, or program rule |
| Requested state | Intended post-movement classification |
| Timing | Earliest execution, deadline, and relevant reporting period |
| Evidence | Agreement, eligibility, vesting, governance, treasury, or program records |
| Owner | Requester and responsible operator |

An incomplete request remains pending and should not be executed through informal instruction.

---

## 6. Authorization

Authorization should match the sensitivity and category.

Review can include:

- allocation-purpose confirmation;
- available and uncommitted balance;
- vault or custody authority;
- vesting, eligibility, milestone, or release condition;
- legal, accounting, treasury, compliance, or jurisdiction review where relevant;
- technical destination and network checks;
- public communication and reporting readiness;
- multisig, timelock, or governance approval where applicable.

The requester, approver, executor, and reconciler should be separated for sensitive movements.

Approval of a program budget is not necessarily approval of every transfer. The operating rule should state whether individual, batch, or threshold-based authorization applies.

---

## 7. Pre-Execution Checks

Immediately before execution, FUZE should confirm:

- source address and category;
- available balance and existing commitments;
- approved amount and destination;
- network and contract identity;
- destination ownership or purpose;
- applicable lock, vesting, or claim status;
- duplicate-payment or duplicate-release checks;
- current signer and role configuration;
- pause, sanctions, incident, or restriction status;
- expected post-transaction classification.

Material differences return the request to review.

---

## 8. Execution and Evidence

The execution record should include:

- signed approval reference;
- source and destination;
- amount;
- transaction hash or system reference;
- network and block or confirmation context;
- fees where relevant;
- executor;
- execution time;
- confirmation status;
- batch manifest where applicable;
- resulting custody and state.

Technical success does not prove correct business classification. The transaction must still reconcile to the approved request and allocation ledger.

---

## 9. Circulating-Supply Classification

FUZE should use a documented method to determine whether released tokens count as circulating.

Factors can include:

- continued lock, vesting, transfer, or contractual restriction;
- custody by FUZE-controlled treasury, reserve, team, advisor, partner, liquidity, or program wallets;
- availability to an eligible recipient;
- operational deployment in a contract or pool;
- ability to transfer or trade;
- return or recovery rights;
- current reporting methodology.

Examples:

- A transfer from one treasury wallet to another remains controlled custody.
- Tokens placed in a vesting contract can be released from the source vault while remaining restricted.
- A claimable amount can remain outside circulation until claimed, depending on the published method.
- Tokens deployed into a liquidity pool require a market-operation classification rather than an assumption that the entire amount is ordinary holder circulation.

Supply terminology and calculation fields belong in [FUZE Token Release and Circulation Clarity](13-FUZE_TOKEN_RELEASE_AND_CIRCULATION_CLARITY_PUBLIC.md).

---

## 10. Batch and Program Controls

Batch releases require:

1. approved participant or destination manifest;
2. amount per entry and reconciled total;
3. duplicate and exception checks;
4. transaction or contract output;
5. failed-item handling;
6. closing allocation and program balance;
7. final status report.

Program owners should track approved budget, committed amount, released amount, returned amount, cancelled amount, and remaining capacity.

A program can pause before the full budget is used. Unused tokens retain their allocation purpose unless a formal reclassification is approved.

---

## 11. Returns and Unused Amounts

Returned tokens should map back to the correct allocation and state.

The return record should explain:

- original release or program;
- reason for return;
- source and destination;
- amount;
- transaction evidence;
- whether obligations remain;
- revised allocation and circulation classification.

Tokens returned from an external or market context may require additional legal, accounting, treasury, or reporting review before reuse.

---

## 12. Exceptions and Corrections

Exceptions can include:

- transfer to an incorrect address;
- wrong amount or allocation;
- duplicate or unauthorized release;
- failed batch item;
- incorrect circulating classification;
- expired or cancelled commitment;
- compromised wallet or contract;
- vesting, eligibility, or claim error;
- missing or inconsistent approval evidence.

FUZE should preserve the original record, stop related action where possible, investigate impact, correct ledgers, seek recovery where appropriate, update public reports, and document the final decision.

A correction should not erase the transaction history.

---

## 13. Pause and Emergency Control

Movement can be paused when a material issue affects:

- custody or signer security;
- contract behavior;
- allocation authority;
- eligibility or manifest integrity;
- treasury reconciliation;
- legal or jurisdiction support;
- third-party venue, bridge, custodian, or infrastructure;
- public reporting accuracy.

The pause record should state scope, effective time, responsible authority, affected requests, interim controls, and review conditions.

Restart requires confirmation that the issue and affected records have been addressed.

---

## 14. Reclassification

Changing an allocation purpose is different from moving tokens between wallets.

A reclassification proposal should identify:

- source and destination categories;
- amount and percentage impact;
- reason another category is required;
- existing commitments and affected stakeholders;
- governance and specialist approvals;
- updated allocation ledger and public table;
- effective date and communication.

The total must continue to reconcile to the fixed 500,000,000 FUZE supply.

Operational convenience is insufficient justification for silently using one allocation for another purpose.

---

## 15. Reporting

A circulation report can show:

- reporting period and method;
- total supply reference;
- opening and closing state balances;
- releases by allocation and movement class;
- locked, vesting, claimable, deployed, returned, and circulating classifications;
- custody transfers excluded from circulation change;
- corrections and reclassifications;
- market-operation deployment where public-safe;
- transaction, governance, or report references.

Reports should state whether figures are point-in-time or period movements. They should also identify methodology changes and restated prior figures.

Public wallet reporting must not expose personal identity, private agreements, credentials, signer details, or security-sensitive procedures.

---

## 16. Relationship to Adjacent Policies

This policy controls common movement and state-transition rules.

- [FUZE Token Release and Circulation Clarity](13-FUZE_TOKEN_RELEASE_AND_CIRCULATION_CLARITY_PUBLIC.md) defines supply terminology and report interpretation.
- [FUZE Vault and Reserve Policy](14-FUZE_VAULT_AND_RESERVE_POLICY_PUBLIC.md) defines custody and reserve purposes.
- [FUZE Vault-by-Vault Release Rules](15-FUZE_VAULT_BY_VAULT_RELEASE_RULES_PUBLIC.md) defines category-specific release conditions.
- [FUZE Team Advisor Partner Vesting](19-FUZE_TEAM_ADVISOR_PARTNER_VESTING_PUBLIC.md) defines contributor vesting.
- [FUZE Liquidity and Listing Policy](21-FUZE_LIQUIDITY_AND_LISTING_POLICY_PUBLIC.md) governs market-operation context.

Platform Credits and stablecoin compensation use separate ledgers and do not change FUZE token circulation.

---

## 17. Public Boundary

Controlled circulation is a governance and reporting policy. It is not a price-management mechanism, release schedule for every allocation, market-making commitment, or statement that a particular amount is currently circulating.

Specific releases depend on the controlling allocation, vault, vesting, eligibility, treasury, partner, migration, community, or market policy.

Circulation-related risks are summarized in [FUZE Token Risk Boundaries](29-FUZE_TOKEN_RISK_BOUNDARIES_PUBLIC.md); readers needing the repository-wide disclosure source should consult the [FUZE Risk and Disclosure Appendix](../WHITEPAPER-PAPERS/05-FUZE_RISK_AND_DISCLOSURE_APPENDIX_PUBLIC.md).

---

## Conclusion

Controlled circulation requires every FUZE token movement to pass through an approved purpose, authorization, execution, state classification, reconciliation, and reporting path.

The state model prevents custody transfers, vesting events, claims, program deployments, and market operations from being treated as identical circulation events.

This common policy supports category-specific release rules while preserving a consistent public account of how supply changes state.
