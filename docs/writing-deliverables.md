# Writing and Structuring Deliverables

> How to break your SCF Build Award application into clear, verifiable milestone deliverables that reviewers trust and panels can approve quickly.

## Why Deliverables Matter

SCF funding is released in four tranches tied to milestones. Reviewers evaluate your deliverables to determine whether your plan is realistic, whether progress can be verified, and whether each tranche unlocks meaningful work. Vague or poorly structured deliverables are one of the most common reasons submissions are scored down or rejected.

---

## The Four-Tranche Framework

Every Build Award distributes funding across these milestones:

| Tranche | Budget | Milestone | What You Prove |
|---------|--------|-----------|---------------|
| 0 | 10% | Award approval | Paid automatically when your award is approved — no deliverables to submit |
| 1 | 20% | MVP | Core Stellar/Soroban integration works |
| 2 | 30% | Testnet | Product is testable end-to-end |
| 3 | 40% | Mainnet + UX readiness | Product is live, usable, and discoverable |

**T0 is not a deliverable milestone.** The 10% T0 payment is released upon award approval (after passing community vote). You do not submit deliverables for T0. Your first deliverable submission is T1.

**A note on tranches:** MVP, Testnet, and Mainnet are the official tranche names, but they each represent applicant-defined milestones. You decide what the specific deliverables are within each tranche. "MVP" doesn't have to mean a traditional minimum viable product, and "Testnet" doesn't have to be exclusively about a testnet deployment. What matters is that each tranche represents a meaningful, verifiable step forward — the deliverables within it should fit your project, not be forced into rigid categories.

Your job is to define concrete deliverables for T1, T2, and T3 that a reviewer can verify without ambiguity.

### Tip: Consider Tightening Your Scope

You can scope your deliverables to whatever your project genuinely requires. That said, before you plan, it's worth asking: **could I tighten this?** Proposals with fewer, more focused deliverables are easier to evaluate and more likely to get funded. A smaller, well-executed award also builds the trust and track record that make follow-up awards much easier to get. The lifetime cap is $150K–$300K, so starting focused doesn't close any doors — it opens them with data instead of promises.

---

## Principles for Good Deliverables

### 1. Each deliverable must be verifiable

A reviewer should be able to look at an artifact — a deployed contract, a working URL, a GitHub repo, a video demo — and confirm "yes, this is done." If a deliverable can't be verified from outside your team, rewrite it.

**Weak:** "Build smart contract logic"
**Strong:** "Deploy token-swap Soroban contract to testnet with passing unit tests; share contract address and GitHub repo link"

### 2. Each tranche should build visibly on the last

Reviewers should see a clear progression from T1 through T3: working core, then testable product, then production-ready launch. Avoid deliverables that jump ahead or repeat previous work.

**Good progression:**
- T1: Soroban contract deployed to testnet with core function, MVP app with wallet connection and basic UI
- T2: Full feature set on testnet, shared with community on Discord for feedback
- T3: Mainnet deployment with onboarding flow, documentation, and usage dashboard

**Bad progression:**
- T1: "Continue development"
- T2: "More development"
- T3: "Launch"

### 3. Deliverables should be scoped to the tranche timeline

Each tranche represents roughly 4-6 weeks of work. If a single deliverable would take 3 months, it's too big — break it down. If you have 10 deliverables for a single tranche, consolidate.

### 4. Include the verification method

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

This is the technical heart of your project. It should be front and center in your T1 deliverables.

### Step 3: Work backward from mainnet

- Mainnet (T3): What must be true for users to use your product on mainnet? UX readiness, documentation, onboarding.
- Testnet (T2): What must be testable? Full feature set, community feedback.
- MVP (T1): What's the minimum that demonstrates your core value proposition works on Stellar?

### Step 4: Assign 2-4 deliverables per tranche

Keep each tranche focused. Two to four deliverables per tranche is the sweet spot. Each should be independently verifiable.

---

## How to Format Each Deliverable

Funded Build Award submissions consistently use a structured format for each deliverable. This makes it easy for reviewers to evaluate and speeds up tranche approval. Use this format:

> **Deliverable N — [Name]**
> - **Description:** What you will build or deliver.
> - **Completion criteria:** How a reviewer confirms it's done — the specific artifact or metric.
> - **Estimated completion:** Date or duration.
> - **Budget:** Cost for this deliverable.

This format comes directly from how successful applicants across rounds 28–40 structured their submissions. Reviewers expect it. Projects that use vague prose instead of structured deliverables consistently score lower.

---

## Verification Methods Reference

Different types of deliverables call for different proof. Here's an expanded reference drawn from patterns in funded projects:

| Deliverable Type | Strong Verification Methods |
|---|---|
| Smart contract deployment | Testnet/mainnet contract address + GitHub repo with source code + passing test suite |
| SDK or library | Published package (npm, crates.io, PyPI) + GitHub repo + documentation site |
| Frontend / app | Live URL or testable build + screen recording or demo video |
| API or backend service | API endpoint URL + documentation + example requests/responses |
| Integration with external service | End-to-end transaction demo (screen recording or live URL) showing the full flow |
| Mobile app | Testable build (TestFlight / APK) + screen recording of core flows |
| Security review or audit | Published audit report (or summary with auditor named) |
| Documentation | Published docs URL with table of contents |
| Community testing | Testable URL shared in Discord + collected feedback report |
| Performance / load testing | Benchmark report with metrics (throughput, latency, error rates) |

---

## Examples by Category

The examples below are modeled on patterns from funded Build Award submissions across SCF rounds. They are not SCF 7 submissions, but the deliverable structure and expectations carry over directly.

### Applications — Fintech / Payments

**Pattern:** Remittance or payment app integrating Stellar anchors, wallets, or stablecoin rails.

**Tranche 1 — MVP** ($36,000)

1. **Stellar asset integration**
   - **Description:** Integrate XLM and Stellar USDC for deposits, withdrawals, and conversion to fiat currencies with same-day payouts.
   - **Completion criteria:** Successful end-to-end deposit, conversion, and local fiat withdrawal on testnet.
   - **Estimated completion:** 2 weeks.
   - **Budget:** $10,000

2. **Card funding via Stellar USDC**
   - **Description:** Enable Stellar USDC deposits to fund payment cards (virtual + physical).
   - **Completion criteria:** User funds a card with Stellar USDC and completes a transaction. Screen recording.
   - **Estimated completion:** 2 weeks.
   - **Budget:** $20,000

3. **QA, compliance, and production rollout**
   - **Description:** Finalize AML/KYC adjustments for Stellar assets, perform QA, deploy production release.
   - **Completion criteria:** All Stellar transactions processed live and fully compliant.
   - **Estimated completion:** 0.5 weeks.
   - **Budget:** $6,000

**Tranche 2 — Testnet** ($40,000)

1. **Partner API for ecosystem projects**
   - **Description:** Develop API allowing Stellar-based projects to issue co-branded cards funded with Stellar USDC.
   - **Completion criteria:** Partner project successfully issues a card, funds with Stellar USDC, and executes a transaction.
   - **Estimated completion:** 3 weeks.
   - **Budget:** $20,000

2. **Mobile app MVP (iOS + Android)**
   - **Description:** Mobile app enabling onboarding, KYC, Stellar wallet setup, card management, and fiat conversion.
   - **Completion criteria:** User completes KYC, activates Stellar wallet, funds card, and spends. Testable builds shared.
   - **Estimated completion:** 4 weeks.
   - **Budget:** $20,000

**Tranche 3 — Mainnet** ($13,500)

1. **Payment rails API integration**
   - **Description:** Integrate payment rails API to enable Stellar USDC to fiat conversion and local payouts in expanded regions.
   - **Completion criteria:** Successful user deposit and withdrawal via supported payout rails on mainnet.
   - **Estimated completion:** 2.5 weeks.
   - **Budget:** $13,500

---

### Financial Protocols — DeFi / Lending

**Pattern:** On-chain lending, escrow, or trading protocol built on Soroban.

**Tranche 1 — MVP** ($41,050)

1. **Soroban core contracts**
   - **Description:** Develop and deploy Loans, LPPool, PolicyRegistry, and LiquidationManager contracts on Soroban localnet. Implement event emissions and inter-contract calls.
   - **Completion criteria:** All contracts deploy and interact via CLI and integration tests. Full loan creation and liquidation logic operational in simulation.
   - **Estimated completion:** 6 weeks.
   - **Budget:** $23,240

2. **Oracle and executor simulation**
   - **Description:** Implement mock oracle adapter (BTC/USD, USDC/USD) and prototype off-chain executor for liquidation receipts.
   - **Completion criteria:** Mock price updates trigger liquidations; receipts acknowledged on-chain. Full liquidation flow runs in simulation.
   - **Estimated completion:** 2 weeks.
   - **Budget:** $7,940

3. **Backend API integration**
   - **Description:** Build lightweight backend API to manage borrower positions (borrow, repay, liquidation) and connect with Soroban contracts.
   - **Completion criteria:** End-to-end user flow (borrow / repay / liquidation trigger) validated locally.
   - **Estimated completion:** 2 weeks.
   - **Budget:** $9,870

**Tranche 2 — Testnet** ($34,100)

1. **Testnet deployment**
   - **Description:** Deploy complete smart contract suite to Stellar testnet with configured governance and admin roles.
   - **Completion criteria:** All modules callable via testnet RPC, verified through end-to-end test transactions.
   - **Estimated completion:** 1.5 weeks.
   - **Budget:** $8,890

2. **Oracle and anchor integrations**
   - **Description:** Integrate DIA/Reflector oracles and implement SEP-10/12/24 for authentication, KYC, and fiat off-ramp.
   - **Completion criteria:** Borrower completes verified end-to-end flow — KYC, loan, fiat transfer, repayment — on testnet with live oracle data.
   - **Estimated completion:** 3 weeks.
   - **Budget:** $18,740

3. **System validation**
   - **Description:** Scenario tests covering interest accrual, liquidation thresholds, and anchor synchronization.
   - **Completion criteria:** All tests pass under expected network conditions; performance metrics logged and verified.
   - **Estimated completion:** 1.5 weeks.
   - **Budget:** $6,470

**Tranche 3 — Mainnet** ($18,510)

1. **Mainnet contract deployment**
   - **Description:** Deploy final Soroban contracts to mainnet with updated parameters and verified governance.
   - **Completion criteria:** Core interactions (borrow, repay, partial liquidation) execute without errors on mainnet.
   - **Estimated completion:** 1.5 weeks.
   - **Budget:** $8,470

2. **Mainnet backend integration**
   - **Description:** Connect backend to mainnet contracts, enable live oracle feeds, synchronize custody records.
   - **Completion criteria:** Stable live operations for 7 consecutive days with no desync or transaction failures.
   - **Estimated completion:** 1.5 weeks.
   - **Budget:** $5,960

3. **Stress testing and validation**
   - **Description:** Mainnet load testing under varying network conditions.
   - **Completion criteria:** Performance benchmarks (throughput, latency) meet predefined thresholds.
   - **Estimated completion:** 1 week.
   - **Budget:** $4,080

---

### Developer Tooling — SDKs and Plugins

**Pattern:** Open-source SDK, plugin, or developer tool for the Stellar/Soroban ecosystem.

**Tranche 1 — MVP** ($18,000)

1. **Core SDK structure and testnet connection**
   - **Description:** Core SDK (e.g., C# Soroban client), connection to testnet contracts, basic transaction and read/write functionality. Internal demo project for proof of concept.
   - **Completion criteria:** GitHub alpha release + demo video. SDK successfully performs testnet transactions.
   - **Estimated completion:** 8 weeks.
   - **Budget:** $18,000 (Engineering $10K, Docs $3K, Design/demo $3K, PM/testing $2K)

**Tranche 2 — Testnet** ($17,000)

1. **Wallet and integration templates**
   - **Description:** Wallet connection + transaction signing. NFT minting and token management examples.
   - **Completion criteria:** Beta release + working Unity sample scenes. All examples run on testnet.
   - **Estimated completion:** 8 weeks.
   - **Budget:** $17,000 (Engineering $10K, Docs $3K, Design $2K, PM/testing $2K)

**Tranche 3 — Mainnet** ($12,000)

1. **Documentation site and public launch**
   - **Description:** Public documentation site and tutorials. Community outreach via Stellar/Soroban dev channels. SDK published (e.g., Unity Asset Store, npm).
   - **Completion criteria:** Public SDK v1.0 launch + outreach report. Docs live at public URL.
   - **Estimated completion:** 8 weeks.
   - **Budget:** $12,000 (Engineering $5K, Docs $4K, Design $2K, PM $1K)

---

### Infrastructure — Platform / API Services

**Pattern:** Hosted service, monitoring tool, or API infrastructure for the Stellar network.

**Tranche 1 — MVP** ($24,000)

1. **Core CLI/SDK with authentication and workspace management**
   - **Description:** CLI tool with auth (login/logout/refresh), workspace management (init/status/config), and core data operations.
   - **Completion criteria:** Package installable + documentation available. Two external systems integrated (whitelisted partners).
   - **Estimated completion:** Month 3.
   - **Budget:** $24,000 (Lead dev 3 mo: $14K, Backend dev 2 mo: $8K, Testing/docs: $2K)

**Tranche 2 — Testnet** ($36,000)

1. **Stellar integration and testnet deployment**
   - **Description:** Selective disclosure features, receipt system, governance smart contract on Stellar testnet, proof-of-concept tokenization, web dashboard for non-technical users.
   - **Completion criteria:** Circuit governance contract deployed on testnet. Web dashboard accessible. Public API documentation published.
   - **Estimated completion:** Month 4.
   - **Budget:** $36,000 (Lead dev: $20K, Stellar integration dev: $9K, Frontend: $4K, Infra: $3K)

**Tranche 3 — Mainnet** ($30,000)

1. **Production deployment and community framework**
   - **Description:** Platform live on Stellar mainnet. Framework released for community developers. Partner integrations live. Monitoring and support infrastructure.
   - **Completion criteria:** Platform operational on mainnet. Performance validated with 1,000+ items across 10+ circuits. Developer docs published. Example apps available.
   - **Estimated completion:** Month 6.
   - **Budget:** $30,000 (Lead dev: $18K, DevOps: $6K, Partnerships: $4K, Docs/community: $2K)

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
