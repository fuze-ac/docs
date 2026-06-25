# FUZE Vault Access Pricing Mechanism

## Executive Summary

The FUZE Vault Access Pricing Mechanism defines how an approved payment-based Public Vault Access Window can calculate, validate, authorize, publish, apply, settle, reconcile, correct, and archive a price used to determine FUZE allocation quantities.

It separates four different concepts:

1. the policy decision to create an access window;
2. the pricing profile approved for that window;
3. the price record produced for a specific validity interval; and
4. the participant allocation and settlement calculated from that price record.

The controlling pricing sequence is:

```text
approved access window
-> approved pricing profile and version
-> approved source set and source-quality rules
-> observation collection
-> source qualification and exclusion
-> normalization and quote conversion
-> reference-price calculation
-> approved adjustment and bounds
-> deterministic precision and rounding
-> deviation and reasonableness tests
-> authorized price record
-> validity interval
-> participant payment and allocation calculation
-> capacity, limit, and settlement checks
-> reconciliation and public-safe reporting
-> expiry, correction, pause, replacement, or archive
```

Each state is separate.

A pricing profile does not create an active access window.

A calculated price does not create participant eligibility.

A valid price record does not create an allocation.

A participant payment does not establish settlement when eligibility, capacity, allocation, or another condition remains incomplete.

A settled allocation does not automatically establish token release.

A release does not automatically establish circulation.

The resulting price is a bounded process input for one approved access window and validity interval.

It is not:

- a general FUZE market price;
- a future-price forecast;
- a valuation opinion;
- a guaranteed floor in external markets;
- a price-support commitment;
- a liquidity commitment;
- a DEX or CEX listing price;
- a resale guarantee;
- or a financial-return promise.

Every active pricing profile should identify:

- stable profile identifier and version;
- authorized access-window identifier;
- pricing type;
- calculation currency and quote unit;
- source assets, pairs, venues, pools, feeds, contracts, providers, or approved fixed records;
- observation period and sampling method;
- source qualification rules;
- normalization and conversion routes;
- aggregation method;
- source weights where applicable;
- minimum source and observation coverage;
- adjustment factor;
- floor, cap, or other approved bound;
- precision and rounding;
- participant and window limit interaction;
- validity interval;
- deviation and reasonableness tests;
- failure and fallback behavior;
- authorization method;
- correction method;
- reporting treatment;
- current status;
- and current-as-of date.

Every price record used for participant allocation should preserve:

- profile version;
- exact input sources;
- raw and normalized observations;
- excluded observations and reasons;
- observation cutoff;
- calculation steps;
- reference price;
- adjustment;
- bounds;
- conversion;
- rounding;
- final quote;
- validity interval;
- quality-test results;
- authority;
- evidence reference;
- correction state;
- and current status.

When required inputs do not pass the active profile, pricing should pause, retry, or enter another pre-approved failure mode.

The process should not silently substitute a source, shorten or extend an observation period, change a weight, alter a floor or cap, or use whichever result produces a preferred outcome.

This paper owns the pricing-profile, source-quality, calculation, authorization, validity, participant-application, settlement, failure, correction, reporting, and archive framework for approved payment-based vault-access windows.

The access-window lifecycle remains governed by [FUZE Public Vault Access Windows](17-FUZE_PUBLIC_VAULT_ACCESS_WINDOWS_PUBLIC.md).

Source-vault authority and token-release conditions remain governed by [FUZE Vault-by-Vault Release Rules](15-FUZE_VAULT_BY_VAULT_RELEASE_RULES_PUBLIC.md).

Market-price communication boundaries remain governed by [FUZE Market Price and Demand Boundary](22-FUZE_MARKET_PRICE_AND_DEMAND_BOUNDARY_PUBLIC.md).

## Purpose of This Paper

This paper explains:

- the public pricing position;
- pricing governance and separation of states;
- pricing-profile requirements;
- approved pricing types;
- source qualification;
- observation collection;
- normalization and quote conversion;
- reference-price calculations;
- adjustment factors and bounds;
- deviation and reasonableness tests;
- precision, rounding, and residual treatment;
- price-record authorization;
- validity intervals;
- participant calculations;
- payment and settlement interaction;
- capacity and participant-limit interaction;
- stablecoin, fiat, bridge, and conversion treatment;
- source, oracle, venue, network, and provider failures;
- fallback, exceptional review, and pause rules;
- recalculation, correction, and restatement;
- reporting and public evidence;
- privacy, security, and record retention;
- status and evidence requirements; and
- public limitations.

This paper does not replace:

- an active access-window notice;
- participant eligibility rules;
- source-vault authority;
- participant limits;
- allocation methods;
- payment instructions;
- proceeds-use decisions;
- refund terms;
- claim instructions;
- vesting or lock schedules;
- token-release approvals;
- liquidity or market-making procedures;
- exchange-listing procedures;
- accounting, tax, legal, compliance, sanctions, or jurisdiction review;
- private vendor or data-provider agreements;
- or smart-contract specifications.

## Public Position

FUZE vault-access pricing should be authorized before use, reproducible after use, consistent within the same validity interval, resistant to stale or abnormal data, and supported by durable evidence.

FUZE should not publish or apply a payment-based access-window price unless:

- the exact access-window version is approved;
- the exact pricing-profile version is approved;
- all required sources and conversion legs are identified;
- the source-quality tests are active;
- the observation method is reproducible;
- the calculation and bounds are deterministic;
- the price record is authorized;
- the validity interval is active;
- participant calculations can be applied consistently;
- payment and settlement systems can retain the price-record reference;
- and failure, pause, refund, correction, and reporting routes are ready.

The following do not independently create an approved price:

- a token-market screenshot;
- a single trade;
- a wallet transfer;
- an explorer quote;
- a community vote without the required authority;
- an exchange listing discussion;
- a liquidity-pool deployment;
- a prior round price;
- a private negotiation;
- a spreadsheet without approval;
- or an internal estimate.

## Pricing Governance and Separation of States

| State | Evidence-backed meaning | What it does not establish |
|---|---|---|
| Profile proposed | A pricing design is being prepared. | Approval or participant use |
| Profile under review | Sources, formula, bounds, risk, authority, and reporting are being assessed. | Approval |
| Profile approved | One exact profile version is authorized for a stated window or condition. | Active price record |
| Inputs collecting | Observations are being gathered under the profile. | Qualified inputs |
| Inputs qualified | Required source and observation tests passed. | Final price |
| Price calculated | The formula produced a result. | Authorization or participant use |
| Price approved | Required authority accepted the exact record. | Active validity interval unless activated |
| Price active | The record is valid for participant calculation within its stated interval. | Eligibility, allocation, or settlement |
| Price expired | The validity interval ended. | Invalidity of participant actions completed while active |
| Pricing paused | New calculations or participant use are temporarily restricted. | Cancellation of the window |
| Price corrected | A later authorized record fixes an error while preserving history. | Erasure of prior participant effects |
| Profile superseded | A later profile version replaces the prior version for future use. | Automatic rewriting of historical prices |
| Archived | The profile and records remain available for history. | Current use |

## Pricing Profile

Every payment-based access window should reference one approved pricing profile for each pricing mode it can use.

### Core Profile Fields

1. profile identifier;
2. profile version;
3. access-window identifier and version;
4. sponsor;
5. pricing owner;
6. approver;
7. pricing type;
8. calculation currency;
9. quote unit;
10. FUZE quantity unit and precision;
11. approved source set;
12. approved pair or conversion route;
13. source hierarchy;
14. observation period;
15. sampling interval;
16. source freshness threshold;
17. minimum activity requirement;
18. minimum depth or executable-size requirement where applicable;
19. minimum source count;
20. minimum observation count;
21. minimum time coverage;
22. integrity and anomaly checks;
23. deviation rules;
24. source-exclusion rules;
25. normalization method;
26. aggregation method;
27. source weights where applicable;
28. adjustment factor;
29. floor, cap, or other bound;
30. conversion method;
31. precision and rounding;
32. participant-limit interaction;
33. window-capacity interaction;
34. validity interval;
35. recalculation cadence;
36. stale-price treatment;
37. failure modes;
38. approved fallback profile where applicable;
39. exceptional-review authority;
40. price-record authorization method;
41. participant calculation method;
42. payment and settlement treatment;
43. correction method;
44. public-reporting treatment;
45. privacy and security classification;
46. effective date;
47. expiry or reassessment trigger;
48. current status; and
49. current-as-of date.

### Profile Versioning

A new profile version is required when a material field changes, including:

- pricing type;
- source set;
- pair or conversion route;
- observation period;
- sampling method;
- source-quality threshold;
- aggregation method;
- source weight;
- adjustment factor;
- floor or cap;
- precision or rounding;
- validity interval;
- fallback behavior;
- or authorization method.

Historical calculations should retain the profile version used at the time.

A new profile version applies prospectively unless an approved correction or restatement says otherwise.

## Approved Pricing Types

### Fixed Approved Reference

A specifically approved quote is used for a defined window, participant tier, stage, or interval.

This method can be appropriate when:

- no reliable market reference exists;
- market references are immature or fragmented;
- the window is not intended to use live market data;
- a fixed value is required for consistent administration;
- or another approved policy basis applies.

The approval record should identify:

- quote unit;
- fixed quote;
- basis;
- source-vault and window context;
- effective time;
- expiry;
- participant scope;
- review authority;
- and public explanation.

A fixed reference is not an external-market floor or forecast.

### Single-Source Market Reference

The calculation uses one approved source that passes the active profile's quality tests.

The profile should identify:

- exact venue, pool, oracle, feed, or provider;
- network;
- pair;
- quote asset;
- source identifier;
- timestamp rule;
- price field;
- depth or executable-size requirement where applicable;
- and incident treatment.

Single-source use requires clear concentration-risk treatment.

### Time-Weighted Average Price

The calculation uses qualified observations across an approved period.

A standard time-weighted form is:

```text
TWAP = sum(observation price x qualified duration) / total qualified duration
```

The profile should define:

- observation period;
- sampling frequency;
- interpolation treatment;
- missing observations;
- minimum coverage;
- outlier treatment;
- and source-failure treatment.

### Volume-Weighted Average Price

Where supported by sufficient reliable trade data, the profile may use:

```text
VWAP = sum(trade price x qualified trade volume) / total qualified trade volume
```

The profile should define:

- trade-source scope;
- qualifying trades;
- wash-trade or abnormal-activity treatment;
- minimum volume;
- and data-quality requirements.

VWAP should not be used when volume data is materially unreliable for the intended calculation.

### Multi-Source Median

Qualified source references are normalized into one quote unit and the median is selected.

This method can reduce the influence of one extreme source.

The profile should define:

- minimum source count;
- even-source treatment;
- source independence expectations;
- exclusion rules;
- and tie or duplicate-source treatment.

### Multi-Source Weighted Average

Qualified sources are combined using approved weights:

```text
reference price =
sum(source reference x approved source weight)
/ sum(active source weights)
```

The profile should define:

- weight basis;
- minimum active weight;
- re-normalization after source exclusion;
- concentration limit;
- and weight-review cadence.

### Formula-Based Reference

The profile uses an approved formula tied to defined inputs rather than a direct market quote.

The formula should identify:

- every input;
- source;
- unit;
- observation rule;
- transformation;
- parameter;
- bound;
- and failure mode.

### Exceptional Review Profile

Normal pricing pauses and an authorized manual or governance review determines a temporary price record.

The exceptional record should identify:

- failed normal condition;
- reason the window remains supportable;
- replacement basis;
- source evidence;
- quote;
- validity;
- participant treatment;
- authority;
- and public status.

Exceptional review should not become an undocumented routine pricing method.

## Source Qualification

A source must pass every applicable profile test before its observation enters the calculation.

### Source Identity

The process should verify:

- venue, pool, feed, oracle, contract, or provider;
- network;
- base asset;
- quote asset;
- pair;
- decimals;
- source identifier;
- and approved endpoint or contract.

A similarly named token, wrapped asset, bridge representation, unsupported pool, or wrong network should not be treated as the canonical source.

### Freshness

The latest observation should fall within the profile's maximum age.

A stale observation should be excluded or trigger the defined failure mode.

### Availability

The source should meet the required availability over the observation period.

The profile may define:

- minimum successful samples;
- maximum missing interval;
- minimum uptime;
- or continuous coverage requirement.

### Activity

The source should meet the defined minimum:

- trade count;
- update count;
- active-liquidity condition;
- quote activity;
- or other relevant activity measure.

### Depth or Executable Size

Where the source is intended to represent an executable market level, it should meet the approved depth or size threshold.

The test should identify:

- reference size;
- allowed price impact;
- bid and ask treatment;
- pool or order-book method;
- and measurement time.

### Integrity

The process should identify:

- impossible values;
- zero or negative values;
- crossed markets;
- duplicate observations;
- frozen feeds;
- abnormal gaps;
- contract errors;
- decimal errors;
- wrong-pair errors;
- manipulated or wash activity indicators;
- known venue or provider incidents;
- and chain reorganization effects.

### Source Independence

Multiple endpoints from one underlying venue, pool, oracle, or provider should not automatically count as independent sources.

The profile should define the independence standard used for source-count requirements.

### Deviation

A source should remain within the approved deviation from:

- a comparison source;
- the multi-source median;
- a prior qualified interval;
- an approved policy reference;
- or another defined benchmark.

### Source Status

Possible source statuses include:

- qualified;
- qualified with warning;
- excluded stale;
- excluded inactive;
- excluded insufficient depth;
- excluded deviation;
- excluded incident;
- excluded identity mismatch;
- unavailable;
- under review;
- and deprecated.

A source can be useful for general market information while remaining unsuitable for an access-window price.

## Observation Collection

### Observation Record

Each retained observation should identify:

- source identifier;
- source type;
- network;
- pair;
- base and quote assets;
- raw value;
- normalized value;
- timestamp;
- block number where applicable;
- trade or update reference;
- depth or size context where applicable;
- source status;
- qualification result;
- exclusion reason where applicable;
- and evidence reference.

### Collection Timing

The active profile should define whether observations are collected:

- continuously;
- at fixed intervals;
- at blocks;
- at a calculation cutoff;
- over a trailing period;
- or from a signed provider report.

### Missing Observations

The profile should define whether missing observations are:

- ignored within a tolerance;
- carried forward for a limited interval;
- interpolated under an approved rule;
- replaced by another approved source;
- or treated as a calculation failure.

No missing-data treatment should be invented during calculation.

### Outliers

Outlier treatment should be defined before the observation period begins.

Possible methods include:

- fixed deviation threshold;
- median-distance threshold;
- interquartile method;
- source-specific threshold;
- or manual exceptional review.

The method should not exclude data merely because it produces an inconvenient price.

## Normalization and Quote Conversion

Qualified observations may use different quote assets, decimals, units, or routes.

They should be normalized before aggregation.

### Direct Pair

Where FUZE is directly quoted in the target unit:

```text
normalized FUZE quote = qualified direct-pair reference
```

### Intermediate Conversion

Where the source uses an intermediate asset:

```text
FUZE quote in target unit
= FUZE quote in intermediate unit
x intermediate-to-target conversion rate
```

Every conversion leg should identify:

- asset;
- network;
- source;
- timestamp or observation period;
- quality tests;
- precision;
- and failure behavior.

### Inverted Pair

Where the source reports the inverse pair:

```text
FUZE quote = 1 / inverse qualified quote
```

The process should verify units and decimals before inversion.

### Stablecoin Conversion

Stablecoins with similar display values are not automatically interchangeable.

The profile should identify:

- exact stablecoin;
- issuer;
- network;
- native or contract reference;
- bridge or wrapped status;
- intended reference unit;
- deviation threshold;
- and incident treatment.

### Fiat Conversion

A fiat conversion should identify:

- currency;
- FX source;
- observation time;
- business-day treatment;
- weekend or holiday treatment;
- spread or fee treatment;
- and fallback behavior.

### Conversion-Leg Failure

If a required conversion leg fails, the final price should pause or use an already approved fallback method.

The system should not silently assume a one-to-one value.

## Reference-Price Calculation

The general structure is:

```text
qualified observations
-> normalized quote unit
-> approved aggregation method
= reference price
```

### Minimum Coverage

Before calculation, the process should verify:

- minimum source count;
- minimum observation count;
- minimum time coverage;
- minimum active weight;
- and any minimum depth or activity requirement.

### Calculation Record

The calculation should preserve:

- all candidate observations;
- qualified observations;
- excluded observations;
- exclusion reasons;
- normalized values;
- aggregation method;
- intermediate values;
- reference result;
- and quality status.

### No Preferred-Result Selection

FUZE should not calculate several methods and then select whichever result is commercially preferred unless the active profile expressly defines that selection rule before the observation period.

## Adjustment Factors and Bounds

An approved profile may transform the reference price.

### Adjustment Factor

```text
adjusted price = reference price x approved adjustment factor
```

The factor may represent an approved:

- neutral factor;
- premium;
- discount;
- stage adjustment;
- participant-tier adjustment;
- cost adjustment;
- or another disclosed policy parameter.

The profile should identify the factor's purpose and value.

### Fixed Adjustment

Where approved:

```text
adjusted price = reference price + approved fixed adjustment
```

The unit and rationale should be explicit.

### Floor

```text
floor-bounded price = max(adjusted price, approved floor)
```

### Cap

```text
cap-bounded price = min(adjusted price, approved cap)
```

### Floor and Cap

```text
bounded price = min(max(adjusted price, approved floor), approved cap)
```

### Boundary Interpretation

A pricing floor or cap applies only to the access-window calculation.

It does not:

- set an external trading floor;
- limit an external-market price;
- guarantee resale value;
- guarantee liquidity;
- or create a market-support obligation.

### Bound Changes

Changing a factor, floor, cap, or adjustment requires:

- a new profile version;
- approval;
- effective time;
- participant treatment;
- and public notice where material.

## Deviation and Reasonableness Tests

### Source Deviation

```text
deviation =
absolute(source price - comparison price)
/ comparison price
```

The active profile defines:

- comparison reference;
- threshold;
- warning level;
- exclusion level;
- and required response.

### Result Deviation

The final reference or bounded price may be compared with:

- prior valid price;
- multi-source median;
- approved fixed reference;
- external comparison index;
- or another approved benchmark.

### Possible Responses

- accept;
- accept with warning;
- exclude one or more sources;
- collect additional observations;
- recalculate under the same profile;
- pause;
- activate an approved fallback profile;
- or escalate to exceptional review.

### Reasonableness Review

A manual reasonableness review may confirm that:

- units and decimals are correct;
- no pair is inverted incorrectly;
- conversions are current;
- bounds applied correctly;
- the result is consistent with the profile;
- and no known incident invalidates the record.

The review should not replace the deterministic formula with an undocumented preference.

## Precision, Rounding, and Residual Treatment

The profile should specify:

- source-price precision;
- normalized-price precision;
- reference-price precision;
- final-price precision;
- FUZE quantity precision;
- payment precision;
- rounding direction at each stage;
- minimum allocation;
- minimum payment;
- residual consideration treatment;
- residual FUZE-capacity treatment;
- and maximum tolerated arithmetic difference.

### Participant Quantity

```text
preliminary FUZE quantity
= accepted consideration / valid final price
```

The preliminary amount is rounded according to the active profile and then checked against:

- participant minimum;
- participant maximum;
- tier limit;
- linked-participant limit;
- remaining window capacity;
- and allocation method.

### Accepted Consideration

```text
accepted consideration
= verified payment
- ineligible amount
- excess amount
- refundable amount
- reversed amount
- other excluded amount under the active terms
```

### Determinism

The same inputs, profile version, and calculation order should produce the same result.

Rounding should not be changed manually for individual participants without an approved correction or exception record.

### Residual FUZE

Residual FUZE caused by rounding may be:

- retained as unused capacity;
- assigned under a published residual method;
- carried into a later stage;
- or returned to the source allocation.

The treatment should be published before allocation.

## Price-Record Authorization

A price used for participant allocation should be stored as an authorized record.

### Required Price-Record Fields

1. price-record identifier;
2. window identifier and version;
3. pricing-profile identifier and version;
4. pricing type;
5. quote unit;
6. calculation currency;
7. source identifiers;
8. raw observation references;
9. normalized observations;
10. excluded observations and reasons;
11. observation start and cutoff;
12. reference calculation;
13. adjustment factor or fixed adjustment;
14. floor and cap;
15. conversion legs;
16. rounding and precision;
17. final price;
18. valid-from time or block;
19. expiry time or block;
20. source-quality results;
21. deviation results;
22. warnings;
23. calculation owner;
24. reviewer;
25. authorization method;
26. authorization time;
27. evidence hash, transaction, report, or immutable-log reference;
28. correction state;
29. supersession state;
30. current status; and
31. current-as-of date.

### Authorization Methods

Possible methods include:

- approved human sign-off;
- multisignature approval;
- governance decision;
- timelock operation;
- signed provider record;
- role-controlled publication;
- verified contract calculation;
- or another approved method.

### Tamper Resistance

The authorization method should prevent an unapproved operator from changing:

- inputs;
- formula;
- final price;
- validity interval;
- or profile version

after participants rely on the record.

### Correction Linkage

A corrected price record should preserve the original identifier and link to the replacement record.

## Validity Interval

Every active price record should have a defined validity interval.

The record should show:

- calculation time;
- observation cutoff;
- valid-from time or block;
- expiry time or block;
- timezone;
- profile version;
- current status;
- and stale-price treatment.

### Participant-Time Rule

The active window should define whether the applicable price is determined by:

- application completion time;
- allocation approval time;
- payment-instruction time;
- payment-receipt time;
- payment-finality time;
- settlement time;
- or another approved event.

The rule should be consistent for similarly situated participants.

### Expired Price

An expired price should not be applied to a new participant action unless the active terms explicitly preserve it for a prior valid instruction.

### Delayed Transaction

The window should define treatment when:

- a participant initiated payment before expiry;
- the network confirmed after expiry;
- a provider delayed settlement;
- or manual review completed after expiry.

### Recalculation Cadence

A longer validity interval can simplify participant experience but increases exposure to changing inputs.

A shorter interval improves recency but creates more operational and settlement complexity.

The active profile should make the tradeoff explicit.

## Participant Calculation

The access window applies an active price record only after the required participant checks.

### Required Inputs

- eligible participant status;
- window version;
- participant tier or limit;
- verified payment or approved consideration;
- active price-record identifier;
- remaining window capacity;
- allocation method;
- and rounding rules.

### Calculation Sequence

```text
verified consideration
-> excluded, refundable, or excess amount treatment
-> accepted consideration
-> divide by active final price
-> deterministic rounding
-> participant-limit check
-> linked-participant-limit check
-> remaining-capacity check
-> allocation-method adjustment
-> final participant allocation
```

### Capacity Constraint

```text
final participant allocation
<= remaining approved window capacity
```

### Participant Limit

```text
final participant allocation
<= applicable participant, tier, group, or program limit
```

### Over-Capacity Demand

If approved demand exceeds remaining capacity, the access-window allocation method controls:

- pro-rata scaling;
- queueing;
- tier priority;
- waitlisting;
- randomization where supported;
- or another published treatment.

Pricing should remain separate from allocation priority.

### Participant Calculation Record

The record should identify:

- participant private reference;
- payment or consideration record;
- price-record identifier;
- accepted consideration;
- preliminary FUZE amount;
- rounding effect;
- limit effect;
- capacity effect;
- allocation-method effect;
- final allocation;
- refund or excess amount;
- reviewer or rule version;
- current status;
- and correction state.

## Payment and Settlement Interaction

### Payment Record

The payment record should identify:

- participant private reference;
- payment instruction;
- asset;
- network;
- expected amount;
- received amount;
- transaction or provider reference;
- confirmation or finality;
- payment time;
- applicable price-record identifier;
- accepted amount;
- excess, shortfall, refund, reversal, or fee;
- allocated FUZE;
- settlement state;
- release state;
- and correction state.

### Fees

Network fees, provider fees, conversion fees, custody fees, or other charges should have an explicit treatment.

They should not appear as unexplained differences between payment and allocation.

### Overpayment

The active window should define whether overpayment is:

- refunded;
- accepted only up to the participant limit;
- held pending instruction;
- or rejected.

### Underpayment

The active window should define whether underpayment causes:

- remediation;
- proportional reduction;
- reduced allocation;
- rejection;
- or refund.

### Failed or Late Payment

Failed or late payment should follow the active window terms.

A discretionary exception requires an approved record identifying participant, reason, authority, capacity effect, and reporting effect.

### Settlement

Settlement requires agreement among:

```text
approved participant allocation
<-> accepted consideration
<-> active price record
<-> source-vault commitment
<-> proceeds record
<-> refund or residual treatment
```

Payment verification alone does not establish settlement if another element remains unresolved.

## Stablecoin, Fiat, Bridge, and Conversion Treatment

### Stablecoin Identity

The active profile and payment instruction should identify:

- exact asset;
- issuer;
- network;
- native or contract reference;
- decimals;
- bridge or wrapped status;
- and intended quote relationship.

### Stablecoin Incident

Pricing or settlement may pause when a supported stablecoin experiences:

- material depeg;
- freeze or blacklist event;
- issuer incident;
- bridge incident;
- custody restriction;
- contract incident;
- or network outage.

### Wrong Asset or Network

An unsupported stablecoin, wrong network, wrong contract, wrapped asset, or bridge representation should not be silently treated as the approved payment asset.

Recovery or refund depends on technical feasibility and the active terms.

### Fiat Payment

A fiat route should define:

- currency;
- provider or institution;
- FX method where applicable;
- settlement time;
- fees;
- chargeback risk;
- payment reversal;
- and reconciliation.

### Bridge Risk

A bridge-based payment or source should identify:

- canonical asset;
- representation;
- backing;
- bridge operator;
- confirmation method;
- and incident treatment.

## Failure, Fallback, and Pause Rules

Pricing should enter its defined failure mode when:

- required sources are unavailable;
- observations are stale;
- minimum source count fails;
- minimum observation coverage fails;
- depth or activity falls below the required threshold;
- deviation exceeds the approved threshold;
- a source, oracle, venue, pool, network, stablecoin, bridge, or provider has a material incident;
- normalization or conversion fails;
- the calculation produces an invalid value;
- the price record cannot be authorized;
- the price record is expired;
- payment or allocation systems cannot apply the price consistently;
- source-vault capacity is no longer supportable;
- or an authorized role suspends pricing.

### Possible Failure Modes

- retry within the same profile;
- wait for additional observations;
- exclude a failed source and recalculate if minimum coverage remains;
- use a pre-approved fallback source;
- use a pre-approved fallback profile;
- pause new applications;
- pause new payment instructions;
- pause allocation;
- pause settlement;
- pause release;
- or enter exceptional review.

### Fallback Requirements

A fallback should identify:

- triggering condition;
- source or method;
- effective time;
- validity;
- participant treatment;
- authority;
- and public status.

### No Silent Substitution

The system should not silently:

- change a source;
- change a quote asset;
- change a conversion route;
- change an observation period;
- change an aggregation method;
- change a source weight;
- change a floor or cap;
- change a validity interval;
- or change a rounding rule.

### Pause Scope

A pricing pause should state whether it affects:

- new calculations;
- existing valid records;
- applications;
- payment instructions;
- payments in transit;
- allocations;
- settlements;
- claims;
- releases;
- or only public display.

### Reactivation

Reactivation should require:

- issue containment;
- source or system restoration;
- renewed quality checks;
- recalculation where needed;
- authorization of a new price record;
- affected-participant treatment;
- reconciliation;
- and public status update.

## Recalculation, Correction, and Restatement

### Normal Recalculation

A new interval produces a new price record under the same approved profile.

A later market movement does not make a previously valid record erroneous.

### Correction

A correction is required when a material error exists in:

- source identity;
- observation;
- timestamp;
- pair;
- decimals;
- conversion;
- formula;
- weight;
- adjustment;
- floor or cap;
- rounding;
- validity;
- authorization;
- participant application;
- or published record.

### Correction Record

The correction record should identify:

1. affected profile and price records;
2. affected validity intervals;
3. prior inputs;
4. corrected inputs;
5. prior result;
6. corrected result;
7. affected participants;
8. affected payments;
9. affected allocations;
10. affected refunds or shortfalls;
11. affected source-vault capacity;
12. affected proceeds;
13. participant treatment;
14. authority;
15. publication time;
16. downstream reports updated;
17. current status; and
18. archive reference.

### Participant Treatment

Possible treatment includes:

- no change where the original record remains valid;
- additional FUZE allocation;
- reduced allocation before release;
- refund;
- additional payment request where legally and contractually supported;
- cancellation;
- claim correction;
- release correction;
- or another approved remedy.

Irreversible transfers may limit available remedies.

### Restatement

A restatement may be required when a methodology change or material error affects prior published pricing reports.

The prior version should remain visible and marked as superseded.

### No Retroactive Repricing for Market Movement

Ordinary market movement after a valid calculation should be handled by the next interval, not by rewriting the past price.

## Pricing Reconciliation

### Price-Record Reconciliation

The authorized price record should reconcile:

```text
qualified observations
-> normalized observations
-> reference price
-> adjustment
-> bounds
-> conversion
-> rounding
= final active price
```

### Participant Allocation Reconciliation

```text
accepted consideration
/ active final price
= preliminary FUZE quantity
```

Then:

```text
preliminary FUZE quantity
+/- rounding, participant-limit, capacity, and allocation-method effects
= final participant allocation
```

### Window-Level Reconciliation

The pricing report should reconcile:

- price intervals;
- valid price records;
- applications using each record;
- accepted consideration;
- preliminary FUZE quantities;
- final participant allocations;
- rounding residuals;
- participant-limit reductions;
- capacity reductions;
- refunds;
- corrections;
- and unused capacity.

### Proceeds Reconciliation

```text
verified consideration received
- refunds
- reversals or chargebacks
- approved fees
- approved conversions or transfers
+/- corrections
= reconciled net proceeds or closing proceeds balance
```

### Unit Separation

The report should keep separate:

- FUZE quantities;
- stablecoin amounts;
- fiat amounts;
- fees;
- refunds;
- FX values;
- Platform Credits;
- participant counts;
- price intervals;
- and accounting values.

## Public Reporting

A public pricing report may include:

- report identifier and version;
- access-window identifier and version;
- source allocation;
- pricing-profile identifier and version;
- pricing type;
- calculation currency;
- quote unit;
- source classes;
- observation period;
- source-quality rules;
- minimum coverage;
- normalization and aggregation method;
- adjustment factor and bounds where public;
- conversion method;
- precision and rounding;
- final price;
- validity interval;
- quality and deviation status;
- fallback or exceptional-review status;
- calculation hash or evidence reference;
- total accepted consideration;
- total FUZE allocated;
- residual amounts;
- pauses;
- corrections;
- methodology limitations;
- review status;
- and current-as-of date.

### Public Evidence

Public evidence may include:

- source classes;
- approved source identifiers where appropriate;
- observation references;
- price-record hash;
- governance or approval reference;
- transaction or immutable-log reference;
- methodology;
- and correction history.

### Private Information

Public reporting should not expose:

- participant identity;
- private payment details;
- private account or wallet-person mappings;
- credentials;
- private vendor terms;
- proprietary source credentials;
- private keys;
- recovery material;
- exact security procedures;
- confidential legal, accounting, tax, audit, or compliance records;
- or private market strategy.

### Status Vocabulary

Public pricing status may show:

- proposed;
- under review;
- approved;
- collecting inputs;
- qualified;
- calculated;
- active;
- expiring;
- expired;
- paused;
- exceptional review;
- corrected;
- superseded;
- and archived.

## Privacy, Security, and Record Retention

The pricing evidence package should retain, as applicable:

- approved profile and all versions;
- source registry;
- source agreements or provider records;
- raw observations;
- normalized observations;
- excluded observations and reasons;
- calculation logs;
- quality and deviation tests;
- authorization evidence;
- price records;
- participant calculations;
- payment records;
- refunds;
- settlements;
- incidents;
- overrides;
- corrections;
- public reports;
- and archive references.

Retention should follow the applicable privacy, security, legal, accounting, tax, compliance, contractual, and operational requirements.

Access to raw participant and provider records should follow least-necessary access.

## Separation from Adjacent Systems

| System or process | Primary role | Why it remains separate |
|---|---|---|
| Public vault access window | Defines who can participate, when, under which limits, and through which settlement and release route | The window does not determine the price formula by itself |
| Vault access pricing mechanism | Defines qualified inputs, formula, bounds, authorization, validity, and correction | Pricing does not create eligibility or allocation authority |
| Public vault visibility | Publishes approved records and evidence | Visibility does not authorize pricing or access |
| Vault-by-vault release rules | Defines source-allocation release authority | A valid price does not authorize token release |
| Controlled circulation | Defines post-release token state and circulation treatment | A pricing record does not establish circulation |
| Stablecoin compensation | Settles approved business obligations | Participant consideration is not compensation |
| Platform Credits | Product-consumption units | Platform Credits are not a FUZE market quote or payment asset unless separately supported |
| Approved distributable value | Reviewed value from product-revenue pools | Access-window proceeds are not automatically approved distributable value |
| Liquidity and listing policy | Governs DEX, CEX, market-making, and market structure | Window pricing does not establish listing or liquidity |
| Market price and demand boundary | Defines public market-language limits | Access price is not a forecast or market-support promise |

## Status and Evidence

This paper defines the pricing mechanism for approved access windows.

It does not independently prove that any current pricing profile, price record, access window, payment route, participant allocation, token release, market price, liquidity deployment, or listing is active.

| Status claim | Evidence direction |
|---|---|
| Profile proposed | Draft profile, window, type, sources, method, bounds, owner, and status |
| Profile approved | Exact version, source set, formula, thresholds, authority, effective date, and decision |
| Source qualified | Source identity, freshness, activity, depth, integrity, deviation, observation period, and result |
| Price calculated | Qualified inputs, normalized values, formula, intermediate values, final result, and calculation time |
| Price authorized | Exact price record, profile version, validity, authority, evidence reference, and status |
| Price active | Authorized record, valid-from and expiry, source-quality status, monitoring, and current status |
| Participant calculation complete | Eligibility, accepted consideration, price record, limits, capacity, rounding, final allocation, and status |
| Payment verified | Asset, network, amount, destination, transaction or provider reference, finality, and participant linkage |
| Allocation settled | Participant allocation, accepted consideration, price record, source commitment, proceeds, and reconciliation |
| Pricing paused | Trigger, scope, effective time, affected records, participant treatment, and reactivation conditions |
| Fallback activated | Trigger, pre-approved method or exceptional decision, quote, validity, authority, and notice |
| Price corrected | Original record, error, corrected inputs and result, affected participants, treatment, authority, and update |
| Profile superseded | Prior and new versions, effective time, affected future records, and historical treatment |
| Pricing archived | Final profile state, records, reports, corrections, archive location, and current status |

The following do not independently establish an approved or active price:

- this paper;
- a market screenshot;
- a single trade;
- an explorer quote;
- a wallet transfer;
- a pool price;
- an exchange discussion;
- a prior-round price;
- a private message;
- an internal spreadsheet;
- code;
- a repository;
- or a social-media post.

## Pricing, Access, Release, Market, and Outcome Separation

The following remain separate:

- pricing-profile proposal;
- pricing-profile approval;
- source observation;
- source qualification;
- price calculation;
- price authorization;
- price validity;
- access-window activation;
- application;
- eligibility;
- payment instruction;
- payment verification;
- participant allocation;
- settlement;
- claim funding;
- claimability;
- token release;
- lock or vesting;
- circulation;
- DEX access;
- CEX discussion;
- CEX application;
- CEX approval;
- listing;
- deposits enabled;
- withdrawals enabled;
- trading live;
- liquidity;
- depth;
- spread;
- volume;
- token demand;
- market price;
- income;
- revenue share;
- and financial return.

A fixed reference, TWAP, VWAP, multi-source calculation, adjustment factor, floor, cap, or active access-window price does not guarantee:

- future market price;
- resale value;
- DEX access;
- CEX listing;
- active liquidity;
- market depth;
- narrow spread;
- trading volume;
- token demand;
- price support;
- price appreciation;
- income;
- revenue share;
- or financial return.

## Public Boundary

This paper publishes the pricing-profile, source qualification, observation, normalization, reference calculation, adjustment, bounds, deviation, precision, authorization, validity, participant calculation, settlement interaction, failure, correction, reporting, privacy, and archive framework.

It does not publish or establish current:

- active access window;
- active pricing profile;
- active price record;
- FUZE access price;
- source venue or provider;
- floor or cap;
- adjustment factor;
- observation period;
- payment asset;
- payment address;
- participant allocation;
- proceeds amount;
- refund amount;
- release amount;
- circulating supply;
- DEX activation;
- CEX application;
- CEX approval;
- listing;
- deposits or withdrawals;
- trading status;
- liquidity;
- depth;
- spread;
- volume;
- token demand;
- token price;
- income;
- revenue share;
- profitability;
- or financial return

unless those details are separately approved and supported by a current access-window notice, pricing profile, authorized price record, payment instruction, participant calculation, settlement record, release report, market-operation report, specialist paper, or public status record.

Every actual pricing process remains subject to its controlling access-window, allocation, vault, treasury, legal, accounting, tax, compliance, sanctions, jurisdiction, technical, security, privacy, custody, payment, refund, release, circulation, reporting, and support requirements.

## Key Takeaways

- FUZE vault-access pricing is a deterministic control process for one approved payment-based access window, not a general market-price system.
- Access-window approval, pricing-profile approval, price calculation, price authorization, participant allocation, settlement, release, and circulation are separate states.
- Every active profile should define its quote unit, sources, observation method, qualification rules, normalization, aggregation, adjustment, bounds, precision, validity, failure mode, and authority before use.
- Sources should pass identity, freshness, availability, activity, depth, integrity, independence, and deviation tests applicable to the profile.
- Fixed reference, TWAP, VWAP, multi-source median, weighted average, formula-based, and exceptional-review profiles require different evidence and controls.
- Every conversion leg should use an approved source, timestamp, precision, and quality test; similar stablecoin display values do not make assets interchangeable.
- Adjustment factors, floors, and caps affect only the access-window calculation and do not create an external-market price floor or support commitment.
- Precision, rounding, participant limits, window capacity, and residual treatment should be deterministic and published.
- Every participant allocation should retain the exact active price-record identifier and calculation effects.
- Pricing should pause rather than silently changing sources, methods, periods, weights, bounds, or validity when required inputs fail.
- Corrections should preserve original records and identify affected participants, payments, allocations, refunds, releases, and reports.
- An active access-window price does not guarantee listing, liquidity, depth, spread, volume, demand, price support, income, revenue share, or financial return.
