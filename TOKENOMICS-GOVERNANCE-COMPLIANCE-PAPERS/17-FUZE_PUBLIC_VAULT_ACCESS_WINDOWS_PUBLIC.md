# FUZE Public Vault Access Windows

## Executive Summary

A FUZE Public Vault Access Window is a defined process through which an approved participant class may access a bounded amount of FUZE from a named allocation vault. A window exists only when its source, purpose, eligibility, timing, limits, pricing method, payment route, release conditions, and reporting controls have been approved and published.

The model replaces ambiguous vault movement with an explicit lifecycle. Each window progresses through proposal, review, approval, notice, opening, processing, allocation, settlement, release, reconciliation, and closure. It can also be paused or cancelled when required conditions fail.

Visibility alone never opens a window. A public vault page can show a balance or status while all access remains closed. Likewise, approval of a source allocation does not establish participant eligibility.

This paper defines the window process. It does not announce an active window or offer current access. Pricing calculations are maintained in the [FUZE Vault Access Pricing Mechanism](18-FUZE_VAULT_ACCESS_PRICING_MECHANISM_PUBLIC.md).

---

## 1. Window Objective

The access-window framework should make every approved process answer:

1. Which allocation supplies the FUZE?
2. Why is access being opened?
3. Who can apply or participate?
4. What amount and time boundary apply?
5. How is pricing or other consideration determined?
6. Which payment, claim, lock, and release conditions apply?
7. How are allocations reconciled and reported?
8. What happens when the window pauses, closes, or is cancelled?

The objective is bounded, reviewable access rather than an open-ended path from treasury custody.

---

## 2. Window and Visibility

The [FUZE Public Vault Visibility System](16-FUZE_PUBLIC_VAULT_VISIBILITY_SYSTEM_PUBLIC.md) publishes approved information. An access window authorizes a controlled process.

| Public vault visibility | Public vault access window |
|---|---|
| Describes a vault, balance, restriction, or event | Defines a route for an approved participant class |
| Can remain continuously available | Exists for a stated period or condition |
| Uses public labels and evidence | Uses eligibility, limits, pricing, payment, and release rules |
| Creates an inspection surface | Creates a controlled application or allocation process |

A visible source vault can remain unavailable. A window can also close while its historical record remains publicly visible.

---

## 3. Eligible Source Categories

Source selection begins with the allocation mandate.

### Community Participation Allocation

Can support approved community, product-user, contributor, or ecosystem access under the [FUZE Community Participation Round](06-FUZE_COMMUNITY_PARTICIPATION_ROUND_PUBLIC.md) or another published community program.

### Ecosystem Growth & Partnerships

Can support a bounded partner, integration, grant, distribution, or ecosystem process where the participant class and purpose fit the category.

### Treasury Reserve

Can serve as a source only when a strategic treasury decision expressly authorizes the purpose, amount, destination, and treatment.

Other categories generally follow their dedicated release routes. Migration uses its continuity process; team and advisor allocations use vesting or contribution rules; holder incentives use earned qualification; market-operation inventory follows liquidity policy; foundation and stability reserves retain their specialized mandates.

Source approval never changes the controlling allocation value. The window is a use of the source category, not a new category.

---

## 4. Window Record

Before publication, the owner prepares a complete window record.

| Field | Required content |
|---|---|
| Window identifier | Stable public name and internal reference |
| Purpose | Outcome supported by the window |
| Source vault | Approved allocation and available budget |
| Participant class | Community, product user, contributor, partner, or other approved group |
| Eligibility | Account, product, contribution, wallet, jurisdiction, or relationship conditions |
| Window boundary | Opening and closing time or condition |
| Maximum amount | Total FUZE available through the process |
| Participant limits | Minimum, maximum, tier, or allocation method where applicable |
| Pricing method | Approved reference, calculation time, floors, caps, and adjustments |
| Consideration | Supported payment asset or other qualifying basis |
| Release | Immediate, staged, claim-based, locked, or vested treatment |
| Proceeds route | Treasury or program destination and reconciliation owner |
| Controls | Review, abuse prevention, custody, technical, and pause controls |
| Reporting | Notice, status, results, evidence, and correction requirements |

Fields that remain undecided prevent activation.

---

## 5. Lifecycle

### Proposed

The sponsor documents the source category, purpose, participant class, estimated amount, dependencies, and expected public value.

### Under review

Treasury, legal, compliance, jurisdiction, product, technical, custody, security, and reporting owners review the areas within their scope.

### Approved

The required authority approves a specific version of the window record. Approval can include conditions that must be satisfied before opening.

### Announced

FUZE publishes a notice containing the approved public fields, support route, and risk boundary. An announcement should distinguish upcoming, conditional, and active status.

### Active

Eligible participants can complete the defined process during the stated boundary. Systems capture applications, payment or qualification evidence, limits, acknowledgements, and status.

### Processing

Submissions undergo eligibility, duplicate, abuse, payment, custody, and calculation checks. Processing can continue after the application boundary closes.

### Allocated

FUZE records the approved participant amount and any continuing release conditions.

### Settled

Payment or other consideration is reconciled, and the source-vault commitment is matched to approved participant records.

### Released

FUZE is transferred, made claimable, or placed into the approved vesting or lock structure.

### Closed

Final balances, unused capacity, proceeds, participant totals, exceptions, and release status are reconciled and reported.

### Archived

The notice, methodology, final report, and correction history remain available for later review.

---

## 6. Activation Gates

A window can open only after the applicable gates have passed.

### Mandate gate

The purpose fits the source allocation and any existing commitments.

### Product or program gate

The connected product, community route, partnership, or ecosystem program is ready to support the stated purpose.

### Legal and jurisdiction gate

The participant classes, locations, communications, consideration, and process have received the required review.

### Treasury and custody gate

The source balance, destination, payment route, proceeds route, signers, and reconciliation owners are confirmed.

### Technical and security gate

Application, eligibility, limit, pricing, payment, claim, vesting, and monitoring systems are tested for the intended scope.

### Reporting gate

The notice, methodology, status fields, evidence references, support route, and final-report owner are ready.

The broader gate framework is maintained in [FUZE Participation Activation Gates](08-FUZE_PARTICIPATION_ACTIVATION_GATES_PUBLIC.md).

---

## 7. Eligibility

Eligibility should be tied to the purpose of the window.

Possible factors include:

- account or product-user status;
- documented contribution or community role;
- approved partner or ecosystem relationship;
- supported jurisdiction;
- age or entity requirements where applicable;
- wallet capability and destination verification;
- completion of required acknowledgements;
- absence of duplicate, abusive, or restricted activity.

Eligibility decisions should produce a status and reason code. Public reporting can aggregate the results while keeping personal identity and evidence permissioned.

Wallet ownership can support destination or eligibility verification, but a wallet balance alone does not create access unless the active window rules say so.

---

## 8. Allocation Methods

The window record should define how approved capacity is assigned.

### First-completed

Allocations follow completed and verified submissions until capacity is reached. Queue and timing rules should be explicit.

### Pro rata

Approved demand is scaled against available capacity using a published calculation.

### Tiered

Participant classes receive different limits based on approved product, contribution, partner, or community criteria.

### Reviewed allocation

FUZE evaluates applications against stated qualitative and quantitative criteria. The decision record should support consistent review.

### Earned or contribution-based

Access depends on verified activity, deliverables, product usage, or another measurable outcome.

A window can combine methods when the order of application is clear. Capacity held for one tier should have a published treatment if unused.

---

## 9. Pricing and Consideration

Where a window uses payment, the record should identify:

- payment asset and supported network;
- pricing source and observation time;
- calculation currency and rounding;
- floor, cap, discount, premium, or deviation rule where approved;
- fee and conversion treatment;
- payment deadline and failed-payment treatment;
- refund route for rejected or cancelled allocations.

Pricing should be reproducible from the published method and relevant evidence. A reference price is an input to the window calculation rather than a forecast of future market value.

Stablecoins can serve as payment and settlement rails when approved. Their use does not merge the payment ledger with FUZE token allocation records.

---

## 10. Limits and Abuse Controls

Limits protect the source allocation and promote consistent administration.

Controls can include:

- per-person, account, entity, or wallet limits;
- related-party and duplicate checks;
- tier budgets;
- rate and transaction controls;
- payment-address verification;
- bot and automation defenses;
- manual review thresholds;
- sanctions, fraud, or restricted-activity screening where required.

The process should document how linked accounts, failed payments, duplicate applications, overpayments, and late submissions are treated.

An override requires authorized reasoning and should remain visible to reviewers.

---

## 11. Release Conditions

Window allocation and token release can occur at different times.

Possible treatments include:

| Treatment | Meaning |
|---|---|
| Direct release | Approved FUZE transfers after settlement and final checks |
| Claim release | Approved FUZE becomes available through a defined claim period |
| Staged release | Portions become available according to stated stages |
| Time lock | Transfer remains restricted until a defined time |
| Vesting | Release depends on a schedule, service period, or milestone |
| Program custody | FUZE remains in a contract or controlled account for the program purpose |

The participant record should show approved amount, released amount, remaining restricted amount, next condition, and correction status.

Release classification follows [FUZE Vault-by-Vault Release Rules](15-FUZE_VAULT_BY_VAULT_RELEASE_RULES_PUBLIC.md) and the [FUZE Controlled Circulation Policy](12-FUZE_CONTROLLED_CIRCULATION_POLICY_PUBLIC.md).

---

## 12. Pause and Cancellation

FUZE can pause a window when a material issue affects:

- legal or jurisdiction support;
- source-vault authority or balance;
- pricing or market-data integrity;
- payment, eligibility, allocation, or claim systems;
- security, abuse, custody, or reconciliation;
- accuracy of the published notice.

During a pause, the public status should identify the affected stage and explain the treatment of submitted applications and payments at an appropriate level.

Cancellation requires a disposition plan for pending submissions, received consideration, committed FUZE, fees, records, and public communication. Refunds or reversals follow the published terms and verified payment route.

---

## 13. Reconciliation

The final window report should reconcile both token capacity and consideration.

```text
Opening FUZE capacity
- approved allocations
- reserved pending allocations
+ cancelled or expired allocations
= unused closing capacity
```

Where payment applies:

```text
Verified consideration received
- refunds and reversals
- approved fees or conversions
= reconciled net proceeds
```

The report should also reconcile allocated, settled, claimable, locked, released, and returned token states. Unused capacity remains with the source allocation unless a separate approval changes its treatment.

---

## 14. Public Notice and Reporting

An opening notice should present:

- purpose and source allocation;
- participant class and eligibility summary;
- window dates or conditions;
- available amount and participant limits;
- allocation and pricing methods;
- payment and proceeds route where applicable;
- release, claim, lock, or vesting terms;
- pause, cancellation, refund, and support process;
- public evidence and policy references.

Status reporting can show upcoming, active, paused, processing, allocated, settled, released, closed, and archived stages.

The final report can publish aggregate application, approval, allocation, payment, release, unused-capacity, and exception data. Personal identity, verification documents, private account data, and credentials remain outside the public record.

---

## 15. Boundaries

This framework defines how a future approved window would operate. It establishes no current sale, solicitation, entitlement, listing, liquidity commitment, or investment outcome.

Access remains conditional on the active notice and applicable controls. Third-party venues and market conditions are separate from a vault-window decision.

Detailed token risks are maintained in [FUZE Token Risk Boundaries](29-FUZE_TOKEN_RISK_BOUNDARIES_PUBLIC.md).

---

## Conclusion

Public Vault Access Windows give FUZE a complete, bounded route from source-vault approval to final reconciliation.

Named eligibility, capacity, pricing, payment, release, reporting, pause, and closure rules make each window reviewable on its own terms. Keeping visibility separate from access also prevents a public vault balance from being mistaken for an open participation route.
