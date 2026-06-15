# FUZE Approved Distributable Value Model

## Executive Summary

Approved distributable value is a controlled accounting and governance status applied to value from a defined FUZE product-revenue pool after confirmation, reconciliation, deductions, reserves, review, and authorization.

The model begins with a named product pool and reporting period. Source receipts are matched to approved offers and fulfilled product activity. Refunds, disputes, fees, taxes, delivery costs, partner obligations, operating needs, and approved reserves are then considered under the applicable treatment. The resulting calculation enters review rather than becoming automatically available.

An approval record identifies the pool, period, source currency or asset, calculation version, approved amount, treasury location, reviewer decisions, restrictions, and reporting status. If wallet-based participation is inactive, an approved calculation does not create a claim process.

This paper owns the calculation lifecycle and value ledger. It does not define wallet eligibility, snapshots, claim mechanics, or the broader activation-gate decision.

---

## 1. Model Objective

The model prevents several different business values from being described as though they were interchangeable.

It distinguishes:

- customer payments from recognized product revenue;
- gross product revenue from reconciled product revenue;
- reconciled product revenue from an amount submitted for approval;
- an approved amount from treasury movement;
- treasury movement from a claimable amount under an active mechanism.

This separation supports accurate accounting, treasury control, governance review, and public communication.

---

## 2. Core Definitions

### Source receipt

A payment or settlement event recorded through an approved product channel. A receipt requires business context before it can be classified as product revenue.

### Confirmed product revenue

Revenue linked to an approved offer, customer or authorized account, fulfilled product or service activity, payment evidence, and applicable period.

### Reconciled product revenue

Confirmed product revenue after corrections, refunds, chargebacks, failures, timing adjustments, and other required reconciliation entries.

### Net pool value

The value remaining after the approved deduction and cost treatment for the defined product-revenue pool and period.

### Reserved value

Value retained for approved obligations, operating continuity, uncertainty, risk, support, tax, refunds, or another documented purpose.

### Candidate distributable value

The calculated amount submitted for legal, accounting, treasury, audit or assurance, governance, and reporting review.

### Approved distributable value

Candidate value that has completed the required review and received formal approval for a stated pool, period, amount, asset, purpose, and mechanism scope.

### Claimable or distributable amount

The amount, if any, made available through an active mechanism after eligibility, treasury, technical, jurisdiction, and claim-period conditions are applied.

These statuses should not be collapsed into a single label such as “revenue available.”

---

## 3. Product-Revenue Pool

Every calculation begins with a defined pool.

The pool specification should include:

| Field | Required content |
|---|---|
| Pool identifier | Stable name and version |
| Product scope | Products, offers, services, or modules included |
| Entity and account scope | Relevant operating entity and approved source accounts |
| Reporting period | Start, end, cutoff, and timezone |
| Revenue basis | Applicable recognition or classification method |
| Payment routes | Included fiat, invoice, card, stablecoin, partner-funded, or other routes |
| Platform Credit treatment | Purchased, included, granted, promotional, consumed, reversed, or expired treatment |
| Fulfillment evidence | Records required to support product delivery |
| Currency or asset basis | Calculation unit and conversion method where needed |
| Cost and deduction policy | Categories and allocation method |
| Reserve policy | Required reserve categories and approval |
| Owner | Product, finance, treasury, and reviewer responsibilities |

Pools should be narrow enough to reconcile. “All FUZE revenue” is insufficient when products, entities, periods, payment routes, fulfillment evidence, and cost structures differ.

Not every product-revenue pool must enter this model. FUZE can retain revenue for product delivery, operations, reserves, growth, or other approved purposes.

---

## 4. Period Close

The period close establishes the source dataset for calculation.

### 4.1 Capture

FUZE collects the approved offer, invoice, payment, settlement, product usage, fulfillment, Platform Credit, refund, dispute, fee, and support records for the period.

### 4.2 Match

Receipts are matched to the relevant product, offer, customer or account, fulfillment record, payment route, and reporting period.

### 4.3 Classify

Each record receives an approved classification such as confirmed revenue, deferred or pending treatment, refund, failed payment, internal transfer, financing receipt, tax, pass-through amount, or another defined category.

### 4.4 Reconcile

Product, payment, treasury, and finance records are compared. Differences receive an explanation, correction, or unresolved-item status.

### 4.5 Lock

The calculation dataset is versioned after the close owner confirms the cutoff and open-item treatment. Later corrections use controlled adjustment entries rather than silently changing the source data.

---

## 5. Calculation Structure

The model can be represented as:

```text
Confirmed product revenue
- refunds, reversals, chargebacks, and failed settlement
- approved taxes, fees, and pass-through obligations
- product delivery and pool-specific costs
- partner, vendor, contributor, and service obligations
- approved operating and risk reserves
+/- documented period and correction adjustments
= candidate distributable value
```

This is a control structure, not a fixed accounting rule. The exact treatment depends on the product, entity, contract, asset, jurisdiction, reporting period, and professional review.

The calculation should avoid double deductions. A cost included in product delivery should not be deducted again through a broad operating allocation without a defined reason.

Where costs support more than one pool, the allocation method should be documented and applied consistently. Possible methods can use direct attribution, measured usage, transaction count, service time, or another supportable driver.

---

## 6. Excluded Sources

The following sources remain outside a product-revenue pool unless an approved specification and professional review establish a different treatment:

| Source | Reason for separate treatment |
|---|---|
| Equity, seed, or other financing receipts | Capital funding rather than ordinary product delivery |
| Token allocation or token-sale-related proceeds | Token or fundraising activity with separate policies |
| Internal treasury transfers | Movement between controlled accounts rather than external revenue |
| Unrealized token or asset value | Market valuation without a settled product transaction |
| Liquidity-pool balances and market inventory | Market-structure assets rather than product revenue |
| Customer deposits or refundable balances | Potential obligation pending fulfillment or final treatment |
| Unpaid invoices and failed settlement | No confirmed receipt |
| Promotional or granted Platform Credits | Product-use allowance without the same purchase record |
| Game scores, simulated balances, or internal resources | Product mechanics rather than recognized external value |
| Restricted, disputed, fraudulent, or unidentified receipts | Unresolved source, ownership, or legal treatment |

Exclusion from this model does not determine the final accounting or legal treatment of the source. It means the value cannot enter the approved-distributable-value calculation without the required classification and review.

---

## 7. Deductions and Costs

The pool policy should identify applicable deduction categories.

### Transaction adjustments

Refunds, chargebacks, failed settlement, duplicate payment, provider reversals, discounts, and corrections tied to source revenue.

### Taxes and statutory obligations

Amounts collected, accrued, withheld, or payable under the relevant treatment.

### Payment and conversion costs

Processor fees, network fees, conversion costs, banking charges, and other costs required to receive or settle the payment.

### Product delivery costs

AI inference, hosting, storage, communications, support, moderation, implementation, event, fulfillment, and other direct costs attributable to the pool.

### Contractual obligations

Partner shares, licensed services, vendor amounts, contributor compensation, referral obligations, and other approved commitments.

### Shared costs

Pool-attributed infrastructure, security, finance, compliance, customer service, or operating costs under an approved allocation method.

The calculation record should show the amount, basis, source, owner, and evidence for each material category.

---

## 8. Reserves

Reserves retain value for obligations or uncertainty rather than treating the complete net pool as a candidate amount.

Potential reserve purposes include:

- refunds and chargebacks;
- tax and statutory obligations;
- service completion and customer support;
- infrastructure and AI usage;
- security and incident response;
- legal, accounting, audit, and compliance work;
- partner and vendor obligations;
- treasury and operating continuity;
- correction or dispute exposure.

Each reserve should identify:

1. purpose;
2. calculation basis;
3. amount;
4. owner and approval;
5. custody or ledger treatment;
6. review or release trigger;
7. reporting classification.

A reserve release in a later period does not enter a candidate calculation automatically. The pool policy should state how released reserves are reconsidered.

---

## 9. Asset and Conversion Treatment

Product revenue can be received in different currencies or assets. The pool should define a consistent calculation basis.

Where conversion is required, the record should identify:

- source asset and amount;
- transaction or settlement reference;
- conversion venue or provider;
- rate source and timestamp;
- fees and slippage;
- resulting asset and amount;
- treasury destination;
- reviewer and reconciliation status.

An on-chain stablecoin receipt still needs product, payer, fulfillment, period, refund, fee, and classification context.

Market movements after receipt should be separated from product revenue performance unless the approved method requires and explains another treatment.

---

## 10. Approval Packet

The candidate amount enters review through an approval packet.

The packet should contain:

- pool specification and version;
- reporting period and cutoff;
- source-revenue summary;
- reconciliation and unresolved-item report;
- deduction and cost schedule;
- reserve schedule;
- asset and conversion records;
- candidate calculation;
- treasury balance and custody confirmation;
- accounting and legal review references;
- audit or assurance findings where required;
- activation-gate status;
- proposed public report;
- approval and rejection fields.

Sensitive customer, employee, partner, identity, contractual, and professional records remain permissioned. The public report can summarize the approved result and method without exposing those materials.

---

## 11. Approval Decision

The authorized decision can:

- approve the candidate amount;
- approve a lower amount;
- defer the decision pending evidence;
- require a larger reserve;
- exclude a source or cost treatment;
- return the calculation for correction;
- reject the candidate amount;
- approve the value while keeping participation inactive.

The decision record should state:

| Decision field | Required record |
|---|---|
| Pool and period | Controlling scope |
| Calculation version | Exact packet reviewed |
| Approved amount | Value and asset or currency |
| Treasury location | Controlled account or vault reference |
| Purpose | Approved mechanism or retained status |
| Conditions | Restrictions, dependencies, or expiry |
| Reviewers and authority | Recorded approvals |
| Effective status | Approved, deferred, rejected, superseded, or cancelled |
| Public-report status | Approved disclosure and publication reference |

Approved distributable value remains a status attached to this record. It is not a general description of all treasury value.

---

## 12. Ledger and Status

FUZE should maintain an approved-value ledger.

| Status | Meaning |
|---|---|
| Draft calculation | Period data is being prepared |
| Under reconciliation | Source records and adjustments are being matched |
| Candidate | Calculation is complete enough for approval review |
| Deferred | Decision awaits evidence, remediation, or another condition |
| Approved | Amount has received the required authorization |
| Reserved pending activation | Approved amount remains controlled while the mechanism is inactive |
| Available to active process | Approved amount is assigned to an activated scope |
| Partially used | A portion has moved through the approved process |
| Completed | The period and process have been reconciled and closed |
| Corrected | A later approved adjustment changes the prior record |
| Cancelled | Prior approval is withdrawn before completion |

The ledger should reconcile opening approved value, authorized movement, unused or returned amounts, corrections, and closing balance.

---

## 13. Relationship to Activation and Eligibility

An approved amount is one prerequisite for wallet-based participation. It does not satisfy the other gates.

Before value can enter an active process, FUZE still needs the applicable:

- activation decision;
- eligibility and snapshot records;
- custody treatment;
- treasury authorization;
- technical configuration;
- jurisdiction scope;
- privacy controls;
- claim or participation period;
- public notice and support route.

The [FUZE Participation Activation Gates](08-FUZE_PARTICIPATION_ACTIVATION_GATES_PUBLIC.md) owns the readiness decision. The [FUZE Wallet-Based Participation Model](07-FUZE_WALLET_BASED_PARTICIPATION_MODEL_PUBLIC.md) owns the participant workflow where activated.

---

## 14. Corrections

Corrections can arise from late refunds, chargebacks, settlement reversals, duplicate records, cost reallocations, tax updates, source-data errors, conversion errors, or audit findings.

A correction record should identify:

1. affected pool, period, and prior version;
2. reason and evidence;
3. amount and category affected;
4. treasury and participant impact;
5. reviewer and approval;
6. revised public report;
7. recovery, offset, reserve, or other approved treatment.

FUZE should preserve the prior report and mark it as corrected or superseded rather than deleting the history.

If an active process is materially affected, the relevant authority can pause it while records and participant impact are reviewed.

---

## 15. Public Reporting

A public approved-value report can include:

- pool name and reporting period;
- calculation status and version;
- confirmed and reconciled revenue summary;
- deduction categories;
- reserve categories;
- candidate and approved amounts where applicable;
- source asset and conversion summary;
- activation status;
- authorized movement and remaining balance;
- correction history;
- report, transaction, or assurance references.

Amounts should state their unit and period. Reports should distinguish an approved amount from a claimable, paid, completed, or circulating amount.

Public wallet or transaction references must not reveal personal identity. Customer, partner, contributor, investor, employee, and tax records remain protected.

---

## 16. Public Boundary

This paper defines a calculation, approval, and ledger model. It is not a payout schedule, accounting opinion, tax conclusion, claim notice, or representation that approved value exists for a current period.

Product revenue can be retained for operations, obligations, reserves, product development, and other approved purposes. A period can close with no candidate or approved distributable value.

Calculation-specific boundaries should be read with [FUZE Token Risk Boundaries](29-FUZE_TOKEN_RISK_BOUNDARIES_PUBLIC.md); the broader public risk source is the [FUZE Risk and Disclosure Appendix](../WHITEPAPER-PAPERS/05-FUZE_RISK_AND_DISCLOSURE_APPENDIX_PUBLIC.md).

---

## Conclusion

Approved distributable value is produced through a controlled chain: define the pool, close the period, confirm and reconcile revenue, apply costs and reserves, prepare the approval packet, record the decision, and maintain the ledger.

This model keeps product revenue, candidate value, approved value, treasury movement, and active-process availability as separate statuses. That distinction allows FUZE to report the calculation clearly without turning ordinary receipts or treasury balances into implied participant claims.
