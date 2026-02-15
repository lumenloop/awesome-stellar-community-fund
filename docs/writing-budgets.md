# Writing Your Budget

> How to build a credible, proportional budget for your SCF Build Award application. Budget is one of the most common areas where submissions lose reviewer confidence — this guide shows you how to get it right.

## Why Budget Matters

Reviewers evaluate whether your budget is proportional to scope, realistic for the deliverables, and tied to concrete work. An inflated budget signals that a team is optimizing for grant extraction rather than building. A budget that's too low suggests the team doesn't understand what the work actually requires. Both are red flags.

The maximum Build Award is $150,000 in XLM. Requesting the maximum is not inherently wrong, but it triggers higher scrutiny. Teams that request less than the max and justify every dollar tend to score better.

---

## Build a Bottom-Up Budget

The strongest budgets are built from the bottom up: start with the work, estimate what it costs, and arrive at a total. Do not start with a number and reverse-engineer line items to justify it.

### Step 1: List Your Deliverables by Tranche

Pull directly from your milestone plan:

| Tranche | Deliverables |
|---------|-------------|
| T0 (10%) | Soroban contract POC, architecture doc |
| T1 (20%) | MVP app with wallet integration, basic UI |
| T2 (30%) | Full testnet deployment, integration tests, community feedback |
| T3 (40%) | Mainnet launch, onboarding UX, docs, dashboard |

### Step 2: Estimate Effort Per Deliverable

For each deliverable, estimate the hours or weeks of work and the role doing it:

| Deliverable | Role | Effort | Rate | Cost |
|------------|------|--------|------|------|
| Soroban contract POC | Smart contract dev | 2 weeks | $4,000/wk | $8,000 |
| Architecture doc | Lead engineer | 1 week | $3,500/wk | $3,500 |
| MVP frontend | Frontend dev | 3 weeks | $3,000/wk | $9,000 |
| Wallet integration | Full-stack dev | 2 weeks | $3,500/wk | $7,000 |
| ... | ... | ... | ... | ... |

### Step 3: Add Non-Labor Costs

Include infrastructure, services, and tooling — but only if they're real:

| Item | Monthly Cost | Duration | Total |
|------|-------------|----------|-------|
| RPC node (dedicated) | $200/mo | 6 months | $1,200 |
| Cloud hosting | $150/mo | 6 months | $900 |
| Domain + SSL | — | — | $50 |

### Step 4: Sum and Sanity-Check

Add up all line items. Then ask:
- Does the total feel proportional to what I'm building?
- Would I pay this amount if it were my own money?
- Can I explain every line item to a reviewer in one sentence?

If the total is significantly less than $150K, that's fine — request what you need. Smaller, well-justified budgets are viewed favorably.

---

## Budget Categories

Organize your budget into clear categories. Here's a standard structure:

### Development (typically 60-75% of budget)
- Smart contract development (Soroban)
- Frontend/UI development
- Backend/API development
- Integration work (SDK, SEP, anchor connections)
- Testing and QA

### Design and UX (typically 5-15%)
- UI/UX design
- User research and testing
- Onboarding flow design
- Brand/visual design (if needed)

### Infrastructure (typically 5-10%)
- Cloud hosting
- RPC/Horizon node costs
- CI/CD pipeline
- Monitoring and alerting tools

### Security (typically 5-10%)
- Smart contract audit (note: LaunchKit provides audit credits at T2 — factor this in)
- Penetration testing
- Security review

### Operations and Other (typically 0-10%)
- Documentation
- Community management
- Legal (if needed for compliance)
- Contingency (keep this small — 5% max — or omit)

---

## How to Tie Budget to Tranches

Your budget should map cleanly to the tranche structure. Reviewers check that the percentage of budget in each tranche matches the scope of work.

| Tranche | % of Budget | What the Money Covers |
|---------|-------------|----------------------|
| T0 (10%) | $X | POC development, initial architecture |
| T1 (20%) | $X | MVP build: core features, basic UI |
| T2 (30%) | $X | Full feature build, testnet deployment, testing, community feedback |
| T3 (40%) | $X | Mainnet launch, UX polish, docs, onboarding, monitoring setup |

The percentages are fixed (10/20/30/40), so your deliverables per tranche should justify receiving that share. If T0 only requires a weekend of work, your budget may be too high overall.

---

## Rate Benchmarks

Reviewers have seen hundreds of budgets. Rates that are wildly above market for the work described raise flags. Here are rough benchmarks (varies by region and experience):

| Role | Reasonable Range (Weekly) |
|------|--------------------------|
| Smart contract developer (Soroban/Rust) | $2,500 – $5,000 |
| Full-stack developer | $2,000 – $4,000 |
| Frontend developer | $1,500 – $3,500 |
| UI/UX designer | $1,500 – $3,000 |
| DevOps / infrastructure | $2,000 – $4,000 |
| Project lead / architect | $3,000 – $5,000 |

These are not hard rules. If your team is in a high-cost market, higher rates are fine — just be transparent. If you're charging $8,000/week for frontend work with no justification, reviewers will flag it.

---

## Common Mistakes

| Mistake | Why It Hurts |
|---------|-------------|
| Requesting $150K for a simple integration | Signals grant extraction. Right-size to scope. |
| Round numbers with no breakdown | "$50,000 for development" tells reviewers nothing. |
| No per-tranche budget mapping | Reviewers can't verify if tranche payments match the work. |
| Paying for "research" in T0 | T0 is proof of intent. The money should fund technical work, not planning. |
| Including "marketing" as a major line item | SCF funds building, not marketing. Small community/docs budget is fine. Large marketing spend is a red flag. |
| Double-counting LaunchKit benefits | If you'll get audit credits through LaunchKit at T2, don't also budget $30K for an audit. |
| Massive contingency buffer | More than 5% contingency looks like padding. |
| No team rates or effort estimates | A budget without rates and hours is a guess, not a plan. |
| Identical rates for all roles | Different roles have different market rates. Flat rates suggest the budget wasn't built bottom-up. |

---

## Budget for Returning Applicants

If you've received prior SCF funding, reviewers expect:
- Clear accounting of how prior funds were used
- Evidence that deliverables from prior tranches were completed
- A budget that reflects lessons learned (not a copy-paste of last time)
- Justification for why additional funding is needed beyond the initial award

The lifetime cap is $150K standard, with up to $300K case-by-case for projects with significant traction.

---

## Example: Well-Structured Budget

**Project:** Cross-border payment app integrating Stellar anchor (USD-PHP corridor)
**Total request:** $85,000

| Category | Item | Effort | Rate | Cost |
|----------|------|--------|------|------|
| **Development** | Soroban contract (escrow + settlement) | 4 weeks | $4,000/wk | $16,000 |
| | Backend API (Node.js) | 6 weeks | $3,000/wk | $18,000 |
| | Mobile app (React Native) | 8 weeks | $3,000/wk | $24,000 |
| | Anchor SEP-31 integration | 3 weeks | $3,500/wk | $10,500 |
| **Design** | UI/UX design + onboarding flows | 3 weeks | $2,500/wk | $7,500 |
| **Infrastructure** | Dedicated RPC node (6 mo) | — | $200/mo | $1,200 |
| | Cloud hosting (6 mo) | — | $300/mo | $1,800 |
| **Security** | Internal security review | 1 week | $4,000/wk | $4,000 |
| | (External audit via LaunchKit at T2) | — | — | $0 |
| **Operations** | Documentation + API docs | 1 week | $2,000/wk | $2,000 |
| | | | **Total** | **$85,000** |

**Tranche mapping:**

| Tranche | Budget | Work Covered |
|---------|--------|-------------|
| T0 (10%) | $8,500 | Soroban escrow contract POC on testnet, architecture finalized |
| T1 (20%) | $17,000 | MVP mobile app with wallet, basic anchor deposit flow |
| T2 (30%) | $25,500 | Full testnet app, KYC, tx history, community testing, security review |
| T3 (40%) | $34,000 | Mainnet launch, onboarding UX, docs, monitoring dashboard |

---

## Checklist Before You Submit

- [ ] Budget is built bottom-up from deliverables, not top-down from a target number
- [ ] Every line item has a role, effort estimate, and rate
- [ ] Budget maps to tranches with matching scope
- [ ] Total is proportional to scope (not inflated to hit $150K)
- [ ] Non-labor costs are specific and realistic
- [ ] LaunchKit benefits (audit credits, etc.) are factored in and not double-counted
- [ ] No large "marketing" or "contingency" buckets
- [ ] For returning applicants: prior funding usage is addressed
