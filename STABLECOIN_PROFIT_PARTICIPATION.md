# STABLECOIN PROFIT PARTICIPATION

## 1. Purpose

This specification defines the `FuzeStablecoinProfitParticipation` contract.

The Stablecoin Profit Participation Contract is the on-chain distribution layer that receives stablecoin funding for a finalized profit-participation cycle and allocates claimable stablecoin amounts to eligible FUZE holders according to the published profit-distribution policy.

Its purpose is to make FUZE holder profit participation transparent, policy-driven, auditable, and compatible with the broader FUZE token architecture.

This contract does not determine platform accounting truth by itself. Platform accounting, distributable profit determination, and policy-defined eligibility are established off-chain and published through FUZE’s transparency process. This contract is the on-chain execution and claim layer for finalized payout cycles.

---

## 2. Contract Identity

- **Contract name:** `FuzeStablecoinProfitParticipation`
- **Contract type:** `PROFIT_PARTICIPATION_DISTRIBUTOR`
- **Primary function:** distribute stablecoin profit participation to eligible FUZE holders
- **Funding asset(s):** approved stablecoin(s), such as USDT and/or USDC
- **Eligibility basis:** published holder policy and finalized payout dataset
- **Claim model:** cycle-based claim accounting

---

## 3. Design Objectives

The contract MUST satisfy the following objectives:

1. Accept stablecoin funding for finalized payout cycles.
2. Support holder claimability by cycle.
3. Ensure no address can claim more than its finalized allocation.
4. Support Foundation Vault participation as an eligible holder under the same published holder policy.
5. Keep cycle-based accounting transparent and queryable.
6. Emit complete events for funding, cycle activation, claim execution, and finalization.
7. Minimize discretionary admin control after a cycle is finalized.
8. Preserve a clear separation between off-chain accounting determination and on-chain claim execution.

---

## 4. Role in the FUZE Profit Model

### 4.1 Off-Chain vs On-Chain Boundary

The full FUZE profit participation process has two layers:

#### Off-Chain Layer
- determine gross revenue
- determine net revenue
- determine approved operating costs
- determine distributable profit under the published policy
- determine eligible holder dataset and payout amounts
- publish quarterly transparency report and payout ledger

#### On-Chain Layer
- receive approved stablecoin funding for a finalized cycle
- register finalized cycle data reference and claim dataset root or mapping
- allow each eligible address to claim its stablecoin amount
- prevent double claims or over-claims
- emit immutable claim events

### 4.2 Contract Scope

This contract is the on-chain distributor and claim system. It MUST NOT be treated as the sole source of accounting truth for revenue or profit determination.

---

## 5. Supported Payout Models

The contract SHOULD be designed to support one or both of the following claim models:

### Model A: Merkle-Root Claim Model
- each cycle publishes a Merkle root of claim entitlements
- claimant proves entitlement by Merkle proof
- efficient for large holder sets

### Model B: Direct Allocation Registry Model
- governance or authorized distributor records final claim amounts per address
- simpler but less scalable for large populations

Preferred v1 model:

> **Merkle-root claim model**

because it scales better for large eligible-holder sets and fits published payout-ledger workflows.

---

## 6. Required State Variables

The contract SHOULD expose, at minimum, the following state:

- `address public governanceMultisig;`
- `address public timelockController;`
- `mapping(address => bool) public approvedStablecoins;`
- `uint256 public currentCycleId;`
- `bool public paused;`
- `string public version;`
- `bytes32 public policyHash;`

For each payout cycle, the contract SHOULD track:
- payout cycle id
- stablecoin asset used
- total stablecoin funded
- total claimable amount
- total claimed amount
- Merkle root or equivalent entitlement reference
- cycle status
- claim window open timestamp
- claim window close timestamp if applicable
- metadata hash or transparency report hash

Recommended structures:
- `mapping(uint256 => CycleData) public cycles;`
- `mapping(uint256 => mapping(address => uint256)) public claimedAmount;`
  or boolean claimed flags if one claim per address per cycle

---

## 7. Cycle Data Model

Each cycle SHOULD include at least:

- `cycleId`
- `stablecoin`
- `fundedAmount`
- `claimableTotal`
- `claimedTotal`
- `merkleRoot` or equivalent
- `openedAt`
- `claimDeadline` if used
- `status`
- `transparencyReportHash`
- `payoutLedgerHash`
- `notesHash` or optional metadata hash

Suggested statuses:
- `UNINITIALIZED`
- `FUNDED`
- `OPEN`
- `CLOSED`
- `FINALIZED`
- `EMERGENCY_PAUSED`

---

## 8. Eligible Holder Policy Integration

### 8.1 Policy Source

Eligibility is determined off-chain according to the published FUZE holder policy, which may include:
- holder rank rules
- minimum eligibility thresholds
- exclusion lists
- approved wallet classifications
- record-date or snapshot logic
- any policy-defined duration or ranking adjustments

### 8.2 On-Chain Treatment

The contract should treat the finalized cycle dataset as authoritative for that cycle.

### 8.3 Foundation Eligibility

`FuzeFoundationVault` MAY be included as an eligible address under the published holder policy.

If included:
- it should receive claimable stablecoin like any other eligible address
- it should claim through its own restricted vault logic
- it must not receive special contract-side treatment beyond its finalized allocation

---

## 9. Allowed Functions

The contract MAY include only the following functional categories.

### 9.1 Initialization

Allowed during setup only:
- set governanceMultisig
- set timelockController
- approve stablecoin(s)
- initialize metadata and policy references

### 9.2 Stablecoin Approval Management

Allowed only through governance + timelock:
- approve supported stablecoin asset
- revoke supported stablecoin asset

### 9.3 Cycle Creation and Funding

Allowed only through governance or authorized distributor role:
- create new payout cycle
- set cycle metadata
- deposit or register stablecoin funding
- set Merkle root or entitlement reference
- open claim window

Recommended function pattern:
- `createCycle(...)`
- `fundCycle(...)`
- `openCycle(...)`

### 9.4 Claim Functions

Allowed:
- claim stablecoin allocation for a specific cycle
- claim only if entitlement is valid
- claim only up to finalized allocation amount

Recommended function pattern:
- `claim(uint256 cycleId, uint256 amount, bytes32[] calldata proof)` for Merkle model

Optional convenience:
- `claimMultiple(uint256[] cycleIds, ...)`

### 9.5 Cycle Closure / Finalization

Allowed:
- close claim window if policy requires
- finalize cycle after claim window ends
- mark unclaimed balance handling status if policy requires

### 9.6 Emergency Pause

Optional:
- pause new claims
- unpause claims

Pause SHOULD NOT erase cycle records or claimed balances.

### 9.7 Foreign Token Recovery

Optional but tightly constrained:
- recover accidental non-approved tokens sent to contract
- MUST NOT permit recovery of valid funded cycle assets in ways that violate claim rights

---

## 10. Forbidden Behaviors

The contract MUST NOT allow any of the following:

1. claim more than finalized entitlement
2. double-claim same allocation
3. use unapproved stablecoin asset for official cycle funding
4. overwrite live cycle allocation data without governance process
5. arbitrary admin transfer of funded claimable stablecoins during active cycle
6. hidden adjustment of holder entitlements after cycle opening without transparent governance process
7. preferential claim route for insider wallets beyond finalized dataset
8. silent deletion of cycle history
9. upgrade path that invalidates already-earned claims
10. arbitrary seizure of active-cycle claimable funds without published policy path

---

## 11. Funding Model

### 11.1 Stablecoin Funding Source

The contract should be funded by stablecoin deposits representing the finalized payout pool for a given cycle.

### 11.2 Funding Requirement

Before a cycle is opened for claims, the funded stablecoin amount SHOULD be sufficient to cover the full claimable total for that cycle.

### 11.3 Asset Constraint

Each cycle SHOULD specify exactly one approved payout stablecoin unless a multi-asset model is intentionally introduced.

Preferred v1 design:
- one stablecoin per cycle
- fully funded before cycle opens

### 11.4 Funding Events

Funding must emit explicit events showing:
- cycle id
- stablecoin asset
- funded amount
- funder address if applicable

---

## 12. Claim Flow Specification

### 12.1 High-Level Flow

1. Off-chain accounting finalizes distributable profit and eligible-holder allocations.
2. Governance funds a payout cycle with approved stablecoin.
3. Governance sets the cycle claim dataset reference.
4. Governance opens the cycle.
5. Eligible addresses claim their stablecoin allocation.
6. Contract updates claim accounting and emits events.
7. Cycle closes and later finalizes according to policy.

### 12.2 Claim Verification Rules

A claim MUST verify:
- cycle exists and is open
- stablecoin funding is present
- claimant entitlement is valid
- claim has not already exhausted entitlement
- proof or dataset reference matches cycle root
- claim deadline has not passed if deadline exists

### 12.3 Partial vs Full Claim

Preferred v1 design:

> **one full claim per address per cycle**

This simplifies accounting.

If partial claim is supported, it MUST maintain exact remaining entitlement accounting.

### 12.4 Claim Destination

Claims should default to the claimant address.

Foundation claims, if executed through `FuzeFoundationVault`, should follow Foundation Vault routing logic, not a special-case path inside this contract.

---

## 13. Unclaimed Funds Policy

The contract SHOULD support a published rule for unclaimed balances after a cycle closes.

Possible approaches:
- remain claimable indefinitely
- claim window closes and unclaimed funds move to a predefined reserve
- claim window closes and unclaimed funds await governance-controlled redistribution under policy

Recommended v1 approach:
- fixed claim window
- unclaimed funds handled only through published policy and explicit event trail

The exact destination for unclaimed funds should be determined by FUZE’s profit-distribution policy and should not be arbitrary.

---

## 14. Admin Model

### 14.1 Governance Structure

The contract SHOULD be governed by:
- **Profit Participation Governance Multisig**
- **Timelock Controller** for sensitive changes

### 14.2 Required Admin Roles

Minimum roles:
- `governanceMultisig`
- `timelockController`

Optional roles:
- `cycleManagerRole`
- `funderRole`
- `pauserRole`

### 14.3 Sensitive Actions Requiring Timelock

The following MUST be timelocked:
- changing governanceMultisig
- changing timelockController
- approving or revoking stablecoins
- changing policyHash
- altering unclaimed-fund handling rules if configurable
- changing critical cycle-management parameters

### 14.4 Non-Permitted Admin Powers

Admins MUST NOT be able to:
- withdraw active-cycle claimable stablecoins arbitrarily
- bypass entitlement verification
- create hidden insider allocations after cycle publication
- erase cycle claim history

---

## 15. Event Model

The contract SHOULD emit the following events:

### 15.1 Governance Events
- `ProfitGovernanceUpdated(address oldGov, address newGov)`
- `ProfitTimelockUpdated(address oldTimelock, address newTimelock)`
- `ProfitParticipationPaused(address actor)`
- `ProfitParticipationUnpaused(address actor)`

### 15.2 Stablecoin Asset Events
- `StablecoinApproved(address stablecoin)`
- `StablecoinRevoked(address stablecoin)`

### 15.3 Cycle Lifecycle Events
- `CycleCreated(uint256 cycleId, address stablecoin, bytes32 merkleRoot, bytes32 reportHash)`
- `CycleFunded(uint256 cycleId, address stablecoin, uint256 amount)`
- `CycleOpened(uint256 cycleId, uint256 openedAt, uint256 claimDeadline)`
- `CycleClosed(uint256 cycleId)`
- `CycleFinalized(uint256 cycleId, uint256 totalClaimed, uint256 unclaimedAmount)`

### 15.4 Claim Events
- `ProfitClaimed(uint256 cycleId, address claimant, address stablecoin, uint256 amount)`

### 15.5 Policy Events
- `ProfitPolicyHashUpdated(bytes32 oldHash, bytes32 newHash)`
- `CycleMetadataUpdated(uint256 cycleId, bytes32 oldHash, bytes32 newHash)`

### 15.6 Recovery Events
If foreign-token recovery exists:
- `ForeignTokenRecovered(address token, uint256 amount, address destination)`

---

## 16. Upgradeability Policy

### 16.1 Preferred Policy

The contract MAY be carefully upgradeable if needed for distributor logic evolution, but upgrades must remain tightly constrained.

### 16.2 Required Upgrade Constraints

If upgradeable, the contract MUST satisfy all of the following:
- upgrade controlled by multisig + timelock
- public event emitted on upgrade
- no upgrade may invalidate already-recorded cycle claims
- no upgrade may remove core cycle history
- no upgrade may create arbitrary admin-withdraw powers over active-cycle claimable funds
- no upgrade may bypass entitlement checks
- no upgrade may remove event logging for funding and claims

### 16.3 Economically Immutable Rules

The following must be treated as economically immutable once a cycle is opened:
- approved payout asset for the cycle
- cycle claim dataset reference
- funded cycle claimable total for that cycle, except transparent corrective governance path if absolutely necessary
- already-executed claims

---

## 17. Security Requirements

The implementation MUST include or address:
- reentrancy protection for claim path
- strict role separation
- robust proof verification if Merkle model is used
- accounting correctness for claimed amounts
- safe stablecoin transfer handling
- invariant tests for over-claim prevention
- invariant tests for cycle isolation
- invariant tests for funding sufficiency assumptions

Recommended test categories:
- valid claimant can claim exactly entitlement
- invalid proof fails
- double claim fails
- claim after deadline fails if deadline enabled
- claim from wrong cycle root fails
- non-approved stablecoin funding path fails
- active-cycle funds cannot be arbitrarily drained

---

## 18. Integration Expectations

The contract is expected to integrate with:
- FUZE transparency reporting process
- Foundation Vault contract
- off-chain payout dataset generation tooling
- frontends or dashboards for claim visibility

Expected public read integration:
- cycle metadata display
- claimable amount lookup
- cycle funding visibility
- total claimed visibility

Foundation integration expectation:
- `FuzeFoundationVault` claims from this contract as an eligible address
- this contract does not need Foundation-specific payout logic beyond normal holder claim support

---

## 19. Canonical Summary

| Field | Value |
|---|---|
| Contract Name | `FuzeStablecoinProfitParticipation` |
| Core Purpose | Distribute finalized stablecoin profit participation to eligible holders |
| Funding Asset | Approved stablecoin(s) |
| Eligibility Source | Published holder policy + finalized payout dataset |
| Claim Model | Cycle-based claim accounting |
| Governance | Profit multisig + timelock |
| Upgradeability | Carefully upgradeable if needed |
| Critical Invariant | No address can claim more than finalized entitlement |

---

## 20. Canonical Policy Statement

The FUZE Stablecoin Profit Participation Contract is the on-chain claim and distribution layer for finalized profit-participation cycles. It receives approved stablecoin funding for a published payout cycle and allows eligible FUZE holders to claim their finalized allocation under transparent, cycle-based accounting rules. The contract executes distribution logic on-chain, while accounting determination, eligibility policy, and distributable profit calculation remain governed by FUZE’s published transparency and profit-distribution framework.
