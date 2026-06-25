# HerHelp ShopOS AI

## Executive Summary

ShopOS AI is the HerHelp operating workspace for small shops, food stalls, cafés, market vendors, service counters, pop-up booths, local retailers, and other owner-operated businesses.

The product brings together practical daily workflows for:

- menu or catalog management;
- QR and staff-assisted ordering;
- checkout and payment-status recording;
- queues and service stages;
- preparation and handoff;
- stock and availability;
- staff tasks and permissions;
- devices and displays;
- loyalty and customer profiles;
- delivery coordination;
- customer communication;
- exception follow-up;
- TrustCheck review; and
- daily, shift, and period reporting.

ShopOS AI is designed for businesses that currently coordinate work through paper, chat, spreadsheets, payment applications, delivery platforms, and staff memory.

A shop may begin with a limited configuration, such as a QR menu and queue, then add supported functions when its workflow, staff, devices, and operating controls are ready.

ShopOS AI assists with preparation, coordination, visibility, and review. It does not replace operator approval, physical stock counts, payment-provider controls, accounting, tax, food-safety practice, employment responsibilities, delivery-provider controls, or other obligations that apply to the business.

## Purpose of This Paper

This paper explains:

- the product purpose and intended users;
- core operating areas;
- shop setup and role design;
- menu and catalog control;
- customer and order journeys;
- queue, preparation, handoff, and delivery workflows;
- payment and reconciliation boundaries;
- stock, staff, loyalty, customer, device, and TrustCheck functions;
- AI assistance and human approval;
- Platform Credit usage;
- data, privacy, and permission controls;
- reporting, correction, and support;
- status and evidence requirements; and
- public limitations.

ShopOS AI is a specialist product inside [HerHelp AI SaaS](02-HERHELP_AI_SAAS_PUBLIC.md). The wider product family appears in the [FUZE AI SaaS Product Index](01-FUZE_AI_SAAS_PRODUCT_INDEX_PUBLIC.md).

## Product Purpose

Small shops need software that fits the pace of the counter.

A system that requires extensive administration, complex devices, or specialist setup can create more work than it removes.

ShopOS AI is designed to give owners and authorized staff a clear operating view of:

- what can be sold;
- what is unavailable;
- which orders are active;
- where each order is in the queue;
- whether payment status is confirmed, pending, failed, refunded, or under review;
- what must be prepared or packed;
- which stock items need attention;
- which staff tasks remain incomplete;
- which delivery or customer issues remain open;
- which loyalty or campaign actions are active;
- which devices or channels are connected; and
- what the owner should review before closing the day.

The product should support the shop's actual service model rather than force one universal workflow.

Possible operating contexts include:

- quick-service food;
- cafés;
- market stalls;
- takeaway counters;
- small restaurants;
- retail booths;
- event shops;
- local delivery;
- service counters; and
- appointment or queue-based local services.

## Intended Users

| User | Typical need |
|---|---|
| Owner | Configure the shop, prices, permissions, reports, payments, and operating rules |
| Manager | Review shifts, staff, stock, issues, refunds, and exceptions |
| Counter staff | Create or confirm orders, record payment status, and manage customer-facing service |
| Preparation staff | Review station tasks, preparation notes, and order status |
| Packing or handoff staff | Confirm packing, pickup, delivery, and completion |
| Stock or purchasing staff | Review counts, low-stock items, adjustments, and purchase needs |
| Finance or bookkeeper | Review payment, refund, settlement, export, and reconciliation records |
| Marketing staff | Prepare approved promotions, loyalty offers, and communication content |
| Support partner | Assist only within the permissions granted by the shop |
| Customer | View supported menus, place orders, review queue state, and receive appropriate updates |

One person may hold several roles in a small shop.

The system should still preserve role-based access so that customer, payment, staff, supplier, and owner-only information is not exposed unnecessarily.

## Core Operating Areas

| Area | ShopOS AI role | What remains human or externally governed |
|---|---|---|
| Menu or catalog | Maintain items, categories, options, prices, descriptions, availability, and images | Final pricing, product claims, ingredients, legal notices, and availability approval |
| Orders | Capture selected items, quantities, options, notes, and status | Customer agreement, exception handling, and final fulfillment |
| Queue | Assign and display service position or reference | Real-world prioritization and local service decisions |
| Checkout | Present totals and record approved payment status | Authorization, settlement, chargebacks, provider controls, and accounting |
| Preparation | Organize station tasks and preparation notes | Food safety, quality, timing, and physical preparation |
| Handoff | Record pickup, packing, delivery, or service completion | Physical transfer and customer confirmation |
| Stock | Track selected products, ingredients, packaging, and exceptions | Physical count, waste, purchasing, and valuation approval |
| Staff | Organize shifts, roles, tasks, opening, handover, and closing | Employment, scheduling, compensation, discipline, and safety obligations |
| Loyalty | Support permissioned offers, visits, stamps, points, or redemptions | Customer consent, program terms, eligibility, and dispute resolution |
| Delivery | Coordinate preparation, packaging, handoff, and issue notes | External platform, driver, route, and delivery-provider controls |
| Communication | Prepare approved replies, announcements, menu copy, and promotions | Final review, timing, claims, destination, and publication authority |
| Devices | Connect supported displays, printers, screens, or audio devices | Hardware compatibility, maintenance, network, and physical security |
| TrustCheck | Organize exceptions, reviews, and corrective actions | Final judgment, investigation, staff decisions, and public claims |
| Reports | Summarize operations, payments, usage, issues, and corrections | Reconciliation, accounting, tax, audit, and public disclosure approval |

A shop does not need to activate every area.

Initial configuration should match the operator's real workflow, staff capacity, and available devices.

## Shop Setup

### Business Workspace

The owner creates a workspace for a:

- location;
- stall;
- booth;
- shop;
- counter;
- branch;
- event unit; or
- service point.

The workspace may define:

- legal or trading name where appropriate;
- public shop name;
- location;
- operating hours;
- service model;
- timezone;
- currency;
- tax settings where supported;
- order and queue rules;
- payment methods;
- delivery methods;
- staff roles;
- device access;
- reporting period;
- loyalty settings;
- support contacts; and
- retention settings.

A workspace should not be treated as evidence that every configured feature is active or legally approved.

### Roles and Permissions

Possible roles include:

| Role | Example authority |
|---|---|
| Owner | Full business configuration, access control, reports, payment methods, and integrations |
| Manager | Shift operations, refunds within limits, stock review, staff tasks, and exception handling |
| Counter staff | Order entry, customer-facing status, and approved payment recording |
| Preparation staff | Preparation queue and station completion |
| Packing or handoff staff | Packing, pickup, delivery handoff, and completion confirmation |
| Stock staff | Counts, adjustments, low-stock review, and purchase preparation |
| Finance reviewer | Payment, refund, settlement, and export review |
| Marketing editor | Menu copy, promotions, and campaign drafts |
| Publisher | Approval of public menus, announcements, campaigns, and offer terms |
| Viewer | Read-only access to approved operational views |
| Service partner | Limited access to an approved support or setup function |

Sensitive actions should require stronger authority than ordinary order handling.

Examples include:

- changing prices;
- issuing refunds;
- editing payment status;
- exporting customer data;
- changing loyalty balances;
- changing staff permissions;
- connecting devices;
- publishing promotions; or
- changing settlement information.

### Menu or Catalog Setup

The operator may enter or import items with fields such as:

- item name;
- category;
- base price;
- option groups;
- customer-facing description;
- availability;
- preparation or service notes;
- allergens or ingredient information where applicable;
- image;
- SKU or product identifier;
- tax treatment where supported;
- linked stock item; and
- channel availability.

AI assistance may help:

- draft descriptions;
- organize categories;
- prepare language variants;
- shorten menu copy;
- identify missing fields;
- compare prices or options across versions; and
- prepare public-safe item summaries.

The shop must review:

- price;
- quantity;
- ingredients;
- claims;
- allergens;
- availability;
- image rights;
- language; and
- channel suitability

before publication.

### Service Flow

The shop defines service statuses appropriate to its business.

A food workflow may use:

```text
received -> confirmed -> preparing -> ready -> handed off -> completed
```

A service business may use:

```text
requested -> accepted -> waiting -> serving -> completed
```

Possible exception states include:

- awaiting payment;
- payment under review;
- delayed;
- substituted;
- partially fulfilled;
- cancelled;
- refunded;
- failed;
- disputed; and
- corrected.

Status names should be understandable to staff and customers.

Internal operational detail should not be exposed on public queue displays unless appropriate.

### Devices and Displays

A basic setup may use:

- one phone;
- a printed QR code; and
- a staff-managed queue.

Depending on available support, a shop may later add:

- tablet;
- customer display;
- preparation screen;
- queue monitor;
- printer;
- label device;
- cash drawer integration;
- speaker;
- scanner; or
- staff device.

Device setup should identify:

- device owner;
- workspace;
- role;
- allowed functions;
- session duration;
- connection status;
- print or display destination;
- revocation method; and
- incident procedure.

Hardware availability, compatibility, and reliability depend on the configured release and operating environment.

## Customer and Order Journey

### 1. View Available Items

A customer may open a supported:

- QR menu;
- catalog;
- staff-assisted order surface;
- kiosk;
- counter display; or
- approved connected channel.

The displayed information should reflect the latest approved:

- items;
- prices;
- options;
- availability;
- offer terms;
- service hours; and
- fulfillment conditions.

A cached or delayed channel should show freshness or availability limitations where relevant.

### 2. Build the Order

The order may record:

- selected item;
- quantity;
- option choices;
- notes;
- pickup or delivery choice;
- service location;
- customer reference where required; and
- price snapshot.

The shop should collect only the customer information needed for:

- fulfillment;
- payment;
- delivery;
- loyalty;
- support; or
- another approved purpose.

### 3. Validate the Order

Before confirmation, the system may check:

- item availability;
- required options;
- quantity limits;
- service hours;
- delivery area;
- promotion eligibility;
- price version;
- duplicate submission; and
- customer confirmation.

An automated check does not replace staff review where the order is unusual, sensitive, or operationally difficult.

### 4. Confirm Checkout

ShopOS AI may present:

- items;
- quantities;
- options;
- discounts;
- taxes where supported;
- fees where applicable;
- total;
- payment method; and
- order reference.

The product may record status from an approved payment or checkout process.

Possible payment states include:

- not started;
- initiated;
- pending;
- authorized;
- confirmed;
- failed;
- cancelled;
- partially refunded;
- refunded;
- disputed;
- chargeback;
- manually reviewed; and
- corrected.

ShopOS AI should not mark payment as successful without the relevant provider confirmation or authorized operator action.

### 5. Assign Queue or Service Position

The system may assign:

- queue number;
- pickup reference;
- table reference;
- order code;
- appointment reference; or
- another service identifier.

Public displays should use a suitable reference rather than full customer identity.

### 6. Prepare and Update

Preparation staff may see:

- order reference;
- item and option details;
- approved notes;
- station;
- priority;
- elapsed time;
- packing requirements; and
- exception status.

Sensitive customer, payment, loyalty, or delivery information should not appear on preparation screens unless required.

### 7. Pack, Hand Off, or Deliver

The shop may record:

- quality check;
- packing check;
- pickup confirmation;
- delivery handoff;
- missing item;
- substitution;
- customer issue; and
- completion.

Physical fulfillment remains a real-world operator responsibility.

### 8. Close or Correct

An order may close as:

- completed;
- cancelled;
- partially fulfilled;
- refunded;
- disputed;
- failed; or
- corrected.

The final state should preserve relevant payment, fulfillment, exception, and support records.

## Queue and Service Operations

ShopOS AI may organize active work by:

- status;
- station;
- queue position;
- priority;
- service type;
- channel;
- delivery method;
- staff owner; or
- elapsed time.

Queue rules should be understandable and reviewable.

A queue system may need exception handling for:

- priority service;
- accessibility needs;
- missing payment;
- unavailable items;
- delayed preparation;
- customer absence;
- duplicate orders;
- cancelled orders; and
- manually corrected order sequence.

AI may help prepare queue announcements or service messages, but the shop determines:

- wording;
- language;
- timing;
- public suitability;
- customer reference; and
- device or channel.

## Payment, Settlement, and Reconciliation

ShopOS AI may support approved payment methods such as:

- cash;
- bank transfer;
- QR payment;
- payment link;
- card or provider checkout;
- wallet-based payment where specifically supported; or
- stablecoin payment where explicitly implemented and approved.

Payment status, settlement, fulfillment, and revenue remain separate.

```text
order total
-> payment initiated
-> payment confirmed
-> order fulfilled
-> payment reconciled
-> accounting treatment confirmed
```

A confirmed payment does not independently prove:

- fulfillment;
- customer acceptance;
- settlement to the shop;
- reconciled sales;
- revenue recognition;
- profit;
- distributable value; or
- financial return.

Manual payment confirmation should identify:

- operator;
- reason;
- evidence reference;
- time;
- amount;
- payment method;
- reconciliation status; and
- correction path.

Refunds should identify:

- order;
- payment reference;
- amount;
- reason;
- approver;
- provider or cash route;
- status;
- settlement effect; and
- completion time.

Stablecoins, where supported, remain operational payment or settlement rails.

They do not turn Platform Credits into FUZE token and do not create token, participation, payout, or investment rights.

## Stock and Availability

The stock area may track selected:

- products;
- ingredients;
- packaging;
- supplies;
- prepared items;
- waste;
- adjustments; and
- purchase needs.

Operators may use ShopOS AI to:

- record counts;
- compare expected and entered quantities;
- identify low-stock exceptions;
- connect unavailable ingredients to affected menu items;
- prepare purchase lists;
- prepare count checklists;
- record waste or adjustment notes;
- review unusual changes; and
- compare approved records with spreadsheet exports.

ShopOS AI does not establish physical stock by itself.

Counts and adjustments require:

- operator input;
- approved connected source;
- device event; or
- another authorized record.

Stock status should distinguish:

- expected quantity;
- entered count;
- physical count;
- reserved quantity;
- unavailable quantity;
- waste;
- adjustment;
- unresolved difference; and
- last review time.

A stock discrepancy should not automatically be interpreted as staff misconduct, loss, or fraud.

It is an exception requiring review.

## Staff Tasks and Handover

Role-based checklists may support:

- opening;
- preparation;
- service;
- cleaning;
- stock count;
- cash or payment review;
- device checks;
- shift handover;
- incident review; and
- closing.

A task may include:

- title;
- description;
- owner;
- role;
- due stage;
- checklist items;
- evidence requirement;
- completion status;
- exception note;
- reviewer; and
- correction.

Task completion records support operational review but do not automatically establish employment performance, compliance, or disciplinary conclusions.

Training material for recurring work may be prepared through [TrainLayer AI](06-HERHELP_TRAINLAYER_AI_PUBLIC.md) when the shop authorizes the handoff.

## Loyalty and Customer Profiles

ShopOS AI may support simple, permissioned loyalty or promotion workflows.

Possible functions include:

- visit or order count;
- stamps;
- points;
- offer eligibility;
- birthday offer;
- redemption status;
- campaign participation;
- reorder history; and
- customer preference where authorized.

A customer profile should collect the minimum information needed for the selected program.

Possible profile fields include:

- customer reference;
- name where needed;
- phone or communication identifier;
- consent or permission state;
- birth month or date where justified;
- loyalty status;
- selected preferences;
- order references; and
- support history.

A birth date, phone number, order history, wallet address, preference, or loyalty record is personal data.

It should not become a general staff directory or public profile.

Loyalty terms should identify:

- earning rule;
- redemption rule;
- expiry where applicable;
- exclusions;
- correction process;
- dispute route; and
- program status.

Shop loyalty points or stamps are separate from:

- Platform Credits;
- FUZE token;
- stablecoins;
- wallets;
- token utility;
- participation; and
- investment rights.

## Delivery Operations

For supported delivery channels, ShopOS AI may coordinate:

- delivery method;
- order preparation;
- packaging checklist;
- customer address;
- customer contact;
- delivery notes;
- pickup time;
- driver or partner reference;
- handoff status;
- issue note;
- customer-message draft; and
- completion or dispute state.

Delivery details should be visible only to roles that require them.

External delivery services remain responsible for their own:

- platform;
- driver controls;
- routing;
- pricing;
- service availability;
- customer terms;
- location tracking;
- dispute process; and
- fulfillment records.

A delivery-platform status should not be treated as final without the shop's own fulfillment and issue records where relevant.

## Customer Communication

ShopOS AI may help prepare:

- item descriptions;
- availability announcements;
- queue messages;
- pickup messages;
- delivery updates;
- birthday offers;
- promotional content;
- service replies;
- complaint-response drafts;
- closure notices; and
- issue follow-up.

Messages should be reviewed for:

- price;
- availability;
- offer eligibility;
- customer identity;
- language;
- tone;
- timing;
- destination;
- legal or product claims; and
- privacy.

[SpeakShop AI](05-HERHELP_SPEAKSHOP_AI_PUBLIC.md) provides the dedicated workflow for promotional scripts, announcements, and voice content.

ShopOS AI should pass only the approved shop context required for that task.

## Devices, Sessions, and Public Displays

Device records may include:

- device identifier;
- device type;
- workspace;
- assigned role;
- current session;
- allowed functions;
- connection status;
- last activity;
- print or display destination;
- revocation state; and
- incident status.

Public displays should avoid exposing:

- full customer name;
- phone number;
- payment details;
- delivery address;
- loyalty profile;
- private order notes;
- staff-only comments; or
- internal exception reasons.

A lost or compromised device should support:

- session revocation;
- device removal;
- password or credential change;
- review of recent actions;
- correction of unauthorized changes; and
- incident logging.

## TrustCheck

TrustCheck is the ShopOS AI review area for operating quality, control gaps, and exception follow-up where that function is available.

TrustCheck organizes evidence rather than issuing an unconditional trust score.

Possible inputs include:

- unresolved order issues;
- repeated stock adjustments;
- checklist exceptions;
- payment and refund mismatches;
- customer feedback categories;
- cancellation patterns;
- unusual availability changes;
- item-information review;
- device incidents;
- manager confirmations;
- correction records; and
- follow-up actions.

A TrustCheck review should identify:

- issue category;
- source record;
- period;
- severity or priority;
- responsible role;
- review status;
- corrective action;
- completion evidence; and
- current state.

TrustCheck should not automatically infer:

- theft;
- fraud;
- staff dishonesty;
- customer misconduct;
- legal violation;
- accounting fraud; or
- business reliability.

Those conclusions require appropriate evidence and human review.

A public-facing trust or quality statement should use approved, scoped, and public-safe information.

It should not expose customers, staff, suppliers, payment details, security methods, or confidential operations.

## Connected Workflows

ShopOS AI may connect to other HerHelp products where the shop authorizes the handoff.

Possible connections include:

- [SheetLayer AI](03-HERHELP_SHEETLAYER_AI_PUBLIC.md) for reviewed menu, stock, sales, supplier, task, or report imports and exports;
- [SpeakShop AI](05-HERHELP_SPEAKSHOP_AI_PUBLIC.md) for approved announcements, promotions, scripts, and voice outputs;
- [TrainLayer AI](06-HERHELP_TRAINLAYER_AI_PUBLIC.md) for staff onboarding, checklists, and process training;
- [CommunityLayer AI](07-HERHELP_COMMUNITYLAYER_AI_PUBLIC.md) for a separately authorized customer, member, volunteer, or local community; and
- FUZE reporting rails for reviewed operational summaries.

A connected task should receive only the fields required for its purpose.

It should not transfer unrelated:

- customer records;
- staff records;
- payment data;
- supplier terms;
- delivery addresses;
- loyalty history;
- private notes;
- credentials;
- wallet-to-person mappings; or
- security information.

A handoff should identify:

- source product;
- destination product;
- selected fields;
- purpose;
- review status;
- version;
- destination permission; and
- correction route.

## AI Role and Human Authority

AI may assist with:

- menu descriptions;
- category organization;
- translations or language variants;
- promotional drafts;
- staff checklist preparation;
- stock-exception summaries;
- customer-reply drafts;
- delivery-issue summaries;
- daily-report drafts;
- TrustCheck summaries;
- anomaly candidates; and
- operational prioritization.

AI does not automatically:

- set prices;
- approve ingredients or allergens;
- confirm physical stock;
- confirm payment;
- issue refunds;
- make employment decisions;
- make disciplinary decisions;
- publish promotions;
- contact customers;
- approve public claims;
- determine tax or accounting treatment;
- determine food safety;
- determine legal compliance; or
- override shop authority.

Review strength should match impact.

| Output or action | Typical review |
|---|---|
| Internal description draft | Authorized staff review |
| Public menu copy | Owner, manager, or publisher review |
| Price or option change | Authorized owner or manager approval |
| Stock adjustment | Stock or manager review |
| Customer reply | Customer-service or manager review |
| Refund suggestion | Authorized manager or finance approval |
| Loyalty correction | Authorized manager review |
| Staff checklist | Manager or process-owner review |
| TrustCheck finding | Human investigation and evidence review |
| Accounting, tax, payroll, or legal conclusion | Appropriate specialist review |

## Platform Credit Use

Metered AI and reporting functions may use Platform Credits.

Examples include:

- drafting menu descriptions;
- preparing language variants;
- generating promotional content;
- creating staff checklists;
- summarizing a shift;
- organizing stock exceptions;
- preparing a customer-reply draft;
- reviewing delivery notes;
- preparing a TrustCheck summary;
- creating an owner report;
- comparing menu or stock versions; or
- generating a public-safe operating summary.

Routine operational functions may follow a different access model.

The product should identify which action consumes Platform Credits before the operator confirms it.

A usage screen should show, where applicable:

- task;
- product function;
- usage unit;
- fixed amount, estimate, range, or maximum;
- available balance;
- authorization;
- reservation status;
- completion condition;
- partial-completion treatment;
- failure or reversal treatment; and
- final record.

A standard lifecycle may be:

```text
quote -> authorize -> reserve if needed -> process
-> complete, partially complete, fail, or cancel
-> consume, release, reverse, or correct -> record
```

Platform Credits are product usage credits.

They are separate from:

- customer loyalty points or stamps;
- stablecoins;
- FUZE token;
- wallets;
- token allocation;
- wallet-based participation;
- claims;
- payouts;
- market access; and
- investment rights.

## Data and Permission Controls

ShopOS AI may process several categories of operational data.

| Data area | Examples | Main control concern |
|---|---|---|
| Customer | Contact, order history, loyalty, preferences, support | Purpose limitation, consent or permission, staff visibility, retention |
| Staff | Roles, schedules, tasks, access, notes | Employment privacy, role separation, management authority |
| Payment | Status, reference, refund, dispute, settlement | Provider authority, reconciliation, restricted visibility |
| Delivery | Address, contact, order, handoff | Need-to-know access and retention |
| Commercial | Prices, costs, suppliers, stock, sales | Confidentiality, accuracy, business authority |
| Devices | Sessions, connections, print, display, access | Revocation, physical security, incident response |
| Loyalty | Visit, stamp, point, offer, redemption | Program terms, correction, customer privacy |
| TrustCheck | Exceptions, investigations, corrective actions | Evidence quality, fairness, restricted access |

Controls may include:

- role permissions;
- workspace separation;
- device authorization;
- restricted fields;
- purpose-specific access;
- approval steps;
- retention settings;
- export controls;
- connection revocation;
- public-display restrictions;
- activity records;
- correction history;
- provider-routing restrictions; and
- incident handling.

Public queue displays should use a suitable service reference rather than full customer identity.

Public reports should use aggregated, redacted, range-based, delayed, or otherwise public-safe information.

Wallet addresses, where used for a specifically supported payment or mechanism, should not be used to reveal private identity or create unsupported financial conclusions.

The [FUZE Data Privacy and AI Data Handling](../CORE-PLATFORM-PAPERS/07-FUZE_DATA_PRIVACY_AND_AI_DATA_HANDLING_PUBLIC.md) provides the wider model.

## Reporting

An owner, shift, or period report may include:

- orders by status;
- order channel;
- recorded sales activity;
- payment status;
- refund and cancellation records;
- popular or unavailable items;
- queue time and service exceptions;
- stock warnings and adjustments;
- staff checklist completion;
- delivery issues;
- loyalty or campaign activity;
- Platform Credit usage;
- TrustCheck exceptions;
- unresolved tasks;
- device incidents; and
- correction history.

Each report should identify:

- workspace or location;
- source period;
- timezone;
- included channels;
- excluded channels;
- payment source;
- fulfillment source;
- data freshness;
- unresolved reconciliation;
- metric definitions; and
- current version.

Reports should distinguish:

- orders created;
- orders confirmed;
- payments confirmed;
- orders fulfilled;
- orders refunded;
- recorded sales activity;
- reconciled settlement;
- accounting revenue; and
- profit.

Recorded sales activity should not be presented as audited revenue.

A payment-provider status should be reconciled against the shop's applicable business record.

A high order count does not independently prove adoption, retention, profitability, or sustainable revenue.

Reporting should follow the [FUZE Transparency and Reporting Rails](../CORE-PLATFORM-PAPERS/09-FUZE_TRANSPARENCY_AND_REPORTING_RAILS_PUBLIC.md).

## End-of-Day Review

An end-of-day or shift-close process may include:

1. review open orders;
2. resolve cancelled, delayed, or partially fulfilled orders;
3. review payment mismatches;
4. review refunds and disputes;
5. review cash or provider totals where applicable;
6. review unavailable items and stock exceptions;
7. complete closing tasks;
8. review device sessions;
9. record incidents;
10. review unresolved customer or delivery issues;
11. generate the owner summary; and
12. preserve correction and handover notes.

Closing a shift does not automatically confirm accounting accuracy.

Material differences should remain visible until reconciled or corrected.

## Error, Correction, and Support Model

ShopOS AI should support clear treatment for:

- duplicate order;
- wrong item or option;
- wrong price;
- unavailable item;
- payment mismatch;
- failed payment;
- manual payment error;
- queue error;
- missing preparation item;
- incorrect handoff;
- delivery failure;
- stock mismatch;
- loyalty correction;
- unauthorized refund;
- device loss or compromise;
- incorrect customer communication;
- incorrect TrustCheck finding;
- Platform Credit mismatch;
- failed export or integration; and
- missing history.

A correction record should identify:

- original record;
- affected order, payment, stock, loyalty, task, or report;
- correction reason;
- responsible reviewer;
- corrected state;
- customer or staff impact where relevant;
- settlement or reconciliation effect;
- downstream report effect; and
- support status.

A corrected order, payment, stock, loyalty, or report record should not silently overwrite the previous approved state without history.

## Product Status and Evidence

This paper defines the approved public product model.

It does not independently prove that ShopOS AI currently has:

- live QR ordering;
- live checkout;
- production payment integrations;
- stablecoin payment support;
- queue displays;
- preparation screens;
- stock synchronization;
- device integrations;
- loyalty functions;
- delivery integrations;
- TrustCheck;
- paid customers;
- active shop adoption; or
- confirmed revenue.

Different functions may reach different stages.

Possible evidence includes:

| Status claim | Evidence direction |
|---|---|
| Product designed | Defined users, operating areas, workflows, data, roles, controls, and boundary |
| Prototype exists | Reviewable menu, order, queue, checkout, stock, staff, loyalty, or report workflow |
| Internally tested | Tests for normal, duplicate, payment, refund, queue, permission, device, and correction paths |
| Limited shop pilot | Controlled location, real staff, current terms, support, monitoring, and known limitations |
| Public beta | Public access route, supported functions, beta terms, support, and release notes |
| Live | Production access, current functions, support, monitoring, and operating evidence |
| Paid delivery | Pricing, payment, active service, fulfillment, support, and customer evidence |
| Revenue confirmed | Reconciled payment, completed service, accounting treatment, period, and review |

The following do not independently prove a live product:

- a public paper;
- a QR menu mockup;
- a screenshot;
- a menu file;
- a prototype queue;
- code;
- a repository;
- a demonstration;
- a pricing concept; or
- a roadmap date.

Current status should be checked in the [FUZE Public Status and Roadmap Matrix](../PUBLIC-INDEX/02-FUZE_PUBLIC_STATUS_AND_ROADMAP_MATRIX.md).

## Product and Token Separation

ShopOS AI performs a shop-operating role.

Customer use of menu, ordering, queue, payment, loyalty, delivery, or support functions does not require token or wallet participation to explain the product purpose.

The following remain separate:

- shop operations;
- customer loyalty points or stamps;
- Platform Credits;
- payments;
- stablecoins;
- wallets;
- FUZE token utility;
- token participation;
- claims;
- payouts; and
- market access.

A payment, customer profile, loyalty record, wallet link, token balance, or Platform Credit event does not automatically establish:

- active token utility;
- wallet eligibility;
- approved distributable value;
- a claim;
- token circulation;
- DEX liquidity;
- CEX access;
- token demand;
- price support; or
- financial return.

Any product-to-token utility must be separately defined, implemented, authorized, activated, and reported under the relevant specialist papers.

## Public Boundary

ShopOS AI can assist with shop setup, menus, orders, queues, stock, staff tasks, loyalty, delivery, communication, exception review, and reporting.

It cannot independently establish:

- accurate physical stock;
- payment settlement;
- accounting accuracy;
- tax treatment;
- food safety;
- allergen compliance;
- lawful employment practice;
- delivery completion;
- customer consent;
- promotion legality;
- regulatory compliance;
- staff misconduct;
- business trustworthiness;
- audited revenue;
- profitability;
- token rights;
- wallet eligibility;
- listing;
- liquidity;
- price support; or
- financial return.

Owners and authorized operators remain responsible for:

- accurate prices and product information;
- ingredient and allergen review;
- physical stock;
- order fulfillment;
- payment reconciliation;
- refunds;
- accounting and tax;
- lawful customer communication;
- staff management;
- device security;
- delivery oversight;
- data protection;
- public claims; and
- compliance with applicable rules.

Detailed product risks appear in [FUZE Product Risk Boundaries](16-FUZE_PRODUCT_RISK_BOUNDARIES_PUBLIC.md). Consolidated limitations appear in the [FUZE Risk and Disclosure Appendix](../WHITEPAPER-PAPERS/05-FUZE_RISK_AND_DISCLOSURE_APPENDIX_PUBLIC.md).

## Key Takeaways

- ShopOS AI is designed around the real operating day of a small shop or local service business.
- A shop can begin with a limited configuration and add supported functions when operationally ready.
- Menu, order, queue, payment, fulfillment, stock, staff, loyalty, delivery, device, and TrustCheck records remain distinct.
- Payment confirmation, fulfillment, settlement, revenue, and profit are different states.
- Physical stock and real-world service remain operator responsibilities.
- TrustCheck organizes evidence and exceptions; it does not automatically produce a trust score or misconduct conclusion.
- Platform Credits meter defined AI and reporting services and remain separate from loyalty points, stablecoins, wallets, and FUZE token.
- Customer, staff, payment, delivery, supplier, and device data require purpose-based access and public-safe reporting.
- This paper does not prove implementation, live release, adoption, paid delivery, or revenue.
- ShopOS AI succeeds only when it reduces real operational friction without weakening owner control, staff accountability, customer privacy, or financial discipline.
