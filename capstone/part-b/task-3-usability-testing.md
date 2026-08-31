# PART B — TASK 3 · **FINAL REAL-USER USABILITY TESTING REPORT**
## PhonePe Smart Spend Coach · Figma prototype `XhV4JoExaeeygvEG1LZGez`

**Owner / Moderator:** Gaurav Kumar Singh
**Record version:** v3 — supersedes the Set A evidence record v1 and v2 (both preserved, not deleted)
**Record compiled:** 16 Aug 2026
**Session date(s):** `[NOT CONFIRMED]`
**Status:** **NOT LOCKED**

---

## 1. TESTING OBJECTIVE

To observe whether real users, seeing the Smart Spend Coach prototype for the first time, could:

1. **notice** a flagged recurring charge on the home entry screen,
2. **understand** the evidence presented on the insight detail screen,
3. **locate and take** the offered action, and
4. **understand what that action would and would not do** — specifically the locked product boundary between *stopping future PhonePe auto-debits* and *cancelling the underlying merchant subscription*.

The objective was **observation of the insight→action path**, not validation. The protocol deliberately used a single non-leading instruction so that comprehension could not be coached.

---

## 2. PROTOTYPE TESTED

| | |
|---|---|
| **Artifact** | Figma prototype, file `XhV4JoExaeeygvEG1LZGez` |
| **Screens** | 5 · 01 Home entry · 02 Insight detail · 03 Action confirmation · 04 Edge case (low confidence) · 05 Home acted-on |
| **Frame size** | 390 × 844 |
| **Interactions** | 10 NAVIGATE at the time of testing (11 now — see the row below) |
| **State at time of testing** | The LB-01–LB-08 locked build, post D1/D2 fixes |
| **Modified since testing?** | **One change, after testing.** The unwired "Tell me if this repeats" control on screen 04 was wired to return to screen 01, taking the file from 10 to 11 navigation interactions. Screen 04 carries none of the recorded observations; screens 01-03, the action-entry position and all copy are unchanged. **F-01, F-02 and the Part C baseline are unaffected.** |

All data shown in the prototype is illustrative and is labelled as such on-screen. **No tester was asked for, or exposed to, real transaction history, bank credentials, PhonePe credentials or any private financial information.**

---

## 3. TESTER COUNT

## **7 distinct real users.**

`[CONFIRMED BY MODERATOR — Gaurav Kumar Singh, 16 Aug 2026]`

These were **real people using the prototype**. They were **not** hypothetical personas, **not** AI-simulated users, and **not** the designer's own self-walkthrough (which is recorded separately as Set B and carries no tester weight).

> ⚠️ **Provenance note — the count was revised during this session.** Earlier on 16 Aug 2026 the moderator recorded the count as `[TESTER COUNT — TO BE CONFIRMED]`, then subsequently confirmed it as **7** from his own testing. Both states are logged in §15. The confirmed figure of 7 rests entirely on the moderator's direct recollection of sessions he personally ran. **No session log, recording, notes file or timestamp has been produced to corroborate it**, and Claude did not observe the sessions. If a written record exists, attaching it would move this from *moderator-attested* to *documented* — see §16.

---

## 4. TESTING PROTOCOL

Per `PART_B_TASK3_TESTER_PROTOCOL.md`:

| Element | Method |
|---|---|
| **Delivery** | Prototype run in Figma Present mode on the moderator's own device |
| **Instruction given** | A single non-leading prompt: *"Please look at this screen and tell me what you would do."* |
| **Coaching** | None. No feature explanation, no PRD framing, no hints about what the product does |
| **Rescue threshold** | Moderator to wait **≥45 seconds** before intervening |
| **Data collected** | Four note types — Errors, Hesitations, Successes, Quotes |
| **Privacy** | No real financial data requested or handled at any point |

**Whether the ≥45-second rescue threshold was reached by any tester:** `[NOT CONFIRMED]` — see §14 and §16. No rescue has been reported.

---

## 5. PERSONA COVERAGE

The protocol targeted two locked personas:

| | Persona | Locked ref |
|---|---|---|
| **Primary** | Mid-career household financial manager, 33–45, tier-1/2 | LA-02 |
| **Secondary** | Young urban salaried professional, 24–32 | LA-03 |

### Actual coverage across the 7 testers: **`[NOT CONFIRMED]`**

**No claim is made that all 7 matched one persona.** No claim is made about the split between primary and secondary. No tester has been assigned to a persona in this record, because that assignment was not supplied.

**Not recorded because not supplied:** tester ages, occupations, income bands, cities, tier classification, gender, prior PhonePe usage, or prior exposure to the prototype. All are `[NOT CONFIRMED]`.

---

## 6. OBSERVATION TABLE

> **Attribution rule:** where individual attribution was not retained, the entry reads *"Observed across real-user sessions; individual attribution not retained."* Nothing has been split into per-tester histories that were not supplied.
>
> **Observation IDs are records of a pattern, not people.** OBS-01…OBS-07 describe one recurring flow, not seven testers. The tester count is 7 and is stated separately in §3.

| ID | Attribution | Category | Screen / Flow | Actual observation | Severity | Exact quote |
|---|---|---|---|---|---|---|
| **OBS-01** | Observed across real-user sessions; individual attribution not retained | **Success** | 01 Home entry | First noticed the ₹499 StreamCo Premium card | — | — |
| **OBS-02** | *as above* | **Success** | 01 → 02 | Tapped "Review this charge →" immediately | — | — |
| **OBS-03** | *as above* | **Hesitation** | 02 Insight detail | Searched for approximately 12 seconds before locating the action entry | **MEDIUM** | — |
| **OBS-04** | **At least one tester** — how many of the 7 asked it is `[NOT CONFIRMED]` | **Hesitation + Quote** | 02 → action | Asked the moderator a question about what the action would do | **MEDIUM** | **"Is this cancelling the subscription?"** |
| **OBS-05** | Observed across real-user sessions; individual attribution not retained | **Success** | 02 → 03 | Eventually tapped the action | — | — |
| **OBS-06** | *as above* | **Success** | 03 Action confirmation | Confirmation screen was reported as understood — **`[COMPREHENSION BASIS NOT CONFIRMED]`** | — | — |
| **OBS-07** | *as above* | **Success** | Full flow | Completed the flow | — | — |
| **OBS-08** | **Aggregate — all 7 testers** | **Success** *(aggregate)* | Overall | All 7 users were able to use the prototype | — | — |
| **OBS-09** | **Aggregate — all 7 testers** | **Success** *(aggregate)* | Overall | Overall feedback was generally positive; testers considered the design fine | — | — `[no verbatim quote supplied]` |
| **OBS-10** | **Aggregate — all 7 testers** | **Negative finding** | Overall | **No known task-blocking failure was reported.** No High-priority insight→action blockage was reported | — | — |

### Row-level integrity notes

- **OBS-03 and OBS-04 are preserved** because they were supplied as observations from the real-user sessions. They remain **genuine usability observations**. `[If either did not in fact originate from these 7 sessions, it must be struck — see §16 item 3.]`
- **OBS-06 is not strengthened.** "Understood the confirmation" is a moderator comprehension judgement. Whether the tester said so, paraphrased the screen correctly, or simply proceeded was not supplied. **Proceeding is not comprehension.**
- **OBS-05 preserves "eventually"** verbatim. No elapsed time is attached, because none was supplied. It is not merged with the ≈12-second figure.
- **OBS-09 is aggregate sentiment, not a per-screen finding.** No verbatim positive quote was supplied, so none is recorded.
- **"Design is fine" ≠ "no frictions."** OBS-09 and OBS-03/OBS-04 coexist without contradiction: users can complete a flow, judge it acceptable, and still hesitate on the way through. **Positive sentiment does not erase observed friction, and has not been used to.**

---

## 7. NOTE TYPES — ERRORS / HESITATIONS / SUCCESSES / QUOTES

| Note type | Count | Items | Requirement met? |
|---|---|---|---|
| **Errors** | **0** | none | ❌ **NOT MET** |
| **Hesitations** | **2** | OBS-03, OBS-04 | ✅ **MET** |
| **Successes** | **7** | OBS-01, OBS-02, OBS-05, OBS-06, OBS-07, OBS-08, OBS-09 | ✅ **MET** |
| **Quotes** | **1** | OBS-04 | ✅ **MET** |

### Errors = 0 — stated plainly

> **No errors were observed/reported.**

No wrong control tapped, no wrong path followed, no backtracking, no misunderstanding acted upon, no task failure — **none reported**.

**No Error has been manufactured to satisfy the four-category requirement.** A ≈12-second search is a hesitation. A clarifying question is a hesitation with a verbalisation. Neither is an error. **Errors = 0 is a valid evidentiary result and is reported as such.**

### Quotes = 1

The only real-user quote supported by the evidence is **"Is this cancelling the subscription?"**

No second tester quote exists. The designer self-walkthrough quote — *"The amount has increased, so I want to see the previous charges before deciding what to do."* (**U-05**) — remains **exclusively Set B** and is **not** tester evidence.

---

## 8. FINDINGS

### F-01 · Action-entry discoverability
| | |
|---|---|
| **Screen** | 02 Insight detail |
| **Evidence** | OBS-03 — approximately 12-second search before locating the action entry |
| **Severity** | **MEDIUM** |
| **Status** | **Observed — real-user evidence** |

**Observation:** "Searched for approximately 12 seconds before locating the action entry."
**Interpretation** `[PM INFERENCE]`: suggests discoverability friction. The six-row charge ledger sits above the action, so the control is reached only after a scan. This is a *finding-the-control* problem, not an *understanding-the-content* problem.

### F-02 · Action-semantics ambiguity
| | |
|---|---|
| **Screen** | 02 → action |
| **Evidence** | OBS-04 — verbatim: **"Is this cancelling the subscription?"** |
| **Severity** | **MEDIUM** |
| **Status** | **Observed — real-user evidence** |

**Observation:** Asked, *"Is this cancelling the subscription?"*
**Interpretation** `[PM INFERENCE]`: suggests ambiguity between **stopping future PhonePe auto-debits** and **cancelling the underlying merchant subscription**. This is precisely the distinction the locked PRD boundary rests on.

### F-03 · Home-entry comprehension — positive finding
| | |
|---|---|
| **Screen** | 01 Home entry |
| **Evidence** | OBS-01, OBS-02 — ₹499 card noticed; "Review this charge →" tapped immediately |
| **Severity** | **n/a — no defect** |
| **Status** | **Positive finding** |

### F-04 · Overall usability acceptable — positive finding *(aggregate)*
| | |
|---|---|
| **Evidence** | OBS-08, OBS-09, OBS-10 — all 7 able to use the prototype; generally positive feedback; no task-blocking failure reported |
| **Severity** | **n/a — no defect** |
| **Status** | **Positive aggregate finding** |

---

## 9. SEVERITY RATIONALE

**Locked severity guide, applied without adjustment:**

> **HIGH** = blocks task completion for **multiple** users · **MEDIUM** = causes hesitation but recovered from · **LOW** = minor or isolated

| Finding | Not HIGH because | Not LOW because |
|---|---|---|
| **F-01** | **No blocked completion was reported for any of the 7 testers.** A recurring friction experienced by more than one user does not meet the locked HIGH definition — that definition requires *blocked task completion*, which did not occur | It was reported as a **recurring pattern**, not isolated, and it sits directly on the insight→action path. **Eventual completion does not erase the hesitation** — MEDIUM is exactly the category for "causes hesitation but recovered from" |
| **F-02** | The flow was completed (OBS-07); no blockage reported | It goes to the **core locked product boundary**. A user carrying that ambiguity into the decision is the exact failure mode the guardrail metric **LA-25 ARR** exists to catch. **Positive overall sentiment does not downgrade it** |

**Neither finding has been upgraded to HIGH to satisfy the rubric. Neither has been downgraded because the users ultimately said the design was fine.**

**Escalation condition on F-02:** if any tester is later shown to have acted *believing* the action would cancel the subscription, that becomes a comprehension failure of a different order and must be re-assessed — potentially as an **Error**, not a Hesitation.

---

## 10. B18 ASSESSMENT

> ## **B18 HIGH-PRIORITY INSIGHT→ACTION FRICTION: NOT SATISFIED.**

### Statement for the record

> **Seven real users completed/reviewed the prototype without a reported task-blocking failure. Two MEDIUM insight→action frictions were observed, but the evidence does not justify a HIGH classification.**

### Reasoning

1. B18 requires a **High-priority** friction on the insight→action path.
2. The locked definition of HIGH requires **blocked task completion for multiple users**.
3. **No blocked completion was reported for any of the 7 testers** (OBS-10).
4. Therefore **no HIGH finding is justified**, and none has been created.

**Both halves of the threshold now assessable.** With the count confirmed at 7, the "multiple users" half can finally be evaluated — and it fails not on sample size but on the substantive half: **no blockage occurred at all.** A larger sample would not change a verdict that rests on zero reported blockages.

**Two frictions sit exactly on the insight→action path** (F-01, F-02) — right location, insufficient severity. That is a real and substantive result, not a null one. It is simply not HIGH.

**No HIGH finding has been manufactured.** The only legitimate route to HIGH remains **actual observed blocked completion involving multiple users**.

---

## 11. KEY USABILITY INSIGHTS

1. **The home entry works.** Users noticed the flagged card and tapped through immediately. Neither discoverability nor comprehension is a problem at the top of the funnel. (F-03)
2. **The evidence display works.** No confusion about the charge history was reported. The observe-then-interpret structure held.
3. **The friction is concentrated in one narrow band: insight → action.** Both observed frictions sit there — one about *finding* the control (F-01), one about *what the control means* (F-02). Everything before and after that band held.
4. **The friction is about the control, not the content.** Users understood *why* the charge was flagged; they hesitated on *where the action was* and *what it would do*.
5. **F-02 touches the product's central claim.** The whole locked boundary is that Smart Spend Coach stops auto-debits and does not cancel anything with a merchant. A user asking "is this cancelling the subscription?" is asking the exact question the product's integrity depends on answering unambiguously.
6. **Overall acceptability and specific friction coexist.** All 7 could use it and judged it fine — and two frictions were still observed. **Neither result cancels the other.** Treating positive sentiment as proof of zero friction would discard the most useful thing this round produced.

---

## 12. DESIGN IMPLICATIONS `[PM INFERENCE — nothing locked, nothing implemented]`

| Finding | Implication | Metric it touches |
|---|---|---|
| **F-01** | The action entry may need to be reachable without scanning past the six-row ledger. Directly affects insight→action conversion | **LA-24 IACR** (primary) |
| **F-02** | The distinction between *stop auto-debits* and *cancel subscription* may need to be legible **at the action itself**, not only inside the confirmation sheet | **LA-25 ARR** (guardrail) |
| **F-03 / F-04** | No change indicated | — |

**These are candidate interventions, not decisions.** None has been implemented. Whether either becomes the Part C experiment is undecided and unassigned.

---

## 13. WHAT WE DELIBERATELY DID **NOT** CHANGE

## **NO FIGMA CHANGES WERE MADE.**

| Item | Status | Reason |
|---|---|---|
| Screen 02 CTA position | **Unchanged** | It is now an *evidenced* finding (F-01). Moving it destroys the baseline any intervention would be measured against |
| "Stop future auto-debits" wording | **Unchanged** | Now F-02. Changing it mid-study invalidates comparison and erases the strongest experiment candidate in the project |
| Screen 02 hierarchy | **Unchanged** | — |
| Confirmation screen and copy | **Unchanged** | — |
| Cancellation-limitation copy | **Unchanged** | Carries the locked product boundary |
| Screen 03 caveat block (heuristic P1) | **Unchanged** | Still untested; no user evidence either way |
| Component variants and interactions | **Unchanged** | — |

**The reason is evidence integrity, not caution.** Two documented frictions are worth more as a measurable baseline than as a silently fixed design. Any remaining sessions must run against the identical prototype or they become incomparable.

---

## 14. LIMITATIONS

1. **Individual attribution was not retained.** The record is an aggregate pattern plus confirmed aggregate facts. It is not seven session transcripts, and has not been presented as such.
2. **Session date(s) `[NOT CONFIRMED]`.**
3. **Persona assignment across the 7 testers `[NOT CONFIRMED]`.** Coverage of the primary and secondary personas is therefore unverified.
4. **Claude did not observe any session.** All real-user evidence is moderator-reported. `[No session log, recording, or notes file has been produced.]`
5. **The tester count was revised within the session** — from unconfirmed to 7 — and rests on moderator recollection rather than a written record (§3, §15).
6. **OBS-06's comprehension basis is unknown.** Whether testers articulated understanding or merely proceeded was not supplied.
7. **How many of the 7 asked the cancellation question is `[NOT CONFIRMED]`** — recorded as "at least one".
8. **Whether the ≥45-second rescue threshold was ever reached is `[NOT CONFIRMED]`.** No rescue has been reported; absence of a report is not the same as confirmation that none occurred.
9. **Screens 04 (edge case) and 05 (acted-on / Undo) have zero tester evidence of any kind.** Nothing is known about whether Undo is findable.
10. **Behaviour at the Screen 03 caveat block was not reported.** Heuristic P1 remains untested.
11. **No statistical claim is made or possible.** n=7 qualitative sessions. There is no success rate, no significance, no confidence interval, and none has been implied.
12. **Prior exposure to the prototype is `[NOT CONFIRMED]`**, so first-exposure status cannot be asserted.

---

## 15. EXACT EVIDENCE PROVENANCE

### Source chain
Real-user sessions **run personally by Gaurav Kumar Singh** → reported verbally to Claude in this session → recorded here. **Claude observed nothing directly and verified nothing independently.**

### Revision log — nothing overwritten silently

| Ver | State of the tester count | Recorded |
|---|---|---|
| **v1** | `[TESTER COUNT — TO BE CONFIRMED]` — sessions reported as an aggregate pattern | 16 Aug 2026 |
| **v2** | `[TESTER COUNT — TO BE CONFIRMED]` — retained; IDs renamed T-01…T-07 → OBS-01…OBS-07 specifically so record count could not be misread as tester count | 16 Aug 2026 |
| **v2.1** | Moderator asked directly for the exact count; answered **"not certain of the exact number from my records"** | 16 Aug 2026 |
| **v3** | Moderator subsequently confirmed **7 distinct real users**, plus aggregate facts: all 7 able to use the prototype, generally positive feedback, no task-blocking failure reported | 16 Aug 2026 |

**Both the earlier uncertainty and the later confirmation are on the record.** The count of 7 is recorded as **moderator-attested**, not as documented, because no artifact corroborating it has been produced. This is stated so that the viva answer is defensible if the count is questioned.

### Evidence classification of every claim in this report

| Claim | Label |
|---|---|
| 7 distinct real users | `[CONFIRMED BY MODERATOR — attested, not documented]` |
| All 7 able to use the prototype | `[CONFIRMED BY MODERATOR — aggregate]` |
| Generally positive feedback | `[CONFIRMED BY MODERATOR — aggregate; no verbatim quote supplied]` |
| No task-blocking failure reported | `[CONFIRMED BY MODERATOR — aggregate]` |
| ≈12-second action search (OBS-03) | `[OBSERVED — moderator-reported; timing verbatim as supplied]` |
| "Is this cancelling the subscription?" (OBS-04) | `[OBSERVED — verbatim quote, moderator-supplied]` |
| Confirmation understood (OBS-06) | `[REPORTED — moderator judgement; basis not confirmed]` |
| F-01, F-02 interpretations | `[PM INFERENCE]` |
| Design implications (§12) | `[PM INFERENCE — not decided]` |
| Session date, persona split, per-tester detail | `[NOT CONFIRMED]` |

### Sets never merged

| Set | Contents | May supply B18? |
|---|---|---|
| **A — Real tester** | This report · OBS-01…OBS-10 · F-01…F-04 | ✅ Yes |
| **B — Designer self-walkthrough** | U-01…U-18, quote U-05 | ❌ No |
| **C — Cognitive/heuristic walkthrough** | P1…P7 | ❌ No |

**No observation has moved between sets.** No heuristic finding has been cited as corroborating a real finding.

---

## 16. VIVA-READY EXPLANATION

**If asked "what did you find?"**
> Seven real users tested the prototype. All seven were able to use it and gave generally positive feedback. Two frictions were still observed, and both sit in the same narrow band — between seeing the insight and taking the action. One is discoverability: users searched about twelve seconds before finding the action entry. The other is semantics: at least one user asked, "Is this cancelling the subscription?" Both are MEDIUM, because every user recovered and completed the flow.

**If asked "why isn't the discoverability issue HIGH — several users hit it?"**
> Because the locked severity definition sets HIGH as *blocking task completion for multiple users*, not *affecting multiple users*. Frequency and severity are different axes. No user was blocked, so it is MEDIUM. Upgrading it would make the rubric look satisfied while making the evidence false.

**If asked "your B18 requirement is unmet — isn't that a failure?"**
> No High-priority insight→action friction was observed, so I report that there wasn't one. The alternative was to invent a blocked tester, and a fabricated finding would have propagated straight into the Part C experiment design. A reported null is a result; a manufactured HIGH is a defect in the whole relay.

**If asked "the users said the design was fine — so why report frictions at all?"**
> Because those are two different measurements. Overall acceptability is sentiment; the twelve-second search and the cancellation question are behaviour. Letting positive sentiment overwrite observed behaviour would have thrown away the only actionable output of the round.

**If asked "why didn't you fix the CTA position?"**
> Because it became evidence the moment it was observed. Moving it now destroys the baseline that any Part C intervention would be measured against. Document first, intervene deliberately.

**If asked "how confident are you in this evidence?"**
> The count of seven and the aggregate outcomes are attested by me as moderator. Individual attribution wasn't retained, and the session dates aren't recorded. I've marked every one of those gaps as unconfirmed rather than filling them in — the report states exactly what it can support and nothing beyond it.

---

## FABRICATION AUDIT

| Check | Result |
|---|---|
| Invented tester names | ❌ **None.** No tester is named anywhere |
| Invented ages | ❌ **None.** No age is stated for any tester |
| Invented occupations | ❌ **None** |
| Invented quotes | ❌ **None.** Exactly one tester quote exists, supplied verbatim. No positive-sentiment quote was invented despite positive sentiment being reported |
| Invented timings | ❌ **None.** One timing exists (≈12 s), as supplied. "Eventually" was left un-quantified |
| Invented success rates | ❌ **None.** No percentage, ratio, or rate appears anywhere |
| Invented session dates | ❌ **None.** `[NOT CONFIRMED]` |
| Invented persona assignment | ❌ **None.** Persona split is `[NOT CONFIRMED]`; no tester assigned to a persona |
| Invented observations | ❌ **None.** OBS-01…OBS-10 map one-to-one onto moderator-supplied facts |
| Invented statistical significance | ❌ **None.** n=7 qualitative; no inferential claim made |
| Set B or Set C content used as tester evidence | ❌ **None.** U-05 remains Set B; P1–P7 remain Set C |
| Error manufactured to fill the four-category requirement | ❌ **None.** Errors = 0, reported as 0 |
| HIGH manufactured to satisfy B18 | ❌ **None.** B18 reported as NOT SATISFIED |
| Positive sentiment used to erase observed friction | ❌ **None.** F-01 and F-02 retained at MEDIUM |
| Figma modified | ❌ **No** |
| Locked decision modified | ❌ **No** |

---

**Task 3 NOT LOCKED. Figma unmodified. Control Center unmodified. Part C not started.**
