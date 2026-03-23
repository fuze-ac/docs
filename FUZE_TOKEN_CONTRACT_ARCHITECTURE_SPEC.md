# FUZE_TOKEN_CONTRACT_ARCHITECTURE_SPEC.md

## 1. Purpose

This specification defines the master on-chain architecture for FUZE token allocation contracts.

The goals are to:
- make all major allocations transparent
- reduce discretionary control
- minimize holder trust assumptions
- separate each allocation by purpose
- enforce clear on-chain behavior
- support FUZE as a transparency-first SaaS ecosystem

This architecture is designed around the principle:

> one allocation bucket = one dedicated contract = one clear purpose = one visible rule set

---

## 2. Scope

This document covers the major FUZE token allocation contracts, including:
- contract names
- token amount per contract
- allowed functions
- forbidden behaviors
- admin model
- event model
- upgradeability policy

This document does not yet define low-level Solidity implementation details, ABI signatures, gas optimizations, or deployment scripts. Those should be specified in follow-up contract-level specifications.

---

## 3. Global Principles

All FUZE allocation contracts MUST follow these principles:

1. One allocation bucket must be held by one dedicated contract.
2. Each contract must have one clear and auditable purpose.
3. Each contract must expose public read functions for balances, governance addresses, and operational status.
4. Each contract must emit explicit events for all privileged actions and token movements.
5. Each contract must define forbidden behaviors clearly.
6. No hidden omnibus treasury should exist for unrelated buckets.
7. All privileged actions must be controlled by multisig unless intentionally permissionless.
8. All sensitive admin changes should be timelocked.
9. Upgradeability should be avoided unless strictly necessary.
10. Public transparency and holder trust take priority over admin convenience.

---

## 4. Master Allocation Map

### 4.1 Community Presale Contract
- **Contract name:** `FuzeCommunityPresale`
- **Token amount:** `110,000,000 FUZE`
- **Status:** already deployed
- **Reference:** current community presale contract

### 4.2 BOARD Migration Contract
- **Contract name:** `FuzeBoardMigrationVault`
- **Token amount:** `25,000,000 FUZE`

### 4.3 Team Vesting Contract
- **Contract name:** `FuzeTeamVestingVault`
- **Token amount:** `45,000,000 FUZE`

### 4.4 Foundation Vault Contract
- **Contract name:** `FuzeFoundationVault`
- **Token amount:** `35,000,000 FUZE`

### 4.5 Platform Treasury Reserve Contract
- **Contract name:** `FuzeTreasuryReserveVault`
- **Token amount:** `120,000,000 FUZE`

### 4.6 Community / Holder Incentives Contract
- **Contract name:** `FuzeHolderIncentivesVault`
- **Token amount:** `55,000,000 FUZE`

### 4.7 Ecosystem Growth & Partnerships Contract
- **Contract name:** `FuzeEcosystemPartnershipVault`
- **Token amount:** `40,000,000 FUZE`

### 4.8 Liquidity & Market Operations Contract
- **Contract name:** `FuzeLiquidityOperationsVault`
- **Token amount:** `30,000,000 FUZE`

### 4.9 Advisors / Strategic Contributors Contract
- **Contract name:** `FuzeAdvisorVestingVault`
- **Token amount:** `15,000,000 FUZE`

### 4.10 Transparency / Stability Reserve Contract
- **Contract name:** `FuzeTransparencyStabilityVault`
- **Token amount:** `25,000,000 FUZE`

---

## 5. Common Contract Interface Requirements

Every FUZE allocation contract SHOULD expose, at minimum:

- `fuzeToken()`
- `vaultName()`
- `vaultType()`
- `allocatedAmount()`
- `currentBalance()`
- `governanceAddress()`
- `timelockAddress()` if applicable
- `isPaused()` if applicable
- `version()`

Optional but recommended:

- `purposeURI()`
- `policyHash()`
- `metadataURI()`

These getters should allow holders and external tools to verify state without requiring privileged access.

---

## 6. Contract-by-Contract Architecture

## 6.1 FuzeCommunityPresale

### Purpose
Manage community presale participation, vesting, and claims.

### Allowed Functions
- accept and record presale participation according to existing rules
- track purchased allocation per participant
- enforce vesting schedule
- allow user claims according to vesting rules
- expose participant allocation and claimed status
- finalize sale state if required by contract design

### Forbidden Behaviors
- no arbitrary reassignment of purchased user allocations
- no manual withdrawal of committed buyer balances
- no hidden minting or off-ledger token creation
- no non-policy token transfers to admins

### Admin Model
- multisig admin
- timelock for sensitive changes if mutable
- pause only for emergency response

### Event Model
- `PresalePurchaseRecorded`
- `PresaleClaimed`
- `PresalePaused`
- `PresaleFinalized`
- `AdminChanged`

### Upgradeability Policy
- existing deployed contract remains as-is unless formally migrated
- if mutable, no economic-rule changes without disclosure and timelock

---

## 6.2 FuzeBoardMigrationVault

### Purpose
Handle BOARD to FUZE migration claims.

### Allowed Functions
- register eligible migration allocations
- verify claims via mapping, Merkle root, or approved eligibility registry
- allow users to claim migrated FUZE
- enforce vesting if migration schedule applies
- finalize the migration after deadline
- redirect unclaimed balance only to predefined destination after deadline

### Forbidden Behaviors
- no arbitrary addition of fake claimants outside governance process
- no withdrawal to arbitrary wallets
- no early redirection of unclaimed tokens before deadline
- no silent extension of migration window without timelock and disclosure

### Admin Model
- governance multisig
- timelock for:
  - root updates
  - deadline changes
  - finalization destination changes
- emergency pause allowed

### Event Model
- `MigrationRootSet`
- `MigrationClaimed`
- `MigrationDeadlineUpdated`
- `MigrationFinalized`
- `UnclaimedTokensRedirected`

### Upgradeability Policy
- non-upgradeable preferred
- if upgradeable, only operational bugfixes, not allocation expansion or economic rewrites

---

## 6.3 FuzeTeamVestingVault

### Purpose
Hold and release team allocation under vesting rules.

### Allowed Functions
- create beneficiary schedules
- allocate tokens to named or approved team beneficiaries
- enforce cliff and linear vesting
- allow beneficiary claims
- revoke ungranted or explicitly revocable future grants if policy allows
- expose vesting status per beneficiary

### Forbidden Behaviors
- no unrestricted immediate withdrawal
- no arbitrary transfer of all team tokens to admin wallet
- no bypass of vesting schedule
- no hidden founder-only escape hatch

### Admin Model
- governance multisig
- optional vesting manager role for operational setup
- timelock for:
  - adding large allocations
  - changing vesting templates
  - changing revocation policy

### Event Model
- `TeamGrantCreated`
- `TeamGrantUpdated`
- `TeamTokensClaimed`
- `TeamGrantRevoked`
- `VestingTemplateUpdated`

### Upgradeability Policy
- non-upgradeable preferred after schedule initialization
- if upgradeable, vesting economics cannot be loosened without timelock and disclosure

---

## 6.4 FuzeFoundationVault

### Purpose
Permanently hold Foundation reserve and claim only stablecoin profit participation.

### Allowed Functions
- hold exactly the Foundation principal allocation
- connect to Stablecoin Profit Participation Contract
- claim stablecoin profit participation
- forward claimed stablecoin only to approved Foundation Operations Wallet
- expose total stablecoin claimed and current claimable balance

### Forbidden Behaviors
- no transfer of FUZE principal
- no approval of FUZE principal to any spender
- no use of principal as collateral
- no bridging, LP use, or operational redeployment of principal
- no arbitrary destination wallet for stablecoin withdrawal
- no unlock function for principal

### Admin Model
- Foundation Governance Council multisig
- timelock for:
  - changing Foundation Operations Wallet
  - changing connected profit participation contract address
- claim function may be public-callable if proceeds always go to fixed wallet

### Event Model
- `FoundationProfitClaimed`
- `FoundationOpsWalletUpdated`
- `ProfitParticipationContractUpdated`
- `FoundationPaused`
- `FoundationGovernanceUpdated`

### Upgradeability Policy
- strongly prefer non-upgradeable
- no upgrade path may unlock or move principal
- if any upgrade path exists, it must preserve the permanent principal lock invariant

---

## 6.5 FuzeTreasuryReserveVault

### Purpose
Hold long-term platform reserve for FUZE ecosystem development.

### Allowed Functions
- hold treasury reserve
- release tokens only to pre-approved deployment paths
- support category-based treasury deployment
- enforce timelocked treasury actions
- expose category budgets and historical usage

### Forbidden Behaviors
- no arbitrary direct transfer by a single signer
- no silent market sales
- no hidden OTC allocations
- no commingling with team or advisor allocations
- no withdrawals outside published categories

### Admin Model
- treasury multisig
- mandatory timelock
- optional budget-controller role
- optional emergency pause

### Event Model
- `TreasuryTransferQueued`
- `TreasuryTransferExecuted`
- `TreasuryCategoryBudgetSet`
- `TreasuryDestinationApproved`
- `TreasuryGovernanceUpdated`

### Upgradeability Policy
- carefully upgradeable if needed for treasury controls
- upgrades may not bypass timelock or category restrictions
- treasury policy hash should be public

---

## 6.6 FuzeHolderIncentivesVault

### Purpose
Distribute community and holder incentives programmatically.

### Allowed Functions
- fund reward campaigns
- allocate incentive budgets to approved reward modules
- stream or release rewards over time
- support claims by eligible users
- support referral, loyalty, or rank-based reward logic

### Forbidden Behaviors
- no manual dumping to arbitrary wallets
- no off-policy incentive issuance
- no unlimited inflation-like reward logic
- no single-admin bulk drain

### Admin Model
- incentives multisig or main governance multisig
- optional reward manager role
- timelock for major campaign budget changes

### Event Model
- `IncentiveCampaignCreated`
- `IncentiveBudgetAllocated`
- `IncentiveClaimed`
- `CampaignClosed`
- `RewardManagerUpdated`

### Upgradeability Policy
- carefully upgradeable if campaign mechanics evolve
- upgrade may not increase allocated amount
- upgrade may not bypass claim accounting

---

## 6.7 FuzeEcosystemPartnershipVault

### Purpose
Manage partnership and ecosystem-growth allocations.

### Allowed Functions
- create partner grants
- create milestone-based unlock schedules
- release allocations to approved partner wallets
- claw back expired or unaccepted grants if policy allows
- expose remaining and committed balances

### Forbidden Behaviors
- no direct free transfer to unknown wallets
- no immediate liquid dumping without milestone record
- no use for team compensation
- no hidden advisor grants through partnership bucket

### Admin Model
- ecosystem multisig
- optional grant manager role
- timelock for large grants or policy changes

### Event Model
- `PartnershipGrantCreated`
- `PartnershipMilestoneApproved`
- `PartnershipTokensReleased`
- `PartnershipGrantRevoked`
- `PartnerWalletApproved`

### Upgradeability Policy
- carefully upgradeable if grant model evolves
- may not be repurposed into team or treasury bucket without major governance process

---

## 6.8 FuzeLiquidityOperationsVault

### Purpose
Support market structure, exchange deployment, and liquidity operations.

### Allowed Functions
- allocate tokens to approved liquidity deployment contracts
- fund approved market-operation wallets
- support LP seeding and exchange-support actions
- enforce per-destination approvals and limits
- emit full event trail for every movement

### Forbidden Behaviors
- no discretionary dumping
- no personal transfers
- no hidden exchange deposits
- no usage outside explicitly approved liquidity and market-operation categories
- no commingling with treasury or incentives

### Admin Model
- operations multisig
- optional execution role for operational bots or designated deployer
- timelock for:
  - new destination wallets
  - large transfers
  - policy changes

### Event Model
- `LiquidityDestinationApproved`
- `LiquidityTransferQueued`
- `LiquidityTransferExecuted`
- `LiquidityPolicyUpdated`
- `OperationsExecutorUpdated`

### Upgradeability Policy
- limited upgradeability acceptable
- no upgrade may remove event logging or transfer controls

---

## 6.9 FuzeAdvisorVestingVault

### Purpose
Hold advisor and strategic contributor allocations under vesting.

### Allowed Functions
- create advisor vesting schedules
- release vested allocations
- revoke inactive or conditional grants if policy allows
- expose advisor claim status

### Forbidden Behaviors
- no unrestricted advisor token withdrawal
- no hidden insider routing through advisor bucket
- no reallocation to unrelated uses without governance process

### Admin Model
- governance multisig
- optional vesting manager
- timelock for grant policy changes

### Event Model
- `AdvisorGrantCreated`
- `AdvisorGrantUpdated`
- `AdvisorTokensClaimed`
- `AdvisorGrantRevoked`

### Upgradeability Policy
- same pattern as Team Vesting Vault
- preferably frozen after setup

---

## 6.10 FuzeTransparencyStabilityVault

### Purpose
Hold special reserve for transparency and stability functions.

### Allowed Functions
- deploy tokens only to approved stability or trust-preserving purposes
- reserve for governance-approved exceptional needs
- expose category-based accounting
- optionally route to designated stability modules if ever added by policy

### Forbidden Behaviors
- no general treasury use by default
- no founder or team compensation
- no undisclosed exchange deposits
- no discretionary drain to arbitrary wallets
- no overlap with liquidity or incentives without explicit governance policy

### Admin Model
- special-purpose multisig
- mandatory timelock
- stronger disclosure requirements than normal treasury

### Event Model
- `StabilityUseQueued`
- `StabilityUseExecuted`
- `StabilityCategoryApproved`
- `StabilityGovernanceUpdated`

### Upgradeability Policy
- conservative
- upgrades should be rare
- must preserve category restrictions and logging guarantees

---

## 7. Shared Admin Model

### 7.1 Governance Layers

The architecture SHOULD use three admin layers:

#### A. Master Governance Multisig
Controls high-level policy contracts and privileged role assignment.

#### B. Functional Multisigs
Separate multisigs for:
- Foundation
- Treasury
- Operations
- Incentives
- Ecosystem grants

#### C. Timelock Controller
Sits in front of sensitive admin actions.

### 7.2 Admin Requirements

Sensitive actions should require:
- multisig approval
- timelock delay
- public event emission

Sensitive actions include:
- changing destination wallets
- changing governance addresses
- changing vesting templates
- updating external connected contract addresses
- executing large treasury transfers
- changing claim roots or migration policy

---

## 8. Shared Event Model

All contracts SHOULD emit standardized events where applicable.

### Core Governance Events
- `GovernanceUpdated(address oldGov, address newGov)`
- `TimelockUpdated(address oldTimelock, address newTimelock)`
- `Paused(address actor)`
- `Unpaused(address actor)`

### Token Movement Events
- `TransferQueued(address token, address to, uint256 amount, bytes32 category)`
- `TransferExecuted(address token, address to, uint256 amount, bytes32 category)`

### Allocation Lifecycle Events
- `AllocationRegistered(address beneficiary, uint256 amount, bytes32 allocationType)`
- `AllocationClaimed(address beneficiary, uint256 amount, bytes32 allocationType)`
- `AllocationRevoked(address beneficiary, uint256 amount, bytes32 allocationType)`

### Policy Events
- `PolicyHashUpdated(bytes32 oldHash, bytes32 newHash)`
- `DestinationApproved(address destination, bytes32 category)`
- `DestinationRevoked(address destination, bytes32 category)`

### Foundation / Profit Events
- `ProfitParticipationContractUpdated(address oldAddr, address newAddr)`
- `StablecoinProfitClaimed(address token, uint256 amount, address destination)`

---

## 9. Upgradeability Policy

### 9.1 General Rule
Default to **non-upgradeable** unless there is a strong operational reason not to.

### 9.2 Contract Upgradeability Recommendations

#### Non-upgradeable preferred
- `FuzeFoundationVault`
- `FuzeBoardMigrationVault`
- `FuzeTeamVestingVault`
- `FuzeAdvisorVestingVault`

#### Carefully upgradeable if needed
- `FuzeTreasuryReserveVault`
- `FuzeHolderIncentivesVault`
- `FuzeEcosystemPartnershipVault`
- `FuzeLiquidityOperationsVault`
- `FuzeTransparencyStabilityVault`

### 9.3 Upgrade Constraints
If any contract is upgradeable:
- upgrade must be controlled by multisig and timelock
- upgrade events must be emitted
- upgrade cannot increase bucket allocation
- upgrade cannot create hidden principal-withdrawal paths
- upgrade cannot disable core event logging
- upgrade cannot bypass existing claim or vesting records

### 9.4 Economic Immutability Principle
Even if a contract is technically upgradeable, the following should be treated as economically immutable unless a major public governance process occurs:
- bucket size
- core bucket purpose
- Foundation principal lock
- vesting claims already earned
- migration claimant entitlements already recorded

---

## 10. Cross-Contract Dependencies

### Required Dependencies
- Foundation Vault ↔ Stablecoin Profit Participation Contract
- Presale Contract ↔ FUZE token
- Migration Vault ↔ eligibility registry or Merkle root
- Vesting Vaults ↔ FUZE token
- Treasury / Incentives / Liquidity / Partnership / Stability Vaults ↔ approved governance modules

### Dependency Rule
Any external contract address update must:
- be timelocked
- emit an event
- be queryable via public getter

---

## 11. Security and Invariants

### 11.1 Critical Invariants

#### Foundation Vault
- 35,000,000 FUZE principal can never leave
- only stablecoin profits may leave
- profit destination must be fixed or whitelisted

#### Team and Advisor Vesting
- claims cannot exceed allocated vesting amount
- unvested tokens cannot be claimed early

#### Migration Vault
- total claims cannot exceed 25,000,000 FUZE
- unclaimed amount cannot be redirected before deadline

#### Treasury / Liquidity / Stability Vaults
- transfers only to approved destinations
- transfers logged with category
- no single-signer control

### 11.2 Required Safeguards
- reentrancy protection
- role separation
- pausability only where operationally needed
- no hidden owner-only rescue of FUZE principal unless explicitly limited to accidental foreign-token recovery
- invariant testing for all critical flows

---

## 12. Canonical Summary Table

| Contract | Amount | Core Purpose | Preferred Upgradeability |
|---|---:|---|---|
| FuzeCommunityPresale | 110M | Presale claims and vesting | Existing |
| FuzeBoardMigrationVault | 25M | BOARD migration claims | Non-upgradeable |
| FuzeTeamVestingVault | 45M | Team vesting | Non-upgradeable |
| FuzeFoundationVault | 35M | Permanent Foundation principal + profit claims | Non-upgradeable |
| FuzeTreasuryReserveVault | 120M | Platform treasury reserve | Carefully upgradeable |
| FuzeHolderIncentivesVault | 55M | Holder and community incentives | Carefully upgradeable |
| FuzeEcosystemPartnershipVault | 40M | Partnerships and ecosystem grants | Carefully upgradeable |
| FuzeLiquidityOperationsVault | 30M | Liquidity and market operations | Carefully upgradeable |
| FuzeAdvisorVestingVault | 15M | Advisor vesting | Non-upgradeable |
| FuzeTransparencyStabilityVault | 25M | Trust and stability reserve | Carefully upgradeable |

---

## 13. Recommended Follow-Up Specifications

This master document should be followed by more specific documents for each critical contract, especially:

1. `foundation-vault.spec.md`
2. `treasury-reserve-vault.spec.md`
3. `stablecoin-profit-participation.spec.md`
4. `board-migration-vault.spec.md`
5. `team-vesting-vault.spec.md`
6. `fuze-allocation-wallet-map.md`

---

## 14. Canonical Architecture Statement

FUZE token allocation architecture is designed to be transparent, purpose-specific, and trust-minimized. Each major allocation is held in a dedicated smart contract with explicit permissions, explicit restrictions, observable events, and governance controls aligned to its purpose. The architecture is intended to support FUZE as a transparency-first SaaS ecosystem with strong holder trust and long-term on-chain accountability.
