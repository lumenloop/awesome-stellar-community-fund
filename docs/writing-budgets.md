# Writing Your Budget

> How to build a credible, proportional budget for your SCF Build Award application. Budget is one of the most common areas where submissions lose reviewer confidence — this guide shows you how to get it right.

## Why Budget Matters

Reviewers evaluate whether your budget is proportional to scope, realistic for the deliverables, and tied to concrete work. An inflated budget signals that a team is optimizing for grant extraction rather than building. A budget that's too low suggests the team doesn't understand what the work actually requires. Both are red flags.

The maximum Build Award is $150,000 in XLM. Requesting the maximum is not inherently wrong, but it triggers higher scrutiny. Teams that request less than the max and justify every dollar tend to score better.

---

## Tip: Consider Starting Smaller

You can request whatever amount your project genuinely needs — there's no penalty for asking for $150K if the scope justifies it. That said, proposals with a tighter scope and a smaller ask tend to be easier to evaluate and more likely to get funded, especially for teams without an existing SCF track record.

**Why smaller and easier-to-execute proposals do well:**

- **They're easier to say yes to.** A focused $50K proposal with clear deliverables is a simpler decision for reviewers than a sprawling $150K plan with many moving parts.
- **You build trust through execution.** Returning applicants who shipped their prior award cleanly get faster review and stronger trust signals. Reputation compounds.
- **You reduce your own risk.** A tighter scope means fewer things can go wrong. You ship, you learn, you adjust before committing to more.
- **You don't lose access to future funding.** The lifetime cap is $150K–$300K. Starting with a smaller award and coming back with traction data for a second award is a well-worn path.

**Something to consider:** What's the smallest version of your project that demonstrates real value on Stellar? If you can ship that in 3-4 months and show users, you'll be in a strong position to come back for more — with data instead of promises.

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

**A note on tranches:** The tranche names — MVP, Testnet, Mainnet — are the official names, but they each represent three applicant-defined milestones. You decide what the specific deliverables are within each tranche. "MVP" doesn't have to mean a traditional minimum viable product, and "Testnet" doesn't have to mean your only deliverable is a testnet deployment. What matters is that each tranche represents a meaningful, verifiable step forward that you define — progressively building toward a live, usable product.

| Tranche | % of Budget | What the Money Covers |
|---------|-------------|----------------------|
| T0 (10%) | $X | POC development, initial architecture |
| T1 / MVP (20%) | $X | Core features working: first meaningful build |
| T2 / Testnet (30%) | $X | Feature-complete build, testable, community feedback |
| T3 / Mainnet (40%) | $X | Production launch, UX readiness, docs, monitoring |

The percentages are fixed (10/20/30/40), so your deliverables per tranche should justify receiving that share. If T0 only requires a weekend of work, your budget may be too high overall.

---

## Budget Ranges from Funded Projects

The following statistics are drawn from 215 funded Build Award submissions across SCF rounds. Use them to calibrate your request — not as targets to hit, but as context for what reviewers have approved.

### By Category

| Category | Median Budget | 25th Percentile | 75th Percentile | Count |
|---|---|---|---|---|
| Applications | $85,000 | $60,000 | $118,000 | 100 |
| Developer Tooling | $75,000 | $35,000 | $99,000 | 33 |
| Financial Protocols | $109,000 | $94,000 | $144,000 | 39 |
| Infrastructure & Services | $116,000 | $62,000 | $143,000 | 40 |

### By Budget Range

| Range | Number of Funded Projects |
|---|---|
| Under $25K | 5 |
| $25K – $50K | 28 |
| $50K – $75K | 39 |
| $75K – $100K | 48 |
| $100K – $125K | 39 |
| $125K – $150K | 56 |

**What this tells you:** There's no single "right" number. Developer tooling projects frequently get funded in the $35K–$75K range. Financial protocols and infrastructure tend to run higher. The most common range overall is $75K–$100K, but plenty of focused projects succeed at $25K–$50K. Request what your scope requires — reviewers are more concerned with proportionality than the absolute number.

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

## More Budget Examples from Funded Projects

The examples below are modeled on budget patterns from funded Build Award submissions. They show different approaches for different project types and sizes.

### Developer Tooling — Small Scope ($47K)

**Project:** Game engine SDK for Soroban integration

| Category | Item | Budget |
|---|---|---|
| Engineering | SDK development and contract testing | $25,000 |
| Documentation | Tutorials and community support materials | $10,000 |
| Design | UI, demo game creation | $7,000 |
| Operations | Project management, testing, hosting, release | $5,000 |
| | **Total** | **$47,000** |

**Per-tranche breakdown:**

| Tranche | Budget | Breakdown |
|---|---|---|
| T1 / MVP | $18,000 | Engineering $10K, Docs $3K, Design $3K, PM $2K |
| T2 / Testnet | $17,000 | Engineering $10K, Docs $3K, Design $2K, PM $2K |
| T3 / Mainnet | $12,000 | Engineering $5K, Docs $4K, Design $2K, PM $1K |

Why this works: Clear four-category split. Each tranche has its own breakdown. Engineering front-loaded in T1/T2, docs and launch costs shift toward T3.

---

### Applications — OSS Platform ($60K)

**Project:** Open-source collaboration hub for Stellar ecosystem

| Tranche | Budget | Breakdown |
|---|---|---|
| T1 / MVP | $30,000 | Development $18K, Escrow integration $7K, Design $3K, Infrastructure $2K |
| T2 / Testnet | $10,000 | QA/testing $5K, Backend optimization $3K, Security improvements $2K |
| T3 / Mainnet | $20,000 | Escrow finalization $6.5K, KYC integration $4K, Backend/hosting $3.5K, UX improvements $4.5K, Post-launch monitoring $1.5K |

Why this works: Tranche budgets match scope — heavy T1 for core build, light T2 for testing, moderate T3 for production features and polish. Every line item is specific.

---

### Infrastructure — CLI/SDK + Platform ($90K)

**Project:** Agricultural traceability platform on Stellar

| Tranche | Budget | Key Roles |
|---|---|---|
| T1 / MVP ($24K) | Lead dev (3 mo): $14K | Backend dev (2 mo): $8K, Testing/docs: $2K |
| T2 / Testnet ($36K) | Lead dev (2 mo): $20K | Stellar integration dev (1.5 mo): $9K, Frontend dev (1 mo): $4K, Infrastructure: $3K |
| T3 / Mainnet ($30K) | Lead dev (2 mo): $18K | DevOps/production: $6K, Partnership integration: $4K, Docs/community: $2K |

Why this works: Role-based breakdown makes rates verifiable. Testnet tranche is the most expensive because it adds the Stellar integration specialist. Infrastructure costs are explicit and small.

---

### Financial Protocols — Lending ($94K)

**Project:** Institutional-grade Lombard lending protocol on Soroban

| Tranche | Budget | Deliverable Costs |
|---|---|---|
| T1 / MVP | $41,050 | Soroban core contracts: $23,240. Oracle/executor simulation: $7,940. Backend API: $9,870 |
| T2 / Testnet | $34,100 | Testnet deployment: $8,890. Oracle/anchor integrations: $18,740. System validation: $6,470 |
| T3 / Mainnet | $18,510 | Mainnet deployment: $8,470. Backend integration: $5,960. Stress testing: $4,080 |

Why this works: Budget is tied to specific deliverables, not abstract categories. Each deliverable has its own cost. The most expensive items (core contracts, oracle integrations) are justified by complexity. Mainnet tranche is lean because the hard technical work is done in T1/T2.

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
