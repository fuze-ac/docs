# FUZE Token Release and Circulation Clarity

## Executive Summary

FUZE token supply reports use distinct terms for allocation, custody, restriction, release, claimability, deployment, and circulation. A transaction or unlock can change one status without changing every other status.

This paper is the public terminology and reporting standard. It defines the supply fields, classification tests, reconciliation equations, event labels, report format, and correction rules needed to interpret FUZE token movement consistently.

The fixed supply is **500,000,000 FUZE**. That total includes all approved allocation categories and remains separate from current transferable, deployed, claimable, or circulating amounts.

The operating movement controls are defined in the [FUZE Controlled Circulation Policy](12-FUZE_CONTROLLED_CIRCULATION_POLICY_PUBLIC.md). Category-specific release conditions remain in the vault and vesting papers.

---

## 1. Clarity Objective

Supply reporting should let a reader answer:

- which number is being presented;
- what date, block, network, and methodology apply;
- which tokens changed state;
- whether custody or economic availability changed;
- which allocation and event caused the change;
- whether prior figures were corrected or restated.

Terms describe different states even when they apply to the same tokens at different points in time.

---

## 2. Controlling Supply

The approved token supply is:

| Field | Value |
|---|---:|
| Fixed total supply | 500,000,000 FUZE |
| Approved allocation categories | 10 |
| Allocation reconciliation | 100.00% |

The [FUZE Token Allocation Table](02-FUZE_TOKEN_ALLOCATION_TABLE_PUBLIC.md) controls category names, amounts, percentages, and mandates.

Supply reports should identify the verified token contract and network when those details are approved for publication. This paper omits the address.

---

## 3. Supply Vocabulary

### Total supply

The complete issued supply under the verified FUZE token contract, adjusted for any verifiable burn or other approved supply-changing event.

The public tokenomics model fixes this value at 500,000,000 FUZE unless an approved and publicly documented technical or policy event changes the on-chain figure consistently with the governing model.

### Allocated supply

Tokens assigned to one of the ten approved purpose categories. Allocation describes mandate, separate from release and circulation.

### Custodied supply

Tokens held in an identified wallet, vault, contract, custodian, bridge, or other controlled location. Custody alone is insufficient to determine circulation.

### Locked supply

Tokens restricted by contract, vesting, lockup, policy, agreement, jurisdiction, claim condition, or another enforceable limitation.

### Unlocked supply

Tokens for which a specified lock or vesting restriction has ended. Other restrictions or controlled custody can remain.

### Vested supply

Tokens that have satisfied the applicable vesting condition. Vested tokens can remain unreleased or non-circulating.

### Unvested supply

Tokens awaiting satisfaction of the vesting condition.

### Claimable supply

Tokens available for an eligible recipient to claim under an active process and current claim window.

### Claimed supply

Tokens successfully claimed under the applicable process. Claimed status alone is insufficient to determine whether another lock applies.

### Released supply

Tokens moved from a prior controlled state under an approved release instruction.

### Operationally deployed supply

Tokens placed into an approved program, contract, partner arrangement, incentive process, treasury use, or market operation.

### Circulating supply

Tokens reasonably available in user or market circulation under the published methodology. The method should explain treatment of controlled treasury wallets, vesting wallets, contracts, liquidity pools, bridges, custodians, claims, and restrictions.

### Reserved supply

Tokens retained for a defined future purpose outside ordinary circulation.

### Treasury-controlled supply

Tokens controlled by FUZE treasury, reserve, foundation, program, signer, or another approved operating authority.

### Liquidity-deployed supply

Tokens placed into an approved liquidity or market-structure operation. Reports should distinguish supplied, paired, withdrawn, committed, custodied, and externally available amounts.

### Bridged or represented supply

A representation backed by locked or custodied FUZE on another network or system. Backed representations should reconcile to the underlying tokens and remain excluded from economic supply as newly issued units.

### Burned supply

Tokens verifiably sent to an approved irreversible burn mechanism and removed from the applicable supply calculation.

---

## 4. Event Vocabulary

| Event | Required interpretation |
|---|---|
| Allocation | Assigns purpose; leaves circulation unchanged by itself |
| Vault deposit | Changes custody; classification depends on continuing control |
| Vault withdrawal | Removes tokens from a vault; resulting state depends on destination and restrictions |
| Unlock | Ends a stated restriction; transfer and circulation require separate evidence |
| Vest | Satisfies a vesting condition; release can remain pending |
| Release | Authorizes or executes movement from a controlled state |
| Claim opens | Makes an approved amount claimable for eligible recipients |
| Claim | Moves or records tokens for a qualified claimant |
| Program deployment | Assigns tokens to an approved operating program |
| Liquidity deployment | Places tokens into market-structure activity under the relevant policy |
| Custody transfer | Moves tokens between controlled locations without necessarily changing circulation |
| Return | Restores unused or recovered tokens to approved control |
| Reclassification | Changes allocation purpose or reporting category under approval |
| Burn | Permanently reduces supply where technically verified |
| Correction | Repairs an erroneous amount, label, or prior report |

Public updates should name the event rather than relying on the vague term “tokens moved.”

---

## 5. Classification Tests

Before assigning circulating status, the reporting owner should assess:

### Control

Does FUZE or another restricted operator retain unilateral or governed control over the tokens?

### Transferability

Can the holder transfer the tokens without a lock, contract, policy, legal, custody, or program restriction?

### Availability

Are the tokens available to users or markets, or merely prepared for future release?

### Obligation

Are the tokens committed to a recipient, program, partner, vesting schedule, claim process, or reserve?

### Custody

Are tokens in self-custody, omnibus custody, treasury custody, a contract, bridge, vesting vault, claim vault, or liquidity position?

### Return rights

Can unused or cancelled tokens be recovered to a controlled allocation?

### Method consistency

Does the classification match the published methodology used for prior periods?

No single test is decisive in every case. The report should explain material judgment.

---

## 6. Reconciliation Equations

The high-level supply equation is:

```text
Total supply = circulating + non-circulating
```

The non-circulating population can include overlapping descriptive attributes, so reports should avoid summing labels that lack mutual exclusivity.

For example, team tokens can be both treasury-custodied and unvested. A report should either use exclusive state buckets or clearly label attributes.

An exclusive state reconciliation can use:

```text
Opening state balance
+ inbound reclassifications
- outbound reclassifications
+ returns and corrections
- releases or deployments
= closing state balance
```

Circulating-supply movement can be expressed as:

```text
Opening circulating supply
+ newly classified circulating
- returned, locked, burned, or otherwise removed
+/- corrections
= closing circulating supply
```

Every report should reconcile to the controlling total and explain any bridged representation or burn treatment.

---

## 7. Point-in-Time and Period Reporting

### Point-in-time report

Shows balances and classifications at a specified timestamp or block.

Required fields include:

- report time and timezone;
- network and block where applicable;
- total supply;
- exclusive circulation categories;
- allocation or custody references;
- methodology version.

### Period movement report

Shows events between an opening and closing point.

Required fields include:

- opening balances;
- release, claim, vesting, deployment, return, correction, and reclassification events;
- closing balances;
- transaction or governance references;
- unresolved items.

Comparisons between a point-in-time balance and a period flow require an explanation of the difference.

---

## 8. Reporting Schema

| Field | Description |
|---|---|
| Report identifier | Stable name and version |
| Scope | Network, contract, allocations, wallets, and systems included |
| As-of record | Timestamp and block or source cutoff |
| Methodology | Classification definitions and calculation rules |
| Total supply | Controlling supply figure |
| Circulating supply | Amount under the published method |
| Non-circulating supply | Reconciled remainder |
| State detail | Exclusive balances or clearly labeled attributes |
| Period events | Releases, claims, deployments, returns, burns, and corrections |
| Allocation detail | Source category for material movement |
| Evidence | Transactions, vaults, contracts, governance, or report references |
| Exceptions | Unresolved or estimated items |
| Prior-period changes | Restatements and methodology changes |
| Owner and review | Responsible preparer and reviewer |

Machine-readable exports and human-readable summaries should use the same definitions.

---

## 9. Interpretation Examples

### Treasury wallet transfer

FUZE moves tokens from one controlled treasury wallet to another after a custody update.

**Report treatment:** custody movement; circulation remains unchanged when control and restrictions remain equivalent.

### Team vesting event

A scheduled portion satisfies vesting but remains in a controlled vesting contract.

**Report treatment:** unvested decreases and vested-unreleased increases; circulating supply may remain unchanged.

### Migration claim

An eligible legacy holder claims tokens during an active window.

**Report treatment:** claimable decreases and claimed increases. Circulation treatment follows any continuing lock and the published method.

### Community approval pending release

A participant receives an approved allocation record but release conditions remain outstanding.

**Report treatment:** committed or approved-pending-release; awaiting release and outside circulation.

### Liquidity-pool deployment

Tokens move from a controlled market-operations wallet into an approved pool.

**Report treatment:** liquidity-deployed amount is reported separately; circulating classification follows the methodology and position structure.

### Bridge mint

Underlying FUZE is locked and an equivalent representation is minted on another network.

**Report treatment:** underlying and representation reconcile one-to-one; the representation remains excluded from new economic supply.

---

## 10. Allocation and Wallet Labels

Public wallets and contracts should use labels that identify:

- controlling allocation or function;
- custody or contract type;
- current status;
- supported network;
- whether the address is active, replaced, or deprecated;
- authoritative publication source.

Mixing unrelated allocation purposes in one wallet requires a documented sub-ledger and reporting method.

An address label supports interpretation; establishing personal ownership requires separate evidence. Public reporting must keep the person behind a wallet private.

---

## 11. Unlock and Release Calendar

A public calendar can show known or conditional events.

Each entry should identify:

- allocation;
- event type;
- earliest or scheduled time;
- amount or calculation method;
- conditions;
- current status;
- resulting classification if completed;
- report or governance reference.

Conditional dates should be labeled as such. A calendar entry alone is insufficient evidence that a release occurred.

Actual events should be reconciled after execution, including delays, partial completion, cancellation, or correction.

---

## 12. Data Providers and Third Parties

Exchanges, explorers, market-data services, partners, and community dashboards can use different circulation methods.

FUZE should publish:

- its authoritative methodology;
- current verified figures;
- public wallet labels;
- report and correction history;
- contact route for material discrepancies.

Third parties may adopt different classifications. Differences should be explained rather than presented as proof that one number is intentionally misleading.

---

## 13. Corrections and Restatements

A correction addresses an error within the existing method. A restatement changes prior figures because of a material error, newly available evidence, or methodology change.

The record should identify:

1. affected report and period;
2. prior and revised figures;
3. reason;
4. affected classifications;
5. methodology version;
6. reviewer and effective date;
7. downstream reports or providers notified.

Prior versions should remain accessible and visibly superseded.

---

## 14. Relationship to Other Systems

Platform Credits remain outside FUZE token supply calculations. Stablecoin balances are payment and treasury records rather than FUZE supply.

Approved distributable value is a separate value-ledger status. Wallet-based participation uses its own eligibility, snapshot, claim, and correction records where activated.

These systems can be reported alongside token supply only when their units and purposes remain distinct.

---

## 15. Public Boundary

This paper covers terminology and reporting methods rather than announcing a release, unlock, claim, burn, bridge, circulating-supply figure, or market event.

Circulation figures require current contract, wallet, custody, restriction, and event data. Market liquidity and venue support remain separate from supply classification.

Circulation-specific risks are summarized in [FUZE Token Risk Boundaries](29-FUZE_TOKEN_RISK_BOUNDARIES_PUBLIC.md), with consolidated treatment in the [FUZE Risk and Disclosure Appendix](../WHITEPAPER-PAPERS/05-FUZE_RISK_AND_DISCLOSURE_APPENDIX_PUBLIC.md).

---

## Conclusion

FUZE release clarity depends on using supply terms as defined states rather than synonyms.

The reporting schema connects each number to a timestamp, methodology, allocation, event, custody record, and reconciliation. This allows readers to distinguish an allocation, transfer, unlock, vest, claim, deployment, and circulating-supply change without inferring more than the evidence supports.
