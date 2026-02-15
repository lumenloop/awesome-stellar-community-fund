# RFP Response Guide

> How to write a strong response to an SCF Request for Proposals. The RFP Track has different dynamics than Integration or Open — this guide covers how to respond to specific requirements, demonstrate relevant expertise, and address the maintenance and developer experience concerns that RFP panels prioritize.

## What the RFP Track Is

RFPs are specific tooling, infrastructure, or ecosystem capabilities that have been identified as strategic gaps in the Stellar ecosystem. The SCF publishes RFPs based on ecosystem needs, and teams respond with proposals to build the requested capability.

**Key differences from other tracks:**

| | Integration Track | Open Track | RFP Track |
|---|---|---|---|
| **You decide what to build** | Partially (from eligible list) | Yes | No (RFP defines it) |
| **Reviewed by** | Pilot delegate panel | Community vote | Domain expert panel |
| **Primary focus** | End-user product | Ecosystem impact | Spec compliance + DX |
| **Maintenance matters** | Somewhat | Somewhat | A lot |

---

## Before You Start

### 1. Read the Full RFP Carefully

This sounds obvious, but it's the most common failure point. RFP panels report that many submissions don't address all requirements listed in the RFP. Before writing a single word:

- Read the RFP document end-to-end, twice
- List every explicit requirement
- List every implicit requirement (things that are clearly expected but not bullet-pointed)
- Note any "nice to haves" vs "must haves"
- Check if there are evaluation criteria specified in the RFP itself

### 2. Assess Your Fit Honestly

RFP panels include domain experts. If the RFP is for an indexer and you've never built indexing infrastructure, your submission will not compete with teams that have. Ask yourself:

- Have I built something like this before?
- Can I point to prior work in this specific domain?
- Do I understand the technical challenges unique to this type of infrastructure?
- Can I maintain this after the initial build?

If the answer to most of these is no, this RFP may not be for you.

### 3. Research Existing Solutions

Before proposing your approach, understand what already exists:

- What tools exist on Stellar today in this space?
- What do other chains use for this (e.g., The Graph for indexing, Foundry for testing)?
- What are the known pain points with existing solutions?
- What does the Stellar developer community specifically want?

Check the Stellar Developer Discord, GitHub issues on stellar-core and soroban repos, and any community feedback linked in the RFP.

---

## How to Structure Your Response

### 1. Requirements Mapping

Create an explicit map from every RFP requirement to your proposed solution. Don't make the panel hunt for compliance — show it clearly.

**Format:**

| RFP Requirement | Your Solution | Details |
|----------------|--------------|---------|
| [Requirement 1 from RFP] | [How you address it] | [Technical specifics] |
| [Requirement 2 from RFP] | [How you address it] | [Technical specifics] |
| [Requirement 3 from RFP] | [How you address it] | [Technical specifics] |

This table should appear early in your submission so reviewers can see at a glance that you've read and responded to every requirement.

### 2. Technical Approach

Go deep on how you'll build it. RFP panels are domain experts — they can tell the difference between genuine technical understanding and hand-waving.

**Include:**
- Architecture diagram showing all components
- Technology choices with justification (why this language, this framework, this approach?)
- Data model or schema design
- API design (endpoints, parameters, response formats) if applicable
- Performance considerations (how does it handle load, large datasets, concurrent users?)
- Compatibility with existing Stellar infrastructure (Horizon, Soroban RPC, SDKs)

### 3. Developer Experience (DX)

Most RFPs target developer tooling and infrastructure. The panel cares deeply about DX. Address:

- **Installation and setup:** How easy is it to get started? One command? Docker? Package manager?
- **Documentation plan:** API reference, tutorials, quickstart guide, examples
- **Error messages:** Will developers get helpful, actionable errors?
- **SDK/library integration:** Does your tool integrate with existing Stellar SDKs?
- **CLI vs GUI vs both:** What interfaces will you provide?
- **Examples and templates:** Will you ship starter examples?

**DX test:** Could a Stellar developer who has never used your tool get a basic workflow running in under 15 minutes?

### 4. Prior Work

Show specific, relevant prior work. Not "I'm a senior developer with 10 years of experience" — show the work:

- Link to prior projects in the same domain
- Show GitHub repos with real code, not just READMEs
- Reference production deployments you've built and maintained
- If you've contributed to Stellar ecosystem tooling before, highlight it specifically

### 5. Maintenance Plan

This is where most RFP submissions are weakest. Infrastructure and tooling need ongoing maintenance. Address:

**During the grant period:**
- Bug fix response time SLA (e.g., critical bugs within 48 hours)
- How you'll handle Stellar network upgrades that affect your tool
- Testing strategy (unit tests, integration tests, CI/CD)
- Version management and release process

**After the grant period:**
- Who maintains this? Is there a plan for ongoing support?
- How will you handle breaking changes in Stellar/Soroban?
- What's your long-term commitment? (Honest answers are better than vague promises)
- Is there a sustainability model? (Open source contributions, community maintenance, future funding)
- What happens if you stop maintaining it? Is the code structured so someone else can take over?

### 6. Timeline

RFP projects are scoped to fill identified gaps quickly. Your timeline should be:

- **Tight but credible.** Don't pad it, but don't be unrealistically aggressive.
- **Mapped to deliverables.** Each milestone has a clear, verifiable output.
- **Front-loaded with the hardest work.** Don't put all the complex engineering in T3.
- **Inclusive of documentation and testing time.** Don't treat these as afterthoughts.

---

## What RFP Panels Look For

Based on common panel feedback, here's what differentiates winning submissions:

### Strong Signals

- Point-by-point response to every RFP requirement
- Deep technical understanding of the specific domain (not just general blockchain knowledge)
- Prior work in the exact area the RFP targets
- Thoughtful DX design (not just "we'll add docs later")
- Credible maintenance plan with specific commitments
- Realistic timeline that accounts for testing and documentation
- Understanding of how the tool fits into the existing Stellar developer workflow

### Weak Signals

- Generic proposal repurposed from another application
- "We'll figure out the details during development"
- No prior work in the relevant domain
- No mention of maintenance or long-term support
- Documentation as a T3 afterthought
- Timeline that doesn't account for testing
- No consideration of developer experience
- Ignoring specific RFP requirements or addressing only some of them

---

## Common Mistakes

| Mistake | Why It Hurts |
|---------|-------------|
| Not addressing every RFP requirement | Panels check compliance first. Missing requirements = immediate downgrade. |
| Repurposing a generic proposal | RFP panels can tell. Tailor your response to the specific RFP. |
| No relevant prior work shown | Domain expertise is critical for RFPs. General dev experience isn't sufficient. |
| Docs planned for "later" | For tooling, documentation IS the product. Plan it alongside development. |
| No maintenance plan | Panels worry about tools that get abandoned. Address this directly. |
| Over-engineering the solution | Build what the RFP asks for. Don't add a governance token, a marketplace, and an AI layer to a testing framework. |
| Ignoring existing tools | If similar tools exist on other chains, reference them. Show you've studied what works. |
| No DX consideration | A powerful tool that's painful to use won't get adopted. |

---

## RFP-Specific Deliverables

RFP deliverables should emphasize different things than Integration or Open Track deliverables:

| Tranche | Focus for RFP Projects |
|---------|----------------------|
| **T0 (10%)** | Core functionality proof-of-concept. Show the hardest technical piece working. |
| **T1 (20%)** | Functional prototype with basic API/CLI. A developer should be able to try it. |
| **T2 (30%)** | Feature-complete on testnet with documentation draft, integration tests, and example usage. |
| **T3 (40%)** | Production-ready with full documentation, CI/CD, published package, and maintenance plan active. |

**Key difference:** RFP deliverables should include documentation and developer-facing artifacts in every tranche, not just T3. For tooling projects, a README with quickstart, API reference, and examples is as important as the code itself.

---

## Checklist Before You Submit

- [ ] Every RFP requirement is addressed with a specific solution
- [ ] Requirements mapping table is included
- [ ] Architecture is described with technical specifics (not just component names)
- [ ] Prior work in the relevant domain is linked and described
- [ ] Developer experience is addressed (setup, docs, errors, examples)
- [ ] Maintenance plan covers both during-grant and post-grant periods
- [ ] Timeline is realistic and front-loads hard work
- [ ] Documentation is planned alongside development, not as an afterthought
- [ ] Deliverables include developer-facing artifacts in every tranche
- [ ] The proposal responds to THIS RFP, not a generic application
