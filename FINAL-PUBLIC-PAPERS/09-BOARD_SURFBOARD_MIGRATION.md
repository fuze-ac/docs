# FILE NAME: 09-BOARD_SURFBOARD_MIGRATION-PUBLIC.md

# BOARD / Surfboard Migration

## Executive Summary

FUZE uses the **BOARD / Surfboard Migration** allocation to protect legacy-holder continuity while keeping FUZE v2 fair for new participants, investors, product users, and future community members.

The migration allocation is **25,000,000 FUZE**, equal to **5.00%** of the fixed **500,000,000 FUZE** total supply. This allocation is reserved for eligible legacy-holder migration. It is not public sale inventory, not treasury inventory, not liquidity inventory, and not team or advisor compensation inventory.

FUZE handles legacy-holder migration through a fair, transparent, claim-based process. Eligible legacy holders claim FUZE through a dedicated migration contract using a finalized snapshot or eligibility registry. The claim process includes eligibility rules, a defined claim window, a staged or vested claim model, and a transparent unclaimed-token policy.

The migration model supports FUZE v2’s Controlled Circulation Policy by preserving legacy continuity without creating unnecessary immediate sell pressure.

## 1. FUZE Position

FUZE reserves **25,000,000 FUZE** for BOARD / Surfboard Migration.

FUZE public rule:

**Migration tokens are claim-based for eligible legacy holders, not public sale inventory.**

FUZE uses **BOARD / Surfboard Migration** as the transitional public name until final naming is formally locked.

Possible naming by context:

| Context | Public Term |
|---|---|
| Tokenomics table | BOARD / Surfboard Migration |
| Community update | Surfboard Holder Migration |
| Technical contract | `FuzeBoardMigrationClaim`, `FuzeSurfboardMigrationClaim`, or `FuzeLegacyMigrationClaim` |
| Investor materials | Legacy-holder migration allocation |
| Legal/compliance review | Legacy migration allocation |

Public explanation:

**The BOARD / Surfboard Migration allocation is reserved for eligible legacy holders. It is not a public sale bucket and not a general treasury allocation.**

The migration process uses:

- finalized eligibility rules
- snapshot or eligibility registry
- dedicated claim contract
- claim window
- duplicate-claim prevention
- optional staged claim or vesting
- public status reporting
- unclaimed-token policy
- legal, compliance, and technical review

## 2. Platform Context

FUZE is a transparency-first AI SaaS platform building practical products on top of shared infrastructure for identity, credits, payments, AI orchestration, reporting, and ecosystem participation.

FUZE execution order is:

**Product usage first. Platform rails second. Broader ecosystem participation after that.**

The BOARD / Surfboard Migration allocation fits this model because FUZE maintains continuity with earlier community history while moving into FUZE v2’s product-first, platform-led, compliance-aware direction.

FUZE v2 launch focus is **HerHelp.com** and **ZAGA.io**, supported by FUZE Core Platform rails and accelerated internally by **Botmad**.

The migration model connects to FUZE platform layers in the following way:

| Platform Area | Migration Relationship |
|---|---|
| FUZE Core Platform | Provides identity, wallet, eligibility, reporting, claim, and transparency rails |
| FUZE token | Ecosystem participation asset used for eligible legacy-holder continuity |
| Platform Credits | Product usage asset, separate from migration allocation |
| Public Vault Access System | Separate system; migration tokens are not public vault sale inventory |
| Controlled Circulation Policy | Supports staged or vested claims to reduce immediate supply pressure |
| Vault-by-Vault Release Rules | Classifies migration allocation as claim-based, not public sale inventory |
| Transparency dashboard | Reports total allocation, claim status, unclaimed amount, policy hash, and contract reference |
| Governance direction | Supports snapshot discipline, claim rules, unclaimed-token policy, and public reporting |
| Compliance posture | Keeps eligibility, jurisdiction, claim design, and communication boundaries reviewed |

FUZE token is for ecosystem participation. Platform Credits are for product usage. Stablecoin compensation is for work payment. Profit participation is a long-term design direction, not an immediate or guaranteed promise.

## 3. Public Model

### 3.1 Migration Allocation

| Item | Value |
|---|---:|
| Allocation | BOARD / Surfboard Migration |
| Amount | 25,000,000 FUZE |
| % of total FUZE supply | 5.00% |
| Purpose | Legacy-holder migration continuity |
| Release model | Claim-based migration |
| Public buy access | No |
| Treasury use | No |
| Liquidity use | No |
| Team/advisor use | No |

### 3.2 Eligibility Model

Eligibility is finalized before migration opens.

Eligibility sources include:

| Eligibility Source | Description | Notes |
|---|---|---|
| Token holder snapshot | Wallets holding eligible BOARD / Surfboard token at snapshot block or time | Transparent and verifiable |
| Contract participant records | Wallets that participated in legacy contract or sale | Useful where legacy contract data exists |
| Manual verified claims | Users submit proof for review | Flexible but more operationally intensive |
| Hybrid model | Snapshot plus review path for exceptions | Useful where legacy records are incomplete |

FUZE uses a snapshot-based eligibility model where possible, with a limited review process for edge cases.

Eligibility defines:

- eligible token or asset
- snapshot chain
- snapshot block or timestamp
- eligible wallet rules
- excluded wallets
- exchange or custodial wallet handling
- contract wallet handling
- minimum balance threshold, where applicable
- duplicate claim prevention
- claim ratio
- claim deadline
- appeal or review process, where applicable

### 3.3 Snapshot Policy

The snapshot is the foundation of migration fairness.

| Snapshot Field | Public Requirement |
|---|---|
| Snapshot asset | BOARD / Surfboard token or other eligible record |
| Snapshot chain | Chain where the legacy asset exists |
| Snapshot block/time | Exact block number or timestamp |
| Excluded wallets | Team, treasury, LP, burn, contract-owned, suspicious wallets where applicable |
| Holder balance source | On-chain balance, contract record, or verified registry |
| Duplicate protection | One wallet / one claim or balance-based claim |
| Custodial handling | Clear treatment for exchange or custodial wallets |
| Dispute window | Review period before final root where applicable |
| Final root | Merkle root or eligibility registry |

The snapshot is published with enough information for community verification while avoiding exposure of private personal data.

### 3.4 Claim Contract Model

FUZE uses a dedicated migration claim contract.

Potential contract names:

- `FuzeBoardMigrationClaim`
- `FuzeSurfboardMigrationClaim`
- `FuzeLegacyMigrationClaim`

The recommended contract name for public-neutral migration handling is:

**`FuzeLegacyMigrationClaim`**

Core claim contract functions include:

- verify eligibility
- claim allocation
- prevent duplicate claims
- support Merkle proof or registry proof
- enforce claim window
- apply vesting or staged claim where used
- emit claim events
- return, lock, or reassign unclaimed tokens after deadline according to policy
- pause if issue is found
- expose public read functions

Public read functions include:

- total migration allocation
- claim start
- claim end
- total claimed
- total unclaimed
- claimed by wallet
- claimable by wallet
- vesting schedule
- Merkle root / eligibility root
- policy hash
- metadata URI

### 3.5 Claim Schedule

FUZE uses a staged claim structure to balance legacy-holder recognition with controlled circulation.

Claim schedule options:

| Option | Description | Public Interpretation |
|---|---|---|
| Immediate full claim | Eligible holders claim all FUZE migration tokens immediately | Simple but higher circulation sensitivity |
| Fully vested claim | Eligible holders claim into a vesting schedule | Stronger market-stability structure |
| Partial upfront + vesting | Eligible holders receive a small upfront amount, then the rest vests | Balanced recognition and circulation control |

FUZE applies the balanced direction:

**Partial upfront + vesting**

Recommended migration claim schedule:

| Phase | Rule |
|---|---|
| Initial claim | 10% claimable at migration opening |
| Cliff | 60-day cliff |
| Remaining claim | 90% linear unlock over 12 months |

Alternative conservative schedule:

| Phase | Rule |
|---|---|
| Initial claim | 5% claimable at migration opening |
| Cliff | 60-day cliff |
| Remaining claim | 95% linear unlock over 12 months |

Default public model:

**10% upfront, 60-day cliff, remaining 90% linear unlock over 12 months.**

This model recognizes legacy holders while keeping most migration tokens under staged release.

### 3.6 Relationship to Community Participation Round

Migration remains separate from Community Participation.

| Item | BOARD / Surfboard Migration | Community Participation Round |
|---|---|---|
| Purpose | Legacy-holder continuity | New eligible community participation |
| Allocation | 25,000,000 FUZE | Suggested 70,000,000 FUZE from 110,000,000 FUZE Community Participation Allocation |
| Access | Eligible legacy holders only | Eligible community participants |
| Payment | No purchase payment if claim-based | Purchase / participation |
| Release | Claim-based with staged claim or vesting | 5% at TGE, 60-day cliff, 95% over 12 months |
| Public buy access | No | Yes, selected windows |
| Legal focus | Migration fairness | Participation / sale compliance |

Rule:

**Migration tokens are not sold through the Community Participation Round.**

### 3.7 Relationship to New FUZE Holders

Migration is fair to legacy holders while protecting new FUZE holders from unclear supply pressure.

Common public questions:

| Question | Answer |
|---|---|
| Is migration extra supply? | No. It is already included in the fixed 500,000,000 FUZE supply. |
| Does migration reduce Community Participation Allocation? | No. It is a separate 25,000,000 FUZE allocation. |
| Can migration tokens be bought by others? | No. They are reserved for eligible legacy-holder claims. |
| Does migration unlock all at once? | FUZE uses staged claim or vesting to support controlled circulation. |
| Is migration part of Seed Round? | No. It is a legacy-holder continuity allocation. |

### 3.8 Unclaimed Token Policy

The migration process defines what happens to unclaimed tokens.

| Option | Description | Public Fit |
|---|---|---|
| Return to Migration Reserve | Keeps tokens available for late claims or appeal process | Useful for short extension |
| Move to Community Reserve | Supports broader community after deadline | Strong community-continuity fit |
| Move to Treasury Reserve | Possible but more sensitive for public trust | Requires strong public explanation |
| Burn | Reduces supply but reduces flexibility | Not default |
| Future migration extension | Allows late eligible holders | Useful where legacy base is hard to reach |

FUZE policy:

**Unclaimed migration tokens remain in the Migration Reserve during the claim period and any appeal or extension period. After the final deadline, unclaimed tokens move to Community Reserve or another governance-approved community continuity purpose.**

Unclaimed migration tokens do not move to team, advisors, or liquidity.

### 3.9 Public UI Requirements

The FUZE website includes a migration page, such as:

**FUZE Legacy Migration**

The page includes:

1. Migration overview
2. Eligibility explanation
3. Snapshot details
4. Claim status
5. Wallet checker
6. Claim schedule
7. Contract address
8. Total allocation
9. Total claimed
10. Total unclaimed
11. Claim deadline
12. Unclaimed-token policy
13. FAQ
14. Risk and compliance notice

User flow:

1. User connects wallet.
2. UI checks eligibility.
3. UI shows claimable amount.
4. User claims upfront amount or starts vesting claim.
5. UI shows remaining vesting schedule.
6. UI shows next claimable date.

### 3.10 Public Communication Plan

FUZE communicates migration calmly and clearly.

Communication sequence:

| Phase | Communication |
|---|---|
| Pre-announcement | Explain migration allocation and confirm it is reserved for eligible legacy-holder continuity |
| Eligibility publication | Publish snapshot method, eligibility rules, excluded wallet rules, and review path |
| Contract readiness | Publish contract address, policy hash, metadata URI, and claim schedule |
| Claim opening | Announce claim window, wallet checker, and claim instructions |
| Claim progress | Report total claimed and total unclaimed |
| Deadline reminder | Remind eligible holders before claim window closes |
| Final settlement | Publish final claimed amount, unclaimed amount, and unclaimed-token treatment |

Public communication uses the following language:

**The BOARD / Surfboard Migration allocation is reserved for eligible legacy holders. It is not extra supply, not a public sale, and not part of the Community Participation Round. The allocation is already included in the fixed 500,000,000 FUZE total supply.**

## 4. Investor and Community Relevance

The BOARD / Surfboard Migration matters because it preserves legacy continuity while supporting FUZE v2’s public trust model.

For legacy holders, the migration allocation shows that FUZE recognizes earlier ecosystem history and provides a structured path for eligible continuity.

For new FUZE holders, the policy clarifies that migration is already included in total supply, separate from the Community Participation Allocation, and not available as public sale inventory.

For investors, the migration model reduces uncertainty by defining the allocation amount, claim model, release schedule, public reporting direction, and unclaimed-token policy.

For community members, the migration policy creates a simple explanation of who the allocation is for, how eligibility works, how claims are handled, and how FUZE avoids hidden redirection of migration tokens.

For strategic partners and future ecosystem participants, migration demonstrates that FUZE handles legacy obligations through transparent process rather than informal discretionary distribution.

FUZE is not relying on token speculation as the only exit path. FUZE is building real products, real users, revenue potential, shared platform rails, and strategic acquisition optionality.

## 5. Public Boundary

FUZE publicly presents the BOARD / Surfboard Migration at the policy and process level.

FUZE publicly explains:

- allocation amount
- percentage of total supply
- migration purpose
- eligibility model
- snapshot method
- claim contract model
- claim schedule
- unclaimed-token policy
- separation from Community Participation Round
- separation from Seed Round
- separation from treasury, liquidity, team, and advisor allocations
- public UI requirements
- claim status reporting

FUZE keeps sensitive or readiness-dependent details subject to legal, compliance, technical, and governance review, including:

- final snapshot block or timestamp before publication
- excluded wallet list before validation
- appeal or review cases
- personal identity data
- private legacy-holder support tickets
- legal treatment of edge cases
- custodial or exchange wallet handling details before resolution
- final contract deployment timing
- security review findings before disclosure readiness

FUZE’s Seed Round discussions are private strategic fundraising conversations. Full details, structure, and terms are shared privately with qualified interested parties. This is not a public token sale.

Public Vault Access, if implemented, is subject to eligibility, jurisdiction, compliance, platform readiness, market-aligned pricing rules, lockups, and final policy approval.

Platform Credits are for product usage and are not investment assets, payout assets, or FUZE tokens.

Profit participation is a long-term design direction and is not immediate or guaranteed. Any future framework requires legal, accounting, treasury, technical, and transparency readiness.

## 6. Risk Boundaries and Safeguards

FUZE does not guarantee token price, liquidity, listing, profit, return, payout, or market performance.

FUZE applies the following safeguards to the BOARD / Surfboard Migration:

| Risk Area | FUZE Safeguard |
|---|---|
| Migration treated as sale inventory | Migration tokens are claim-based for eligible legacy holders only |
| New holder dilution concern | Migration allocation is already included in the fixed 500,000,000 FUZE total supply |
| Community Participation confusion | Migration remains separate from the Community Participation Round |
| Immediate sell-pressure concern | FUZE uses partial upfront claim and staged vesting |
| Eligibility disputes | Snapshot, registry, review path, and published rules support verification |
| Duplicate claims | Claim contract prevents duplicate claims through proof or registry logic |
| Hidden token redirection | Unclaimed tokens move only according to published policy |
| Treasury misuse concern | Migration tokens do not become general treasury inventory during claim period |
| Team/advisor misuse concern | Migration tokens do not move to team or advisor allocation |
| Private data exposure | Snapshot and reporting avoid exposing private personal data |
| Legal overstatement | Eligibility, jurisdiction, compliance, and contract readiness remain reviewed |

FUZE does not guarantee exchange listing, listing timing, liquidity, price performance, or market outcome.

Migration does not remove market risk. It defines legacy-holder continuity, eligibility controls, staged release, public reporting, and unclaimed-token treatment.

## 7. Reporting and Transparency Direction

FUZE reports BOARD / Surfboard Migration through public documentation, website UI, contract references, and dashboard summaries.

Migration reporting can appear in:

- FUZE Legacy Migration page
- public tokenomics section
- vault dashboard
- transparency dashboard
- public contract and wallet registry
- migration FAQ
- investor materials
- community FAQ
- governance reporting
- Controlled Circulation Policy documentation
- Vault-by-Vault Release Rules documentation
- whitepaper-compatible public documentation

FUZE transparency direction includes:

| Reporting Area | Public Transparency Direction |
|---|---|
| Allocation amount | Shows 25,000,000 FUZE migration allocation |
| Supply percentage | Shows 5.00% of fixed total supply |
| Eligibility method | Shows snapshot, registry, proof, or hybrid method |
| Snapshot details | Shows block/time and verification logic where ready |
| Claim contract | Shows verified contract address when deployed |
| Claim window | Shows start, end, and deadline |
| Claim schedule | Shows upfront percentage, cliff, and linear unlock period |
| Total claimed | Shows aggregate claimed amount |
| Total unclaimed | Shows remaining unclaimed amount |
| Unclaimed policy | Shows reserve, extension, or community-continuity treatment |
| Policy hash | Links migration policy to public record |
| FAQ | Explains migration relationship to Community Participation, Seed Round, and total supply |
| Risk notice | Shows price, liquidity, listing, return, payout, eligibility, and jurisdiction boundaries |

FUZE uses reporting to make migration understandable. Public readers can see that migration is already accounted for, claim-based, separate from public participation, and governed by published rules.

## 8. Conclusion

FUZE uses the BOARD / Surfboard Migration allocation to preserve legacy-holder continuity while keeping FUZE v2 fair, transparent, and controlled.

The **25,000,000 FUZE** migration allocation is reserved for eligible legacy-holder claims. It is not public sale inventory, not treasury inventory, not liquidity inventory, and not team or advisor inventory.

FUZE handles migration through eligibility rules, snapshot or registry proof, a dedicated claim contract, staged release, public UI, claim reporting, and unclaimed-token policy.

This approach supports legacy trust, new-holder clarity, investor confidence, Controlled Circulation, and FUZE’s broader transparency-first AI SaaS platform direction.