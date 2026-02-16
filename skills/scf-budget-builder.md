---
name: scf-budget-builder
description: "Build bottom-up budgets for SCF Build Award applications. Use when a team needs help constructing a proportional, justified budget with role-based rates, per-deliverable cost breakdowns, and tranche mapping. Produces a complete budget section with line items, effort estimates, and tranche allocation based on patterns from 215 funded Build Awards."
---

# SCF Budget Builder

## Overview

Walks teams through constructing a bottom-up budget for their SCF Build Award application. Starts from deliverables, estimates effort and cost for each, maps to tranches, and validates against funded project benchmarks.

## When to Use

- A team has deliverables defined but no budget yet
- A team has a top-down number ("we need $100K") but no breakdown
- A team wants to validate whether their budget is proportional to scope
- A team needs help mapping budget to the 4-tranche structure

## Process

### Step 1: Inventory Deliverables

List every deliverable across all four tranches. If the team doesn't have deliverables yet, help them define them first using the [Writing Deliverables Guide](../docs/writing-deliverables.md).

For each deliverable, identify:
- What type of work it requires (smart contract dev, frontend, backend, design, testing, documentation)
- What roles are needed
- Rough complexity (simple, moderate, complex)

### Step 2: Estimate Effort

For each deliverable, estimate effort by role:

| Deliverable | Role | Effort |
|---|---|---|
| Soroban lending contracts | Senior Soroban dev | 4 weeks |
| Soroban lending contracts | Security reviewer | 1 week |
| Frontend dashboard | Frontend dev | 3 weeks |
| API integration layer | Backend dev | 2 weeks |

**Estimation tips:**
- Soroban contract development: 2–6 weeks for moderate complexity
- Frontend development: 2–4 weeks per major interface
- Backend/API work: 1–3 weeks per integration
- Testing and QA: 15–25% of development time
- Documentation: 1–2 weeks for comprehensive docs
- Add 10–15% buffer for integration testing and iteration

### Step 3: Apply Rates

Use market-appropriate rates. Benchmarks from funded projects:

| Role | Typical Range | Notes |
|---|---|---|
| Senior Soroban/smart contract dev | $3,500–$5,500/week | Higher end for specialized DeFi/protocol work |
| Backend developer | $2,500–$4,500/week | Depends on complexity and experience |
| Frontend developer | $2,500–$4,000/week | React/Next.js typical stack |
| Full-stack developer | $3,000–$4,500/week | Common for smaller teams |
| UI/UX designer | $2,000–$3,500/week | Often part-time or per-deliverable |
| DevOps / infrastructure | $2,500–$4,000/week | Often part-time across tranches |
| Technical writer | $1,500–$2,500/week | Documentation-heavy deliverables |
| Project management | $1,500–$2,500/week | Usually partial allocation |

**Rate guidance:**
- Rates should reflect the team's actual geography and experience level
- Unusually high rates without justification are a red flag
- Unusually low rates raise questions about team quality or commitment
- Blended team rates are acceptable if broken down per deliverable

### Step 4: Build the Budget Table

Produce a per-deliverable breakdown:

```
### Budget Breakdown

| Tranche | Deliverable | Role | Rate | Effort | Cost |
|---|---|---|---|---|---|
| T0 | Soroban contract MVP | Senior dev | $4,500/wk | 3 weeks | $13,500 |
| T0 | Testnet deployment | Senior dev | $4,500/wk | 1 week | $4,500 |
| T1 | Backend API | Backend dev | $3,500/wk | 3 weeks | $10,500 |
| T1 | Frontend prototype | Frontend dev | $3,000/wk | 2 weeks | $6,000 |
| ... | ... | ... | ... | ... | ... |

**Total: $XX,XXX**
```

### Step 5: Map to Tranches

SCF Build Awards use a 10% / 20% / 30% / 40% tranche structure:

| Tranche | % of Total | Purpose |
|---|---|---|
| T0 | 10% | Proof of intent — technical deliverable on Stellar/Soroban |
| T1 | 20% | Core build — primary development work |
| T2 | 30% | Feature complete — full functionality, audit readiness |
| T3 | 40% | Production ready — mainnet, UX, documentation, launch |

**Mapping rules:**
- T0 budget should be ~10% of total. If T0 work costs more, redistribute other tranches
- T3 is the largest tranche and should include UX readiness, documentation, and launch work
- Each tranche should have enough budget to cover its deliverables
- The tranche amounts don't need to be exact percentages — close is fine

Produce a tranche summary:

```
### Tranche Allocation

| Tranche | Budget | % of Total | Key Deliverables |
|---|---|---|---|
| T0 | $X,XXX | ~10% | [Deliverable names] |
| T1 | $XX,XXX | ~20% | [Deliverable names] |
| T2 | $XX,XXX | ~30% | [Deliverable names] |
| T3 | $XX,XXX | ~40% | [Deliverable names] |
| **Total** | **$XX,XXX** | **100%** | |
```

### Step 6: Validate

Check the budget against these benchmarks:

**Budget ranges by category (from 215 funded Build Awards):**

| Category | Median | Middle 50% Range |
|---|---|---|
| Applications | $85,000 | $55K–$115K |
| Developer Tooling | $75,000 | $47K–$100K |
| Financial Protocols | $109,000 | $80K–$147K |
| Infrastructure | $116,000 | $75K–$149K |

**Red flags to check:**
- [ ] Total exceeds $150K without strong justification (lifetime cap is $150K–$300K)
- [ ] Any line item over 40% of total budget without explanation
- [ ] Marketing line items (SCF funds building, not marketing)
- [ ] External audit budget that duplicates LaunchKit credits (available at T2)
- [ ] Contingency or miscellaneous line items over 5%
- [ ] Rates significantly above benchmarks without justification
- [ ] Top-down budget that doesn't trace back to deliverables
- [ ] Budget is significantly higher than category median without proportional scope

**Strengths to confirm:**
- [ ] Every line item traces to a specific deliverable
- [ ] Rates and effort are explicit for each item
- [ ] Tranche allocation roughly follows 10/20/30/40
- [ ] Budget is proportional to scope complexity
- [ ] LaunchKit benefits factored in (audit credits at T2)
- [ ] No ineligible expenses

## Output Format

Produce three sections:

1. **Per-Deliverable Budget Table** — Every line item with role, rate, effort, cost, mapped to tranche
2. **Tranche Allocation Summary** — Per-tranche totals with key deliverables listed
3. **Budget Notes** — Any assumptions, justifications for above-median amounts, LaunchKit considerations, and flagged concerns

## What Not to Do

- **Don't start from a target number and work backward.** Always build bottom-up from deliverables.
- **Don't pad the budget.** Rejected submissions average higher budgets ($102K) than funded ones ($93K). Right-sizing wins.
- **Don't include marketing.** Small documentation and community budgets are fine. Large marketing line items are not.
- **Don't forget LaunchKit.** Build Award recipients unlock audit credits and other resources at T2. Don't budget separately for things LaunchKit covers.
- **Don't use vague line items.** "Development: $50,000" tells reviewers nothing. Break it down.

## Reference Guides

- [Writing Budgets](../docs/writing-budgets.md) — Full budget construction guide with statistics and funded examples
- [Writing Deliverables](../docs/writing-deliverables.md) — Deliverable structuring (budgets trace to deliverables)
- [Tips for Applying](../docs/tips-for-applying.md) — Budget right-sizing advice
- [Submission Template](../docs/submission-template.md) — Where the budget section fits in the full application

## Reference Links

- [SCF Handbook](https://communityfund.stellar.org/handbook)
- [Build Track](https://communityfund.stellar.org/build)
- [FAQ](https://communityfund.stellar.org/faq)
