# Tips for a Winning SCF Application

> Practical advice for getting your Stellar Community Fund Build Award application funded. Based on panelist feedback, patterns from 1,048 Build Award submissions (212 awarded, 515 rejected, 196 prescreen failures), and insights from the Stellar community.

---

## The Numbers You Should Know

Before you start writing, understand the landscape:

- **20.2% of Build Award submissions get funded.** Four out of five don't.
- **18.7% fail at prescreen** — rejected before a reviewer ever sees them. Common causes: incomplete submissions, no Stellar integration, ineligible teams.
- **Rejected submissions had higher average budgets ($102K)** than awarded ones ($93K). Asking for more doesn't help — right-sizing to scope does.
- **The median funded Build Award is $93,700.** The middle 50% fall between $60K and $128K.

These aren't meant to discourage you. They're meant to show that the bar is real and that the advice below directly addresses why 80% of applications don't make it.

---

## 1. Be Crystal Clear About What You're Building

The most common reason proposals lose reviewer confidence is ambiguity. If a panelist has to guess what your project does, who it's for, or why Stellar matters, you've already lost points.

**Define the problem first.** A specific pain point for a specific audience beats a broad vision. "Cross-border payments are slow" is too vague. "Freelancers in Latin America wait 3–5 days and pay 5–8% fees to receive USD payments from US clients" is specific and testable.

**Make Stellar's role unmistakable.** Reviewers specifically check whether your project could work equally well without Stellar. If it could, that's a red flag. Explain exactly which Stellar capabilities you depend on — Soroban contracts, SEPs, asset issuance, anchors, network finality — and why they're essential, not interchangeable.

**Use plain language.** Buzzwords and jargon don't impress panelists who review dozens of submissions per round. Clear, direct writing signals clear, direct thinking.

**One-line test:** Can someone outside your team read your one-sentence description and understand what you build, for whom, and why it needs Stellar? If not, rewrite it.

---

## 2. Show Your Work, Not Just Your Idea

Ideas are cheap. Panelists look for tangible evidence that you can execute.

**Link to real artifacts.** A GitHub repo with code, a working demo URL, a screen recording, a deployed testnet contract — any of these is worth more than a paragraph of promises. Make sure every link in your submission actually works. Broken links are a surprisingly common reason for low scores.

**If you've built before, show it.** Prior SCF awards, open-source contributions, mainnet deployments on Stellar or other chains — all of this builds trust. If you're a returning applicant, show exactly what you delivered with prior funding.

**If you haven't built on Stellar yet, prove you can.** Deploy a basic Soroban contract. Build a proof of concept. Show that you've done more than read the docs. Panelists need to see that your team can interact with the network technically, not just describe plans to do so.

**Acknowledge complexity honestly.** If your project involves hard problems — building an anchor, regulatory compliance, cross-chain bridges — don't gloss over them. Show that you understand the requirements, the edge cases, and the Stellar-specific quirks. Reviewers respect teams that acknowledge difficulty and present credible plans to handle it.

---

## 3. Structure Your Deliverables Like Funded Projects Do

Funded submissions share a consistent deliverable format. Use it:

> **Deliverable N — [Name]**
> - **Description:** What you will build or deliver.
> - **Completion criteria:** How a reviewer confirms it's done.
> - **Estimated completion:** Date or duration.
> - **Budget:** Cost for this deliverable.

**Aim for 2–4 deliverables per tranche.** Each one should be independently verifiable. If a reviewer can't confirm completion from outside your team, rewrite it.

**Tranche 0 must be technical.** Your proof of intent needs to include code interacting with Stellar or Soroban — not a design doc, not a research phase, not an environment setup.

**Show clear progression.** T1 builds on T0, T2 builds on T1, T3 takes it to production. Avoid vague milestones like "continue development" or "further research."

**T3 must include UX readiness.** Since SCF 7.0, the final tranche requires functional interfaces and usable onboarding — not just a mainnet deployment.

See [Writing Deliverables](writing-deliverables.md) for full guidance and category-specific examples.

---

## 4. Right-Size Your Budget

Budget is one of the most common areas where submissions lose points. The data shows a clear pattern: **rejected submissions ask for more, not less.**

| Status | Average Budget | Median Budget |
|---|---|---|
| Awarded | $93,358 | $93,700 |
| Not Awarded | $101,754 | $101,000 |
| Prescreen Failed | $103,735 | $109,670 |

This doesn't mean asking for less guarantees funding. It means that inflated budgets correlate with weaker proposals. Teams that right-size their budget to their actual scope tend to write tighter, more credible applications.

**Build bottom-up, not top-down.** Start with your deliverables, estimate the effort and cost for each, and arrive at a total. Don't start with $150K and work backward.

**Include rates and effort for every line item.** "Development: $50,000" tells reviewers nothing. "Soroban contract development: 4 weeks at $4,000/week = $16,000" tells them everything.

**Don't request money for ineligible expenses.** Marketing is the most common red flag. SCF funds building, not marketing. Small documentation and community budgets are fine. Large marketing line items are not.

**Consider starting smaller.** A focused $50K–$80K proposal with clear deliverables is easier to approve than a sprawling $150K plan. Returning with traction data for a second award is a proven path — the lifetime cap is $150K–$300K, so starting smaller doesn't close any doors.

**Factor in LaunchKit.** Build Award recipients unlock audit credits and other resources at T2. Don't budget $30K for an external audit if you'll get credits through LaunchKit.

See [Writing Budgets](writing-budgets.md) for detailed guidance, rate benchmarks, and real budget examples from funded projects.

---

## 5. Prove There's Demand

A technically sound project with no evidence of demand is a hard sell. Panelists want to see that someone besides your team cares about what you're building.

**If you have users, show metrics.** Monthly active users, transaction volume, growth rate, retention — with verification links (block explorer, public dashboard, app store listing). Specific numbers beat vague claims.

**If you're pre-launch, show demand signals.** Waitlist signups with specific numbers and collection periods. Named partner commitments. User interview findings. Community engagement metrics. A letter of intent from a potential customer is worth more than 1,000 Twitter followers.

**Set concrete adoption targets.** After funding, what does success look like? "500 MAU within 3 months of mainnet launch" is verifiable. "Grow our user base" is not.

See [Proving Traction](proving-traction.md) for the full framework.

---

## 6. Build Community Support Before You Submit

Visibility matters — especially for the Open Track, where community vote decides your fate. But there's a right way and a wrong way to do it.

**Engage authentically, don't spam.** Dropping links in random Discord channels is ineffective and hurts your reputation. Instead, participate in conversations where your target users and fellow developers actually gather. Add value before you ask for attention.

**The right channels:**
- **Stellar Developer Discord** — The primary hub. Ask questions in #scf-general, share progress, get feedback on your idea before submitting.
- **Stellar Global** — Broader community reach.
- **X / Twitter** — Share progress updates and technical insights.
- **GitHub** — Open-source your work early to build credibility.

**Find advocates, not followers.** Your goal is to turn passive observers into people who understand your project and will vouch for it. Share your progress, ask for feedback, and be responsive. An engaged community member who can articulate why your project matters is more valuable than a hundred people who retweeted your launch announcement.

**Get a referral if you can.** SCF 7.0 introduced a verified referral pathway. Referred submissions get stronger trust signals and faster review. Pilots and SDF staff can refer you. Build those relationships early.

---

## 7. Address Compliance and Security Head-On

Panelists notice when teams avoid hard questions about regulation and security. Being proactive about these topics builds trust.

**Outline regulatory risks and your strategy.** If your project handles user funds, touches KYC/AML, or operates in regulated markets, don't pretend those challenges don't exist. Name the risks and describe your approach — even if the approach is "we're consulting with legal counsel and will implement [specific framework]."

**Plan for security audits.** If your project involves smart contracts that handle value, mention your audit plan. Internal review, external audit, bug bounty — whatever fits your scope and budget. Remember that LaunchKit provides audit credits at T2.

**Handle key management explicitly.** How are private keys stored? Who has access? What's your multisig setup? Reviewers look for this in the security section of your architecture.

---

## 8. Make Your Submission Self-Contained

Reviewers evaluate what's in the submission form. They don't visit your website, browse your GitHub, or watch your YouTube channel unless you link to specific artifacts and explain their relevance inline.

**Don't assume context.** Write as if the reviewer knows nothing about your project. Explain acronyms. Define terms. Provide enough detail that someone can evaluate your proposal without leaving the page.

**Link to evidence, but summarize it inline.** "See our GitHub" is not enough. "Our testnet contract is deployed at [address] (GitHub repo). It implements [specific functions] with [X] passing tests" gives the reviewer what they need without clicking away.

**Check every link before submitting.** Broken links are one of the most common and most avoidable problems. Test every URL in your submission.

---

## 9. Pick the Right Track

SCF 7.0 has three Build Award tracks. Applying to the wrong one is a fast path to rejection.

**Integration Track** — You're building an end-user app whose core purpose is integrating an existing Stellar building block (DeFi protocol, wallet SDK, anchor service). The building block must be the center of your project, not a peripheral feature. Check the current quarter's eligible list before applying.

**Open Track** — You're building something novel — a new protocol, infrastructure, or on-chain primitive. No requirement to integrate a pre-defined building block. Goes to community vote.

**RFP Track** — You're responding to a published Request for Proposals targeting a specific ecosystem gap. Address every requirement in the RFP.

**Quick test:** Is your project primarily about bringing an existing Stellar component to users? Integration Track. Is it about building something new for the ecosystem? Open Track. Is it answering a specific published need? RFP Track.

See [SCF 7.0 Guide](scf-7-guide.md) for detailed track descriptions and tips.

---

## 10. Learn From What Didn't Work

The most reliable way to improve your submission is to study what gets rejected. From panelist feedback and data patterns:

| Common Rejection Reason | What to Do Instead |
|---|---|
| Stellar integration feels bolted on | Make Stellar essential to your core value proposition |
| Vague deliverables ("continue development") | Use the structured format with specific completion criteria |
| Budget not justified | Bottom-up breakdown with roles, rates, and effort per deliverable |
| No evidence of demand or traction | Concrete metrics, waitlist numbers, or named partner commitments |
| Incomplete submission | Answer every field. Check every link. Have someone outside your team read it |
| Team credentials unclear | Name every team member with relevant experience and links |
| Scope too large for budget/timeline | Tighten scope. Start smaller. Come back with traction for more |
| No technical proof in T0 | Deploy something on testnet before you submit |
| Security and compliance ignored | Address risks proactively, even if briefly |
| Submission requires external context to understand | Make it self-contained |

---

## Checklist Before You Submit

- [ ] One-sentence description is clear to someone outside your team
- [ ] Stellar's role is essential and explicitly explained
- [ ] Architecture section includes diagrams, data flows, and Soroban/SEP details
- [ ] Team members are named with relevant experience and links
- [ ] Traction evidence is specific and verifiable (or demand signals are concrete)
- [ ] Deliverables use the structured format (description, completion criteria, date, budget)
- [ ] T0 includes a technical deliverable interacting with Stellar/Soroban
- [ ] T3 includes UX readiness (onboarding, documentation, usability)
- [ ] Budget is bottom-up with rates, effort, and per-tranche breakdown
- [ ] Budget is proportional to scope (not inflated to hit $150K)
- [ ] LaunchKit benefits are factored in and not double-counted
- [ ] No large marketing or contingency line items
- [ ] Every link in the submission works
- [ ] Submission is self-contained — doesn't require external context
- [ ] Correct track selected (Integration, Open, or RFP)
- [ ] Referral secured if possible
- [ ] Someone outside your team has read and understood the full submission

---

## Related Guides

- [SCF 7.0 Guide](scf-7-guide.md) — Program overview, tracks, and evaluation criteria
- [Interest Form Tips](interest-form-tips.md) — Getting past the first filter
- [Submission Template](submission-template.md) — Fill-in-the-blank application draft
- [Writing Deliverables](writing-deliverables.md) — Structured deliverable format with funded examples
- [Writing Budgets](writing-budgets.md) — Budget construction with real statistics
- [Proving Traction](proving-traction.md) — Metrics, demand signals, and adoption targets
- [Technical Architecture](technical-architecture.md) — Architecture section best practices
