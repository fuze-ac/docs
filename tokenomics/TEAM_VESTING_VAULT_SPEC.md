# TEAM_VESTING_VAULT_SPEC.md

## 1. Purpose

This specification defines the `FuzeTeamVestingVault` contract.

The Team Vesting Vault is the dedicated non-upgradeable vesting contract for the FUZE team allocation. Its purpose is to hold the Team Allocation under strict vesting rules and release vested FUZE only to approved beneficiaries according to published schedules.

This contract is intended to support long-term alignment for the founder, core team, future key hires, and long-term builders, while preventing early extraction, hidden admin override behavior, and discretionary insider disposal.

---

## 2. Contract Identity

- **Contract name:** `FuzeTeamVestingVault`
- **Vault type:** `TEAM_VESTING_VAULT`
- **Token held:** `FUZE`
- **Principal allocation:** `45,000,000 FUZE`
- **Upgradeability:** `Non-upgradeable`
- **Core model:** beneficiary-based vesting schedules with claimable vested balances

---

## 3. Design Objectives

The contract MUST satisfy the following objectives:

1. Hold the Team Allocation on-chain under explicit vesting rules.
2. Support beneficiary-specific vesting schedules.
3. Prevent claiming of unvested tokens.
4. Prevent arbitrary admin withdrawal of team allocation.
5. Keep team allocation separate from treasury, foundation, liquidity, incentives, advisor, and migration buckets.
6. Expose transparent public read functions for grants, vesting progress, and claims.
7. Emit complete event logs for grant creation, updates, revocations if any, and claims.
8. Remain non-upgradeable after deployment.

---

## 4. Team Allocation Policy

### 4.1 Team Allocation Amount

The Team Allocation is:

> **45,000,000 FUZE**

This allocation is reserved for:
- founder
- core team
- future key hires
- long-term builders
- approved strategic internal operators

### 4.2 Team Allocation Philosophy

The Team Allocation exists to reward long-term contribution to the FUZE ecosystem. It is not intended for immediate liquidity or short-term extraction.

### 4.3 Vesting Principle

All team allocations held in this contract MUST be subject to vesting.

No beneficiary may claim tokens before the vesting rules for that beneficiary allow such claim.

### 4.4 Separation Principle

The Team Vesting Vault MUST NOT function as:
- general treasury
- founder hot wallet
- advisor bucket
- ecosystem grant bucket
- operational liquidity source
- discretionary emergency reserve

---

## 5. Recommended Vesting Policy

The contract should be flexible enough to support beneficiary-specific schedules, but FUZE’s canonical team policy should default to a strict long-term model.

### Recommended default vesting template
- **Cliff:** 12 months
- **Linear vesting:** 36 months after cliff
- **Claim model:** vested tokens claimable on demand after vesting accrues

### Optional alternative schedules
The contract MAY support different schedules for future hires or special internal roles, but such schedules must still be explicitly registered on-chain and remain visible.

---

## 6. Required State Variables

The contract SHOULD expose, at minimum, the following state:

- `address public fuzeToken;`
- `address public governanceMultisig;`
- `address public timelockController;`
- `uint256 public constant TEAM_ALLOCATION = 45_000_000 * 1e18;`  
  or adjusted for FUZE decimals
- `uint256 public totalAllocated;`
- `uint256 public totalClaimed;`
- `uint256 public totalRevoked;` if revocation is supported
- `bool public paused;`
- `string public version;`
- `bytes32 public policyHash;`

For each beneficiary, the contract SHOULD track:
- beneficiary address
- total grant amount
- start timestamp
- cliff timestamp
- vesting end timestamp
- claimed amount
- revoked amount if applicable
- schedule status
- whether the grant is revocable or irrevocable

Suggested structure:
- `mapping(address => VestingSchedule) public vestingSchedules;`

Optional but recommended:
- `string public purposeURI;`
- `string public metadataURI;`

---

## 7. Vesting Schedule Model

Each beneficiary schedule SHOULD include at least:

- `beneficiary`
- `totalAmount`
- `startTime`
- `cliffTime`
- `endTime`
- `claimedAmount`
- `revokedAmount`
- `isRevocable`
- `isRevoked`
- `exists`

### Vested Amount Calculation

The schedule should support the following general behavior:
- before cliff: vested = 0
- after cliff and before end: vested grows linearly
- after end: vested = totalAmount minus revokedAmount if applicable

### Claimable Amount Calculation

`claimable = vestedAmount - claimedAmount`

The contract MUST never allow claim greater than claimable.

---

## 8. Core Invariants

The following invariants are critical and MUST always hold:

### 8.1 No Early Claim Invariant

No beneficiary may claim more than the vested amount available at claim time.

### 8.2 No Admin Drain Invariant

No governance or admin path may transfer the Team Allocation arbitrarily to an unrelated wallet.

### 8.3 Grant Accounting Invariant

`totalAllocated` must never exceed the Team Allocation cap.

### 8.4 Claim Accounting Invariant

A beneficiary’s cumulative claimed amount must never exceed that beneficiary’s vested entitlement.

### 8.5 Bucket Separation Invariant

Team Vesting Vault funds must not be reused as treasury, liquidity, partnership, or advisor reserves.

### 8.6 Non-Upgradeability Invariant

The deployed contract must remain non-upgradeable.

---

## 9. Allowed Functions

The contract MAY include only the following functional categories.

### 9.1 Initialization

Allowed during setup only:
- set FUZE token address
- set governanceMultisig
- set timelockController
- initialize policy metadata
- accept or receive the 45,000,000 FUZE allocation

### 9.2 View Functions

Required public view functions should include:
- `fuzeToken()`
- `governanceMultisig()`
- `timelockController()`
- `teamAllocation()`
- `currentFuzeBalance()`
- `totalAllocated()`
- `totalClaimed()`
- `totalRevoked()` if revocation exists
- `isPaused()`
- `version()`
- `policyHash()`
- `vestingSchedules(address beneficiary)`
- `vestedAmount(address beneficiary)`
- `claimableAmount(address beneficiary)`

### 9.3 Grant Creation

Allowed only through governance + timelock or tightly governed grant manager flow:
- create beneficiary vesting schedule
- assign total grant amount
- assign start, cliff, and end timestamps
- mark grant as revocable or irrevocable

Recommended function pattern:
- `createGrant(...)`

### 9.4 Grant Update

Strongly preferred restriction:
- no arbitrary weakening of beneficiary protections once a grant exists

If updates are supported, they should be limited to:
- administrative correction before claim activity begins
- metadata correction
- policy-consistent revocation state updates

Recommended approach for safety:
- minimal update surface
- prefer immutable grant terms after creation

### 9.5 Claiming

Allowed:
- beneficiary claims vested tokens
- beneficiary claims only up to `claimableAmount`

Recommended function pattern:
- `claim()`
or
- `claimFor(address beneficiary)` if intentionally supported

Preferred v1 model:
- beneficiary claims to their own address

### 9.6 Revocation

Optional and policy-sensitive.

If revocation is supported, it MUST be explicit and narrow.

Recommended rule:
- only grants marked `isRevocable = true` may be revoked
- only unvested remainder may be revoked
- already vested amounts must remain claimable unless a stricter published policy explicitly says otherwise

Recommended function pattern:
- `revokeGrant(address beneficiary)`

### 9.7 Emergency Pause

Optional:
- pause claims and/or grant creation
- unpause claims and/or grant creation

Pause should not erase grant records or vested accounting.

### 9.8 Foreign Token Recovery

Optional but tightly constrained:
- recover accidental foreign tokens sent to contract
- MUST NOT permit recovery of FUZE team allocation in a way that bypasses vesting

---

## 10. Forbidden Behaviors

The contract MUST NOT allow any of the following:

1. arbitrary transfer of team allocation to admin wallet
2. claim of unvested tokens
3. grant creation that silently exceeds allocation cap
4. admin override that changes a grant into immediately liquid allocation without governance process
5. hidden founder-only privileged withdrawal path
6. use of team allocation as treasury source
7. use of team allocation as liquidity source
8. use of team allocation as advisor bucket substitute
9. contract upgrade or proxy-based logic replacement
10. silent deletion of claim history or beneficiary schedules
11. arbitrary external call patterns that can move FUZE outside vesting rules
12. revocation of vested and already-earned beneficiary tokens unless explicitly allowed by published policy and visible in schedule terms

---

## 11. Grant Lifecycle Flow

### 11.1 High-Level Flow

1. Governance approves a beneficiary grant.
2. Grant is created on-chain with explicit vesting schedule.
3. Beneficiary waits through cliff and vesting progression.
4. Beneficiary claims vested tokens over time.
5. Grant remains active until fully claimed or revoked if revocable.

### 11.2 Grant Creation Rules

Grant creation MUST verify:
- beneficiary address is valid
- grant amount is greater than zero
- total allocated after creation does not exceed Team Allocation cap
- cliff and end timestamps are valid
- schedule does not conflict with policy constraints

### 11.3 Claim Rules

Claim execution MUST verify:
- beneficiary has an existing schedule
- vault is not paused if pause affects claims
- claimable amount is positive
- claim amount does not exceed claimable amount

### 11.4 Revocation Rules

If supported, revocation MUST verify:
- schedule exists
- schedule is marked revocable
- revocation has not already occurred
- only unvested remainder is revoked according to published rules

---

## 12. Admin Model

### 12.1 Governance Structure

The contract SHOULD be governed by:
- **Team Vesting Governance Multisig**
- **Timelock Controller** for sensitive actions

### 12.2 Required Admin Roles

Minimum roles:
- `governanceMultisig`
- `timelockController`

Optional roles:
- `grantManagerRole`
- `pauserRole`

If optional roles are used, they must remain constrained and observable.

### 12.3 Sensitive Actions Requiring Timelock

The following MUST be timelocked:
- changing governanceMultisig
- changing timelockController
- creating large grants if grant creation is governance-routed
- changing policyHash
- invoking revocation if revocation is supported and policy-sensitive

### 12.4 Non-Permitted Admin Powers

Admins MUST NOT be able to:
- bypass vesting rules
- grant themselves arbitrary liquidity from the vault
- erase beneficiary history
- change contract code or logic post-deployment
- seize vested claimed balances from beneficiaries

---

## 13. Event Model

The contract SHOULD emit the following events:

### 13.1 Governance Events
- `TeamVestingGovernanceUpdated(address oldGov, address newGov)`
- `TeamVestingTimelockUpdated(address oldTimelock, address newTimelock)`
- `TeamVestingPaused(address actor)`
- `TeamVestingUnpaused(address actor)`

### 13.2 Grant Lifecycle Events
- `TeamGrantCreated(address beneficiary, uint256 amount, uint256 startTime, uint256 cliffTime, uint256 endTime, bool isRevocable)`
- `TeamGrantUpdated(address beneficiary)` if limited updates are supported
- `TeamGrantRevoked(address beneficiary, uint256 revokedAmount)` if revocation exists

### 13.3 Claim Events
- `TeamTokensClaimed(address beneficiary, uint256 amount)`

### 13.4 Policy / Metadata Events
- `TeamVestingPolicyHashUpdated(bytes32 oldHash, bytes32 newHash)`
- `TeamVestingMetadataURIUpdated(string oldURI, string newURI)`

### 13.5 Recovery Events
If foreign-token recovery exists:
- `TeamVestingForeignTokenRecovered(address token, uint256 amount, address destination)`

---

## 14. Upgradeability Policy

### 14.1 Required Policy

The Team Vesting Vault MUST be:

> **Non-upgradeable**

### 14.2 Implementation Rule

The deployment MUST NOT use:
- upgradeable proxy pattern
- admin-controlled implementation replacement
- hidden migration hook that can substitute logic post-deployment

### 14.3 Economic Immutability Principle

The following properties must remain immutable after deployment except through explicit grant-level state transitions allowed by the contract itself:
- Team Allocation cap
- non-upgradeable nature
- core vesting rules enforced by the contract
- claim accounting history

---

## 15. Security Requirements

The implementation MUST include or address:
- reentrancy protection for claim path if needed
- strict role separation
- safe token transfer handling
- accurate vested amount computation
- no arbitrary external call execution paths
- invariant tests for cap and claim correctness
- invariant tests for non-upgradeability assumptions

Recommended test categories:
- beneficiary cannot claim before cliff
- beneficiary can claim correct vested amount after cliff
- beneficiary cannot over-claim
- total allocated cannot exceed 45,000,000 FUZE
- non-beneficiary cannot claim someone else’s grant unless explicitly supported by policy
- revocation cannot seize already vested claimable amount unless explicitly designed and policy-consistent
- no admin route can drain vault balance arbitrarily

---

## 16. Integration Expectations

The Team Vesting Vault is expected to integrate with:
- FUZE token contract
- governance multisig
- timelock controller
- public dashboards or reporting tools for vesting visibility

Expected public read integration:
- beneficiary vesting status
- total allocated vs remaining capacity
- total claimed visibility
- policy metadata visibility

This contract should not require integration with profit participation logic unless the published holder policy explicitly includes vested or unvested team allocations, which should be treated as a separate policy question outside this contract.

---

## 17. Canonical Summary

| Field | Value |
|---|---|
| Contract Name | `FuzeTeamVestingVault` |
| Principal Amount | `45,000,000 FUZE` |
| Core Purpose | Team, founder, core builder, and future hire vesting |
| Principal Mobility | Claimable only through vesting rules |
| Claim Model | Beneficiary-based vesting claims |
| Governance | Team vesting multisig + timelock |
| Upgradeability | Non-upgradeable |
| Critical Invariant | No unvested token can be claimed |

---

## 18. Canonical Policy Statement

The FUZE Team Vesting Vault is the non-upgradeable on-chain vesting contract for the 45,000,000 FUZE Team Allocation. It exists to align the founder, core team, future key hires, and long-term builders with the long-term success of the FUZE ecosystem through explicit vesting schedules, claim accounting, and transparent on-chain enforcement. The contract may release only vested FUZE to approved beneficiaries and must never function as a discretionary source of insider liquidity or treasury disposal.
