# Proving Traction Evidence

> How to demonstrate product-market fit, user demand, and real-world traction in your SCF Build Award application. Traction is one of the most decisive evaluation factors — this guide covers what counts, how to present it, and what to avoid.

## Why Traction Matters

SCF reviewers need to believe that your project will be used. The strongest signal is evidence that it already is — or that clear demand exists. The SCF handbook states that projects must demonstrate they have either "significant user traction" or "a validated need identified by a team or individual experienced in the Stellar ecosystem."

For returning applicants, the bar is higher: you must share "evidence of significant traction from prior funding, ideally onchain metrics."

---

## What Counts as Traction

Traction evidence falls into several categories, ranked roughly from strongest to weakest:

### Tier 1: On-Chain Metrics (Strongest)

Verifiable, tamper-resistant, and the gold standard for SCF reviewers.

- **Transaction volume:** Number and value of transactions over time
- **Unique active wallets:** Daily/weekly/monthly unique addresses interacting with your contracts
- **TVL (Total Value Locked):** For DeFi projects, the value held in your contracts
- **Contract invocations:** How often your Soroban contracts are called
- **Asset holders:** Number of accounts holding your issued asset
- **Liquidity pool participation:** Volume and depth in AMM pools

**How to present:** Link to a Stellar block explorer, a public dashboard, or specific transaction hashes. On-chain data is self-verifying — make it easy for reviewers to check.

### Tier 2: Product Usage Metrics

Real usage data from your application, even if not fully on-chain yet.

- **Monthly active users (MAU):** How many unique users engage with your product each month
- **Retention rates:** What percentage of users return after 1 week, 1 month
- **Session data:** Average sessions per user, time spent
- **Conversion rates:** From signup to first transaction, from free to paid
- **Revenue or payment volume:** If applicable, actual revenue generated

**How to present:** Screenshots of analytics dashboards (Google Analytics, Mixpanel, PostHog, etc.), or a summary table with time periods. If you can't share raw dashboards, a summary with context works.

### Tier 3: Demand Signals

Evidence that people want your product, even if it isn't fully live yet.

- **Waitlist signups:** How many people signed up to be notified
- **Letter of intent from partners:** Written commitments from integration partners, anchor services, or distribution channels
- **Pilot agreements:** Formal or informal agreements to run a pilot
- **Pre-orders or deposits:** Users who've committed money before launch
- **Community engagement:** Active Discord/Telegram members, forum posts, feedback threads

**How to present:** Share screenshots, links, or excerpts. For partner letters, quote the relevant commitment (with permission). Quantify everything you can.

### Tier 4: Market Validation

Evidence that the problem you're solving is real and the market exists.

- **Competitor traction:** Other products solving the same problem have significant users (proves market demand)
- **Industry data:** Reports or statistics showing market size, growth, or unmet need
- **User interviews or surveys:** Structured feedback from potential users confirming the pain point
- **Ecosystem gaps:** Analysis showing no existing Stellar project solves this problem

**How to present:** Cite specific sources. Reference competitor user counts or funding rounds. Summarize interview findings with sample sizes.

---

## How to Structure Traction in Your Submission

### For New Projects (No Live Product)

Focus on demand signals and market validation. The key question is: "Why should we believe people will use this?"

**Structure:**
1. **The problem:** What specific pain point exists? Who feels it?
2. **Market evidence:** How big is this market? What do competitors look like?
3. **Demand signals:** Waitlist numbers, partner LOIs, pilot agreements, community interest
4. **Why Stellar:** Why does solving this on Stellar create unique value?

### For Projects with Existing Users

Lead with your hardest data. The key question is: "Is this growing and will the Stellar integration accelerate it?"

**Structure:**
1. **Current metrics:** MAU, transaction volume, retention — hard numbers with time ranges
2. **Growth trajectory:** Month-over-month or quarter-over-quarter trends
3. **Stellar-specific opportunity:** What the Stellar integration unlocks that you can't do today
4. **Adoption targets:** What metrics you'll hit with SCF funding

### For Returning SCF Applicants

The bar is explicitly higher. You must show what you achieved with prior funding.

**Structure:**
1. **Prior deliverables:** What you built and shipped with your last award
2. **On-chain metrics:** Transaction volume, wallets, TVL — ideally on a public dashboard
3. **User growth since launch:** How your product has grown since mainnet deployment
4. **What's next:** Why additional funding will compound the traction you've demonstrated

---

## Presenting Metrics Effectively

### Be Specific

**Weak:** "We have many users and growing interest."
**Strong:** "1,200 MAU as of January 2026, up from 340 in October 2025. 45% month-over-month growth. 62% of users complete at least one transaction per week."

### Use Time Ranges

Always anchor metrics to a specific date or range. "10,000 transactions" means nothing without knowing if that's per day or since inception.

### Show Trends, Not Just Snapshots

A single number is a snapshot. Two or more data points over time show direction. Include month-over-month or weekly trends wherever possible.

### Compare to Relevant Benchmarks

If your retention rate is 40% at 30 days, compare it to industry norms. If your transaction volume is growing faster than comparable projects, say so.

### Make It Verifiable

Link to public sources wherever possible:
- Block explorers for on-chain data
- Public dashboards (even a simple one on Dune or your own site)
- App store listings with download counts and ratings
- Social media accounts with visible follower counts and engagement

---

## Traction Red Flags Reviewers Watch For

| Red Flag | Why It Hurts |
|----------|-------------|
| No metrics at all | Signals the team hasn't validated demand |
| Vague claims ("significant traction," "strong interest") | Unverifiable. Reviewers discount vague language completely. |
| Metrics from a different product or chain only | Shows traction elsewhere but not that Stellar-specific demand exists |
| Inflated bot traffic | Reviewers check on-chain data. Fake activity is detectable and disqualifying. |
| Token holders as the only metric | Holding a token is not product usage. Show actual product interaction. |
| No adoption targets for post-funding | Tells reviewers you haven't thought about growth |
| Claiming traction from a pump.fun or meme token launch | This is a strong negative signal. Real traction comes from product usage, not speculation. |
| Prior SCF funding with no on-chain metrics to show | For returning applicants, this is nearly disqualifying |

---

## Adoption Targets

Your submission should include forward-looking targets — what you'll achieve with SCF funding. These should be:

- **Specific:** "500 MAU within 3 months of mainnet launch," not "gain users"
- **Measurable:** Tied to a metric you can report on
- **Time-bound:** Anchored to a tranche milestone or calendar date
- **Realistic:** Based on your current trajectory, not wishful thinking
- **On-chain where possible:** "100 unique wallets interacting with our contract weekly" is stronger than "1,000 app downloads"

---

## Examples

### Strong Traction Section (Existing Product)

> Our remittance app currently serves 2,400 MAU across 3 corridors (US-PH, US-MX, US-NG). Transaction volume has grown from $45K/month in Q3 2025 to $180K/month in Q4 2025. User retention at 30 days is 58%, and average transaction frequency is 2.3x per month. Our NPS score is 67. We have LOIs from two additional anchor partners to expand to 5 corridors. On-chain transaction data is publicly viewable at [explorer link]. With SCF funding, we target 5,000 MAU and $500K/month transaction volume within 6 months of the Stellar integration launch.

### Strong Traction Section (New Project)

> No comparable Soroban-native lending protocol exists today. The closest on-chain alternatives on other chains (Aave on Ethereum, MarginFi on Solana) have combined TVL exceeding $8B, demonstrating massive market demand. We've surveyed 120 Stellar DeFi users via the Stellar Discord and found that 78% want to borrow against their XLM holdings without bridging to another chain. We have 430 waitlist signups collected over 6 weeks through our landing page. StellarX and [Partner Name] have provided letters of intent to list our lending pools on their interfaces. Post-launch target: $2M TVL within 90 days of mainnet deployment.

---

## Checklist Before You Submit

- [ ] Traction evidence is specific, quantified, and time-bound
- [ ] On-chain metrics are linked to a verifiable source (block explorer, dashboard)
- [ ] Growth trends are shown, not just single snapshots
- [ ] Adoption targets are included with specific numbers and timelines
- [ ] No vague language ("significant," "strong," "many") without backing numbers
- [ ] For returning applicants: on-chain metrics from prior funding are included
- [ ] For new projects: demand signals or market validation are concrete
- [ ] Claims are verifiable — a reviewer could check them independently
