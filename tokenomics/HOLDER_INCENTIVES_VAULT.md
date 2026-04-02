# HOLDER INCENTIVES VAULT

## 1. Purpose

This specification defines the `FuzeHolderIncentivesVault` contract.

The Holder Incentives Vault is the dedicated smart contract for the FUZE Community / Holder Incentives allocation. Its purpose is to hold and distribute incentive allocations through transparent, policy-governed, and preferably programmatic mechanisms that reward ecosystem participation without turning the bucket into an opaque discretionary reserve.

This contract is intended to support long-term community alignment across the FUZE ecosystem, including holder rewards, loyalty programs, referral incentives, activation campaigns, rank-based ecosystem participation, and other approved holder-facing incentive systems.

---

## 2. Contract Identity

- **Contract name:** `FuzeHolderIncentivesVault`
- **Vault type:** `HOLDER_INCENTIVES_VAULT`
- **Token held:** `FUZE`
- **Principal allocation:** `55,000,000 FUZE`
- **Core model:** governed incentive reserve with programmatic or campaign-based distribution paths
- **Preferred posture:** transparent, category-based, and event-rich distribution logic

---

## 3. Design Objectives

The contract MUST satisfy the following objectives:

1. Hold the Community / Holder Incentives allocation on-chain.
2. Support policy-governed incentive campaign creation and funding.
3. Support transparent holder incentive distribution.
4. Prevent arbitrary admin dumping or opaque insider routing.
5. Support formula-based or claim-based reward mechanisms where possible.
6. Expose transparent public read functions for campaign budgets, claim states, and governance state.
7. Emit complete event logs for campaign lifecycle actions and claims.
8. Keep the incentives bucket separate from treasury, team, foundation, liquidity, advisor, migration, and partnership buckets.

---

## 4. Incentives Allocation Policy

### 4.1 Incentives Allocation Amount

The Community / Holder Incentives allocation is:

> **55,000,000 FUZE**

This allocation is intended to support holder and community-alignment programs across the FUZE ecosystem.

### 4.2 Incentives Philosophy

The incentives bucket exists to reward ecosystem participation, loyalty, activation, and community growth under transparent rules.

It is not intended to function as:
- hidden treasury reserve
- disguised founder or team allocation
- discretionary market-sell wallet
- substitute for partnership grants
- substitute for advisor compensation

### 4.3 Incentive Design Principle

Wherever possible, incentives should be:
- formula-based
- campaign-scoped
- claim-based
- category-labeled
- capped by explicit budgets
- event-emitting and publicly auditable

---

## 5. Recommended Incentive Categories

The Holder Incentives Vault SHOULD support explicit approved incentive categories. Recommended v1 categories include:

1. **Holder Loyalty Programs**
   - long-term holder campaigns
   - rank-based ecosystem participation incentives
   - loyalty accrual programs

2. **Referral and Ambassador Programs**
   - referral campaigns
   - community ambassador incentives
   - ecosystem introduction rewards

3. **Product Activation Campaigns**
   - onboarding incentives
   - usage activation campaigns across FUZE SaaS products
   - launch participation campaigns

4. **Community Participation Programs**
   - governance participation incentives if policy allows
   - public community contribution campaigns
   - ecosystem engagement initiatives

5. **Special Approved Holder Campaigns**
   - time-bounded or event-based programs approved through governance

This contract SHOULD NOT be used for direct team compensation, advisor vesting, or treasury-style strategic deployment.

---

## 6. Distribution Model Options

The contract SHOULD support one or more of the following reward models:

### Model A: Campaign Budget + Direct Claim Registry
- governance creates a campaign
- campaign budget is assigned
- eligible claimants are registered or rooted
- users claim according to campaign rules

### Model B: Merkle-Root Incentive Campaigns
- a campaign budget is created
- a Merkle root defines claimant entitlements
- users claim using proofs

### Model C: Modular Reward Engine Funding
- vault funds approved downstream reward modules
- downstream modules execute campaign logic under approved constraints

Preferred v1 posture:

> support campaign-based budget accounting and either direct claim registry or Merkle-root campaign distributions

This provides a clean mix of flexibility and transparency.

---

## 7. Required State Variables

The contract SHOULD expose, at minimum, the following state:

- `address public fuzeToken;`
- `address public governanceMultisig;`
- `address public timelockController;`
- `uint256 public constant HOLDER_INCENTIVES_ALLOCATION = 55_000_000 * 1e18;`  
  or adjusted for FUZE decimals
- `uint256 public totalAllocatedToCampaigns;`
- `uint256 public totalClaimed;`
- `uint256 public totalExpiredOrRevoked;`
- `bool public paused;`
- `string public version;`
- `bytes32 public policyHash;`

Recommended additional state:
- `mapping(bytes32 => IncentiveCampaign) public campaigns;`
- `mapping(bytes32 => bool) public approvedCategories;`
- `mapping(bytes32 => uint256) public categoryBudget;`
- `mapping(bytes32 => uint256) public categorySpent;`
- claimant tracking per campaign
- root or registry per campaign

Optional:
- `string public purposeURI;`
- `string public metadataURI;`

---

## 8. Incentive Campaign Model

Each campaign SHOULD include at least:

- `campaignId`
- `category`
- `budget`
- `claimed`
- `startTime`
- `endTime`
- `claimDeadline`
- `status`
- `distributionModel`
- `metadataHash`
- `entitlementRoot` or equivalent if Merkle model is used
- `isRevocable` if campaign may be cancelled under policy

Suggested statuses:
- `UNINITIALIZED`
- `CREATED`
- `OPEN`
- `PAUSED`
- `CLOSED`
- `FINALIZED`
- `REVOKED`

---

## 9. Core Invariants

The following invariants are critical and MUST always hold:

### 9.1 Allocation Cap Invariant

Campaign allocations must never cause the vault to exceed the total Community / Holder Incentives allocation cap.

### 9.2 Campaign Budget Invariant

No campaign may distribute more than its assigned budget.

### 9.3 Claim Accounting Invariant

No claimant may claim more than the amount they are entitled to under the campaign rules.

### 9.4 Category Accounting Invariant

Every campaign must belong to an approved category and update category accounting.

### 9.5 Bucket Separation Invariant

The Holder Incentives Vault must not be reused as treasury, team, advisor, liquidity, migration, or partnership capital.

### 9.6 Event Completeness Invariant

Every campaign creation, update, revocation, funding, opening, closure, and claim must emit an event.

---

## 10. Allowed Functions

The contract MAY include only the following functional categories.

### 10.1 Initialization

Allowed during setup only:
- set FUZE token address
- set governanceMultisig
- set timelockController
- initialize approved categories
- initialize policy metadata
- accept or receive the 55,000,000 FUZE allocation

### 10.2 View Functions

Required public view functions should include:
- `fuzeToken()`
- `governanceMultisig()`
- `timelockController()`
- `holderIncentivesAllocation()`
- `currentFuzeBalance()`
- `totalAllocatedToCampaigns()`
- `totalClaimed()`
- `totalExpiredOrRevoked()`
- `isPaused()`
- `version()`
- `policyHash()`
- `isCategoryApproved(bytes32 category)`
- `categoryBudget(bytes32 category)`
- `categorySpent(bytes32 category)`
- `campaigns(bytes32 campaignId)`
- claimability and claim-status getters per campaign where applicable

### 10.3 Category Management

Allowed only through governance + timelock:
- approve category
- revoke category
- set category budget
- increase or decrease category budget under policy

### 10.4 Campaign Creation

Allowed only through governance + timelock or tightly controlled campaign-manager flow:
- create incentive campaign
- assign category
- assign budget
- assign timing
- assign distribution model
- set entitlement root or equivalent reference if needed
- set metadata hash

Recommended function pattern:
- `createCampaign(...)`

### 10.5 Campaign Opening / Closing

Allowed:
- open campaign
- close campaign
- finalize campaign
- pause / unpause campaign if model supports campaign-level pausing

### 10.6 Claiming

Allowed:
- claimant claims FUZE incentive from an open campaign
- claim only if entitlement is valid
- claim only up to remaining entitlement

Recommended function pattern:
- `claim(bytes32 campaignId, uint256 amount, bytes32[] calldata proof)` for Merkle model

Optional:
- `claimMultiple(...)`

### 10.7 Campaign Revocation or Expiry Handling

Optional and policy-sensitive.

If revocation is supported:
- only campaigns marked revocable should be revocable
- already-earned or already-claimable user amounts should be handled according to published campaign rules
- expired or revoked residual budget should be explicitly accounted for

### 10.8 Approved Module Funding

Optional and advanced.

If the vault supports downstream reward modules:
- downstream modules must be approved destinations
- funding must remain category-scoped and event-emitting
- downstream modules must not create silent off-policy disposal paths

### 10.9 Emergency Pause

Optional:
- pause new campaign creation
- pause claims
- unpause operations

Pause should not erase campaign history or claim records.

### 10.10 Foreign Token Recovery

Optional but tightly constrained:
- recover accidental foreign tokens sent to contract
- MUST NOT permit FUZE incentives allocation to be withdrawn outside campaign rules

---

## 11. Forbidden Behaviors

The contract MUST NOT allow any of the following:

1. arbitrary direct transfer of incentives allocation to unrelated wallets
2. campaign creation that silently exceeds allocation cap
3. claim beyond entitlement
4. campaign distribution beyond budget
5. hidden insider allocation through community campaign paths
6. use of holder incentives bucket as treasury source
7. use of holder incentives bucket as team or advisor compensation bucket
8. use of holder incentives bucket as liquidity operations source
9. silent deletion of campaign history
10. arbitrary external call patterns that move FUZE outside approved campaign logic
11. upgrade path that bypasses campaign accounting or claimant protections
12. opaque mass transfer with no campaign association

---

## 12. Incentive Campaign Lifecycle Flow

### 12.1 High-Level Flow

1. Governance approves category and budget.
2. Campaign is created on-chain with explicit budget and rules.
3. Campaign is opened.
4. Eligible users claim according to campaign entitlement logic.
5. Campaign closes or expires.
6. Final accounting is recorded.
7. Residual or revoked amounts are handled according to policy.

### 12.2 Campaign Creation Rules

Campaign creation MUST verify:
- category is approved
- budget is greater than zero
- category budget is sufficient if category budgets are enforced
- total campaign allocations remain within overall allocation cap
- timing fields are valid
- distribution model is recognized

### 12.3 Claim Rules

Claim execution MUST verify:
- campaign exists and is open
- claimant entitlement is valid
- claim amount does not exceed entitlement
- claim amount does not exceed remaining campaign budget
- vault is not paused if pause affects claims

### 12.4 Closure and Finalization Rules

Campaign closure or finalization SHOULD record:
- total claimed
- residual budget
- expired or revoked amount
- final campaign status

---

## 13. Admin Model

### 13.1 Governance Structure

The contract SHOULD be governed by:
- **Holder Incentives Governance Multisig**
- **Timelock Controller** for sensitive actions

### 13.2 Required Admin Roles

Minimum roles:
- `governanceMultisig`
- `timelockController`

Optional roles:
- `campaignManagerRole`
- `pauserRole`
- `moduleManagerRole`

If optional roles are used, their powers must remain constrained and observable.

### 13.3 Sensitive Actions Requiring Timelock

The following MUST be timelocked:
- changing governanceMultisig
- changing timelockController
- approving or revoking categories
- changing category budgets
- creating large campaigns if creation is governance-routed
- changing policyHash
- approving downstream modules if module funding exists

### 13.4 Non-Permitted Admin Powers

Admins MUST NOT be able to:
- bypass campaign accounting
- assign arbitrary undisclosed incentives to themselves
- erase claimant history
- reclassify unrelated use as community incentives after the fact
- route incentives allocation into founder, team, treasury, or liquidity channels without published governance process

---

## 14. Event Model

The contract SHOULD emit the following events:

### 14.1 Governance Events
- `HolderIncentivesGovernanceUpdated(address oldGov, address newGov)`
- `HolderIncentivesTimelockUpdated(address oldTimelock, address newTimelock)`
- `HolderIncentivesPaused(address actor)`
- `HolderIncentivesUnpaused(address actor)`

### 14.2 Category Events
- `IncentiveCategoryApproved(bytes32 category)`
- `IncentiveCategoryRevoked(bytes32 category)`
- `IncentiveCategoryBudgetSet(bytes32 category, uint256 oldBudget, uint256 newBudget)`

### 14.3 Campaign Lifecycle Events
- `IncentiveCampaignCreated(bytes32 campaignId, bytes32 category, uint256 budget, uint256 startTime, uint256 endTime, bytes32 metadataHash)`
- `IncentiveCampaignOpened(bytes32 campaignId)`
- `IncentiveCampaignClosed(bytes32 campaignId)`
- `IncentiveCampaignFinalized(bytes32 campaignId, uint256 totalClaimed, uint256 residualAmount)`
- `IncentiveCampaignRevoked(bytes32 campaignId, uint256 revokedAmount)` if revocation exists

### 14.4 Claim Events
- `IncentiveClaimed(bytes32 campaignId, address claimant, uint256 amount)`

### 14.5 Module Events
If downstream modules are supported:
- `IncentiveModuleApproved(address module, bytes32 category)`
- `IncentiveModuleRevoked(address module, bytes32 category)`
- `IncentiveModuleFunded(address module, bytes32 category, uint256 amount)`

### 14.6 Policy / Metadata Events
- `HolderIncentivesPolicyHashUpdated(bytes32 oldHash, bytes32 newHash)`
- `HolderIncentivesMetadataURIUpdated(string oldURI, string newURI)`

### 14.7 Recovery Events
If foreign-token recovery exists:
- `HolderIncentivesForeignTokenRecovered(address token, uint256 amount, address destination)`

---

## 15. Upgradeability Policy

### 15.1 Preferred Policy

The Holder Incentives Vault MAY be carefully upgradeable if needed for campaign-logic evolution, but upgrades must remain tightly constrained.

### 15.2 Required Upgrade Constraints

If upgradeable, the contract MUST satisfy all of the following:
- upgrade controlled by multisig + timelock
- public event emitted on upgrade
- no upgrade may increase the Holder Incentives allocation beyond 55,000,000 FUZE
- no upgrade may remove campaign accounting guarantees
- no upgrade may remove claimant protection rules
- no upgrade may create arbitrary admin-transfer paths
- no upgrade may disable event logging for campaign lifecycle and claims

### 15.3 Economically Immutable Rules

The following should be treated as economically immutable unless a major public governance process occurs:
- 55,000,000 FUZE allocation cap
- category-based incentive framing
- campaign or claim association requirement for distributions
- separation from treasury, team, advisor, and liquidity buckets

---

## 16. Security Requirements

The implementation MUST include or address:
- reentrancy protection for claim path if needed
- strict role separation
- safe token transfer handling
- robust proof verification if Merkle model is used
- budget accounting correctness
- invariant tests for campaign-cap enforcement
- invariant tests for over-claim prevention
- no arbitrary external call execution paths unless explicitly governed and constrained

Recommended test categories:
- claimant cannot claim beyond entitlement
- campaign cannot exceed budget
- total campaign allocations cannot exceed 55,000,000 FUZE
- unauthorized campaign creation fails
- paused state blocks claims if pause is enabled
- revoked or closed campaign claim behavior matches policy
- no admin path can drain the vault arbitrarily

---

## 17. Integration Expectations

The Holder Incentives Vault is expected to integrate with:
- FUZE token contract
- governance multisig
- timelock controller
- community dashboards and campaign frontends
- optional downstream approved reward modules

Expected public read integration:
- campaign list and metadata visibility
- campaign budget and claimed amount visibility
- claimant status visibility where supported
- category accounting visibility

This contract should remain focused on incentives and should not directly absorb treasury, vesting, or liquidity responsibilities.

---

## 18. Canonical Summary

| Field | Value |
|---|---|
| Contract Name | `FuzeHolderIncentivesVault` |
| Principal Amount | `55,000,000 FUZE` |
| Core Purpose | Community and holder incentive distribution |
| Principal Mobility | Campaign-based and policy-governed |
| Distribution Model | Campaign budgets + claim or reward logic |
| Governance | Holder incentives multisig + timelock |
| Upgradeability | Carefully upgradeable if needed |
| Critical Invariant | No incentive distribution may exceed campaign entitlement or budget |

---

## 19. Canonical Policy Statement

The FUZE Holder Incentives Vault is the dedicated smart contract for the 55,000,000 FUZE Community / Holder Incentives allocation. It exists to distribute holder- and community-facing incentives through transparent, category-based, campaign-governed mechanisms with explicit accounting, explicit limits, and full on-chain event visibility. The contract must never function as a discretionary treasury, insider compensation channel, or hidden liquidity source.
