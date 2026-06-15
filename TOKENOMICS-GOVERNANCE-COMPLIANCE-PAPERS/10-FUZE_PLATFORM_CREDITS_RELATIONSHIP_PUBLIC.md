# FUZE Platform Credits Relationship

## Executive Summary

Platform Credits are FUZE product-consumption units. They allow supported product actions to be priced, authorized, metered, corrected, and reported without making ordinary SaaS usage depend on token ownership.

A credit balance can come from purchase, subscription allowance, enterprise or partner funding, trial, promotion, support adjustment, or another approved grant. Those sources require separate ledger classifications because they can have different payment, revenue, expiry, refund, and reporting treatment.

Credits move through a controlled lifecycle: issue or allocate, make available to an account or workspace, reserve for an action, consume after the action reaches its defined completion state, reverse or adjust when needed, and expire or close under policy.

Platform Credits remain separate from FUZE token. They are also distinct from the payment asset used to fund a purchase. This paper defines that relationship and the controlling credit ledger; product-specific metering examples remain in the product and platform credit papers.

---

## 1. Credit Objective

FUZE products can consume different levels of AI processing, data work, reporting, support, infrastructure, and product capacity. Platform Credits provide a common way to represent that consumption.

The credit system should help users and operators answer:

- what balance is available;
- which account or workspace controls it;
- which product action can consume it;
- how much is authorized or reserved;
- when consumption becomes final;
- what happens after failure or correction;
- which source funded the balance;
- how payment, revenue, and product records reconcile.

Credits are useful when they make product usage predictable. They should not obscure prices, create unexplained deductions, or merge product access with token rights.

---

## 2. Credit Classes

The ledger should preserve the source and policy of each credit class.

| Credit class | Typical source | Key treatment |
|---|---|---|
| Purchased credits | Confirmed customer payment | Linked to payment, offer, refund, and revenue treatment |
| Subscription allowance | Included in a recurring plan | Tied to the plan period, renewal, rollover, and cancellation rules |
| Enterprise or partner credits | Contracted organization budget | Controlled by agreement, workspace, and authorized administrators |
| Trial credits | Onboarding or product evaluation | Limited by scope, period, and abuse controls |
| Promotional credits | Campaign or approved promotion | Separately labeled from purchased value |
| Support credits | Service correction or customer support action | Linked to the original issue and approval |
| Granted credits | Testing, education, community, or another approved program | No assumed customer payment or ordinary revenue record |
| Internal testing credits | Quality assurance or operational testing | Excluded from customer usage and revenue reporting |

Credits from different classes can appear in one workspace while retaining separate lot or source records.

---

## 3. Ledger Model

Each credit ledger entry can include:

1. credit transaction identifier;
2. account, workspace, or organization;
3. credit class and source reference;
4. product or permitted scope;
5. amount;
6. status;
7. issue, effective, and expiry times;
8. payment or contract reference where applicable;
9. reservation or usage reference;
10. approval and correction history.

The account balance is the sum of available credit entries after finalized additions, consumption, reversals, transfers where permitted, and expiry.

Ledger history should remain append-oriented. Corrections should create linked entries rather than silently rewriting the original transaction.

---

## 4. Credit Lifecycle

### 4.1 Issue or allocate

FUZE creates or assigns credits under an approved package, subscription, agreement, trial, promotion, support decision, or internal process.

The record identifies the credit class, amount, permitted scope, responsible owner, and applicable policy.

### 4.2 Make available

Credits become available to a user, workspace, team, shop, community, partner, or organization after the source conditions are satisfied.

A purchase can remain pending until payment confirmation. A partner allocation can remain pending until the agreement or milestone becomes effective.

### 4.3 Authorize

Before a product action begins, the system checks:

- available balance;
- product and feature eligibility;
- role and workspace authority;
- estimated or maximum usage;
- rate-card version;
- relevant limits.

### 4.4 Reserve

A variable or long-running action can reserve an estimated maximum. Reserved credits are unavailable for other use but are not yet final consumption.

### 4.5 Consume

Credits are finalized when the product reaches its defined billable or usage-complete state. The usage record should identify the action, quantity, result status, rate, and final amount.

### 4.6 Release or reverse

Unused reservation is released. Failed, duplicated, cancelled, or incorrectly metered actions can receive a full or partial reversal according to policy.

### 4.7 Expire or close

Credits can expire when the controlling package, plan, grant, or agreement permits it. The ledger records the amount, policy basis, notice treatment, and effective time.

---

## 5. Usage Authorization

A product should present the credit basis before a user confirms an action where practical.

| Usage model | User-facing information |
|---|---|
| Fixed action | Exact credit amount for the defined action |
| Volume-based | Unit, rate, estimate, and final measured quantity |
| Session or task budget | Maximum reservation and completion treatment |
| Included allowance | Remaining allowance and overage behavior |
| Tiered action | Selected level, included work, and additional usage |

The interface should distinguish an estimate from a final charge.

If the product cannot estimate accurately, it should use a maximum authorization, staged confirmation, or another control that prevents unexpected balance exhaustion.

---

## 6. Completion and Failure Rules

Every credit-supported action needs a completion definition.

Completion can mean:

- a report is generated and available;
- an approved product workflow reaches its terminal state;
- a scheduled service period is delivered;
- an event, campaign, or placement begins or completes under its terms;
- a work session produces the agreed output;
- another product-specific acceptance condition is satisfied.

Failure handling should distinguish:

| Outcome | Credit treatment |
|---|---|
| Action never started | Release the reservation |
| System failure before useful output | Reverse or release under policy |
| Partial output accepted | Apply the defined partial treatment |
| User cancellation | Apply the disclosed cancellation rule |
| Duplicate action | Correct the duplicate entry |
| Product output delivered but disputed | Use the support and review process |
| Abuse or prohibited use | Apply the applicable restriction and ledger treatment |

Product teams should not invent ad hoc credit adjustments outside the approved support and correction process.

---

## 7. Accounts, Workspaces, and Budgets

Credits can belong to an individual account or a managed workspace.

Workspace controls can include:

- owners and billing administrators;
- members allowed to use credits;
- product and feature limits;
- team, project, branch, or campaign budgets;
- per-action and period limits;
- approval requirements;
- alerts and low-balance thresholds;
- report access;
- transfer or reassignment rules.

A workspace administrator should not automatically gain access to the private content of every product action merely because the administrator manages the credit budget. Billing visibility and product-data permission are separate controls.

---

## 8. Payment Relationship

A payment can fund a Platform Credit purchase, but the payment asset does not become the credit.

```text
Approved offer -> payment authorization -> settlement confirmation
-> credit issuance -> product consumption -> reconciliation
```

The payment record should identify:

- payer or contracting account within authorized systems;
- amount and currency or asset;
- provider, bank, network, or transaction reference;
- fees and conversion;
- offer, invoice, or package;
- settlement and refund status;
- resulting credit entry.

Supported payment routes can include approved fiat, card, bank, invoice, stablecoin, partner-funded, or other provider flows.

A stablecoin transfer without product and invoice context should not create credits automatically.

---

## 9. Revenue Relationship

Credit issuance and revenue recognition are separate records.

A purchased credit package can create a payment and a credit obligation before the credits are consumed. Subscription allowance, promotional credits, granted credits, refunds, expiry, and unused balances can require different treatment.

The revenue record should connect:

1. the approved offer;
2. payment and settlement;
3. issued credit class and amount;
4. product delivery or consumption evidence;
5. refunds, reversals, expiry, and adjustments;
6. applicable accounting period and classification.

Credit consumption proves that a supported product action occurred under the usage system. It does not by itself prove a cash receipt or final revenue treatment.

The [FUZE Product Revenue Model](../INVESTOR-PARTNER-PAPERS/02-FUZE_PRODUCT_REVENUE_MODEL_PUBLIC.md) provides the investor-facing commercial chain. Any later approved-value review belongs in [FUZE Approved Distributable Value Model](09-FUZE_APPROVED_DISTRIBUTABLE_VALUE_MODEL_PUBLIC.md).

---

## 10. Relationship to FUZE Token

Platform Credits and FUZE token serve different user needs.

| Platform Credits | FUZE token |
|---|---|
| Represent supported product consumption | Supports approved ecosystem token functions |
| Recorded in the product credit ledger | Recorded through the applicable token and wallet systems |
| Can be purchased, included, granted, adjusted, or expired under credit policy | Governed by token supply, allocation, utility, custody, circulation, and market policies |
| Designed for straightforward product use | Relevant only where a token-related product or ecosystem function is defined |

A product can use credits without requiring a wallet. A token utility can exist without charging Platform Credits. When both appear in one workflow, the interface should explain each condition separately.

FUZE should not market credits as a token substitute or imply that credit balances convert into FUZE token unless a future approved policy expressly defines a supported conversion. No such conversion is established by this paper.

---

## 11. Transfer, Sharing, and Conversion

The credit policy should state whether credits can:

- move between users in the same workspace;
- be reassigned by an administrator;
- move between workspaces under one organization;
- transfer to another customer;
- roll over into a later period;
- convert between product-specific packages;
- be redeemed or refunded.

Default restrictions should match product, fraud, accounting, support, and customer-expectation needs.

Open external transferability or market trading would materially change the nature of the credit system and require classification, governance, legal, accounting, and technical review.

---

## 12. Expiry, Refunds, and Adjustments

Expiry and refund rules should be visible before purchase or allocation.

The policy can distinguish:

- refundable unused purchased credits;
- non-refundable consumed credits;
- failed-action reversals;
- subscription allowance that resets;
- promotional or trial credits that expire;
- enterprise balances governed by contract;
- support adjustments;
- account closure treatment.

An adjustment entry should identify the original transaction, reason, amount, approver, and effect on payment, credit, usage, and revenue records.

---

## 13. Abuse and Integrity

Credit controls should address:

- automated or abnormal consumption;
- duplicate requests;
- compromised accounts;
- unauthorized workspace use;
- manipulated referral or promotion activity;
- payment fraud and chargebacks;
- exploitation of failure reversals;
- attempts to resell restricted credits;
- meter or rate-card errors.

FUZE can limit, pause, or investigate affected usage while preserving evidence and providing an appropriate support route.

Controls should avoid exposing security-sensitive thresholds or private customer information in public reports.

---

## 14. Reporting and Privacy

Users should be able to review:

- opening and closing balance;
- additions by credit class;
- reservations and releases;
- finalized usage by product or action;
- reversals, adjustments, transfers, and expiry;
- rate or policy version;
- payment references where appropriate.

Workspace reports can aggregate by team, project, branch, product, period, or budget without exposing product content to unauthorized billing roles.

Public reporting can use aggregate issued, purchased, granted, consumed, reversed, and expired categories. It must not expose customer identity, workspace content, payment credentials, private product data, or personal wallet associations.

---

## 15. Product Implementation References

Product teams define the exact action, meter, estimate, reservation, completion, and correction behavior through [FUZE Product to Platform Credits](../AI-SAAS-PRODUCT-PAPERS/18-FUZE_PRODUCT_TO_PLATFORM_CREDITS_PUBLIC.md).

Reader-facing examples across AI tasks, shops, training, communities, events, market research, games, and work sessions are maintained in [FUZE Platform Credits Usage Examples](../CORE-PLATFORM-PAPERS/06-FUZE_PLATFORM_CREDITS_USAGE_EXAMPLES_PUBLIC.md).

This relationship paper remains the primary source for ledger classes, payment and revenue separation, workspace controls, and credit policy.

---

## 16. Public Boundary

This paper defines product credits and their relationship to payment, revenue, and FUZE token. It does not publish prices, refund terms for a specific offer, formal accounting policy, or token-conversion rights.

Actual credit packages, rates, validity, transferability, refunds, supported products, and payment routes depend on the approved product offer and current policy.

Credit purchases or usage do not establish wallet-participation eligibility or a claim against FUZE token, treasury assets, or product revenue.

---

## Conclusion

Platform Credits provide a product-first usage layer with a traceable lifecycle from source and allocation through authorization, reservation, consumption, correction, and expiry.

Their value as an operating system depends on clear credit classes, append-oriented ledger records, transparent user authorization, workspace controls, and reconciliation with payment and product delivery.

Keeping credits separate from FUZE token lets customers use supported products through familiar product flows while token functions remain governed by their dedicated policies.
