# ADVISOR_VESTING_VAULT_SPEC.md

## 1. Purpose

This specification defines the `FuzeAdvisorVestingVault` contract.

The Advisor Vesting Vault is the dedicated smart contract for the FUZE Advisors / Strategic Contributors allocation. Its purpose is to hold advisor and strategic contributor allocations under transparent, policy-governed vesting rules and release vested FUZE only to approved beneficiaries according to explicit schedules.

This contract is intended to support long-term alignment for qualified advisors, strategic contributors, senior ecosystem operators, and approved external contributors, while preventing early extraction, hidden admin override behavior, and discretionary insider disposal.

---

## 2. Contract Identity

- **Contract name:** `FuzeAdvisorVestingVault`
- **Vault type:** `ADVISOR_VESTING_VAULT`
- **Token held:** `FUZE`
- **Principal allocation:** `15,000,000 FUZE`
- **Upgradeability:** `Non-upgradeable` preferred
- **Core model:** beneficiary-based vesting schedules with claimable vested balances

---

## 3. Design Objectives

The contract MUST satisfy the following objectives:

1. Hold the Advisors / Strategic Contributors allocation on-chain under explicit vesting rules.
2. Support beneficiary-specific vesting schedules.
3. Prevent claiming of unvested tokens.
4. Prevent arbitrary admin withdrawal of advisor allocation.
5. Keep the advisor allocation separate from treasury, foundation, team, liquidity, incentives, partnership, and migration buckets.
6. Expose transparent public read functions for grants, vesting progress, and claims.
7. Emit complete event logs for grant creation, updates if any, revocations if any, and claims.
8. Preserve strong trust guarantees for beneficiaries and holders.

---

## 4. Advisor Allocation Policy

### 4.1 Advisor Allocation Amount

The Advisors / Strategic Contributors allocation is:

> **15,000,000 FUZE**

This allocation is reserved for:
- strategic advisors
- senior external contributors
- approved ecosystem operators
- special contributors with long-term value to FUZE
- policy-approved strategic contributors

### 4.2 Advisor Allocation Philosophy

The advisor allocation exists to reward long-term value creation and strategic contribution to the FUZE ecosystem. It is not intended for immediate liquidity or short-term extraction.

### 4.3 Vesting Principle

All advisor allocations held in this contract MUST be subject to vesting.

No beneficiary may claim tokens before the vesting rules for that beneficiary allow such claim.

### 4.4 Separation Principle

The Advisor Vesting Vault MUST NOT function as:
- general treasury
- founder hot wallet
- team vesting bucket
- ecosystem grant bucket
- operational liquidity source
- discretionary emergency reserve

---

## 5. Recommended Vesting Policy

The contract should be flexible enough to support beneficiary-specific schedules, but FUZE’s canonical advisor policy should default to a structured long-term model.

### Recommended default vesting template
- **Cliff:** 6 months
- **Linear vesting:** 18 months after cliff
- **Claim model:** vested tokens claimable on demand after vesting accrues

### Optional alternative schedules
The contract MAY support different schedules for exceptional contributors, but such schedules must still be explicitly registered on-chain and remain visible.

### Policy note
Advisor schedules should generally remain more conservative than immediate-liquid grants and should clearly distinguish strategic contribution from short-term promotional activity.

---

## 6. Required State Variables

The contract SHOULD expose, at minimum, the following state:

- `address public fuzeToken;`
- `address public governanceMultisig;`
- `address public timelockController;`
- `uint256 public constant ADVISOR_ALLOCATION = 15_000_000 * 1e18;`  
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

No governance or admin path may transfer the Advisor Allocation arbitrarily to an unrelated wallet.

### 8.3 Grant Accounting Invariant

`totalAllocated` must never exceed the Advisor Allocation cap.

### 8.4 Claim Accounting Invariant

A beneficiary’s cumulative claimed amount must never exceed that beneficiary’s vested entitlement.

### 8.5 Bucket Separation Invariant

Advisor Vesting Vault funds must not be reused as treasury, liquidity, partnership, team, or incentives reserves.

### 8.6 Beneficiary Transparency Invariant

Every advisor grant must be explicitly represented on-chain through a schedule or equivalent record. No off-ledger advisor allocation should be treated as if it were part of this vault.

---

## 9. Allowed Functions

The contract MAY include only the following functional categories.

### 9.1 Initialization

Allowed during setup only:
- set FUZE token address
- set governanceMultisig
- set timelockController
- initialize policy metadata
- accept or receive the 15,000,000 FUZE allocation

### 9.2 View Functions

Required public view functions should include:
- `fuzeToken()`
- `governanceMultisig()`
- `timelockController()`
- `advisorAllocation()`
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

Allowed only through governance + timelock or tightly governed grant-manager flow:
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
- MUST NOT permit FUZE advisor allocation to be recovered or withdrawn in a way that bypasses vesting

---

## 10. Forbidden Behaviors

The contract MUST NOT allow any of the following:

1. arbitrary transfer of advisor allocation to admin wallet
2. claim of unvested tokens
3. grant creation that silently exceeds allocation cap
4. admin override that changes a grant into immediately liquid allocation without governance process
5. hidden privileged withdrawal path for insiders
6. use of advisor allocation as treasury source
7. use of advisor allocation as team compensation substitute
8. use of advisor allocation as liquidity source
9. silent deletion of claim history or beneficiary schedules
10. arbitrary external call patterns that can move FUZE outside vesting rules
11. revocation of vested and already-earned beneficiary tokens unless explicitly allowed by published policy and visible in schedule terms
12. hidden recycling of revoked allocations outside published governance process

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
- total allocated after creation does not exceed Advisor Allocation cap
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
- **Advisor Vesting Governance Multisig**
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
- seize vested claimed balances from beneficiaries
- convert the contract into another bucket by governance shortcut

---

## 13. Event Model

The contract SHOULD emit the following events:

### 13.1 Governance Events
- `AdvisorVestingGovernanceUpdated(address oldGov, address newGov)`
- `AdvisorVestingTimelockUpdated(address oldTimelock, address newTimelock)`
- `AdvisorVestingPaused(address actor)`
- `AdvisorVestingUnpaused(address actor)`

### 13.2 Grant Lifecycle Events
- `AdvisorGrantCreated(address beneficiary, uint256 amount, uint256 startTime, uint256 cliffTime, uint256 endTime, bool isRevocable)`
- `AdvisorGrantUpdated(address beneficiary)` if limited updates are supported
- `AdvisorGrantRevoked(address beneficiary, uint256 revokedAmount)` if revocation exists

### 13.3 Claim Events
- `AdvisorTokensClaimed(address beneficiary, uint256 amount)`

### 13.4 Policy / Metadata Events
- `AdvisorVestingPolicyHashUpdated(bytes32 oldHash, bytes32 newHash)`
- `AdvisorVestingMetadataURIUpdated(string oldURI, string newURI)`

### 13.5 Recovery Events
If foreign-token recovery exists:
- `AdvisorVestingForeignTokenRecovered(address token, uint256 amount, address destination)`

---

## 14. Upgradeability Policy

### 14.1 Preferred Policy

The Advisor Vesting Vault SHOULD be:

> **Non-upgradeable**

This is preferred because vesting credibility improves when beneficiaries and holders know the contract logic cannot later be modified through a proxy or implementation swap.

### 14.2 If Non-Upgradeability Is Relaxed

If there is any reason to use an upgradeable pattern, that decision should be explicitly disclosed and justified in a separate policy document. It should not be the default.

### 14.3 Economic Immutability Principle

The following properties should remain economically immutable after deployment except through explicit grant-level state transitions allowed by the contract itself:
- Advisor Allocation cap
- claim accounting history
- core vesting rules enforced by the contract
- beneficiary grant records once created, except limited policy-consistent actions such as explicit revocation of revocable grants

---

## 15. Security Requirements

The implementation MUST include or address:
- reentrancy protection for claim path if needed
- strict role separation
- safe token transfer handling
- accurate vested amount computation
- no arbitrary external call execution paths
- invariant tests for cap and claim correctness
- invariant tests for beneficiary protections

Recommended test categories:
- beneficiary cannot claim before cliff
- beneficiary can claim correct vested amount after cliff
- beneficiary cannot over-claim
- total allocated cannot exceed 15,000,000 FUZE
- non-beneficiary cannot claim someone else’s grant unless explicitly supported by policy
- revocation cannot seize already vested claimable amount unless explicitly designed and policy-consistent
- no admin route can drain vault balance arbitrarily

---

## 16. Integration Expectations

The Advisor Vesting Vault is expected to integrate with:
- FUZE token contract
- governance multisig
- timelock controller
- public dashboards or reporting tools for vesting visibility

Expected public read integration:
- beneficiary vesting status
- total allocated vs remaining capacity
- total claimed visibility
- policy metadata visibility

This contract should not require integration with profit participation logic unless the published holder policy explicitly includes advisor allocations, which should be treated as a separate policy question outside this contract.

---

## 17. Canonical Summary

| Field | Value |
|---|---|
| Contract Name | `FuzeAdvisorVestingVault` |
| Principal Amount | `15,000,000 FUZE` |
| Core Purpose | Advisor and strategic contributor vesting |
| Principal Mobility | Claimable only through vesting rules |
| Claim Model | Beneficiary-based vesting claims |
| Governance | Advisor vesting multisig + timelock |
| Upgradeability | Non-upgradeable preferred |
| Critical Invariant | No unvested token can be claimed |

---

## 18. Canonical Policy Statement

The FUZE Advisor Vesting Vault is the dedicated smart contract for the 15,000,000 FUZE Advisors / Strategic Contributors allocation. It exists to align strategic advisors and approved contributors with the long-term success of the FUZE ecosystem through explicit vesting schedules, claim accounting, and transparent on-chain enforcement. The contract may release only vested FUZE to approved beneficiaries and must never function as a discretionary source of insider liquidity, treasury disposal, or hidden allocation routing.
