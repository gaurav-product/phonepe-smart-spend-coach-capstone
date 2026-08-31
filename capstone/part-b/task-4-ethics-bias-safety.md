# PART B — TASK 4 · ETHICS, BIAS & SAFETY PASS
## PhonePe Smart Spend Coach

**Requirements covered:** B19 · B20 · B21 · B22 · B23 (five ethics principles) · B24 (exactly one bias type)
**Upstream locked and not reopened:** LA-02 persona · LA-17 C2 · LA-20 detection · LA-18b action · LA-26 edge case · LB-01–LB-08 prototype · LB-09 AI-augmented · LB-10 hallucination rate

---

## 1. EXACT REQUIREMENT

**Ethics (B19–B23), verbatim in substance:** one sentence per principle — **Transparency, User Control, Privacy-by-Design, Fairness, Graceful Failure** — each naming **a concrete design choice your prototype makes or should make.**

**Acceptance criterion explicitly rejects** generic statements such as *"we will be transparent"* with no stated mechanism.

**Bias (B24):** name **exactly one** of **Representation / Measurement / Aggregation / Evaluation** — the one most realistic for a spending-pattern feature tuned on existing transaction data — plus a one-paragraph risk explanation.

**Not required:** a mitigation plan, a governance process, a fairness audit, or more than one bias type. Adding those is presentation, not compliance. **[NOT SPECIFIED BY CAPSTONE]**

---

## 2. THE FIVE ETHICS PRINCIPLES

> Every sentence below names a **specific, locatable design choice**. Where the choice is already built into the prototype it is marked **[BUILT]**; where it is specified in the locked PRD but not depicted on a screen it is marked **[SPECIFIED, NOT DEPICTED]**. Nothing is claimed as built that is not built.

### 2.1 Transparency
> **Smart Spend Coach shows the user the evidence before the conclusion: the insight detail screen carries a "WHAT WE OBSERVED" block listing the six dated charges that triggered the flag, and a separate "WHY YOU'RE SEEING THIS" block naming the specific rule that fired — the amount increased against the user's own prior charges — so the user can check the reasoning rather than being asked to trust a verdict.** **[BUILT — Screen 02]**

*Why this satisfies the criterion:* the mechanism is a named, separated evidence block on a named screen, not a promise of openness.

### 2.2 User Control
> **No auto-debit is ever stopped by a single tap: the action entry opens a mandatory confirmation sheet stating exactly what will stop and what will not change, offering "Go back" as an equal exit, and after confirmation the home screen carries an "Undo" control on the acted-on card — so the user confirms deliberately and can reverse the decision afterwards.** **[BUILT — Screens 02 → 03 → 05]**

*Why this satisfies the criterion:* it names the confirmation gate, the exit, and the reversal control. A change-to-variant shortcut that would have let a single tap bypass the confirmation was built during prototyping and **deliberately removed in QA** (EV-044) for exactly this reason.

### 2.3 Privacy-by-Design
> **Detection reads only the user's own PhonePe transaction record — merchant, amount, date and interval — and the product states this limitation to the user on the insight screen itself: "Smart Spend Coach does not know whether you still use this service. It only sees your payments," which is an on-screen commitment that no email, app-usage, merchant-side or third-party data source is used.** **[BUILT — Screen 02, and LA-20 detection scope]**

*Why this satisfies the criterion:* the mechanism is a data-scope restriction that is both architectural (detection inputs) and user-visible (the on-screen sentence). The feature's most tempting capability — knowing whether a service is still used — was **proposed, found to be invented, and removed** (EV-039). The privacy posture is the result of that removal, not a claim layered on top of it.

### 2.4 Fairness
> **A commitment is only flagged after at least three consecutive occurrences at a regular interval, and a pattern that does not clear that evidence bar receives no stop action at all — it is shown as low-confidence with no action entry — so users with short or sparse PhonePe transaction histories are not pushed toward acting on weak evidence that would be treated as strong for a heavier user.** **[BUILT — Screen 04, edge case; LA-20 base condition; LA-26]**

*Why this satisfies the criterion:* it names an explicit evidence threshold and the specific behaviour when the threshold is not met. **Also specified but not depicted:** the eligibility rule degrades essential-category commitments (insurance, loan EMI, utilities) to a reminder rather than a stop action — locked in the PRD, illustrated with a discretionary example in the prototype. **[SPECIFIED, NOT DEPICTED]**

### 2.5 Graceful Failure
> **When the system has insufficient history it says so in plain language and declines to draw a conclusion in either direction — "We are not saying this charge is fine, and we are not saying it is a problem. We do not have enough to say either" — rather than hiding the item or guessing a verdict from thin data.** **[BUILT — Screen 04]**

*Why this satisfies the criterion:* the mechanism is a specific empty-state behaviour with the failure surfaced to the user, not suppressed.

---

## 3. BIAS — EXACTLY ONE TYPE

## ▶ **MEASUREMENT BIAS**

### The one-paragraph risk explanation

> Smart Spend Coach is exposed to **measurement bias**: the thing it can measure is not the thing it actually cares about. The construct that matters to the user is *"this commitment is no longer worth paying for"* — but nothing in a transaction record contains that. What the feature can observe is a proxy: a charge that recurs at a regular interval, whose amount has increased against the user's own prior charges, or which resumed after a gap. Tuning the feature on existing transaction data risks quietly treating that proxy as if it were the construct, so that a price rise on a service the household uses every day scores identically to a price rise on a service nobody has opened in a year — the data cannot distinguish them, because usage is not in the data. The bias is compounded by which transactions are visible at all: a commitment paid through PhonePe is measurable, while the same household's commitments paid by card, net-banking or another app are invisible, so the feature's picture of a user's recurring spend is systematically partial in a direction it cannot detect. The concrete harm is that the flag reads as a judgement about *worth* when it is only a measurement of *pattern*, and a user who trusts it as the former may stop a commitment they needed.

### Why measurement bias rather than the other three `[PM INFERENCE]`

| Type | Why not chosen |
|---|---|
| **Representation** | Real and present — the PhonePe transacting base is not the Indian population, and heavy users are over-represented. But it is a bias about *who is in the data*, and this feature makes no cross-user comparison: every judgement is made against the **same user's own history**. Representation bias bites hardest on models that generalise across people; this one does not. |
| **Aggregation** | Would apply if one model were forced across groups with genuinely different spending behaviour. The deterministic detection rule is applied per user, so there is no pooled model to mis-fit. |
| **Evaluation** | Would apply if the benchmark used to judge the system were unrepresentative. There is currently **no benchmark at all** — naming this would require inventing an evaluation set that does not exist. |
| **Measurement** ✅ | Chosen because it is not a hypothetical: it is the exact gap the locked product principle already names — the system identifies *patterns that may be worth reviewing*, not *waste*. The bias is structurally present in the feature as designed, and the whole PRD boundary exists to manage it. |

**The strongest reason to name this one:** it is the bias the project has already *acted on*. The invented "usage signal" was removed precisely because it pretended to close the proxy-to-construct gap. The confirmation screen's limitation copy, the "does not know whether you still use this service" line, and the user-decides principle are all responses to measurement bias. **Naming it is consistent with what was built, not an afterthought.**

---

## 4. INTEGRITY CHECK

- Five principles, five sentences, each naming a locatable mechanism — **no "we will be transparent"-style statement anywhere.**
- **Exactly one** bias type named, as required. The other three are discussed only to justify the choice and are clearly not additional answers.
- No fairness audit, governance process, compliance certification or regulatory claim is asserted. **[NOT SPECIFIED BY CAPSTONE]**
- No capability is claimed that the feature does not have. Every **[BUILT]** marker corresponds to locked prototype rows LB-02 – LB-08.
- The one item specified-but-not-depicted (essential-category degradation) is labelled rather than implied.

---

*Part B Task 4 complete. Figma unmodified. No decision locked without instruction.*
