---
name: scf-prescreen-checker
description: "Simulate the SCF prescreen filter on a Build Award application before submission. Use when a team wants to check whether their application would pass or fail the automated prescreening that filters 18.7% of submissions. Checks for completeness, Stellar integration, eligibility, budget issues, and common disqualifiers."
---

# SCF Prescreen Checker

## Overview

Simulates the SCF prescreening process that all non-referred submissions go through before human reviewers see them. Identifies issues that would cause an application to fail at prescreen — the stage where 18.7% of Build Award submissions are eliminated.

## When to Use

- A team has a draft submission and wants to check if it would pass prescreen
- A team wants to understand what causes prescreen failures
- A team is submitting without a referral and wants to maximize their chances of reaching human review

## How Prescreening Works

Non-referred submissions go through AI-powered prescreening that evaluates whether the application meets basic quality and relevance thresholds. Referred submissions bypass this filter entirely.

The most common prescreen failure causes (from historical data):
1. **Incomplete applications** — Missing sections, unanswered fields, broken links
2. **No Stellar integration** — Project could work on any chain or doesn't use Stellar at all
3. **Ineligible teams or proposals** — Sanctioned jurisdictions, duplicate submissions, ineligible project types
4. **Vague or incoherent proposals** — Submission doesn't clearly describe what's being built

Prescreen-failed submissions had an average budget of $103,735 — the highest of any category, suggesting that low-effort, high-ask submissions are common failures.

## Prescreen Simulation

Run through each check. For each item, report: **PASS**, **FLAG** (potential issue), or **FAIL** (likely prescreen failure).

### 1. Completeness Check

| Check | What to Verify |
|---|---|
| Project description | Is there a clear description of what's being built? |
| Problem statement | Is the problem being solved articulated? |
| Target audience | Is the intended user or market defined? |
| Technical approach | Is there any technical detail beyond a concept? |
| Team information | Are team members named with roles? |
| Deliverables | Are deliverables listed for each tranche? |
| Budget | Is a budget provided with any breakdown? |
| Timeline | Are estimated dates or durations included? |
| Links | Do all provided links actually work? Test every one. |
| Track selection | Has the team selected Integration, Open, or RFP? |

**FAIL condition:** Any core section is entirely missing or blank.
**FLAG condition:** A section exists but is vague, minimal, or incomplete.

### 2. Stellar Integration Check

| Check | What to Verify |
|---|---|
| Stellar mentioned | Does the submission explicitly reference Stellar? |
| Specific capabilities | Does it name specific Stellar features (Soroban, SEPs, anchors, asset issuance, etc.)? |
| Essential vs optional | Would this project work equally well without Stellar? |
| Technical specifics | Are there technical details about how Stellar is used (contract design, SDK usage, protocol integration)? |
| On-chain component | Is there an on-chain element, or is Stellar only mentioned in passing? |

**FAIL condition:** Stellar is not mentioned, or the project has no meaningful Stellar dependency.
**FLAG condition:** Stellar is mentioned but feels peripheral or interchangeable with other chains.

### 3. Eligibility Check

| Check | What to Verify |
|---|---|
| Project type | Is this a project type the SCF funds (software, infrastructure, protocol)? Not marketing campaigns, events, or pure research. |
| Team eligibility | No sanctioned jurisdictions or known-ineligible entities? |
| Duplicate submission | Is this the same project submitted under a different name? |
| Prior funding | If previously funded, has the team delivered on past awards? |
| Track fit | Does the project fit the selected track? (Integration Track requires an eligible building block; RFP Track requires addressing a published RFP) |
| Budget range | Is the budget within the Build Award range (up to $150K for first award)? |

**FAIL condition:** Ineligible project type, sanctioned jurisdiction, or clear track mismatch.
**FLAG condition:** Borderline eligibility or unclear track fit.

### 4. Quality Threshold Check

| Check | What to Verify |
|---|---|
| Coherence | Does the submission tell a coherent story from problem to solution to execution plan? |
| Specificity | Are claims specific and concrete, or vague and generic? |
| Technical depth | Is there enough technical detail to evaluate the approach? |
| Budget proportionality | Is the budget roughly proportional to scope (not $150K for a simple frontend)? |
| Writing quality | Is the submission comprehensible? (Not looking for perfection — looking for clarity) |

**FAIL condition:** Submission is incoherent, entirely generic, or clearly AI-generated boilerplate with no project-specific content.
**FLAG condition:** Low specificity or thin technical detail.

### 5. Red Flag Scan

Check for common disqualifiers:

- [ ] Budget over $150K without prior SCF award
- [ ] Large marketing line items
- [ ] No technical deliverable in T1
- [ ] Team members have no verifiable identity or history
- [ ] Project description is copied from another submission or website
- [ ] Submission reads like a whitepaper rather than a grant application
- [ ] Claims of partnerships or integrations with no evidence
- [ ] Token launch as a primary deliverable
- [ ] No Soroban or on-chain component at all

## Output Format

```
## Prescreen Simulation: [Project Name]

### Overall: [LIKELY PASS / AT RISK / LIKELY FAIL]

### Completeness
- Status: [PASS / FLAG / FAIL]
- Issues: [List any missing or incomplete sections]

### Stellar Integration
- Status: [PASS / FLAG / FAIL]
- Issues: [Is Stellar essential or peripheral?]

### Eligibility
- Status: [PASS / FLAG / FAIL]
- Issues: [Any eligibility concerns]

### Quality Threshold
- Status: [PASS / FLAG / FAIL]
- Issues: [Specificity, coherence, depth concerns]

### Red Flags
- [List any triggered red flags]

### Fix Before Submitting
1. [Most critical issue]
2. [Second most critical]
3. [...]

### Prescreen Risk Assessment
[1-2 sentence summary of whether this submission would likely pass automated prescreening and what the team should prioritize fixing]
```

## Scoring Logic

- **LIKELY PASS** — No FAILs, at most 1 FLAG
- **AT RISK** — No FAILs, but 2+ FLAGs
- **LIKELY FAIL** — Any FAIL in Completeness, Stellar Integration, or Eligibility

## What This Does Not Check

This is a prescreen simulation, not a full review. Passing prescreen doesn't mean the application is strong — it means it won't be filtered out before human review. A submission can pass prescreen and still score poorly on:

- Team readiness and credibility
- Traction and demand evidence
- Budget justification and proportionality
- Deliverable quality and verifiability
- Ecosystem commitment and long-term alignment

For a full application review, use the [SCF Reviewer](scf-reviewer.md) skill.

## Reference Guides

- [Tips for Applying](../docs/tips-for-applying.md) — Prescreen statistics and common failure causes
- [SCF 7.0 Guide](../docs/scf-7-guide.md) — Track definitions and eligibility
- [Getting a Referral](../docs/getting-a-referral.md) — How referrals bypass prescreen
- [Interest Form Tips](../docs/interest-form-tips.md) — The first filter before the full application

## Reference Links

- [SCF Handbook](https://communityfund.stellar.org/handbook)
- [Build Track](https://communityfund.stellar.org/build)
- [FAQ](https://communityfund.stellar.org/faq)
