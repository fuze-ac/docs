# FUZE Public Metrics and Transparency

## Executive Summary

FUZE public metrics are intended to help readers distinguish documented direction, completed work, controlled testing, active use, reconciled commercial evidence, and independently reviewed records. A published number is useful only when its definition, period, scope, source, evidence level, review status, and limitations are understandable.

This paper sets the investor-facing standard for selecting, calculating, reviewing, publishing, correcting, and retiring public metrics. It covers metric definitions, registries, evidence levels, publication classes, privacy treatment, dashboard controls, file integrity, correction history, and investor interpretation.

FUZE may publish selected product, commercial, platform, AI-safety, reliability, partner, community, wallet, token, and ecosystem information when supporting records are available and public disclosure is appropriate. Public reporting remains narrower than internal operations, customer reports, partner reports, finance records, security evidence, or qualified diligence.

Metrics are evidence, not conclusions by themselves. Account creation, first meaningful product value, repeated use, paid delivery, reconciled revenue, wallet activity, token movement, and partner announcements are different events. They should not be blended under one broad label.

This paper is a reporting framework. It does not confirm that any specific metric, dashboard, product, customer, partner, revenue category, token mechanism, or external examination is currently active.

## 1. Purpose and Primary Readers

This paper answers one practical diligence question:

**What should a reader require before relying on a FUZE public metric?**

It is written for:

- prospective and current investors reviewing public evidence;
- partners evaluating delivery, integration, or campaign progress;
- enterprise reviewers assessing reporting discipline;
- product users and community members following operating updates;
- analysts comparing status across products and platform functions;
- FUZE teams preparing information for publication.

The paper defines a disclosure discipline rather than a promise to publish every available record.

Some information belongs in:

- internal operating reports;
- customer or workspace reports;
- partner reports;
- qualified diligence materials;
- accounting and tax workpapers;
- legal records;
- security and incident records;
- private wallet, treasury, or identity evidence.

The [FUZE Transparency and Reporting Rails](../CORE-PLATFORM-PAPERS/09-FUZE_TRANSPARENCY_AND_REPORTING_RAILS_PUBLIC.md) paper governs the wider technical reporting architecture. The [FUZE Product Status and Evidence Matrix](14-FUZE_PRODUCT_STATUS_AND_EVIDENCE_MATRIX_PUBLIC.md) governs the related product-status framework.

## 2. Current Public Position

FUZE public papers define intended metrics, reporting methods, evidence levels, publication controls, correction practices, and public-safe boundaries.

They do not by themselves prove:

- that a dashboard is live;
- that a metric is operating or current;
- that a product has active users or paying customers;
- that a commercial value has been recognized as revenue;
- that a wallet or token record has been reconciled to a business purpose;
- that a partner relationship is active;
- that a report has been audited, certified, or independently examined;
- that future metrics will improve;
- that product, token, liquidity, market, revenue, or investor outcomes will occur.

Stronger claims require current evidence for the exact metric, period, source, definition, cohort, review method, publication version, and operating scope.

## 3. What Makes a Metric Decision-Useful

A decision-useful metric connects a claim to a defined observation.

| Required element | Reader question |
|---|---|
| Metric name | Which measure is being discussed? |
| Business purpose | What decision or claim does the measure inform? |
| Definition | What exactly counts and does not count? |
| Calculation | How is the value produced? |
| Unit | Is it users, organizations, actions, value, time, or a rate? |
| Scope | Which product, feature, geography, channel, or audience is included? |
| Period | When did measurement begin and end? |
| Cohort | Which records qualify for inclusion? |
| Exclusions | Which tests, duplicates, retries, refunds, failures, or internal events were removed? |
| Source | Which system or approved record supports the result? |
| Owner | Who maintains the definition and reviews exceptions? |
| Evidence level | How directly can the result be verified? |
| Review status | Which domain, privacy, finance, or other review has occurred? |
| Version | Which definition and report release produced the figure? |
| Limitations | Which gaps or assumptions affect interpretation? |

A total without this context may hide material differences.

For example, these are separate events:

- account registered;
- user invited;
- user authenticated;
- first workflow started;
- first workflow completed;
- first meaningful value reached;
- repeat use observed;
- payment initiated;
- payment settled;
- service fulfilled;
- revenue reconciled.

Combining them under one label such as “users,” “customers,” or “revenue” weakens the report.

Rates require both numerator and denominator. A completion percentage should identify what started, what counted as completion, which period and cohort applied, and how retries, failures, and abandoned sessions were treated.

## 4. Public Metric Registry

FUZE should maintain an approved registry for recurring public measures.

Each registry entry may include:

1. stable metric identifier;
2. approved public name;
3. business purpose;
4. current definition and calculation;
5. unit;
6. authoritative source;
7. responsible owner;
8. scope, period, cohort, and exclusions;
9. privacy and aggregation requirements;
10. expected update cadence;
11. evidence level;
12. definition version and effective date;
13. quality checks;
14. known limitations;
15. related reports and dashboards;
16. correction, restatement, or supersession history;
17. publication status.

The registry helps prevent the same label from acquiring different meanings across a website update, investor deck, dashboard, partner report, community announcement, and diligence package.

When a calculation changes materially, FUZE should issue a new definition version and explain whether prior periods were recalculated, restated, or left as a separate series.

Experimental measures should be labeled as experimental until their usefulness, source quality, and definition stability are understood.

## 5. Evidence Levels

Public metrics may carry different strengths of support.

| Level | Evidence character | Appropriate public treatment |
|---|---|---|
| E0: Direction | Proposed measure or reporting intention | Describe as planned, proposed, or under definition |
| E1: Documented | Definition, owner, source design, and controls exist | State that the measurement method is documented |
| E2: Tested | Sample or controlled records were processed and reviewed | Present as test evidence with scope and period |
| E3: Operating | Source and calculation run in a bounded live environment | Report observed operating results with cohort and limitations |
| E4: Reconciled | Relevant records passed domain review and reconciliation | Identify review basis, adjustments, and reporting period |
| E5: Independently examined | An approved external party examined a stated scope | Name the scope and form of examination only when authorized |

Evidence strength belongs to the metric and reporting period rather than permanently to the product.

Examples:

- a product may have E3 usage data but only E1 revenue measurement;
- a wallet transfer may be publicly visible while its business classification remains unreconciled;
- a partner announcement may be public while implementation evidence remains at E0 or E1;
- an AI workflow may have E2 evaluation results without E3 operating reliability evidence.

The [FUZE Public Status and Roadmap Matrix](../PUBLIC-INDEX/02-FUZE_PUBLIC_STATUS_AND_ROADMAP_MATRIX.md) should remain aligned with metric evidence.

## 6. Metric Families

FUZE may organize public reporting into metric families without forcing every product to use the same dashboard.

### 6.1 Product access and adoption

Possible measures include:

- qualified access;
- invited users;
- onboarding completion;
- first workflow started;
- first meaningful value reached;
- continued use;
- workflow completion;
- output review;
- support activity;
- retention by cohort.

Raw event volume should remain separate from meaningful product completion.

Internal testing, demonstrations, automated activity, promotional use, duplicate attempts, and retries require explicit treatment.

### 6.2 Commercial evidence

Commercial reporting may distinguish:

- offer readiness;
- checkout or invoice initiation;
- payment attempt;
- settled payment;
- fulfilled service;
- refund or reversal;
- dispute;
- repeat purchase;
- renewal;
- reconciled product revenue.

The [FUZE Product Revenue Model](02-FUZE_PRODUCT_REVENUE_MODEL_PUBLIC.md) owns the detailed classification.

Public summaries should use approved aggregates and should not expose customer identities, contracts, invoices, private pricing, or accounting workpapers.

### 6.3 Platform use and reliability

Shared-rail metrics may include:

- products using a platform function;
- successful and failed requests;
- availability and latency;
- queue, retry, and timeout status;
- identity and permission decisions;
- Platform Credit reservations, use, reversals, and adjustments;
- reconciliation exceptions;
- incident and recovery status.

Adoption by several operating products is stronger platform evidence than an architecture description alone.

Platform Credit activity remains separate from token records, cash receipts, and revenue classification.

### 6.4 AI quality and safety

Possible signals include:

- task completion;
- human acceptance;
- human correction or rejection;
- escalation;
- refusal or policy denial;
- source-support findings;
- privacy or permission findings;
- tool authorization;
- latency and cost;
- incidents and containment.

The workflow, version, test method, and consequence level are required context.

The [FUZE AI Safety and Reliability](07-FUZE_AI_SAFETY_AND_RELIABILITY_PUBLIC.md) paper governs the underlying control lifecycle.

### 6.5 Distribution and partner delivery

Possible channel measures include:

- qualified opportunities;
- demonstrations;
- onboarding;
- activation;
- workflow completion;
- support burden;
- paid conversion;
- repeat use;
- partner milestones;
- active deployment;
- renewal.

Introductions, meetings, memoranda, announcements, pilots, integrations, active deployments, and renewals are different stages.

### 6.6 Community and ecosystem activity

Possible measures include:

- defined program participation;
- game or event completion;
- education completion;
- product feedback;
- contributor work;
- moderator or operator activity;
- recurring product use;
- approved governance participation.

Audience size, followers, wallet connections, registrations, incentive activity, bot activity, and sustained product use are different signals.

### 6.7 Wallet, token, vault, and market records

These records should appear only when the corresponding mechanism, source, and reporting basis are active and applicable.

Specialist papers govern:

- token supply and release;
- vault status;
- wallet eligibility;
- custody;
- claims;
- market access;
- liquidity;
- transaction purpose;
- correction and reconciliation.

A public transaction does not by itself prove revenue, participant identity, eligibility, or investment outcome.

## 7. Stage and Cohort Separation

Public reports should not combine incompatible stages.

FUZE should separate:

- design from implementation;
- internal tests from external use;
- invited pilots from public access;
- promotional activity from paid activity;
- registered accounts from qualified active users;
- workflow starts from completed outcomes;
- wallet connections from approved ecosystem participation;
- transaction attempts from settled payments;
- settled payments from fulfilled delivery;
- gross inflows from reconciled revenue;
- signed interest from active partner delivery;
- public announcements from operating evidence;
- product usage from token demand;
- game values from withdrawable or externally transferable value.

Early cohorts may still provide useful evidence when their size, selection, and environment are visible.

A result from five invited organizations answers a different question from a result observed after open public release.

FUZE should avoid extrapolating one cohort beyond the environment actually measured.

Where a cumulative number is published, the related period report should explain material additions, removals, exclusions, corrections, or definition changes.

## 8. Evidence Sources

The metric owner should use the source closest to the observed event.

Possible sources include:

- product event records;
- authentication records;
- workspace and role records;
- payment-provider status;
- invoices and fulfillment records;
- approved finance schedules;
- support systems;
- release records;
- evaluation results;
- incident logs;
- partner acceptance records;
- community program records;
- governance decisions;
- public-chain references;
- signed or hashed reports.

A spreadsheet or dashboard may calculate or present a value, but the report should still identify the underlying source.

Manual adjustments require:

- reason;
- owner;
- source evidence;
- approval;
- review history;
- effect on the published result.

## 9. Quality Checks

Before publication, review may test:

- required fields;
- timestamp consistency;
- timezone and cutoff;
- duplicate and retry handling;
- internal and test-account exclusions;
- automated or bot activity;
- late-arriving or missing records;
- refund, reversal, cancellation, and dispute treatment;
- source-to-report reconciliation;
- calculation and rounding;
- currency, network, or unit conversion;
- cohort and stage classification;
- privacy and aggregation transformations;
- prior-period comparability;
- definition version.

Known gaps should be stated in proportion to their effect.

Treating missing records as zero may create a misleading result, especially when an external provider, blockchain network, or integration is delayed.

## 10. Publication Classes

FUZE information may be delivered at different access levels.

| Class | Typical content |
|---|---|
| Internal operating report | Detailed events, costs, failures, exceptions, incidents, and owner actions |
| User or workspace report | Activity and records belonging to an authorized user or organization |
| Partner report | Measures agreed for a specific integration, campaign, pilot, or delivery scope |
| Qualified diligence report | Approved commercial, financial, technical, governance, security, and risk evidence |
| Public report | Selected aggregate status and metrics suitable for unrestricted access |

Moving information to a wider audience requires a separate disclosure decision.

Accuracy approval does not automatically authorize publication.

Public availability of a wallet address, transaction, company name, or product event does not make its private business, identity, customer, legal, or treasury context public.

Qualified investors may receive greater detail under the applicable access and confidentiality process.

## 11. Public Review Workflow

A recurring metric should pass a repeatable process:

```text
registered definition
-> source extraction
-> quality validation
-> calculation
-> domain review
-> privacy and disclosure review
-> approval
-> publication
-> registry and index update
```

Domain review depends on the subject:

- product owners review product meaning;
- finance owners review commercial and revenue classification;
- operations owners review reliability;
- AI owners review evaluation and safety context;
- privacy and security owners review exposure;
- partner owners review attribution;
- token, wallet, treasury, governance, legal, or compliance reviewers enter where required.

A released report should identify:

- report name;
- metric identifiers;
- period;
- scope and cohort;
- evidence level;
- definition version;
- publication date;
- current status;
- limitations;
- correction or supersession reference where applicable.

A draft dashboard, internal snapshot, or preliminary calculation should not be cited publicly as an approved period report.

## 12. Privacy and Aggregation

Public transparency must preserve the boundary between reviewable activity and private identity.

Publication review should consider:

- direct identifiers;
- customer and employee records;
- private investor information;
- partner terms;
- credentials and signer details;
- wallet-to-person associations;
- exact locations;
- small cohorts;
- unique events;
- combinations that enable re-identification.

Available controls include:

- aggregation across an appropriate cohort;
- minimum cohort-size rules;
- delayed release;
- category grouping;
- value ranges;
- redaction;
- pseudonymous references without identity linkage;
- omission when transformation still creates material exposure.

An on-chain address or transaction may be referenced when it supports an approved public purpose.

FUZE should not publish the private person behind an address merely to make a report appear more complete.

The [FUZE Data Privacy and Permission Model](08-FUZE_DATA_PRIVACY_AND_PERMISSION_MODEL_PUBLIC.md) governs the wider privacy treatment.

## 13. Dashboards and Period Reports

Dashboards and period reports serve different purposes.

A public dashboard should show:

- metric name;
- definition reference;
- product and scope;
- current period;
- freshness or last-update time;
- evidence or source category;
- definition version;
- known delay, incident, or incomplete-data notice;
- current status;
- link to the latest formal report or correction.

A dashboard may be provisional when records continue to arrive.

A period report provides a closed and reviewed record for a stated period. It should explain:

- material movement;
- cohort changes;
- definition changes;
- corrections;
- source limitations;
- events affecting comparability.

If a dashboard differs from a closed-period report, update timing and source treatment should explain the difference.

A smaller set of stable metrics is more useful than a large dashboard with shifting definitions and vanity totals.

## 14. Hashes, Signatures, and Publication Integrity

A report hash may help readers verify that a retrieved file matches the version registered by FUZE.

A publication entry may include:

- title;
- report identifier;
- period;
- definition and report version;
- hash algorithm;
- digest;
- release date;
- publication location;
- current status.

Hash verification answers an integrity question about the file.

It does not prove:

- source completeness;
- calculation correctness;
- professional audit;
- identity of every source event;
- future continuation of the reported result.

Where digital signatures are used, FUZE also needs:

- controlled signing keys;
- authorized signer records;
- verification instructions;
- rotation procedures;
- revocation status.

## 15. Corrections, Restatements, and Supersession

Public credibility requires visible correction rather than silent replacement.

When a material issue is identified, the report owner should:

1. assess affected metrics, periods, products, and audiences;
2. label, suspend, or withdraw the affected version where necessary;
3. preserve the original under controlled history;
4. correct the source, classification, calculation, or disclosure;
5. complete required domain and privacy review;
6. publish a replacement or correction note;
7. explain the reason and material effect;
8. update dashboards, indexes, investor materials, and dependent reports.

A **restatement** changes a previously reported value or interpretation materially.

A **supersession** replaces a report because a newer period, definition, or document is current.

A **correction note** may address a smaller error that does not materially change the result.

Definition changes should not be presented as performance changes.

Where historical recalculation is impractical, FUZE should clearly mark the break and begin a new series.

## 16. Metric Ownership and Governance

Each recurring public metric should have a named owner responsible for:

- definition quality;
- source authority;
- exception handling;
- review cadence;
- publication approval routing;
- correction history;
- retirement or supersession.

Metrics should be retired or paused when:

- the source is no longer reliable;
- the definition no longer matches the product;
- the metric creates misleading incentives;
- privacy risk becomes disproportionate;
- comparability is lost;
- operating cost exceeds decision value;
- the measure is replaced by a better metric.

Metric governance should resist incentives to publish a favorable number before its definition and evidence are ready.

## 17. Investor Interpretation

Investors can evaluate a public metric through seven questions:

1. **Relevance:** Does it connect to product value, execution, economics, or control?
2. **Definition:** Could another reviewer reproduce the inclusion and calculation logic?
3. **Evidence:** Which source and evidence level support the value?
4. **Comparability:** Are periods, cohorts, units, and definitions consistent?
5. **Quality:** Which exclusions, adjustments, missing records, or corrections matter?
6. **Privacy:** Has public disclosure preserved customer, user, partner, and wallet boundaries?
7. **Context:** How does the metric relate to product status, costs, support, risk, and the next operating decision?

No single number proves the FUZE investment thesis.

A stronger view combines:

- product completion;
- first meaningful value;
- continued use;
- paid delivery;
- reconciled commercial evidence;
- platform reuse;
- reliability;
- AI-safety evidence;
- partner execution;
- governance;
- evidence quality.

## 18. Investor Review Questions

Reviewers should ask:

- Is the metric registered and versioned?
- Does the name match the actual event measured?
- Which source is authoritative?
- Which accounts, events, wallets, tests, retries, refunds, or internal records were excluded?
- Is the cohort visible?
- Is the value tested, operating, reconciled, or independently examined?
- Which reviewer approved the result?
- Has privacy or re-identification risk been assessed?
- Are dashboard and period-report values consistent?
- Were prior figures corrected or restated?
- Which metrics were retired and why?
- Does the metric connect to product value or merely visibility?
- Is a commercial value cash collected, fulfilled, adjusted, or reconciled revenue?
- Is an on-chain value linked to an approved business purpose?

## 19. Public Boundary

This paper is a reporting framework.

It is not:

- an audit opinion;
- a financial statement;
- an investment offer;
- a valuation;
- a forecast;
- a certification;
- a guarantee of metric accuracy or future performance.

FUZE may withhold, delay, redact, or aggregate information when publication would expose:

- personal data;
- customer records;
- confidential commercial terms;
- private investor information;
- security controls;
- treasury context;
- private wallet associations;
- legal, tax, accounting, or professional workpapers;
- another protected interest.

The existence of a metric does not require unrestricted disclosure.

Product activity or reporting volume should not be interpreted as proof of token demand, price, liquidity, exchange access, revenue growth, profitability, market share, investment return, or future ecosystem outcomes.

## Key Takeaways

- A public number is useful only when its definition, source, period, cohort, evidence level, and limitations are clear.
- Direction, documentation, testing, operation, reconciliation, and independent examination are different evidence states.
- Account creation, activation, repeat use, paid delivery, reconciled revenue, wallet activity, and token activity are different events.
- Public metrics should use sources closest to the observed event and should pass domain, quality, privacy, and disclosure review.
- Dashboards provide current visibility; period reports provide reviewed records.
- Public transparency should not expose personal identity, customer records, private wallet associations, confidential agreements, or security detail.
- Material errors should be corrected visibly with version and history controls.
- Investors should evaluate metric relevance and evidence rather than relying on headline totals.