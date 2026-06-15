# FUZE Vault Access Pricing Mechanism

## Executive Summary

The FUZE Vault Access Pricing Mechanism defines how an approved Public Vault Access Window can calculate, validate, publish, and settle its access price. It separates the policy decision to open a window from the technical process used to produce a reproducible price.

Each active pricing profile must identify its unit of account, reference sources, observation period, source-quality rules, calculation method, floor or cap where approved, adjustment factor, rounding, validity period, deviation limits, and failure behavior. The resulting price should be traceable to a signed or otherwise authorized calculation record.

Market data can serve as an input only when it is sufficiently current and reliable for the approved profile. Early or disrupted conditions can instead use a specifically approved fixed reference. When required inputs fail validation, the pricing process pauses rather than silently substituting a new method.

This mechanism applies only to a window activated under [FUZE Public Vault Access Windows](17-FUZE_PUBLIC_VAULT_ACCESS_WINDOWS_PUBLIC.md). It publishes no current FUZE price and provides no forecast of market value.

---

## 1. Pricing Objective

An access price should be:

- authorized before use;
- reproducible from stated inputs;
- resistant to stale or abnormal data;
- consistent across eligible participants in the same pricing interval;
- bounded by approved policy parameters;
- recorded with enough evidence for later review.

The mechanism should answer who approved the profile, which data was used, how the calculation worked, when the result was valid, and why any override or pause occurred.

---

## 2. Scope

This paper governs the calculation of FUZE quantity or consideration for a specific approved vault window.

It covers:

- fixed approved references;
- single-source and multi-source market references;
- time-weighted calculations;
- floors, caps, and adjustment factors;
- source qualification and deviation tests;
- stablecoin conversion and payment treatment;
- signed price records;
- recalculation, pause, correction, and reporting.

It does not set window eligibility, source-vault authority, participant limits, token release conditions, or proceeds use. Those fields belong to the active window record.

---

## 3. Pricing Profile

Every window using payment should reference one approved pricing profile.

| Profile field | Required definition |
|---|---|
| Profile identifier | Stable name and version |
| Window identifier | Access window authorized to use the profile |
| Quote unit | Stablecoin, fiat-equivalent unit, or other approved denomination |
| Reference type | Fixed approved, spot reference, TWAP, or multi-source calculation |
| Sources | Approved venues, pools, feeds, or signed policy records |
| Pair and route | FUZE quote pair and any conversion path |
| Observation period | Start, end, sampling method, and timezone or block range |
| Source tests | Freshness, depth, activity, deviation, and availability requirements |
| Adjustment | Approved multiplier or fixed adjustment |
| Bounds | Floor, cap, or other approved limit |
| Precision | Decimal places and rounding direction |
| Validity | Time or block interval for use |
| Failure mode | Pause, retry, alternate approved profile, or manual review |
| Authority | Approver and signer or publication method |

Profile changes require a new version. Historical calculations should retain the profile version used at the time.

---

## 4. Pricing Profiles

### Fixed approved reference

A specifically approved quote is used for a defined window or interval.

This profile can be appropriate when market references are absent, immature, fragmented, or unsuitable. Its approval record should state the basis, quote unit, validity period, source-vault context, and review authority.

### Market-reference profile

The calculation uses a current price from an approved market source that passes the profile's quality tests.

This profile should identify the exact venue, pair, route, timestamp rule, and treatment of spreads or fees.

### Time-weighted profile

The calculation uses observations across an approved period to reduce dependence on one instant.

The profile should define sampling frequency, missing observations, weighting, and the minimum usable data coverage.

### Multi-source profile

The calculation combines qualified observations from more than one approved source.

The profile should state how sources are normalized, weighted, filtered, and combined. A median, weighted average, or another method can be used only when the active version defines it.

### Exceptional review profile

Pricing is paused pending an approved manual decision because normal inputs have failed. Any replacement quote requires its own basis, authorization, validity, and public status.

---

## 5. Source Qualification

A source must pass qualification before its observation enters a calculation.

### Identity

The venue, pool, feed, contract, pair, network, and quote asset must match the approved profile.

### Freshness

The latest observation must fall within the profile's maximum age. A source beyond that age is stale.

### Activity

The source should meet the defined minimum activity, trade, or update requirement for the observation period.

### Depth

Where market depth matters, the source should meet the approved liquidity or executable-size threshold.

### Integrity

The process should detect abnormal gaps, crossed values, impossible quantities, duplicated observations, data-feed errors, or known source incidents.

### Deviation

The source should remain within the approved difference from other qualified sources or from the profile's comparison reference.

A source can be valid for public market information yet unsuitable for an access-window calculation. Qualification is profile-specific.

---

## 6. Reference Calculation

The general structure is:

```text
Qualified observations
-> normalized quote unit
-> approved aggregation method
= reference price
```

For a time-weighted profile:

```text
Reference price =
sum(observation price x observation duration)
/ total qualified duration
```

For a weighted multi-source profile:

```text
Reference price =
sum(source reference x approved source weight)
/ sum(active source weights)
```

Weights, observation periods, and minimum coverage are parameters, not assumptions. The active profile must provide them.

If too few sources or observations remain after qualification, the calculation enters its defined failure mode.

---

## 7. Adjustment and Bounds

An approved profile can transform the reference price.

```text
Adjusted price = reference price x approved adjustment factor
```

The factor can remain neutral or implement a specifically approved premium or other policy adjustment. Its purpose and value should be visible in the window record.

Where a lower bound applies:

```text
Bounded price = max(adjusted price, approved floor)
```

Where an upper bound also applies:

```text
Bounded price = min(max(adjusted price, approved floor), approved cap)
```

Floors and caps control the window calculation only. They do not set or protect prices on an external venue.

Changes to a factor, floor, or cap require profile versioning and approval before they affect participants.

---

## 8. Deviation Tests

Deviation tests determine whether a result is credible enough to publish.

For a source against the comparison reference:

```text
Deviation =
absolute(source price - comparison price)
/ comparison price
```

The profile defines the permitted threshold and required response.

Possible responses include:

- exclude the source and recalculate;
- require additional observations;
- shorten or extend the observation period under an already approved rule;
- pause publication;
- escalate to exceptional review.

The system should avoid selecting whichever source produces the preferred result. Source inclusion follows the profile established before calculation.

---

## 9. Quote Conversion

A reference can require conversion when the source pair differs from the window's quote unit.

```text
FUZE quote in target unit =
FUZE reference in intermediate unit
x intermediate-to-target conversion rate
```

Every conversion leg needs its own approved source, timestamp, precision, and quality tests. The final record should preserve the original observations and converted result.

Stablecoin denominations should identify the exact asset and network. Similar display values do not make different stablecoins, wrapped assets, or custody balances interchangeable.

When a conversion asset materially departs from its intended reference or encounters a custody or network incident, the profile's failure rule applies.

---

## 10. Precision and Rounding

The profile should specify:

- price precision;
- token-quantity precision;
- payment precision;
- rounding direction;
- treatment of residual amounts;
- minimum executable payment or allocation.

The participant calculation is:

```text
FUZE quantity =
eligible consideration
/ valid bounded price
```

The result is rounded according to the active profile and then checked against participant and window limits.

Rounding should be deterministic. The same inputs and profile version should produce the same price and quantity.

---

## 11. Validity Interval

Each published price has a defined validity interval.

The price record should show:

- calculation time;
- observation cutoff;
- valid-from time or block;
- expiry time or block;
- profile version;
- status.

Applications or payments received after expiry use the next valid price or follow the window's expiration treatment. A delayed transaction should not silently inherit an expired quote.

Longer validity can simplify participant experience but increases exposure to changing inputs. Shorter validity improves recency but requires more frequent calculation and settlement handling. The active profile makes that tradeoff explicit.

---

## 12. Signed Price Record

A price used for allocation should be stored as an authorized record.

| Field | Content |
|---|---|
| Price record ID | Unique calculation identifier |
| Window and profile | Window ID and profile version |
| Quote | Final price, unit, and precision |
| Inputs | Source identifiers and observation references |
| Calculation | Reference, adjustment, bounds, conversion, and rounding |
| Validity | Start and expiry |
| Quality status | Freshness, depth, coverage, and deviation results |
| Authority | Signer, multisignature, governance, contract, or approved publisher |
| Evidence | Hash, transaction, report, or immutable log reference |

The authorization method should prevent an unapproved operator from changing a price after participants rely on it.

---

## 13. Participant Calculation

The window applies the valid price record after eligibility and payment checks.

```text
Accepted consideration =
verified payment
- ineligible, excess, failed, or refundable amount
```

```text
Preliminary FUZE amount =
accepted consideration
/ valid price
```

The preliminary amount is then subject to participant limits, remaining window capacity, allocation method, and rounding.

If approved demand exceeds capacity, the allocation method in the window record determines scaling or queue treatment. Pricing should remain separate from allocation priority.

---

## 14. Payment and Settlement

The payment record should identify:

- participant or permissioned account reference;
- payment asset and network;
- expected and received amount;
- transaction or custody evidence;
- price record used;
- allocated FUZE;
- excess, refund, or shortfall;
- settlement and release status.

Network fees, conversion costs, payment-provider fees, or custody charges require an explicit treatment. They should not appear as unexplained differences between consideration and allocation.

Proceeds reporting can use public categories while invoices, customer identity, account information, and detailed treasury records remain permissioned.

---

## 15. Failure and Pause Rules

Pricing should pause when:

- required sources are unavailable or stale;
- data coverage falls below the profile minimum;
- deviation exceeds the approved threshold;
- a source, oracle, network, stablecoin, or venue has a material incident;
- the signed record is missing, invalid, or expired;
- payment or allocation systems cannot apply the price consistently;
- an approved authority suspends the window.

The public status should identify whether pricing, applications, payment, allocation, or release is paused. Submitted records should retain their applicable terms and status.

An alternate profile can activate only when it was pre-approved for the condition or receives a new exceptional approval.

---

## 16. Correction and Recalculation

A correction is required when an input, formula, parameter, conversion, rounding rule, or published record was wrong.

The correction record should include:

1. affected price records and validity intervals;
2. prior and corrected inputs;
3. prior and corrected results;
4. affected applications, payments, and allocations;
5. participant treatment;
6. approval and publication time;
7. downstream reports updated.

A market movement after a valid calculation is not a calculation error. Repricing follows the next interval rather than rewriting a previously valid record.

---

## 17. Reporting

A public pricing report can show:

- window and source allocation;
- profile identifier and pricing type;
- quote unit and validity interval;
- approved source classes;
- observation and aggregation method;
- adjustment factor and bounds where public;
- source-quality and deviation status;
- final price and calculation hash;
- total consideration and FUZE allocated;
- pauses, overrides, and corrections.

The report should make the method understandable without publishing private participant data, credentials, protected vendor terms, or security procedures.

---

## 18. Boundaries

The mechanism governs a specific access-window calculation. It is separate from general market price, venue liquidity, token demand, and future resale conditions.

A floor is a window parameter, a TWAP is a historical reference, and an adjustment is a policy input. None provides a price target or market-support commitment.

Market communication boundaries are maintained in [FUZE Market Price and Demand Boundary](22-FUZE_MARKET_PRICE_AND_DEMAND_BOUNDARY_PUBLIC.md). DEX-first and possible later CEX considerations remain in the [FUZE Liquidity and Listing Policy](21-FUZE_LIQUIDITY_AND_LISTING_POLICY_PUBLIC.md).

---

## Conclusion

FUZE vault-access pricing depends on an approved profile, qualified inputs, deterministic calculation, explicit bounds, fixed precision, a validity interval, and an authorized price record.

This structure lets participants and reviewers reproduce how a window price was produced. It also gives FUZE a clear pause and correction route when data quality, settlement, or authorization fails.
