# FUZE CHAIN ARCHITECTURE
## 1. Purpose

This specification defines the chain architecture of the FUZE ecosystem.

Its purpose is to establish the canonical role of each chain used by FUZE, define how the main token layer connects with the platform-commerce layer and the stablecoin payout layer, and make the system understandable for product, token, treasury, and transparency design.

FUZE is intentionally designed as a multi-layer ecosystem rather than a single-chain system. This is because different parts of the platform have different requirements:
- the FUZE token requires a credible canonical token layer
- platform credits require fast, cheap, high-frequency transaction support
- stablecoin profit participation requires efficient claim flows and transparent payout cycles

This document defines how those layers fit together.

---

## 2. Canonical Chain Decision

The FUZE chain model is:

### 2.1 Ethereum Mainnet
**FUZE token stays on Ethereum mainnet**.

### 2.2 Base
**FUZE Platform Credits run on Base**.

### 2.3 Base
**Stablecoin profit participation runs on Base**, using Ethereum FUZE-holder snapshots as the eligibility source.

This is the canonical chain architecture for FUZE unless formally changed by a future governance or architecture decision.

---

## 3. Why FUZE Uses Multiple Layers

FUZE uses multiple chain layers because the platform has three different economic and operational domains:

### 3.1 Token Truth Domain
The canonical FUZE token should live where token identity, holder balances, and long-term trust are strongest.

### 3.2 Platform Commerce Domain
Product usage, subscriptions, credits, and consumption-ledger activity require low fees, fast confirmations, and high operational throughput.

### 3.3 Profit Distribution Domain
Stablecoin profit participation should be cheap enough for practical claiming and cycle-based payouts, while still remaining clearly linked to the canonical FUZE holder base.

Trying to force all three domains into one chain would create unnecessary tradeoffs.

---

## 4. Layer Roles

## 4.1 Ethereum Mainnet Layer

### Canonical Role
Ethereum mainnet is the **canonical token layer** of FUZE.

### Ethereum Responsibilities
Ethereum mainnet is the source of truth for:
- FUZE token contract
- holder balances
- token identity
- holder rank inputs where applicable
- snapshot-based holder eligibility for profit participation
- long-term token credibility and ecosystem anchor

### Ethereum Non-Goals
Ethereum mainnet is **not** the preferred layer for:
- high-frequency platform credit updates
- subscriptions and product consumption ledgers
- frequent micro-spend product actions
- low-cost user claim activity at scale

### Architectural Meaning
Ethereum answers the question:

> **Who holds FUZE?**

It is not the main answer to:
- who has credits
- who spent credits
- who can make cheap repeated product actions

---

## 4.2 Base Layer for Platform Credits

### Canonical Role
Base is the **operational product-commerce layer** of FUZE.

### Base Credit Responsibilities
Base is the source of truth for:
- FUZE Platform Credits ledger
- credit issuance after verified payment
- credit balances
- subscriptions
- usage billing
- premium feature unlocks
- add-ons
- product-level spending
- refunds and reversals
- credit expiry where applicable
- workspace and account-based credit balances

### Why Base
Base is selected because the platform credits layer needs:
- cheap gas
- fast confirmation
- support for many small ledger actions
- better user experience for app activity

### Architectural Meaning
Base answers the question:

> **What can the user spend inside FUZE products right now?**

---

## 4.3 Base Layer for Stablecoin Profit Participation

### Canonical Role
Base is also the **profit-participation execution layer** of FUZE.

### Base Payout Responsibilities
Base is the source of truth for:
- `FuzeStablecoinProfitParticipation`
- stablecoin payout cycle funding
- cycle claim logic
- cycle-based payout records
- holder claim execution
- Foundation Vault claim participation if included under holder policy

### Why Base for Payouts
Stablecoin profit participation is placed on Base because:
- claim gas should be low enough for regular holders
- payout cycles should be practical at scale
- Base aligns operationally with the credits layer
- Base provides a more usable environment for frequent claim interactions than Ethereum mainnet

### Architectural Meaning
Base answers the question:

> **How do eligible FUZE holders actually claim stablecoin profit participation?**

---

## 5. Asset Map by Chain

| Layer | Chain | Canonical Asset / System | Primary Role |
|---|---|---|---|
| Token Layer | Ethereum mainnet | FUZE token | Canonical token truth and holder eligibility source |
| Commerce Layer | Base | FUZE Platform Credits | Internal platform consumption ledger |
| Profit Distribution Layer | Base | Stablecoin Profit Participation | Stablecoin payout execution and claims |

---

## 6. Core Architectural Principle

The most important rule is:

> **FUZE token, FUZE credits, and stablecoin profit participation are connected, but they are not the same asset and must not be merged conceptually.**

### 6.1 FUZE Token
- lives on Ethereum
- is the ecosystem participation token
- is used for holder status, eligibility, and platform-level token utility

### 6.2 FUZE Platform Credits
- live on Base
- are internal platform spending units
- are account-bound / workspace-bound
- are used for subscriptions, usage, and feature access

### 6.3 Stablecoin Profit Participation
- runs on Base
- distributes approved stablecoin payout cycles
- uses Ethereum holder snapshots as eligibility input

---

## 7. Connection Between Layers

The layers are connected by policy, verification, snapshots, treasury settlement, and published transparency processes.

They are **not** connected by naive 1:1 asset conversion.

---

## 8. Payment to Credits Flow

The payment-to-credits flow is:

1. user pays through an approved payment rail
2. payment is verified off-chain
3. payment value is normalized under policy
4. credits are issued on Base
5. credits are spent across FUZE products

### Supported payment rails
- fiat / Stripe
- USDT / stablecoins
- FUZE token
- Telegram Stars
- Apple In-App Purchase
- Google Play Billing

### Important rule
Payments are external input rails.
Credits are the unified internal consumption unit.

This means:

> **payment rail -> verified payment -> credits on Base**

---

## 9. Credits to Profit Participation Relationship

Credits do not directly become stablecoin profit participation payouts.

### Correct relationship
1. payments are verified
2. credits are issued on Base
3. users spend credits across products
4. revenue is reconciled off-chain
5. costs are deducted under policy
6. distributable profit is determined
7. stablecoin payout pool is funded on Base
8. eligible Ethereum FUZE holders claim on Base

### Important rule
A sold credit is not automatically profit.
Credits belong to the consumption layer.
Profit belongs to accounting and treasury settlement.

---

## 10. Ethereum Snapshot Model

### 10.1 Snapshot Role
Ethereum FUZE balances are used as the eligibility source for profit participation.

### 10.2 Snapshot Responsibilities
The snapshot process should determine:
- eligible holder addresses
- excluded wallets
- holder balances at the relevant snapshot point
- any policy-based rank or duration adjustments if adopted
- Foundation inclusion or exclusion based on policy

### 10.3 Excluded or Policy-Dependent Wallet Types
The published policy should explicitly define treatment for:
- Treasury Reserve Vault
- Team Vesting Vault
- Advisor Vesting Vault
- Liquidity Operations Vault
- undistributed incentive pools
- unclaimed migration pools
- Foundation Vault if applicable

### 10.4 Output
The snapshot output becomes the basis for the payout dataset used on Base.

---

## 11. Profit Participation Funding Flow

The stablecoin payout cycle should work as follows:

1. treasury and accounting finalize distributable profit
2. Ethereum snapshot determines eligible FUZE holder dataset
3. entitlement dataset is prepared
4. payout cycle is funded in stablecoin on Base
5. `FuzeStablecoinProfitParticipation` opens the claim cycle
6. eligible holders claim stablecoin on Base

This creates a clear cross-chain model:
- **Ethereum for eligibility truth**
- **Base for stablecoin payout execution**

---

## 12. Foundation Integration

`FuzeFoundationVault` is a special-case governance and stewardship contract, but its eligibility in stablecoin profit participation should still be governed by the published holder policy.

If included, the flow is:
- Foundation exists as a holder address or included entitlement address
- payout entitlement is computed under the same cycle rules
- claim is executed through Foundation Vault logic on Base if designed that way

The Foundation should not require a separate economic model from the rest of the payout architecture.

---

## 13. Treasury and Settlement Layer

The chain architecture must preserve a clear treasury and settlement boundary.

### Treasury responsibilities
Treasury and accounting are responsible for:
- payment settlement
- revenue reconciliation
- cost recognition
- distributable profit determination
- stablecoin funding of payout cycles

### Chain responsibilities
The chains are responsible for:
- token truth
- credit truth
- payout execution truth

This means the chain architecture supports transparency, but does not replace accounting.

---

## 14. Why This Architecture Is Strong

This architecture creates a clean separation of concerns.

### 14.1 Ethereum gives token credibility
FUZE token remains on the strongest canonical token layer.

### 14.2 Base gives product usability
Credits and spending happen where gas is cheap and UX is practical.

### 14.3 Base gives cheaper payout UX
Stablecoin claims become realistic for a broader holder base.

### 14.4 Cross-layer logic stays understandable
- token truth is on Ethereum
- product spending is on Base
- stablecoin claims are on Base
- accounting bridges the commercial reality between them

---

## 15. Non-Goals and Boundaries

The FUZE chain architecture MUST NOT imply any of the following:

### 15.1 No assumption that credits are public trade assets
Credits are not meant to be a freely tradable market token.

### 15.2 No assumption that all paid value is immediately profit
Credit purchases do not directly or automatically become distributable stablecoin payouts.

### 15.3 No assumption that Base credits replace Ethereum FUZE
Credits and FUZE are different assets with different purposes.

### 15.4 No assumption that snapshot policy can remain vague
The Ethereum snapshot and exclusion policy must be explicit and published.

---

## 16. Recommended Cross-Chain Services

FUZE should eventually operate with a clear internal service layer that connects Ethereum and Base.

Recommended services include:

### 16.1 Payment Verification Service
Verifies incoming payment rails and triggers credit issuance.

### 16.2 Credits Issuance and Reconciliation Service
Converts verified payment value into Base credits and records accounting references.

### 16.3 Ethereum Snapshot Service
Computes payout eligibility and exclusion logic for FUZE holders.

### 16.4 Profit Dataset Builder
Builds finalized cycle entitlements for `FuzeStablecoinProfitParticipation`.

### 16.5 Treasury Funding Service
Funds stablecoin payout cycles on Base after policy approval.

---

## 17. Security and Trust Principles

The chain architecture should preserve the following trust principles:

1. Ethereum remains the canonical token truth.
2. Credits remain separate from public token ownership.
3. Stablecoin payout contracts remain fully funded per cycle before opening where practical.
4. Snapshot rules remain published and auditable.
5. Cross-chain logic is visible through policy, event logs, and transparency reports.
6. No hidden wallet-based shortcuts should replace the documented chain roles.

---

## 18. Recommended Public Explanation

The best simplified public explanation is:

> **FUZE uses Ethereum as its canonical token layer and Base as its operational platform layer. The FUZE token remains on Ethereum, while platform credits and stablecoin profit participation run on Base. Ethereum holder balances are used for eligibility snapshots, and Base is used for fast, low-cost credits, subscriptions, usage billing, and stablecoin payout claims.**

---

## 19. Canonical Summary

| Field | Value |
|---|---|
| Canonical Token Chain | Ethereum mainnet |
| Platform Credits Chain | Base |
| Stablecoin Profit Participation Chain | Base |
| Eligibility Source for Profit Participation | Ethereum FUZE-holder snapshots |
| Credits Asset Type | Internal consumption unit |
| Profit Participation Asset Type | Stablecoin payout entitlement |
| Core Design Principle | Separate token truth, commerce truth, and payout execution truth |

---

## 20. Canonical Policy Statement

FUZE uses a layered chain architecture in which Ethereum mainnet serves as the canonical FUZE token and holder-eligibility layer, while Base serves as the operational platform layer for credits and stablecoin profit participation. The FUZE token remains the ecosystem participation asset on Ethereum, Platform Credits act as the internal consumption ledger on Base, and stablecoin profit participation is funded and claimed on Base using Ethereum holder snapshots as the eligibility source. This design allows FUZE to combine token credibility, low-cost product usage, and practical payout execution within one transparent ecosystem.
