# PART A — TASK 5: PRD-LITE (REVISED v2)
## Requirements A25–A31 · **SET — awaiting Gaurav's lock**

**Project:** PhonePe Smart Spend Coach Capstone · **Owner:** Gaurav Kumar Singh · **Revised:** 15 Aug 2026
**Supersedes:** PRD-lite v1. All 10 corrections from `PART_A_TASK5_PRD_AUDIT.md` applied, with Gaurav's C1 modification.
**Locked upstream (not reopened):** LA-02 primary persona · LA-03 secondary persona · LA-09 Expected Retention · LA-17 selected feature **C2** · LA-14 competitive wedge

**No user research, interviews, surveys, usability tests, quotes or research participants exist for this project. Nothing here claims otherwise.** Persona framing is PM-derived and labelled as such.

---

## ⚠️ ONE ITEM REQUIRING YOUR ACKNOWLEDGEMENT (a locked decision is involved — I have not changed it)

The **locked wedge (LA-14)** reads *"a one-tap action on **wasteful** recurring household commitments."* This revision removes "wasteful" from the **product's own language**, because the feature cannot objectively establish waste (C1).

**I have not altered LA-14.** My reading is that the two are reconcilable and no change is needed:

> The wedge describes the **user's perception and the value we offer** — a household manager who can see waste but cannot act on it. The PRD describes **what the system may assert** — a pattern worth reviewing, with the judgement left to the user. A positioning statement may speak in the user's terms; a specification may not.

**If you disagree, LA-14 needs revising and that is your decision, not mine.** Flagging it rather than letting it pass silently.

---

# 0. THE ONE-TAP ACTION DECISION

`[CASE DATA]` The Capstone establishes that Smart Spend Coach surfaces short personalised nudges **with a one-tap way to act**, and requires **a one-tap action-confirmation screen** as one of four mandatory Part B screens. It does **not** establish what the action executes.

## Options considered

| | Option | User value | Feasibility | Safety | Capstone evidence | Prototypeable | Part B continuity | Part C continuity |
|---|---|---|---|---|---|---|---|---|
| **A** | Apply a spending cap | Low here — a cap cannot constrain a charge that is identical every month | High | Very low | *"suggested weekly cap"* is `[CASE DATA]`, but for a **variance** nudge | Easy | Weak — low stakes | Yes |
| **B** | **Stop future auto-debits** from PhonePe, behind a confirmation | High — a real payer-side control on the flagged commitment | **`[NOT VERIFIED]`** | Needs eligibility rule, confirmation, undo | **The required confirmation screen sits naturally inside the feature** | Easy | **Strong** | **Strong** |
| **C** | Set a reminder to review | Low — defers rather than resolves | Very high | None | Consistent | Easy | Weak | Weak |
| **D** | Deep-link into mandate management, pre-selected | Moderate-High — removes search friction, completes one screen away | **Highest of the loop-closing options** | **Low — completes in an existing safeguarded flow** | Confirmation belongs to another surface | Easy | Moderate | Moderate — completion happens off-surface |

## Recommended decision

> **Option B — "Stop future auto-debits from PhonePe for this commitment."**
>
> **Eligibility rule** `[PM DECISION]`: offered for **discretionary** recurring commitments only. For commitments in essential categories — insurance, loan EMIs, utilities, school fees — the insight is still surfaced but the action degrades to *"Remind me before the next charge."*
>
> **Documented fallback:** if the platform capability is not confirmed, the action degrades to **Option D** — a one-tap entry into mandate management with the commitment pre-selected. The PRD, prototype, metrics and Part C experiment all survive; only the final screen changes.

## Reasoning

**Why not A.** The cap is `[CASE DATA]` for a *food-delivery variance* nudge — a discretionary category. LA-17 (locked) is about **recurring commitments**, and a cap cannot constrain a charge that is identical every month. Choosing A would contradict a locked decision.

**Why not C.** Safest and easiest, and it fails the thing the wedge exists to fix — it converts the insight into a future chore.

**Why B over D — and what D wins on.** `[FACT]` **Ask Google Pay is documented as unable to initiate or complete payment transactions.** Both B and D beat that. **D is genuinely better on feasibility and safety, and that is not argued away.** B is selected because the Capstone **requires a one-tap action-confirmation screen inside the prototype** `[CASE DATA]` — direct case evidence that the action completes within the feature — and because a completion event on-surface is cleanly attributable in Part C. The deciding input is a mandatory Capstone screen, not demo appeal.

## Status

> ### `[DESIGN ASSUMPTION — PLATFORM CAPABILITY NOT VERIFIED]`
> **The selected PM design assumes PhonePe can execute the payer-side auto-debit stop from the Smart Spend Coach flow. This is not established by the Capstone and must be validated before implementation.** Option D is retained as the documented fallback.

---

# A25. PROBLEM STATEMENT

A mid-career household financial manager — typically 33–45, in a tier-1 or tier-2 city, and the one person in the home who watches the money — carries a set of recurring commitments that accumulate quietly: subscriptions and services paid from their own PhonePe account on behalf of different household members, signed up at different times and never revisited together. `[PM INFERENCE — persona framing derived from the locked Task 1 analysis; no user research was conducted and none is claimed]` Each charge is individually small and debits automatically, so no single one becomes urgent enough to deal with, and the household manager has no moment at which the full set is put in front of them. `[CASE DATA]` PhonePe is only now exploring a feature that would surface this — so today the transaction history contains the pattern but nothing assembles it into something a person can act on, and `[FACT]` the means of stopping a recurring payment sits in a separate mandate screen with no insight attached to it. The consequence is that noticing a commitment and doing something about it are two separate tasks on two different days, and the second is easy to defer indefinitely. The opportunity is to close that distance: surface the specific recurring commitment worth reviewing, and put a supported control in the same place as the observation.

---

# A26. CHOSEN SOLUTION

## C2 — Flagged Commitment + One-Tap Action

### The core principle of this feature

> **Smart Spend Coach does not know that a commitment is wasteful.** It analyses the user's own transaction categories `[CASE DATA]` and identifies **transaction patterns that may indicate a commitment is worth reviewing**. It surfaces the pattern and the evidence behind it; **the user decides whether the commitment is actually unnecessary.** All product language reflects this — *"flagged for review"*, *"recurring charge worth reviewing"*, *"change in recurring spending pattern"* — never a claim that a charge is objectively wasteful.

### Detection — transaction-derived signals only `[PM DECISION]`

**Base condition** — a recurring charge to the same merchant at a regular interval, observed for at least **3 consecutive occurrences** `[PM-SELECTED THRESHOLD — not supplied by the Capstone]`. Three is the fewest at which an interval can be confirmed rather than guessed.

**Plus at least one review trigger:**

| # | Trigger | Why it is derivable |
|---|---|---|
| **T1** | The charge amount has **increased relative to the user's own previous charges** to that merchant | Computed entirely from the user's own transaction history |
| **T2** | The recurring charge **appeared after a previous period with no charge** from that merchant | An observable gap-then-resume pattern in the user's own transaction history |

### What the feature explicitly does NOT know `[NOT VERIFIED — must never be claimed]`

Whether the user actually uses the service · any merchant-side usage or account data · any email or app activity · whether a free trial existed or has ended · whether the commitment is objectively unnecessary. **None of these is available from transaction data, and no part of this PRD assumes them.**

### How the experience works

| Step | Screen | What happens |
|---|---|---|
| **1. Detection** | — | Base condition + at least one review trigger is met on the user's own transactions |
| **2. Home entry card** | **Home entry** | A card surfaces one flagged commitment: merchant, amount, interval, and the specific trigger that flagged it |
| **3. Understand** | **Insight detail** | Tapping the card opens the detail view showing the charge history that produced the flag, so the user verifies the pattern themselves rather than trusting an unexplained recommendation |
| **4. One-tap action entry** | **Insight detail** | The detail screen carries **the one-tap action entry** — *Stop future auto-debits* — which opens the confirmation |
| **5. Confirm** | **Confirmation** *(mandatory Part B screen)* | States exactly what will stop, from when, what will **not** change, and the limitation below. The user confirms |
| **6. Outcome** | **Home entry** | The card moves to an *acted-on* state, with an undo available for a defined window `[DESIGN ASSUMPTION]` |

### `[C10] The one-tap definition — stated explicitly to avoid ambiguity`
The insight is surfaced on the **home entry card**. Tapping the card opens the **insight detail screen**. The insight detail screen contains **the one-tap action entry**. That entry opens the **mandatory confirmation screen**, where the user confirms. **This is a one-tap action entry, not a claim that the entire financial operation completes from a single tap** — the Capstone's *"one-tap way to act"* and its mandatory *"one-tap action-confirmation screen"* are both satisfied by this flow, and a confirmation step is a deliberate safety requirement, not friction to be removed.

### `[C2] Limitation stated on the confirmation screen — a product limitation, not a claim about merchant behaviour`

> **Stopping future auto-debits prevents PhonePe from making further payments to this merchant; it does not cancel the user's account or subscription with the merchant, and the user may need to cancel the service separately.**

`[PM DECISION]` This is a limitation of the payer-side control this product offers. **It makes no claim about what any merchant does** — PhonePe cannot know a merchant's access, billing or refund policy, and the product must not imply otherwise.

### `[DESIGN ASSUMPTION — PLATFORM CAPABILITY NOT VERIFIED]`
**The selected PM design assumes PhonePe can execute the payer-side auto-debit stop from the Smart Spend Coach flow. This is not established by the Capstone and must be validated before implementation.** Option D — a one-tap entry into mandate management with the commitment pre-selected — is retained as the documented fallback.

---

## Rejected Alternative

**C1 — Recurring Spend Digest** *(a periodic summary of recurring commitments, no action attached)*

## Why It Was Rejected

**RICE** — runner-up at **1.800** against C2's **2.800**. C1 scores *higher* on Reach (9 vs 7) and lower on Effort (2 vs 4). It loses on **Impact — 0.5 vs 2.0**, and that single input carries the argument.

**User value** — C1 delivers the half of the job that already works. The problem in A25 is not that the household manager cannot *see* a commitment; it is that seeing it and acting on it are separate tasks. A digest adds a fourth thing to read and a fifth to remember.

**Scope** — genuinely cheaper and faster, which is what makes it tempting. Its scope excludes the one capability the Task 2 teardown found missing across the compared market, so the build would go to the part of the problem already solved.

**Feasibility** — C1 is more feasible, and this is the honest cost of rejecting it. C2 carries a platform dependency C1 does not. That is accepted deliberately, with a documented fallback so it is not a bet on an unverified capability.

**Product strategy** — `[FACT]` **Ask Google Pay is documented as unable to initiate or complete payment transactions.** Building C1 would compete with a Gemini-powered assistant on explanation while declining the one thing it is documented as unable to do. C1 is the strategically weakest of the five candidates precisely because it is the safest.

---

# A27. USER STORIES

| ID | User Story |
|---|---|
| **US1** | As a household financial manager, I want to be shown a specific recurring charge that has been flagged for review, so that I find out about it without having to go looking through my transaction history. |
| **US2** | As a household financial manager, I want to see the charge history that caused a commitment to be flagged, so that I can judge for myself whether it is worth acting on before I do anything. |
| **US3** | As a household financial manager, I want to start the supported action on a flagged commitment from the screen where I saw it, so that I do not have to find and complete the same action somewhere else later. |
| **US4** | As a household financial manager, I want a clear confirmation of exactly what was stopped and what was not, so that I can act on a flag without worrying I have broken something the household depends on. |
| **US5** | As a household financial manager, I want the feature to tell me when it does not have enough history to judge a charge, so that I am not pushed into acting on the basis of thin evidence. |

*`[DESIGN ASSUMPTION — PLATFORM CAPABILITY NOT VERIFIED]` US3 and US4 both depend on the payer-side auto-debit stop described in §0 and A26. Under the Option D fallback, US3 becomes an action entry into mandate management and US4's confirmation is scoped accordingly.*

---

# A28. INVEST VALIDATION

### US1 — Be shown a flagged recurring charge

| INVEST | Validation |
|---|---|
| **Independent** | Fully independent. Detection and surfacing require no other story — a flag can be built and tested before any action exists on it. |
| **Negotiable** | The *what* is fixed, the *how* is open: trigger thresholds, card copy, placement and frequency are all undecided. |
| **Valuable** | **Valuable as a necessary build increment toward C2** — every later story depends on a flag existing. **It is deliberately not claimed to be sufficient as a standalone product experience: insight-only is exactly what C1 was, and C1 was rejected.** |
| **Estimable** | Bounded: a recurrence rule plus two triggers over existing transaction data, and one card surface. No external dependency. |
| **Small** | One detection rule and one card component. Fits a single iteration. |
| **Testable** | Given a seeded history meeting the base condition and one trigger, a card either appears with the correct merchant, amount, interval and trigger, or it does not. |

### US2 — See the charge history behind the flag

| INVEST | Validation |
|---|---|
| **Independent** | Independent of US3 and US4. Depends on a flag existing but is buildable and testable against a stubbed flag. |
| **Negotiable** | Open on presentation: a charge list, a timeline, or plain-language explanation are all viable. |
| **Valuable** | Standalone value in trust. It converts an unexplained recommendation into a verifiable pattern — the precondition for the user acting at all, and the mechanism by which judgement stays with the user. |
| **Estimable** | A read-only view over data already retrieved for detection. Low uncertainty. |
| **Small** | One screen, no writes, no new data. |
| **Testable** | The charges shown must be exactly those that produced the flag, and no others. |

### US3 — Start the supported action where the insight appears

| INVEST | Validation |
|---|---|
| **Independent** | ⚠️ **Partially dependent — stated honestly.** It needs a flag to act on. It is *not* dependent on US2 or US4, and is buildable against a stubbed flag, so the dependency is on data rather than another story's implementation. Not rewritten to force a clean answer. |
| **Negotiable** | Deliberately open — the action may execute in place (Option B) or enter mandate management (Option D). The **one-tap action entry** is fixed; the mechanism is not. |
| **Valuable** | The highest-value story in this set — it is the differentiator, and the one capability a verified competitor is documented as lacking. |
| **Estimable** | ⚠️ **Estimable only once the §0 platform dependency is answered.** Small and confidently sized under Option D; larger and carrying unresolved risk under Option B. Flagged, not assumed. |
| **Small** | Small under either option — one action entry plus one confirmation screen, scoped to **one** commitment at a time. Bulk action is C3, rejected. |
| **Testable** | The action entry produces a confirmation, and confirming produces a recorded stop on that specific commitment and no other. |

### US4 — Confirmation of what was and was not stopped

| INVEST | Validation |
|---|---|
| **Independent** | ⚠️ **Independent as a unit of work and testable against a stubbed stopped-commitment state; conceptually sequenced after US3.** Stated rather than glossed. |
| **Negotiable** | Open: undo window length, wording, and whether undo lives on the card or a separate screen. |
| **Valuable** | Valuable specifically for this persona — household commitments affect other people, so knowing precisely what did **and did not** change is what makes acting reasonable at all. |
| **Estimable** | A state change plus a time-bounded reversal. `[DESIGN ASSUMPTION]` The undo inherits the same unverified platform dependency as the stop itself. |
| **Small** | One confirmation state and one reversal path. |
| **Testable** | Sharply testable, and it defines the guardrail metric in A29: an action confirmed then reversed inside the window is directly countable. |

### US5 — Be told when there is not enough history

| INVEST | Validation |
|---|---|
| **Independent** | Fully independent. An alternative output of the same detection rule as US1; requires nothing else to exist. |
| **Negotiable** | Threshold, wording, and whether a low-confidence item is shown at all or suppressed are open. |
| **Valuable** | Protects the judgement principle the whole feature rests on. For a persona managing other people's commitments, being pushed into a wrong action is worse than not being told. |
| **Estimable** | A threshold check on the existing rule plus one alternative card state. |
| **Small** | One conditional branch and one screen state. The smallest story in this set. |
| **Testable** | Given a history below the threshold, the low-confidence state must appear and the action entry must be absent. |

---

# A29. SUCCESS METRICS

### Primary Success Metric

**Name:** Insight-to-Action Completion Rate (IACR)

**Formula:**

```
           Number of flagged-commitment insights for which the user
           completes and confirms the supported action within 7 days
           of first viewing that insight
IACR  =  ──────────────────────────────────────────────────────────────  × 100
           Number of distinct flagged-commitment insights first viewed
           by users during the same measurement period
```

**Numerator:** distinct flagged-commitment insights reaching a **confirmed** action state (past the confirmation screen), counted once per insight, within 7 days of that insight's first view.
**Denominator:** distinct flagged-commitment insights **first viewed** by a user in the period. Surfaced-but-never-viewed insights are excluded — this measures the insight→action gap, not delivery. Low-confidence items (Edge Case 1) are excluded, since no action is offered on them.
**Time window:** **7 days** from first view, per insight; reported as a rolling weekly figure.

> **`[CAPSTONE-SUPPLIED NUMBER]`** The 7-day window follows the Capstone's own worked example of a precise metric — *"percentage of Smart-Spend-Coach users who take at least one recommended action within 7 days of viewing an insight."* It is not a PM invention.

**Why it matters:** this is the direct measurement of the wedge. `[FACT]` Ask Google Pay is documented as unable to initiate or complete payment transactions, so the value Smart Spend Coach claims is not that the user is *informed* but that the user *finishes*. IACR is the metric in this PRD that fails when the feature explains well and changes nothing. **No baseline or target is proposed** — setting one before any measurement would be an invented number.

### Guardrail Metric

**Name:** Action Reversal Rate (ARR)

**Formula:**

```
           Number of confirmed actions that the user reverses
           (undo, or re-authorises the same commitment)
           within 14 days of confirmation
ARR   =  ──────────────────────────────────────────────────────────────  × 100
           Total number of confirmed actions in the same period
```

**Numerator:** confirmed actions subsequently reversed within 14 days, whether by in-flow undo or by re-authorising the same merchant commitment.
**Denominator:** all confirmed actions in the period.
**Time window:** **14 days** from confirmation; reported weekly. `[PM-SELECTED NUMBER]` Longer than the primary window because regret on a recurring commitment typically surfaces at the next billing cycle rather than immediately.

**Why it matters:** it detects the specific harm this feature can cause. The primary metric rewards getting users to act; unguarded, that incentive rewards pushing users into stopping commitments they needed — especially serious for a household financial manager whose commitments affect other people. A rising ARR means detection is flagging the wrong patterns, the confirmation screen is not explaining consequences clearly, or the flags are pressuring users past their own judgement. **It is also the direct test of the judgement principle in A26: if the product is genuinely leaving the decision with the user, reversals should be rare.**

---

# A30. EDGE CASES

### Edge Case 1 — Not enough history to judge *(designated Part B edge-case screen)*

**Condition:** fewer than **3 observed occurrences** `[PM-SELECTED THRESHOLD]` of a candidate recurring charge, **or** fewer than **5 transactions in the relevant category** `[CAPSTONE-SUPPLIED — the brief's own worked example]`.

**Expected behaviour:** the item is shown in an explicit **low-confidence state**. The card states plainly that Smart Spend Coach has seen this charge only a small number of times and does not have enough history to say whether it is worth reviewing. The number of occurrences observed is shown, so the user can see the basis for the caution.

**Available action:** view the charge history; optionally *"Tell me if this repeats."*

**Must not happen:** no flag-for-review claim, **no action entry offered**, and the item must not enter the IACR denominator — it is not an actionable insight.

**Why this protects trust:** a confident claim built on two or three data points is a sampling error presented as an insight. For this persona the cost is asymmetric — a wrong action on a household commitment affects other people — so the feature must be willing to say it does not have enough to go on. **It is also the clearest expression of A26's principle: the product reports patterns it can evidence and stays silent where it cannot.**

### Edge Case 2 — User opts out of transaction analysis mid-month

**Condition:** the user withdraws consent for transaction analysis while flagged commitments are already surfaced, and possibly while a confirmed action is still inside its undo window.

**Expected behaviour:** analysis stops immediately; no new commitments are detected or flagged. Existing flags are cleared from view rather than left frozen. The user is shown one plain statement of what has stopped, what happens to previously derived insights, and that any action already confirmed remains in effect because it changed a real payment instruction, not a piece of analysis.

**Available action:** re-enable transaction analysis; and if an undo window is still open on a confirmed action, that undo remains available `[DESIGN ASSUMPTION — inherits the §0 platform dependency]` — because withdrawing consent to *analysis* must not strip the user of control over a change they already made.

**Must not happen:** no continued analysis after opt-out, no retention of derived insights beyond the stated policy, **no silent reversal of a confirmed action**, and no re-prompt for consent at the opt-out moment.

**Why this protects trust:** consent withdrawal is the moment a user is most alert to whether a product respects the boundary it advertised. Continuing to analyse, or quietly keeping derived insights, turns a privacy control into privacy theatre — and for a feature reading household financial data that is the failure most likely to end the relationship permanently. Separating *analysis* (which stops) from *actions already taken* (which stand, but stay undoable) is what makes the behaviour both honest and safe.

---

# A31. OUT OF SCOPE

> **Out of scope for this version: any recurring commitment not paid through the user's own PhonePe account — including charges on other UPI apps, credit or debit cards, net banking, cash, or any other household member's account — will not be detected, flagged, or acted upon by Smart Spend Coach.**

*This constrains the feature without excluding its core: detection, insight and the one-tap action entry all remain fully in scope for commitments paid through the user's own PhonePe account. It holds the line established in Task 2 §0 — the household angle is served through the money-manager's own transactions, never by aggregating anyone else's.*

---

## APPENDIX — NUMBER PROVENANCE

| Number | Where used | Provenance |
|---|---|---|
| **Fewer than 5 transactions in a category** | Edge Case 1 | **`[CAPSTONE-SUPPLIED]`** — the brief's own worked edge-case example |
| **7-day metric window** | A29 primary | **`[CAPSTONE-SUPPLIED]`** — the brief's own worked example of a precise metric |
| **3 recurring occurrences** | A26 base condition, Edge Case 1 | **`[PM-SELECTED]`** — fewest at which an interval can be confirmed rather than guessed |
| **14-day guardrail window** | A29 guardrail | **`[PM-SELECTED]`** — regret surfaces at the next billing cycle |
| **Undo window length** | A26, US4, EC2 | **`[PM-SELECTED — deliberately unspecified]`**, deferred to Part B |
| **₹499 · 6 months · "since March"** | *(removed from this revision)* | **`[ILLUSTRATIVE ONLY]`** — no example figures are presented as user data anywhere in this PRD |

**No baselines, targets or benchmarks appear anywhere in this document.**

---

*End of Part A Task 5 (revised). Part B, Figma, usability testing, pricing, Part C and Airtable not started.*
