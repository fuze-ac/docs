# QTB

## Executive Summary

QTB, or Quant AI Trade Brain, is the FUZE product for AI-assisted market research, interpretation, and decision-context management.

It helps users organize selected:

- market data;
- exchange and venue information;
- public project documents;
- token and supply information;
- charts and indicators;
- scheduled events;
- news and announcements;
- watchlists;
- onchain observations where supported;
- private notes;
- trading-journal entries; and
- team research

into structured, reviewable outputs with sources, timestamps, assumptions, conflicts, uncertainty, and follow-up conditions.

QTB may support:

- daily market reviews;
- asset and sector research;
- token and project analysis;
- watchlist maintenance;
- chart-context notes;
- scenario comparisons;
- decision checklists;
- private journal reflection;
- educational explanations;
- public-safe market briefs; and
- research handoffs.

QTB is a research and market-intelligence product.

It is not:

- a broker;
- an exchange;
- a custody service;
- a portfolio manager;
- an investment adviser;
- a trade-execution engine;
- an autonomous trading system;
- a guaranteed-signal provider;
- a market maker; or
- a source of guaranteed return, price, liquidity, listing, or market outcome.

The product remains separate from [AIMM](12-AIMM_PUBLIC.md).

QTB organizes and interprets market information. AIMM addresses authorized liquidity-operations intelligence, monitoring, and reporting. Neither product independently decides or executes an unauthorized market action.

## Purpose of This Paper

This paper explains:

- the QTB product purpose;
- intended users;
- source and freshness controls;
- the research lifecycle;
- market briefs, watchlists, token research, chart context, scenarios, and journals;
- alerts and scheduled review;
- public communication;
- private and team workspaces;
- Platform Credit usage;
- data, permission, provider, and reliability controls;
- reporting and correction;
- separation from trading execution and AIMM;
- product status and evidence; and
- public limitations.

QTB appears in the [FUZE AI SaaS Product Index](01-FUZE_AI_SAAS_PRODUCT_INDEX_PUBLIC.md).

## Product Purpose

Crypto and digital-asset information arrives through:

- market feeds;
- exchange interfaces;
- project documentation;
- token disclosures;
- news;
- social discussion;
- onchain activity;
- governance updates;
- release schedules;
- technical charts;
- research reports;
- community messages;
- private notes; and
- prior decisions.

The main difficulty is often not access to information.

The difficulty is determining:

- what is current;
- which venue or source is being described;
- whether two values are comparable;
- whether a statement is observed, reported, calculated, assumed, or inferred;
- whether an event is scheduled, announced, approved, completed, or cancelled;
- whether a token figure describes allocation, release, circulation, liquidity, or exchange balance;
- whether a price move has one cause or several plausible causes;
- what evidence is missing;
- what would invalidate the current view; and
- what requires specialist or operational review.

QTB gives users a repeatable way to:

- state a research question;
- define asset, venue, period, and timezone;
- select authorized sources;
- preserve source origin and as-of time;
- separate facts from interpretation;
- compare conflicting information;
- record scenarios and invalidation conditions;
- maintain watchlists and journals;
- prepare reviewable reports;
- identify missing information; and
- continue research without losing the original context.

A polished QTB output should not hide uncertainty or turn incomplete information into certainty.

## Intended Users

| User | Typical QTB workflow |
|---|---|
| Individual researcher | Daily market review, asset note, sector review, and watchlist |
| Trader | Pre-decision checklist, scenario review, and post-decision journal |
| Analyst | Structured project, token, sector, liquidity, or narrative research |
| Web3 operator | Market context for product, treasury, communication, and launch planning |
| Community manager | Neutral and reviewed public market explanation |
| Educator or creator | Source-aware glossary, lesson, or market-concept guide |
| Product team | Market context, competitor review, and event tracking |
| Risk reviewer | Evidence gaps, conflicting signals, assumptions, and invalidation conditions |
| Team lead | Shared research, reviewer notes, approval history, and handoff continuity |
| Reporting reviewer | Public-safe research summaries with methodology and limitations |

QTB is most useful where a user already has access to information but needs stronger research discipline and durable context.

## Source Model

QTB should identify the type and role of every source.

| Source type | Example use | Main limitation |
|---|---|---|
| Market feed | Price, volume, volatility, spread, depth, or other venue data | Venue-specific, delayed, incomplete, or unavailable |
| Exchange page | Trading pair, market access, announcement, or status | May change, be region-specific, or reflect exchange custody |
| Project document | Product, token, governance, roadmap, or release statement | Project-authored and not automatically independently verified |
| Blockchain or explorer data | Public transaction, balance, contract, or event observation | Public address is not private identity and interpretation may require context |
| News source | Reported event or market context | Publication delay, incomplete sourcing, or later correction |
| Social or community source | Announcement, sentiment, or discussion context | May be unofficial, manipulated, selective, or false |
| Chart | Historical or current market visualization | Depends on venue, interval, indicator, and data quality |
| User note | Personal thesis, assumption, or observation | Not independently verified |
| Private journal | Decision process and behavioral reflection | Sensitive and not a public source |
| Team research | Reviewed internal context | May contain confidential, stale, or unapproved material |
| Calculated indicator | Derived metric or transformation | Depends on formula, data window, and assumptions |

A source record should preserve, where applicable:

- provider;
- title or endpoint;
- asset;
- venue;
- market pair;
- network;
- contract;
- period;
- interval;
- timezone;
- observed or published time;
- retrieval time;
- delay or freshness note;
- version;
- access state;
- methodology;
- confidentiality level;
- correction state; and
- source owner.

QTB should distinguish:

- observed fact;
- source-reported claim;
- project statement;
- calculated value;
- model interpretation;
- user assumption;
- scenario;
- unresolved conflict;
- missing information;
- stale information; and
- reviewer-approved conclusion.

## Time, Venue, and Market-Pair Discipline

Market statements should identify enough context to be reproducible.

Important fields may include:

- asset;
- base and quote currency;
- venue;
- market type;
- network where relevant;
- contract where relevant;
- interval;
- period;
- timezone;
- data timestamp;
- retrieval timestamp;
- source delay;
- calculation method; and
- known data gaps.

The following are not automatically interchangeable:

- spot and derivatives markets;
- one exchange and another exchange;
- centralized and decentralized venues;
- last price and index price;
- mark price and trade price;
- daily and intraday volume;
- reported volume and independently observed volume;
- token allocation and circulating supply;
- unlocked supply and actively tradable supply;
- wallet balance and exchange-account balance;
- liquidity depth and total liquidity;
- announced listing and active trading;
- trading enabled and withdrawals enabled; and
- scheduled event and completed event.

QTB should not combine these states without an explicit method and explanation.

## Research Lifecycle

### 1. State the Question

The user defines what they are trying to understand.

Examples include:

- why an asset moved during a defined period;
- how a token release may affect market context;
- whether a sector narrative is strengthening or weakening;
- what changed in a project's documentation;
- whether a watchlist condition occurred;
- what evidence supports or challenges a thesis;
- what process errors appeared in prior journal entries; or
- which facts require verification before a public update.

A research question should not be framed as a request for guaranteed profit or certainty.

### 2. Define Scope

The task should identify:

- assets;
- project;
- venue or venues;
- market type;
- network or contract where relevant;
- period;
- timezone;
- data types;
- intended audience;
- private, team, or public classification;
- output type; and
- review owner.

### 3. Select Authorized Sources

The user chooses or approves the sources that may be used.

QTB may flag:

- missing source;
- stale source;
- inaccessible source;
- conflicting source;
- unsupported claim;
- unverifiable value;
- venue mismatch;
- timeframe mismatch; and
- methodology gap.

The product should not silently substitute a weaker source for a required source.

### 4. Build the Evidence Record

QTB organizes:

- observed values;
- reported events;
- project statements;
- calculations;
- assumptions;
- competing explanations;
- source conflicts;
- uncertainty;
- known gaps;
- event timing;
- market structure;
- invalidation conditions; and
- follow-up questions.

### 5. Generate a Structured Draft

The user may choose:

- market brief;
- asset note;
- token note;
- project note;
- sector note;
- chart-context note;
- watchlist update;
- scenario comparison;
- journal review;
- educational explanation;
- public-safe update; or
- team handoff.

AI-generated conclusions remain drafts until reviewed.

### 6. Review

The reviewer checks:

- asset and pair;
- venue;
- period and timezone;
- source freshness;
- event state;
- supply terminology;
- calculation method;
- missing sources;
- conflicting evidence;
- unsupported causal claims;
- uncertainty;
- public suitability;
- private information;
- conflicts of interest; and
- required specialist review.

### 7. Approve, Record, or Withdraw

A reviewed output may be:

- approved for private use;
- approved for team use;
- approved for public use;
- returned for correction;
- marked provisional;
- superseded;
- withdrawn; or
- archived.

The record should preserve:

- version;
- source set;
- as-of time;
- reviewer;
- approval state;
- correction history; and
- next review condition.

### 8. Revisit

A later review may compare:

- new market data;
- changed project documents;
- completed or cancelled events;
- updated supply information;
- changed venue status;
- changed liquidity conditions;
- prior assumptions;
- invalidated scenarios;
- journal outcomes; and
- unresolved questions.

The purpose is to understand what changed rather than recreate the research from memory.

## Core Workspaces

### Market Brief

A market brief may summarize selected:

- price;
- volume;
- volatility;
- spread;
- depth;
- liquidity;
- derivatives context;
- macro context;
- sector context;
- news;
- scheduled events;
- project events;
- narrative context;
- onchain observations; and
- risk conditions.

The brief should identify:

- as-of time;
- period;
- venues;
- methodology;
- source set;
- delayed or missing data;
- observed facts;
- possible explanations;
- conflicting signals;
- uncertainty; and
- follow-up conditions.

A market move may have several plausible contributors.

QTB should avoid presenting one cause as established when the evidence supports only correlation or inference.

### Watchlists

A watchlist may track:

- asset;
- project;
- sector;
- narrative;
- public event;
- token release or unlock;
- governance event;
- documentation change;
- exchange-access change;
- liquidity condition;
- spread condition;
- volatility condition;
- technical level;
- onchain condition;
- product milestone;
- legal or regulatory development; or
- another user-defined condition.

Each watchlist item should identify:

- question;
- source;
- venue;
- timeframe;
- condition;
- current state;
- last review;
- next review;
- alert setting;
- owner; and
- archive rule.

A watchlist is an observation tool.

It is not a trade instruction or guarantee that an opportunity exists.

### Project and Token Research

A research note may organize:

- product purpose;
- user need;
- team and governance claims from approved sources;
- token role;
- total supply;
- allocation;
- release schedule;
- unlocked supply;
- circulating-supply methodology;
- treasury or reserve statements;
- contract and network;
- utility status;
- claim status;
- roadmap or product status;
- exchange-access status;
- liquidity context;
- holder and wallet context;
- ecosystem activity;
- community activity;
- competing products;
- material risks;
- source conflicts; and
- open questions.

QTB should distinguish:

- allocation;
- release;
- unlock;
- distribution;
- circulation;
- exchange balance;
- treasury balance;
- liquidity provision;
- market-making inventory;
- holder count;
- wallet count; and
- beneficial ownership.

These are different concepts.

A wallet count is not automatically a unique-person count.

A public wallet balance is not automatically evidence of private identity, beneficial ownership, liquidity, or intent to sell.

### Chart Context

Chart context may describe:

- trend;
- range;
- support or resistance observations;
- volume;
- volatility;
- momentum;
- gap;
- market structure;
- liquidity zones;
- correlation;
- divergence;
- scenario levels; and
- invalidation conditions.

The note should identify:

- asset and pair;
- venue;
- market type;
- interval;
- period;
- indicator settings;
- as-of time;
- missing data;
- whether levels are observed or calculated; and
- whether the interpretation is descriptive or scenario-based.

Technical analysis does not provide certainty.

A level may fail, a market may gap, liquidity may disappear, and venue prices may diverge.

### Scenario Analysis

A scenario is a conditional interpretation, not a prediction.

A scenario should identify:

- starting evidence;
- assumptions;
- trigger;
- confirmation condition;
- invalidation condition;
- relevant timeframe;
- relevant venue;
- downside or adverse condition;
- missing information;
- review point; and
- alternative explanations.

Possible states include:

- proposed;
- active for review;
- supported by new evidence;
- weakened;
- invalidated;
- expired;
- superseded; and
- archived.

A model-generated confidence label is not a probability of profit.

### Trading Journal

A private journal may record:

- research question;
- thesis;
- source set;
- decision context;
- planned risk;
- entry or exit rationale;
- conditions considered;
- scenario and invalidation;
- emotional or behavioral notes;
- execution record entered by the user;
- result;
- process error;
- missed condition;
- review notes; and
- lesson.

QTB may help identify repeated patterns across selected entries.

It should distinguish:

- user-entered fact;
- imported record;
- AI-generated observation;
- reviewer conclusion; and
- unresolved pattern.

Private journal content should not become visible to a team, public audience, advertiser, partner, product community, wallet workflow, or unrelated service without authorization.

A journal pattern does not automatically establish a medical, psychological, professional, or legal conclusion.

### Educational Explanations

QTB may help explain:

- liquidity;
- spread;
- depth;
- slippage;
- volatility;
- token supply;
- token release;
- circulation;
- market structure;
- order books;
- decentralized venues;
- centralized venues;
- derivatives;
- funding rates;
- liquidation;
- risk management;
- wallet and custody models;
- research methods; and
- another selected market concept.

An explanation should identify:

- intended audience;
- current or stable knowledge;
- examples;
- assumptions;
- source date;
- jurisdiction-specific boundary where relevant; and
- where specialist advice is required.

[TrainLayer AI](06-HERHELP_TRAINLAYER_AI_PUBLIC.md) may convert reviewed material into a structured learning module.

## Output Structure

A QTB output may include:

1. question and purpose;
2. asset, venue, period, and timezone;
3. as-of time and source set;
4. observed facts;
5. source-reported statements;
6. calculated or derived indicators;
7. market or project context;
8. scenarios;
9. conflicting signals;
10. uncertainty and missing information;
11. risk observations;
12. invalidation conditions;
13. follow-up research;
14. reviewer notes; and
15. approval or publication state.

This structure helps readers understand the basis of an interpretation and makes later correction easier.

Evidence or confidence labels should describe the method used.

They should not imply:

- certainty;
- probability of profit;
- guaranteed accuracy;
- guaranteed price direction;
- guaranteed liquidity;
- guaranteed execution; or
- guaranteed market access.

## Alerts and Scheduled Review

Where supported, QTB may monitor a user-defined condition and create a review item.

Conditions may relate to:

- price;
- percentage movement;
- volume;
- volatility;
- spread;
- depth;
- public announcement;
- scheduled event;
- document change;
- token release;
- governance action;
- exchange-access status;
- onchain observation;
- news publication;
- watchlist review date; or
- another available data point.

An alert record should show:

- condition requested;
- asset;
- pair;
- venue;
- source;
- threshold or event;
- observation time;
- retrieval time;
- detected value or event;
- delay or data-quality note;
- related watchlist or research item;
- delivery state;
- review state; and
- correction history.

Possible alert states include:

- configured;
- active;
- triggered;
- delivered;
- delayed;
- failed;
- duplicated;
- acknowledged;
- reviewed;
- dismissed;
- corrected;
- expired; and
- cancelled.

Users should account for:

- feed delay;
- venue outage;
- source outage;
- stale data;
- inconsistent prices;
- false positives;
- missed conditions;
- duplicate delivery;
- timezone error;
- threshold crossing between observations; and
- changing market conditions.

An alert is a prompt for review.

It does not establish that an opportunity remains available or that an action should be taken.

## Practical Workflows

### Daily Market Review

A user selects a watchlist, venues, period, and timezone.

QTB organizes:

- major observed changes;
- relevant public events;
- venue differences;
- source gaps;
- conflicting signals;
- scenario changes;
- risk notes; and
- follow-up questions.

The user records personal conclusions separately.

### Token Research

The user supplies a project and approved sources.

QTB prepares a source-linked note across:

- product;
- token role;
- supply;
- allocation;
- release;
- circulation;
- governance;
- utility status;
- market access;
- liquidity context;
- ecosystem activity;
- community activity;
- risks; and
- unresolved verification needs.

### Event Review

A user tracks an announced token release, governance vote, product launch, listing process, or another event.

QTB distinguishes:

- announced;
- scheduled;
- under review;
- approved;
- activated;
- completed;
- delayed;
- cancelled;
- disputed; and
- corrected.

### Journal Review

A user selects private journal entries.

QTB groups possible patterns in:

- research process;
- source selection;
- timing;
- risk planning;
- invalidation discipline;
- repeated mistakes;
- emotional notes; and
- post-decision review.

The user determines whether a pattern is meaningful and what action to take.

### Community Update

A community administrator selects public sources and a narrow topic.

QTB drafts neutral context with:

- as-of time;
- source links;
- facts;
- interpretation;
- uncertainty;
- missing information;
- risk language; and
- publication notes.

[CommunityLayer AI](07-HERHELP_COMMUNITYLAYER_AI_PUBLIC.md) may support the separate review, publication, moderation, and community-support workflow.

### Team Research Handoff

An analyst records:

- question;
- scope;
- source set;
- findings;
- conflicts;
- assumptions;
- unresolved questions;
- invalidation conditions;
- next review date; and
- owner.

Another authorized team member can continue without losing the original context.

## Public Communication

QTB may assist with public market-context material.

A public output should:

- use public or specifically approved sources;
- identify asset, venue, period, and as-of time;
- distinguish facts from interpretation;
- distinguish project statements from independent observations;
- describe uncertainty;
- disclose material methodology;
- identify delayed or missing data;
- avoid individualized advice;
- avoid undisclosed private positions or trading plans;
- avoid unsupported causal claims;
- avoid guaranteed price, return, liquidity, demand, listing, or market-access language;
- avoid presenting a scenario as a prediction;
- avoid exposing private journal or team research; and
- receive authorized review before publication.

A public communication record may identify:

- draft owner;
- source set;
- reviewer;
- approval time;
- publication channel;
- as-of time;
- correction route;
- withdrawal state; and
- archive state.

## AI Role and Human Authority

AI may assist with:

- source organization;
- summarization;
- comparison;
- contradiction detection;
- scenario drafting;
- chart-context drafting;
- watchlist review;
- journal-pattern drafting;
- alert explanation;
- glossary preparation;
- public-safe redrafting;
- report formatting; and
- follow-up-question generation.

AI does not automatically:

- verify every source;
- determine market truth;
- determine causation;
- predict price;
- guarantee a signal;
- determine suitability;
- manage a portfolio;
- execute a trade;
- move funds;
- approve a market action;
- verify legal compliance;
- verify exchange listing;
- verify liquidity availability;
- determine token value;
- determine wallet ownership; or
- replace authorized human review.

Review strength should match the impact and audience.

| Output or action | Typical review |
|---|---|
| Private research draft | User review |
| Team research | Authorized analyst or team reviewer |
| Public market brief | Authorized publisher and factual review |
| Token or supply analysis | Source, methodology, and terminology review |
| Legal or regulatory interpretation | Appropriate legal or compliance review |
| Treasury or operational decision context | Authorized organization review |
| Transition to liquidity operations | Destination workflow authorization under AIMM controls |
| Personalized financial decision | User responsibility and appropriate licensed advice where required |

## Platform Credit Use

QTB may use Platform Credits for metered processing such as:

- generating a market brief;
- comparing a watchlist period;
- preparing a token or project note;
- analyzing selected journal entries;
- drafting chart context;
- comparing scenarios;
- monitoring a defined condition;
- explaining an alert;
- comparing document versions;
- producing a public-safe market update;
- creating an educational explanation;
- formatting a team research report; or
- preparing a correction summary.

The interface should show, where applicable:

- task;
- source scope;
- asset count;
- venue count;
- period;
- output type;
- fixed amount, estimate, range, or maximum;
- available balance;
- authorization;
- reservation state;
- completion condition;
- partial-completion treatment;
- failure or reversal treatment; and
- final usage record.

A standard lifecycle may be:

```text
quote -> authorize -> reserve if needed -> process
-> complete, partially complete, fail, or cancel
-> consume, release, reverse, or correct -> record
```

Platform Credits are product usage credits.

They remain separate from:

- portfolio value;
- trading capital;
- stablecoins;
- wallets;
- FUZE token;
- token participation;
- positions;
- profits;
- losses;
- claims;
- payouts;
- market access; and
- investment rights.

## Data, Permissions, and Privacy

QTB may contain:

- private watchlists;
- personal research;
- team research;
- unpublished reports;
- trading-journal entries;
- portfolio references entered by the user;
- account or execution references entered by the user;
- communication plans;
- public drafts;
- user-defined alerts;
- connected-source credentials;
- proprietary methodology;
- risk notes; and
- reviewer comments.

Controls may include:

- private and team workspaces;
- source-connection authorization;
- role-based access;
- restricted journal visibility;
- field and source selection;
- review before team sharing;
- review before publication;
- export controls;
- retention and deletion settings;
- connection revocation;
- provider-routing controls;
- secret and credential separation;
- output-version history;
- correction history;
- incident handling; and
- public-report de-identification.

Private journal entries, positions, strategy notes, unpublished research, and user-specific conclusions should not be included in public reporting.

Wallet data is generally unnecessary for ordinary market interpretation.

Any wallet-based access, billing, or separately activated feature should remain separate from:

- private research content;
- journal content;
- personal identity;
- unpublished positions;
- team conclusions; and
- public reporting.

The [FUZE Data Privacy and AI Data Handling](../CORE-PLATFORM-PAPERS/07-FUZE_DATA_PRIVACY_AND_AI_DATA_HANDLING_PUBLIC.md) provides the wider model.

## Provider and Data-Feed Boundaries

Where QTB uses an external model, market feed, news source, chart provider, storage provider, connector, or monitoring service, the product should evaluate:

- source scope;
- data license;
- delay;
- venue coverage;
- historical coverage;
- correction policy;
- availability;
- authentication;
- personal data sent;
- private research sent;
- provider retention;
- model-training or service-improvement settings;
- processing location where relevant;
- subcontractors;
- deletion capability;
- output logging;
- incident handling; and
- contractual and security controls.

A fallback provider should not silently weaken:

- freshness;
- venue coverage;
- source attribution;
- privacy;
- journal confidentiality;
- methodology;
- retention;
- market-pair accuracy; or
- user-facing expectations.

A feed value should not be presented as current when the source is stale, delayed, unavailable, or substituted.

## Reliability and Model-Risk Controls

QTB outputs may be affected by:

- stale data;
- missing venues;
- inconsistent symbols;
- wrong contract;
- wrong network;
- wrong market pair;
- timezone error;
- duplicate news;
- corrected news;
- project misinformation;
- social manipulation;
- fake announcements;
- model hallucination;
- unsupported causal inference;
- chart-indicator misuse;
- overfitting;
- survivorship bias;
- selection bias;
- look-ahead bias;
- incomplete supply data;
- custodial-wallet ambiguity;
- API outage;
- connector failure;
- prompt injection inside connected content; and
- human confirmation bias.

Controls may include:

- source attribution;
- freshness checks;
- venue and pair confirmation;
- contract confirmation;
- independent-source comparison;
- assumption labeling;
- calculation disclosure;
- contradiction surfacing;
- scenario and invalidation fields;
- restricted use of private data;
- public-review gates;
- correction history;
- model-output labeling; and
- human review.

A model should not treat instructions embedded in connected market content as authority to override system, workspace, privacy, or publication controls.

## Reporting

Product reporting may include:

- research tasks by type and status;
- source availability;
- source freshness;
- feed delay;
- venue coverage;
- watchlist activity;
- alert configuration;
- alert delivery;
- output review;
- publication state;
- corrections;
- withdrawn outputs;
- provider or processing errors;
- Platform Credit usage;
- support activity; and
- aggregated product activity.

Reports should distinguish:

- source connected;
- source available;
- source retrieved;
- source current;
- research started;
- draft generated;
- reviewed;
- approved;
- published;
- corrected;
- withdrawn;
- alert configured;
- alert triggered;
- alert delivered;
- alert reviewed; and
- follow-up completed.

These states are not interchangeable.

Public reporting should exclude:

- private conclusions;
- journal details;
- user positions;
- unpublished research;
- private strategy;
- proprietary methodology;
- credentials;
- private source access;
- wallet-to-person mappings;
- partner-confidential material; and
- personally identifying activity.

A high research-task or alert count does not independently prove:

- research quality;
- prediction accuracy;
- profitable decisions;
- product adoption;
- retention;
- revenue;
- token demand; or
- investment performance.

Reporting should follow the [FUZE Transparency and Reporting Rails](../CORE-PLATFORM-PAPERS/09-FUZE_TRANSPARENCY_AND_REPORTING_RAILS_PUBLIC.md).

## Error, Correction, and Support Model

QTB should support clear treatment for:

- wrong asset;
- wrong symbol;
- wrong contract;
- wrong network;
- wrong market pair;
- wrong venue;
- wrong timeframe;
- wrong timezone;
- stale feed;
- missing feed;
- duplicate event;
- corrected announcement;
- missing source;
- inaccessible source;
- wrong supply terminology;
- calculation error;
- chart error;
- alert false positive;
- missed alert;
- duplicate alert;
- failed connector;
- provider failure;
- private data in a public draft;
- unsupported causal claim;
- unsupported confidence label;
- Platform Credit mismatch;
- missing version history; and
- public-report error.

A correction record should identify:

- original output;
- asset, venue, pair, period, and timezone;
- affected source;
- affected calculation or interpretation;
- correction reason;
- reviewer;
- corrected output;
- alert or watchlist effect;
- publication effect;
- withdrawal requirement;
- downstream report effect; and
- support status.

A corrected or withdrawn output should not remain represented as current without an explicit historical label.

## Separation from Trading Execution

QTB may help a user prepare context before a decision and review the process after a decision.

It should not independently:

- place an order;
- cancel an order;
- modify an order;
- sign a transaction;
- move funds;
- connect to a broker for autonomous execution;
- manage position size;
- rebalance a portfolio;
- select leverage;
- liquidate a position;
- promise best execution;
- guarantee a fill;
- guarantee a price; or
- guarantee a return.

If a user or organization moves from research to an operational action, the destination system must apply its own:

- authorization;
- permissions;
- account controls;
- risk limits;
- review;
- execution rules;
- custody rules;
- monitoring;
- correction; and
- reporting.

QTB research approval is not execution approval.

## Separation from AIMM

QTB and AIMM serve different purposes.

| Area | QTB | AIMM |
|---|---|---|
| Primary purpose | Market research and interpretation | Authorized liquidity-operations intelligence, monitoring, and reporting |
| Main user task | Understand selected market context | Review and supervise defined liquidity-operation objectives and conditions |
| Output | Research note, scenario, alert, journal, or public brief | Operational dashboard, alert, review item, reconciliation, or report |
| Authority | Research-layer user or reviewer | Authorized operational roles under destination controls |
| Execution | No autonomous trade execution | Does not authorize uncontrolled or deceptive market action |
| Main boundary | Not advice, execution, or guaranteed signal | Not price protection, guaranteed liquidity, or guaranteed profitability |

A QTB observation may be referenced inside an AIMM review only through an authorized handoff.

The handoff should identify:

- source output;
- asset and venue;
- as-of time;
- methodology;
- assumptions;
- unresolved conflicts;
- reviewer;
- destination purpose;
- destination permissions; and
- expiry or next-review condition.

QTB interpretation should not silently become an operational instruction.

## Product Status and Evidence

QTB is presented as a developing product unless current evidence supports a stronger status.

Different capabilities may have different statuses.

Possible evidence includes:

| Status claim | Evidence direction |
|---|---|
| Product designed | Defined source model, research lifecycle, workspaces, controls, data, reporting, and boundaries |
| Prototype exists | Reviewable source-to-brief, watchlist, chart, journal, alert, or handoff workflow |
| Feed connected | Working authorized feed with documented venue, pair, delay, freshness, error, and correction behavior |
| Watchlist implemented | Working item creation, review, status, alert link, history, and correction behavior |
| Alerts implemented | Working condition, observation, delivery, failure, acknowledgement, and correction behavior |
| Journal implemented | Working private entry, selection, analysis, visibility, export, and deletion behavior |
| Team research implemented | Working roles, sharing, review, version, approval, and withdrawal behavior |
| Internally tested | Test evidence for source conflict, stale data, wrong pair, privacy, provider failure, alerts, and correction |
| Limited release | Controlled users, supported sources, current terms, support, monitoring, and known limitations |
| Public beta | Public access route, beta terms, supported features, support, and release notes |
| Live | Production access, current features, support, monitoring, and operating evidence |
| Paid delivery | Pricing, payment, active service, fulfillment, support, and customer evidence |
| Revenue confirmed | Reconciled payment, completed service, accounting treatment, period, and review |

The following do not independently prove a live product:

- this paper;
- a sample market brief;
- a screenshot;
- a watchlist mockup;
- a chart explanation;
- code;
- a repository;
- a model prompt;
- an alert concept;
- a pricing concept; or
- a roadmap date.

Current status should be checked in the [FUZE Public Status and Roadmap Matrix](../PUBLIC-INDEX/02-FUZE_PUBLIC_STATUS_AND_ROADMAP_MATRIX.md).

## Product, Token, Payment, and Market Separation

The following remain separate:

- market research;
- chart interpretation;
- watchlists;
- alerts;
- journal records;
- operational decisions;
- trade execution;
- portfolio value;
- Platform Credits;
- payments;
- stablecoins;
- wallets;
- FUZE token utility;
- token participation;
- claims;
- payouts;
- DEX access;
- CEX access;
- liquidity; and
- market price.

A research note, alert, chart, wallet link, token balance, payment, or Platform Credit event does not automatically establish:

- a trade recommendation;
- execution authority;
- active token utility;
- wallet eligibility beyond a defined rule;
- approved distributable value;
- a claim;
- a payout;
- token circulation;
- DEX liquidity;
- CEX listing;
- token demand;
- price support; or
- financial return.

A QTB paper or output should not be used as evidence of exchange approval, listing, liquidity, price support, market-making performance, or token value.

## Public Boundary

QTB can help users organize market information, compare sources, prepare scenarios, maintain watchlists, review journals, generate alerts, and produce reviewed market-context outputs.

It cannot independently establish:

- truth of every source;
- complete market coverage;
- current price on every venue;
- causation;
- future price direction;
- profitable opportunity;
- suitability for a user;
- trade execution;
- best execution;
- liquidity availability;
- market access;
- listing approval;
- wallet ownership;
- token value;
- price support;
- income;
- payout;
- adoption;
- revenue;
- profitability; or
- financial return.

Users and authorized organizations remain responsible for:

- source selection;
- factual verification;
- venue and timeframe selection;
- methodology;
- risk decisions;
- professional or licensed advice where required;
- execution authorization;
- custody;
- public communication;
- privacy;
- correction;
- support; and
- compliance with applicable rules.

Detailed product risks appear in [FUZE Product Risk Boundaries](16-FUZE_PRODUCT_RISK_BOUNDARIES_PUBLIC.md). Consolidated limitations appear in the [FUZE Risk and Disclosure Appendix](../WHITEPAPER-PAPERS/05-FUZE_RISK_AND_DISCLOSURE_APPENDIX_PUBLIC.md).

## Key Takeaways

- QTB is a market-research and decision-context product, not an autonomous trading system.
- Asset, venue, market pair, period, timezone, source, freshness, and methodology are core parts of every reliable output.
- QTB should distinguish observed facts, source claims, calculations, assumptions, scenarios, conflicts, and reviewer conclusions.
- Watchlists and alerts prompt review; they are not guaranteed opportunities or trade instructions.
- Token research must distinguish allocation, release, unlock, circulation, exchange balance, liquidity, wallet count, and beneficial ownership.
- Private journal and team research require strict permission and publication controls.
- QTB research approval is not execution approval.
- QTB remains separate from AIMM, which handles authorized liquidity-operations intelligence, monitoring, and reporting.
- Platform Credits meter defined research processing and remain separate from trading capital, wallets, stablecoins, and FUZE token.
- This paper does not prove that live feeds, alerts, journals, team research, paid delivery, adoption, or revenue are active.
- QTB succeeds only when it improves research discipline without overstating certainty, causation, execution authority, or financial outcome.