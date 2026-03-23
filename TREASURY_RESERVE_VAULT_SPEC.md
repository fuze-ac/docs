# TREASURY RESERVE VAULT SPEC

## 1. Purpose

This specification defines the `FuzeTreasuryReserveVault` contract.

The Treasury Reserve Vault is the long-term strategic reserve of the FUZE ecosystem. Its purpose is to hold the platform treasury allocation under strong governance controls, transparent on-chain rules, and explicit category-based deployment constraints.

The Treasury Reserve Vault is not a founder wallet, not a general-purpose hot wallet, and not a discretionary dumping reserve. It exists to support long-term platform growth, ecosystem durability, and disciplined capital allocation for FUZE as a transparency-first SaaS ecosystem.

---

## 2. Contract Identity

- **Contract name:** `FuzeTreasuryReserveVault`
- **Vault type:** `TREASURY_RESERVE_VAULT`
- **Token held:** `FUZE`
- **Principal allocation:** `120,000,000 FUZE`
- **Governance mode:** multisig + timelock
- **Policy model:** category-based treasury deployment

---

## 3. Design Objectives

The contract MUST satisfy the following objectives:

1. Hold the Treasury Reserve allocation on-chain.
2. Prevent arbitrary or single-signer treasury disposal.
3. Restrict outflows to approved categories and approved destinations.
4. Require timelock for sensitive treasury actions.
5. Emit full event logs for all treasury approvals and executions.
6. Support budget-based treasury governance.
7. Preserve separation from team, advisor, foundation, incentives, liquidity, and migration buckets.
8. Expose transparent public read functions for balances, budgets, queued actions, and governance state.

---

## 4. Treasury Economic Policy

### 4.1 Treasury Principal

The Treasury Reserve allocation is:

> **120,000,000 FUZE**

This allocation is intended to serve as the long-term platform reserve for FUZE.

### 4.2 Treasury Function

The treasury exists to support long-horizon platform and ecosystem needs, not short-term discretionary extraction.

### 4.3 Treasury Deployment Philosophy

Treasury usage MUST be:
- policy-governed
- budget-aware
- destination-restricted
- timelocked
- event-emitting
- publicly reviewable

### 4.4 Treasury Is Not a Personal Asset

The Treasury Reserve is platform-controlled capital. It MUST NOT be treated as:
- founder personal property
- team salary wallet
- advisor vesting wallet
- hidden liquidity wallet
- off-policy partnership slush fund

---

## 5. Allowed Treasury Categories

The Treasury Reserve Vault SHOULD support explicit approved categories. Recommended v1 categories:

1. **Platform Expansion**
   - strategic platform growth
   - infrastructure scaling
   - product line support

2. **Strategic Acquisitions or Integrations**
   - governance-approved ecosystem integrations
   - strategic technical or business combinations

3. **Long-Term Ecosystem Development**
   - public-good platform tooling
   - ecosystem bootstrapping where not handled by dedicated partnership bucket

4. **Governance-Approved Strategic Reserve Actions**
   - exceptional strategic deployments consistent with treasury policy

5. **Emergency Platform Defense**
   - only if separately approved by policy and subject to stronger disclosure

The treasury contract SHOULD NOT be used by default for routine incentives, advisor grants, standard liquidity operations, or normal team compensation because those have dedicated buckets.

---

## 6. Required State Variables

The contract SHOULD expose, at minimum, the following state:

- `address public fuzeToken;`
- `address public governanceMultisig;`
- `address public timelockController;`
- `uint256 public constant TREASURY_ALLOCATION = 120_000_000 * 1e18;`
- `bool public paused;`
- `string public version;`
- `bytes32 public policyHash;`

Recommended additional state:
- `mapping(bytes32 => uint256) public categoryBudget;`
- `mapping(bytes32 => uint256) public categorySpent;`
- `mapping(address => bool) public approvedDestinations;`
- `mapping(address => bytes32) public destinationCategory;`
- `mapping(bytes32 => bool) public approvedCategories;`
- queue structures for timelocked treasury actions
- `uint256 public cumulativeTreasuryOutflow;`

Optional:
- `string public purposeURI;`
- `string public metadataURI;`

---

## 7. Core Invariants

The following invariants are critical and MUST always hold:

### 7.1 No Single-Signer Disposal Invariant

No single signer, role, or externally owned account may directly move treasury funds without the required governance and timelock path.

### 7.2 Destination Restriction Invariant

Treasury tokens may only be sent to pre-approved destinations.

### 7.3 Category Restriction Invariant

Every treasury outflow must be associated with an approved category.

### 7.4 Budget Accounting Invariant

Executed treasury outflows must update category accounting and must not silently bypass budget tracking.

### 7.5 Bucket Separation Invariant

Treasury flows must not be used to simulate or replace:
- team vesting
- advisor vesting
- foundation principal
- holder incentives
- routine liquidity operations
- migration obligations

### 7.6 Event Completeness Invariant

Every treasury approval, queue, cancellation, and execution must emit an event.

---

## 8. Allowed Functions

The contract MAY include only the following functional categories.

### 8.1 Initialization

Allowed during setup only:
- set FUZE token address
- set governance multisig
- set timelock controller
- initialize approved categories
- initialize approved destinations if known
- accept or receive the 120,000,000 FUZE allocation
- initialize policy metadata

### 8.2 View Functions

Required public view functions should include:
- `fuzeToken()`
- `governanceMultisig()`
- `timelockController()`
- `treasuryAllocation()`
- `currentFuzeBalance()`
- `isPaused()`
- `version()`
- `policyHash()`
- `isCategoryApproved(bytes32 category)`
- `categoryBudget(bytes32 category)`
- `categorySpent(bytes32 category)`
- `isDestinationApproved(address destination)`
- `destinationCategory(address destination)`
- queue inspection getters for pending treasury actions

### 8.3 Category Management

Allowed only through governance + timelock:
- approve category
- revoke category
- set category budget
- increase or decrease category budget subject to policy

### 8.4 Destination Management

Allowed only through governance + timelock:
- approve destination wallet or contract
- revoke destination
- map approved destination to allowed category or categories

### 8.5 Treasury Transfer Queueing

Allowed:
- queue treasury transfer request with category, amount, and destination
- enforce timelock before execution
- cancel queued action before execution if governance chooses
- execute queued action after timelock and validity checks

Recommended function pattern:
- `queueTreasuryTransfer(...)`
- `cancelTreasuryTransfer(...)`
- `executeTreasuryTransfer(...)`

### 8.6 Emergency Pause

Optional:
- pause new treasury execution
- unpause treasury execution

Pause should not erase queue history or budget records.

### 8.7 Accidental Foreign Token Recovery

Optional but tightly constrained:
- recover accidental foreign tokens sent to the treasury vault, excluding FUZE principal accounting logic unless explicitly safe and policy-compliant

---

## 9. Forbidden Behaviors

The contract MUST NOT allow any of the following:

1. arbitrary direct transfer by a single signer
2. treasury outflow to non-approved destination
3. treasury outflow without category association
4. treasury outflow without event emission
5. silent OTC transfer or hidden deal routing
6. use of treasury as direct founder compensation wallet
7. use of treasury as normal team vesting source
8. use of treasury as advisor grant source unless separately authorized by major governance process
9. unrestricted market dumping from treasury
10. commingling treasury with foundation principal or dedicated bucket funds
11. hidden arbitrary external call patterns that can move FUZE without category checks
12. upgrade path that bypasses timelock, destination checks, or category accounting

---

## 10. Treasury Transfer Flow Specification

### 10.1 High-Level Flow

1. Governance approves category and budget.
2. Governance approves destination.
3. Treasury action is queued with category, amount, destination, and metadata.
4. Timelock period passes.
5. Execution conditions are rechecked.
6. Transfer executes.
7. Category spent accounting updates.
8. Contract emits execution event.

### 10.2 Queue Rules

Every queued action SHOULD include:
- action id
- category
- destination
- amount
- queue timestamp
- earliest execution timestamp
- metadata or rationale hash

### 10.3 Execution Rules

Execution MUST verify:
- action exists and is not cancelled
- timelock has expired
- destination is still approved
- category is still approved
- category budget is sufficient
- vault has sufficient balance

### 10.4 Cancellation Rules

Queued actions may be cancelled by governance before execution. Cancellation must emit event.

---

## 11. Admin Model

### 11.1 Governance Structure

The contract SHOULD be governed by:
- **Treasury Governance Multisig**
- **Timelock Controller** for sensitive treasury actions

### 11.2 Required Admin Roles

Minimum roles:
- `governanceMultisig`
- `timelockController`

Optional roles:
- `budgetManagerRole`
- `queueManagerRole`
- `pauserRole`

If optional roles are used, their powers MUST remain constrained and observable.

### 11.3 Sensitive Actions Requiring Timelock

The following MUST be timelocked:
- changing governanceMultisig
- changing timelockController
- approving or revoking destinations
- approving or revoking categories
- changing category budgets
- queueing large treasury transfers if queueing itself is governance-authorized
- changing policy metadata or policy hash

### 11.4 Non-Permitted Admin Powers

Admins MUST NOT be able to:
- bypass timelock for sensitive treasury actions
- transfer treasury funds to arbitrary addresses
- reclassify unrelated bucket usage as treasury policy after the fact
- erase historical accounting or event trail

---

## 12. Event Model

The contract SHOULD emit the following events:

### 12.1 Core Governance Events
- `TreasuryGovernanceUpdated(address oldGov, address newGov)`
- `TreasuryTimelockUpdated(address oldTimelock, address newTimelock)`
- `TreasuryPaused(address actor)`
- `TreasuryUnpaused(address actor)`

### 12.2 Category Events
- `TreasuryCategoryApproved(bytes32 category)`
- `TreasuryCategoryRevoked(bytes32 category)`
- `TreasuryCategoryBudgetSet(bytes32 category, uint256 oldBudget, uint256 newBudget)`

### 12.3 Destination Events
- `TreasuryDestinationApproved(address destination, bytes32 category)`
- `TreasuryDestinationRevoked(address destination, bytes32 category)`

### 12.4 Transfer Lifecycle Events
- `TreasuryTransferQueued(bytes32 actionId, bytes32 category, address destination, uint256 amount, uint256 executeAfter, bytes32 metadataHash)`
- `TreasuryTransferCancelled(bytes32 actionId)`
- `TreasuryTransferExecuted(bytes32 actionId, bytes32 category, address destination, uint256 amount)`

### 12.5 Policy / Metadata Events
- `TreasuryPolicyHashUpdated(bytes32 oldHash, bytes32 newHash)`
- `TreasuryMetadataURIUpdated(string oldURI, string newURI)`

### 12.6 Recovery Events
If foreign-token recovery exists:
- `TreasuryForeignTokenRecovered(address token, uint256 amount, address destination)`

---

## 13. Upgradeability Policy

### 13.1 Preferred Policy

The Treasury Reserve Vault MAY be carefully upgradeable if justified by treasury control evolution, but the default posture should remain conservative.

### 13.2 Required Upgrade Constraints

If upgradeable, the contract MUST satisfy all of the following:
- upgrade controlled by multisig + timelock
- public event emitted on upgrade
- no upgrade may increase Treasury allocation beyond 120,000,000 FUZE
- no upgrade may remove category restrictions
- no upgrade may remove destination approval checks
- no upgrade may bypass queue + timelock execution model
- no upgrade may disable core accounting or event logging

### 13.3 Economically Immutable Rules

The following treasury rules must be treated as economically immutable unless a major public governance process occurs:
- 120,000,000 FUZE treasury allocation cap
- treasury is distinct from team, foundation, advisor, incentives, and liquidity buckets
- treasury transfers require category association
- treasury transfers require approved destination
- treasury transfers require event trail

---

## 14. Security Requirements

The implementation MUST include or address:
- reentrancy protection where needed
- strict role separation
- queue id uniqueness and replay safety
- safe token transfer handling
- robust validation for destination approvals
- robust validation for category accounting
- no arbitrary external call execution paths
- invariant tests for budget and destination controls

Recommended test categories:
- single signer cannot move treasury
- non-approved destination execution fails
- over-budget execution fails
- cancelled action cannot execute
- paused state blocks execution if pause is enabled
- event emission occurs on every treasury lifecycle action

---

## 15. Integration Expectations

The Treasury Reserve Vault may interact with approved downstream contracts or wallets, but only through the approved destination model.

Expected integration patterns may include:
- approved deployment wallets
- approved ecosystem contracts
- approved governance modules
- approved strategic reserve modules if added later

No integration may bypass the treasury’s category, destination, and event restrictions.

---

## 16. Canonical Summary

| Field | Value |
|---|---|
| Contract Name | `FuzeTreasuryReserveVault` |
| Principal Amount | `120,000,000 FUZE` |
| Core Purpose | Long-term platform treasury reserve |
| Principal Mobility | Governed, not permanently locked |
| Transfer Model | Approved category + approved destination + timelock |
| Governance | Treasury multisig + timelock |
| Upgradeability | Carefully upgradeable if needed |
| Critical Invariant | No arbitrary treasury disposal |

---

## 17. Canonical Policy Statement

The FUZE Treasury Reserve Vault is the long-term strategic reserve of the FUZE ecosystem holding 120,000,000 FUZE under governance-controlled rules. Treasury assets may only be deployed through approved categories, approved destinations, and timelocked execution paths with full on-chain event logging. The Treasury Reserve is distinct from founder, team, foundation, advisor, incentives, liquidity, and migration allocations, and must never function as a discretionary or opaque source of token disposal.
