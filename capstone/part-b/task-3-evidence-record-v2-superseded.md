# PART B — TASK 3 · **SET A: REAL TESTER EVIDENCE**
## PhonePe Smart Spend Coach · Figma `XhV4JoExaeeygvEG1LZGez`

**Owner:** Gaurav Kumar Singh
**Record created:** 16 Aug 2026 · **Provenance cleanup applied:** 16 Aug 2026 (v2)
**Session date(s):** `[SESSION DATE — TO BE CONFIRMED]`
**Number of testers:** `[TESTER COUNT — TO BE CONFIRMED]`
**Status:** **SUPERSEDED by `PART_B_TASK3_FINAL_REAL_USER_TESTING_REPORT.md` (v3, 16 Aug 2026).** Preserved unedited as the v2 record. The tester count was subsequently confirmed as **7**; this document's `[TESTER COUNT — TO BE CONFIRMED]` reflects the state of knowledge at the time it was written and is **not** rewritten. Cite v3, not this file.

---

## 0. PROVENANCE AND SCOPE

All content in this document originates from real tester sessions **run by Gaurav** and **reported by Gaurav to Claude** on 16 Aug 2026. Claude did not observe these sessions.

**Everything recorded here is limited to exactly what was supplied.** No tester names, ages, genders, locations, occupations, counts, additional quotes, additional timings, session durations, or demographic details have been invented. Where information is missing it is marked `[TO BE CONFIRMED]` rather than estimated.

### ⚠️ CRITICAL PROVENANCE RULE — OBSERVATION IDs ARE NOT TESTERS

The supplied evidence is an **aggregated recurring pattern across testers**, not a set of individual tester transcripts.

Observation records are therefore numbered **OBS-01 … OBS-07**. This is a **sequence of observation records describing one recurring flow pattern**. It is **not seven testers**, and no statement anywhere in this project may read "7 testers", "all seven testers", or "each of the seven".

**The number of testers is `[TESTER COUNT — TO BE CONFIRMED]` and cannot be derived from the number of observation records.**

*(v2 change: IDs renamed from T-01…T-07 to OBS-01…OBS-07 for exactly this reason. Underlying evidence unchanged.)*

---

## 1. THE THREE EVIDENCE SETS — SEPARATION MAINTAINED

| Set | Contents | Status | May supply B18? |
|---|---|---|---|
| **A · REAL TESTER EVIDENCE** | **This document.** OBS-01 – OBS-07 | **POPULATED** as of 16 Aug 2026 | ✅ Yes — the only set that may |
| **B · DESIGNER SELF-WALKTHROUGH** | U-01 – U-18 (Gaurav walking his own prototype) | Unchanged, unaltered | ❌ No |
| **C · INDEPENDENT AI/PM COGNITIVE WALKTHROUGH** | `PART_B_COGNITIVE_WALKTHROUGH.md`, findings P1 – P7 | Unchanged; heuristic only | ❌ No |

**No item may migrate between sets.** The self-walkthrough quote **U-05** — *"The amount has increased, so I want to see the previous charges before deciding what to do."* — belongs **exclusively to Set B** and is **not** a tester quote. Heuristic findings P1–P7 remain design opinions and are **not** usability findings, even where a real observation appears to sit near one.

---

## 2. REAL-TESTER EVIDENCE TABLE — OBSERVATION ONLY

> **Rule applied throughout:** the "Actual observation" column contains only what was reported to have happened or been said. It contains **no** inference about mental state — no "the tester was confused", no "the tester struggled". Interpretation lives in §3, separately.

| ID | Tester | Category | Screen / Flow | Actual observation | Severity | Exact quote | Evidence |
|---|---|---|---|---|---|---|---|
| **OBS-01** | `[TESTER COUNT — TO BE CONFIRMED]` · reported as a recurring pattern across testers | **Success** | 01 Home entry | First noticed the ₹499 StreamCo Premium card | — | — | `[OBSERVED — reported by moderator; session date TBC]` |
| **OBS-02** | *as above* | **Success** | 01 → 02 | Tapped "Review this charge →" immediately | — | — | `[OBSERVED — reported by moderator]` |
| **OBS-03** | *as above* | **Hesitation** | 02 Insight detail | Searched for approximately 12 seconds before locating the action entry | **MEDIUM** *(candidate)* | — | `[OBSERVED — reported by moderator; timing verbatim as supplied: "approximately 12 seconds"]` |
| **OBS-04** | **At least one tester** · exact number `[TO BE CONFIRMED]` | **Hesitation** + **Quote** | 02 → action | Asked: *"Is this cancelling the subscription?"* | **MEDIUM** *(candidate)* | **"Is this cancelling the subscription?"** | `[OBSERVED — verbatim quote supplied by moderator]` |
| **OBS-05** | `[TESTER COUNT — TO BE CONFIRMED]` | **Success** | 02 → 03 | Eventually tapped the action | — | — | `[OBSERVED — reported by moderator; "eventually" preserved verbatim, no elapsed time supplied]` |
| **OBS-06** | *as above* | **Success** | 03 Action confirmation | Confirmation screen was reported as understood; behavioural/verbal basis not yet supplied — **`[COMPREHENSION BASIS TO BE CONFIRMED]`** | — | — | `[REPORTED — moderator judgement, basis TBC]` |
| **OBS-07** | *as above* | **Success** | Full flow | Completed the flow | — | — | `[OBSERVED — reported by moderator]` |

### Notes attached to specific rows

**OBS-06 — not strengthened.** "Understood the confirmation screen" is a **comprehension judgement made by the moderator**, not a raw behaviour. Whether the tester said so, correctly paraphrased the screen, or simply proceeded was not supplied. Proceeding is not comprehension. This row is deliberately carried at its stated strength and no further.

**OBS-05 — "eventually" preserved.** No elapsed time is attached, because none was supplied. It is **not** merged with the ≈12-second figure in OBS-03.

**OBS-04 — attribution is "at least one".** The evidence was supplied once as a pattern "across the testers" and once as "at least one tester explicitly asked". The **weaker** attribution is recorded. See §7 item 4.

---

## 3. INTERPRETATION — SEPARATED FROM OBSERVATION

| Ref | Observation (§2 — what happened) | Interpretation `[PM INFERENCE]` (what it may mean) |
|---|---|---|
| **OBS-03** | "Searched for approximately 12 seconds before locating the action entry." | Suggests **discoverability friction** at the action entry on Screen 02. The six-row charge ledger sits above the action, so the control is reached only after a scan. This is a *finding-the-control* problem, not an *understanding-the-content* problem. |
| **OBS-04** | Asked: *"Is this cancelling the subscription?"* | Suggests **ambiguity between stopping future PhonePe auto-debits and cancelling the underlying merchant subscription.** This is precisely the distinction the locked PRD boundary rests on. |
| **OBS-01 / OBS-02** | Noticed the ₹499 card; tapped Review immediately | Suggests **home-entry comprehension and entry-point discoverability are working.** No friction evidence exists at this stage. |
| **OBS-05 / OBS-06 / OBS-07** | Eventually tapped; confirmation reported understood; flow completed | Suggests **recovery** after the two frictions above. Recovery is why neither finding reaches HIGH (§5). |

**What the evidence does NOT support:** the conclusion "the design is bad." Two localised issues sit on the insight→action path; the entry, the evidence display, the confirmation and the completion all held. This is a **specific usability issue, not a general design failure.**

---

## 4. FOUR NOTE TYPES — FROM SET A ONLY

| Note type | Count from **real testers** | Items | Requirement met? |
|---|---|---|---|
| **Errors** | **0** | none | ❌ **NOT MET** |
| **Hesitations** | **2** | OBS-03, OBS-04 | ✅ **MET** |
| **Successes** | **5** | OBS-01, OBS-02, OBS-05, OBS-06, OBS-07 | ✅ **MET** |
| **Quotes** | **1** | OBS-04 | ✅ **MET** |

### Errors — explicit statement

> **Errors are not represented in the supplied sessions.**

An **Error** is a wrong action taken, a wrong path followed, or a task failed. None was reported.

- A ≈12-second search is a **hesitation**, not an error.
- A clarifying question is a **hesitation with a verbalisation**, not an error.
- No wrong tap, wrong path, backtrack or task failure was reported.

**No Error has been manufactured to satisfy the four-category requirement.** Three of the four categories are met; Errors is the open gap and can only be closed by observation (§7 item 6).

### Quotes — exactly one

The only real-tester quote supported by the supplied evidence is **"Is this cancelling the subscription?"** No second tester quote exists. The designer self-walkthrough quote U-05 remains **exclusively Set B**.

---

## 5. FINAL FINDINGS AND SEVERITY

**Locked severity guide applied strictly:**
> **HIGH** = blocks task completion for **multiple** users · **MEDIUM** = causes hesitation but recovered from · **LOW** = minor or isolated

### F-01 · Action-entry discoverability
| | |
|---|---|
| **Screen** | 02 Insight detail |
| **Evidence** | OBS-03 — approximately 12-second search before locating the action entry |
| **Severity** | **MEDIUM** *(candidate)* |
| **Status** | **Observed** |

**Why not HIGH:** no blocked completion has been reported. A recurring friction experienced by more than one tester does **not** by itself meet the locked HIGH definition — that definition requires *blocked task completion*.
**Why not downgraded to LOW:** it was reported as a **recurring pattern**, not an isolated instance, and it sits directly on the insight→action path. **Eventual task completion does not erase the friction** — MEDIUM is precisely the category for "causes hesitation but recovered from".

### F-02 · Action-semantics ambiguity
| | |
|---|---|
| **Screen** | 02 → action |
| **Evidence** | OBS-04 — verbatim: **"Is this cancelling the subscription?"** |
| **Severity** | **MEDIUM** *(candidate)* |
| **Status** | **Observed** |

**Why not HIGH:** no blocked completion has been reported; the flow was completed (OBS-07).
**Why not downgraded to LOW:** it goes to the **core locked product boundary** — the feature stops auto-debits and explicitly does not cancel anything with the merchant. A user carrying that ambiguity into the decision is exactly the failure mode LA-25 ARR guards against. **Eventual completion does not downgrade it.**
**Escalation condition:** if a tester is later shown to have acted *believing* the action would cancel the subscription, that is a comprehension failure of a different order and must be re-assessed — potentially as an **Error**, not a Hesitation.

### F-03 · Home-entry comprehension — positive finding
| | |
|---|---|
| **Screen** | 01 Home entry |
| **Evidence** | OBS-01, OBS-02 — ₹499 card noticed; "Review this charge →" tapped immediately |
| **Severity** | **n/a — no defect** |
| **Status** | **Positive finding** |

**Nothing is upgraded to HIGH.**

---

## 6. B18 STATUS

> ## **B18 HIGH-PRIORITY INSIGHT→ACTION FRICTION: NOT SATISFIED BY CURRENT EVIDENCE.**

**Reasoning, stated at the strength the evidence actually supports:**

1. B18 requires a **High-priority** friction on the insight→action path.
2. The locked definition of HIGH requires **blocked task completion for multiple users**.
3. > **No blocked completion has been reported in the supplied real-tester evidence.**
4. > **Because the current evidence contains no reported blocked completion, no HIGH finding is currently justified.**

**On the "multiple users" half of the threshold:** tester count is `[TESTER COUNT — TO BE CONFIRMED]`. **The multiple-user threshold has NOT been numerically verified and is not claimed to have been.** The verdict does not depend on it — the blocked-completion half of the definition is not met regardless of how many testers there were.

*(v2 correction: the earlier wording "every tester completed the flow" asserted more than the moderator explicitly confirmed. It has been replaced with the no-reported-blocked-completion formulation above. Absence of a reported blockage is not the same as confirmation that none occurred — see §7 item 10.)*

**Two frictions do sit exactly on the insight→action path** (F-01, F-02) — right location, insufficient severity. That is a real and substantive result. It is simply not HIGH.

**No HIGH finding has been manufactured.** The only legitimate route to HIGH is **actual observed blocked completion involving multiple users**, per the locked severity definition.

---

## 7. REMAINING MISSING INFORMATION

| # | Missing item | Why it matters | Blocking lock? |
|---|---|---|---|
| 1 | **Exact number of testers** | Required for the record, the write-up, and any future "multiple users" assessment. Cannot be inferred from seven observation records | **Yes** |
| 2 | **Session date(s)** | Every evidence entry needs `[OBSERVED: date]` | **Yes** |
| 3 | **Per-tester attribution** | The record is currently an aggregate. Severity reasoning would be stronger with per-tester data | **Yes** |
| 4 | **How many testers asked the cancellation question** | Recorded as "at least one". If it was all of them, F-02 becomes a stronger MEDIUM — still MEDIUM | High value |
| 5 | **Basis for OBS-06** `[COMPREHENSION BASIS TO BE CONFIRMED]` | Said so? Paraphrased correctly? Or merely proceeded? | High value |
| 6 | **Any errors — wrong taps, wrong paths, backtracking** | The only unmet note-type category | **Yes — for coverage** |
| 7 | **Anything observed on Screens 04 and 05** | Edge case and acted-on/Undo state have **zero** tester evidence of any kind | Medium |
| 8 | **Behaviour at the confirmation caveat block** | Heuristic P1's highest-value unknown; no tester evidence either way | Medium |
| 9 | **Whether testers had prior exposure to the prototype** | Determines whether these are first-exposure observations | Medium |
| 10 | **Whether any tester was blocked and rescued by the moderator** | The protocol sets a ≥45-second rescue threshold. A rescue is a completion-blockage signal and is **the single most B18-relevant missing item** | **Yes — directly B18-relevant** |

---

## 8. REDESIGN DECISION

## **NO FIGMA CHANGES.**

**Reason: the prototype is now the controlled baseline for the remaining testing and for any potential Part C intervention.**

| Item | Decision |
|---|---|
| Screen 02 CTA position | **Do not move** |
| "Stop future auto-debits" wording | **Do not rewrite** |
| Confirmation screen | **Do not change** |
| Cancellation limitation copy | **Do not change** |
| Screen 03 caveat block (heuristic P1) | **Do not redesign** — still untested |
| Anything else in the file | **Do not change** |

Remaining sessions must run against the **unmodified** prototype, or earlier and later sessions become incomparable. **Document first; redesign only as a deliberate, measured Part C intervention.**

---

## 9. IMPLICATIONS FOR THE PART C BATON `[PM INFERENCE — nothing locked]`

Before this evidence, Part C had **no observed friction to carry forward** — only heuristic opinion. It now has two real, located insight→action frictions.

1. **F-01** is the most directly testable: a measured behavioural signal (search time) and an obvious intervention shape, mapping cleanly onto the locked primary metric **IACR**.
2. **F-02** is the higher-stakes finding: it touches the locked boundary between stopping auto-debits and cancelling a subscription, with a direct relationship to the guardrail metric **ARR**.
3. **B18 remains unmet.** A MEDIUM must not be presented as a HIGH to make the relay work. Either further sessions produce a genuine HIGH, or the relay is carried explicitly by the strongest MEDIUM with its severity stated accurately.

**No baton assigned. Nothing locked. Part C not started.**

---

## 10. INTEGRITY STATEMENT

Nothing here was inferred, estimated, rounded, extrapolated or invented. Tester count unstated — not supplied. Session date unstated — not supplied. Per-tester attribution unstated — not supplied. One quote, verbatim; no second quote exists. Zero errors, not manufactured. Zero HIGH severities, not manufactured. Observation IDs are records, not people.

**Control Center unmodified. Figma unmodified. No decision locked. Part C not started.**
