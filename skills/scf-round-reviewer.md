---
name: scf-round-reviewer
description: "Review and rank an entire SCF Build Award round end-to-end. Use when given a set of SCF submission files and asked to evaluate, score, calibrate, and rank all submissions. Covers data collection, categorization, parallel batch review with 6-dimension scoring, cross-batch calibration, referral adjustments, final ranking, and PDF generation. Produces individual review files, calibration reports, a master index, and a final ranking report."
---

# SCF Build Award Round Reviewer

## Purpose

Step-by-step instructions to independently review and rank all submissions to an SCF Build Award round. This was created from the SCF #41 review process and can be adapted for future rounds.

## Prerequisites

### Files Required
- Submission files in `submissions/{slug}.md` (one per submission) — see Submission File Format below
- Review skill definitions in `.claude/skills/`:
  - `scf-reviewer.md` — Core review framework with 6-area scoring
  - `scf-prescreen-checker.md` — 5-area prescreen simulation
  - `scf-budget-builder.md` — Budget validation with category benchmarks
  - `scf-competitor-analyst.md` — Competitive landscape analysis
- The `read-gdoc` skill installed for fetching Google Docs/Drive documents (see "Fetching External Architecture Docs" below)

All skills are available at: https://github.com/lumenloop/awesome-stellar-community-fund/tree/main/skills

### Submission File Format
Each submission file (`submissions/{slug}.md`) must contain the following sections:

```markdown
# {Project Name}

## Metadata

| Field | Value |
|---|---|
| ID | recXXX |
| Tagline | One-line description |
| URL | https://communityfund.stellar.org/dashboard/submissions/recXXX |
| Budget | $140,000 USD |
| Award Type | Build |
| Referrer | Name - SDF (or "None") |
| Previous Awards | 0 |
| Status | Community Vote |

## Team

| Name | Role | Background | LinkedIn | GitHub | Twitter |
|---|---|---|---|---|---|
| ... | ... | ... | ... | ... | ... |

## Description

Full verbatim text from the submission.

## Key Components

| Component | Description |
|---|---|
| ... | ... |

## Stellar Integration

Full verbatim text from the submission.

## Traction

Full verbatim text from the submission.

## Tranches

### Tranche 1 — MVP ($28,000, Month 1-3)

**Budget Breakdown:**

| Item | Cost |
|---|---|
| ... | ... |

**Deliverables:**

| Deliverable | Description | Budget | Acceptance Criteria |
|---|---|---|---|
| ... | ... | ... | ... |

(Repeat for each tranche)

## Links

| Link | URL |
|---|---|
| Website | ... |
| GitHub | ... |
| Architecture | ... |
```

If submissions are not yet scraped, use the SCF website scraping process described in Phase 0.

### Fetching External Architecture Docs

Many SCF submissions link to external architecture documents (Google Docs, Google Drive PDFs, Notion pages, IPFS). These often contain 10x more technical detail than the submission text and can significantly affect Technical Depth scores. Fetching them is critical for fair evaluation.

**Google Docs and Google Drive PDFs** — Use the `read-gdoc` skill (invoked via the Skill tool with `skill: "read-gdoc"`). This skill:
- Accepts a Google Docs or Google Drive URL as an argument
- Converts the sharing URL to an export/download URL internally
- Returns the full document text content
- Works with publicly shared docs (viewer access is sufficient)
- For Google Docs: converts `docs.google.com/document/d/{id}` to export format
- For Google Drive files: converts `drive.google.com/file/d/{id}` to direct download

Common URL patterns to look for in submission Links sections (especially the Architecture row):
- `docs.google.com/document/d/...` — Google Doc
- `drive.google.com/file/d/...` — Google Drive PDF/file
- `drive.google.com/open?id=...` — Google Drive link (alternate format)

**Notion pages** — Use WebFetch directly. Most public Notion pages render accessible HTML.

**IPFS links** — Use WebFetch with the gateway URL (e.g., `ipfs.io/ipfs/{hash}`). Some gateways are slow; skip after 15 seconds.

**Unfetchable** — DocSend, Excalidraw, Figma links cannot be reliably fetched. Mark as UNFETCHABLE and note in the review.

---

## Phase 0: Data Collection (if needed)

Skip this phase if submission files already exist.

1. Save the SCF round community voting page as HTML from `communityfund.stellar.org`
2. Parse submission URLs from the page, extracting project names and `/dashboard/submissions/{id}` links
3. Extract referrer data by matching `Referred by:` badges
4. Fetch each submission page and scrape the full application content
5. Create one markdown file per submission in `submissions/` following the format above
6. Verify all files against live pages — check for missing fields, truncated content, budget math errors
7. Install the 8 SCF analysis skills from https://github.com/lumenloop/awesome-stellar-community-fund/tree/main/skills into `.claude/skills/`

---

## Phase 1: Categorize and Index

**Executor**: Leader agent (you)

### Step 1.1: Read All Submissions
Read every file in `submissions/`. For each, extract:
- id, project_name, budget_total, referrer, team size, previous_awards
- Primary technology (Soroban contracts, Horizon API, SEPs, etc.)
- What the project does (DeFi, tooling, identity, payments, etc.)

### Step 1.2: Categorize
Assign each submission to exactly one category:

| Category | Criteria | Budget Benchmark |
|---|---|---|
| Financial Protocol | DeFi, DEX, lending, staking, trading, derivatives, capital protection | $109,000 |
| Developer Tooling | SDKs, IDEs, debugging tools, testing frameworks, developer experience | $75,000 |
| Infrastructure | Identity, compliance, compute layers, bridges, escrow, public goods, privacy | $116,000 |
| End-User Application | Wallets, merchant payments, card programs, consumer apps | $85,000 |

Use judgment for borderline cases. A project that builds infrastructure enabling DeFi goes to Infrastructure. A project that IS a DeFi protocol goes to Financial Protocol.

### Step 1.3: Build Batches
Create 6 batches of 5-6 submissions, grouped by category. Keep same-category submissions together so reviewers can compare within category. If a category has too few submissions (like Dev Tooling), combine it with a related category batch.

### Step 1.4: Create Output Directories
```
mkdir -p reviews/reviews
```

### Step 1.5: Write Master Index
Write `reviews/00-master-index.md` containing:
- Summary statistics (count, total budget, median, range, cap count, referral breakdown)
- Category tables with columns: #, ID, Slug, Project, Budget, Referrer, Team Size
- Batch assignments table
- Budget distribution breakdown
- Referral breakdown (SDF staff, community, none)

The slug for each submission should be a kebab-case version of the project name (e.g., "Hatom Protocol" → "hatom-protocol").

### Step 1.6: Identify Special Cases
Flag these before review starts:
- Submissions at the $150K budget cap (need extra budget scrutiny)
- Submissions with prior SCF awards (need delivery record check)
- Submissions with SDF staff referrals (for later referral adjustment)
- Submissions with community referrals (for later referral adjustment)

---

## Phase 2+3: Parallel Review

**Executor**: 6 parallel agents (one per batch), created via TeamCreate

### Agent Setup
Create a team and spawn 6 agents. Each agent receives:
- Their batch assignment (which submission IDs/slugs to review)
- The full review instructions below
- The category and budget benchmark for their submissions

IMPORTANT: Tell each agent to use SLUG filenames (not IDs) for output files. Tell them that if a WebFetch hangs, mark it UNVERIFIED and move on — do not get stuck on any single URL.

### Per-Submission Review Process

Each agent performs these steps for every submission in their batch:

#### Step A: Read Submission File
Read `submissions/{slug}.md`. Note all sections including team, tranches, links, traction, stellar integration.

#### Step B: Prescreen (5 checks)

| Check | What to Evaluate | Rating |
|---|---|---|
| Completeness | All required fields present? Team bios with verifiable backgrounds? Budget breakdown with per-deliverable costs? Tranches with acceptance criteria? | PASS / FLAG / FAIL |
| Stellar Integration | Is Stellar genuinely central to the project (not bolted-on)? Does it use Soroban, Horizon, SEPs, or Protocol 25 features? Could this project work on any chain? | PASS / FLAG / FAIL |
| Eligibility | Correct award type (Build)? Community Vote status? Budget within $150K limit? | PASS / FLAG / FAIL |
| Quality Threshold | Professional writing? Coherent technical architecture? Realistic timelines (not 4 products in 6 months)? | PASS / FLAG / FAIL |
| Red Flag Scan | Plagiarism signals? Impossible claims? Team misrepresentation? Unverifiable traction? Scope creep? GitHub 404? Website mismatch with proposal? | PASS / FLAG / FAIL |

Prescreen result:
- LIKELY PASS: No FAILs, at most 1 FLAG
- AT RISK: No FAILs, 2+ FLAGs
- LIKELY FAIL: Any FAIL

#### Step C: Link Verification
WebFetch every URL in the submission's Links section, plus any URLs mentioned in the Traction or Stellar Integration sections.

For each URL, record:
- Status: ACCESSIBLE or UNVERIFIED
- Brief note on what was found

Rules:
- Do NOT penalize for inaccessible links (the URL may be temporarily down)
- If WebFetch hangs for more than 15 seconds, skip it and mark UNVERIFIED
- Note any GitHub repos with very few commits or recent creation dates
- Note any websites that don't match the proposal description

#### Step D: Score 6 Dimensions (1-5 each)

| Dimension | Weight | Scoring Guide |
|---|---|---|
| Ecosystem Impact (x3) | CRITICAL | 5: Category-creating, unlocks entirely new capability for Stellar. 4: Significant gap-filler, high composability. 3: Useful addition. 2: Marginal benefit, mostly serves the project itself. 1: No clear ecosystem benefit. |
| Technical Depth (x2) | HIGH | 5: Novel cryptography/architecture, Soroban-native design, formal verification. 4: Detailed contract architecture, security model, demonstrates deep Soroban understanding. 3: Adequate technical plan. 2: Surface-level, could be any chain. 1: No technical substance. |
| Differentiation (x2) | HIGH | 5: First-of-kind on Stellar AND cross-chain. 4: First on Stellar, unique approach. 3: Some differentiation from existing solutions. 2: Entering crowded space with minimal novelty. 1: Direct duplicate of existing Stellar project. |
| Traction (x1.5) | MEDIUM | 5: Live product with significant on-chain metrics, institutional partnerships. 4: Working product with verified users/volume. 3: Testnet deployment or credible pilot. 2: Concept with LOIs or early interest. 1: Idea stage, no evidence of demand. |
| Budget (x1.5) | MEDIUM | 5: Bottom-up with hourly rates, well below benchmark, every dollar justified. 4: Detailed breakdown, at or near benchmark. 3: Adequate breakdown, somewhat above benchmark. 2: Vague breakdown, significantly above benchmark. 1: No breakdown, requesting maximum with no justification. |
| Community Readiness (x1.5) | MEDIUM | 5: Deep Stellar history, prior SCF delivery, active community contributor, open source. 4: Proven team with relevant blockchain experience, clear maintenance plan. 3: Credible team, some blockchain background. 2: Team exists but thin credentials, no Stellar history. 1: Unverifiable team, no public profiles. |

For each dimension, write 2-4 sentences of specific evidence. Quote the submission. Cite on-chain data. Reference competitors.

#### Step E: Competitive Analysis
Do a WebSearch for competing projects:
1. Search Stellar ecosystem specifically (Soroswap, Phoenix, etc.)
2. Search broader blockchain ecosystem if relevant
3. Note if the project is duplicative or genuinely novel
4. Note any live competitors the submission didn't mention

#### Step F: Compute Composite Score
```
weighted = (EI * 3) + (TD * 2) + (Diff * 2) + (Trac * 1.5) + (Bud * 1.5) + (CR * 1.5)
composite = weighted / 57.5 * 100
```

#### Step G: Assign Recommendation
- FUND: composite >= 75
- FUND WITH CONDITIONS: composite 60-74
- DO NOT FUND: composite < 60

Use judgment at boundaries. A submission at 58 with exceptional ecosystem impact may merit FUND WITH CONDITIONS. A submission at 61 with critical red flags may merit DO NOT FUND.

#### Step H: Write Review File

Write to `reviews/reviews/{slug}.md`. Each review file follows this structure:

**Title**: `# {Project Name} — SCF #{round} Review`

**Header table** with columns Field and Value, containing: ID, Budget, Category, Referrer (or "None"), Team Size, Prior Awards (or "$0").

**Prescreen section** (`## Prescreen`): Table with columns Check, Result, Notes — one row per check (Completeness, Stellar Integration, Eligibility, Quality Threshold, Red Flag Scan). Each result is PASS, FLAG, or FAIL. Below the table, state the prescreen result: LIKELY PASS, AT RISK, or LIKELY FAIL.

**Link Verification section** (`## Link Verification`): Table with columns URL, Status, Notes — one row per URL checked. Status is ACCESSIBLE or UNVERIFIED.

**Scoring section** (`## Scoring`): Six subsections, one per dimension. Each subsection title includes the raw score and weighted value, e.g. `### Ecosystem Impact — 4/5 (x3 = 12)`. Body is 2-4 sentences of specific evidence quoting the submission and citing competitors or on-chain data.

**Composite Score section** (`## Composite Score`): Summary table with columns Dimension, Raw, Weight, Weighted — one row per dimension plus a TOTAL row showing the sum out of 57.5. Below the table, state the normalized score (out of 100) and the tier (1-4).

**Recommendation section** (`## Recommendation: FUND / FUND WITH CONDITIONS / DO NOT FUND`): 2-3 sentence summary covering key strength, key concern, and verification gaps.

### After All Reviews Complete
Each agent sends a message to the team lead with their batch summary: project names, scores, and recommendations.

---

## Phase 4: Cross-Comparison and Calibration

**Executor**: 2 calibration agents

### Step 4.1: Collect All Scores
Sort all submissions by composite score. Divide into three groups:
- Top 10 + Bottom 10 → Agent A
- Middle N (everything in between) → Agent B

### Step 4.2: Agent A — Top/Bottom Consistency

For each of the ~20 submissions:
1. Read the review file
2. Read the submission file to get external doc links
3. Fetch external architecture docs (see "Fetching External Architecture Docs" in Prerequisites):
   - Google Docs/Drive URLs → use `read-gdoc` skill via Skill tool
   - Notion URLs → use WebFetch
   - IPFS URLs → use WebFetch with gateway URL
   - DocSend/Excalidraw/Figma → skip, mark UNFETCHABLE
4. Check if external doc reveals substantial new information not captured in the review
5. Cross-check scoring consistency:
   - Are similar-quality submissions scored similarly across different batch reviewers?
   - Is a "4" in Batch 1 equivalent to a "4" in Batch 3?
   - Are budget benchmarks applied consistently?
6. Write findings to `reviews/calibration-top-bottom.md`

### Step 4.3: Agent B — Borderline Zone

For each of the ~13 middle submissions:
1. Same doc fetching as Agent A
2. Pairwise comparisons for submissions within 5 points of each other
3. Tier boundary analysis — the 60-point line separating FUND WITH CONDITIONS from DO NOT FUND is the most critical boundary. Are submissions near it (55-65) correctly placed?
4. Check for tied scores — are ties justified or should they be broken?
5. Write findings to `reviews/calibration-middle.md`

### Step 4.4: Apply Adjustments
The leader reviews both calibration reports and applies score adjustments. Rules:
- Only adjust if there is clear evidence of mis-scoring (not just disagreement)
- Adjustments should be to specific dimensions, not arbitrary composite changes
- Document every adjustment with reason

---

## Phase 5: Final Ranking

**Executor**: Leader agent

### Step 5.1: Compute Referral Adjustments
For the WITH-referrer ranking:
- SDF staff referral: +0.5 on Community Readiness → +0.75 weighted → +1.3 composite
- Community/pilot/alumni referral: +0.25 on CR → +0.375 weighted → +0.65 composite
- No referral: no adjustment

### Step 5.2: Write Final Ranking Report
Write `reviews/01-ranking.md` with these sections:

**Section 1: Ranking WITH Referrer Consideration (Primary)**
Full table with columns: Rank, Project, Slug, Category, Budget, Calibrated Score, Referrer Adj, Final Score, Referrer. Grouped by tier.

**Section 2: Ranking WITHOUT Referrer (Substance-Only)**
Full table with columns: Rank, Project, Score, Tier, Rec, Category, Budget. Note any submissions that change tier between the two rankings.

**Section 3: Do Not Fund — With Specific Feedback**
For each DO NOT FUND submission, write:
- **Why**: 2-3 sentences on the core reason for rejection
- **To improve**: 2-3 specific actionable suggestions for resubmission

This feedback should be constructive, not punitive. The goal is to help teams improve.

**Section 4: Additional Analysis**
Include:
- Calibration adjustments table (what changed and why)
- Tier boundary justifications (why each boundary is where it is)
- Pairwise comparisons for submissions within 3 points of each other
- Category-level patterns (avg score, avg budget, fund rate by category)
- Budget distribution analysis (score vs budget correlation)
- Statistical summary (mean, median, std dev, score range)

### Step 5.3: Generate PDFs
Convert all markdown files to PDFs for handoff:
```
handoff/
  00-master-index.pdf
  01-ranking.pdf
  02-evaluation-plan.pdf
  calibration-top-bottom.pdf
  calibration-middle.pdf
  PROGRESS.pdf
  reviews/
    {slug}.pdf (one per submission)
```

Use the `md2pdf.py` script with markdown-it-py (for proper GFM table rendering) + pymupdf Story API.

---

## Common Pitfalls

1. **WebFetch hangs**: Some URLs (especially Notion, Google Drive folders) may hang indefinitely. Set timeouts and skip after 15 seconds.
2. **Score inflation**: Agents tend to score 3-4 on everything. Enforce that 5 is rare and 1-2 should be used for genuinely weak submissions.
3. **Batch reviewer getting stuck**: Monitor progress. If a batch reviewer hasn't written any files after 10 minutes, replace it with a new agent.
4. **Table rendering in PDFs**: Python's `markdown` library doesn't handle GFM tables in all contexts. Use `markdown-it-py` with `.enable('table')` instead.
5. **Slug filenames**: Agents will default to using IDs for filenames. Explicitly tell them to use slug names.
6. **Zombie agents**: After a team is done, check for lingering processes before deleting the team. Remove zombie entries from the team config if needed.
7. **External docs changing scores**: Architecture docs on Google Drive/Docs often contain 10x more technical detail than the submission text. This can significantly affect Technical Depth scores. Always try to fetch them.
8. **Chain-hopping detection**: Watch for projects that are primarily built on another chain (Solana, Ethereum, MultiversX) and are just "adding Stellar support." These should score lower on Ecosystem Impact and Stellar Integration in prescreen.

---

## Timing Expectations

| Phase | Duration | Parallelism |
|---|---|---|
| Phase 0: Data collection | 30-60 min | Serial (can parallel-verify) |
| Phase 1: Categorize and index | 10-15 min | Serial |
| Phase 2+3: Reviews | 20-40 min | 6 parallel agents |
| Phase 4: Calibration | 15-25 min | 2 parallel agents |
| Phase 5: Final ranking + PDFs | 15-20 min | Serial |
| **Total** | **~90-160 min** | |

---

## Adapting for Future Rounds

1. **Budget benchmarks may change** — check the latest funded/rejected averages from SCF dashboard
2. **Category distribution may differ** — adjust batch sizes and counts accordingly
3. **New Stellar features** — update Technical Depth scoring to account for new protocol capabilities
4. **Track changes** — this runbook is for Open Track. Activation Track, Turbo Track, etc. have different weighting priorities (check scf-reviewer.md)
5. **Round-specific context** — check if SDF has published any round-specific priorities or focus areas
