# PART B — TASK 2: AI CLASSIFICATION & RISK
## Planning / audit phase · **NOTHING DECIDED, NOTHING LOCKED**

**Project:** PhonePe Smart Spend Coach Capstone · **Owner:** Gaurav Kumar Singh · **Date:** 16 Aug 2026
**Locked upstream (not reopened):** LA-02 persona · LA-17 **C2** · LA-20 detection logic · LA-18b one-tap action assumption · LA-24 IACR · LA-25 ARR · LA-26 low-confidence edge case · LA-28 out-of-scope · LB-01–LB-08 prototype

---

## 1. EXACT CAPSTONE REQUIREMENTS

**Task wording (verbatim, Part B Task 2):**

> *"Classify the feature as **AI-augmented or AI-native** using the standard distinction between the two, with a **one-paragraph justification tied to how much of the experience would stop functioning without the AI layer**. State which of the **four AI evaluation dimensions (accuracy, response speed/latency, token cost/efficiency, hallucination rate)** is the **single biggest risk** for this specific feature, and **why**."*

**Acceptance criterion (verbatim):**

> *"The AI-augmented/AI-native classification is stated with a justification, and **exactly one** of the four evaluation dimensions is named as the top risk with a stated reason."*

### What is and is not required

| Item | Required? |
|---|---|
| Classification (one of two) | ✅ Required |
| One-paragraph justification tied to what stops working without the AI layer | ✅ Required |
| Exactly **one** of the four dimensions named as top risk | ✅ Required — **"exactly one", not a ranking** |
| A stated reason for that choice | ✅ Required |
| **Mitigation plan** | **[NOT SPECIFIED BY CAPSTONE]** — not required by the task or the acceptance criterion |
| **Monitoring language** | **[NOT SPECIFIED BY CAPSTONE]** — monitoring belongs to Part C Task 4, a different framework |
| **Model/provider/architecture detail** | **[NOT SPECIFIED BY CAPSTONE]** — must not be invented |
| Quantified risk levels or benchmarks | **[NOT SPECIFIED BY CAPSTONE]** |

### ⚠️ FRAMEWORK SEPARATION — Control Center alarm A6

| | Part B Task 2 *(here)* | Part C Task 4 *(later — do not touch)* |
|---|---|---|
| Framework | **4-dimension per-feature risk** | **5-dimension monitoring** |
| Dimensions | accuracy · response speed/latency · token cost/efficiency · hallucination rate | quality · cost · accuracy · operational efficiency · safety |
| Output | name **one** biggest risk | pick **two** to monitor weekly |

The Capstone explicitly warns these are *"a distinct, broader lens… they are not the same list restated."* **Naming a dimension here does not commit Part C.** Part C's two monitoring dimensions remain undecided.

---

## 2. AI CLASSIFICATION — ANALYSIS

### The standard distinction
`[PM DEFINITION]` **AI-native**: the product's core value cannot be delivered without the AI layer — remove it and the feature ceases to exist. **AI-augmented**: AI improves an experience that would still function, in degraded form, without it.

### What the locked feature actually does

Walking LA-20 honestly, component by component:

| Component | Locked definition | Does it require AI? |
|---|---|---|
| Base detection | Same merchant, regular interval, **≥3 consecutive occurrences** | **No.** Deterministic pattern match over transaction timestamps and payee. |
| Trigger T1 | Charge amount **increased vs the user's own previous charges** | **No.** Arithmetic comparison on the user's own history. |
| Trigger T2 | Charge **resumed after a period with no charge** | **No.** Gap detection on a date series. |
| Evidence display | Charge history shown on the insight detail screen | **No.** A read of the same data. |
| One-tap action | Stop future auto-debits (LA-18b) | **No.** A payment-rail operation, not an inference. |
| **Merchant normalisation** | Mapping raw transaction descriptors to a recognisable merchant | **Plausibly yes** `[PM DESIGN ASSUMPTION]` — classification/entity-resolution, commonly ML. **[NOT SPECIFIED BY CAPSTONE]** |
| **Category classification** | Discretionary vs essential — drives the LA-18b eligibility rule | **Plausibly yes** `[PM DESIGN ASSUMPTION]` |
| **Nudge copy generation** | Turning the observation into a short personalised sentence | **Plausibly yes** `[PM DESIGN ASSUMPTION]` |

### ▶ Recommendation: **AI-AUGMENTED**

**Draft one-paragraph justification** `[AI SUGGESTION — for your approval]`:

> Smart Spend Coach is **AI-augmented**, not AI-native. Its detection logic is deterministic: a recurring charge is identified by matching merchant, interval and at least three consecutive occurrences, and it is flagged for review only when the amount has increased against the user's own previous charges or has resumed after a gap — all arithmetic over the user's own transaction history, requiring no model. Remove the AI layer entirely and the feature still detects the commitment, still shows the charge history as evidence, and still offers the one-tap action; what degrades is the *presentation* — raw merchant descriptors instead of recognisable names, weaker discretionary-versus-essential classification, and templated rather than personalised nudge copy. Because the core value chain of observe → evidence → act survives without the model and only the explanation layer depends on it, this is AI enhancing an experience that already works rather than AI constituting it.

**Why not AI-native** `[PM INFERENCE]`: it would be easy — and wrong — to classify this AI-native because the Capstone premise calls it *"an AI-powered feature."* AI-powered and AI-native are not the same claim. The honest test the Capstone actually asks for is *how much of the experience stops functioning without the AI layer*, and for this feature the answer is: the polish, not the function.

**⚠️ A consequence of our own correction, worth stating in the viva.** In the first PRD draft, detection depended on a "usage signal" — knowing whether the service was still being used. That would have made the feature look considerably more AI-native. **That capability was invented and was removed** (EV-039), leaving deterministic detection. **The classification therefore follows from the correction, and demonstrates the relay is intact rather than decorative.**

---

## 3. FOUR-DIMENSION RISK ANALYSIS

**Boundary held throughout:** the system identifies transaction-derived patterns worth reviewing. It does **not** know service usage, merchant-side data, email or app activity, trial status, objective necessity, or whether a commitment is genuinely wasteful. **The user makes the judgement.** No dimension below reintroduces any of those.

### D1 · Accuracy
`[PM INFERENCE]` **Where the risk actually sits.** Because detection is deterministic (§2), the arithmetic is correct by construction — the residual accuracy risk concentrates in the two ML-plausible components: **merchant normalisation** (two distinct merchants collapsing into one, or one merchant fragmenting across descriptors, producing a false interval or a false amount increase) and **category classification** (an insurance premium or a loan EMI classified as discretionary, so the LA-18b eligibility rule offers a stop action where it should have degraded to "remind me").
**Consequence:** the user stops an auto-debit the household needed. Directly measured by **LA-25 ARR**.
**Partially mitigated by design:** screen 02 shows the observed charge history, so the user can verify the pattern before acting.

### D2 · Response speed / latency
`[PM INFERENCE]` **Structurally low for this feature.** The nudge is surfaced asynchronously on a home entry card; nobody is waiting on a response. The user-facing sequence — card → detail → action entry → confirmation — reads already-computed data. Latency would only become material if the copy were generated on screen-open rather than ahead of time, which is `[NOT SPECIFIED BY CAPSTONE]`.
**Traceability note:** latency *would* have been a serious risk for **C4 Pre-Debit Intervention**, which had to fire before a charge executed. C4 was scored and rejected (RICE 1.000), so the feature we actually selected does not carry that exposure.

### D3 · Token cost / efficiency
`[PM DESIGN ASSUMPTION]` Material only if nudge copy is model-generated — **[NOT SPECIFIED BY CAPSTONE]**. If it is, cost scales with users × flagged commitments per period. Detection being deterministic keeps the expensive layer small: only flagged items would ever reach a model, and Edge Case 1 (LA-26) suppresses low-confidence items entirely, further reducing volume.
**Nature of the harm:** a **business** risk, not a user-harm risk. It degrades margin, not trust.

### D4 · Hallucination rate
`[PM INFERENCE]` **The failure mode of the one thing the AI layer is actually for.** In this feature the model's job is *explanation* — stating why a charge was flagged. A hallucination here means the copy asserts something the transaction data does not support: most dangerously, **exactly the capabilities we deliberately removed** — *"you haven't used this service"*, *"your trial has ended"*, *"this subscription is unnecessary"* — or an invented figure or date.
**Why it is uniquely severe here:** the entire product principle is that the system reports what it observed and the user judges. A hallucinated explanation **breaches that boundary directly** — the system would be claiming knowledge it does not have, which is the one thing the locked PRD forbids.
**And it defeats the design mitigation that protects accuracy.** Screen 02's charge history lets a user verify a *pattern*. It does **not** protect against a false *explanation*, because the hallucinated sentence sits immediately beside the true data and carries the same authority. The user has no way to tell that one is derived and the other is fabricated.

---

## 4. BIGGEST-RISK RECOMMENDATION

### ▶ Recommended: **HALLUCINATION RATE** — with Accuracy as the serious alternative

**Draft reason** `[AI SUGGESTION — for your approval]`:

> Hallucination rate is the single biggest AI risk for Smart Spend Coach, because the AI layer's only real job in this feature is explanation. Detection is deterministic, so the arithmetic that decides *whether* to flag a charge cannot hallucinate; what the model produces is the sentence telling the user *why*. If that sentence asserts something the transaction data does not support — that the service is unused, that a trial has ended, that a commitment is unnecessary — it does not merely mislead, it breaks the feature's core principle that the system reports observed patterns and the user decides. Worse, the design safeguard that protects against inaccuracy does not protect against this: the insight screen shows the charge history so a user can verify a pattern, but a fabricated explanation appears alongside that true data with identical authority, giving the user nothing to check it against. For a household financial manager acting on commitments that affect other people, a confident false explanation is the failure most likely to produce an irreversible wrong action and permanent loss of trust.

### The honest counter-case for **Accuracy**
`[PM INFERENCE]` Accuracy is a legitimate answer and the Capstone's own briefing notes lean toward it. Its strengths: the consequence is the most concrete (a needed auto-debit stopped), it is the risk our guardrail metric **LA-25 ARR** actually measures, and it governs the eligibility rule that keeps the stop action away from essential commitments. Its weakness relative to hallucination: deterministic detection structurally lowers it, and the design already mitigates it by showing the evidence.

**Both are defensible. This is your judgement call.** The Capstone requires exactly one — do not hedge in the final document.

**Not recommended:** *response speed/latency* (structurally low; the latency-sensitive candidate C4 was rejected) and *token cost/efficiency* (a margin risk, not a user-harm risk, and contingent on an unspecified implementation).

---

## 5. WHAT REQUIRES YOUR DECISION

| # | Decision | Recommendation | Note |
|---|---|---|---|
| **1** | AI-augmented **or** AI-native | **AI-augmented** | Follows from deterministic detection after the EV-039 correction |
| **2** | Which one of the four is the biggest risk | **Hallucination rate** | Accuracy is genuinely defensible — pick the one you can argue unprompted |
| **3** | Whether to state mitigations at all | Optional | **[NOT SPECIFIED BY CAPSTONE]** — the acceptance criterion asks only for the named risk and a reason. Adding mitigation is presentation, not compliance |
| **4** | Whether to name the ML-plausible components explicitly | Recommended | Merchant normalisation, category classification and copy generation are `[PM DESIGN ASSUMPTION]` — naming them makes the classification concrete and shows you know where the model actually sits |

**No model, provider, API, training pipeline or architecture is named anywhere.** Every implementation detail the Capstone does not specify is labelled `[NOT SPECIFIED BY CAPSTONE]` or `[PM DESIGN ASSUMPTION]`.

**Part C's five monitoring dimensions remain undecided and untouched.**

---

*End of Part B Task 2 planning. Nothing locked. Usability testing, ethics, bias, pricing and Part C not started. Figma prototype unmodified.*
