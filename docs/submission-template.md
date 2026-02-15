# SCF Build Award Submission Template

> A fill-in-the-blank template connecting all the guides in this repo into one coherent application draft. Use this as a starting structure, then refer to the individual guides for depth on each section.

## How to Use This Template

1. Fill in each section with your project's specifics.
2. Use the linked guide for detailed advice on each section.
3. Delete all instructional text (in brackets) before submitting.
4. Have someone outside your team read the finished submission — if they can't understand your project in one pass, revise.

This template covers the key sections of a Build Award application. The actual SCF form may have additional or slightly different fields — always follow the form's structure, but use this to draft your content.

---

## Project Overview

**Project name:** [Your project name]

**One-line description:** [What your project does in one sentence — problem + solution + Stellar's role]

**Track:** [Integration / Open / RFP]

**For Integration Track:** Integration partner: [Name of building block / partner]. Eligible list confirmed: [Yes/No — check the current quarter's list]

**For RFP Track:** Responding to RFP: [Title and link to the specific RFP]

---

## Problem Statement

[2-3 paragraphs describing:]
- [What specific problem exists? Who feels it?]
- [How big is this problem? Quantify if possible (market size, number of affected users, cost of the current solution)]
- [Why hasn't this been solved yet, or why are existing solutions inadequate?]

---

## Solution

[2-3 paragraphs describing:]
- [What you're building and how it solves the problem above]
- [Why Stellar and/or Soroban is essential to your solution — what specific capabilities does it provide? See: [SCF 7.0 Guide](scf-7-guide.md)]
- [What makes your approach unique or better than alternatives?]

**For Integration Track:** [Explain what the building block provides and what you build on top of it. The integration should be the core of your value proposition, not a peripheral feature. See: [SCF 7.0 Guide — Integration Track](scf-7-guide.md#1-integration-track)]

---

## Technical Architecture

> See: [Technical Architecture Guide](technical-architecture.md) for detailed best practices

### System Overview

[High-level diagram or structured description of all major components and how they interact]

**Components:**
- Frontend: [Technology, what it does]
- Backend: [Technology, what it does, or "N/A — client-side only"]
- Smart contracts: [Soroban contracts — list each one and its purpose]
- Stellar integration: [SEPs implemented, asset model, account structure]
- External dependencies: [Anchors, oracles, partner APIs]

### Stellar/Soroban Integration Details

[Detailed explanation of how your project uses Stellar and/or Soroban]

**For Soroban projects:**
- Contract 1: [Name] — [Purpose, key functions, state managed]
- Contract 2: [Name] — [Purpose, key functions, state managed]
- On-chain vs off-chain: [What data lives where and why]
- State archival strategy: [How you handle TTL-based expiration]

**For Stellar-native projects (SEPs, payments, assets):**
- SEPs implemented: [Which ones and why]
- Asset strategy: [Existing asset vs new issuance, trustlines]
- Account model: [Custodial vs non-custodial, multisig setup]

**For Integration Track:**
- Building block: [Name and provider]
- Integration points: [Exact SDK/API calls and how they connect to your app]
- What the building block provides vs what you build: [Clear separation]

### Data Flow

[End-to-end walkthrough of your primary user action]

```
User does [action]
  -> [Step 1: what happens in your frontend]
  -> [Step 2: what happens in your backend / contract]
  -> [Step 3: what happens on the Stellar network]
  -> [Step 4: result returned to user]
```

### Security

- Key management: [How private keys are stored and handled]
- Access control: [Who can call which functions, admin controls]
- Audit plan: [Internal review, external audit, LaunchKit audit credits]
- Known risks and mitigations: [Relevant attack vectors for your project type]

### Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | [e.g., React, React Native] |
| Smart Contracts | [e.g., Soroban / Rust] |
| Backend | [e.g., Node.js, or N/A] |
| Database | [e.g., PostgreSQL, or on-chain only] |
| RPC | [Public Horizon / dedicated node] |
| Auth | [e.g., SEP-10, OAuth, etc.] |

---

## Team

> Reviewers specifically look for named, credible team members with relevant experience.

| Name | Role | Relevant Experience | Links |
|------|------|-------------------|-------|
| [Full name] | [Role] | [Prior Stellar/Soroban work, relevant domain experience, years of experience] | [GitHub, LinkedIn, portfolio] |
| [Full name] | [Role] | [Experience] | [Links] |
| [Full name] | [Role] | [Experience] | [Links] |

**Prior Stellar/Soroban experience:** [Describe any previous Stellar work — prior SCF awards, open-source contributions, mainnet deployments]

**Prior blockchain experience:** [If no Stellar experience, describe work on other chains]

---

## Traction

> See: [Proving Traction Guide](proving-traction.md) for detailed best practices

### Current Metrics (if applicable)

| Metric | Value | Time Period |
|--------|-------|-------------|
| Monthly active users | [Number] | [Month/Year] |
| Transaction volume | [Amount] | [Period] |
| Growth rate | [%] | [MoM or QoQ] |
| Retention (30-day) | [%] | [Period] |

**Verification:** [Links to block explorer, public dashboard, app store listing, or other verifiable source]

### Demand Signals (if pre-launch)

- [Waitlist signups: number and collection period]
- [Partner commitments: named partners with specific commitments]
- [User interviews: number conducted, key findings]
- [Community interest: Discord members, forum engagement, social following]

### Adoption Targets (post-funding)

| Milestone | Target | Timeline |
|-----------|--------|----------|
| Testnet launch (T2) | [e.g., 50 beta testers, community feedback collected] | [Date] |
| Mainnet launch (T3) | [e.g., 500 MAU, $50K monthly tx volume] | [Date] |
| 3 months post-launch | [e.g., 2,000 MAU, 3 new corridors] | [Date] |

---

## Deliverables and Milestones

> See: [Writing Deliverables Guide](writing-deliverables.md) for detailed best practices

### Tranche 0 — Proof of Intent (10%)

**Deliverables:**
1. [Technical deliverable that interacts with Stellar/Soroban — e.g., "Deploy escrow contract to testnet with passing tests"]
   - Verification: [How a reviewer confirms this — e.g., "Contract address + GitHub repo link"]
2. [Second deliverable if applicable]
   - Verification: [Method]

**Timeline:** [Estimated weeks]

### Tranche 1 — MVP (20%)

**Deliverables:**
1. [Core feature deliverable — e.g., "Working app with wallet connection and basic transaction flow"]
   - Verification: [Method]
2. [Second deliverable]
   - Verification: [Method]

**Timeline:** [Estimated weeks]

### Tranche 2 — Testnet Launch (30%)

**Deliverables:**
1. [Full feature set on testnet — e.g., "Complete testnet deployment with all core features"]
   - Verification: [Method]
2. [Community testing — e.g., "Testable build shared in Stellar Discord"]
   - Verification: [Method]
3. [Quality assurance — e.g., "Integration test suite with >80% coverage"]
   - Verification: [Method]

**Timeline:** [Estimated weeks]

### Tranche 3 — Mainnet + UX Readiness (40%)

> See: [UX Readiness Guide](ux-readiness.md) for T3 requirements

**Deliverables:**
1. [Mainnet deployment — e.g., "All contracts deployed to mainnet, app live at production URL"]
   - Verification: [Method]
2. [UX readiness — e.g., "Onboarding flow with in-app tutorial, error handling, FAQ"]
   - Verification: [Method]
3. [Documentation — e.g., "User docs and API reference published"]
   - Verification: [Method]
4. [Metrics — e.g., "Public dashboard showing transaction volume and user count"]
   - Verification: [Method]

**Timeline:** [Estimated weeks]

---

## Budget

> See: [Writing Budgets Guide](writing-budgets.md) for detailed best practices

### Cost Breakdown

| Category | Item | Effort | Rate | Cost |
|----------|------|--------|------|------|
| Development | [e.g., Soroban contract development] | [X weeks] | [$X/wk] | [$X] |
| Development | [e.g., Frontend build] | [X weeks] | [$X/wk] | [$X] |
| Development | [e.g., Backend / API] | [X weeks] | [$X/wk] | [$X] |
| Design | [e.g., UI/UX design] | [X weeks] | [$X/wk] | [$X] |
| Infrastructure | [e.g., RPC node, hosting] | [X months] | [$X/mo] | [$X] |
| Security | [e.g., Internal review] | [X weeks] | [$X/wk] | [$X] |
| | | | **Total** | **$[X]** |

### Budget by Tranche

| Tranche | Amount | Work Covered |
|---------|--------|-------------|
| T0 (10%) | $[X] | [Summary of T0 work] |
| T1 (20%) | $[X] | [Summary of T1 work] |
| T2 (30%) | $[X] | [Summary of T2 work] |
| T3 (40%) | $[X] | [Summary of T3 work] |

---

## Ecosystem Fit

[1-2 paragraphs answering:]
- [How does this project benefit the broader Stellar ecosystem?]
- [Does it create composable value that other projects can build on?]
- [What's your long-term commitment to Stellar? (vs chain-hopping risk)]
- [Are there existing Stellar projects in this space? If so, how are you different?]

---

## Competitors and Differentiation

| Competitor | Chain | What They Do | How You Differ |
|-----------|-------|-------------|----------------|
| [Name] | [Chain] | [Brief description] | [Your differentiation] |
| [Name] | [Chain] | [Brief description] | [Your differentiation] |

---

## Post-Launch Plan

[Brief description of your plan after mainnet launch:]
- [Growth targets for 3-6 months post-launch]
- [User acquisition strategy]
- [Maintenance and support plan]
- [Interest in SCF post-launch programs: Growth Hack, Launch Weeks, etc.]

---

## Pre-Submission Checklist

> Run through this before you hit submit.

- [ ] **Problem:** Clearly stated, specific, quantified
- [ ] **Solution:** Stellar's role is essential (not swappable)
- [ ] **Architecture:** Detailed, with diagrams, data flows, and security section
- [ ] **Team:** Named members with relevant experience and links
- [ ] **Traction:** Specific metrics or concrete demand signals
- [ ] **Deliverables:** 2-4 per tranche, verifiable, with T0 including Stellar/Soroban technical work
- [ ] **Budget:** Bottom-up, proportional, mapped to tranches
- [ ] **UX readiness:** Planned for in T3 deliverables
- [ ] **Self-contained:** Submission makes sense without visiting external links
- [ ] **Track:** Correct track selected (Integration, Open, or RFP)
- [ ] **For Integration Track:** Partner named, building block is central, on current eligible list
- [ ] **Referral:** Secured if possible
