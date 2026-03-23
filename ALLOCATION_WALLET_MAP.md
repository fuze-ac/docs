# ALLOCATION WALLET MAP

## 1. Purpose

This document defines the canonical wallet and contract map for all major FUZE token allocations.

Its purpose is to provide a clear, public, and auditable reference showing:
- which allocation bucket exists
- which smart contract or wallet is intended to hold it
- the token amount assigned to that bucket
- the purpose of that bucket
- whether the bucket is locked, vested, claim-based, or operational
- how the bucket relates to governance, transparency, and profit participation

This document is intended to work together with:
- `FUZE_TOKEN_CONTRACT_ARCHITECTURE_SPEC.md`
- `foundation-vault.spec.md`
- `TREASURY_RESERVE_VAULT_SPEC.md`
- `STABLECOIN_PROFIT_PARTICIPATION_SPEC.md`

---

## 2. Canonical Principles

The FUZE allocation map follows these principles:

1. Each major allocation must be assigned to a dedicated contract or clearly defined wallet.
2. Each allocation must have a distinct purpose.
3. High-trust allocations should prefer smart contracts over plain wallets.
4. Every governance-sensitive address should be publicly identifiable.
5. No hidden omnibus wallet should hold unrelated major allocations.
6. Every operational or treasury movement should be explainable by the published policy.
7. Public holders should be able to understand the allocation structure without needing internal context.

---

## 3. Master Allocation Summary

| Allocation Bucket | Amount | Holder Type | Canonical Holder | Primary Purpose |
|---|---:|---|---|---|
| Community Presale | 110,000,000 FUZE | Smart contract | `FuzeCommunityPresale` | Presale purchase, vesting, and user claims |
| BOARD Migration | 25,000,000 FUZE | Smart contract | `FuzeBoardMigrationVault` | BOARD-to-FUZE migration claims |
| Team Allocation | 45,000,000 FUZE | Smart contract | `FuzeTeamVestingVault` | Team, founder, core builders, and future key hires under vesting |
| Foundation Reserve | 35,000,000 FUZE | Smart contract | `FuzeFoundationVault` | Permanently locked Foundation principal with profit participation only |
| Platform Treasury Reserve | 120,000,000 FUZE | Smart contract | `FuzeTreasuryReserveVault` | Long-term platform treasury reserve |
| Community / Holder Incentives | 55,000,000 FUZE | Smart contract | `FuzeHolderIncentivesVault` | Holder rewards, campaigns, referrals, loyalty, and ecosystem activation |
| Ecosystem Growth & Partnerships | 40,000,000 FUZE | Smart contract | `FuzeEcosystemPartnershipVault` | Partnerships, ecosystem deals, grants, and milestone-based releases |
| Liquidity & Market Operations | 30,000,000 FUZE | Smart contract | `FuzeLiquidityOperationsVault` | Liquidity seeding, market operations, and exchange support |
| Advisors / Strategic Contributors | 15,000,000 FUZE | Smart contract | `FuzeAdvisorVestingVault` | Advisor and strategic contributor vesting |
| Transparency / Stability Reserve | 25,000,000 FUZE | Smart contract | `FuzeTransparencyStabilityVault` | Transparency, trust, and stability-related reserve actions |

**Total Supply:** `500,000,000 FUZE`

---

## 4. Wallet and Contract Map by Allocation

## 4.1 Community Presale

### Canonical Holder
- **Contract / Wallet Name:** `FuzeCommunityPresale`
- **Holder Type:** smart contract
- **Allocation Amount:** `110,000,000 FUZE`

### Current Status
- This allocation is already associated with the deployed Community Presale contract.
- Known reference discussed in planning: `0xfa5a469e273cfbd671ae61ab6a60dc0dae7f2d7b`

### Purpose
- manage presale participation
- manage vesting and claims
- act as the public launch distribution contract

### Classification
- claim-based
- vesting-based
- public allocation

### Notes
This bucket is distinct from all other allocations and should not be reused for treasury, operations, or private insider purposes.

---

## 4.2 BOARD Migration

### Canonical Holder
- **Contract / Wallet Name:** `FuzeBoardMigrationVault`
- **Holder Type:** smart contract
- **Allocation Amount:** `25,000,000 FUZE`

### Purpose
- support BOARD-to-FUZE migration claims
- enforce migration window and migration logic
- redirect unclaimed tokens only according to published policy after deadline

### Classification
- claim-based
- migration reserve
- time-sensitive distribution contract

### Notes
This contract should not operate as general treasury. It is a dedicated migration pool only.

---

## 4.3 Team Allocation

### Canonical Holder
- **Contract / Wallet Name:** `FuzeTeamVestingVault`
- **Holder Type:** smart contract
- **Allocation Amount:** `45,000,000 FUZE`

### Purpose
- hold allocation for founder, core team, future key hires, and long-term builders
- enforce vesting schedules and claims

### Classification
- vesting-based
- insider allocation
- builder incentive pool

### Notes
This bucket should remain distinct from treasury and foundation assets.

---

## 4.4 Foundation Reserve

### Canonical Holder
- **Contract / Wallet Name:** `FuzeFoundationVault`
- **Holder Type:** smart contract
- **Allocation Amount:** `35,000,000 FUZE`

### Purpose
- permanently hold Foundation principal
- participate only through stablecoin profit participation
- never sell, transfer, or operationally deploy the FUZE principal

### Classification
- permanently locked principal
- stewardship reserve
- profit-participation eligible

### Notes
This is one of the most important trust-signaling allocations in the FUZE system.

The Foundation principal should remain permanently visible in the contract balance. The Foundation may receive stablecoin proceeds from the Stablecoin Profit Participation Contract and route them to the approved Foundation Operations Wallet.

---

## 4.5 Platform Treasury Reserve

### Canonical Holder
- **Contract / Wallet Name:** `FuzeTreasuryReserveVault`
- **Holder Type:** smart contract
- **Allocation Amount:** `120,000,000 FUZE`

### Purpose
- hold long-term platform treasury reserve
- support governance-approved strategic deployments
- support category-based treasury actions

### Classification
- governance-controlled reserve
- not permanently locked
- timelocked operational reserve

### Notes
This bucket should be heavily governed and should never appear as a plain personal or hot wallet balance.

---

## 4.6 Community / Holder Incentives

### Canonical Holder
- **Contract / Wallet Name:** `FuzeHolderIncentivesVault`
- **Holder Type:** smart contract
- **Allocation Amount:** `55,000,000 FUZE`

### Purpose
- support holder incentives
- support campaigns, loyalty rewards, referrals, activation, and ecosystem participation

### Classification
- programmatic incentives reserve
- campaign-driven distribution vault

### Notes
This bucket should be formula-based and policy-restricted wherever possible.

---

## 4.7 Ecosystem Growth & Partnerships

### Canonical Holder
- **Contract / Wallet Name:** `FuzeEcosystemPartnershipVault`
- **Holder Type:** smart contract
- **Allocation Amount:** `40,000,000 FUZE`

### Purpose
- support partnership grants
- support ecosystem integrations
- support milestone-based ecosystem growth deals

### Classification
- grant / partnership vault
- milestone-based release vault

### Notes
This allocation should not be used as a disguised advisor, treasury, or team bucket.

---

## 4.8 Liquidity & Market Operations

### Canonical Holder
- **Contract / Wallet Name:** `FuzeLiquidityOperationsVault`
- **Holder Type:** smart contract
- **Allocation Amount:** `30,000,000 FUZE`

### Purpose
- support market-making operations
- support LP seeding and exchange support actions
- support controlled liquidity deployment

### Classification
- operational market structure vault
- high-sensitivity operational bucket

### Notes
This bucket requires strong controls and public event traceability because market operations are sensitive for holder trust.

---

## 4.9 Advisors / Strategic Contributors

### Canonical Holder
- **Contract / Wallet Name:** `FuzeAdvisorVestingVault`
- **Holder Type:** smart contract
- **Allocation Amount:** `15,000,000 FUZE`

### Purpose
- hold advisor and strategic contributor vesting allocations

### Classification
- vesting-based
- contributor reward bucket

### Notes
This should remain separate from team, ecosystem grants, and treasury allocations.

---

## 4.10 Transparency / Stability Reserve

### Canonical Holder
- **Contract / Wallet Name:** `FuzeTransparencyStabilityVault`
- **Holder Type:** smart contract
- **Allocation Amount:** `25,000,000 FUZE`

### Purpose
- support transparency, trust, and stability-related reserve actions under published policy

### Classification
- governance-controlled special-purpose reserve
- trust and stability bucket

### Notes
This bucket should be used conservatively and only under clearly published rules.

---

## 5. Governance and Operations Wallet Layer

In addition to the main allocation contracts, the FUZE system is expected to include governance and operational wallets that do **not** themselves hold the major allocation principals as primary storage.

These supporting addresses may include:

### 5.1 Governance Multisigs
- Master Governance Multisig
- Foundation Governance Multisig
- Treasury Governance Multisig
- Operations Governance Multisig
- Incentives Governance Multisig

### 5.2 Timelock Controllers
- protocol-level timelock controller
- vault-specific timelock controller where applicable

### 5.3 Operational Destination Wallets
- Foundation Operations Wallet
- approved treasury destination wallets
- approved liquidity destination wallets
- approved partnership recipient wallets

These addresses should be published separately in a live operational wallet registry once deployed.

---

## 6. Recommended Live Wallet Registry Structure

Once mainnet deployment is complete, FUZE should publish a live registry with fields like:

| Label | Address | Type | Controlled By | Purpose | Public? |
|---|---|---|---|---|---|
| Community Presale Contract | `<address>` | Smart contract | Governance | Presale claim and vesting | Yes |
| Board Migration Vault | `<address>` | Smart contract | Governance | Migration claims | Yes |
| Team Vesting Vault | `<address>` | Smart contract | Governance | Team vesting | Yes |
| Foundation Vault | `<address>` | Smart contract | Foundation governance | Locked principal | Yes |
| Treasury Reserve Vault | `<address>` | Smart contract | Treasury governance | Strategic reserve | Yes |
| Holder Incentives Vault | `<address>` | Smart contract | Incentives governance | Rewards and campaigns | Yes |
| Ecosystem Partnership Vault | `<address>` | Smart contract | Governance | Partnerships | Yes |
| Liquidity Operations Vault | `<address>` | Smart contract | Operations governance | Liquidity operations | Yes |
| Advisor Vesting Vault | `<address>` | Smart contract | Governance | Advisor vesting | Yes |
| Transparency Stability Vault | `<address>` | Smart contract | Governance | Stability reserve | Yes |
| Foundation Ops Wallet | `<address>` | Wallet / multisig | Foundation governance | Stablecoin proceeds operations | Yes |
| Master Governance Multisig | `<address>` | Multisig | Authorized signers | Master governance | Yes |

This registry should be updated when addresses are first deployed and whenever a governance-approved address change occurs.

---

## 7. Recommended Public Labels

For public transparency, each main address should have a stable public label in dashboards, docs, and explorers.

Recommended labels:
- FUZE Community Presale Contract
- FUZE BOARD Migration Vault
- FUZE Team Vesting Vault
- FUZE Foundation Vault
- FUZE Treasury Reserve Vault
- FUZE Holder Incentives Vault
- FUZE Ecosystem Partnership Vault
- FUZE Liquidity Operations Vault
- FUZE Advisor Vesting Vault
- FUZE Transparency Stability Vault
- FUZE Foundation Operations Wallet
- FUZE Governance Multisig

---

## 8. Profit Participation Map

The wallet map also affects stablecoin profit participation.

### Eligible by Design or Policy
Potential eligible holders may include:
- regular eligible holder wallets
- Foundation Vault
- any other address explicitly included under the published holder policy

### Typically Excluded or Policy-Dependent
The following should be explicitly classified by published holder policy and should not be left ambiguous:
- Treasury Reserve Vault
- Liquidity Operations Vault
- Team Vesting Vault
- Advisor Vesting Vault
- unclaimed migration pools
- undistributed incentive pools

This classification should be published as part of the quarterly transparency process.

---

## 9. Allocation State Categories

Each canonical allocation should be understood as belonging to one of these state categories:

| Allocation | State Category |
|---|---|
| Community Presale | Claim + vesting distribution |
| BOARD Migration | Claim + migration distribution |
| Team Allocation | Vesting |
| Foundation Reserve | Permanently locked |
| Platform Treasury Reserve | Governed reserve |
| Community / Holder Incentives | Programmatic incentive reserve |
| Ecosystem Growth & Partnerships | Milestone grant reserve |
| Liquidity & Market Operations | Operational reserve |
| Advisors / Strategic Contributors | Vesting |
| Transparency / Stability Reserve | Special-purpose governed reserve |

This categorization helps define what each address is allowed to do and what holders should expect from it.

---

## 10. Canonical Deployment Order Recommendation

A practical deployment order for the live wallet map is:

1. FUZE token contract (if not already finalized)
2. Community Presale Contract verification
3. BOARD Migration Vault
4. Team Vesting Vault
5. Foundation Vault
6. Treasury Reserve Vault
7. Stablecoin Profit Participation Contract
8. Holder Incentives Vault
9. Ecosystem Partnership Vault
10. Liquidity Operations Vault
11. Advisor Vesting Vault
12. Transparency Stability Vault
13. Governance multisigs and operational registry publication

This order supports public trust by prioritizing high-significance contracts early.

---

## 11. Canonical Summary

### Core Rule
All major FUZE token allocations should live in dedicated, publicly labeled smart contracts rather than hidden omnibus wallets.

### Foundation Rule
The Foundation Reserve must remain visible as permanently locked principal in `FuzeFoundationVault`.

### Treasury Rule
Treasury assets must remain separated from vesting, liquidity, and incentive allocations.

### Wallet Registry Rule
All governance-significant wallets and contracts should be published in a live registry after deployment.

---

## 12. Canonical Policy Statement

The FUZE Allocation Wallet Map defines the canonical storage and governance locations for every major FUZE token allocation. Each allocation is assigned to a dedicated smart contract or clearly defined wallet structure with a distinct purpose, distinct policy, and distinct transparency expectations. This map exists to ensure that holders, contributors, and ecosystem participants can understand where each major allocation lives, why it exists, and how it is governed.
