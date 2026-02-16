# SCF #40 Review: Goated App

**Track:** Integration
**Budget Requested:** $120,000
**Integration Partners:** Freighter Connect, Stellar Wallets Kit, Stellar Disbursement Platform
**Reviewer Date:** 2026-02-16

---

## Checklist Review: Goated App
Track: Integration

---

### Integration Partner Fit
- **Status:** FLAG
- **Evidence:** The submission lists three integration partners: Freighter Connect, Stellar Wallets Kit, and Stellar Disbursement Platform. These are legitimate Stellar building blocks. The proposal describes using Stellar Wallets Kit and Freighter for wallet abstraction and account management, and the Stellar Disbursement Platform for distributing USDC rewards to challenge winners. The described use case (settling social predictions/challenges in USDC via Stellar) is a reasonable integration scenario.
- **Concerns:**
  - The integration partners are listed but the architecture section does not demonstrate deep technical familiarity with their SDKs or APIs. The descriptions read as high-level marketing language rather than implementation-specific detail.
  - The core product (social challenges and predictions) functions entirely without Stellar today. Stellar is being added as a payment/settlement layer on top of an existing Web2 product. This means the building blocks are not central to the product's core value proposition -- they enable an optional economic layer.
  - This submission reads more like an Open Track project (adding a crypto settlement layer to an existing app) with integration partners attached, rather than a project built around the integration partners themselves. If Freighter, Wallets Kit, or the Disbursement Platform were removed, the product would still function as-is.

---

### Technical Architecture
- **Status:** FLAG
- **Evidence:** The submission describes a FastAPI-based "Soroban Settlement Module" backend service, a `SocialAgreementRegistry.rs` Soroban smart contract, and USDC settlement flows. The contract would manage agreement lifecycle (creation, resolution, settlement). The architecture is described as "non-custodial, backend-driven" with account abstraction for end users.
- **Concerns:**
  - **Architecture documents are inaccessible.** The Google Drive link for the technical architecture PDF (`Goated App - Technical Architecture Stellar Soroban.pdf`) could not be rendered or verified. The pitch deck PDF (`pitchGOATED.pdf`) is marked as **trashed** by its owner (ruperbass@gmail.com), meaning it has been deleted. Reviewers cannot verify any architectural diagrams or detailed design documents.
  - No code repository (GitHub or otherwise) is shared or linked. There is no evidence of any existing Stellar or Soroban development work.
  - The Soroban contract description is surface-level: a single contract name (`SocialAgreementRegistry.rs`) with a three-state lifecycle (active, resolved, settled). No contract interfaces, function signatures, state management details, resource usage considerations, or security model are provided.
  - No data flow walkthrough is included in the submission text itself (the linked PDFs are inaccessible).
  - No discussion of on-chain vs off-chain data separation, state archival strategy, or key management approach.
  - The claim of "non-custodial" architecture conflicts with "backend-driven" transaction signing. If the backend prepares, signs, and submits transactions, the key management model needs to be explained in detail. Who holds the keys? How are user accounts created? This is not addressed.
  - No security considerations, audit plan, or discussion of smart contract risks.

---

### Team Readiness
- **Status:** FLAG
- **Evidence:** Three team members are named:
  - **Roberto Sanz** -- Financial & Product/Strategy Lead. LinkedIn profile (linkedin.com/in/robertosanzcriptomonedas) identifies him as a crypto educator and host of the "LAVIDA CRYPTO" podcast. His website (robertosanzcriptomonedas.com) offers cryptocurrency education. He has crypto ecosystem knowledge but in a content/education capacity.
  - **Pablo (Prixenn)** -- Core Developer. Instagram handle provided (@prixenn). No public developer portfolio, GitHub profile, or verifiable technical track record was found.
  - **Anna Armaos** -- Marketing, Growth & Community. LinkedIn profile (linkedin.com/in/annarmaos/) could not be accessed or verified.
- **Concerns:**
  - **No Stellar or Soroban experience on the team.** None of the team members have demonstrable experience building on Stellar, writing Soroban/Rust smart contracts, or integrating Stellar SDKs. The submission itself acknowledges this gap by stating the grant's purpose is "to expand the team's technical capacity by hiring additional blockchain-specialized profiles (Stellar + Soroban)."
  - Roberto Sanz's verifiable background is as a crypto content creator/educator, not as a product builder or technical lead. No evidence links him to the Goated App's development.
  - The core developer (Pablo/Prixenn) has no verifiable public presence as a developer. No GitHub, no portfolio, no technical writing. The Instagram handle returned no relevant results.
  - The pitch deck PDF owner email (ruperbass@gmail.com) does not obviously correspond to any named team member, adding opacity to the team structure.
  - The submission names "Roberto Garcia Sanz" as the project team member but "Roberto Sanz" in the team description. A web search for "Roberto Garcia Sanz" returns unrelated individuals (an HR director at a bank, a construction machinery rental company in Valladolid). The connection between the named team member and the Goated App could not be independently verified.
  - The team is asking for $120,000 to hire Stellar/Soroban developers they don't yet have. This means the actual builders are unknown at the time of application.

---

### Traction
- **Status:** FLAG
- **Evidence:** The Goated App is a real, live product available on both Google Play and the iOS App Store. The app is a social challenges/predictions platform where users create groups, complete challenges (with photo/video proof), and earn points. This is verified:
  - **Google Play:** 100K+ downloads, 4.5 stars, 438 reviews (com.goatedapp.goated, published by Goated Development)
  - **iOS App Store:** 4.7 stars, 29 ratings, last updated July 11, 2025 (v4.0.1)
  - **Website:** goatedapp.com is live and accurately describes the product
- **Concerns:**
  - **Internal metric contradictions.** The submission states "15,000+ monthly active users" in the Products & Services section but "more than 6,000 monthly active users" in the Traction Evidence section. This is a significant discrepancy within the same application.
  - **Registered user claims vs store data.** The submission claims "230,000 registered users" but Google Play shows "100K+ downloads." Even accounting for iOS users, 230K registered users from ~100K Android downloads and what appears to be a much smaller iOS install base (29 ratings vs 438 on Android) is difficult to reconcile. The ratio of registered users to app store downloads would need to be explained.
  - **Google Play ranking claims are unverifiable.** The submission claims "Ranked Top 1 Social App in March 2025" and "Ranked Top 3 overall app in April 2025." No evidence was found to support these claims in any app ranking database, industry report, or news coverage. These may refer to a specific regional/category ranking (e.g., a subcategory in Spain) but the claims are presented without qualification or source.
  - **Firebase metrics spreadsheet is inaccessible.** The linked Google Sheets document ("Resumen de Firebase Goated") could not be read or verified. The traction metrics cannot be independently confirmed.
  - **No adoption targets for the Stellar integration.** The submission does not state what on-chain metrics they expect to achieve. No target for number of USDC settlements, active wallets, transaction volume, or on-chain engagement is provided.
  - The traction is entirely Web2 (app downloads, points-based engagement). There is zero Stellar or blockchain traction, which is expected for a new integration but means all claimed metrics reflect a product that works without Stellar.

---

### Budget & Deliverables
- **Status:** FLAG
- **Evidence:** The $120,000 budget is split across three tranches (T1: $24,000, T2: $36,000, T3: $48,000). Note: T0 is not explicitly mentioned in the tranche breakdown, though the T1 section references "$12,000" as "20% after Tranche #0 approval," suggesting a T0 of $12,000 exists somewhere. The tranche structure follows a 6-week / 4-week / 4-week timeline (14 weeks total). Deliverables include Soroban contract development, USDC settlement flows, wallet abstraction, Disbursement Platform integration, testnet MVP, load testing, mainnet deployment, and documentation.
- **Concerns:**
  - **No bottom-up budget.** There is no line-item breakdown, no hourly/weekly rates, no role-based cost allocation, and no effort estimates. The budget is presented as flat dollar amounts per tranche with no visibility into how funds will be spent. This is a common red flag per SCF review guidelines.
  - **Budget includes hiring unnamed developers.** The submission states funds will be used to hire "blockchain-specialized profiles (Stellar + Soroban)" who are not yet identified. Reviewers are being asked to fund a team that does not yet exist.
  - **$120,000 is above the median** for funded application projects ($85,000 median). While not disqualifying, the lack of any budget justification or breakdown makes it impossible to assess proportionality.
  - **T0 is unclear.** The tranche structure in the submission text starts at "Tranche 1" with $24,000 (described as foundation/MVP), but references a "Tranche #0 approval." The actual T0 deliverable and budget are not clearly defined.
  - **Deliverables are somewhat specific** (Soroban contract, USDC settlement flow, testnet demo) but lack verifiable completion criteria. "A successful end-to-end demo on Stellar testnet" is a reasonable T1 measure, but later tranches use vaguer language ("stable backend synchronization under load," "no critical outages").
  - **14-week timeline for the full scope** (foundation through mainnet) with a team that needs to hire Stellar/Soroban developers is aggressive, especially given no existing blockchain code.
  - **No UX readiness plan for T3.** The T3 deliverables focus on mainnet deployment and infrastructure but do not address the SCF 7.0 requirement for UX readiness at T3.

---

### Ecosystem Commitment
- **Status:** FLAG
- **Evidence:** The submission positions Stellar as infrastructure chosen for "low cost, high speed, and reliability for frequent micropayments." The product concept (settling social predictions in USDC) would generate real transaction volume on Stellar if successful. The use of USDC on Stellar for micropayments aligns with the network's strengths.
- **Concerns:**
  - **No prior Stellar involvement.** Neither the team nor the product has any history in the Stellar ecosystem. No community participation, no prior SCF applications, no Stellar developer activity.
  - **No maintenance or post-launch plan.** The submission does not address what happens after T3. How will the Stellar integration be maintained? What is the long-term commitment to the Stellar network?
  - **Chain-agnostic framing.** The "non-custodial, backend-driven architecture" described could be implemented on any chain with smart contracts and stablecoins. The submission does not articulate why Stellar specifically is essential beyond cost and speed advantages that could be matched by other L1s/L2s.
  - **No referral.** The submission has no referral, which means it must pass through prescreening on its own merits.

---

### Overall Assessment

- **Recommendation:** Do not fund (in current form)
- **Key strength:** Goated is a real, production app with genuine users (100K+ Google Play downloads verified) and organic traction in the social challenges space. The concept of settling social predictions in USDC via Stellar is a legitimate use case with potential for high-frequency micropayments.
- **Key concern:** The submission has multiple verification failures: inaccessible/trashed documents, internally contradictory user metrics, unverifiable ranking claims, no Stellar/Soroban experience on the current team, no code repository, no bottom-up budget, and plans to hire the actual builders with grant funds. The team cannot be verified as capable of executing the proposed Stellar integration.
- **Verification gaps:**
  - Pitch deck PDF is trashed/deleted by owner
  - Technical architecture PDF is inaccessible
  - Firebase metrics spreadsheet could not be read
  - Google Play ranking claims (Top 1, Top 3) could not be confirmed through any public source
  - Discrepancy between 15,000 MAU and 6,000 MAU within the same submission
  - 230,000 registered users claim cannot be reconciled with ~100K Google Play downloads
  - Pablo (Prixenn) has no verifiable developer presence
  - Anna Armaos LinkedIn profile could not be accessed
  - Connection between "Roberto Garcia Sanz" (project member field) and "Roberto Sanz" (crypto educator) is assumed but not confirmed
  - No GitHub repository or existing Stellar/Soroban code

---

## Summary for Review Form

### Products & Services
- Goated is a real social app (Google Play: 100K+ downloads, 4.5 stars) for group challenges and predictions. The proposal adds USDC settlement via Stellar/Soroban.
- The core product works without Stellar. Integration partners (Freighter, Wallets Kit, Disbursement Platform) enable a payment layer, not core functionality.

### Technical Architecture
- Architecture docs (Google Drive PDFs) are inaccessible; the pitch deck is trashed. No code repo shared.
- Soroban contract design is surface-level: one contract name, three states, no interfaces or security model.
- "Non-custodial, backend-driven" claim needs key management explanation that is not provided.

### Team
- Roberto Sanz is a verifiable crypto educator/podcaster, but no evidence of product development or Stellar experience.
- Core developer (Pablo/Prixenn) has no verifiable public technical presence.
- The team explicitly plans to hire Stellar/Soroban developers with grant funds -- actual builders are TBD.

### Traction
- Real app with real users, but metrics contradict internally (15K vs 6K MAU in the same submission).
- 230K registered users claim is hard to reconcile with Google Play showing 100K+ downloads.
- "Top 1 Social App" and "Top 3 overall" ranking claims could not be verified through any public source.
- Firebase data spreadsheet is inaccessible for independent verification.

### Budget
- $120,000 with no line-item breakdown, no rates, no effort estimates. Budget is a flat number without justification.
- Funds partially intended to hire unnamed Stellar/Soroban developers.
- No UX readiness plan for T3 as required by SCF 7.0.

### Ecosystem Commitment
- No prior Stellar ecosystem involvement. No maintenance plan. Architecture is chain-agnostic in design.
- Stellar chosen for cost/speed but the submission does not explain why Stellar is irreplaceable.
