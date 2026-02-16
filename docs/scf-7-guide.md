# SCF 7.0 Guide

> Stellar Community Fund v7.0 launched in January 2026. This guide covers every track, what changed from prior versions, and best practices for applying.

## Table of Contents

- [What Is the SCF?](#what-is-the-scf)
- [SCF 7.0 Tracks](#scf-70-tracks)
  - [Integration Track](#1-integration-track)
  - [Open Track](#2-open-track)
  - [RFP Track](#3-rfp-track)
  - [Instawards](#4-instawards)
- [Award Amounts and Funding Structure](#award-amounts-and-funding-structure)
- [How to Apply](#how-to-apply)
- [What Changed from Previous Versions](#what-changed-from-previous-versions)
  - [SCF 7.0 vs 6.0](#scf-70-vs-60)
  - [Brief History (1.0 through 6.0)](#brief-history-10-through-60)
- [Evaluation Criteria](#evaluation-criteria)
- [Best Practices by Track](#best-practices-by-track)
  - [Integration Track Tips](#integration-track-tips)
  - [Open Track Tips](#open-track-tips)
  - [RFP Track Tips](#rfp-track-tips)
  - [General Best Practices (All Tracks)](#general-best-practices-all-tracks)
- [Post-Launch Support](#post-launch-support)
- [Links](#links)

---

## What Is the SCF?

The [Stellar Community Fund](https://communityfund.stellar.org) (SCF) is an open-application awards program run by the Stellar Development Foundation. It distributes grants in XLM to teams building meaningful products, services, and infrastructure on Stellar and Soroban. For over six years the SCF has funded hundreds of projects across payments, DeFi, developer tooling, and real-world asset use cases.

---

## SCF 7.0 Tracks

SCF 7.0 reorganizes the Build Award into three specialized tracks, plus a decentralized early-stage program:

### 1. Integration Track

**Who it's for:** Teams building an end-user application whose primary purpose is to integrate a specific Stellar ecosystem building block — a DeFi protocol, wallet SDK, anchor service, or other ready-to-use component — into a product that serves real users.

**Critical distinction:** The Integration Track is a grant *for* an integration. It is not an Open Track submission that happens to mention an integration partner. The integration partner and the building block being integrated must be the central focus of the project. Reviewers evaluate whether the partner is relevant, whether the integration is substantive, and whether the end product delivers the building block's value to users. If your project is a novel protocol or tool that merely touches an existing component, it belongs in the Open Track instead.

- Reviewed by a quarterly-rotating panel of SCF Pilot delegates.
- The specific building blocks and use cases eligible for the Integration Track are decided by quarterly (and ad hoc) community votes. Check the current list before applying.
- Ideal for fintech apps, neobanks, remittance platforms, and other end-user products that leverage existing Stellar infrastructure rather than building new primitives from scratch.
- The integration partner should be named, active in the Stellar ecosystem, and directly relevant to the project's core functionality.

### 2. Open Track

**Who it's for:** Experienced teams building novel financial protocols, on-chain primitives, or functionality that pushes the Stellar ecosystem forward. No requirement to integrate a pre-defined building block.

- Submissions are evaluated for ecosystem impact, originality, and technical soundness.
- Final award decisions are made through community vote (using Neural Quorum Governance).
- Ideal for new DeFi protocols, bridges, oracle networks, novel smart contract patterns, and composable infrastructure.

### 3. RFP Track

**Who it's for:** Developers responding to an active SCF Request for Proposals — specific **developer tooling and infrastructure** that have been identified as strategic gaps.

- RFPs target dev tooling needs: SDKs, indexers, testing frameworks, and other developer infrastructure.
- Submissions are reviewed and selected by a panel of SCF Pilot delegates with relevant technical and domain expertise.

### 4. Instawards

**Who it's for:** Very early-stage teams that aren't yet ready for a full Build Award.

- A decentralized evolution of the former SCF Kickstart program.
- Regional Stellar Ambassador chapters can recommend projects for small awards of **up to $15K** per project.
- Supports early experimentation, prototyping, and local pilots.
- All award decisions remain subject to SDF review and approval.
- Designed to feed the Build Award pipeline: teams that mature through Instawards can later apply for a full Build Award.

---

## Award Amounts and Funding Structure

### Build Award (Integration, Open, and RFP Tracks)

- **Maximum:** Up to **$150,000 in XLM** per award.
- **Duration:** Intended to cover approximately 6 months of development costs through mainnet launch.
- **Lifetime cap:** Up to $150K across all awards. Projects exceeding this may be eligible for additional funding on a case-by-case basis, up to a $300K lifetime maximum.
- **XLM valuation:** Calculated using the CF Stellar Lumens-Dollar Settlement Price on the payment date, not at the time of application.

### Milestone-Based Tranches

Funding is distributed across four milestones to incentivize execution:

| Tranche | % of Budget | Milestone |
|---------|-------------|-----------|
| Tranche 0 | 10% | Paid on award approval — no deliverables required |
| Tranche 1 | 20% | MVP deliverable complete |
| Tranche 2 | 30% | Testnet launch (also unlocks Stellar LaunchKit) |
| Tranche 3 | 40% | Mainnet launch with UX readiness |

**T0 is an upfront payment.** The 10% T0 tranche is released when your award is approved (after passing community vote). You do not submit deliverables for T0 — your first deliverable submission is T1.

**Important change in 7.0:** The final tranche now requires **UX readiness** — clear onboarding flows, functional and tested interfaces, and basic usability validation. Mainnet deployment alone is no longer sufficient.

### Stellar LaunchKit

Build Award recipients unlock the Stellar LaunchKit at the Testnet milestone, which can include:

- Audit credits
- UX audits and user testing
- Infrastructure offers
- Connections to accelerators and other SDF funding mechanisms

---

## How to Apply

1. **Submit the Interest Form** at [communityfund.stellar.org](https://communityfund.stellar.org). All new projects start here.
2. **Eligibility review.** A panel evaluates your submission for potential value to the Stellar ecosystem, eligibility, and team capability.
3. **Invitation to Build Award round.** If you pass, you may be invited to submit a full Build Award application in an upcoming round.
4. **Full submission.** Fill out the Build Award form on the SCF website. You can save progress and return.
5. **Prescreening.** SCF team members review your submission at a high level. Referred submissions receive expedited handling.
6. **Panel or community review.** Depending on the track:
   - Integration and RFP: Reviewed by a delegate panel.
   - Open: Goes to community vote via Neural Quorum Governance.
7. **Award and tranche disbursement.** Approved projects receive Tranche 0 and begin building toward milestones.

### Referral Pathway (New in 7.0)

Trusted ecosystem participants — Pilots and SDF staff — can refer incoming teams. Referred teams receive:

- Stronger trust signals during review
- Faster time-to-decision
- Referrers earn recognition and financial incentives tied to team success

Teams without referrals enter the standard pipeline and go through AI-based prescreening that filters low-signal submissions.

### Build Award Rounds

Rounds run approximately every **6 weeks**. Check [communityfund.stellar.org/awards](https://communityfund.stellar.org/awards) for current deadlines.

---

## What Changed from Previous Versions

### SCF 7.0 vs 6.0

| Area | SCF 6.0 | SCF 7.0 |
|------|---------|---------|
| **Tracks** | Single Build Award track | Three specialized tracks: Integration, Open, RFP |
| **Early-stage support** | Kickstart (5-day bootcamp, up to $15K) | Instawards (decentralized, ambassador-led, up to $15K) |
| **Intake process** | Direct submission to Build Award rounds | Interest Form first, then invitation to Build Award round |
| **Referral system** | None | Verified referral pathway with incentives |
| **Prescreening** | Manual review only | AI-powered prescreening for non-referred submissions |
| **Tranche structure** | Milestone-based (MVP, Testnet, Mainnet) | Four explicit tranches: 10% / 20% / 30% / 40% |
| **Final milestone** | Mainnet deployment | Mainnet deployment **plus UX readiness** |
| **Post-launch support** | Limited (LaunchKit, accelerator connections) | Growth Hack program, BD support, liquidity grants, public good funding, investment access |
| **Lifetime funding cap** | Up to $150K | Up to $150K standard, up to $300K case-by-case |
| **Governance** | Category Delegate Panels | Track-specific panels + community vote for Open Track |

### Brief History (1.0 through 6.0)

| Version | Era | Key Innovation |
|---------|-----|----------------|
| **1.0** (Rounds 1-5) | 2019-2020 | Replaced centralized Build Challenge with community voting. 12M XLM/year distributed quarterly. |
| **2.0** (Rounds 6-7) | 2020-2021 | Split into Lab Fund (small experiments) and Seed Fund (scaling companies). Panel-driven selection. |
| **3.0** (Rounds 8-11) | 2021-2022 | Iterative community feedback loops. Awards up to $100K. |
| **4.0** (Rounds 12-19) | 2022-2023 | Soroban era. 10% Proof of Intent upfront, 90% after community vote. Rapid round cadence. |
| **5.0** (Rounds 20+) | 2023-2024 | Activation Award + Community Award model. Neural Quorum Governance introduced. |
| **6.0** | 2024-2025 | Merged into single Build Award (up to $150K). Kickstart bootcamp. Category Delegate Panels. LaunchKit. |
| **7.0** | 2026-present | Three specialized tracks. Instawards. Referral system. AI prescreening. UX readiness gate. Growth Hack. |

---

## Evaluation Criteria

Review panels assess submissions across three high-level dimensions:

1. **Potential value to the Stellar or Soroban ecosystem** — Does this project create lasting, composable value? Does it fill a gap?
2. **Eligibility and alignment with SCF goals** — Is Stellar core to the project (not bolted on)? Does the team meet all eligibility requirements?
3. **Team capability and readiness** — Can this team execute? Do they have relevant experience, especially with Stellar or Soroban?

### Prescreen Criteria

Before reaching the review panel, submissions must clear prescreening:

- Submission is complete and coherent.
- Project is building on Stellar and/or Soroban.
- Stellar plays a core and valuable role (not shoehorned).
- Team is not ineligible (e.g., no outstanding unfulfilled grants, no Matching/Enterprise Fund investments).
- Budget is within limits and reasonable for scope.

### What Reviewers Look For

- Deep understanding of Stellar and Soroban.
- Clear technical architecture with specifics on how Stellar/Soroban is used.
- Evidence of product-market fit or validated need.
- Named, credible team members with relevant experience.
- Realistic, proportional budget tied to concrete deliverables.
- First deliverable includes a technical component interacting with Stellar/Soroban.
- Uniqueness — if competitors exist, clear differentiation.
- Self-contained submission that doesn't require external context.

---

## Best Practices by Track

### Integration Track Tips

1. **Understand what this track is.** The Integration Track is a grant *for* an integration. Your project's core value proposition must be delivering an existing Stellar building block to end users. If you're building a novel protocol that happens to touch an existing component, apply to the Open Track instead.
2. **Name your integration partner explicitly.** State which building block you're integrating, who built it, and confirm it's on the current quarter's eligible list. Reviewers reject submissions with vague or peripheral partners.
3. **Know the building blocks.** Research which ecosystem components (DeFi protocols, wallet SDKs, anchor services) are eligible for the current quarter. The list changes based on community votes — check it before you write your application.
4. **Show the integration architecture.** Include diagrams or specs showing exactly how you connect to the Stellar component. Reviewers want to see that you understand the SDK/API, not just the concept.
5. **Demonstrate end-user value.** This track rewards applications that put Stellar functionality in the hands of real users. Show your target audience, their pain point, and how the integration solves it.
6. **Highlight existing traction.** If you already have users on another chain or platform, quantify them. The panel wants evidence that integrating Stellar will serve real demand, not speculative interest.
7. **Don't over-scope.** Keep your proposal focused on the integration itself and the user experience around it. You're incorporating an existing solution, not building new primitives.

### Open Track Tips

1. **Lead with ecosystem impact.** Community voters decide Open Track awards. Frame your project in terms of what it unlocks for other builders and users on Stellar — composability and ecosystem-level value matter.
2. **Demonstrate technical depth.** Open Track proposals are expected to be highly technical. Include smart contract architecture, Soroban usage details, protocol design, and security considerations.
3. **Differentiate clearly.** If anything similar exists on Stellar or other chains, explain precisely why your approach is better, different, or uniquely suited to Stellar's architecture.
4. **Show Soroban-native design.** Projects that treat Soroban as a core component (not a wrapper around off-chain logic) are much stronger. Explain how your smart contracts work and why Soroban's capabilities (e.g., resource metering, state archival) matter for your design.
5. **Engage the community early.** Since the Open Track goes to community vote, building relationships in the Stellar Developer Discord and sharing your thinking before you submit can significantly help your proposal's reception.

### RFP Track Tips

1. **Respond to the specific RFP.** Don't repurpose a general proposal. Address every requirement listed in the active RFP and explain how you meet each one.
2. **Prove relevant expertise.** The panel selecting RFP submissions includes technical domain experts. Show prior work in the specific area the RFP targets (e.g., if it's an indexer RFP, show your experience with indexing infrastructure).
3. **Focus on developer experience.** Most RFPs target developer tooling and infrastructure. Prioritize usability, documentation quality, and maintenance plans alongside raw functionality.
4. **Include a maintenance plan.** Infrastructure and tooling need ongoing upkeep. Address how you'll maintain and support the tool beyond initial development — this is a common weak spot in RFP submissions.
5. **Be realistic about timeline.** RFP projects are scoped to fill identified gaps quickly. A tight, credible timeline beats an ambitious one.

### General Best Practices (All Tracks)

**Before you write:**

- **Study Stellar and Soroban deeply.** One of the most common reviewer complaints is that applicants haven't done their homework. Understand Stellar's consensus model, asset issuance, SEPs, and Soroban's smart contract model before writing a word.
- **Research the ecosystem.** Know your competitors, potential partners, and existing projects. Check the [awards page](https://communityfund.stellar.org/awards) for previously funded projects in your space.
- **Join the Stellar Developer Discord.** Ask questions in #scf-general. Get feedback on your idea before submitting. Build relationships with community members who may later vote on your proposal or refer you.

**Writing your submission:**

- **Make Stellar's role unmistakable.** Your submission must show that Stellar and/or Soroban plays a core, valuable role — not a tacked-on afterthought. Reviewers specifically look for whether the project could work equally well without Stellar; if yes, that's a red flag.
- **Be technically detailed.** Include architecture diagrams, process flows, contract design, and code samples or GitHub links. The more specific you are, the more credible you appear.
- **Explain why your team can execute.** Name your team members. List relevant experience. Prior Stellar/Soroban work is a strong signal. Building on other chains also counts.
- **Right-size your budget.** Don't request $150K if you can ship for $60K. Reviewers notice when budgets are inflated. Build a bottom-up cost breakdown tied to your roadmap.
- **Nail Tranche 0 / your first deliverable.** The first deliverable must include a technical component that interacts directly with Stellar or Soroban. It serves as your proof of intent, and reviewers evaluate it closely.
- **Separate your tranches clearly.** Each tranche (MVP, Testnet, Mainnet) should have concrete, verifiable deliverables. Vague milestones like "continue development" will hurt your application.
- **Make the submission self-contained.** Reviewers only evaluate what's in the submission form. Don't assume they'll check your website, GitHub, or social media unless you link to specific artifacts and explain their relevance inline.

**After you submit:**

- **Seek a referral.** If you know Pilots or SDF staff, ask them to refer you through the verified referral pathway. This gives your application a trust signal and faster review.
- **Prepare for UX readiness.** Remember that the final tranche now requires functional interfaces and usable onboarding — not just a mainnet deployment. Plan for UX from the start, not as an afterthought.
- **Plan for growth.** SCF 7.0 offers post-launch support for teams that demonstrate traction. Think beyond launch: what are your adoption targets, growth loops, and metrics?

---

## Post-Launch Support

SCF 7.0 extends well beyond the initial Build Award for teams that ship and gain traction:

- **Growth Hack** — Targeted funding and support for user acquisition experiments and repeatable growth loops.
- **Liquidity Grants** — Funding to bootstrap liquidity for DeFi protocols and trading pairs on Stellar.
- **Public Good Funding** — Support for open-source infrastructure, public goods, and ecosystem-wide tooling.
- **BD and go-to-market support** — Strategic introductions and go-to-market sprint assistance.
- **Agency, distribution, and investment access** — Introductions to marketing partners, ecosystem distribution channels, and investor networks.
- **Additional Build Awards** — After completing all tranches, teams with significant traction can apply for subsequent awards.

Only projects with **live mainnet deployments and verifiable on-chain usage** qualify for post-launch support.

---

## Links

- [SCF Website](https://communityfund.stellar.org)
- [SCF Awards / Apply](https://communityfund.stellar.org/awards)
- [SCF Handbook](https://stellar.gitbook.io/scf-handbook)
- [SCF 7.0 Announcement](https://stellar.org/blog/ecosystem/introducing-scf-v7)
- [SCF v6.0 Announcement](https://stellar.org/blog/developers/introducing-stellar-community-fund-v6-0)
- [Submission Best Practices (Blog)](https://stellar.org/blog/ecosystem/stellar-community-fund-soroban-submission-best-practices)
- [SCF FAQ](https://stellar.gitbook.io/scf-handbook/additional-support/faq)
- [Stellar Grants and Funding](https://stellar.org/grants-and-funding)
- [Stellar Developer Discord](https://discord.gg/stellardev)
