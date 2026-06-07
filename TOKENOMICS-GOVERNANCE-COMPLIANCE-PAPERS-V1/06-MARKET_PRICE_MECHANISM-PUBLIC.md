# Market Price Mechanism

## Executive Summary

FUZE uses the **Market Price Mechanism** to define how selected vault-token access can be priced when Public Vault Access windows, market-aligned access, or policy-approved token access are enabled.

The purpose of the Market Price Mechanism is to prevent arbitrary admin-set pricing, hidden discounts, unfair insider access, and unclear pricing when selected FUZE vault tokens become available through policy-approved access windows.

FUZE uses staged pricing because market maturity changes over time. Early-stage access can use signed approved prices and minimum price floors. Mature-stage access can use time-weighted average price references, signed reference prices, premium multipliers, minimum floors, deviation checks, purchase caps, lockups, and public reporting.

The Market Price Mechanism supports FUZE’s Controlled Circulation Policy by making selected vault access transparent, market-aligned, policy-based, time-limited, manipulation-resistant, and visible through FUZE public documentation or transparency surfaces where applicable.

FUZE does not use the Market Price Mechanism to promise price support, liquidity, listing, profit, return, payout, or market performance.

This paper defines the public pricing model, staged pricing framework, data reference logic, controls, Public Vault Access relationship, reporting direction, and risk safeguards.

## 1. FUZE Position

FUZE presents the Market Price Mechanism as a market-aligned access-pricing policy for selected vault-token access.

FUZE pricing principle:

**Market-aligned vault access uses approved price policies, minimum price floors, purchase caps, lockups, and public reporting. No single admin can silently set or change selected vault access prices.**

The Market Price Mechanism follows FUZE’s tokenomics principle:

**Purpose-specific allocation. Vault-based control. Controlled circulation. Product-first utility. Long-term ecosystem alignment.**

FUZE position:

**The Market Price Mechanism defines pricing controls for selected vault-token access. It is not a token valuation promise, listing price promise, liquidity promise, price-support system, or financial-return model.**

The mechanism exists because selected vault access can affect public trust. When pricing is unclear, community members can worry about hidden discounts, preferential insider access, arbitrary admin decisions, or unfair token movement. Market-aligned pricing helps FUZE present a more transparent and policy-based access model.

## 2. Platform Context

FUZE is a transparency-first AI SaaS platform building practical products on top of shared infrastructure for identity, credits, payments, AI orchestration, reporting, and ecosystem participation.

The Market Price Mechanism connects to FUZE’s platform context in several ways:

| Platform Area | Market Price Mechanism Relationship |
|---|---|
| Controlled Circulation Policy | Ensures selected vault access follows purpose, timing, lockup, eligibility, and reporting controls |
| Public Vault Access System | Uses pricing policy for selected eligibility-controlled access windows |
| Vault-by-Vault Release Rules | Defines which vaults can use pricing-based access and which vaults use other release logic |
| Governance / Multisig / Timelock Model | Controls approved price policies, updates, pauses, and policy references |
| Liquidity and Listing Policy | Separates liquidity operations from price promises and listing outcomes |
| Platform Credits | Remain separate product usage credits and do not use token market pricing |
| ZAGA | Can connect wallet-aware access and utility participation where product rules allow |
| FUZE Core Platform | Supports identity, eligibility, reporting, payment rails, policy references, and public documentation where applicable |

FUZE launch focus is HerHelp.com and ZAGA.io, supported by FUZE Core Platform rails and accelerated internally by Botmad.

The Market Price Mechanism supports that launch focus by making token-access pricing more transparent when selected token access is available under final policy.

## 3. Public Model

### 3.1 Market Price Mechanism Definition

The Market Price Mechanism is a public pricing policy for selected FUZE vault-token access.

| Element | Public Meaning |
|---|---|
| Approved price policy | A pricing rule approved under FUZE governance and public policy controls |
| Minimum price floor | A lower bound that prevents selected access from being priced below approved policy |
| Signed approved price | A policy-approved price signed or authorized by approved governance controls |
| TWAP reference | Time-weighted average price reference where sufficient market maturity exists |
| Premium multiplier | A policy-based adjustment above a reference price where applicable |
| Deviation check | A control that detects abnormal price divergence or unreliable market conditions |
| Purchase cap | Limit per account, wallet, access window, participant class, or policy period |
| Lockup | Restriction that delays full active circulation after access |
| Policy reference | Public policy document, hash, governance record, or approval reference |
| Public reporting | Public-safe disclosure of pricing method, access window status, and access history |

The mechanism exists to support policy-based pricing discipline, not token valuation forecast.

### 3.2 Staged Pricing Model

FUZE uses staged pricing because market maturity changes over time.

| Stage | Pricing Model | Public Role |
|---|---|---|
| Early-stage / low-liquidity stage | Signed approved price, minimum price floor, purchase caps, lockups, and policy approval |
| Transitional stage | Signed reference price, market reference where available, deviation checks, caps, lockups, and reporting |
| Mature market stage | TWAP reference, premium multiplier where applicable, minimum floor, deviation checks, caps, lockups, and public reporting |
| Exceptional policy stage | Paused, manually reviewed, or governance-approved pricing where abnormal conditions exist |

This staged model prevents FUZE from pretending that early-stage and mature-stage markets behave the same.

### 3.3 Early-Stage Pricing

Early-stage pricing is used when reliable market references are not yet mature enough.

| Control | Public Role |
|---|---|
| Signed approved price | Price approved through policy and governance controls |
| Minimum price floor | Prevents selected access below approved lower bound |
| Purchase caps | Limits concentration and reduces unfair access |
| Lockups | Reduces immediate uncontrolled circulation |
| Eligibility controls | Limits access to approved participant classes |
| Public access window | Shows purpose, amount, rules, and status where applicable |
| Policy reference | Connects pricing to public policy or governance record |
| Pause control | Allows access to stop if conditions become unsuitable |

Early-stage pricing is a policy-controlled access method. It is not a market price prediction.

### 3.4 Transitional Pricing

Transitional pricing is used when market data begins to exist but does not yet provide a strong mature-market reference.

| Control | Public Role |
|---|---|
| Signed reference price | Combines approved policy with emerging market context |
| Limited market reference | Uses available market data where reliable enough |
| Minimum floor | Maintains approved lower bound |
| Deviation checks | Detects abnormal movement or unreliable data |
| Purchase caps | Limits concentration and access-window pressure |
| Lockups | Supports controlled circulation |
| Public reporting | Explains method and status where appropriate |
| Governance review | Allows adjustment or pause under defined controls |

Transitional pricing recognizes market development without over-relying on immature liquidity.

### 3.5 Mature Market Pricing

Mature market pricing can use TWAP references and policy controls.

| Control | Public Role |
|---|---|
| TWAP reference | Uses time-weighted average price where reliable market data exists |
| Premium multiplier | Can apply above reference price where policy requires |
| Minimum price floor | Prevents pricing below approved floor |
| Deviation check | Identifies abnormal or manipulated market conditions |
| Liquidity threshold | Confirms whether reference data is sufficient for use |
| Purchase cap | Limits access concentration |
| Lockup / vesting | Controls post-access circulation |
| Public reporting | Shows pricing method, reference logic, and access status where public-safe |
| Governance override | Allows pause or review under abnormal conditions |

Mature market pricing uses market data as a reference, not as a guarantee.

### 3.6 Price Reference Inputs

The Market Price Mechanism can use different reference inputs depending on market maturity and policy readiness.

| Input | Public Role |
|---|---|
| Approved policy price | Governance-approved price for early-stage access |
| Stablecoin-denominated reference | Price expressed in USDC, USDT, or approved stablecoin where applicable |
| DEX TWAP | Time-weighted average price from approved DEX source where reliable |
| CEX reference | Exchange price reference where approved and available |
| Multi-source reference | Combined reference across approved venues where appropriate |
| Liquidity threshold | Confirms whether a source has sufficient depth or activity |
| Volatility range | Identifies abnormal price movement |
| Deviation range | Detects difference between sources or unexpected movement |
| Governance approval | Confirms source and method under policy |
| Public record | Records selected method for transparency where applicable |

Reference inputs are selected by policy. They are not informal admin discretion.

### 3.7 Minimum Price Floor

FUZE can use a minimum price floor for selected access windows.

| Floor Function | Public Role |
|---|---|
| Prevent underpricing | Reduces hidden-discount concerns |
| Protect public fairness | Helps avoid unfair access below approved policy |
| Support controlled circulation | Reduces incentive for immediate pressure after access |
| Improve reporting clarity | Gives a visible lower bound where applicable |
| Require policy approval | Keeps floor changes governed |
| Avoid arbitrary access | Prevents silent admin-set pricing |

A minimum price floor is a pricing-control tool. It is not a promise that the market price will remain above that level.

### 3.8 Premium Multiplier

FUZE can apply a premium multiplier in mature-stage pricing where policy allows.

| Premium Function | Public Role |
|---|---|
| Access discipline | Avoids vault access below market-aligned conditions |
| Public fairness | Helps prevent selected participants from receiving unfair pricing |
| Controlled circulation | Reduces incentive for immediate circulation pressure |
| Treasury alignment | Supports policy-based proceeds direction where applicable |
| Governance reference | Multiplier remains subject to policy approval |
| Public explanation | Method can be explained where appropriate |

A premium multiplier is an access-pricing policy, not a token appreciation promise.

### 3.9 Deviation Checks

Deviation checks protect the pricing process from unreliable market conditions.

| Deviation Area | Public Role |
|---|---|
| Source-to-source deviation | Compares approved market references where multiple sources exist |
| TWAP-to-spot deviation | Identifies abnormal short-term movement |
| Liquidity weakness | Detects insufficient market depth |
| Abnormal volatility | Flags unstable conditions |
| Manipulation risk | Supports review when movement appears abnormal |
| Data outage | Pauses or reviews pricing when data is unavailable |
| Governance pause | Allows approved users or contracts to pause access |
| Public reporting | Can show pause or review status where public-safe |

Deviation checks improve pricing integrity.

### 3.10 Purchase Caps

Purchase caps help reduce concentration and unfair access.

| Cap Type | Public Role |
|---|---|
| Per-account cap | Limits one account’s access |
| Per-wallet cap | Limits one wallet’s access |
| Per-entity cap | Limits one organization or related party where applicable |
| Per-window cap | Limits access during one window |
| Global window cap | Limits total tokens available in the access window |
| Category cap | Limits participant class or eligibility category |
| Time-based cap | Limits access per day, week, or period where applicable |
| Anti-sybil controls | Reduces duplicate or abuse patterns |

Purchase caps support public fairness and controlled circulation.

### 3.11 Lockups and Staged Release

Pricing controls work together with lockups.

| Lockup Tool | Public Role |
|---|---|
| Immediate lockup | Prevents immediate full active circulation |
| Vesting | Releases tokens over a defined period |
| Cliff | Delays release until a defined point |
| Staged claim | Releases tokens in multiple claim periods |
| Utility-based release | Connects release to product or participation conditions where policy allows |
| Governance pause | Allows access or release to pause under defined conditions |
| Public reporting | Shows locked and released amounts where public-safe |

Lockups support controlled circulation. They do not create price support, return assurance, or liquidity assurance.

### 3.12 Public Vault Access Relationship

The Market Price Mechanism is used inside the Public Vault Access System where approved.

| Public Vault Access Field | Pricing Relationship |
|---|---|
| Source vault | Pricing applies to selected approved vault source |
| Access window | Pricing is bound to a defined window |
| Eligible participants | Pricing applies only to eligible participants |
| Pricing method | Shows approved method, stage, and policy reference |
| Minimum price floor | Defines lower bound where applicable |
| Reference price | Uses signed price, TWAP, or other approved reference |
| Premium multiplier | Applies where policy requires |
| Purchase caps | Limits concentration |
| Lockups | Controls post-access circulation |
| Reporting | Shows public-safe pricing and transaction history where available |

Market Price Mechanism gives Public Vault Access a pricing discipline layer.

### 3.13 Vault-by-Vault Pricing Fit

Not every vault uses market-based pricing.

| Vault / Allocation | Market Price Mechanism Fit |
|---|---|
| Community Participation Vault | Strong fit for selected Public Vault Access windows where approved |
| Treasury Reserve Vault | Possible fit for controlled strategic access where policy allows |
| Ecosystem Growth & Partnerships Vault | Possible fit for partner or ecosystem access windows where appropriate |
| Holder Incentives Vault | Usually earned-release logic rather than pricing-based access |
| Liquidity Operations Vault | Governed primarily by liquidity and market-operations policy |
| Team Vesting Vault | Not normally priced through public access |
| Advisor / Strategic Contributor Vault | Not normally priced through public access |
| Foundation Reserve Vault | Long-horizon stewardship reserve |
| Transparency / Stability Vault | Exceptional reserve only |
| BOARD / Surfboard Migration Vault | Migration claim logic, not market-priced public access |

The pricing mechanism is selective and vault-specific.

### 3.14 Payment and Proceeds Direction

Where selected Public Vault Access involves payment, accepted payment assets and proceeds routing follow approved policy.

| Area | Public Role |
|---|---|
| Accepted payment asset | USDC, USDT, or approved stablecoin where applicable |
| Proceeds destination | Treasury, product development, liquidity operations, stablecoin compensation pool, ecosystem reserve, or other approved destination |
| Payment record | Transaction record where available |
| Accounting review | Treatment remains subject to accounting and tax review |
| Refund / cancellation rules | Follow final product and legal policy |
| Public reporting | Shows high-level proceeds destination where public-safe |

Payment and proceeds reporting helps reduce confusion.

### 3.15 Public Reporting Model

Market Price Mechanism reporting can include:

| Reporting Area | Public Direction |
|---|---|
| Access window status | Upcoming, active, closed, paused, settled, or archived |
| Source vault | Which vault uses the pricing method |
| Pricing stage | Early-stage, transitional, mature-stage, or exceptional policy stage |
| Pricing method | Signed price, minimum floor, TWAP, premium multiplier, or policy-defined method |
| Reference period | Time period used for reference pricing where appropriate |
| Minimum floor | Lower bound where disclosed |
| Purchase cap | Per-user, per-wallet, per-window, or global cap where disclosed |
| Lockup | Release restriction and schedule summary |
| Amount available | Total window size |
| Amount accessed | Amount already accessed where available |
| Amount remaining | Remaining access amount where available |
| Proceeds destination | High-level direction where applicable |
| Contract reference | Contract, vault, or oracle reference where available |
| Policy reference | Policy document, approval, or governance record |
| Risk boundary | Token, listing, liquidity, price, payout, jurisdiction, and eligibility boundaries |

Reporting makes access-pricing more visible and easier to review.

## 4. Investor and Community Relevance

The Market Price Mechanism matters because pricing fairness is a public trust issue.

Investor relevance:

- Reduces concern around hidden discounts and arbitrary admin pricing
- Connects selected vault access to approved pricing policy
- Supports market-aligned access where final policy allows
- Uses minimum floors, caps, lockups, and deviation checks to support discipline
- Connects Public Vault Access to reporting and governance
- Supports diligence around vault releases and token movement
- Reinforces controlled circulation and product-first utility
- Improves public readability of token access policy

Community relevance:

- Helps eligible community participants understand how access pricing works
- Explains why not every access window uses the same pricing model
- Shows that early-stage pricing differs from mature-market pricing
- Explains minimum floors, purchase caps, lockups, and public reporting
- Reduces confusion around hidden insider access
- Repeats that pricing method does not guarantee future market outcome
- Separates Platform Credits from FUZE token

Strategic partner relevance:

| Partner Type | Market Price Mechanism Value |
|---|---|
| Strategic investors | Clearer vault-access pricing discipline |
| Web3 communities | More transparent access windows and risk boundaries |
| Product users | Platform Credits remain separate from token pricing |
| Ecosystem partners | Partner access can follow policy-based pricing where approved |
| Treasury partners | Proceeds and pricing rules become easier to review |
| Governance partners | Pricing policy, reference sources, deviation checks, and reporting improve reviewability |
| Compliance partners | Eligibility, pricing, jurisdiction, and disclosure controls become clearer |
| Market partners | Pricing and liquidity policy remain separate from market-outcome promises |

The mechanism strengthens FUZE public trust by making selected pricing decisions more explainable.

## 5. Public Boundary

FUZE publicly presents the Market Price Mechanism as a market-aligned access-pricing policy for selected vault-token access.

FUZE publicly explains:

- approved pricing policy
- pricing stage
- minimum price floor
- signed approved price
- TWAP reference where applicable
- premium multiplier where applicable
- deviation checks
- purchase caps
- lockups
- source vault
- access window status
- proceeds destination where applicable
- contract reference where available
- policy reference where available
- risk boundaries

FUZE keeps the following areas subject to product, technical, legal, accounting, tax, privacy, compliance, payment, platform, smart contract, oracle, market, treasury, governance, and operational readiness where applicable:

- whether Public Vault Access is implemented
- exact pricing formulas
- exact minimum price floors
- exact premium multipliers
- exact TWAP windows
- exact reference sources
- exact deviation thresholds
- exact purchase caps
- exact lockup schedules
- exact accepted payment assets
- exact proceeds routing
- smart contract deployment timing
- market-data source selection
- oracle design
- jurisdiction-specific access
- public dashboard format
- pause and emergency controls

The Market Price Mechanism is not a token valuation promise, public token sale announcement, exchange listing plan, payout plan, price support system, liquidity promise, or financial-return plan.

## 6. Risk Boundaries and Safeguards

FUZE applies risk boundaries around the Market Price Mechanism.

### 6.1 Market Price Mechanism Boundary

The Market Price Mechanism defines access-pricing controls for selected vault-token access. It does not guarantee future token price, listing price, market price, market stability, liquidity, profit, return, payout, or market outcome.

### 6.2 General Token Boundary

FUZE does not guarantee token price, liquidity, listing, profit, return, payout, or market performance.

### 6.3 Platform Credits Boundary

Platform Credits are for product usage and are not investment assets, payout assets, or FUZE tokens.

### 6.4 Public Vault Access Boundary

Public Vault Access, if implemented, is subject to eligibility, jurisdiction, compliance, platform readiness, market-aligned pricing rules, lockups, and final policy approval.

### 6.5 Community Participation Boundary

Any future Community Participation Round is subject to legal, compliance, jurisdiction, product, platform, and smart contract readiness review.

### 6.6 Listing Boundary

FUZE does not guarantee exchange listing, listing timing, liquidity, price performance, or market outcome.

### 6.7 Reference Data Boundary

Reference prices, TWAPs, market data, liquidity data, venue data, or oracle data can be incomplete, delayed, unavailable, manipulated, volatile, or unsuitable. FUZE can pause, review, or reject reference use when data conditions are not reliable.

### 6.8 Lockup Boundary

Lockups and staged releases support controlled circulation. They do not create price support, return assurance, or liquidity assurance.

### 6.9 Development Standards Boundary

FUZE uses standards-inspired or standards-aligned processes. FUZE does not claim formal certification unless certification has been completed.

## 7. Reporting and Transparency Direction

FUZE reports the Market Price Mechanism through public documentation, Public Vault Access pages, tokenomics pages, vault pages, ZAGA.io, FUZE product pages, community FAQ, investor materials, release notes, governance references, and transparency surfaces where applicable.

Reporting areas include:

| Reporting Area | Public Direction |
|---|---|
| Pricing policy | Shows approved pricing method and stage where applicable |
| Source vault | Shows which vault uses the pricing mechanism |
| Access window | Shows status, available amount, accessed amount, and remaining amount where available |
| Minimum floor | Shows lower-bound policy where disclosed |
| TWAP reference | Shows reference method and period where public-safe |
| Premium multiplier | Shows multiplier where applicable and disclosed |
| Purchase caps | Shows access limits where public-safe |
| Lockups | Shows release restrictions and schedule summary |
| Deviation checks | Shows pause or review status where appropriate |
| Proceeds destination | Shows high-level proceeds direction where applicable |
| Contract reference | Shows smart contract, vault, or oracle reference where available |
| Policy reference | Shows policy, approval, hash, or governance record where available |
| Risk boundaries | Repeats token, listing, liquidity, payout, price, return, jurisdiction, eligibility, and data boundaries |

FUZE uses pricing transparency to reduce hidden-discount concerns and strengthen controlled circulation.

## 8. Conclusion

FUZE uses the Market Price Mechanism to make selected vault-token access pricing more transparent, market-aligned, policy-based, and controlled.

The mechanism prevents silent admin pricing, hidden discounts, and unclear access pricing by using approved price policies, minimum price floors, signed approved prices, TWAP references where mature market data exists, premium multipliers where applicable, deviation checks, purchase caps, lockups, and public reporting.

The Market Price Mechanism works with the Public Vault Access System, Controlled Circulation Policy, Vault-by-Vault Release Rules, Liquidity and Listing Policy, Governance / Multisig / Timelock Model, and FUZE Core Platform reporting.

FUZE token is for ecosystem participation. Platform Credits are for product usage. Stablecoins pay for work. FUZE tokens align long-term participation.

Product usage comes first. Platform rails come second. Broader ecosystem participation comes after that.
