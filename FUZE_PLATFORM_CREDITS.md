# FUZE PLATFORM CREDITS

## 1. Purpose

This specification defines the FUZE Platform Credits architecture and the core contract/system requirements for the FUZE on-chain credits layer.

FUZE Platform Credits are the unified internal consumption unit of the FUZE ecosystem. They are designed to let users pay through multiple payment rails, receive a normalized credit balance, and spend those credits across FUZE products through a shared on-chain credit ledger.

The Platform Credits system is intended to:
- unify commerce across all FUZE products
- separate external payment rails from internal product spending
- provide transparent, secure, and trackable credit issuance and spending
- support subscriptions, usage billing, feature unlocks, and platform services
- operate on a fast, low-cost chain for high-frequency application activity

---

## 2. Chain Architecture Context

The FUZE chain model is:

- **FUZE token stays on Ethereum mainnet** as the canonical token layer
- **FUZE Platform Credits run on Base** as the operational credits layer
- **Stablecoin profit participation runs on Base**, using Ethereum FUZE-holder snapshots as the eligibility source

This specification covers the Platform Credits layer on Base.

---

## 3. What a Credit Is

A **FUZE Platform Credit** is the internal spending unit of the FUZE ecosystem.

A credit is:
- a platform consumption unit
- recorded in a shared on-chain credit ledger
- usable across FUZE products according to entitlement and pricing rules
- account-bound to a user account or workspace account
- non-equity, non-governance, and non-profit-participation in nature

A credit is **not**:
- the FUZE token itself
- a freely tradable public token
- an ownership unit
- a dividend / profit-right unit

Credits represent **platform purchasing power** inside the FUZE ecosystem.

---

## 4. Product Scope

Platform Credits should be usable across all FUZE products, including:

- **QTB — Quant AI Trade Brain**
- **AIMM — AI Market Maker**
- **ZAGA — Token Utility OS**
- **AIE — Event Intelligence**
- **HerHelp — AI-assisted sheet-to-app SaaS for SMEs**
- **Botmad — AI desktop employee**

Credits may be used for:
- subscriptions
- usage billing
- AI actions
- premium features
- add-ons
- feature unlocks
- reports
- automation runs
- seat packages
- plan renewals

---

## 5. Core Design Objectives

The FUZE Platform Credits system MUST satisfy the following objectives:

1. Support multi-rail payment inputs.
2. Normalize payment value into one shared internal credit unit.
3. Record issuance, spend, refund, expiry, and adjustment activity on a shared on-chain ledger.
4. Keep credits account-bound or workspace-bound rather than freely transferable.
5. Support product-specific or ecosystem-wide usage.
6. Provide role-controlled issuance and reversal paths.
7. Keep clear separation between credits, revenue accounting, and stablecoin profit participation.
8. Make all major credit events transparent, secure, and trackable.

---

## 6. Multi-Rail Payment Inputs

The Platform Credits system MUST support payment verification and credit issuance from the following payment rails:

- fiat / Stripe
- USDT / stablecoins
- FUZE token
- Telegram Stars
- Apple In-App Purchase
- Google Play Billing

The payment rails themselves are external inputs.

The Platform Credits system should treat them as:
- verified payment sources
- normalized-value inputs
- sources of credit issuance

The payment asset is not the same thing as the credit asset.

---

## 7. Why Payment -> Credit -> On-Chain

FUZE uses the model:

> **payment rail -> verified payment -> platform credits -> on-chain ledger**

This exists for three main reasons:

### 7.1 Transparency
- credit issuance and spending become visible and auditable
- product balances are not hidden inside fragmented internal databases

### 7.2 Security
- one shared ledger is safer than disconnected product-specific balances
- role-controlled issuance and reversal rules reduce operational ambiguity

### 7.3 Trackability
- top-ups, spends, refunds, bonus credits, and unlocks can all be tracked consistently
- credit movements can be reconciled with revenue and product usage

---

## 8. Credit Ledger Chain

### Canonical Credit Chain

The Platform Credits ledger MUST be deployed on:

> **Base**

### Reasoning
Base is used because the credits layer needs:
- low gas fees
- fast confirmations
- support for frequent application writes
- better UX for subscriptions, usage billing, and product consumption

Ethereum mainnet is not the preferred chain for credits because credits are an operational consumption ledger, not the canonical token layer.

---

## 9. Credit Classes

The Platform Credits system SHOULD support at least the following credit classes.

### 9.1 Paid Credits
Credits issued after verified payment.

Properties:
- non-expiring by default
- account-bound or workspace-bound
- broadest allowed usage within policy
- highest trust class

### 9.2 Bonus Credits
Credits issued through promotional, referral, loyalty, or support pathways.

Properties:
- may expire
- may have limited scope or spend priority
- issued only through approved programs or roles

### 9.3 Restricted Credits
Credits issued for limited use cases.

Properties:
- may be product-specific
- may be campaign-specific
- may have expiry
- may have limited transfer or spend contexts within the same account/workspace

---

## 10. Mint / Issue Rules

Credits MUST NOT be freely mintable by arbitrary admin action.

Credits may be issued only through defined issuance paths.

### 10.1 Paid Issuance
Credits may be issued when a verified payment is completed through an approved payment rail.

Flow:
1. payment is verified off-chain
2. payment value is normalized
3. conversion policy is applied
4. credits are issued to the user or workspace on Base
5. issuance is recorded in the ledger

### 10.2 Reward Issuance
Credits may be issued through approved non-payment paths such as:
- promotions
- referrals
- loyalty rewards
- ecosystem campaigns
- customer support compensation
- service recovery adjustments

Reward issuance must be:
- policy-defined
- role-restricted
- reason-coded
- event-emitting

### 10.3 Manual Adjustment Issuance
Credits may be issued manually only for narrow operational reasons such as:
- correction of platform error
- enterprise invoice settlement adjustment
- customer support resolution
- fraud recovery correction

This path should be rare and highly logged.

### 10.4 No Arbitrary Infinite Mint
The system MUST include:
- issuer-role controls
- issuance reason codes
- event trail
- policy-based issuance boundaries where needed

---

## 11. Conversion Engine

External payment value must be converted into credits using a defined conversion engine.

The conversion engine SHOULD support:
- payment rail identification
- gross payment amount
- fee-aware normalization
- promotional bonus rules
- FUZE-payment enhanced conversion rules if policy allows
- product or channel-specific adjustments

Example conceptual model:
- fiat / Stripe -> standard credit rate
- USDT / stablecoins -> standard credit rate
- FUZE token -> enhanced or bonus credit rate if approved
- Telegram Stars / Apple / Google -> channel-adjusted credit rate

The conversion engine should be part of the verified issuance path, not an arbitrary manual calculation.

---

## 12. Spend Rules

Credits may be spent only on approved product or platform actions.

### 12.1 Allowed Spend Types
Credits may be spent for:
- subscription activation
- plan renewal
- usage billing
- AI actions
- reports
- premium feature unlocks
- add-ons
- automation runs
- workspace or seat entitlements

### 12.2 Spend Validation
Every spend MUST verify:
- sufficient balance
- allowed credit class usage
- product pricing rule
- entitlement context
- account or workspace ownership

### 12.3 Spend Accounting
Every spend MUST:
- deduct from the appropriate balance
- update ledger state
- emit event
- be traceable to product, action, or billing reason

### 12.4 Spend Priority
The system MAY support spend-priority rules, such as:
1. expiring promotional credits first
2. bonus credits second
3. paid credits last

If implemented, spend priority rules must be visible and deterministic.

---

## 13. Refund Rules

Refund handling must distinguish between payment refunds and credit reversals.

### 13.1 Unused Paid Credits
If a valid refund occurs before paid credits are spent, the corresponding unused credits may be reversed or burned.

### 13.2 Partially Used Balances
If credits have been partially spent, only the unused portion should normally be eligible for credit reversal tied to payment refund.

### 13.3 Channel Refunds
For Apple, Google, and Telegram Stars:
- channel refund and revocation rules must be respected
- verified refund or revocation events must trigger corresponding unused-credit adjustment logic

### 13.4 Support Replacement Credits
The platform may issue replacement credits as goodwill or support compensation. This is not the same as refunding the original payment rail.

### 13.5 Fraud / Chargeback Handling
If payment is reversed through chargeback or fraud path:
- unused credits should be removed or frozen
- already-spent balances may require account restriction or negative-balance handling

---

## 14. Expiry Rules

### 14.1 Paid Credits

> **Paid credits should be non-expiring by default.**

This supports trust, better UX, and stronger platform credibility.

### 14.2 Bonus Credits
Bonus credits may expire.

If so, the expiry rules must be:
- explicit
- recorded in metadata or class policy
- visible to the user

### 14.3 Restricted Credits
Restricted credits may be expiring or non-expiring depending on policy.

Their restrictions must be visible and enforceable.

---

## 15. Transferability Rules

### 15.1 Default Rule

> **FUZE Platform Credits should be account-bound, not freely transferable.**

Credits are internal consumption units, not open-market assets.

### 15.2 Allowed Ownership Scope
Credits may be attached to:
- a personal user account
- a workspace or organization account

### 15.3 Controlled Internal Transfers
The system MAY support controlled internal transfer patterns such as:
- user -> workspace balance migration
- workspace sub-balance allocation
- support-approved migration between accounts
- enterprise billing ownership adjustments

These are not public free-market transfers.

### 15.4 Forbidden Transfer Model
Credits should not be freely tradable on the open market and should not behave like unrestricted ERC-20 assets.

---

## 16. Revenue Separation Principle

Credits are not profit.

A sold credit does **not** automatically equal distributable profit.

This is because revenue still depends on:
- payment rail fees
- app store fees
- Stars economics
- refunds
- support costs
- AI costs
- infrastructure costs
- operational expenses
- accounting recognition rules

Therefore:
- **credits belong to the platform consumption ledger**
- **profit belongs to the accounting and treasury settlement layer**

Only after accounting closes can stablecoin profit participation be funded.

---

## 17. Relationship to FuzeStablecoinProfitParticipation

The Platform Credits ledger and `FuzeStablecoinProfitParticipation` are connected by accounting and treasury settlement, not by direct 1:1 credit conversion.

### Correct relationship
1. verified payments create credits
2. credits are spent in products
3. accounting reconciles revenue and costs
4. distributable profit is determined under policy
5. stablecoin payout pool is funded on Base
6. eligible FUZE holders claim through `FuzeStablecoinProfitParticipation`

### Important rule
Credits themselves do not directly become profit-participation assets. They are usage units.

---

## 18. Relationship to Ethereum FUZE Token

The Ethereum FUZE token remains the canonical token layer for:
- holder identity
- holder balance truth
- holder rank inputs
- snapshot-based eligibility for profit participation
- ecosystem token utility

The Platform Credits ledger on Base is the operational product-commerce layer.

These two layers are connected by:
- policy
- backend verification and reconciliation
- snapshot services
- published transparency reporting

They are not the same asset and should not be merged conceptually.

---

## 19. Account Model

The credits system SHOULD support:

### 19.1 Personal Credit Accounts
For individual user balances.

### 19.2 Workspace Credit Accounts
For team, company, or organization balances.

Products should be able to spend against:
- personal balance
- workspace balance
based on product rules and entitlements.

---

## 20. Required Ledger Events

The Platform Credits ledger SHOULD emit at least the following event families:

### Issuance Events
- `CreditsIssued`
- `BonusCreditsIssued`
- `CreditsAdjusted`

### Spend Events
- `CreditsSpent`
- `CreditsReserved`
- `CreditsReleased`

### Refund / Reversal Events
- `CreditsReversed`
- `CreditsRefunded`
- `NegativeBalanceRecorded` if negative-balance logic exists

### Expiry Events
- `CreditsExpired`

### Ownership / Internal Transfer Events
- `CreditsTransferredInternally`
- `WorkspaceCreditAssigned`

### Governance / Policy Events
- `CreditsPolicyHashUpdated`
- `CreditClassPolicyUpdated`
- `IssuerRoleUpdated`

All material credit lifecycle actions should be recorded.

---

## 21. Recommended Contract Structure

The Platform Credits system may be implemented as one contract or as a small contract family. Recommended high-level structure:

### A. `FuzePlatformCreditsLedger`
Core ledger contract on Base.

Responsibilities:
- maintain balances
- record credit classes
- issue credits
- spend credits
- reverse credits
- emit ledger events

### B. `FuzeCreditsEntitlementRouter` (optional)
Links products and pricing logic to the ledger.

Responsibilities:
- route product spend requests
- enforce entitlement / pricing integration
- manage product-specific spend contexts

### C. `FuzeCreditsIssuerRegistry` (optional)
Manage approved issuer roles and reason-coded issuance paths.

Responsibilities:
- define who can issue credits
- define allowed issuance classes
- track approved issuance sources

A simple v1 could start with a single ledger contract plus backend routing, but the policy model should assume strong role separation.

---

## 22. Required State Variables

At minimum, the core ledger contract SHOULD expose:

- `address public governanceMultisig;`
- `address public timelockController;`
- `string public version;`
- `bytes32 public policyHash;`
- `bool public paused;`

Recommended additional state:
- balances by account or workspace
- balances by credit class
- total issued by class
- total spent by class
- total reversed by class
- total expired by class
- approved issuer roles
- approved internal transfer roles
- optional spend-priority policy references

---

## 23. Admin Model

### 23.1 Governance Structure
The credits system SHOULD be governed by:
- credits governance multisig
- timelock controller for sensitive actions

### 23.2 Sensitive Actions Requiring Timelock
The following MUST be timelocked:
- changing governanceMultisig
- changing timelockController
- changing issuance policy
- changing credit class policy
- changing spend-priority policy
- adding or removing highly privileged issuer roles

### 23.3 Non-Permitted Admin Powers
Admins MUST NOT be able to:
- arbitrarily drain user balances
- silently rewrite credit history
- convert credits into freely transferable public assets by undisclosed change
- bypass accounting and event requirements

---

## 24. Security Requirements

The implementation MUST include or address:
- role separation
- safe accounting updates
- strong event logging
- protection against unauthorized minting
- protection against over-spend
- protection against unauthorized reversal
- clear support for auditability
- invariant tests for class balances and total accounting

Recommended test categories:
- unauthorized issuer cannot mint
- spend cannot exceed balance
- reversal cannot exceed eligible reversible balance
- paid credits do not expire if policy says non-expiring
- bonus credits expiry works as configured
- internal transfer cannot exceed allowed scope
- event emission occurs on all material state changes

---

## 25. Canonical Summary

| Field | Value |
|---|---|
| Core Name | `FuzePlatformCreditsLedger` |
| Chain | Base |
| Asset Type | Internal platform consumption unit |
| Transferability | Account-bound / workspace-bound |
| Paid Credits | Non-expiring by default |
| Bonus Credits | May expire |
| Mint Sources | Verified payments, approved rewards, limited admin corrections |
| Spend Model | Product and entitlement governed |
| Relationship to FUZE Token | Separate asset; FUZE stays on Ethereum |
| Relationship to Profit Participation | Connected by accounting and treasury settlement, not direct 1:1 conversion |

---

## 26. Canonical Policy Statement

FUZE Platform Credits are the unified internal consumption unit of the FUZE ecosystem. They are issued after verified payment or approved reward events, recorded on an on-chain credit ledger on Base, spent across FUZE products under entitlement rules, and remain account-bound rather than freely transferable. Paid credits are non-expiring by default, while promotional or restricted credits may follow policy-defined expiry rules. Credits are separate from the Ethereum FUZE token and separate from stablecoin profit participation, but they connect to the broader FUZE economy through transparent accounting, treasury settlement, and product usage.
