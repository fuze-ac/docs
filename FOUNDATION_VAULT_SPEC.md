# foundation-vault.spec.md

## 1. Purpose

This specification defines the `FuzeFoundationVault` contract.

The Foundation Vault is the permanent on-chain stewardship reserve of the FUZE ecosystem. Its primary purpose is to hold a fixed principal amount of FUZE indefinitely and to participate in the Stablecoin Profit Participation system as an eligible holder, without ever selling, transferring, or operationally deploying the FUZE principal.

The Foundation Vault exists to strengthen long-term trust, reduce sell-pressure risk, and support FUZE as a transparency-first SaaS ecosystem.

---

## 2. Contract Identity

- **Contract name:** `FuzeFoundationVault`
- **Vault type:** `FOUNDATION_VAULT`
- **Token held:** `FUZE`
- **Principal allocation:** `35,000,000 FUZE`
- **Stablecoin source:** `Stablecoin Profit Participation Contract`
- **Primary operations destination:** `Foundation Operations Wallet`

---

## 3. Design Objectives

The contract MUST satisfy the following objectives:

1. Hold exactly the Foundation principal allocation on-chain.
2. Prevent all direct and indirect disposal of the FUZE principal.
3. Act as an eligible holder in the Stablecoin Profit Participation system.
4. Allow claiming of stablecoin profit participation only.
5. Forward claimed stablecoins only to an approved Foundation Operations Wallet.
6. Expose transparent public read functions and event logs.
7. Minimize admin trust assumptions.
8. Preserve the permanent lock invariant under all normal contract behavior.

---

## 4. Principal Economic Policy

### 4.1 Foundation Principal

The Foundation principal is:

> **35,000,000 FUZE**

This principal MUST remain inside the Foundation Vault permanently.

### 4.2 Stablecoin Profit Participation

The Foundation Vault MAY receive stablecoin profit participation under the same published holder-eligibility policy used by the Stablecoin Profit Participation Contract.

The Foundation Vault does not realize value through sale of FUZE principal.
It realizes value only through stablecoin profit participation.

### 4.3 No Principal Liquidity Use

The Foundation principal MUST NOT be:
- sold
- transferred
- approved to third parties
- deposited into liquidity pools
- bridged to another network
- pledged as collateral
- used in lending protocols
- used in staking systems that alter custody or lock assumptions
- delegated to market-making operations

---

## 5. Required State Variables

The contract SHOULD expose, at minimum, the following state:

- `address public fuzeToken;`
- `address public stablecoinProfitParticipationContract;`
- `address public foundationOpsWallet;`
- `address public governanceMultisig;`
- `address public timelockController;`
- `uint256 public constant FOUNDATION_PRINCIPAL = 35_000_000 * 1e18;`  
  or adjusted for FUZE decimals
- `uint256 public cumulativeStablecoinClaimed;`
- `bool public paused;`
- `string public version;`
- `bytes32 public policyHash;`

Optional but recommended:
- `string public purposeURI;`
- `string public metadataURI;`

---

## 6. Core Invariants

The following invariants are critical and MUST always hold:

### 6.1 Principal Lock Invariant

The Foundation Vault MUST never allow outbound movement of FUZE principal.

Formally:
- no successful call path may reduce FUZE principal below its intended locked level except for accidental-token handling that explicitly excludes FUZE
- the contract must not expose transfer, approve, or arbitrary call patterns that can move FUZE principal

### 6.2 Claim Destination Invariant

Stablecoin profit claims may only be routed to the approved `foundationOpsWallet` or a tightly governed whitelist if such whitelist is explicitly adopted.

### 6.3 No Hidden Approval Invariant

The contract MUST never approve FUZE principal spending to any external spender.

### 6.4 Profit-Only Outflow Invariant

The only economic outflow permitted by this contract is stablecoin profit participation proceeds.

### 6.5 Governance-Change Safety Invariant

Any change to governance-critical addresses must be timelocked and event-emitting.

---

## 7. Allowed Functions

The contract MAY include only the following functional categories.

### 7.1 Initialization

Allowed during setup only:
- set FUZE token address
- set Stablecoin Profit Participation Contract address
- set Foundation Operations Wallet
- set governance multisig
- set timelock controller
- accept or receive the 35,000,000 FUZE principal

### 7.2 View Functions

Required public view functions should include:
- `fuzeToken()`
- `stablecoinProfitParticipationContract()`
- `foundationOpsWallet()`
- `governanceMultisig()`
- `timelockController()`
- `foundationPrincipal()`
- `currentFuzeBalance()`
- `claimableStablecoinProfit()`
- `cumulativeStablecoinClaimed()`
- `isPaused()`
- `version()`
- `policyHash()`

### 7.3 Stablecoin Profit Claiming

Allowed:
- claim Foundation’s stablecoin allocation from the Stablecoin Profit Participation Contract
- forward claimed stablecoins directly to `foundationOpsWallet`

Recommended function pattern:
- `claimProfit()`

Preferred behavior:
- callable by anyone or by authorized role
- proceeds always routed to fixed destination wallet
- no caller-selected payout address

### 7.4 Governance Address Updates

Allowed only through multisig + timelock:
- update Foundation Operations Wallet
- update Stablecoin Profit Participation Contract address
- update governance multisig address
- update timelock controller address
- update policy hash or metadata references

### 7.5 Emergency Pause

Optional:
- pause stablecoin claiming path
- unpause stablecoin claiming path

Pause MUST NOT enable principal withdrawal.

### 7.6 Accidental Foreign Token Recovery

Optional but tightly constrained:
- recover accidental non-FUZE, non-governed foreign tokens sent to the contract

This MUST explicitly exclude:
- FUZE principal
- stablecoin proceeds already governed by Foundation policy unless separately handled by approved accounting logic

---

## 8. Forbidden Behaviors

The contract MUST NOT allow any of the following:

1. transfer of FUZE principal to any wallet or contract
2. approval of FUZE principal to any spender
3. arbitrary external call execution using FUZE principal
4. changing claim destination per call
5. sale, swap, bridge, lend, or collateralization of FUZE principal
6. self-destruction or destruction patterns that can release principal
7. admin rescue of FUZE principal
8. hidden owner-only escape hatch
9. upgrade path that creates principal withdrawal ability
10. use of Foundation Vault as general treasury
11. routing stablecoin profit to founder personal wallet by default
12. unstated usage categories outside Foundation policy

---

## 9. Claim Flow Specification

### 9.1 High-Level Flow

1. Stablecoin Profit Participation Contract computes the Foundation’s eligible share.
2. `FuzeFoundationVault` becomes entitled to a claimable stablecoin amount.
3. `claimProfit()` is executed.
4. Stablecoin Profit Participation Contract transfers or releases stablecoin to the Foundation Vault flow.
5. Foundation Vault forwards stablecoin only to `foundationOpsWallet`.
6. Contract emits claim event.

### 9.2 Claim Function Rules

`claimProfit()` SHOULD:
- determine claimable amount from the linked profit contract
- reject zero-claim attempts if desired
- claim only the Foundation’s entitled amount
- transfer proceeds only to `foundationOpsWallet`
- update cumulative accounting
- emit event with token, amount, and destination

### 9.3 Public Callable vs Restricted Callable

Preferred v1 design:
- `claimProfit()` may be public-callable
- funds must always route to fixed destination wallet

This reduces operational dependency while preserving safety.

---

## 10. Foundation Operations Wallet Rules

### 10.1 Purpose

The `foundationOpsWallet` receives stablecoin profits claimed by the Foundation Vault.

### 10.2 Allowed Role

It exists as the operational destination for Foundation-managed stablecoin proceeds.

### 10.3 Governance Requirement

Changing this wallet MUST require:
- multisig approval
- timelock delay
- public event emission

### 10.4 Recommended Restrictions Outside Contract

Operational policy outside the contract should require that funds received by the Foundation Operations Wallet are used only for approved Foundation purposes, such as:
- transparency and reporting
- audits and security reviews
- ecosystem grants
- research and documentation
- governance support
- community public-good programs

---

## 11. Admin Model

### 11.1 Governance Structure

The contract SHOULD be governed by:
- **Foundation Governance Council multisig**
- **timelock controller** for sensitive changes

### 11.2 Required Admin Roles

Minimum roles:
- `governanceMultisig`
- `timelockController`

Optional roles:
- `pauserRole`

### 11.3 Sensitive Actions Requiring Timelock

The following actions MUST be timelocked:
- changing `foundationOpsWallet`
- changing `stablecoinProfitParticipationContract`
- changing `governanceMultisig`
- changing `timelockController`
- changing policy metadata references if governance-sensitive

### 11.4 Non-Permitted Admin Powers

Admins MUST NOT be able to:
- withdraw FUZE principal
- approve FUZE principal spending
- call arbitrary external contracts with FUZE principal
- alter claim destination at execution time without policy-governed change process

---

## 12. Event Model

The contract SHOULD emit the following events:

### 12.1 Core Governance Events
- `FoundationGovernanceUpdated(address oldGov, address newGov)`
- `FoundationTimelockUpdated(address oldTimelock, address newTimelock)`
- `FoundationPaused(address actor)`
- `FoundationUnpaused(address actor)`

### 12.2 Operations Wallet Events
- `FoundationOpsWalletUpdated(address oldWallet, address newWallet)`

### 12.3 Profit Participation Events
- `ProfitParticipationContractUpdated(address oldAddr, address newAddr)`
- `FoundationProfitClaimed(address stablecoin, uint256 amount, address destination)`

### 12.4 Metadata / Policy Events
- `FoundationPolicyHashUpdated(bytes32 oldHash, bytes32 newHash)`
- `FoundationMetadataURIUpdated(string oldURI, string newURI)`

### 12.5 Recovery Events
If foreign-token recovery exists:
- `ForeignTokenRecovered(address token, uint256 amount, address destination)`

No event should ever represent FUZE principal outbound movement, because such movement must not exist.

---

## 13. Upgradeability Policy

### 13.1 Preferred Policy

The Foundation Vault SHOULD be:

> **non-upgradeable**

This is strongly preferred because the Foundation principal lock is one of the strongest trust signals in the FUZE system.

### 13.2 If Upgradeability Is Unavoidable

If an upgradeable pattern is used, it MUST satisfy all of the following:
- upgrade controlled by multisig + timelock
- public event emitted on upgrade
- no upgrade may create principal withdrawal path
- no upgrade may create FUZE approval path
- no upgrade may remove core events or public getters
- no upgrade may change principal lock semantics

### 13.3 Economically Immutable Rules

The following Foundation rules must be treated as economically immutable:
- 35,000,000 FUZE principal lock
- no sale / no transfer of principal
- profit-only participation model
- fixed or governed destination rule for stablecoin proceeds

---

## 14. Security Requirements

The implementation MUST include or address:
- reentrancy protection for claim path if required
- strict role separation
- no arbitrary external call capability
- careful validation of external contract address updates
- safe token transfer handling
- invariant tests for principal lock
- tests for unauthorized claim redirection failure
- tests for admin abuse prevention

Recommended test categories:
- principal cannot move under any authorized role
- claim succeeds only to approved destination
- governance changes require correct access path
- pause does not affect principal lock
- foreign-token recovery cannot touch FUZE principal

---

## 15. Integration with Stablecoin Profit Participation Contract

### 15.1 Integration Requirement

`FuzeFoundationVault` MUST integrate with the Stablecoin Profit Participation Contract as an eligible holder address.

### 15.2 Integration Expectations

The linked profit participation contract should support:
- querying Foundation claimable amount
- claiming Foundation stablecoin allocation
- returning stablecoin token address or payout asset information

### 15.3 Address Update Rule

The linked profit participation contract address MAY be updated only by multisig + timelock.

### 15.4 Trust Boundary

The Foundation Vault depends on the correctness of the Stablecoin Profit Participation Contract for amount calculation, but the Foundation Vault itself remains responsible for ensuring:
- no principal FUZE outflow
- no redirected stablecoin destination

---

## 16. Canonical Summary

| Field | Value |
|---|---|
| Contract Name | `FuzeFoundationVault` |
| Principal Amount | `35,000,000 FUZE` |
| Core Purpose | Permanent Foundation stewardship reserve |
| Principal Mobility | Permanently locked |
| Allowed Economic Outflow | Stablecoin profit participation only |
| Stablecoin Destination | Approved `foundationOpsWallet` only |
| Governance | Foundation multisig + timelock |
| Upgradeability | Non-upgradeable strongly preferred |
| Critical Invariant | FUZE principal can never leave |

---

## 17. Canonical Policy Statement

The FUZE Foundation Vault is a permanently locked on-chain stewardship reserve holding 35,000,000 FUZE. The vault may not sell, transfer, approve, collateralize, bridge, or otherwise deploy the FUZE principal. Its only economic participation is through stablecoin profit participation under the Stablecoin Profit Participation Contract. Claimed stablecoins may be forwarded only to the approved Foundation Operations Wallet under governance-controlled policy. The principal lock must remain permanent and verifiable on-chain.
