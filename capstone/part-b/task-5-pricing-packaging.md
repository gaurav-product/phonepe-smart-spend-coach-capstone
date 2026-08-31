# PART B — TASK 5 · PRICING & PACKAGING
## PhonePe Smart Spend Coach

**Requirements covered:** B25 (freemium vs free-trial) · B26 (packaging shape) · B27 (justify against persona WTP) · B28 (name ≥1 pricing trap avoided) · B29 (decoy tier — conditional)

---

## 1. EXACT REQUIREMENT

Two decisions, both required:

1. **Freemium** *or* **free-trial**
2. **Packaging shape** — tiered / usage-based / hybrid

Plus: justify against the Part A personas' **willingness to pay**, and **explicitly name at least one** of the three pricing traps being avoided — **cost-plus / competitive / gut-feel**. A **decoy tier is optional**; if used, all three tiers must be named along with which one the decoy pushes toward.

**Not required:** specific price points, revenue projections, LTV/CAC modelling, or a market-sizing exercise. **[NOT SPECIFIED BY CAPSTONE]**

---

## 2. THE WTP CONSTRAINT WE ACTUALLY HAVE

From locked Part A (verified against the Airtable Personas table):

| Persona | WTP tier | Acquisition channel |
|---|---|---|
| **Primary** — Household Financial Manager, 33–45, tier-1/2 | **Medium** `[HYPOTHESIS]` | In-app entry banner on PhonePe (owned surface) |
| **Secondary** — Young Urban Salaried Professional, 24–32 | **Medium** `[HYPOTHESIS]` | In-app entry banner on PhonePe (owned surface) |

Two facts about this constraint must be carried honestly into the pricing decision:

1. **Both personas rate Medium, and the rating is a hypothesis, not a finding.** Part A recorded that **no credible source quantifying Indian consumer willingness to pay for a personal-finance / budgeting / subscription-management product was located.** The two Mediums differ in composition — the primary persona has more ability to pay, the secondary more perceived value — but neither is evidenced.
2. **WTP was explicitly *not* the primary segmentation factor** (LA-09 = Expected Retention), partly because it failed to separate the two finalists and is the least-evidenced of the four factors. Part A also recorded that WTP "will directly shape the pricing and packaging decision later in this project." **This is that decision, and it inherits the uncertainty rather than escaping it.**

---

## 3. DECISION 1 — **FREEMIUM**, not free-trial

## ▶ **FREEMIUM** `[PM DECISION]`

### The reason is structural to this feature, not a preference

The locked detection rule (LA-20) requires **at least three consecutive occurrences at a regular interval** before a commitment can be flagged, plus a trigger — an amount increase against the user's own prior charges, or a resumption after a gap.

For a **monthly** commitment, that is roughly **three months of transaction history before the feature can produce its first flag**, and longer before it produces one carrying a trigger.

**A free trial is therefore structurally unable to demonstrate this product's value.** A 7-, 14- or 30-day trial expires before the evidence threshold that makes the product work has been met. The user would experience the trial as an empty screen and conclude the feature does nothing — which is exactly what it would have done, in that window, by design.

**Freemium does not have this problem** because it is not time-boxed: the free tier can sit quietly accumulating history and produce its first genuine flag whenever the pattern actually matures, which is the only moment the product can prove anything.

### Reinforcing reason — it matches the locked primary segmentation factor

**LA-09 locks Expected Retention as the primary factor.** The persona was chosen because the underlying need is permanent and recurs. A pricing model whose entire mechanism is a countdown to expiry is misaligned with a segmentation decision made on the basis of sustained repeat use. **Freemium and retention-first segmentation are the same bet.**

### Reinforcing reason — WTP is Medium and unevidenced

Medium WTP means the user must see value **before** being asked to pay, and an unevidenced Medium means we should not design a model that fails if the true figure is lower. Freemium degrades gracefully under a wrong WTP assumption — the free tier still delivers, and the paid conversion simply underperforms. **A trial-and-paywall model fails hard** if WTP is actually lower than assumed, because the user is dropped at the exact moment the trial ends.

### What was rejected and why

**Free-trial — rejected.** Reason above: the feature's evidence threshold outlasts any reasonable trial window. This is a genuine structural incompatibility, not a stylistic preference.

---

## 4. DECISION 2 — PACKAGING SHAPE: **TIERED**

## ▶ **TIERED** `[PM DECISION]`

### Why usage-based is actively wrong for this feature

Usage-based pricing would charge per insight surfaced or per action taken. Both are unacceptable here:

- **Charging per action taken directly attacks the primary metric.** IACR measures the share of viewed insights that reach a confirmed action. Putting a price on the action introduces a cost the user weighs against acting — the product would be charging for exactly the behaviour it exists to produce.
- **Charging per insight surfaced creates an incentive to over-flag**, which is the failure mode the guardrail metric ARR exists to detect. **A pricing model must not be structurally opposed to the guardrail metric of the same feature.**
- The product's honest value is *not* volume. A good month may produce **zero** flags, because nothing warranted review. **Usage-based pricing would make the product's best outcome its lowest-revenue outcome.**

### Why hybrid is not chosen

Hybrid adds a usage component, and every objection above applies to that component. Hybrid also adds explanation cost for a feature whose central design commitment is that the user understands exactly what is happening.

### Why tiered fits

Tiered separates on **capability**, not on quantity of financial activity. It lets the free tier carry the honest core — observation, evidence, and the user's own judgement — while a paid tier adds breadth. It aligns with a Medium, unevidenced WTP because it allows a single modest paid step rather than a spend-scaling commitment.

### The tier structure `[PM DECISION]`

| Tier | Contains | Rationale |
|---|---|---|
| **Free** | Flagged-commitment detection on the user's PhonePe transaction history, full charge-history evidence, the one-tap stop action, confirmation and undo | The core loop stays free. This is what makes the freemium argument work — and what makes retention possible |
| **Paid** | Breadth and continuity features `[PM DECISION]` — e.g. longer transaction history depth for detection, and proactive notification ahead of an upcoming flagged charge rather than in-app discovery only | Adds convenience and coverage without gating the honest core |

> ### ⚠️ NO PRICE POINT IS STATED — DELIBERATELY
>
> **`[NOT VERIFIED]`** No specific rupee figure is proposed, because **no willingness-to-pay data for this category in India was located** (Part A §8, recorded as a research gap, not an oversight). Naming a price would be a fabricated precise figure of exactly the kind the Capstone warns against elsewhere in the brief.
>
> **The method for setting it, rather than the number:** a willingness-to-pay study on the primary persona — price-sensitivity questioning against the specific free/paid split above — run before any price is committed. **The Capstone does not require a price point; it requires the two decisions above and their justification.** `[NOT SPECIFIED BY CAPSTONE]`

---

## 5. THE PRICING TRAP BEING AVOIDED

## ▶ Primary trap named and avoided: **COST-PLUS PRICING**

**What it would look like here, concretely.** Smart Spend Coach's marginal cost per user is close to trivial: detection is deterministic arithmetic over transaction records the platform already holds (LB-09), and the only variable cost is the model call that generates the explanation sentence — which the Part C token-cost optimisation reduces further by routing formulaic T1 insights to a cheaper path. **Pricing from that cost base would produce a price near zero and would say nothing whatsoever about what the feature is worth to a household that stops a ₹499 monthly charge it no longer wants.** Cost-plus is the trap this feature is *most* exposed to, precisely because its costs are so low that the number feels defensible.

**How the decision avoids it:** the free/paid split above is drawn on **user value** — what the household gains from breadth and proactive coverage — and the price is explicitly deferred to WTP research rather than derived from cost.

### Also avoided, secondarily: **COMPETITIVE PRICING**

The nearest comparators are **bundled and free**: Ask Google Pay ships inside Google Pay at no separate charge, and CRED Money is free to CRED members. Anchoring to them would set the price at zero by imitation — a conclusion reached without ever asking what this feature is worth. **Naming a competitor's price is not a valuation.**

### Not claimed
**Gut-feel** is not named as the avoided trap, because deferring the price to research is not the same as having avoided intuition-based pricing — **no price has been set at all yet.** Claiming to have avoided a trap we have not yet had the opportunity to fall into would be an overclaim.

---

## 6. DECOY TIER (B29 — conditional)

## ▶ **NO DECOY TIER IS USED.** `[PM DECISION]`

The Capstone marks this optional. It is declined for three reasons:

1. **A decoy requires three price points, and we have none.** Constructing a decoy would mean inventing three numbers with no WTP data behind any of them — a fabricated pricing structure dressed as strategy.
2. **A decoy is a deliberate choice-architecture nudge toward a tier the user might not otherwise select.** This feature's entire ethical posture (Task 4: Transparency, User Control) is that the system presents evidence and the user decides. **Engineering the pricing page to steer the decision would contradict the product principle on the screen next to it.**
3. It is optional, so declining costs nothing on the acceptance criteria.

**Because no decoy is used, B29 does not apply** — no three tiers to name, no push direction to state.

---

## 7. REQUIREMENT CHECK

| Req | Requirement | Answer | Status |
|---|---|---|---|
| **B25** | Freemium or free-trial | **Freemium** | ✅ stated, justified structurally |
| **B26** | Packaging shape | **Tiered** | ✅ stated, alternatives rejected with reasons |
| **B27** | Justified against persona WTP | Both personas Medium `[HYPOTHESIS]`; freemium degrades gracefully under a wrong WTP assumption, trial does not; tiered allows a single modest step | ✅ |
| **B28** | ≥1 pricing trap explicitly named as avoided | **Cost-plus** (primary), **competitive** (secondary) | ✅ |
| **B29** | Decoy tier — if used, name three tiers + push direction | **Not used**, with reason | ✅ N/A by choice |

**Nothing invented:** no price point, no conversion rate, no revenue figure, no market size, no competitor price beyond the verified fact that the two named comparators are not separately charged.

---

*Part B Task 5 complete. No decision locked without instruction.*
