# PROTOTYPE AUDIT — PRE-WALKTHROUGH
## PhonePe Smart Spend Coach · Figma `XhV4JoExaeeygvEG1LZGez`
**Date:** 16 Aug 2026 · **Purpose:** prepare the Part B Task 3 walkthrough. **No usability findings created.**
**Method:** live extraction of every text string, every interactive element and every destination from the current file — not from memory or screenshots.

---

# 1. SCREEN-BY-SCREEN INVENTORY

## 01 · Home entry — 390×844

| | |
|---|---|
| **Purpose** | Surface one flagged recurring commitment unprompted, plus one low-confidence item |
| **Visible information** | "Smart Spend Coach" / "Your recurring payments, reviewed with you" · **"PROTOTYPE — illustrative data, not real user transactions"** · "1 recurring charge worth reviewing" · card: RECURRING CHARGE WORTH REVIEWING / StreamCo Premium / ₹499 / "Charged every month · last 6 charges" / **What we observed** — "The amount increased compared with your previous charges." · "Not enough history yet" · MusicBox ₹149 / "Seen 2 times · not enough history to flag for review" |
| **Primary CTA** | "Review this charge →" (whole card is the hit target) |
| **Secondary CTA** | "See why →" on the MusicBox entry |
| **Evidence shown** | Interval ("every month · last 6 charges"), the T1 trigger stated as an observation |
| **Decision required** | Whether to look further |
| **Intended next state** | 02 · Insight detail |
| **PRD requirement** | LB-02 · LA-20 detection · LA-26 low-confidence coexistence |
| **[DESIGN REVIEW]** | The card carries the trigger sentence *and* the section label "1 recurring charge worth reviewing" — the same idea in two registers. Not an error; density worth watching. |

## 02 · Insight detail — 390×844

| | |
|---|---|
| **Purpose** | Show the evidence, state why it was flagged, hand the judgement to the user, offer the action entry |
| **Visible information** | Back · "Recurring charge worth reviewing" · StreamCo Premium ₹499 · "Charged approximately every month from your PhonePe account" · **WHAT WE OBSERVED**: 12 Mar ₹399 · 12 Apr ₹399 · 12 May ₹399 · 12 Jun ₹499 · 12 Jul ₹499 · 12 Aug ₹499 · **WHY YOU'RE SEEING THIS**: "The amount increased compared with your previous charges — from ₹399 to ₹499 in June." · **"Smart Spend Coach does not know whether you still use this service. It only sees your payments."** · "You decide whether this commitment is worth keeping." |
| **Primary CTA** | "Stop future auto-debits" — the **action entry** |
| **Secondary CTA** | "Keep this charge" · "← Back" |
| **Evidence shown** | Six dated charges; the ₹399→₹499 step is visible and colour-marked |
| **Decision required** | Act, keep, or leave |
| **Intended next state** | 03 · Confirmation |
| **PRD requirement** | LB-03 · LA-20 T1 · LA-18b action entry · LA-24 IACR measurement point |
| **[DESIGN REVIEW]** | Only trigger **T1** (amount increased) is exercised anywhere in the prototype. **T2** (charge resumed after a gap) is never demonstrated. LA-20 requires *at least one* trigger, so this is compliant — but a viva question "show me T2" has no screen to point at. |

## 03 · Action confirmation — 390×844

| | |
|---|---|
| **Purpose** | Mandatory confirmation before any payment-instruction change |
| **Visible information** | "Stop future auto-debits?" · "StreamCo Premium · ₹499 every month" · **WHAT WILL STOP**: "PhonePe will stop paying this merchant from your next due date, 12 Sep." · **WHAT WILL NOT CHANGE**: the mandated limitation verbatim, plus "You may need to cancel the service with StreamCo separately" and "Payments already made are not affected." · "You can undo this from the Smart Spend Coach card." |
| **Primary CTA** | "Yes, stop future auto-debits" |
| **Secondary CTA** | "Go back" (safe exit) |
| **Decision required** | Confirm or retreat |
| **Intended next state** | 05 · acted-on (confirm) / 02 (go back) |
| **PRD requirement** | LB-04 · LA-18b · C2 limitation |
| **Date check** | ✅ Last charge 12 Aug, monthly interval → next due 12 Sep. Internally consistent. |

## 04 · Edge case — not enough history — 390×844

| | |
|---|---|
| **Purpose** | Implement LA-26: state the absence of confidence rather than guessing |
| **Visible information** | "Not enough history yet" · MusicBox ₹149 · **LOW CONFIDENCE · NOT FLAGGED FOR REVIEW** · WHAT WE HAVE SEEN SO FAR: 14 Jul ₹149, 14 Aug ₹149 · "We've seen this charge only 2 times. That's not enough history for Smart Spend Coach to flag it for review." · **"We are not saying this charge is fine, and we are not saying it is a problem. We do not have enough to say either."** · "No 'Stop future auto-debits' action is offered in this state." |
| **Primary CTA** | "View charge history" |
| **Secondary CTA** | "Tell me if this repeats" |
| **Decision required** | None — comprehension only |
| **PRD requirement** | LB-05 · LA-26 |
| **⚠️ [DESIGN REVIEW — POTENTIAL ISSUE]** | **"View charge history" navigates to Home.** But the charge history is *already on this screen* ("WHAT WE HAVE SEEN SO FAR"). The control is both **redundant** and its **destination contradicts its label**. See §2 defect **D2**. |

## 05 · Home — acted-on state — 390×844

| | |
|---|---|
| **Purpose** | Post-action state with undo |
| **Visible information** | Same header · prototype banner · "1 commitment updated" · **AUTO-DEBITS STOPPED** · StreamCo Premium ₹499 · "Stopped 16 Aug · you can undo this" · **What changed** — "PhonePe will not make further payments to this merchant." · "Undo ↺" · MusicBox entry repeated |
| **Primary CTA** | "Undo ↺" |
| **Decision required** | Keep or reverse |
| **PRD requirement** | LB-07 acted-on variant · US4 · LA-25 ARR measurement point |
| **⚠️ [DESIGN REVIEW — POTENTIAL ISSUE]** | **The MusicBox low-confidence entry is UNWIRED here** but wired on screen 01. Same control, two behaviours. See defect **D1**. |
| **[DESIGN REVIEW]** | Terminology shifts: 01 says "recurring **charge** worth reviewing", 05 says "1 **commitment** updated". Both terms are used in the locked PRD, so neither is wrong — but they are not identical words on adjacent screens. |
| **[DESIGN REVIEW]** | The "does not cancel your subscription" caveat appears only at the decision point (03), not in the persistent acted-on state. Defensible — but a user returning later has no reminder. |

---

# 2. INTERACTION MAP

| Screen | Element → behaviour → destination |
|---|---|
| 01 | Nudge Card (instance) → NAVIGATE → **02 Insight detail** |
| 01 | Low confidence entry → NAVIGATE → **04 Edge case** |
| 02 | "← Back" → NAVIGATE → **01 Home** |
| 02 | **Action entry / Stop future auto-debits** → NAVIGATE → **03 Confirmation** |
| 02 | "Keep this charge" → NAVIGATE → **01 Home** |
| 03 | "Yes, stop future auto-debits" → NAVIGATE → **05 Acted-on** |
| 03 | "Go back" → NAVIGATE → **02 Insight detail** |
| 04 | "← Back" → NAVIGATE → **01 Home** |
| 04 | "View charge history" → NAVIGATE → **01 Home** ⚠️ label/destination mismatch |
| 04 | "Tell me if this repeats" → **no reaction** (deliberate, EV-045) |
| 05 | "Undo ↺" → NAVIGATE → **01 Home** |
| 05 | Low confidence entry → **no reaction** ⚠️ **DEFECT D1** |
| Component set | **No reactions at all** ✅ — confirms the unsafe CHANGE_TO removal (EV-044) held |

**Verification**

| Check | Result |
|---|---|
| Dead-end screens | ✅ None — every screen has ≥1 outgoing link |
| Confirmation bypassable? | ✅ **No.** The only route to the acted-on state is 02 → 03 → Confirm. No variant shortcut exists. |
| Accidental variant change | ✅ None — component set carries zero reactions |
| Undo coherent | ✅ 05 → 01 restores the pre-action home |
| Safe exit coherent | ✅ 03 "Go back" → 02, not home — returns to the decision context |
| Dead controls | ⚠️ **2**: screen 05 low-confidence entry (**D1, unintended**); screen 04 "Tell me if this repeats" (**deliberate**) |

---

# 3. COPY AUDIT

**Automated scan across all five screens for forbidden constructions: 0 hits.** No instance of "wasteful", "unused", "you don't use", "unnecessary", "cancel your subscription" as a product claim, or any model/provider/architecture reference.

| Check | Result | Evidence |
|---|---|---|
| Unsupported capability claimed | ✅ **Clean** | Screen 02 states the opposite explicitly: *"Smart Spend Coach does not know whether you still use this service. It only sees your payments."* |
| Accidental "waste" judgement | ✅ **Clean** | Language is "worth reviewing" / "not flagged for review" throughout |
| Merchant-side claims | ✅ **Clean** | 03 says PhonePe stops paying; explicitly disclaims cancelling the account. No claim about merchant access, refunds or billing |
| Cancellation claims | ✅ **Clean** | *"It does not cancel your account or subscription with the merchant"* + *"You may need to cancel the service with StreamCo separately"* |
| Implies knowledge of usage | ✅ **Clean** | Explicitly denied on 02 |
| Implies objective necessity | ✅ **Clean** | 04: *"We are not saying this charge is fine, and we are not saying it is a problem. We do not have enough to say either."* |
| AI overclaiming | ✅ **Clean** | The word "AI" does not appear on any screen. Consistent with LB-09 AI-augmented |
| Cross-screen consistency | ⚠️ **[DESIGN REVIEW]** | "charge" (01, 02, 04) vs "commitment" (01 card CTA context, 05). Both are locked-PRD vocabulary; not an error |

**This is the strongest part of the prototype.** The copy holds the locked product boundary on every screen, including in the places where it would have been easiest to slip.

---

# 4. EVIDENCE / INTERPRETATION AUDIT

| Screen | OBSERVATION (transaction-derived fact) | INTERPRETATION (what the user is asked to consider) | ACTION |
|---|---|---|---|
| **01** | "Charged every month · last 6 charges" · "The amount increased compared with your previous charges." | "worth reviewing" | Open the detail |
| **02** | Six dated charges with amounts; ₹399→₹499 step visible | "WHY YOU'RE SEEING THIS" names the trigger; then hands over: *"You decide whether this commitment is worth keeping."* | Stop / Keep / Back |
| **03** | Next due date derived from the observed interval | What will stop vs what will not change | Confirm / Go back |
| **04** | Two dated charges | Explicit refusal to interpret | None offered |
| **05** | "Stopped 16 Aug" | "PhonePe will not make further payments to this merchant" — a statement of system state, not an interpretation | Undo |

**Verdict:** ✅ **No screen presents an interpretation as an observed fact.** The separation is architectural — every screen carries a labelled observation block ("WHAT WE OBSERVED" / "WHAT WE HAVE SEEN SO FAR") distinct from the interpretation block ("WHY YOU'RE SEEING THIS"). Screens 02 and 04 additionally state the limits of what the system knows.

---

# 5. VISUAL HIERARCHY AUDIT

| Dimension | Assessment |
|---|---|
| Typography hierarchy | Clear four-level system: screen title 19–22 Bold → merchant 17–18 Semi Bold → body 13–14 → micro-labels 10 Bold uppercase. Consistent across all five |
| **CTA prominence** | **Only the primary action is filled purple.** Every secondary is white with a hairline border. Unambiguous at a glance |
| Card hierarchy | White cards on a slate field, 16px radius, hairline borders. Low-confidence card is dashed — a real visual distinction from the flagged card |
| Spacing | 24px screen gutters, 10–14px between cards, 14–16px card padding. Even |
| Scanability | Uppercase micro-labels act as anchors; the charge list is a two-column ledger |
| Information density | Screen 02 is the densest — six charge rows + three prose blocks + two CTAs, ending 807px into an 844px frame. **Tight but fits.** Nothing is clipped |
| Contrast | Ink `#1A1A2E` on white and white on purple `#5F259F` both comfortably exceed 4.5:1. Muted grey `#6B7280` on white ≈ 4.8:1 — passes AA for body text |
| Consistency | Header block, card treatment and CTA pattern identical across screens |
| Mobile suitability | 390×844 (iPhone 14 class). CTA tap targets ≥48px tall |
| **Is the most important action discoverable?** | **[WATCH DURING WALKTHROUGH]** — the action entry sits at the *bottom* of screen 02, after six charge rows and three prose blocks. On a 390×844 frame the content ends at 807px, so it is visible without scrolling in the prototype. **Whether it is noticed is exactly what the walkthrough must find out — I am not pre-judging it.** |

---

# 6. PERSONA CONSISTENCY

**Primary — household financial manager (LA-02).** The scenario is a recurring commitment paid from their own account, with a price increase they did not authorise consciously. The confirmation's "what will not change" block speaks to someone whose decisions affect other people. ✅ Coherent.

**Secondary — young urban salaried professional (LA-03).** Same flow works; a ₹499 monthly streaming charge with a mid-year price rise is equally plausible for this segment. The household framing is not visible in the prototype copy, so nothing excludes the secondary persona. ✅ Coherent.

**No additional persona needs invented.**

---

# 7. PRD → FIGMA TRACEABILITY

| PRD requirement | Figma screen | Visible implementation |
|---|---|---|
| **C2** — Flagged Commitment + One-Tap Action | 01 → 02 → 03 → 05 | One flagged commitment, surfaced, evidenced, actioned |
| **LA-20** — transaction-derived detection | 01, 02 | Interval + occurrence count + T1 amount increase, shown as a dated ledger. **T2 not demonstrated** (compliant — only one trigger required) |
| **LA-18b** — action entry → mandatory confirmation | 02 → 03 | Entry on 02, confirmation on 03, no bypass |
| **LA-24 IACR** | 02 (denominator: insight viewed) → 03 Confirm (numerator: confirmed action) | Both measurement points exist as distinct screens |
| **LA-25 ARR** | 05 "Undo ↺" | The reversal event is a real control |
| **LA-26** — low-confidence edge case | 04 | Dashed card, LOW CONFIDENCE chip, occurrence count, explicit refusal to judge, **no action entry** |
| **LA-28** — user's own PhonePe account only | 02 | "Charged approximately every month **from your PhonePe account**". No other member's data anywhere |
| **Product principle** | 02, 04 | Two explicit "we do not know" statements |

✅ **Every locked requirement has a visible implementation.**

---

# 8. CAPSTONE COMPLIANCE (against locked LB-01–LB-08)

| Requirement | Status | Evidence |
|---|---|---|
| ≥4 screens | **PASS** | 5 built, all 390×844 |
| Home-screen entry point | **PASS** | 01 |
| Insight detail | **PASS** | 02 |
| One-tap action-confirmation screen | **PASS** | 03 |
| Edge-case screen matching a Part A edge case | **PASS** | 04 = LA-26 |
| ≥1 component | **PASS** | "Nudge Card" |
| ≥1 variant | **PASS** | State=Default / State=Acted-on |
| ≥3 interactions | **PASS** | 10 NAVIGATE wired, 0 dead-end screens |
| Confirmation cannot be bypassed | **PASS** | Only route is 02→03→Confirm |
| **Shareable, anyone-with-link view** | **BLOCKED** | LB-08b — manual, not done |
| T2 trigger demonstrated | **NOT VERIFIED** | Not required; no screen exercises it |

---

# 9. USABILITY-TEST WATCHLIST
**Every item is `[WATCH DURING WALKTHROUGH]`. None is a finding. None becomes a finding unless Gaurav actually experiences it.**

| # | Watch item | Screen |
|---|---|---|
| W1 | **Whether the action entry is noticed** — it sits below six charge rows and three prose blocks. *Possible CTA discoverability point.* **This is the most likely source of the B18 baton and must not be pre-judged or pre-fixed.** | 02 |
| W2 | **Whether "Keep this charge" creates ambiguity** — is it "dismiss", "approve", or "do nothing"? *Possible comprehension issue.* | 02 |
| W3 | **Whether the WHAT WILL NOT CHANGE block is read or skipped**, and whether the merchant limitation lands. *Possible confirmation comprehension issue.* | 03 |
| W4 | **Whether the "does not know whether you still use this service" line is noticed** — it is the product principle made visible. *Possible comprehension point.* | 02 |
| W5 | **Whether the ₹399→₹499 step is spotted unaided** or only after reading the WHY block. *Possible evidence-legibility point.* | 02 |
| W6 | **Whether the absence of an action on the edge case reads as intentional or broken.** *Possible edge-case comprehension issue.* | 04 |
| W7 | **Whether Undo is understood as reversing the payment change** vs dismissing the card. *Possible comprehension issue.* | 05 |
| W8 | **Whether "next due date, 12 Sep" is understood** as when the stop takes effect. *Possible timing comprehension point.* | 03 |
| W9 | **Whether the two home entries are read as two different things** (flagged vs low-confidence) or as one list. *Possible hierarchy point.* | 01 |

---

# 10. WHAT YOU SHOULD **NOT** SAY

Unless you genuinely experience it, do not report any of these — each would become a fabricated finding, and the Part C experiment would then be built on nothing:

- ❌ "The button was hard to find." — only if you actually searched for it
- ❌ "I was confused." — name what specifically was unclear, or don't say it
- ❌ "I didn't understand the recommendation."
- ❌ "The confirmation was unclear."
- ❌ "I hesitated." — only if you actually paused, and you must be able to say what caused the pause
- ❌ "Users would probably…" / "A real user might…" — that is a hypothesis, not an observation
- ❌ "It took too many taps." — only if you counted and it felt like too many *to you, in the moment*
- ❌ Any severity rating assigned to make the rubric work
- ❌ Any reaction to the two known prototype limitations: **"Tell me if this repeats" has no destination** (deliberate), and — until fixed — **the MusicBox card on screen 05 does nothing**

**"That was clear, I knew exactly what to do" is a real finding.** It records as a Success. A walkthrough that produces mostly Successes is a legitimate result.

---

# POST-AUDIT SUMMARY

## 1. Overall prototype quality: **8.5 / 10**

Strong on the things that carry marks: copy discipline is close to flawless, the evidence/interpretation separation is architectural rather than cosmetic, every locked PRD requirement is visibly implemented, and the confirmation cannot be bypassed. Loses points for two wiring inconsistencies (§below), one control whose label contradicts its destination, and only one of the two locked detection triggers being demonstrable.

## 2. Actual defects to FIX before usability testing

**D1 — Screen 05: the MusicBox low-confidence entry is unwired**, while the identical control on screen 01 navigates to screen 04. Same control, two behaviours, one screen apart. If you tap it during the walkthrough you will record a false error. **Fix: wire it to 04, matching screen 01.**

**D2 — Screen 04: "View charge history" navigates to Home**, but the charge history is already displayed on that screen ("WHAT WE HAVE SEEN SO FAR"). The control is redundant *and* its destination contradicts its label. **Recommend relabelling to "Back to Smart Spend Coach"** — it preserves the control, removes the contradiction, and changes no product decision. Removing it entirely is the alternative.

Both are prototype-wiring defects, not product defects. Neither touches a locked decision.

## 3. Issues that must NOT be fixed yet — they need to be tested first

- **W1 — action-entry discoverability on screen 02.** This is the single most likely source of the mandatory B18 insight→action observation. **Fixing it now would destroy the evidence the Part C experiment is supposed to be built on.**
- **W2 — "Keep this charge" ambiguity.** If it confuses you, that is a finding. Pre-solving it forfeits the finding.
- **W3 — whether the WHAT WILL NOT CHANGE block is actually read.**
- **W6 — whether the edge case reads as intentional or broken.**

## 4. Screens to pay closest attention to

**Screen 02 above all** — it is where the insight→action transition happens, where IACR is measured, and where the baton will come from if it comes at all. Then **screen 03** (does the limitation land?) and **screen 04** (does absence read as intentional?).

## 5. Is the prototype safe for the walkthrough?

**Not yet — fix D1 first.** D1 will actively generate a false error. D2 will probably generate one too. Both are five-minute fixes. **After those two, yes.**

## 6. Walkthrough sequence

1. **01 Home entry** — observe, don't tap
2. **01 → 02** via the card
3. **02 Insight detail** — read; note whether you find the action entry unaided *(W1 — the critical moment)*
4. **02 → 03** via the action entry
5. **03 Confirmation** — read both blocks; decide
6. **03 → 05** via Confirm
7. **05 Acted-on** — check Undo comprehension
8. **05 → 01** via Undo
9. **01 → 04** via the MusicBox entry
10. **04 Edge case** — comprehension only; **ignore "Tell me if this repeats" having no destination**

Then repeat as the secondary persona.

---

*Audit complete. No usability findings created. No fabricated observations, quotes, hesitations, errors or successes. Task 3 observations begin only on your instruction.*
