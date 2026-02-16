# Submitting Tranche Deliverables

> You've been funded. Now you need to submit your deliverables at each milestone to unlock your next tranche payment. This guide covers what to include, how to present your work, and how to avoid delays.

## How Tranche Review Works

After your Build Award is approved, funding is released in tranches tied to milestones:

| Tranche | % of Budget | Milestone |
|---------|-------------|-----------|
| T0 | 10% | Paid automatically upon award approval — no deliverables to submit |
| T1 | 20% | MVP |
| T2 | 30% | Testnet (also unlocks Stellar LaunchKit) |
| T3 | 40% | Mainnet + UX readiness |

**T0 (10%) is released when your award is approved** — there are no deliverables to submit for T0. Your first deliverable submission is T1.

For T1, T2, and T3, you submit your deliverables for review. A reviewer checks that you've completed what you promised in your application. If everything checks out, your payment is released. If not, you'll get feedback on what's missing before you can resubmit.

The smoother and clearer your submission, the faster your payment. Ambiguous or incomplete submissions create back-and-forth that delays everyone.

---

## General Principles

### 1. Make It Easy to Verify

Your reviewer wasn't part of your team. They need to confirm your deliverables are done using only what you provide. For each deliverable, give them:

- **What you said you'd deliver** (reference your original application)
- **What you actually delivered** (the artifact)
- **How to verify it** (link, address, recording, or instructions)

If a reviewer has to hunt for evidence or guess whether something is done, your tranche approval will be delayed.

### 2. Map Deliverables to Your Application

Your submission should reference the deliverables from your original application. Don't restructure, rename, or quietly drop deliverables without explanation. If something changed during development (and things do change), explain what changed and why.

**Format:**

| Original Deliverable | Status | Evidence |
|---------------------|--------|----------|
| Deploy escrow contract to testnet | Complete | Contract address: `CXXX...` / [GitHub repo link] |
| Architecture diagram | Complete | [Link to diagram in repo] |
| Wallet integration POC | Complete | [Screen recording link] |

### 3. Show, Don't Just Tell

"We completed the smart contract" is not evidence. A contract address on Stellar Expert is. A link to a GitHub repo with passing tests is. A screen recording of the feature working is. Always provide an artifact a reviewer can inspect.

### 4. Address Deviations

If you deviated from your original plan — different tech stack, changed scope, dropped a deliverable, added something new — explain it. Reviewers understand that plans evolve during development. What they don't accept is unexplained gaps between what you promised and what you delivered.

---

## What to Submit for Each Tranche

### T1 — MVP

This is your first deliverable submission after being funded (T0 is paid on approval with no submission required). Your core functionality should be working. This doesn't need to be polished, but it needs to demonstrate that the fundamental value proposition works on Stellar.

**What reviewers expect:**
- Core feature(s) functional and demonstrable
- Stellar/Soroban integration visible in the working product

**Strong T1 submissions include:**
- Working app or interface (even if rough) with core user flow functional
- Screen recording or live demo URL showing the feature in action
- Smart contracts deployed to testnet with tests
- Brief written summary of what was built, what works, and what's next

**Common T1 delays:**
- No way to see the product working (no demo, no recording, no URL)
- Core Stellar integration isn't visible in the deliverable

### T2 — Testnet

Your product should be feature-complete and testable on testnet. This is also when you unlock the Stellar LaunchKit.

**What reviewers expect:**
- Full feature set deployed to testnet
- Product is testable by someone outside your team
- Quality and stability are reasonable (not constantly crashing)

**Strong T2 submissions include:**
- Testable URL or build that the reviewer can try themselves
- All smart contracts deployed to testnet with addresses listed
- Evidence of community feedback (Discord thread, feedback form responses, beta tester comments)
- Test suite results (unit tests, integration tests)
- Security review or audit report (if applicable — LaunchKit audit credits become available here)

**Common T2 delays:**
- Testnet deployment isn't accessible or is broken
- Major features from the application are missing without explanation
- No evidence of testing beyond the team
- Smart contracts deployed but no interface to interact with them

### T3 — Mainnet + UX Readiness

Your product must be live on mainnet and usable by real users. SCF 7.0 added UX readiness as an explicit requirement — deployment alone is not enough.

**What reviewers expect:**
- All contracts and infrastructure deployed to mainnet
- A functional, usable interface (not a CLI or raw API)
- Onboarding flow that a new user can follow without help
- Basic documentation (FAQ, getting started, or in-app guidance)

**Strong T3 submissions include:**
- Live production URL and mainnet contract addresses
- Screen recording of the full user journey from first visit to completed action
- User-facing documentation (FAQ, help section, getting started guide)
- Evidence of real usage (transaction count, unique wallets, user signups) if available
- Summary of changes since T2 and how community feedback was incorporated

**Common T3 delays:**
- Product is deployed but not usable (broken flows, missing onboarding)
- No documentation of any kind
- UX issues that prevent a reviewer from completing the core action
- Mainnet deployment exists but the interface still points to testnet

See [UX Readiness Guide](ux-readiness.md) for the full T3 UX requirements and checklist.

---

## Submission Format

A clean tranche submission follows this structure:

```
## Tranche [X] Submission: [Project Name]

### Summary
[2-3 sentences: what was accomplished in this tranche]

### Deliverables

| # | Deliverable (from application) | Status | Evidence |
|---|-------------------------------|--------|----------|
| 1 | [Original deliverable text] | Complete | [Link / address / recording] |
| 2 | [Original deliverable text] | Complete | [Link / address / recording] |
| 3 | [Original deliverable text] | Complete | [Link / address / recording] |

### Deviations from Plan
[Any changes from your original application — or "None"]

### Key Links
- GitHub: [link]
- Live app / testnet URL: [link]
- Contract addresses: [list]
- Demo recording: [link]
- Documentation: [link]

### What's Next
[Brief description of the next tranche's goals]
```

---

## Tips for Faster Approval

- **Submit everything at once.** Don't send a partial submission and promise to add links later. Reviewers evaluate what's in front of them.
- **Test your own links.** Before submitting, click every link in your submission. Broken links are the most common avoidable delay.
- **Include contract addresses explicitly.** Don't make reviewers dig through your GitHub to find deployed addresses. List them in the submission.
- **Record a walkthrough.** A 3-5 minute screen recording showing your deliverables working is often the fastest way to demonstrate completion. Tools like Loom or a simple screen capture work fine.
- **Show a diff from the previous tranche.** Especially for T2 and T3, briefly explain what changed since the last milestone. This helps reviewers see progression.
- **Keep your GitHub repo clean.** A clear README, organized code, and meaningful commit history signal professionalism. A repo with no README and 200 uncommitted files does not.
- **Respond to feedback quickly.** If a reviewer flags something, address it within a few days. Submissions that go cold for weeks may need to be re-reviewed entirely.

---

## When Things Change

Development rarely goes exactly as planned. That's fine — but communicate proactively.

### Scope Changes

If you need to change a deliverable (swap one feature for another, adjust the technical approach), explain:
- What changed
- Why it changed
- How the new deliverable still aligns with the project's goals and the SCF's investment

Minor adjustments are normal and usually approved without issue. Major scope changes (dropping a core feature, pivoting the product direction) may require a conversation with the SCF team before your tranche is reviewed.

### Timeline Delays

If you're behind schedule, communicate before your tranche is due — not after. The SCF team works with funded projects and understands that timelines slip. What they don't accept is silence.

### Undelivered Items

If a specific deliverable genuinely can't be completed (dependency issue, technical blocker, changed requirements), explain what happened and what you're doing instead. Don't quietly omit it and hope no one notices — reviewers check against your original application.

---

## Checklist Before You Submit

- [ ] Every deliverable from your application is addressed (completed, modified, or explained)
- [ ] Each deliverable has a verifiable artifact (link, address, recording, or screenshot)
- [ ] All links work (click them yourself before submitting)
- [ ] Contract addresses are listed explicitly (not buried in code)
- [ ] Deviations from the original plan are explained
- [ ] GitHub repo has a clear README and organized structure
- [ ] For T2: testnet deployment is accessible and functional
- [ ] For T3: product is live on mainnet with usable UX and documentation
- [ ] Summary explains what was accomplished and what's next
