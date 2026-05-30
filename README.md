# Subspace.money — Product Teardown
**Product Intern Assignment · 2026**
Submitted by **Shishir Agarwal**

---

## TL;DR

Subspace has real product-market fit (₹36.5 Cr ARR, bootstrapped) but is fighting on too many fronts at once — and has a platform integrity crisis hiding in its 1-star reviews. This teardown covers five pillars: UX, Features, GTM & ICP, Competitor Analysis, and Collaborations. Every observation was made through direct app usage and public data. No filler.

---

## How I Approached This

Before downloading the app, I noticed Subspace's Play Store rating was 3.5 stars — a meaningful gap from the category average of 4.0+. That number is a structural signal.

I filtered reviews to 1-star, sorted by "Most Relevant," and read every one. A pattern emerged fast: admins revoking access after payment with no refund, gift cards stuck in processing, app crashes on launch, and money locked in wallets. The most-upvoted review (10 helpful votes) revealed something deeper — an admin had retaliated against a negative reviewer by removing them from groups and coordinating mass 1-star ratings. That's not a support failure. That's a platform integrity crisis.

With that context, I downloaded the app and used it as a real user: homepage, onboarding, gift card purchase, cart, wallet top-up, UPI payment. I documented specific screens and flows, noting where experience broke relative to what the product promised.

**Personally reproduced bugs:**
- Rs.100 quick-select on Dominos gift card adds Rs.425 to cart
- Cart count badge increments beyond actual item count
- Custom UPI picker triggers Android's native intent chooser — two taps for one action

Finally, I reviewed Subspace's external presence: LinkedIn (3,484 followers, ~5 reactions/post), Instagram (906 followers), and Play Store listing. The most recent LinkedIn post promotes renting gear for a photoshoot — a persona with zero overlap with the hostel student splitting a Netflix bill.

Everything in this teardown is grounded in what I actually saw and used.

---

## The Five Pillars

| # | Pillar | Core Finding |
|---|--------|-------------|
| [01] | **UX** | Three sequential checkout friction points that compound at the highest-stakes moment — payment |
| [02] | **Features / Services** | A financial integrity bug (wrong cart amount) + a missing Access Guarantee creating real user risk |
| [03] | **GTM & ICP** | Messaging three different people at once and converting none efficiently |
| [04] | **Competitor Analysis** | CRED has entered Subspace's lane — and Subspace has no counter-positioning |
| [05] | **Collaborations** | Subspace's best users already live together but aren't being activated as a cluster |

---

## Key Findings at a Glance

### UX — Checkout has three compounding friction points
1. No "Buy Now" button — buying a single item from a multi-item cart requires 6+ extra taps
2. Non-intuitive quick-select amounts (Rs.1670, Rs.2505) — internal plan values surfaced directly to users
3. Double UPI selector — Subspace's custom picker triggers Android's native "Open with" chooser immediately after. The tagline "Superfast, zero failures" appears on the screen that creates the failure.

### Features — Financial integrity and platform trust at risk
- **Bug:** Rs.100 quick-select adds Rs.425 to cart (Dominos gift card, reproduced consistently)
- **Bug:** Cart badge count does not sync with actual cart state
- **Structural gap:** No Access Guarantee or escrow — admins can revoke subscription access after payment with no automated refund. Multiple 1-star reviews confirm this is not an edge case.

### GTM & ICP — Fragmented messaging across incompatible audiences
- LinkedIn promotes premium rentals to urban professionals
- Instagram posts generic discount content with 906 followers
- Play Store listing targets students, subscription sharers, renters, gift card buyers, and B2B providers simultaneously
- Homepage tagline: "Your subscription management platform" — first interaction: a delivery address modal for the rental feature

### Competitor Analysis — No counter-positioning against CRED
- CRED launched "CRED Money" in July 2024: subscription tracking, recurring payment reminders, AA-framework bank integration — for 12M+ verified premium users
- Subspace's gift card vertical competes directly with CRED Store, Woohoo, Amazon Pay, and PhonePe — all with structural trust advantages Subspace cannot match on brand alone
- Subspace's only truly differentiated feature — P2P subscription sharing + Negotiate API — is buried in marketing materials and undefended externally

### Collaborations — Cluster acquisition is untapped
- Subspace pays individual CAC for students who already live on the same hostel floor
- No hostel/PG partnerships, no campus ambassador program, no location-based group suggestion engine
- A partnership with Stanza Living, OYO PG, or NestAway could onboard entire floors as a unit — with 12–24 month retention naturally tied to the academic year

---

## Competitor Snapshot

| Feature / Dimension | Subspace | CRED | Splitwise | Fi Money | PlayBucks |
|---------------------|----------|------|-----------|----------|-----------|
| P2P Subscription Sharing | ✅ | ❌ | ❌ | ❌ | ✅ |
| Gift Cards | ✅ | ✅ | ❌ | ❌ | ❌ |
| Expense / Sub Tracking | Partial | ✅ | ✅ | ✅ | ❌ |
| Negotiate API | ✅ | ❌ | ❌ | ❌ | ❌ |
| Access Guarantee / Escrow | ❌ | N/A | N/A | N/A | ❌ |
| Brand Trust | Medium | Very High | High | High | Low |
| User Base | Growing | 12M+ | 50M+ global | Growing | Small |
| Bootstrapped / Profitable | ✅ | ❌ | ❌ | ❌ | ❌ |

**Key insight:** Subspace's only truly differentiated features are P2P subscription sharing and the Negotiate API. No other player in the Indian market offers both. Every other vertical — gift cards, expense tracking, rentals — has at least one better-resourced competitor.

---

## Prioritization

Subspace is bootstrapped with ~3 employees. Every product decision is a resource allocation decision.

| Priority | Action | Pillar | Effort | Rationale |
|----------|--------|--------|--------|-----------|
| 🔴 **1** | Fix cart bugs + Launch Access Guarantee | Features | 2–3 weeks | Financial integrity bugs must be fixed before any growth spend. A user overcharged or losing access tells five friends. |
| 🟠 **2** | Fix double UPI selector + Add Buy Now button | UX | 3–5 days | Lowest effort, highest checkout conversion impact. UPI fix is a single-line change. |
| 🟡 **3** | ICP refocus + Instagram content strategy for students | GTM & ICP | 2 weeks | Zero engineering cost. Marketing sprint only. Compounds over time. |
| 🟢 **4** | CRED counter-positioning + Negotiate API as headline feature | Competitor | 1 week | Positioning sprint: one landing page, homepage rewrite. No new engineering. |
| 🔵 **5** | Hostel / PG partnership pilot (one Bengaluru property) | Collaborations | 30-day pilot | Highest long-term LTV impact. Validate with one pilot before full rollout. |

> I would prioritize #1 regardless of effort — financial integrity bugs in a fintech product erode trust faster than any other failure mode.

---

## Exhibits

All screenshots were captured during live app testing on **May 30–31, 2026** and from the Subspace Play Store review section (filtered: Most Relevant, 1-star).

| Exhibit | Description |
|---------|-------------|
| [A] | Cart screen — "Your Cart, 2 items" — only "Proceed to Pay Rs.4846", no Buy Now per item |
| [B]| Product Details — Playstore gift card — quick select values: Rs.10 / Rs.1670 / Rs.2505 / Rs.5000 |
| [C] | Wallet screen |
| [D] | Wallet screen — Subspace custom UPI picker ("Superfast, zero failures") |
| [E] | Wallet screen — Android native "Open with" intent chooser appearing immediately after C |
| [F] | Recent LinkedIn post regarding "premium gear for a photoshoot" — #SmartRental   |
| [G] | Instagram profile — 906 followers — generic savings content, no consistent person |
| [H] | Cart — Dominos gift card — Rs.100 selected, Rs.425 added to cart Video Recording|
| [I] | Subspace.money 1 star Reviews Most Relevant and quoted |
---
H- Screen Recording https://drive.google.com/file/d/1RumDRw8W92V7B9zQA8OT5B4C_WbPXDyk/view?usp=sharing
## Full PDF Submission

The complete teardown with all pillar write-ups is available here: [Subspace_Teardown_Shishir_Agarwal.pdf](Subspace_Teardown_Shishir_Agarwal.pdf)

---

## About

**Shishir Agarwal**
Product Intern Assignment — Subspace.money, 2026
Submission date: May 31, 2026

*All observations are based on direct app usage, Play Store review analysis, and public social media research.*
