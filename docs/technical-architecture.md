# Building Your Technical Architecture Section

> Best practices for writing the technical architecture portion of your SCF Build Award application. This is where reviewers assess whether your team genuinely understands Stellar/Soroban and whether your design is sound.

## Why the Architecture Section Matters

The technical architecture section is often the single most scrutinized part of an SCF submission. Reviewers use it to evaluate:

- Whether you actually understand Stellar and/or Soroban (or are just name-dropping)
- Whether your design is technically feasible
- Whether Stellar plays a core, necessary role in the architecture (not shoehorned in)
- Whether the team can execute on the design

A weak architecture section signals that the team hasn't done its homework. A strong one builds confidence that you can deliver.

---

## What to Include

### 1. System Overview

Start with a high-level diagram or description of your system. Show all major components and how they interact. The reader should understand your entire product in 30 seconds.

**Include:**
- Frontend/client applications
- Backend services (if any)
- Smart contracts (Soroban)
- Stellar network interactions (payments, SEPs, assets)
- External dependencies (oracles, anchors, partner APIs)
- Data storage (on-chain vs off-chain)

**Format:** A box-and-arrow diagram is ideal. If you can't create one, a structured text description with clear component labels works too.

### 2. Stellar/Soroban Integration Details

This is the most important subsection. Explain exactly how your project uses Stellar and/or Soroban. Be specific.

**For Soroban projects, address:**
- Which smart contracts you'll write and what each one does
- Contract interfaces (key functions, parameters, return values)
- State management (what data lives on-chain vs off-chain and why)
- How contracts interact with each other
- Resource usage considerations (CPU, memory, storage — Soroban meters these)
- State archival strategy (how you handle Soroban's TTL-based state expiration)

**For Stellar-native projects (SEPs, assets, payments), address:**
- Which SEPs you implement and why (e.g., SEP-31 for cross-border, SEP-24 for deposit/withdraw)
- Asset issuance strategy (existing asset vs new issuance, trustlines)
- Account structure (custodial vs non-custodial, multisig)
- Transaction flow from user action to on-chain settlement

**For Integration Track specifically:**
- Name the building block and its API/SDK
- Show the exact integration points between your app and the building block
- Explain what the building block provides and what you build on top of it

### 3. Data Flow

Walk through at least one key user action end-to-end. Show what happens at every layer.

**Example format:**

```
User clicks "Send Payment"
  -> Frontend validates input, constructs transaction parameters
  -> Backend (or client-side) builds Stellar transaction with SEP-10 auth
  -> Transaction submitted to Stellar Horizon
  -> Anchor receives payment notification via SEP-31 callback
  -> Recipient receives payout in local currency
  -> Frontend displays confirmation with transaction hash
```

Show the happy path in detail. Mention error handling for critical failure points (e.g., "if the anchor callback fails, the transaction is refunded via clawback").

### 4. Security Considerations

Reviewers notice when security is absent from the architecture. Address:

- **Key management:** How are private keys stored? (Hardware wallet, custodial service, MPC, client-side?)
- **Access control:** Who can call which contract functions? How are admin operations gated?
- **Input validation:** How do you prevent malicious inputs from reaching your contracts?
- **Audit plans:** Will you seek a security audit? (Build Award recipients can access audit credits through the LaunchKit.)
- **Known attack vectors:** For DeFi projects, address reentrancy, oracle manipulation, flash loan attacks, and other relevant risks.

### 5. Infrastructure and Deployment

Briefly describe where and how your system runs:

- Hosting (cloud provider, self-hosted, decentralized)
- RPC/Horizon endpoint strategy (public vs dedicated)
- Monitoring and alerting
- Testnet vs mainnet deployment plan

### 6. Technology Stack

List your stack concisely. Reviewers want to see that your choices are reasonable for the scope.

**Example:**

| Layer | Technology |
|-------|-----------|
| Frontend | React + Stellar SDK |
| Smart Contracts | Soroban (Rust) |
| Backend | Node.js |
| Database | PostgreSQL (off-chain user data) |
| RPC | Dedicated Stellar RPC node |
| Auth | SEP-10 for wallet auth |

---

## How to Show Stellar Is Core (Not Shoehorned)

This is the number one thing reviewers look for. Ask yourself: **could this project work equally well without Stellar?** If yes, your architecture section will fail.

**Signs that Stellar is core:**
- Soroban contracts handle core business logic (not just a token wrapper)
- Stellar's consensus, asset issuance, or SEP infrastructure provides capabilities you couldn't easily get elsewhere
- On-chain state is essential to the product's trust model
- The architecture would fundamentally change without Stellar

**Signs that Stellar is shoehorned:**
- The only Stellar component is a token you issued
- You could swap Stellar for any other chain with no architectural changes
- Smart contracts do trivial operations that don't require a blockchain
- The architecture diagram shows Stellar as a small box on the periphery

### Integration Track Specifically

For the Integration Track, your architecture must center on the building block you're integrating. The diagram should clearly show the building block as a core component, not an optional module. If removing the integration partner would leave your product mostly intact, the architecture doesn't fit the Integration Track.

---

## Common Mistakes

| Mistake | What to Do Instead |
|---------|-------------------|
| Listing technologies without explaining how they connect | Draw the connections. Show data flow. |
| Saying "we'll use Soroban" without contract details | Describe each contract, its purpose, and key functions. |
| No diagram | Include at least one visual. Even a text-based flowchart helps. |
| Architecture that works without Stellar | Redesign, or explain why Stellar is irreplaceable in your stack. |
| Ignoring state management | Explicitly address what's on-chain vs off-chain and why. |
| No security section | Add one. Even a brief acknowledgment of key risks and mitigations. |
| Over-engineering | Don't describe a microservices architecture for a simple app. Match complexity to scope. |
| Copying another project's architecture | Reviewers have seen many submissions. Make your architecture specific to your product. |
| Claiming "decentralized" with a centralized backend | Be honest about what's decentralized and what isn't. Reviewers respect honesty. |

---

## Architecture Section Template

Use this as a starting structure for your submission:

```
## Technical Architecture

### System Overview
[1-2 paragraph description + diagram]

### Stellar/Soroban Integration
[Detailed explanation of how Stellar/Soroban is used]
- Smart contracts: [list with descriptions]
- On-chain data: [what and why]
- SEPs implemented: [if applicable]

### Data Flow
[End-to-end walkthrough of a key user action]

### Security
- Key management: [approach]
- Access control: [approach]
- Audit plan: [yes/no, timing]

### Infrastructure
- Hosting: [where]
- RPC strategy: [public/dedicated]
- Deployment: [testnet -> mainnet plan]

### Tech Stack
[Table of technologies by layer]
```

---

## Checklist Before You Submit

- [ ] Architecture includes a system overview diagram or detailed description
- [ ] Stellar/Soroban integration is described with specifics (contracts, SEPs, asset model)
- [ ] At least one end-to-end data flow is shown
- [ ] Security considerations are addressed
- [ ] On-chain vs off-chain data split is explained
- [ ] The architecture would break without Stellar (Stellar is core, not peripheral)
- [ ] Technology stack is listed and appropriate for scope
- [ ] For Integration Track: the building block is central to the diagram, not an appendage
