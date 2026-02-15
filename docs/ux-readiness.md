# UX Readiness

> SCF 7.0 introduced UX readiness as a requirement for the final tranche (T3). Mainnet deployment alone is no longer sufficient — your product must be usable. This guide covers what UX readiness means, what reviewers expect, and how to plan for it from the start.

## What Changed in SCF 7.0

In previous versions, the final milestone was mainnet deployment. Teams could ship a working contract and a bare-bones interface and call it done. SCF 7.0 changed this: the final tranche (40% of your budget) now requires **UX readiness** — clear onboarding flows, functional and tested interfaces, and basic usability validation.

This is a gate. If your product is live on mainnet but unusable by a normal person, you will not receive your final tranche payment.

---

## What UX Readiness Means

UX readiness does not mean your product needs to win design awards. It means a new user can find your product, understand what it does, create an account or connect a wallet, and complete the core action — without getting stuck, confused, or lost.

### The Core Test

Ask yourself: **Could someone who has never seen my product use it successfully within 5 minutes, without help from my team?**

If the answer is no, your UX is not ready.

### Minimum Requirements

| Requirement | What It Means |
|------------|--------------|
| **Functional interface** | A working frontend (web or mobile) that lets users interact with your product. Not a CLI, not a raw API, not "coming soon." |
| **Onboarding flow** | A clear path from first visit to first meaningful action. Account creation, wallet connection, KYC (if applicable), and first transaction should be guided. |
| **Error handling** | When something goes wrong, users see a helpful message — not a blank screen, a stack trace, or a silent failure. |
| **Loading and state feedback** | Users should always know what's happening. Transactions processing, data loading, confirmation states — all should be visible. |
| **Basic documentation** | FAQ, help section, or in-app guidance that answers the most common questions. |
| **Responsive or appropriate design** | If it's a web app, it should work on common screen sizes. If it's mobile, it should work on current iOS/Android versions. |

### What's NOT Required

- Pixel-perfect design
- Design system or component library
- Multi-language support
- Advanced analytics integration
- A/B testing infrastructure
- Marketing landing page (though it helps)

---

## How to Plan for UX from Day One

The biggest mistake teams make is treating UX as a final polish step. If you wait until T3 to think about usability, you'll either rush it or fail the gate.

### During T0 (Proof of Intent)

- **Define your core user flow.** Before you write a line of code, sketch the path from "user lands on your site" to "user completes the key action." This can be rough — napkin sketches or wireframes.
- **Identify UX-critical decisions early.** Custodial vs non-custodial wallet? SEP-24 interactive flow vs embedded? These choices shape your entire UX.

### During T1 (MVP)

- **Build the UI alongside the logic.** Don't build a backend-only MVP and plan to add UI later. Your MVP should be usable, even if ugly.
- **Test with at least 2-3 people outside your team.** Watch them try to use it. Note where they get stuck. Fix those points.

### During T2 (Testnet)

- **Share your testnet build with the Stellar Discord community.** Ask for feedback in #scf-general or #build. Community feedback is both useful and visible to reviewers.
- **Refine your onboarding flow.** The testnet version should have a complete (even if simplified) onboarding path.
- **Document known UX gaps.** If something is rough, acknowledge it in your tranche submission and explain how you'll fix it by T3.

### During T3 (Mainnet + UX Readiness)

- **Conduct a usability walkthrough.** Record yourself or a test user going through the entire flow from scratch. This recording can be part of your tranche submission.
- **Write user-facing documentation.** FAQ, getting started guide, or in-app tooltips.
- **Test error states.** Insufficient balance, rejected transaction, network error, expired session — all should produce clear feedback.
- **Verify on multiple devices/browsers.** At minimum, test on Chrome and one mobile browser.

---

## UX Readiness Checklist for T3 Submission

Use this checklist when preparing your final tranche deliverable:

### Onboarding
- [ ] New user can create account or connect wallet without external help
- [ ] First-time user flow is guided (not a blank dashboard)
- [ ] Required steps (KYC, trustline setup, etc.) are explained in-context
- [ ] User understands what the product does within 30 seconds of landing

### Core Functionality
- [ ] Primary user action (send payment, deposit, swap, borrow, etc.) works end-to-end
- [ ] Transaction confirmation is clear (success state, tx hash, next steps)
- [ ] Transaction history or activity log is accessible
- [ ] Key information is visible (balances, fees, rates, status)

### Error Handling
- [ ] Insufficient balance shows a clear message
- [ ] Failed transactions explain what went wrong
- [ ] Network errors show a retry option or helpful guidance
- [ ] Form validation catches obvious mistakes before submission

### Feedback and State
- [ ] Loading states are visible (spinners, progress indicators)
- [ ] Pending transactions show status updates
- [ ] Success and failure states are clearly different
- [ ] Users are not left on blank or ambiguous screens

### Documentation
- [ ] FAQ or help section covers top 5 user questions
- [ ] Getting started guide exists (in-app or linked)
- [ ] Contact or support channel is accessible from the product

### Accessibility Basics
- [ ] Text is readable (sufficient contrast, reasonable font sizes)
- [ ] Buttons and links are large enough to tap on mobile
- [ ] App works on current Chrome and one mobile browser

---

## What Reviewers Check at T3

When evaluating UX readiness for the final tranche, reviewers will:

1. **Visit your product** and attempt the core user flow from scratch
2. **Check onboarding** — can they get started without your help?
3. **Test error states** — what happens when they enter bad data or have no balance?
4. **Look for documentation** — is there a FAQ, help section, or getting started guide?
5. **Verify it's functional** — not a landing page, not a "coming soon," not a broken prototype

If a reviewer gets stuck, confused, or can't complete the core action, UX readiness is not met.

---

## Leveraging the Stellar LaunchKit

Build Award recipients unlock the Stellar LaunchKit at the Testnet milestone (T2). This can include:

- **UX audits and user testing** — Professional UX review of your product
- **Audit credits** — For security, which indirectly affects UX (secure flows build user trust)
- **Infrastructure offers** — Reliable infrastructure means fewer error states for users

Request UX audit support through the LaunchKit as early as possible. The feedback you get between T2 and T3 directly helps you pass the UX readiness gate.

---

## Common UX Problems in SCF Projects

| Problem | Impact | Fix |
|---------|--------|-----|
| Wallet connection is confusing | Users drop off before starting | Use established patterns (WalletConnect, Freighter), add clear instructions |
| No explanation of fees | Users don't understand costs | Show fee breakdown before transaction confirmation |
| Trustline setup is manual | Users don't know what a trustline is | Auto-prompt trustline setup with plain-language explanation |
| Raw error messages from Horizon | Users see technical jargon | Map API errors to human-readable messages |
| No loading states | Users think the app is broken | Add spinners, progress bars, and status messages |
| Desktop-only design | Mobile users can't use the product | Test and fix for mobile browsers at minimum |
| No "what is this?" context | Users don't understand blockchain concepts | Add tooltips or a glossary for terms like XLM, trustline, memo |
