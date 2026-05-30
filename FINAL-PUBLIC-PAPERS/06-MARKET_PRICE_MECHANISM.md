# FILE NAME: 06-MARKET_PRICE_MECHANISM-PUBLIC.md

# Market Price Mechanism

## Executive Summary

FUZE uses a **Market Price Mechanism** to determine pricing for selected vault access windows under the FUZE Public Vault Access System.

The purpose of this mechanism is to prevent arbitrary admin-set pricing, hidden discounts, unfair insider access, and price manipulation when selected FUZE vault tokens become available through policy-approved access windows.

FUZE uses staged pricing because market maturity changes over time. Early-stage access uses signed approved prices and minimum price floors. Mature-stage access uses time-weighted average price references, signed reference prices, premium multipliers, minimum floors, deviation checks, purchase caps, lockups, and public reporting.

The Market Price Mechanism supports FUZE v2’s Controlled Circulation Policy by ensuring that selected vault access is transparent, market-aligned, policy-based, time-limited, manipulation-resistant, and visible on the FUZE website.

FUZE does not use the Market Price Mechanism to promise price support, liquidity, listing, profit, return, payout, or market performance.

## 1. FUZE Position

FUZE applies a staged Market Price Mechanism for selected vault access windows.

FUZE does not rely on a single pricing model because pricing reliability depends on market maturity, liquidity depth, oracle availability, public vault access design, and compliance readiness.

FUZE pricing principle:

**Market-aligned vault purchases use approved price policies, minimum price floors, purchase caps, lockups, and public reporting. No single admin can silently set or change token access prices.**

FUZE uses the following staged pricing model:

| Stage | Pricing Method |
|---|---|
| Early stage / before deep liquidity | Signed approved price + approved minimum price floor |
| Intermediate stage | Signed approved price + DEX TWAP reference + minimum price floor |
| Mature stage / after reliable liquidity | 24h TWAP × premium multiplier, checked against signed reference price and minimum approved price |

Early-stage formula:

**Final Price = max(signedApprovedPrice, approvedMinimumPrice)**

Mature-stage formula:

**Final Price = max(24h TWAP × premiumMultiplier, signedReferencePrice, approvedMinimumPrice)**

FUZE does not allow selected vault tokens to be purchased below an approved minimum price.

## 2. Platform Context

FUZE is a transparency-first AI SaaS platform building practical products on top of shared infrastructure for identity, credits, payments, AI orchestration, reporting, and ecosystem participation.

FUZE execution order is:

**Product usage first. Platform rails second. Broader ecosystem participation after that.**

The Market Price Mechanism fits this execution model by giving selected vault access a pricing framework that is transparent, policy-linked, and controlled by platform rules.

FUZE v2 launch focus is **HerHelp.com** and **ZAGA.io**, supported by FUZE Core Platform rails and accelerated internally by **Botmad**.

The Market Price Mechanism connects to FUZE platform layers in the following way:

| Platform Area | Market Price Mechanism Relationship |
|---|---|
| FUZE Core Platform | Provides identity, reporting, governance, policy control, and access-window infrastructure |
| Public Vault Access System | Uses pricing logic for selected vault access windows |
| Controlled Circulation Policy | Keeps vault-token movement tied to policy and market-aligned access |
| Treasury Reserve Vault | Uses approved pricing rules for selected policy-based windows |
| Community Participation Round | Uses reviewed pricing without return-based public framing |
| Ecosystem Partnership Vault | Uses market-aligned or milestone-linked access rules where applicable |
| Platform Credits | Product usage asset, separate from FUZE token pricing |
| FUZE token | Ecosystem participation asset on Ethereum mainnet |
| Transparency dashboard | Reports access-window price method, policy hash, floor, cap, and window status |
| Governance direction | Uses multisig, timelock, signer control, price expiry, and deviation checks |
| Compliance posture | Keeps pricing, eligibility, jurisdiction, and public-risk language clearly bounded |

FUZE token is for ecosystem participation. Platform Credits are for product usage. Profit participation is a long-term design direction, not an immediate or guaranteed promise.

## 3. Public Model

### 3.1 Price Mechanism Overview

FUZE supports three pricing modes.

| Pricing Mode | Description | Best Used When |
|---|---|---|
| Signed Approved Price | Approved signer or committee signs a price message | Early stage before reliable liquidity |
| TWAP-Based Price | Contract reads a time-weighted average price from a DEX pool | After reliable liquidity exists |
| Hybrid Price | Contract uses TWAP, signed reference price, minimum floor, and deviation checks | Mature stage / highest-trust model |

### 3.2 Early-Stage Pricing

Before FUZE has reliable market liquidity, a DEX TWAP can be easier to manipulate. In this stage, FUZE uses:

**signedApprovedPrice + approvedMinimumPrice**

Formula:

**Final Price = max(signedApprovedPrice, approvedMinimumPrice)**

Example:

| Item | Value |
|---|---:|
| signedApprovedPrice | $0.050 |
| approvedMinimumPrice | $0.045 |
| final price | $0.050 |

If the signed approved price is below the minimum:

| Item | Value |
|---|---:|
| signedApprovedPrice | $0.035 |
| approvedMinimumPrice | $0.045 |
| final price | $0.045 |

The signed price includes:

- price
- quote currency
- payment token
- timestamp
- expiry time
- source description
- policy ID
- window ID
- maximum token amount
- signer address
- nonce
- chain ID
- contract address

This prevents replay and stale-price usage.

### 3.3 Mature-Stage Pricing

After FUZE has reliable DEX liquidity, the contract can use TWAP.

TWAP means:

**Time-Weighted Average Price**

TWAP reduces spot-price manipulation because it averages price over a selected time window.

| Use Case | TWAP Window |
|---|---|
| Treasury / partnership / public vault access | 24 hours |
| Operational liquidity actions | 1–4 hours |
| Emergency stability action | Custom policy-approved window |
| Public Community Participation | 24 hours or reviewed fixed price, depending on legal and compliance review |

Mature-stage formula:

**Final Price = max(24h TWAP × premiumMultiplier, signedReferencePrice, approvedMinimumPrice)**

Example:

| Item | Value |
|---|---:|
| 24h TWAP | $0.050 |
| premiumMultiplier | 1.02 |
| signedReferencePrice | $0.049 |
| approvedMinimumPrice | $0.045 |
| final price | $0.051 |

If TWAP drops below the minimum floor:

| Item | Value |
|---|---:|
| 24h TWAP | $0.030 |
| premiumMultiplier | 1.02 |
| signedReferencePrice | $0.032 |
| approvedMinimumPrice | $0.045 |
| final price | $0.045 |

### 3.4 Premium Multiplier

FUZE can apply a premium above TWAP for direct vault purchases.

A buyer purchasing directly from a vault can avoid market slippage. A small premium helps protect existing holders and the vault.

| Window Type | Premium Range |
|---|---:|
| Treasury public access | 1%–3% above TWAP |
| Strategic buyer access | 0%–5% depending on lockup |
| Partner access | 0%–5% depending on milestone value |
| Community participation | Reviewed price |
| Team/advisor compensation conversion | 0%–3% depending on policy |

Standard market-aligned vault purchases use a 2% premium unless another policy is approved.

Formula:

**TWAPAdjustedPrice = TWAP × 1.02**

### 3.5 Minimum Approved Price

Every access window has a minimum approved price.

The contract never sells below that floor.

The minimum approved price protects:

- vault value
- tokenomics discipline
- existing holder trust
- treasury and reserve integrity
- access-window fairness
- protection against manipulated low-price purchases
- protection against panic-window sales
- protection against admin underpricing

Rule:

**Final Price is never lower than approvedMinimumPrice.**

The minimum price is set through governance or multisig control and uses timelock control where appropriate.

### 3.6 Discount Rules

Discounts are not the default.

FUZE v2 avoids public discount-based token sale marketing. Where discount logic exists, it remains tied to policy, lockup, contribution, strategic value, and legal review.

Discount access requires:

- specific policy approval
- lockup or vesting
- milestone-based contribution
- strategic value justification
- token amount cap
- public disclosure where appropriate
- legal and compliance review
- no TGE multiple framing

Discount rule:

**Any discount is tied to measurable strategic value, longer lockup, or milestone delivery. Discounts are not marketed as guaranteed upside.**

Guardrail:

| Discount Level | Required Lockup |
|---|---|
| 0% discount / market price | Standard lockup or window-specific rules |
| 1%–5% discount | 6–12 month lockup |
| 5%–10% discount | 12–24 month lockup and milestone justification |
| More than 10% discount | Exceptional review only |

Public-facing materials use:

**market-aligned price**

not:

**discount**

### 3.7 Price Expiry

Signed prices expire.

| Price Type | Max Age |
|---|---:|
| Signed approved price | 1–24 hours depending on window |
| Treasury access price | 24 hours maximum |
| Partner window price | 24 hours maximum |
| Emergency price | Shorter policy-defined window |
| TWAP value | Read fresh or validated at purchase time |

Expired signed prices are rejected.

Required fields include:

- `validFrom`
- `validUntil`
- `nonce`
- `chainId`
- `contractAddress`
- `windowId`

### 3.8 Oracle and Price Source

FUZE uses a staged oracle design.

#### Early Stage

Early-stage pricing uses:

- signed approved price
- approved minimum price
- multisig-approved price policy

#### Intermediate Stage

Intermediate-stage pricing uses:

- signed approved price
- DEX TWAP reference
- minimum price floor
- max deviation check

#### Mature Stage

Mature-stage pricing uses:

- DEX TWAP
- signed reference price
- minimum price floor
- premium multiplier
- max deviation check
- optional multi-source reference

Mature model:

**Hybrid Oracle + TWAP + Signed Reference Price + Minimum Floor**

### 3.9 Max Deviation Check

The contract rejects suspicious price differences.

If signedReferencePrice differs from TWAP by more than the approved threshold, the transaction reverts or the access window pauses.

| Window Type | Max Deviation |
|---|---:|
| Standard access window | 10% |
| Strategic access window | 15% |
| Liquidity operation | Policy-specific |
| Emergency window | Policy-specific |

Rule:

**If price sources deviate beyond the approved threshold, the transaction reverts or the access window pauses.**

### 3.10 Purchase Caps

The price mechanism works with purchase caps. Caps reduce market pressure and concentration risk.

| Cap Type | Purpose |
|---|---|
| max per wallet | Prevent concentration |
| max per transaction | Prevent large single purchase |
| max per window | Cap total release |
| max per day / week | Reduce sudden circulation |
| max by eligibility tier | Control user or group access |
| max by jurisdiction group | Support compliance controls where needed |

### 3.11 Lockup Requirement

Market-aligned purchase does not always mean immediate liquidity.

Purchased tokens can enter a lockup or vesting contract depending on window size, buyer type, discount level, and policy.

| Window Type | Lockup Direction |
|---|---|
| Community Participation Round | 5% at TGE, 60-day cliff, 95% over 12 months |
| Treasury public access | 0–6 months depending on size |
| Strategic buyer access | 6–24 months |
| Partner access | 6–24 months |
| Discounted access | Longer lockup required |
| Team/advisor compensation conversion | 6–24 months |

### 3.12 Governance Controls

Price policy changes use governance controls.

Actions requiring multisig or timelock include:

- setting approvedMinimumPrice
- changing premiumMultiplier
- approving signer set
- changing maxDeviationBps
- changing TWAP window
- changing oracle source
- allowing discount
- changing proceeds destination
- creating large access windows
- pausing or unpausing pricing module
- changing price expiry limits

Rule:

**No single admin can silently set, lower, or override the market price.**

### 3.13 Public UI Pricing Display

The FUZE website displays price information clearly for each access window.

Public UI fields include:

| Field | Purpose |
|---|---|
| current price | Shows final active access price |
| pricing method | Shows signed price, TWAP, or hybrid model |
| minimum approved price | Shows floor protection |
| premium multiplier | Shows premium above market reference where applicable |
| price expiry | Shows expiration of signed price |
| TWAP window | Shows reference time window where applicable |
| payment token | Shows accepted stablecoin |
| lockup rule | Shows post-purchase restriction |
| purchase cap | Shows max access amount |
| policy hash | Links price to policy record |
| risk notice | Shows market and participation boundaries |

## 4. Investor and Community Relevance

The Market Price Mechanism gives investors and community members a clearer view of how FUZE prices selected vault access.

For investors, the mechanism improves supply discipline and pricing governance. It shows that selected vault access is not based on arbitrary admin pricing, hidden discounts, or weak access controls.

For holders, the mechanism protects against underpriced vault access by requiring minimum approved prices, market references, premiums where applicable, and public reporting.

For eligible community participants, the mechanism explains how access-window pricing works and why pricing can differ by stage, liquidity maturity, policy, lockup, and legal review.

For strategic partners, the mechanism provides a transparent framework for market-aligned participation without presenting partner access as unrestricted discounted token access.

For contributors, team members, and advisors, the mechanism supports compensation conversion models where stablecoin proceeds can pay for approved work while FUZE token access remains policy-governed.

The Market Price Mechanism supports the FUZE position that tokenomics is long-term ecosystem infrastructure, not short-term hype.

## 5. Public Boundary

FUZE publicly presents the Market Price Mechanism as a pricing and governance framework for selected vault access windows.

FUZE publicly explains:

- pricing mode
- pricing formula
- approved minimum price
- TWAP window where applicable
- signed price source where applicable
- premium multiplier where applicable
- max deviation threshold
- price expiry
- purchase caps
- lockup or vesting rules
- policy hash
- risk notice
- window status

FUZE keeps readiness-dependent or sensitive details subject to the correct review process, including:

- signer identity details where disclosure is not yet ready
- oracle source configuration before deployment
- exact private partner terms
- private Seed Round terms
- market-maker or exchange-related details
- jurisdiction-specific eligibility details
- legal or tax treatment
- final contract deployment timing
- emergency pricing controls before formal activation

Public Vault Access, if implemented, is subject to eligibility, jurisdiction, compliance, platform readiness, market-aligned pricing rules, lockups, and final policy approval.

Platform Credits are for product usage and are not investment assets, payout assets, or FUZE tokens.

Profit participation is a long-term design direction and is not immediate or guaranteed. Any future framework requires legal, accounting, treasury, technical, and transparency readiness.

FUZE’s Seed Round discussions are private strategic fundraising conversations. Full details, structure, and terms are shared privately with qualified interested parties. This is not a public token sale.

## 6. Risk Boundaries and Safeguards

FUZE does not guarantee token price, liquidity, listing, profit, return, payout, or market performance.

FUZE applies the following safeguards through the Market Price Mechanism:

| Risk Area | FUZE Safeguard |
|---|---|
| Arbitrary admin pricing | Uses signed prices, minimum floors, TWAP references, policy hashes, multisig, and timelock |
| Hidden discount concern | Publicly reports pricing method, access rules, lockups, and policy records |
| Manipulated spot price | Uses TWAP, deviation checks, minimum floors, and fresh price validation |
| Underpriced vault access | Enforces approvedMinimumPrice |
| Stale signed price | Uses validFrom, validUntil, nonce, chain ID, contract address, and window ID |
| Concentrated access | Uses purchase caps per wallet, transaction, window, time period, eligibility tier, or jurisdiction group |
| Immediate sell pressure | Uses lockups and vesting where policy requires |
| Insider access concern | Uses public vault access rules, eligibility controls, reporting, and policy-linked pricing |
| Public return expectation | Avoids discount-to-TGE, TGE multiple, ROI, price target, and upside marketing |
| Legal overstatement | Uses compliance-aware language and avoids price, liquidity, listing, payout, or return claims |

FUZE does not guarantee exchange listing, listing timing, liquidity, price performance, or market outcome.

The Market Price Mechanism does not remove market risk. It defines how FUZE governs selected vault access pricing, protects vault value, reduces manipulation risk, and reports pricing policy publicly.

## 7. Reporting and Transparency Direction

FUZE reports the Market Price Mechanism through public documentation, website UI, vault dashboards, and access-window records.

The Market Price Mechanism can appear in:

- FUZE Vault Access website page
- public vault dashboard
- transparency dashboard
- public contract and wallet registry
- Public Vault Access documentation
- Controlled Circulation Policy documentation
- Community Participation Round documentation
- tokenomics paper
- investor materials
- community FAQ
- governance reporting
- whitepaper-compatible public documentation

FUZE transparency direction includes:

| Reporting Area | Public Transparency Direction |
|---|---|
| Pricing mode | Shows signed approved price, TWAP-based price, or hybrid price |
| Formula | Shows the active price calculation method |
| Minimum approved price | Shows the floor used to protect the vault |
| Premium multiplier | Shows any premium above TWAP |
| TWAP window | Shows reference period where applicable |
| Signed reference price | Shows approved reference where disclosure is available |
| Price expiry | Shows when signed pricing becomes invalid |
| Deviation check | Shows threshold or policy summary where appropriate |
| Purchase caps | Shows wallet, transaction, window, or time-based limits |
| Lockup terms | Shows post-purchase restrictions |
| Policy hash | Links pricing to public policy record |
| Contract address | Shows verified module address when registry-ready |
| Risk notice | Shows price, liquidity, listing, return, payout, eligibility, and jurisdiction boundaries |

FUZE uses reporting to make selected vault pricing understandable. Public readers can see how price is determined, what protections apply, what limits exist, and which policy governs the access window.

## 8. Conclusion

FUZE uses the Market Price Mechanism to make selected vault access pricing transparent, policy-based, market-aligned, and resistant to arbitrary pricing.

The mechanism supports staged pricing across early, intermediate, and mature market conditions. It uses signed approved prices, minimum approved price floors, TWAP references, premium multipliers, deviation checks, purchase caps, lockups, price expiry, and governance controls.

This pricing framework supports FUZE v2’s Controlled Circulation Policy and Public Vault Access System. It helps investors, holders, eligible participants, contributors, and strategic partners understand how selected FUZE vault tokens can enter circulation under clear pricing rules.

FUZE treats pricing as part of transparency-first tokenomics governance, not as discount marketing, return framing, or price-performance assurance.