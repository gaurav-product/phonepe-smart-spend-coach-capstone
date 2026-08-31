# PART A — TASK 5: PRD-LITE COMPLIANCE & HALLUCINATION AUDIT
**Audits:** `PART_A_TASK5_PRD_LITE.md` (drafted 15 Aug 2026)
**Status: NOTHING LOCKED.** LA-18b and LA-19 – LA-28 remain SET. The 13 locked decisions are untouched.

---

# HEADLINE — 3 THINGS I GOT WRONG

| # | Issue | Why it matters |
|---|---|---|
| **H1** | **I invented a capability the feature does not have.** The PRD defines "wasteful" partly as *"no corresponding usage signal."* Smart Spend Coach analyses **transaction categories** `[CASE DATA]`. It has **no usage data** — it cannot know whether a subscription is being used. This is the core detection logic of the entire feature, resting on a capability that does not exist. | **The single highest marking risk in the document.** An evaluator asking *"how does it know it's wasteful?"* exposes it in one question. |
| **H2** | **I made an unverifiable claim about third-party merchant behaviour, and put it on a user-facing screen.** A26 step 5 states *"any service access continues until the current paid period ends."* PhonePe cannot know this — it varies by merchant. Worse, it exposes a real product truth I had glossed over: **stopping an auto-debit is not the same as cancelling a subscription with the merchant.** | Presents an invented fact to the user, and hides a genuine limitation of the chosen action. |
| **H3** | **"Cancellation" regressed into US3** after we specifically corrected it in the Task 2 pre-lock pass. US3 reads *"…complete the cancellation somewhere else later."* | Reintroduces exactly the overclaim EV-035 was written to prevent. |

Plus two unsupported superlatives, one unverified claim about PhonePe's current app, and one internal contradiction between US1 and the C1 rejection.

---

# AUDIT 1 — CASE DATA VS PM DECISION

| # | Claim | Current wording | Correct classification | Evidence / source | Risk | Required change |
|---|---|---|---|---|---|---|
| 1 | **PhonePe can stop/revoke an AutoPay mandate** | "*Stop future auto-debits… executes on confirm*" | **`[DESIGN ASSUMPTION]`** | None. Plausible (mandates are registered through the payer's UPI app) but **no primary source located** | **HIGH** | Already labelled in §0, but the label must be repeated **inside A26 and US3**, not only in §0. A reader of A26 alone currently sees it as settled |
| 2 | **"One-tap way to act"** | Used throughout | **`[CASE DATA]`** | Capstone: *"a one-tap way to act on each nudge"* | None | Keep. This is the one part of the action that is genuinely case data |
| 3 | **Recurring-commitment detection** (same merchant, regular interval) | "*detects a recurring charge… same merchant, regular interval*" | **`[PM DECISION]`** — derivable from transaction data | Capstone establishes category-level transaction analysis; recurrence detection is a reasonable extension of it | LOW | Label as PM decision. Defensible — it needs only transaction timestamps and payee |
| 4 | **≥3 occurrences threshold** | "*at least three observed occurrences*" | **`[PM DECISION]` — invented number** | Not in the Capstone | MEDIUM | Keep, but label explicitly as a PM-selected threshold, not a rule from the case |
| 5 | **<5 transactions in a category** | Edge Case 1 condition | **`[CASE DATA]`** | Capstone's own worked example: *"a user with fewer than five transactions in a category"* | None | Keep. Cite it as case-supplied — this is a strength |
| 6 | **"Wasteful" detection logic** | "*no corresponding usage signal, an amount increased against its own prior, a commitment past a trial period*" | **MIXED — one valid, two invalid** | See rows 7 and 8 | **HIGH** | **Must be rebuilt.** Only transaction-derivable signals may remain |
| 7 | **"Usage signal"** | "*no corresponding usage signal*" | **`[NOT VERIFIED]` — INVENTED CAPABILITY** | **The feature analyses transaction categories `[CASE DATA]`. It has no usage telemetry, no app-open data, no merchant-side data.** The LMS briefing's illustration referenced a user noticing no matching usage *in their email* — email access is emphatically not in scope | **HIGH** | **DELETE.** Replace with transaction-derivable signals only (see §Required Corrections, C1) |
| 8 | **Trial-period detection** | "*a commitment past a trial period*" | **`[NOT VERIFIED]` — weakly invented** | The feature cannot know a trial existed. It could observe *"a charge began after a period of ₹0 or no charges"*, which is a different and much weaker inference | MEDIUM | **DELETE as written.** If retained, restate as the observable pattern, not as trial knowledge |
| 9 | **Amount increased against its own history** | "*a charge that has increased against its own prior amount*" | **`[PM DECISION]` — valid** | Fully derivable from the user's own transaction history | LOW | **Keep.** This is the one detection signal that survives |
| 10 | **Undo capability** | "*an undo option remains available for a defined window*" | **`[DESIGN ASSUMPTION]`** | Not in the Capstone. A reasonable safety design, but a capability being assumed | MEDIUM | Label as a design assumption. It also carries the same platform dependency as row 1 — undoing a mandate stop means re-authorising |
| 11 | **Paid-period access continues** | "*any service access continues until the current paid period ends*" | **`[NOT VERIFIED]` — INVENTED FACT about third parties** | PhonePe cannot know a merchant's access policy | **HIGH** | **DELETE.** Replace with what PhonePe *can* truthfully state — see §Required Corrections, C2 |
| 12 | **Household subscription behaviour** ("subscriptions taken out by different family members") | A25 | **`[PM INFERENCE]`**, and **scope-ambiguous** | Plausible framing, but as written it can be read as implying visibility into other members' accounts, which LA-28 explicitly excludes | MEDIUM | Reword to *"subscriptions paid from the manager's own account on behalf of different family members"* — preserves the household angle within the locked scope |
| 13 | **NPCI / AutoPay statistics** | A25, 20M revocations | **`[FACT — reported]`** | Business Standard reporting NPCI data; **NPCI did not confirm before press time** | MEDIUM | **Remove from A25** per Audit 5. Correctly labelled where it lives, but it does not belong in a PRD problem statement |
| 14 | **Competitor capability claims** | "*the most capable AI assistant in the market… cannot act*" | **SPLIT: the inability is `[FACT]`; "most capable" is `[NOT VERIFIED]`** | Google Pay help page verifies *"cannot initiate or complete payment transactions"*. Nothing verifies it is the most capable | **HIGH** (superlative) | Keep the verified inability, delete the superlative — see Audit 2 |
| 15 | **PhonePe's current app behaviour** | "*PhonePe shows the individual transactions as they occur but never assembles them into a recurring pattern*" | **`[NOT VERIFIED]`** | I have not verified what PhonePe's app currently does or does not surface | MEDIUM | Reframe as the case premise (*the feature is being explored, i.e. does not exist*) rather than as a claim about the shipped app |
| 16 | **Any statement implying real user research** | — | **NONE FOUND** | Searched: no interviews, surveys, quotes, "users said", or research participants | None | ✅ Clean |
| 17 | **Any statement implying usability evidence** | — | **NONE FOUND** | No usability findings, tester behaviour, or observations claimed | None | ✅ Clean |

**Audits 1 verdict: 4 HIGH-risk classification errors (rows 1, 7, 11, 14), 5 MEDIUM, and a clean bill on fabricated research.**

---

# AUDIT 2 — UNSUPPORTED SUPERLATIVES

| Phrase | Location | Supported? | Required replacement |
|---|---|---|---|
| "the most capable AI assistant in the market" | A25 | ❌ **NO.** I verified Ask Google Pay is Gemini-powered and cannot transact. I did **not** verify it is the most capable | *"a leading AI spend-insight product in this market is documented as unable to initiate or complete payment transactions"* |
| "the market's most capable AI spend-insight product" | A29, Why it matters | ❌ **NO.** Same problem | *"a verified competitor is documented as unable to act on its own insight"* |
| "the one capability Task 2 found missing across the compared market" | A26 | ✅ **YES** — "compared market" is the correct narrow qualifier, and Task 2 defines the comparison set | Keep unchanged |
| "the highest-value story in the set" | A28, US3 | ✅ Internal comparison within five stories I authored | Keep |
| "the smallest story in the set" | A28, US5 | ✅ Internal comparison | Keep |
| "Strongest — real stakes produce real hesitation" | §0 option table | ✅ Internal comparison across four options I authored | Keep |
| "Highest of the loop-closing options" | §0, Option D | ✅ Internal comparison | Keep |
| "C1 is the strategically weakest option available" | A26 | ✅ Internal comparison across the five candidates | Keep |
| "the only metric that fails when the feature explains well and changes nothing" | A29 | ⚠️ **Narrow it.** True of the two metrics in this PRD; stated as if universal | *"the metric in this PRD that fails when the feature explains well and changes nothing"* |
| "the second rarely happens" | A25 | ⚠️ **Unsupported frequency claim** | *"the second is easy to defer indefinitely"* — a mechanism claim, not a frequency claim |

**Two HIGH-risk superlatives, two to narrow. No genuinely supported claim needs weakening.**

---

# AUDIT 3 — RE-EVALUATING THE ONE-TAP ACTION

### 3.1 Does A conflict with the locked feature?
**Yes — confirmed, and the conflict holds under re-examination.** A category-level cap does not act on the *specific flagged commitment*, and a cap cannot constrain a charge that is identical every month. LA-17 (locked) is *"Flagged Commitment + One-Tap Action"* and LA-14 (locked) is an action *on a wasteful recurring household commitment*. **A is ruled out by the locks, not by preference.**

### 3.2 A new finding that changes the B-vs-D calculus
Working through H2 surfaced something the first draft glossed over:

> **`[PM INFERENCE]` Stopping an auto-debit is not the same as cancelling a subscription.** Revoking a mandate stops *PhonePe from paying*; it does not end the user's relationship with the merchant, does not guarantee the merchant stops billing through another rail, and may leave the user in non-payment rather than cleanly cancelled. This is consistent with the reported UPI AutoPay revocation pattern `[FACT — reported]`, where mandates end through failure rather than a clean exit.

**This is a genuine limitation of Option B that the PRD must state, not hide.** It does not disqualify B — a payer-side stop is still a real, useful control — but the PRD cannot describe it as though it resolves the commitment entirely.

### 3.3 Can B legitimately remain primary?

**Yes — and one piece of `[CASE DATA]` I under-weighted decides it.**

The Capstone requires, as one of four mandatory Part B screens, **"a one-tap action-confirmation screen"** `[CASE DATA]`. That is direct case evidence that the action is **completed inside the feature, with a confirmation** — independent of what the action executes. Option D (deep-link) hands the user to another surface, where the confirmation belongs to the mandate flow rather than to Smart Spend Coach. **D fits the required screen list less naturally than B.**

| Criterion | B (stop in place) | D (deep-link) | Winner |
|---|---|---|---|
| Capstone evidence | Required confirmation screen sits naturally inside the feature | Confirmation belongs to another surface | **B** |
| Product logic | Acts on the flagged commitment directly | Same end effect, one screen away | **B**, narrowly |
| Feasibility | `[NOT VERIFIED]` platform dependency | Requires navigation only | **D** |
| Safety | Needs eligibility rule + confirmation + undo | Completes in an existing safeguarded flow | **D** |
| Prototypeability | Equal — a Figma prototype has no backend either way | Equal | Tie |
| Part B continuity | Produces the required confirmation screen and a high-stakes moment to observe | Hand-off friction is observable, but the confirmation screen is off-surface | **B** |
| Part C continuity | Clean action-completion event to measure | Completion happens off-surface — harder to attribute | **B** |

### 3.4 Recommendation

> **B remains the primary PM decision — with three mandatory tightenings, not as currently written.**
>
> 1. **Rename the action to what a payer-side control can truthfully do:** *"Stop future auto-debits from PhonePe for this commitment."* Not "cancel", not "stop the subscription."
> 2. **State the limitation on the confirmation screen itself:** this stops PhonePe paying it; it does not cancel the service with the merchant, and the user may need to do that separately.
> 3. **Repeat the platform-dependency label inside A26 and US3**, not only in §0. A reader of A26 in isolation currently sees a settled capability.
>
> **D remains the documented fallback** and is the *safer* option on feasibility and safety alone — but it is weaker on the two continuity criteria that carry marks, and the required confirmation screen is case evidence for B's shape.

**This recommendation is not made on demo impressiveness.** The deciding input is a mandatory Part B screen specified by the Capstone; the feasibility and safety columns both favour D, and that is stated plainly rather than argued away.

---

# AUDIT 4 — INVENTED NUMBERS

| Number | Where | Source | Status | Keep / change |
|---|---|---|---|---|
| **5 transactions** in a category | Edge Case 1 | **Capstone worked example** — *"a user with fewer than five transactions in a category"* | ✅ **CAPSTONE-REQUIRED (supplied)** | **Keep, and cite as case-supplied.** This is a compliance strength |
| **7 days** (primary metric window) | A29 | **Capstone's own good-metric example** — *"…who take at least one recommended action within 7 days of viewing an insight"* | ✅ **CAPSTONE-SUPPORTED** | **Keep, and cite.** Do not present as my invention |
| **3 occurrences** (detection threshold) | A26, EC1 | Mine | ⚠️ **PM-SELECTED** | Keep, **label as a PM-selected threshold with the reasoning** (fewest points at which an interval can be confirmed rather than guessed) |
| **14 days** (guardrail window) | A29 | Mine | ⚠️ **PM-SELECTED** | Keep, **label**, and keep the stated reasoning (regret surfaces at the next billing cycle) |
| **"a defined window"** (undo) | A26 | Mine — deliberately unspecified | ⚠️ **UNSPECIFIED** | Either specify with a label, or state explicitly that the window is a design decision deferred to Part B |
| **₹499**, **6 months**, **"since March"** | A26 nudge copy | Mine | ⚠️ **ILLUSTRATIVE** | Keep, but mark the whole line as **illustrative copy**, not a specification |
| Any target or baseline | — | — | ✅ **NONE PRESENT** | Verified: no targets, baselines or benchmarks anywhere. Correct |

**No unsupported number is load-bearing. Two Capstone-supplied numbers are currently uncredited — crediting them is free marks.**

---

# AUDIT 5 — PROBLEM STATEMENT

| Requirement | Present? | Note |
|---|---|---|
| Identifies primary persona | ✅ | "mid-career household financial manager… 33–45, tier-1 or tier-2" |
| Cites persona's frustration | ✅ | Commitments accumulating unreviewed; correctly labelled `[PM INFERENCE]` |
| Explains the problem | ✅ | Each charge individually small and auto-debited, so none becomes urgent |
| Explains current limitation | ⚠️ | Present, but contains an **unverified claim about PhonePe's current app** (Audit 1 row 15) |
| Explains consequence | ✅ | Noticing and acting become two tasks on two days |
| Identifies opportunity | ✅ | Close the distance between observation and control |
| Avoids generic statements | ✅ | No "people struggle with money" |
| Claims no unsupported research | ✅ | Explicitly labelled PM-derived |

**Your instruction on the NPCI statistic is correct and I agree.** It is doing rhetorical rather than structural work — the problem statement stands entirely without it, and importing a reported-but-unconfirmed national statistic into a PRD invites a question that has nothing to do with the PRD. **Remove it from A25.** It stays where it belongs, in the Task 2 teardown supporting GAP-1.

**Also remove:** the superlative in Audit 2, the frequency claim *"rarely happens"*, and the unverified app-behaviour claim. A25 becomes shorter and harder to attack.

---

# AUDIT 6 — USER STORIES

| Check | Result |
|---|---|
| 3–5 stories | ✅ 5 |
| Exact format *"As a [persona], I want to [goal], so that [benefit]"* | ✅ All 5, verified by pattern match |
| Every story belongs to C2 | ✅ All 5 |
| Realistic to prototype | ✅ All 5 map to screens |
| **No unapproved capability introduced** | ❌ **FAILS — two stories** |

**US3 — "…complete the cancellation somewhere else later."** Reintroduces the cancellation overclaim that EV-035 was written to prevent. **Must be reworded** to *"…complete the same action somewhere else later."*

**US4 — "a clear confirmation of exactly what was stopped and the ability to undo it."** The undo is a `[DESIGN ASSUMPTION]` carrying the same unverified platform dependency as the stop itself. The story is fine; **the assumption must be labelled where the story is specified.**

---

# AUDIT 7 — INVEST, RE-CHECKED

I re-checked all 30 justifications rather than confirming they exist. **Three problems.**

| # | Story / letter | Problem | Fix |
|---|---|---|---|
| **I1** | **US1 — Valuable** | *"Delivers the first half of the wedge on its own — the user learns about a commitment they were not tracking, which has value even before any action is attached."* **This directly contradicts A26**, where C1 (insight-only) is rejected on the grounds that insight without action has Impact 0.5. **An evaluator reading both will see the PRD arguing insight alone is valuable in one section and near-worthless in another.** | Rewrite as: *valuable as a build increment toward C2 — it is a necessary precondition for every later story — but not shippable as a standalone product, which is precisely why C1 was rejected.* Turns a contradiction into a consistency proof |
| **I2** | **US4 — Independent** | *"Independent as a unit of work"* is defensible but glosses a real conceptual sequence: there is nothing to confirm or undo until US3 exists | Restate honestly: *independent as a unit of work and testable against a stubbed stopped-commitment state; conceptually sequenced after US3* |
| **I3** | **US3 — Estimable** | Correctly flagged as blocked on the platform dependency. ✅ **This one is right and should stay** — it is the model for how the other two should read | No change |

**US1 Independent, Negotiable, Estimable, Small, Testable** — re-checked, all correct.
**US2, US5** — all six re-checked, all correct. US5 is the cleanest story in the set.

---

# AUDIT 8 — METRICS

| Requirement | Result |
|---|---|
| Exactly ONE primary | ✅ Insight-to-Action Completion Rate |
| Exactly ONE guardrail | ✅ Action Reversal Rate |
| Precise formula | ✅ Both |
| Numerator | ✅ Both, explicitly |
| Denominator | ✅ Both, explicitly |
| Time window | ✅ 7 days / 14 days, both stated with reasoning |
| Clear meaning | ✅ Both |
| No invented targets or baselines | ✅ Verified — none present |
| No secondary metric added | ✅ Verified — Part A asks for two, and two are given |

**Part C continuity — verified and strong.** The Part C pilot funnel `[CASE DATA]` runs *…first personalized insight viewed → recommended action taken*. IACR's denominator is nudges first viewed and its numerator is confirmed actions — **it maps exactly onto that final funnel transition.** Part C's Metric Triad can then take IACR as primary and ARR as guardrail, adding only a secondary. No rework will be needed.

**One wording fix only** (Audit 2): narrow *"the only metric that fails…"* to *"the metric in this PRD that fails…"*.

---

# AUDIT 9 — EDGE CASES

| Check | EC1 (insufficient history) | EC2 (mid-month opt-out) |
|---|---|---|
| Concrete condition | ✅ <3 occurrences or <5 category transactions | ✅ Consent withdrawn while nudges live |
| Expected behaviour | ✅ Explicit low-confidence state, occurrence count shown | ✅ Analysis stops, nudges cleared, plain statement |
| Available action | ✅ View history; optional watch control | ✅ Re-enable; any open undo remains |
| Must-not-happen | ✅ No confident claim, no stop action, excluded from IACR denominator | ✅ No continued analysis, no silent reversal, no re-prompt |
| Straightforward to prototype | ✅ **Yes — single screen state. Correctly designated as the Part B edge-case screen** | ⚠️ Harder — a state transition rather than a screen |
| Thresholds labelled | ❌ **<5 not credited to the Capstone; <3 not labelled as PM-selected** | n/a |

**Both edge cases are structurally sound.** EC1 needs only the threshold labelling from Audit 4. **EC2 carries the same dependency issue as elsewhere** — "any open undo remains available" assumes the undo capability (Audit 1 row 10) and must inherit its label.

---

# AUDIT 10 — OUT OF SCOPE

✅ **Exactly one sentence.** ✅ **Protects scope** — excludes commitments outside the user's own PhonePe account, including other household members', which reinforces LA-28 and the Task 2 §0 constraint. ✅ **Does not exclude C2** — detection, insight and the one-tap action all remain in scope for commitments paid through the user's own account.

**No change required. This is the cleanest section in the PRD.**

---

# AUDIT 11 — RELAY-RACE CHECK

```
LOCKED PERSONA (LA-02, household financial manager 33–45)
   ↓ A25 problem statement addresses this persona ✅
LOCKED FEATURE (LA-17, C2)
   ↓ A26 describes C2 and nothing else ✅
PRD (A25–A31)
   ↓ flow produces exactly the four Part B screens the Capstone mandates:
     home entry ✅ · insight detail ✅ · one-tap confirmation ✅ · edge case (EC1) ✅
PART B PROTOTYPE
   ↓ high-stakes confirmation step creates a genuine place for friction to appear ✅
PART B USABILITY OBSERVATION (mandatory: insight→action friction)
   ↓ IACR measures exactly that transition ✅
PART C EXPERIMENT
   ↓ IACR maps to funnel stage "insight viewed → action taken" ✅
```

**The relay is intact and unusually well aligned.** Two watch items, neither a break:

| # | Watch item | Why it matters |
|---|---|---|
| **R1** | **Ambiguity: is the action one tap from the *nudge*, or from the *insight detail* screen?** A26 implies detail-then-action; "one-tap" implies action on the nudge | **This is precisely where the mandatory Part B friction observation will come from.** Leaving it ambiguous is not fatal — but it should be a deliberate, stated design choice, because Part C's hypothesis will target it |
| **R2** | If Option D is ever invoked as the fallback, the action completes off-surface | Would complicate Part C attribution. Note it in the fallback, do not solve it now |

**Nothing in the PRD forces a later relay violation.**

---

# AUDIT 12 — MARKING RISK

## HIGH-RISK ISSUES

| # | Issue | Why it matters | Exact fix |
|---|---|---|---|
| **HR1** | **"No usage signal" — invented capability at the heart of the detection logic** | The feature analyses transaction categories and has no usage telemetry. "How does it know it's wasteful?" is the most obvious evaluator question, and the current answer is a capability that does not exist | Delete. Rebuild "wasteful" from transaction-derivable signals only — see Required Corrections C1 |
| **HR2** | **"Access continues until the paid period ends" — invented fact about third-party merchants, shown to the user** | PhonePe cannot know this. It also conceals that stopping an auto-debit ≠ cancelling a subscription | Delete; replace with the honest limitation — Required Corrections C2 |
| **HR3** | **"Cancellation" in US3 — regression against EV-035** | Reintroduces the exact overclaim we corrected before locking Task 2 | Reword to *"complete the same action somewhere else later"* |
| **HR4** | **Two unsupported superlatives about a competitor** | "Most capable in the market" is unverified. The *verified* claim (cannot transact) is strong enough on its own — the superlative adds risk and no value | Replace with the narrow verified claim |
| **HR5** | **Platform dependency labelled only in §0** | A26 and US3 read as settled capability in isolation, and an evaluator may read only the PRD body | Repeat the `[DESIGN ASSUMPTION]` label inside A26 and US3 |

## MEDIUM-RISK ISSUES

| # | Issue | Why it matters | Exact fix |
|---|---|---|---|
| **MR1** | **US1 "Valuable" contradicts the C1 rejection** | The PRD argues insight-alone is valuable in A28 and near-worthless in A26 | Rewrite as build-increment value — turns a contradiction into a consistency proof |
| **MR2** | **Trial-period detection** | Cannot be known from transaction data | Delete, or restate as the observable charge pattern |
| **MR3** | **Unverified claim about PhonePe's current app** | I have not verified what PhonePe surfaces today | Reframe as the case premise (feature does not yet exist) |
| **MR4** | **"Family members' subscriptions" wording brushes LA-28** | Can be read as implying visibility into other accounts | *"paid from the manager's own account on behalf of different family members"* |
| **MR5** | **NPCI statistic inside A25** | Reported-not-confirmed national statistic imported into a PRD; invites an off-topic challenge | Remove from A25; it remains correctly placed in Task 2 |
| **MR6** | **Capstone-supplied numbers uncredited (<5 transactions, 7 days)** | Crediting them demonstrates compliance; leaving them uncredited looks like invention | Cite both as case-supplied |
| **MR7** | **Undo capability unlabelled** | Assumed capability carrying the same platform dependency | Label as `[DESIGN ASSUMPTION]` in A26, US4 and EC2 |
| **MR8** | **R1: one-tap ambiguity** | Determines where the mandatory Part B friction observation comes from | Make it an explicit, stated design choice |

## LOW-RISK ISSUES

| # | Issue | Fix |
|---|---|---|
| LR1 | "the only metric that fails…" overstated | Narrow to "the metric in this PRD…" |
| LR2 | "the second rarely happens" — unsupported frequency claim | "the second is easy to defer indefinitely" |
| LR3 | Illustrative nudge copy (₹499, 6 months, March) unmarked | Mark the line as illustrative |
| LR4 | 3-occurrence and 14-day thresholds unlabelled | Label as PM-selected, with the reasoning already written |
| LR5 | US4 "Independent" glosses a conceptual sequence | Restate honestly |

---

# REQUIRED CORRECTIONS (exact)

**C1 — Rebuild the "wasteful" definition using transaction-derivable signals only.** Replace *"no corresponding usage signal, an amount increased against its own prior amount, or a commitment past a trial period"* with a definition drawn only from what the user's own transaction history can show. `[AI SUGGESTION — for your approval]` A commitment is flagged when it has run for at least a stated number of consecutive intervals **and** at least one of: (a) the charge amount has increased against its own prior amount; (b) the user holds two or more concurrent recurring commitments in the same category; (c) the commitment's cumulative spend has passed a stated share of that category's total. **All three are computable from transaction data alone, and none assumes knowledge the feature does not have.**

**C2 — Replace the merchant-behaviour claim.** Delete *"any service access continues until the current paid period ends."* Replace with the honest statement of what the action does: *stopping future auto-debits prevents PhonePe from making further payments to this merchant; it does not cancel the user's account with the merchant, and the user may need to do that separately.*

**C3** — Reword US3 to remove "cancellation."
**C4** — Replace both superlatives with the narrow verified claim.
**C5** — Repeat the `[DESIGN ASSUMPTION]` platform-dependency label inside A26 and US3.
**C6** — Rewrite US1 "Valuable" and US4 "Independent" per MR1 and LR5.
**C7** — Remove the NPCI statistic, the app-behaviour claim, and "rarely happens" from A25.
**C8** — Credit the two Capstone-supplied numbers; label the four PM-selected ones.
**C9** — Reword the family-members phrase to stay inside LA-28.
**C10** — Resolve R1 as an explicit design choice.

---

# FINAL DECISION

## **C. NOT SAFE TO LOCK**

**Why not "B — minor fixes":** most of these corrections *are* wording. **HR1 is not.** The definition of "wasteful" is the feature's central inference, and it currently rests partly on data the feature does not have. Fixing it changes what the product detects — that is a substantive change to A26, EC1 and the detection threshold, not a copy edit. **HR2 is also more than wording**, because removing it exposes a real limitation of the chosen action that the PRD must now state honestly.

**What is NOT wrong** — and should not be disturbed when correcting: the structure and section order, the five user stories' format and scope, both metric formulas and their Part C mapping, the out-of-scope line, the edge-case structure, the relay chain, and the absence of any fabricated user research or usability evidence.

**Nothing has been locked.** LA-18b and LA-19 – LA-28 remain **SET**. The 13 locked decisions are untouched. Part B, Figma, usability testing, pricing and Part C not started.

**Awaiting your instruction to apply the corrections.** I have not applied them — you asked for the audit first.
