# HerHelp ShopOS AI

## Executive Summary

ShopOS AI is the HerHelp operating workspace for small shops and local service businesses. It brings menu or catalog setup, order handling, queues, checkout records, stock review, staff tasks, customer communication, delivery notes, loyalty activity, and daily reporting into one practical workflow.

The product is intended for operators who currently coordinate work through paper, chat, spreadsheets, payment applications, and staff memory. A shop can begin with a limited setup, such as a QR menu and queue, then add other supported functions as its operating needs develop.

ShopOS AI assists owners and staff with preparation, coordination, and review. It does not replace operator approval, payment-provider controls, accounting records, food-safety practice, employment responsibilities, or other obligations that apply to the business.

---

## 1. Product Purpose

Small shops need software that fits the pace of the counter. A system that requires extensive setup or specialist administration can create more work than it removes.

ShopOS AI is designed to give an owner a clear daily operating view:

- what can be sold;
- which orders are active;
- where each order is in the queue;
- whether payment status has been recorded;
- which stock items need attention;
- what staff must complete;
- which delivery or customer issues are open; and
- what the owner should review at the end of the day.

The product can support food stalls, cafes, market vendors, small restaurants, service counters, pop-up booths, local retailers, and other owner-operated businesses. Available features and integrations depend on the configured release and the shop's operating context.

---

## 2. Core Operating Areas

| Area | ShopOS AI role |
|---|---|
| Menu or catalog | Maintain items, categories, prices, descriptions, options, and availability |
| Orders | Capture selected items, quantities, notes, and progress status |
| Queue | Assign and display an order sequence or service position |
| Checkout | Present totals and retain approved payment-status records |
| Stock | Review products, ingredients, supplies, and low-stock exceptions |
| Staff | Organize opening, service, handover, and closing work |
| Loyalty | Support permissioned customer offers and repeat-visit activity |
| Delivery | Coordinate preparation, handoff, status, and issue notes |
| Communication | Prepare menu copy, announcements, replies, and promotions |
| Reports | Summarize sales activity, operations, exceptions, and usage |

These areas can operate together, but a shop does not need to activate every one. The initial configuration should match the operator's actual workflow.

---

## 3. Shop Setup

### 3.1 Business workspace

The owner creates a workspace for a location, stall, booth, or service point. Access can be separated for owners, managers, counter staff, preparation staff, and approved support partners.

### 3.2 Menu or catalog

The operator can enter or import items with fields such as:

- item name and category;
- price and option choices;
- customer-facing description;
- availability;
- preparation or service notes;
- image where supported; and
- linked stock information.

AI assistance may help draft descriptions, organize categories, or prepare language variants. The shop reviews pricing, ingredients, claims, and availability before publication.

### 3.3 Service flow

The shop defines the statuses used during service, such as received, confirmed, preparing, ready, completed, or cancelled. A service business may use appointment or counter stages instead of food-order stages.

### 3.4 Devices and displays

A basic setup may use a phone and printed QR code. Depending on available support, a shop may later add a tablet, customer display, preparation screen, printer, label device, monitor, or speaker.

Device connections should be tested for the operating environment. Hardware availability and compatibility are configuration matters rather than universal product promises.

---

## 4. Customer and Order Journey

### Step 1: View available items

A customer can open a supported QR menu, catalog, or staff-assisted order surface. The displayed information should reflect the latest approved item and availability data.

### Step 2: Create the order

The order records selected items, quantities, options, and necessary notes. The shop should avoid collecting customer information that is unrelated to fulfillment.

### Step 3: Confirm checkout

ShopOS AI can present an order total and record status received from an approved payment or checkout process. Payment methods may include conventional rails and, where specifically supported, an approved stablecoin payment path.

The underlying payment provider remains responsible for its own authorization and settlement functions. ShopOS AI should not mark payment as successful without the relevant confirmation or operator action.

### Step 4: Assign service position

The system can provide a queue number or other service reference. Staff can move the order through the configured stages, while customer displays or announcements use only the information appropriate for public presentation.

### Step 5: Prepare and hand off

Preparation notes, station tasks, packing checks, or service instructions can accompany the order. Staff confirm completion before the item is collected, delivered, or closed.

### Step 6: Record exceptions

Cancelled items, refunds, delays, substitutions, complaints, or other exceptions can be recorded for manager review. Sensitive customer or payment details should remain restricted.

---

## 5. Daily Shop Operations

### Queue and service status

ShopOS AI can organize active work by order stage, station, or priority. A queue view may show service references, elapsed time, and current status without revealing unnecessary customer identity.

AI can help prepare announcement wording, but the shop determines the language, timing, and suitability for its customers and location.

### Stock and availability

The stock area can track selected products, ingredients, packaging, or supplies. Operators may use it to:

- review quantities entered by staff;
- identify low-stock exceptions;
- link an unavailable ingredient to affected menu items;
- prepare a purchase or count checklist;
- record waste or adjustment notes where supported; and
- compare approved shop records with a spreadsheet export.

ShopOS AI does not establish physical stock by itself. Counts and adjustments require operator input or an authorized connected source.

### Staff tasks

Role-based checklists can support opening, preparation, service, cleaning, handover, and closing. Managers can assign an owner and due stage to a task, then review completion or exceptions.

Training material for recurring processes can be prepared through [TrainLayer AI](./06-HERHELP_TRAINLAYER_AI_PUBLIC.md) when the shop authorizes that handoff.

### Delivery work

For supported delivery channels, the workspace can consolidate preparation notes, status, packaging checks, handoff information, and customer-message drafts. Delivery addresses and contact details should be visible only to roles that require them.

An external delivery service remains responsible for its own platform, driver, and fulfillment controls.

---

## 6. Loyalty and Customer Communication

ShopOS AI may support simple loyalty or promotion workflows based on the shop's configuration and customer permission. These can include visit records, offer eligibility, birthday campaigns, or redemption status.

Customer profiles should collect the minimum information needed for the selected program. A birth date, phone number, order history, or preference is personal data and should not become a general staff directory.

The communication workspace can help prepare:

- promotional copy;
- item announcements;
- queue or pickup messages;
- service replies;
- birthday offers;
- delivery updates; and
- issue-response drafts.

[SpeakShop AI](./05-HERHELP_SPEAKSHOP_AI_PUBLIC.md) provides the dedicated workflow for promotional scripts and announcement content. ShopOS AI supplies only the approved shop context needed for that task.

Messages should be reviewed for price, availability, eligibility, language, and destination before use.

---

## 7. TrustCheck

TrustCheck is the ShopOS AI review area for operating quality and exception follow-up where that function is available. It can organize evidence rather than issue an unconditional trust score.

Relevant records may include:

- unresolved order issues;
- repeated stock adjustments;
- checklist exceptions;
- customer feedback categories;
- refund or cancellation patterns;
- item-information review;
- manager confirmations; and
- corrective actions.

Access should reflect the sensitivity of the underlying records. A public-facing quality statement should be supported by approved, appropriately scoped information and should not expose customers, staff, or confidential shop operations.

---

## 8. Connected Workflows

ShopOS AI is one module within [HerHelp AI SaaS](./02-HERHELP_AI_SAAS_PUBLIC.md). Connections are intended to reduce duplicate preparation while maintaining product-specific permissions.

Examples include:

- [SheetLayer AI](./03-HERHELP_SHEETLAYER_AI_PUBLIC.md) for reviewed menu, stock, sales, or task imports and exports;
- SpeakShop AI for approved customer-facing announcements;
- TrainLayer AI for staff onboarding and process material;
- CommunityLayer AI for a separately authorized local or member community; and
- FUZE reporting rails for suitable operating evidence.

A connected task should receive only the fields necessary for its purpose. Customer, staff, payment, and supplier records should not be copied into unrelated modules.

---

## 9. Platform Credit Use

Metered AI and reporting functions in ShopOS AI may use Platform Credits. Examples can include:

- drafting menu descriptions or translations;
- preparing a promotional message;
- generating a staff checklist;
- summarizing a service period;
- organizing stock exceptions;
- producing a customer-reply draft;
- reviewing delivery issue notes;
- preparing a TrustCheck summary; or
- creating an owner report.

Routine order or shop functions may follow a different product-access model. The usage screen should identify which action consumes credits and the applicable basis before the operator confirms it.

Platform Credits account for product activity; they are separate from the FUZE token and are not a customer loyalty point or payment currency.

---

## 10. Data and Permission Controls

ShopOS AI can process several categories of operational data:

| Data area | Control concern |
|---|---|
| Customer | Contact details, order history, loyalty eligibility, and preferences |
| Staff | Roles, schedules, tasks, performance notes, and access |
| Payment | Status, reference, refund, and reconciliation information |
| Delivery | Address, contact, order, and handoff details |
| Commercial | Pricing, sales, suppliers, costs, and stock |
| Devices | Session, connection, print, display, and access records |

Controls may include role permissions, workspace separation, device authorization, restricted fields, approval steps, retention settings, export controls, and connection revocation.

Public queue displays should use a suitable service reference rather than a full customer identity. Public reporting should rely on aggregated or non-identifying information. Further principles appear in [FUZE Data, Privacy and AI Data Handling](../CORE-PLATFORM-PAPERS/07-FUZE_DATA_PRIVACY_AND_AI_DATA_HANDLING_PUBLIC.md).

---

## 11. Reporting

An owner report can combine the operational information needed to review a shift or period, such as:

- orders by status;
- recorded sales activity;
- popular or unavailable items;
- queue and service exceptions;
- stock warnings and adjustments;
- staff checklist completion;
- delivery issues;
- loyalty or campaign activity;
- refunds or cancellations;
- Platform Credit usage; and
- follow-up tasks.

Each report should identify its source period and any excluded channels. Recorded sales activity should not be presented as audited revenue, and payment status should be reconciled against the applicable provider or business record.

Where a shop continues to use spreadsheets, approved exports and comparisons can be handled through SheetLayer AI without giving every spreadsheet user access to the live ShopOS workspace.

---

## 12. Product Status and Boundary

ShopOS AI is presented as a developing product. QR menu, order, queue, checkout, loyalty, stock, staff, delivery, TrustCheck, device, payment, and integration functions may reach availability at different stages.

The product supports shop coordination and AI-assisted preparation. Owners remain responsible for accurate prices and item information, lawful customer communication, staff management, physical stock, payment reconciliation, accounting, tax, safety, and regulatory requirements.

Customer use of the shop surface does not require participation in FUZE token or wallet programs. Any separate ecosystem mechanism is governed by its own activation and disclosure materials.

---

## 13. Conclusion

ShopOS AI gives a small operator one place to coordinate the working day, from menu availability and orders through staff tasks, stock exceptions, customer communication, and owner review.

Its value depends on practical adoption at the counter: clear roles, limited setup, reliable records, reviewed AI outputs, and tools that match the shop's actual operating needs.
