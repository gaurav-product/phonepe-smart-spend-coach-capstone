# INDEPENDENT COGNITIVE WALKTHROUGH — HEURISTIC EVALUATION
## PhonePe Smart Spend Coach · Figma `XhV4JoExaeeygvEG1LZGez`
**Date:** 16 Aug 2026
**Type: PM/UX heuristic evaluation. NOT usability evidence. NOT tester evidence. NOT B18 evidence.**

---

# ⚠️ TWO LIMITATIONS THAT CONSTRAIN EVERYTHING BELOW

**1. I cannot genuinely see this for the first time.** I authored every screen, wrote every line of copy, chose the CTA position, and audited the file twice. You asked me to "temporarily forget the PRD" and evaluate as a first-time user. **I cannot actually do that, and claiming I had would be its own form of fabrication** — presenting biased evaluation as fresh-eyes evaluation. What follows is a structured heuristic review by someone with complete prior knowledge. That has real value for spotting structural problems. It has **close to zero value as a proxy for what a first-time user would understand**, which is exactly what B18 requires.

**2. I could not fetch fresh renders.** Figma's MCP tool-call limit was reached. This evaluation uses the renders captured earlier in this session — current in all respects except the D2 label change on Screen 04, which I know changed from "View charge history" to "Back to Smart Spend Coach" — plus a **live structural extraction of every text string and interaction performed earlier this turn**, which is current.

**Consequence for the Capstone: nothing in this document may be recorded as a usability observation, quote, error, hesitation, success, or severity rating.** It is a design-review input only.

---

# EVIDENCE SEPARATION — THE THREE SETS MUST NEVER MERGE

## A. REAL TESTER EVIDENCE
**EMPTY.** No real testers have been run. No tester observations, quotes, errors, hesitations, successes or severities exist. The protocol is prepared; the sessions have not happened.

> 🔄 **SUPERSEDED — see §11 Post-Walkthrough Real-Tester Update.** At the time this heuristic report was created, no real testers had been run. Subsequent real-tester sessions were run and are recorded separately in `PART_B_TASK3_REAL_TESTER_EVIDENCE.md`. **The original statement above is preserved as written, not rewritten.**

## B. DESIGNER SELF-WALKTHROUGH
**U-01 to U-18 only.** Gaurav's own walkthrough as the primary persona, Tasks 1–3. **0 Errors · 0 Hesitations · 17 Successes · 1 Quote.** No High-priority insight→action friction observed. Unaltered and not reinterpreted by this document.

## C. INDEPENDENT AI/PM COGNITIVE WALKTHROUGH
**This document.** Heuristic only. Carries no evidentiary weight for Part B Task 3 and cannot supply the B18 baton.

---

# 1. OVERALL UX ASSESSMENT: **8 / 10**

Strong on comprehension architecture and safety; the deductions are about hierarchy competition and one piece of meta-copy — not about correctness.

---

# 2. SCREEN-BY-SCREEN WALKTHROUGH

## 01 · Home entry

**What I notice first:** the amber "PROTOTYPE — illustrative data" banner sits at the very top of the body, above everything. Amber is the strongest attention colour on the screen and it occupies the most valuable position.

**What I think the screen is telling me:** two recurring payments have been looked at; one is worth reviewing, one has too little history. The solid card versus the dashed card carries that distinction visually before the words do.

**What I would naturally tap:** the StreamCo card — it's solid, it has the strongest label, and "Review this charge →" reads as the invitation.

**What I'm looking for:** why this charge and not others.

**What I expect next:** an explanation.

**Unclear:** the section label "1 recurring charge worth reviewing" sits directly above a card chip reading "RECURRING CHARGE WORTH REVIEWING". The same phrase twice in two type treatments, stacked. Not confusing, but it spends hierarchy on repetition.

**What would make me hesitate:** nothing structural.

**Trust:** the "What we observed" label inside the card is doing real work — it frames the statement as an observation before I read it. That is a genuine trust move, not decoration.

## 02 · Insight detail

**What I notice first:** the merchant and ₹499, then the ledger of six dated charges.

**What I think the screen is telling me:** here is the payment history, here is why we flagged it, and the decision is yours.

**What I would naturally tap:** the purple button — it is the only saturated element in the body and sits at the natural end of a top-to-bottom read.

**What I'm looking for:** confirmation the increase is real. The colour-marked ₹499 rows supply it.

**What I expect next:** a confirmation, because "stop" implies consequence.

**Unclear:** nothing in the copy.

**What would make me hesitate:** "Stop future auto-debits" and "Keep this charge" are the same size, stacked, one filled and one outlined. Fill-versus-outline is a standard convention, but the two options are semantically opposed and visually adjacent. A first-time user deciding under uncertainty has to hold both in mind at the same moment.

**Trust:** *"Smart Spend Coach does not know whether you still use this service. It only sees your payments."* This is the strongest single line in the product. It pre-empts the exact objection a sceptical user would raise.

## 03 · Action confirmation

**What I notice first:** the sheet rising over a dimmed version of the previous screen — a familiar, correctly-executed modal pattern.

**What I think the screen is telling me:** here is precisely what changes and what does not.

**What I would naturally tap:** the purple confirm, after reading.

**Unclear:** nothing.

**What would make me hesitate — and this is the most interesting structural observation in the whole walkthrough:** the amber "WHAT WILL NOT CHANGE" block is **visually larger and denser than the green "WHAT WILL STOP" block** — three bullets against one. At the decision moment, the caveats outweigh the action. That is arguably correct for a financial control, and arguably a load that suppresses confirmation. **Which of those it is cannot be determined without users.**

**Trust:** very high. Telling a user what your product *cannot* do, at the moment they are about to act, is the opposite of dark-pattern design.

## 04 · Edge case — not enough history

**What I notice first:** the dashed card and the grey "LOW CONFIDENCE" chip.

**What I think the screen is telling me:** we noticed something but we're not going to draw a conclusion.

**What I would naturally tap:** unclear — both controls are outlined, equal weight, neither primary. By design there is no main action, but the screen doesn't signal that; it simply presents two equal options.

**Unclear:** *"No 'Stop future auto-debits' action is offered in this state."* — **this is meta-copy.** It explains the design's rationale to the user rather than telling the user something about their money. In a shipping product this line would read as a developer note. In a prototype being evaluated it is useful; in a portfolio piece it is a visible seam.

**Trust:** *"We are not saying this charge is fine, and we are not saying it is a problem. We do not have enough to say either."* — an unusually honest empty state.

## 05 · Home — acted-on state

**What I notice first:** the green "AUTO-DEBITS STOPPED" chip. State change is immediately legible.

**What I think the screen is telling me:** it worked, and I can reverse it.

**What I would naturally tap:** nothing — I'm done.

**What would make me hesitate:** **"Undo ↺" is a text link inside the card, not a button.** Every other consequential control in this product is a full-width button. The one control that reverses a financial change has the lowest affordance in the system. Structurally inconsistent with the safety posture everywhere else.

**Trust:** the "What changed" block restates the effect accurately and claims nothing about the merchant.

---

# 3. STRONGEST DESIGN DECISIONS

1. **The observation/interpretation split is architectural, not cosmetic.** Every screen carries a labelled evidence block ("WHAT WE OBSERVED", "WHAT WE HAVE SEEN SO FAR") separate from an interpretation block ("WHY YOU'RE SEEING THIS"). Most products blur these.
2. **Stating the system's ignorance out loud.** "Does not know whether you still use this service" pre-empts the strongest objection to a spend-nudge feature.
3. **The confirmation tells you what it will *not* do.** Naming the limit of your own product at the decision moment is rare and correct.
4. **The edge case refuses to guess** — and says so in plain language rather than hiding the item.
5. **The evidence is shown, not summarised.** Six dated rows with the increase marked lets a user verify rather than trust.

---

# 4. POTENTIAL FRICTION POINTS

| # | Potential friction | Screen | Nature |
|---|---|---|---|
| **P1** | Caveat block visually outweighs the action block at the decision moment | 03 | Hierarchy / cognitive load |
| **P2** | Undo has the lowest affordance of any consequential control in the system | 05 | Affordance inconsistency |
| **P3** | Meta-copy explaining the design's own rationale to the user | 04 | Voice / polish |
| **P4** | Two equal-weight outlined controls with no primary | 04 | Hierarchy |
| **P5** | Semantically opposed CTAs adjacent and same-sized | 02 | Decision load |
| **P6** | Duplicate phrasing between section label and card chip | 01 | Redundancy |
| **P7** | Prototype banner occupies the highest-value position in amber | 01 | Test artefact, not product |

---

# 5. SEVERITY ASSESSMENT

> **⚠️ These use a HEURISTIC scale, deliberately NOT the locked usability severity scale.**
> The locked scale defines HIGH as *"blocks task completion for multiple users"* — a statement about observed user behaviour. **No user behaviour has been observed here.** Applying that scale to heuristic findings would smuggle unearned evidentiary weight into the record. Heuristic labels below are **Design-Notable / Design-Minor / Cosmetic**, and none of them converts to a usability severity without real testing.

| # | Heuristic severity | Reasoning | Would testing change the assessment? |
|---|---|---|---|
| **P1** | **Design-Notable** | Sits precisely at the conversion moment the primary metric measures. Could be reassuring or could suppress action — genuinely indeterminate | **Yes — decisively** |
| **P2** | **Design-Notable** | Guardrail metric ARR depends on undo being findable. Low affordance on the safety net is a structural inconsistency | Yes |
| **P3** | **Design-Minor** | Reads as a designer's note; a portfolio reviewer may notice the seam | Partly — a user may simply skip it |
| **P4** | **Design-Minor** | No action is intended, so ambiguity may be harmless | Yes |
| **P5** | **Design-Minor** | Fill-vs-outline is a standard convention; may be entirely sufficient | Yes |
| **P6** | **Cosmetic** | Redundancy, not confusion | No |
| **P7** | **Not a product issue** | Test artefact. Correctly present for honesty about illustrative data | N/A |

---

# 6. DOES ANYTHING JUSTIFY REDESIGN?

## **No. Nothing here justifies redesigning before user testing — and P1 specifically must NOT be touched.**

**P1 is the highest-value uncertainty in the prototype.** It sits exactly where the locked primary metric measures conversion. If real testers hesitate at the caveat block, that is potentially the genuine B18 finding and the Part C baton. **Redesigning it now would destroy the evidence before it can be collected.** This is the single most important recommendation in this document.

**P2 (undo affordance)** is the only item with a case for pre-emptive fixing, since it is an internal consistency defect rather than a comprehension question. **I still recommend leaving it** — Undo behaviour is on the walkthrough watchlist (W7), and changing it now removes a testable question for a benefit you cannot yet size.

**P3 (meta-copy)** is the one item safe to change at any point, because it is voice rather than behaviour. Even so, there is no urgency, and changing copy mid-study invalidates cross-tester comparison.

**Everything else is below the threshold for action.**

---

# 7. WHAT SHOULD REMAIN UNCHANGED

- **The action-entry position on Screen 02.** Non-negotiable — it is the W1 test point.
- **All copy on Screens 02, 03 and 04** — particularly the "does not know", "we are not saying", and merchant-limitation lines. These carry the locked product boundary.
- **The confirmation structure**, including the caveat block that P1 flags.
- **The absence of an action on the edge case.**
- **Every locked interaction and the component variants.**
- **The prototype banner** — it is the honest disclosure that the data is illustrative.

---

# 8. WHAT SHOULD BE TESTED FURTHER WITH REAL USERS

Ranked by decision value:

1. **P1 — behaviour at the caveat block.** Do users read it, skim it, or stall? Highest-value unknown in the product.
2. **W1 — action-entry discoverability.** Does the six-row ledger delay reaching the action?
3. **P5 / W2 — the Stop-versus-Keep decision.** Which do users tap, and do they understand "Keep" as a real choice or as dismissal?
4. **P2 / W7 — Undo comprehension.** Is it found? Is it read as reversing the payment change or dismissing the card?
5. **P4 / W6 — does the edge case read as intentional or broken?**
6. **W4 — is the "does not know" line noticed at all**, or does it pass unread as boilerplate?

---

# 9. REQUIRED EXPLICIT STATEMENT

> **These findings are heuristic/cognitive-walkthrough findings and are NOT real-user usability evidence.**

They may not be recorded as observations, quotes, errors, hesitations, successes, or severity ratings in Part B Task 3. They may not supply the B18 finding. They may not become the Part C baton. Their only legitimate use is as design-review input and as a prioritised list of what to watch during real testing.

---

# 10. WHAT THE CURRENT REAL-USER EVIDENCE SUPPORTS

**Real-user evidence collected to date: none.** Zero testers have been run.

> 🔄 **SUPERSEDED — see §11.** This section states the position **as of 16 Aug 2026, before real-tester sessions were run.** It is preserved unchanged. The current evidence position is in §11 and in `PART_B_TASK3_REAL_TESTER_EVIDENCE.md`. Do not cite §10 as the current state.

| Requirement | Supported by real-user evidence? |
|---|---|
| **Errors** | ❌ **NO** — none exist from any source |
| **Hesitations** | ❌ **NO** — none exist from any source |
| **Successes** | ⚠️ **Only from the designer self-walkthrough** (17, U-01 – U-18). **Not real-user evidence.** |
| **Quotes** | ⚠️ **One, from the designer self-walkthrough** (U-05). Recorded as a self-walkthrough verbalisation, **not** a tester quote |
| **High-priority insight→action friction** | ❌ **NO** |

### Verbatim, for the record:

> **No High-priority insight→action friction was observed in the completed testing.**

**The B18 requirement is unmet.** Category coverage is also unmet — two of the four required note types (Errors, Hesitations) are empty. Neither gap can be closed by this document, and neither should be closed by invention.

**The only path that can close both is real testers who have never seen the prototype.** The protocol for that is ready.

---

*Heuristic evaluation complete. Figma unmodified. Control Center unmodified. No decision locked. No observations fabricated. Part C not started.*

---
---

# 11. POST-WALKTHROUGH REAL-TESTER UPDATE
### Appended 16 Aug 2026 · **Sections 1–10 above are unaltered**

## 11.1 What changed

- **This heuristic report was created *before* any real tester sessions were run.** That was true when it was written.
- **Real-tester sessions have since been run by Gaurav.** Claude did not observe them; they were reported by the moderator.
- **The real-tester evidence is maintained in a separate document:** `PART_B_TASK3_REAL_TESTER_EVIDENCE.md` (Set A).
- **This report does not become usability evidence.** Its findings P1–P7 remain **heuristic design opinions** on the Design-Notable / Design-Minor / Cosmetic scale. They are not observations, not errors, not hesitations, not severities, and cannot supply B18.
- **Sections 1–10 are not rewritten.** Two statements that are now stale carry a `🔄 SUPERSEDED` marker pointing here. **History is preserved, not edited.**

## 11.2 Provenance-safe restatement

> **At the time this heuristic report was created, no real testers had been run. Subsequent real-tester sessions are recorded separately in the Post-Walkthrough Real-Tester Update and in `PART_B_TASK3_REAL_TESTER_EVIDENCE.md`.**

## 11.3 Current evidence position (summary only — the record lives in Set A)

| | Then (this report) | Now (Set A) |
|---|---|---|
| Errors | 0 | **0** |
| Hesitations | 0 | **2** (OBS-03, OBS-04) |
| Successes | Set B only | **5** real-tester (OBS-01, OBS-02, OBS-05, OBS-06, OBS-07) |
| Quotes | Set B only (U-05) | **1** real-tester (OBS-04) + U-05 still Set B only |
| B18 | Unmet | **Still NOT SATISFIED** — no blocked completion reported |

**Observation IDs OBS-01…OBS-07 are observation records describing one recurring flow pattern. They are NOT seven testers.** The tester count is `[TESTER COUNT — TO BE CONFIRMED]`.

**The verbatim statement in §9 of the previous report — "No High-priority insight→action friction was observed in the completed testing" — remains accurate under the real-tester evidence**, because **no blocked completion has been reported in the supplied evidence**. It now rests on real observation rather than on the absence of it.

## 11.4 Where heuristic findings and real findings appear to align — and why that changes nothing

Real finding **F-01** (action-entry discoverability, ≈12-second search, OBS-03) sits near the area flagged as watchlist item **W1**, and heuristic **P1** remains entirely untested.

**An apparent alignment does not promote a heuristic finding.** P1–P7 keep their heuristic scale and their zero evidentiary weight. F-01 and F-02 carry the locked usability scale and stand on the observation alone. **They must never be cited together as if mutually corroborating** — one is opinion, the other is evidence, and merging them would manufacture confidence that was not earned.

## 11.5 Redesign posture — unchanged and now stronger

The original recommendation was: **do not redesign before testing.** The updated recommendation is: **do not redesign now that partial testing has occurred**, because the prototype is the baseline the remaining sessions and any Part C intervention would be measured against. Figma remains unmodified.

---

*Update appended. Sections 1–10 unaltered. No heuristic finding reclassified. No evidence merged. Figma unmodified. Control Center unmodified. No decision locked. Part C not started.*
