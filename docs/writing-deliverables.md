# Writing and Structuring Deliverables

> How to break your SCF Build Award application into clear, verifiable milestone deliverables that reviewers trust and panels can approve quickly.

## Why Deliverables Matter

SCF funding is released in four tranches tied to milestones. Reviewers evaluate your deliverables to determine whether your plan is realistic, whether progress can be verified, and whether each tranche unlocks meaningful work. Vague or poorly structured deliverables are one of the most common reasons submissions are scored down or rejected.

---

## The Four-Tranche Framework

Every Build Award distributes funding across these milestones:

| Tranche | Budget | Milestone | What You Prove |
|---------|--------|-----------|---------------|
| 0 | 10% | Award approval | Proof of intent |
| 1 | 20% | Milestone 1 | Core Stellar/Soroban integration works |
| 2 | 30% | Milestone 2 | Product is testable end-to-end |
| 3 | 40% | Milestone 3 + UX readiness | Product is live, usable, and discoverable |

**A note on naming:** You'll see tranches referred to as "MVP," "Testnet," and "Mainnet" in SCF documentation. These labels are more symbolic than literal — think of them as Milestone 1, 2, and 3. Your T1 doesn't have to be a traditional MVP, and your T2 doesn't have to be exclusively a testnet deployment. What matters is that each milestone represents a meaningful, verifiable step forward. The names signal the general direction (working core -> testable build -> production launch), but your specific deliverables should fit your project, not be forced into rigid categories.

Your job is to define concrete deliverables under each tranche that a reviewer can verify without ambiguity.

### Scope Down, Ship, Come Back

Before you plan your deliverables, ask: **Can I reduce the scope?** One of the strongest strategies — especially for first-time applicants — is to define a tighter, smaller set of deliverables, request less funding, execute cleanly, and come back for a second award with traction data.

Reputation and trust matter enormously in the SCF ecosystem. A team that completes a focused $40K–$70K award on time, with verifiable on-chain results, is in a far stronger position for a larger follow-up award than a team that proposed an ambitious $150K plan and stalled. The lifetime cap is $150K–$300K — you don't lose access to future funding by starting small. You gain credibility.

---

## Principles for Good Deliverables

### 1. Each deliverable must be verifiable

A reviewer should be able to look at an artifact — a deployed contract, a working URL, a GitHub repo, a video demo — and confirm "yes, this is done." If a deliverable can't be verified from outside your team, rewrite it.

**Weak:** "Build smart contract logic"
**Strong:** "Deploy token-swap Soroban contract to testnet with passing unit tests; share contract address and GitHub repo link"

### 2. Tranche 0 must include a Stellar/Soroban technical component

This is your proof of intent. Reviewers look at this deliverable closely. It must show that your team can interact with Stellar or Soroban technically — not just produce a design doc.

**Good Tranche 0 deliverables:**
- Deploy a basic Soroban smart contract to testnet that implements your core operation
- Build a working prototype that reads from / writes to the Stellar network
- Create an SDK integration proof-of-concept with a working code sample

**Bad Tranche 0 deliverables:**
- "Research and planning phase"
- "Write technical specification"
- "Set up development environment"

### 3. Each tranche should build visibly on the last

Reviewers should see a clear progression: intent, then working core, then testable product, then production-ready launch. Avoid deliverables that jump ahead or repeat previous work.

**Good progression:**
- T0: Soroban contract deployed to testnet with core function
- T1: MVP app with wallet connection, contract interaction, and basic UI
- T2: Full feature set on testnet, shared with community on Discord for feedback
- T3: Mainnet deployment with onboarding flow, documentation, and usage dashboard

**Bad progression:**
- T0: "Research"
- T1: "Continue development"
- T2: "More development"
- T3: "Launch"

### 4. Deliverables should be scoped to the tranche timeline

Each tranche represents roughly 4-6 weeks of work. If a single deliverable would take 3 months, it's too big — break it down. If you have 10 deliverables for a single tranche, consolidate.

### 5. Include the verification method

For each deliverable, state how a reviewer will confirm it's done. This builds trust and speeds up tranche approval.

| Deliverable | Verification |
|------------|-------------|
| Soroban contract on testnet | Contract address + GitHub link |
| Wallet integration working | Screen recording or live demo URL |
| Testnet launch | Testable URL shared in Discord |
| Mainnet deployment | Mainnet contract address + working app URL |
| User onboarding flow | Video walkthrough or live demo |

---

## How to Break Down a Project

### Step 1: Define your end state

What does "done" look like at mainnet launch? Write that down first.

### Step 2: Identify the core Stellar/Soroban interaction

This is the technical heart of your project. It goes in Tranche 0 or Tranche 1.

### Step 3: Work backward from mainnet

- Mainnet (T3): What must be true for users to use your product on mainnet? UX readiness, documentation, onboarding.
- Testnet (T2): What must be testable? Full feature set, community feedback.
- MVP (T1): What's the minimum that demonstrates your core value proposition works?
- Proof of intent (T0): What's the smallest technical proof that your Stellar integration is real?

### Step 4: Assign 2-4 deliverables per tranche

Keep each tranche focused. Two to four deliverables per tranche is the sweet spot. Each should be independently verifiable.

---

## Integration Track Deliverable Example

**Project:** Remittance app integrating Stellar anchor for USD-to-PHP corridor

| Tranche | Deliverables |
|---------|-------------|
| **T0 (10%)** | 1. Working prototype connecting to anchor's SEP-31 API, sending a test transaction. GitHub repo link. 2. Architecture diagram showing user flow from deposit to payout. |
| **T1 (20%)** | 1. MVP mobile app with wallet creation, KYC flow stub, and anchor deposit initiation. 2. End-to-end transaction on testnet from USD deposit to PHP payout (screen recording). |
| **T2 (30%)** | 1. Full-featured testnet app with KYC, transaction history, and fee display. 2. Testable build shared in Stellar Discord for community feedback. 3. Integration test suite covering anchor API edge cases. |
| **T3 (40%)** | 1. Mainnet deployment with live anchor connection. 2. Onboarding flow with in-app tutorial and FAQ. 3. Public landing page with documentation. 4. Dashboard showing transaction volume and user count. |

## Open Track Deliverable Example

**Project:** Soroban-based lending protocol

| Tranche | Deliverables |
|---------|-------------|
| **T0 (10%)** | 1. Core lending-pool Soroban contract deployed to testnet with deposit/withdraw functions and passing tests. Contract address + GitHub repo. 2. Protocol design doc with interest rate model and liquidation logic. |
| **T1 (20%)** | 1. Full smart contract suite (lending pool, oracle adapter, liquidation bot) on testnet with integration tests. 2. Basic frontend for deposit, borrow, and repay operations. |
| **T2 (30%)** | 1. Complete testnet deployment with all contracts, frontend, and SDK. 2. Security review (internal or external audit report). 3. Testable URL shared with community, feedback incorporated. |
| **T3 (40%)** | 1. Mainnet deployment of all contracts. 2. Production frontend with onboarding, documentation, and risk disclaimers. 3. SDK published to npm. 4. Liquidity bootstrap plan and initial pool metrics. |

---

## Common Mistakes

| Mistake | Why It Hurts |
|---------|-------------|
| "Continue development" as a deliverable | Unverifiable. Tells the reviewer nothing. |
| No Stellar component in T0 | Fails the proof-of-intent check. Likely rejected at prescreen. |
| All the hard work in T3 | Signals that earlier tranches are filler. Reviewers want to see progressive value. |
| 8+ deliverables in one tranche | Suggests the scope is too large or the work isn't properly organized. |
| Deliverables that overlap tranches | Makes it unclear what triggers each tranche release. Keep boundaries clean. |
| No verification method mentioned | Forces the reviewer to guess how to confirm completion. Slows down tranche approval. |
| Design docs as the only T0 deliverable | Reviewers need to see code interacting with Stellar, not just plans. |

---

## Checklist Before You Submit

- [ ] T0 includes a technical deliverable that interacts with Stellar or Soroban
- [ ] Each tranche has 2-4 concrete, verifiable deliverables
- [ ] Each deliverable states how a reviewer can confirm it's done
- [ ] Tranches show clear progression (intent -> core -> testable -> live)
- [ ] T3 includes UX readiness (onboarding, documentation, usability)
- [ ] No deliverable says "continue development" or "further research"
- [ ] Budget per tranche aligns with the work described
- [ ] Timeline per tranche is realistic (4-6 weeks each)
