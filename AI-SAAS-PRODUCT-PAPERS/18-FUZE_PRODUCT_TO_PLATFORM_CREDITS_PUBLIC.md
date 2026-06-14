# FUZE Product to Platform Credits

## Executive Summary

This paper maps FUZE product activity to Platform Credit consumption. It explains how a product turns a user request into a defined action, presents the applicable usage basis, confirms authority and balance, delivers an output, and creates a readable record.

The model is shared, but the unit of value is product-specific. Generating a training module, processing a spreadsheet, preparing an event briefing, and running a bounded desktop task consume different resources and produce different evidence. Each product therefore defines its own actions, completion conditions, limits, and pricing rules within a common credit framework.

Platform Credits keep this product usage visible without requiring customers to interpret token mechanics. Product interfaces should make the action, expected consumption, result, and balance effect understandable before and after use.

---

## 1. Purpose and Scope

FUZE products include AI generation, data processing, shop operations, training, community administration, games, event intelligence, market research, operational monitoring, utility discovery, sponsored visibility, and desktop work assistance.

These activities cannot be metered responsibly through one generic label. This paper provides a cross-product design for answering six questions:

1. What product action is the user requesting?
2. What determines its credit use?
3. Who can authorize the action?
4. When is consumption finalized?
5. What happens when execution changes or fails?
6. Which record allows the user or workspace to review it?

Actual prices, packages, allowances, and commercial terms remain product decisions. Worked scenarios are available in [FUZE Platform Credits Usage Examples](../CORE-PLATFORM-PAPERS/06-FUZE_PLATFORM_CREDITS_USAGE_EXAMPLES_PUBLIC.md). The deeper relationship among credits, payments, revenue treatment, and token utility is covered by [FUZE Platform Credits Relationship](../TOKENOMICS-GOVERNANCE-COMPLIANCE-PAPERS/10-FUZE_PLATFORM_CREDITS_RELATIONSHIP_PUBLIC.md).

---

## 2. The Product Consumption Route

A credit-supported action should move through a predictable lifecycle:

```text
Choose action -> review usage basis -> authorize -> execute -> finalize -> report
```

### Choose action

The product identifies a meaningful service such as preparing a report, generating approved content, processing a data set, or opening a premium workflow. The action name should make sense to the user rather than expose an internal service code.

### Review usage basis

Before confirmation, the interface presents a fixed amount, estimate, range, included allowance, unit basis, or maximum authorization. Variable work should explain which factor can change the final amount.

### Authorize

The product checks balance, entitlement, workspace role, product scope, and any spending limit. Higher-cost or sensitive actions can require a second approval.

### Execute

The service processes only the permitted inputs and displays an accurate state such as queued, running, awaiting review, or dependent on an external system.

### Finalize

Consumption is recorded when the defined completion condition is reached. A reservation can be released, adjusted, or reversed when the action does not complete under the product rule.

### Report

The user receives the output and a history entry showing what occurred. Workspace owners receive the level of detail appropriate to their role.

---

## 3. Defining a Credit-Supported Action

Before assigning Platform Credits to a feature, the product owner should define:

| Field | Product question |
|---|---|
| Action name | What recognizable service is being requested? |
| User value | Which task or outcome does the service help produce? |
| Usage basis | Is consumption fixed, metered, packaged, or allowance-based? |
| Input boundary | Which data, file, prompt, event, or workflow is included? |
| Completion event | What must occur before consumption is final? |
| Output | What does the user receive or access? |
| Authority | Which account or workspace role can approve spending? |
| Limit | Which task, period, budget, or volume ceiling applies? |
| Exception rule | How are cancellation, failure, retry, or correction handled? |
| Record | What will appear in the authorized usage history? |

This definition prevents credits from becoming an unexplained charge attached to ordinary navigation. A metered action should correspond to a service that can be described, delivered, and reviewed.

---

## 4. Product-to-Credit Map

The following map identifies plausible consumption categories. Availability and pricing depend on the approved product configuration.

| Product | Credit-supported action categories | Useful usage evidence |
|---|---|---|
| HerHelp AI SaaS | AI drafts, summaries, document workflows, and selected premium modules | Task class, output reference, completion state |
| SheetLayer AI | Sheet inspection, field mapping, formula assistance, dashboard drafts, and data-processing tasks | Source scope, processing unit, generated artifact |
| ShopOS AI | Selected reports, menu content, operating checklists, and AI-assisted shop tools | Shop workspace, action type, reporting period |
| SpeakShop AI | Announcement scripts, campaign voice content, and sound-pack preparation | Requested format, language or variant, output set |
| TrainLayer AI | Guides, quizzes, onboarding material, and structured learning modules | Source collection, module type, editor, output |
| CommunityLayer AI | Support drafts, moderation-assistance batches, recurring summaries, and operational reports | Community workspace, period, review status |
| ZAGA products | Defined administration, content, event, reporting, or share-card services around game experiences | Game product, service type, event or run reference |
| QTB | Research summaries, monitored-topic reports, journals, and analytical workspaces | Topic set, source period, report reference |
| AIMM | Operational monitoring, venue comparison, liquidity-analysis tasks, and controlled reports | Authorized workspace, task period, output status |
| AIE | Event briefs, planning boards, sponsor summaries, recaps, and feedback analysis | Event workspace, deliverable, reporting window |
| ToolGrid AI | Premium discovery tools, approved listing services, campaign setup, and sponsored-placement reporting | Listing or campaign reference, service period |
| Botmad | Bounded desktop tasks, document preparation, workflow summaries, and approved processing sessions | Task scope, permitted sources, reviewer state |

This table is a category map, not a published price list. It also does not require every listed action to use credits. A subscription, enterprise agreement, included allowance, or other approved commercial model can cover some services.

---

## 5. Choosing a Metering Basis

The metering basis should reflect the service users recognize and the resources FUZE must manage.

### Fixed action

A known deliverable uses a stated amount. This works well for a standard report, defined content package, or single generation with controlled scope.

### Volume unit

Consumption follows a measurable quantity such as data range, processing volume, item count, or monitored topic set. The interface should show the unit and any maximum before execution.

### Session or task budget

A bounded work session receives an authorized credit ceiling. This can suit Botmad tasks, extended analyses, or multi-step workflows where the precise consumption is known only after execution.

### Included allowance

A plan or workspace package includes a balance for a defined period. Usage history still records consumption so owners can understand remaining capacity.

### Reserved maximum

The system temporarily reserves an amount for variable or externally dependent work and finalizes the actual use afterward. Any unused portion returns according to the product rule.

Products can combine these bases, but each action should present one understandable calculation to the user.

---

## 6. Accounts, Workspaces, and Budgets

Platform Credits can belong to an individual account, team workspace, shop, community, event, campaign, partner program, or enterprise arrangement. Ownership determines who can view the balance and who can spend it.

Useful controls include:

- role-based spending authority
- product-specific balances
- maximum consumption per action
- daily, weekly, or monthly limits
- approval thresholds
- low-balance notifications
- pause controls
- campaign or event budgets
- partner-funded restrictions
- separate views for grants and purchased balances

A workspace member may be able to prepare an action without authority to confirm its credit use. Likewise, a manager may review aggregate consumption without receiving access to private prompts, customer records, or restricted outputs.

When a balance has special conditions, the interface should identify them. Examples include an expiry rule, product scope, trial limit, campaign period, or support adjustment.

---

## 7. Completion, Reservations, and Corrections

Credit handling should follow the actual service state.

| State | Expected treatment |
|---|---|
| Quoted | Usage basis is shown; no final consumption has occurred. |
| Authorized | The user or workspace has approved the action. |
| Reserved | A maximum or estimated amount is held during execution. |
| Completed | The defined output or access condition has been delivered. |
| Released | A reservation is returned because final consumption was lower or absent. |
| Reversed | A completed record is adjusted under an approved correction or refund process. |
| Disputed | Support review is underway and the original record remains traceable. |

Retries need particular care. An automatic retry for the same authorized task should not create an unexplained duplicate charge. A materially new request can be treated as a new action after the user sees its usage basis.

Corrections should preserve the original event, adjustment, reason, timestamp, and authorized reviewer. User-facing explanations can remain concise while internal evidence stays permissioned.

---

## 8. Product Usage Records

A useful history entry can contain:

- date and time
- account or workspace
- product and action
- usage basis or task class
- credits quoted, reserved, consumed, released, or returned
- completion or correction status
- output reference where appropriate
- applicable pricing-rule version
- actor or approving role visible to authorized users

The wording should describe the product service. “Prepared event sponsor brief” is clearer than a ledger event identifier.

Records serve several audiences:

| Audience | Primary need |
|---|---|
| User | Understand the action and current balance |
| Workspace owner | Review budgets, roles, and team consumption |
| Support | Investigate failures, retries, refunds, and discrepancies |
| Product operator | Monitor demand, service health, and action performance |
| Finance and accounting | Reconcile grants, payments, consumption, and adjustments |
| Partner or sponsor | Review the agreed service within permission limits |

Public reporting may present approved aggregate categories. Detailed billing histories, prompts, customer data, internal market information, and private partner terms remain controlled.

---

## 9. Payments and Product Separation

A supported payment can fund a credit grant, but payment and consumption are separate records:

```text
Payment confirmed -> credit balance granted -> product action completed -> usage recorded
```

This separation supports reconciliation when a payment fails, a grant is duplicated, a refund applies, or part of a balance remains unused. Stablecoins can serve as a payment or settlement route where supported without changing the product-credit function.

Platform Credits represent product usage rather than FUZE token ownership. Credit acquisition or consumption does not itself create wallet eligibility, governance authority, or a claim on product revenue. Detailed policy treatment belongs in the specialist credit and tokenomics papers.

---

## 10. Product and Data Controls

Credit-supported actions inherit the controls of the product performing the work. Relevant controls can include:

- permission checks before source data is processed
- approved AI model and data-handling rules
- human review for sensitive outputs
- limits on file, workspace, venue, or campaign access
- separation of public summaries from private records
- fraud and abuse monitoring
- pricing-rule version control
- operational alerts for abnormal consumption
- support access with an auditable reason

Metering should not expose more data than the action requires. A usage record can identify that a spreadsheet report was generated without publishing the spreadsheet contents. A campaign record can show delivery status while withholding private commercial terms.

---

## 11. Implementation Checklist

A product is ready to introduce a Platform Credit action when:

1. the service and user value are named clearly;
2. the usage basis is understandable before confirmation;
3. completion and failure conditions are defined;
4. account and workspace authority is enforced;
5. balance effects are visible;
6. reservations, retries, and corrections have rules;
7. the output and history entry can be linked;
8. private data remains within its permissions;
9. support and reconciliation teams have sufficient evidence;
10. the product page states current availability and commercial terms accurately.

The Product Language Dictionary provides naming guidance, while individual product papers define the workflow and output in more detail.

---

## 12. Public Boundary

This paper defines a consumption and reporting model, not approved prices or package terms. Product pages and applicable agreements control current actions, amounts, allowances, expiry, transfer, refund, and availability.

Platform Credit records show product service activity. They do not certify the accuracy, commercial effect, market result, learning outcome, customer response, or other external performance of the resulting work.

---

## Conclusion

The product-to-credit connection is strongest when users can see what they requested, how consumption is calculated, who authorized it, what was delivered, and how the balance changed.

FUZE can apply that common lifecycle across very different products while allowing each product to define its own action units, permissions, completion events, and evidence.
