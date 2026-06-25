# ZAGA Arena

## Executive Summary

ZAGA Arena is the short-session battle-arena product in the ZAGA family.

Players enter a run, move and dodge, fight enemy waves and bosses, collect game drops, choose temporary strategies, build a run score called **Net Worth**, and review results through supported summaries, leaderboards, badges, event records, and shareable outputs.

The product is designed around a direct loop:

```text
enter -> learn the rules -> fight -> survive -> make choices
-> build the run score -> finish -> review -> replay
```

ZAGA Arena may use market-inspired terms such as:

- USDT;
- Token Value;
- Net Worth;
- Liquidity Node;
- Market Role;
- Strategy Option;
- treasury;
- price;
- resource; and
- reward.

In the ordinary Arena context, these are gameplay, scoring, progression, or narrative terms.

They do not automatically represent:

- real USDT;
- stablecoin balances;
- legal ownership;
- redeemable assets;
- token allocation;
- payment;
- payout;
- income;
- investment return;
- exchange access;
- liquidity; or
- future financial value.

Any wallet-aware, FUZE-token, claim, payment, or externally redeemable mechanism must be separately defined, authorized, implemented, tested, activated, and disclosed.

ZAGA Arena remains separate from [ZAGA Districts](10-ZAGA_DISTRICTS_PUBLIC.md). Arena runs do not automatically create Districts roles, resources, property, city progress, faction progress, or governance rights.

## Purpose of This Paper

This paper explains:

- the Arena product purpose;
- intended players and organizers;
- the run lifecycle;
- combat, waves, bosses, drops, strategy, and scoring;
- market-inspired gameplay terminology;
- progression and recognition;
- leaderboards, events, and shareable results;
- anti-cheat, anti-abuse, dispute, and correction controls;
- Platform Credit usage;
- wallet-aware and token-related boundaries;
- data and privacy controls;
- reporting and evidence discipline;
- product status; and
- public limitations.

ZAGA Arena is one product inside the [ZAGA family](08-ZAGA_PUBLIC.md).

## Product Purpose

ZAGA Arena is designed to provide a game session that:

- starts quickly;
- is understandable to a new player;
- becomes more strategic with experience;
- supports replay for a better result;
- creates visible feedback during play;
- provides a clear end condition;
- explains the final score;
- supports fair event and leaderboard rules;
- can be shared through approved community surfaces; and
- remains enjoyable without requiring wallet or token participation.

The product may support:

- solo runs;
- cooperative play;
- competitive matches;
- boss events;
- score challenges;
- survival challenges;
- seasonal modes;
- community events;
- Telegram-ready entry or sharing;
- browser access; and
- other explicitly supported modes.

Availability depends on the current release.

A product paper, mockup, screenshot, codebase, prototype video, or event concept does not independently prove that a mode is live.

## Intended Players and Operators

| User | Typical need |
|---|---|
| First-time player | Clear controls, tutorial, objectives, hazards, and result explanation |
| Returning player | Strategy variation, harder encounters, progression, and score improvement |
| Competitive player | Defined rules, valid-run criteria, leaderboard methodology, and dispute route |
| Casual player | Short session, readable feedback, and easy replay |
| Telegram community | Entry links, event reminders, score sharing, and community recaps |
| Event organizer | Time-bounded setup, eligibility, scoring, anti-abuse review, and result publication |
| Moderator or support operator | Player support, content review, disputes, and corrections |
| Product reviewer | Build status, test evidence, telemetry definitions, issue history, and known limitations |
| Reporting reviewer | Public-safe activity summaries with clear metric definitions |

Access requirements may differ by:

- release stage;
- browser;
- device;
- network;
- Telegram availability;
- event;
- age;
- jurisdiction;
- account requirement;
- community rule;
- multiplayer availability;
- wallet requirement where separately activated; and
- technical capacity.

## Run Lifecycle

### 1. Enter the Supported Surface

A player opens the available:

- browser surface;
- Telegram-ready surface;
- event link;
- test build;
- supported client; or
- another current entry route.

The entry surface should identify:

- release or build;
- mode;
- current status;
- device requirements;
- rules;
- data use;
- known limitations;
- support route; and
- event terms where applicable.

### 2. Establish the Player Context

The run may use:

- player profile;
- chosen display name;
- anonymous or guest session where supported;
- event entry;
- community association;
- selected character;
- selected Market Role;
- selected loadout;
- selected difficulty;
- wallet condition where separately activated; and
- current rule acknowledgement.

A display name or player identifier is not automatically legal identity.

### 3. Review Controls and Rules

The player should be able to review:

- movement;
- attack;
- aiming;
- dodge or defensive action;
- interaction;
- pause behavior;
- score basis;
- collection rules;
- boss rules;
- run-ending conditions;
- event modifiers;
- supported input methods;
- anti-abuse expectations; and
- public leaderboard treatment.

### 4. Begin the Run

The system creates a run or match record containing, where supported:

- run identifier;
- player identifier;
- event identifier;
- game version;
- rule version;
- mode;
- start time;
- device or client context;
- initial role or loadout;
- eligibility state; and
- telemetry status.

### 5. Fight and Survive

The player moves through:

- ordinary enemies;
- stronger enemy variants;
- hazards;
- waves;
- objectives;
- drops;
- temporary choices;
- boss phases; and
- event-specific mechanics.

The interface should provide understandable feedback for:

- damage dealt;
- damage received;
- health or status;
- incoming danger;
- collected values;
- strategy changes;
- score changes;
- active effects;
- boss phase;
- objective progress; and
- run-ending risk.

### 6. Finish the Run

A run may finish through:

- player defeat;
- time limit;
- objective completion;
- boss defeat;
- event completion;
- team result;
- voluntary exit;
- disconnect;
- invalidation;
- administrative stop; or
- another stated condition.

The result should identify the end condition.

A disconnect, crash, timeout, or incomplete telemetry event should not silently become a normal completed result.

### 7. Validate the Result

Before a result is accepted for a leaderboard, event, badge, or public summary, the product may check:

- supported build;
- supported client;
- eligibility;
- required telemetry;
- score consistency;
- timing consistency;
- impossible-state indicators;
- duplicate run;
- automation indicators;
- event period;
- rule version;
- moderation state; and
- correction history.

A validation check may produce:

- accepted;
- pending review;
- partially recorded;
- invalid;
- disputed;
- corrected;
- removed; or
- restored.

### 8. Review and Share

The player may review:

- score;
- survival time;
- enemies defeated;
- bosses defeated;
- game values collected;
- strategy choices;
- Market Role;
- badges;
- leaderboard status;
- event status;
- validation status;
- shareable result; and
- correction or dispute route.

Public sharing should use a suitable game identity and should not reveal private account, wallet, security, moderation, or device information.

### 9. Replay or Continue

The player may:

- replay the same mode;
- select another strategy;
- join an event;
- attempt a better score;
- review progression;
- enter another supported arena;
- report an issue; or
- exit.

## Combat System

### Movement and Positioning

Movement and positioning shape:

- enemy avoidance;
- attack range;
- safe space;
- access to drops;
- access to objectives;
- boss-pattern response;
- team coordination;
- escape routes; and
- risk-reward choices.

Supported movement may include:

- directional movement;
- dodge;
- dash;
- temporary speed effects;
- movement penalties;
- arena obstacles;
- hazard zones; and
- event-specific movement rules.

The interface should communicate movement restrictions and hazards clearly.

### Attacks and Feedback

Supported combat may include:

- aiming;
- shooting;
- projectiles;
- area attacks;
- melee attacks;
- temporary abilities;
- power-ups;
- cooldowns;
- critical effects;
- status effects;
- defensive effects; and
- event-specific mechanics.

Visual and audio feedback should help the player understand:

- successful hits;
- missed attacks;
- incoming damage;
- invulnerability;
- active effects;
- cooldown state;
- boss vulnerability;
- damage source; and
- defeat condition.

### Enemy Waves

A wave may vary by:

- enemy type;
- number;
- health;
- speed;
- route;
- attack pattern;
- spawn timing;
- arena position;
- objective pressure;
- environmental effect; and
- event modifier.

Wave difficulty should not be described as fair or balanced solely because it increases gradually.

Balance requires testing, telemetry, player feedback, and correction.

### Boss Encounters

Bosses may use:

- phases;
- telegraphed attacks;
- arena effects;
- temporary vulnerability;
- summoned enemies;
- special objectives;
- timed pressure;
- drop rules;
- score rules; and
- event-specific completion conditions.

A boss encounter should identify:

- entry condition;
- defeat condition;
- failure condition;
- score effect;
- drop effect;
- event effect;
- difficulty setting; and
- known special rules.

### Drops and Temporary Effects

Game drops may provide:

- score value;
- health;
- temporary power;
- temporary defense;
- movement effect;
- attack effect;
- strategy modifier;
- event progress; or
- another defined in-run benefit.

A drop should identify whether it is:

- temporary;
- run-specific;
- event-specific;
- account-bound;
- cosmetic;
- persistent; or
- externally meaningful under a separately activated mechanism.

Ordinary game drops are not automatically redeemable assets.

## Market-Inspired Game Mechanics

ZAGA Arena uses market-inspired language as a game theme.

| Term | Ordinary Arena meaning | What it does not automatically mean |
|---|---|---|
| USDT | Named in-game drop, score component, or run value | Real USDT or redeemable stablecoin balance |
| Token Value | Game variable affecting score, strategy, or run state | Price of a real token or investment return |
| Net Worth | Primary run score or value summary | Legal net worth, account balance, or redeemable asset |
| Liquidity Node | Contestable, drainable, defendable, or strategic game objective | Real liquidity pool or market-making position |
| Market Role | Selectable play style, class, or strategic identity | Regulated financial role or professional status |
| Strategy Option | Run-specific choice affecting risk, combat, movement, collection, or scoring | Trading advice or investment strategy |
| Treasury | Game, event, or narrative value container | Claim on real treasury assets |
| Reward | In-product result, recognition, or separately defined campaign item | Guaranteed payout, income, or token allocation |

The current game or event rules should define the actual calculation.

Market-inspired language does not provide:

- trading guidance;
- investment advice;
- price prediction;
- liquidity guarantee;
- token-value guarantee;
- income expectation;
- payout promise; or
- exchange-access promise.

## Scoring and Net Worth

Net Worth is the Arena run score or value summary where that mechanic is implemented.

A score may be affected by:

- survival time;
- enemies defeated;
- boss damage;
- bosses defeated;
- objectives completed;
- drops collected;
- strategy choices;
- Market Role;
- difficulty;
- event modifier;
- penalties;
- invalid activity;
- disconnect treatment; and
- completion condition.

The relevant rules should identify:

- included components;
- calculation order;
- multipliers;
- caps;
- floors;
- penalties;
- rounding;
- tie treatment;
- invalidation conditions;
- correction process; and
- rule version.

The result screen should show enough information for the player to understand why the score changed.

A score should not be presented as externally redeemable unless a separately approved mechanism expressly creates that right.

## Strategy and Progression

Replayability should come from meaningful choices rather than only larger enemy numbers.

Possible strategy dimensions include:

- aggressive or defensive movement;
- boss-focused or survival-focused play;
- score collection versus safe positioning;
- Liquidity Node control;
- Market Role selection;
- temporary modifiers;
- route choice;
- target priority;
- team composition;
- resource timing;
- event-specific risk; and
- power-up timing.

Progression may include:

- improved scores;
- profile history;
- unlocked options;
- difficulty access;
- cosmetics;
- achievements;
- badges;
- event recognition;
- role mastery records;
- tutorial completion; and
- supported account-level unlocks.

Every progression item should identify whether it is:

- run-specific;
- event-specific;
- seasonal;
- temporary;
- account-bound;
- cosmetic;
- persistent;
- transferable;
- wallet-linked; or
- externally meaningful under a separately activated rule.

Arena progression does not automatically create Districts progression.

## Run Summary

A run summary may include:

- run identifier;
- arena;
- event;
- release or build;
- rule version;
- start and end time;
- duration;
- survival time;
- enemies defeated;
- bosses attempted;
- bosses defeated;
- Net Worth;
- collected game values;
- Market Role;
- strategy choices;
- power-ups;
- completion or defeat condition;
- validation state;
- badge state;
- leaderboard state;
- correction state; and
- public share-card version.

A share card should exclude:

- private account identity;
- wallet-to-person mapping;
- device identifiers;
- security telemetry;
- moderation notes;
- anti-cheat methods;
- private event data; and
- restricted support records.

## Leaderboards

Leaderboards may be:

- daily;
- weekly;
- seasonal;
- all-time;
- event-based;
- boss-based;
- mode-based;
- community-based;
- team-based;
- role-based; or
- tied to another defined metric.

Every leaderboard should identify:

- product and mode;
- metric;
- rule version;
- eligible runs;
- start and end;
- timezone;
- supported build;
- tie rule;
- update timing;
- anti-abuse review;
- invalidation rule;
- correction process;
- display identity; and
- current status.

A rank may change when:

- new eligible results arrive;
- a run is corrected;
- an invalid result is removed;
- a restored result returns;
- a rule is corrected;
- an event closes; or
- a final review completes.

A leaderboard position does not automatically establish:

- payout eligibility;
- token allocation;
- professional status;
- future rank;
- financial value;
- legal right; or
- investment performance.

## Badges and Recognition

Badges may recognize:

- first run;
- survival milestone;
- boss defeat;
- event participation;
- event completion;
- strategy use;
- Market Role achievement;
- streak;
- community participation;
- score milestone;
- fair-play recognition; or
- another defined condition.

Every badge should identify:

- rule;
- period;
- qualifying activity;
- current status;
- correction process;
- expiry where applicable; and
- whether it is temporary, seasonal, account-bound, or persistent.

A badge does not automatically create:

- a governance right;
- property right;
- token right;
- claim;
- payout;
- future access;
- financial value; or
- investment right.

## Community Events

An organizer may use ZAGA Arena for a time-bounded challenge.

### Event Definition

An event should identify:

- organizer;
- mode or arena;
- boss where relevant;
- start and end;
- timezone;
- supported build;
- eligible players or communities;
- access method;
- account requirement;
- wallet requirement where separately activated;
- scoring rule;
- valid-run rule;
- allowed devices;
- team rule;
- leaderboard type;
- badge or recognition;
- prohibited conduct;
- anti-abuse process;
- dispute route;
- correction process;
- result-publication method;
- current status; and
- archive rule.

### Event States

Possible event states include:

- concept;
- draft;
- under review;
- approved;
- scheduled;
- active;
- paused;
- completed;
- under final review;
- disputed;
- corrected;
- cancelled;
- withdrawn; and
- archived.

An event page or announcement does not prove that the event is active.

### Telegram-Ready Participation

A supported Telegram surface may provide:

- entry links;
- reminders;
- score sharing;
- event updates;
- community leaderboard views;
- support routes;
- moderation notices; and
- public recaps.

Players should be able to distinguish:

- official product messages;
- official organizer messages;
- automated system messages;
- player-shared results;
- unofficial claims; and
- potentially deceptive messages.

### Result Publication

Organizers should review:

- event status;
- result validation;
- anti-abuse review;
- disputes;
- corrections;
- display identity;
- recognition fulfillment; and
- public-report scope

before presenting final results.

[CommunityLayer AI](07-HERHELP_COMMUNITYLAYER_AI_PUBLIC.md) may assist with approved support queues, event summaries, moderation, appeals, and public-safe recaps.

Final event rulings remain with the authorized event operator.

## Fair Play and Anti-Abuse Controls

Arena competition may face:

- bots;
- automated input;
- macros;
- multi-accounting;
- score manipulation;
- client tampering;
- memory or speed manipulation;
- replay manipulation;
- event-rule exploitation;
- collusion;
- connection abuse;
- duplicate submissions;
- forged screenshots;
- impersonation;
- false reports;
- coordinated reporting;
- account compromise;
- invalid build use;
- test-data leakage; and
- attempts to expose detection methods.

Controls may include:

- supported-client checks;
- build checks;
- server-side validation;
- event telemetry;
- rate limits;
- input-pattern review;
- impossible-state review;
- duplicate-run review;
- timing review;
- score-component review;
- session review;
- account and device review;
- restricted anti-cheat evidence;
- human investigation;
- temporary result hold;
- appeal;
- correction; and
- public-safe enforcement reporting.

An anomaly is not automatically proof of misconduct.

A high score is not automatically proof of cheating.

A failed anti-cheat check does not automatically prove guilt without review of the relevant evidence and system limitations.

High-impact actions should follow the applicable authority, review, notification, appeal, and correction process.

## Disputes and Appeals

A player may dispute, where supported:

- missing run;
- wrong score;
- wrong end condition;
- invalidation;
- event eligibility;
- leaderboard removal;
- badge denial;
- moderation action;
- account restriction;
- wallet-related eligibility;
- Platform Credit event; or
- public-report error.

A dispute record may include:

- player or event reference;
- run or match reference;
- build and rule version;
- disputed result;
- source evidence;
- player submission;
- reviewer;
- anti-abuse evidence where permitted;
- decision;
- correction;
- notification; and
- appeal state.

A material appeal should not be decided solely by the same automated output that supported the original action.

## Platform Credit Use

Platform Credits may meter defined Arena services such as:

- generating an enhanced run recap;
- generating a share card;
- preparing a community event;
- administering a supported event function;
- generating a leaderboard report;
- preparing a boss report;
- using an AI-assisted support function;
- preparing a public-safe event summary;
- processing a selected premium product feature; or
- using another clearly defined Arena service.

The interface should show, where applicable:

- action;
- usage unit;
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

Platform Credits are product-consumption units.

They remain separate from:

- Net Worth;
- game USDT;
- Token Value;
- drops;
- badges;
- scores;
- real stablecoins;
- wallets;
- FUZE token;
- token participation;
- claims;
- payouts;
- market access; and
- investment rights.

## Wallet-Aware Features

Some Arena features may use a wallet to check a specifically defined condition.

Possible examples include:

- entry to a controlled event;
- recognition of an eligible FUZE-holding wallet;
- token-gated access;
- campaign participation;
- a separately defined claim step;
- onchain event evidence; or
- another approved utility rule.

Every wallet-aware feature should identify:

- purpose;
- asset;
- network;
- contract where relevant;
- measurement or snapshot time;
- qualifying condition;
- self-custody or custodial treatment;
- evidence method;
- correction route;
- expiry;
- claim rule where applicable;
- public-report treatment; and
- activation status.

A wallet address does not automatically prove:

- legal identity;
- beneficial ownership;
- exchange-account ownership;
- entitlement to every Arena event;
- token utility;
- claim eligibility;
- payout; or
- financial right.

## FUZE Token Utility

Ordinary Arena play should not imply that a player earns, receives, holds, redeems, or is entitled to FUZE token.

A separately approved Arena utility may use FUZE token for a defined function such as:

- access;
- eligibility;
- recognition;
- participation gating;
- claim logic;
- campaign logic; or
- another activated product utility.

The utility must state:

- exact function;
- product scope;
- activation status;
- network;
- contract where relevant;
- eligibility;
- timing;
- limits;
- custody treatment;
- expiry;
- correction;
- reporting; and
- what the token does not provide.

The presence of:

- game USDT;
- Token Value;
- Net Worth;
- Liquidity Nodes;
- Market Roles;
- scores;
- badges;
- rankings; or
- rewards

does not create FUZE-token rights.

## Data and Privacy

ZAGA Arena may process:

- player profile;
- display name;
- guest or account reference;
- device and session information;
- client and build information;
- control and gameplay events;
- run and match telemetry;
- score components;
- enemy and boss events;
- progression;
- achievement and badge records;
- leaderboard records;
- event and community association;
- support records;
- moderation records;
- anti-cheat records;
- dispute and correction history;
- Platform Credit usage; and
- wallet information only where a separately activated feature requires it.

Controls may include:

- product and environment separation;
- test-data separation;
- public and private profile settings;
- selected display identity;
- role-based operator access;
- restricted anti-cheat records;
- event-specific access;
- wallet-purpose limitation;
- retention settings;
- export controls;
- deletion and correction handling;
- session revocation;
- connection revocation;
- provider and connector controls;
- incident handling; and
- public-report de-identification.

Public leaderboards and share cards should use a player-selected game identity or another suitable non-identifying reference.

Wallet addresses should not be linked publicly to private identity.

Security and anti-abuse records may require more restricted access and different retention from ordinary run history.

The [FUZE Data Privacy and AI Data Handling](../CORE-PLATFORM-PAPERS/07-FUZE_DATA_PRIVACY_AND_AI_DATA_HANDLING_PUBLIC.md) provides the wider model.

## Reporting

Arena reporting may include:

- release and build status;
- supported entry routes;
- supported modes;
- runs started;
- runs completed;
- valid runs;
- invalid runs;
- runs pending review;
- unique player or profile counts;
- survival distributions;
- completion distributions;
- score distributions;
- boss attempts;
- boss defeats;
- event participation;
- leaderboard updates;
- badges issued under defined rules;
- corrections;
- disputes;
- anti-abuse reviews;
- Platform Credit usage;
- support activity;
- incidents; and
- public community recaps.

Reports should distinguish:

- profile created;
- session started;
- run started;
- run ended;
- run completed;
- run validated;
- score accepted;
- leaderboard entry created;
- badge issued;
- event entered;
- event completed;
- dispute opened;
- correction completed; and
- public result published.

These states are not interchangeable.

A headline player or run count should identify:

- period;
- timezone;
- build;
- mode;
- unique-account method;
- guest treatment;
- bot or duplicate treatment;
- retry treatment;
- test-data treatment;
- incomplete-telemetry treatment;
- data freshness;
- exclusions; and
- known limitations.

A high run count does not independently prove:

- unique users;
- retention;
- satisfaction;
- fair play;
- product-market fit;
- token demand;
- revenue;
- profitability; or
- investment performance.

Reporting should follow the [FUZE Transparency and Reporting Rails](../CORE-PLATFORM-PAPERS/09-FUZE_TRANSPARENCY_AND_REPORTING_RAILS_PUBLIC.md).

## Error, Correction, and Support Model

ZAGA Arena should support clear treatment for:

- failed load;
- unsupported device;
- wrong build;
- failed input;
- disconnect;
- crash;
- missing run;
- incomplete telemetry;
- wrong score component;
- wrong score;
- wrong end condition;
- invalid leaderboard entry;
- missing badge;
- wrong event status;
- eligibility error;
- anti-cheat false positive;
- duplicate run;
- account compromise;
- moderation error;
- wallet-check error;
- failed claim where applicable;
- duplicate Platform Credit event;
- failed share card;
- failed connector;
- public-report error; and
- missing history.

A correction record should identify:

- original run, event, score, badge, wallet check, or report;
- build and rule version;
- source evidence;
- correction reason;
- reviewer;
- corrected result;
- leaderboard effect;
- badge effect;
- event effect;
- wallet or claim effect where relevant;
- player notification;
- appeal effect;
- downstream report effect; and
- support status.

A corrected or removed result should not remain represented as current without an explicit historical label.

## Product Status and Evidence

ZAGA Arena is presented as a developing product unless current evidence supports a stronger status.

Different capabilities may have different statuses.

Possible evidence includes:

| Status claim | Evidence direction |
|---|---|
| Product designed | Defined run loop, mechanics, scoring, events, controls, data, reporting, and boundaries |
| Prototype exists | Reviewable playable build with a supported run lifecycle |
| Combat implemented | Working movement, attack, enemy, damage, and result behavior in the cited build |
| Boss implemented | Working boss encounter with defined entry, phase, and completion behavior |
| Internally tested | Test evidence for normal, failure, scoring, telemetry, abuse, dispute, and correction paths |
| Limited test | Controlled players, current build, rules, support, monitoring, and known limitations |
| Public beta | Public access route, beta terms, supported features, support, and release notes |
| Live | Production access, current features, support, monitoring, and operating evidence |
| Telegram access active | Current supported bot or mini-app route, version, rules, support, and operating evidence |
| Leaderboard active | Current methodology, eligible runs, anti-abuse review, correction process, and live data |
| Wallet utility active | Current rule, asset, network, snapshot, contract where relevant, evidence, correction, and reporting |
| Token utility active | Current product scope, activation, contract where relevant, eligibility, limits, correction, and reporting |
| Paid delivery | Pricing, payment, active service, fulfillment, support, and customer evidence |
| Revenue confirmed | Reconciled payment, completed service, accounting treatment, period, and review |

The following do not independently prove a live product:

- this paper;
- concept art;
- screenshots;
- code;
- a repository;
- a local build;
- a prototype video;
- a Telegram bot shell;
- a leaderboard mockup;
- a sample score;
- an event concept;
- token references; or
- a roadmap date.

Current status should be checked in the [FUZE Public Status and Roadmap Matrix](../PUBLIC-INDEX/02-FUZE_PUBLIC_STATUS_AND_ROADMAP_MATRIX.md).

## Product, Token, Payment, and Market Separation

The following remain separate:

- ordinary gameplay;
- Net Worth;
- game USDT;
- Token Value;
- drops;
- badges;
- leaderboards;
- progression;
- Platform Credits;
- real payments;
- stablecoins;
- wallets;
- FUZE token utility;
- token participation;
- claims;
- payouts;
- DEX access;
- CEX access; and
- market price.

A run, score, badge, rank, wallet link, token balance, payment, or Platform Credit event does not automatically establish:

- ownership of a real asset;
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

A game paper should not be used as evidence of exchange approval, listing, liquidity, market-making performance, price support, or token value.

## Public Boundary

ZAGA Arena can provide a short-session battle game with runs, combat, bosses, scores, events, leaderboards, badges, and community participation where supported.

It cannot independently establish:

- release status;
- uninterrupted availability;
- compatibility with every device;
- fair play in every case;
- absence of cheating or abuse;
- legal identity;
- wallet ownership;
- real USDT;
- token value;
- redeemability;
- payout;
- income;
- legal ownership;
- token utility activation;
- claim eligibility;
- DEX liquidity;
- CEX listing;
- price support;
- adoption;
- retention;
- revenue;
- profitability; or
- financial return.

Product owners and authorized operators remain responsible for:

- gameplay rules;
- scoring;
- build status;
- event terms;
- anti-cheat controls;
- human review;
- player-impacting actions;
- disputes and appeals;
- wallet and token utility activation;
- privacy;
- public reporting;
- correction;
- support; and
- compliance with applicable rules.

Detailed product risks appear in [FUZE Product Risk Boundaries](16-FUZE_PRODUCT_RISK_BOUNDARIES_PUBLIC.md). Consolidated limitations appear in the [FUZE Risk and Disclosure Appendix](../WHITEPAPER-PAPERS/05-FUZE_RISK_AND_DISCLOSURE_APPENDIX_PUBLIC.md).

## Key Takeaways

- ZAGA Arena is the short-session action product inside the ZAGA family.
- The core loop is enter, fight, survive, make choices, build Net Worth, finish, review, and replay.
- Market-inspired terms are gameplay terms unless a separately activated mechanism expressly states otherwise.
- Net Worth, game USDT, Token Value, Liquidity Nodes, Market Roles, drops, badges, and rankings do not automatically represent real assets or financial rights.
- Scores, leaderboards, events, and badges require explicit rules, telemetry, anti-abuse review, disputes, and corrections.
- Arena identity, wallet identity, and private identity remain separate.
- Platform Credits meter defined product services and remain separate from game scores, wallets, real stablecoins, and FUZE token.
- Arena runs do not automatically create ZAGA Districts progress, roles, resources, or governance.
- This paper does not prove that browser access, Telegram access, multiplayer, bosses, events, leaderboards, wallet utility, token utility, paid delivery, or revenue are live.
- ZAGA Arena succeeds only when the game remains clear, responsive, replayable, fair enough to review, and honest about the boundary between play and financial value.