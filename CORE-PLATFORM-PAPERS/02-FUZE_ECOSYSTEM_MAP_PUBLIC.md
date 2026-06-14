# FUZE Ecosystem Map

## Executive Summary

The FUZE ecosystem connects people who need practical software, distinct product families, shared platform capabilities, and controlled Web3 participation. This paper maps those relationships so readers can see where an activity begins, which layer supports it, and where its records or controls belong.

The map separates four flows that are often confused: product usage, operational payments, public-safe records, and ecosystem utility. Those flows can meet within the same platform without becoming the same instrument or user experience.

Use this paper when evaluating scope and dependencies across FUZE. Individual product, platform-rail, tokenomics, status, and risk papers remain the sources for implementation detail.

---

## 1. Ecosystem at a Glance

```text
PEOPLE AND ORGANIZATIONS
Individuals | Shops | SMEs | Teams | Communities | Players | Events | Partners
                                  |
                                  v
PRODUCT EXPERIENCES
HerHelp family | ZAGA games | QTB and AIMM | AIE | ToolGrid AI | Botmad
                                  |
                                  v
SHARED PLATFORM CAPABILITIES
Access | Usage | Payments | AI | Data | Permissions | Wallet records | Reporting
                                  |
                    +-------------+-------------+
                    |                           |
                    v                           v
OPERATIONS AND EVIDENCE                 ECOSYSTEM MECHANISMS
Support | Monitoring | Reports          FUZE token utility | Governance
Reconciliation | Status | Audit         Activation-gated participation
                    |                           |
                    +-------------+-------------+
                                  v
GOVERNANCE, PRIVACY, AND RISK CONTROLS
```

The arrows describe dependencies, not a requirement that every participant use every layer. A shop customer may interact only with a product checkout. A product operator may use identity, reporting, and payment services. A tokenomics reviewer may follow wallet, governance, and evidence records across several specialist papers.

---

## 2. Participant Groups

FUZE serves an ecosystem rather than a single user profile.

| Group | Primary interaction | What can connect them further |
|---|---|---|
| Consumers and individual users | A product feature, game, utility, or AI workflow | Account history, credits, reports, or relevant ecosystem access |
| Shops and SMEs | Operations, customer service, content, data, training, and payments | Multi-product workflows and consolidated controls |
| Teams and enterprises | Permissioned workspaces, reporting, integrations, and governance | Shared services across business units or partner deployments |
| Communities | Moderation, support, verification, games, events, and communication | Community records, roles, campaigns, and selected Web3 functions |
| Players | ZAGA Arena or ZAGA Districts | Profiles, progression, community activity, and defined utility |
| Event organizers | Planning, information, participants, partners, and outcomes | AIE workflows, community tools, reports, and integrations |
| Strategic partners | Distribution, technology, content, enterprise, event, game, or Web3 collaboration | Qualified integrations and lifecycle governance |
| Contributors and operators | Product development, service delivery, support, treasury, or governance work | Role-based systems, evidence, approvals, and compensation operations |

These groups can overlap. A community may also be a partner; a shop owner may use training and spreadsheet products; a player may join wider ecosystem activity. Permissions and product context determine which relationship is active.

---

## 3. Product Experience Layer

The product layer is organized by user job rather than by infrastructure.

### HerHelp Family

HerHelp covers practical AI SaaS workflows. SheetLayer AI handles spreadsheet and business-data work. ShopOS AI supports shop operations. SpeakShop AI creates promotional voice and announcement material. TrainLayer AI supports learning and onboarding. CommunityLayer AI assists with community operations.

### ZAGA

ZAGA provides the game and token-utility context. ZAGA Arena is the fast battle-arena product, while ZAGA Districts develops the Telegram-native cyberpunk MMORPG experience. Their gameplay and community models remain separate even when they use common platform services.

### Specialized Products

QTB organizes market interpretation and research workflows. AIMM supports liquidity-operations monitoring and reporting. AIE serves event-intelligence workflows. ToolGrid AI combines utility discovery with clearly identified sponsored visibility. Botmad provides permission-controlled AI work assistance.

The [FUZE AI SaaS Product Index](../AI-SAAS-PRODUCT-PAPERS/01-FUZE_AI_SAAS_PRODUCT_INDEX_PUBLIC.md) links to the dedicated explanation for each product.

---

## 4. Shared Capability Layer

Products can draw on a common service foundation according to their needs.

| Shared area | Receives | Produces |
|---|---|---|
| Identity and access | Account, workspace, role, device, or approved wallet context | Session and access decisions |
| Usage services | Product action and pricing or credit rule | Consumption record and balance update |
| Payment operations | Checkout, settlement, treasury, or compensation instruction | Reconciled payment record |
| AI orchestration | Approved prompt, context, model policy, and task | Output plus review and usage metadata |
| Data controls | Product data and permission state | Governed storage, retrieval, retention, or deletion action |
| Wallet-aware records | Address or transaction context required by a mechanism | Public-safe reference or internal verification record |
| Reporting | Product, operational, financial, or status events | Dashboard, summary, evidence package, or public report |
| Governance | Proposal, configuration change, exception, or release request | Approval, rejection, delay, or controlled execution |

The shared layer reduces duplication in implementation and operations. It also creates consistent interfaces between products and the teams responsible for security, privacy, finance, support, and reporting.

For infrastructure detail, read [FUZE Core Platform Rails](04-FUZE_CORE_PLATFORM_RAILS_PUBLIC.md).

---

## 5. Four Distinct Flows

### 5.1 Product Usage Flow

```text
User action -> product service -> usage decision -> result -> usage record
```

This flow delivers software value. Platform Credits can be consumed for supported actions such as an AI task, report, module, or defined workflow. The product should make the action and consumption understandable to its user.

### 5.2 Operational Value Flow

```text
Payment source -> approved route -> settlement or treasury process -> reconciliation
```

This flow handles commercial or operational value. A product may support card, fiat, stablecoin, marketplace, app, or other routes according to its implementation and region. Stablecoins can serve payment, settlement, treasury, or compensation functions; that classification does not turn them into product credits or FUZE token.

### 5.3 Evidence and Transparency Flow

```text
Product or platform event -> controlled record -> review -> internal or public-safe report
```

Evidence can include product metrics, usage records, approvals, report hashes, wallet references, vault activity, or status changes. The audience and sensitivity determine whether the result stays internal, enters qualified diligence, or becomes public.

Wallet transparency should expose only the record needed for verification. Personal identity and sensitive customer, partner, contributor, financial, security, or legal information remain permissioned.

### 5.4 Ecosystem Utility Flow

```text
Defined ecosystem activity -> utility rule -> FUZE token interaction -> governed record
```

This flow applies only where a product or ecosystem mechanism defines token utility. Governance, circulation, wallet eligibility, or participation mechanics require their own controls and current status. Ordinary product usage and token holding should not be assumed to create the same rights or results.

The [FUZE Tokenomics Overview](../TOKENOMICS-GOVERNANCE-COMPLIANCE-PAPERS/01-FUZE_TOKENOMICS_OVERVIEW_PUBLIC.md) is the entry point for that layer.

---

## 6. Cross-Ecosystem Connections

The following examples show relationships without requiring a single bundled experience.

| Starting point | Possible connection | Shared dependency |
|---|---|---|
| ShopOS AI | Train staff with TrainLayer AI | Roles, content, usage, and reporting |
| SheetLayer AI | Feed approved business data into a report | Data permission, AI orchestration, and evidence |
| CommunityLayer AI | Support a ZAGA community | Moderation, roles, summaries, and game-community records |
| AIE | Coordinate an event partner or community campaign | Participant data, permissions, content, and reporting |
| ToolGrid AI | Surface a sponsored utility | Sponsorship labeling, destination review, and metrics |
| Botmad | Assist work across an approved product workspace | Task scope, credentials, data limits, and human review |
| QTB | Organize research used by an analyst | Data sources, interpretation, watchlists, and reporting |
| AIMM | Monitor market-operations information | Permissions, governance, venue data, and risk controls |

A connection becomes meaningful only when it improves a defined workflow and has clear ownership. Shared branding alone is not an integration.

---

## 7. Control and Accountability Map

Different teams or governance functions are responsible for different parts of the ecosystem.

| Responsibility | Typical scope |
|---|---|
| Product ownership | User problem, feature decisions, workflow quality, support, and product reporting |
| Platform operations | Shared-service availability, integration standards, monitoring, and incident response |
| Data and privacy | Permission design, sensitive-data handling, retention, and disclosure review |
| Finance and treasury | Payment classification, reconciliation, reserves, compensation, and approved records |
| Token and governance | Utility rules, allocations, circulation, contracts, vaults, approvals, and activation |
| Security | Credentials, access, infrastructure, contract, wallet, and incident controls |
| Public reporting | Status, evidence selection, correction, and public-safe presentation |
| Legal and compliance review | Jurisdictional, claim, privacy, market, and document-specific review where required |

Accountability should follow the underlying action. A wallet record does not transfer responsibility for product data to token governance. A product integration does not make a strategic partner responsible for unrelated platform operations.

---

## 8. Reading the Map by Topic

| Topic | Primary route |
|---|---|
| Overall platform experience | [FUZE Platform Overview](01-FUZE_PLATFORM_OVERVIEW_PUBLIC.md) |
| Execution order | [FUZE Product-First Execution Model](03-FUZE_PRODUCT_FIRST_EXECUTION_MODEL_PUBLIC.md) |
| Shared infrastructure | [FUZE Core Platform Rails](04-FUZE_CORE_PLATFORM_RAILS_PUBLIC.md) |
| Credit use | [FUZE Platform Credits Usage Examples](06-FUZE_PLATFORM_CREDITS_USAGE_EXAMPLES_PUBLIC.md) |
| Data and AI handling | [FUZE Data Privacy and AI Data Handling](07-FUZE_DATA_PRIVACY_AND_AI_DATA_HANDLING_PUBLIC.md) |
| Wallet-aware platform records | [FUZE Wallet-Based Platform Model](08-FUZE_WALLET_BASED_PLATFORM_MODEL_PUBLIC.md) |
| Evidence and public reporting | [FUZE Transparency and Reporting Rails](09-FUZE_TRANSPARENCY_AND_REPORTING_RAILS_PUBLIC.md) |
| Current status | [FUZE Public Status and Roadmap Matrix](../PUBLIC-INDEX/02-FUZE_PUBLIC_STATUS_AND_ROADMAP_MATRIX.md) |

---

## 9. Ecosystem Boundaries

This map shows intended relationships, not current activation of every product, integration, payment route, wallet function, or token mechanism. Status must be supported by the relevant implementation or evidence source.

AI output, game activity, sponsored visibility, market interpretation, and operational monitoring do not establish business, financial, adoption, or market outcomes. Wallet records provide a transparency tool without making private identity public.

The [FUZE Risk and Disclosure Appendix](../WHITEPAPER-PAPERS/05-FUZE_RISK_AND_DISCLOSURE_APPENDIX_PUBLIC.md) is the final route for dependencies or limitations that extend beyond one layer of this map.

---

## Conclusion

FUZE can be read as a set of connected but independently accountable layers. People and organizations enter through products. Shared capabilities support those experiences. Operations and evidence make activity reviewable. Ecosystem mechanisms add governed utility where defined.

Keeping product usage, operational value, transparency records, and token utility as separate flows makes the ecosystem easier to build, operate, and understand.
