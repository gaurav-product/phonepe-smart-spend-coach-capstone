# CAPSTONE CONTROL CENTER
## PhonePe Smart Spend Coach — Feature Design, Validation & Growth Case
**Owner:** Gaurav Kumar Singh | **Batch:** 220 | **Module:** 6 | **Instructor:** Krishnan Parameswaran
**Version:** v3.0 | **Updated:** 16 Aug 2026

> **v3.0 changelog — Part B Task 2 LOCKED**
> - **LB-09 🔒 LOCKED — AI-AUGMENTED.** LB-10 🔒 **LOCKED — HALLUCINATION RATE.** Both PM DECISION, 16 Aug 2026. Artifact: `PART_B_TASK2_AI_CLASSIFICATION.md`.
> - **Gaurav's verbal justification, recorded for the explainability requirement (Guideline 4):**
>   *"I am locking Task 2 as AI-augmented because the core Smart Spend Coach flow survives without the AI layer: detection, evidence and action remain functional, while AI primarily improves recognition and explanation. I am choosing hallucination rate as the biggest risk because a fabricated explanation would directly violate the product boundary that the system reports observed transaction patterns and the user makes the judgement."*
> - **Exactly one risk dimension is named**, per the acceptance criterion. The other three are **not** ranked and no "second biggest risk" is stated.
> - ⚠️ **Alarm A6 armed:** naming hallucination rate here does **NOT** commit Part C. Part C Task 4's five monitoring dimensions (quality · cost · accuracy · operational efficiency · safety) remain **undecided**, and the Capstone forbids restating one list as the other.
> - **No model provider, API, architecture, training pipeline or benchmark named anywhere.** ML-plausible components (merchant normalisation, category classification, copy generation) remain `[PM DESIGN ASSUMPTION]`; everything unspecified remains `[NOT SPECIFIED BY CAPSTONE]`.
> - **Nothing else changed.** LA-02, LA-17, LA-20, LA-18b, LA-24, LA-25, LA-26, LA-28 and LB-01 – LB-08 untouched. **Part A Task 4 rows LA-18c – LA-18e remain SET** (not yet locked); **LA-18f and LB-08b remain BLOCKED.**
> - **Total locked decisions: 34.**
> - Usability testing, ethics, bias, pricing and Part C not started.



> **v2.9 changelog — Part A Task 4 (Airtable) BUILT**
> - **Airtable base created:** "PhonePe Smart Spend Coach — Capstone (Part A)" · `appozPM3QfEc0ZJ7V` · https://airtable.com/appozPM3QfEc0ZJ7V
> - **Task 4 status: NOT BUILT → BUILT / READY FOR LOCK**, subject to the two open items below.
> - **New rows LA-18c – LA-18f SET** (not locked), using the established suffix convention — no new numbering scheme invented.
> - **Exactly 2 tables**, exact column names, 2 + 5 records, all values traced to locked LA-02/03/05/08/15/16/17. **Views, formulas and filters: [NOT SPECIFIED BY CAPSTONE] — none created.**
> - **No user research, observations, quotes or customer records exist in the base** — the Part B walkthrough has not happened.
> - ⚠️ **Two open items requiring Gaurav:** (1) **Persona Name** uses the locked segment label, not an invented individual — replace if a named persona is wanted; (2) **Acquisition Channel** is `[PM INFERENCE from CASE DATA]` and is load-bearing for Part C Task 3.
> - ⛔ **LA-18f sharing BLOCKED** — manual step, same as LB-08b.
> - **Part B Task 2 not started.**



> **v2.8 changelog — Part B Task 1 LOCKED**
> - **LB-01 – LB-08 🔒 LOCKED** by Gaurav, 16 Aug 2026, on the **current corrected state**. Evidence class: **PM DECISION**. Verbal justification recorded in §8.B.
> - **LB-08 is locked as the corrected 10-NAVIGATE interaction map**, zero dead ends: 01→02 · 01→04 · 02→01 (back) · 02→03 · 02→01 (keep charge) · 03→05 (confirm) · 03→02 (safe exit) · 04→01 (back) · 04→01 (view history) · 05→01 (undo).
> - **The unsafe CHANGE_TO variant shortcut remains removed and must not be restored** (EV-044). **No change-to-variant interaction exists**; the Capstone permits navigate-to *or* change-to-variant, and 10 navigates satisfy the ≥3 requirement. Variant states are demonstrated by screens 01 and 05.
> - **EV-044 and EV-045 remain recorded** as the QA defect/resolution and the prototype-integrity repair.
> - **Total locked decisions: 32.** Part A 24 + Part B Task 1 8.
> - ⚠️ **Numbering correction:** the prototype-sharing row had been created as "LB-09", colliding with the established LB-09 (AI-augmented/AI-native classification). **Renumbered to LB-08b.** The established numbering is preserved; LB-09 remains AI classification and is untouched.
> - **LB-08b remains ⛔ BLOCKED** — sharing must be set manually by Gaurav and verified logged-out. **Not locked.**
> - No Part A decision altered. LA-18b not reopened. Confirmation and low-confidence edge case unchanged. No new product capability added.
> - **Part B Task 2 not started.**



> **v2.7 changelog — Part B Task 1 (Figma prototype) built**
> - **Figma file created:** "PhonePe Smart Spend Coach — Capstone Prototype" · fileKey `XhV4JoExaeeygvEG1LZGez` · https://www.figma.com/design/XhV4JoExaeeygvEG1LZGez
> - **LB-01 – LB-08 SET** (not locked). 5 screens, 1 component set with 2 variants, 7 interactions.
> - **LB-09 added and BLOCKED:** prototype sharing must be set to "Anyone with the link can view" **manually by Gaurav** — the Figma Plugin API cannot change file sharing.
> - **No Part B Task 2 work started.** No usability testing, no observations, no pricing, no Part C.
> - Relay verified: locked persona → C2 → locked PRD → these screens. Nothing new introduced.



> **v2.6 changelog — EV-043 resolved · Part A Task 5 LOCKED**
> - **EV-043 RESOLVED.** `[PM DECISION — Gaurav, 16 Aug 2026]` **LA-14 remains unchanged and is not reopened.** "Wasteful" is retained **only** in the competitive wedge / positioning language. **The product itself must never claim it objectively knows a commitment is wasteful.** Product language remains: *flagged for review · worth reviewing · recurring spending pattern · change in recurring spending pattern*. **The user makes the judgement.**
> - **Part A Task 5 (PRD-lite) LOCKED** — LA-18b and LA-19 – LA-28, eleven rows, locked 16 Aug 2026 with a recorded verbal justification (see §8.A).
> - **Total locked decisions: 24.** Task 1 (4) + Task 2 / Task 3 (9) + Task 5 (11).
> - **C2 remains the selected feature.** Primary persona unchanged. Metrics unchanged (IACR primary, ARR guardrail).
> - **Platform capability remains explicitly `[NOT VERIFIED]`**; **Option D remains the documented fallback.**
> - **Part A Task 4 (Airtable) still NOT BUILT** — unchanged status.
> - **No Part B decision has been made.** Part B Task 1 (Figma prototype) begins after this lock.



> **v2.5 changelog — PRD-lite corrected after hallucination audit**
> - **10 corrections applied** to `PART_A_TASK5_PRD_LITE.md` (see EV-039 – EV-042). **Still SET, still not locked.**
> - **Detection logic rebuilt (EV-039).** *"No usage signal"* and *"past a trial period"* were invented capabilities and are removed. Detection now uses transaction-derived signals only, and the product no longer asserts that a commitment is "wasteful" — it flags patterns worth reviewing and leaves the judgement to the user.
> - **Merchant-behaviour claim removed (EV-040).** *"Access continues until the paid period ends"* deleted; replaced with the truthful product limitation.
> - **"Cancellation" removed from US3 (EV-041)** — a regression against EV-035.
> - **Superlatives removed (EV-042).** Only the narrow verified claim about Ask Google Pay remains.
> - ⚠️ **Naming question raised against LOCKED row LA-14**, not resolved unilaterally — see the note under LA-14.



> **v2.4 changelog — Part A Task 5 (PRD-lite) drafted**
> - **LA-18b added and LA-19 – LA-28 filled.** All **SET — awaiting Gaurav's lock**. Artifact: `PART_A_TASK5_PRD_LITE.md`.
> - **U8 resolved as LA-18b**, explicitly as a `[PM DECISION]` / design assumption with an unverified platform dependency and a documented fallback — **not** as case data.
> - **No decision locked.** LA-01, LA-02, LA-03, LA-09, LA-10 – LA-18 unchanged (13 locked).
> - ⚠️ **Gap flagged: Part A Task 4 (Airtable base) not built.**

> **v2.3 changelog — Task 2 LOCKED**
> - **LA-10 through LA-18 LOCKED by Gaurav, 15 Aug 2026.** Values unchanged from the v2.2 corrected state. Verbal justification recorded in §8.A.
> - **Total locked decisions: 13** (LA-01, LA-02, LA-03, LA-09 from Task 1; LA-10 – LA-18 from Task 2).
> - **Structural fix applied while locking:** the nine Task 2 rows had been written with six columns instead of the table's seven — the Date column was missing, shifting the downstream-impact text into it. Adding the lock date restores all nine rows to seven columns. **No value was altered.**
> - **U8 explicitly preserved as unresolved** and flagged as a mandatory PRD question. Locking the one-tap action does not authorise cancellation.

> **v2.2 changelog — Task 2 pre-lock corrections (3)**
> 1. **Cancellation overclaim removed (EV-035).** The Capstone specifies the one-tap action, not what it executes. Wedge, C2 scope and selection rationale now read *"an appropriate one-tap action, such as applying a cap or another supported control."* Cancellation is labelled a potential implementation option `[NOT VERIFIED]`. New uncertainty **U8** carries this into the PRD.
> 2. **NPCI inference softened (EV-036).** *"Terminated by failure rather than by decision"* → *"the reported revocation pattern suggests a meaningful share of recurring commitments may end through payment failure rather than deliberate user action."* The not-independently-confirmed caveat now travels with every citation.
> 3. **RICE Reach = 7 justified (EV-037).** Explicitly a relative ordinal estimate, not a population figure, positioned against C1/C4/C5 on the declared scale.
>
> **Unchanged:** LA-01, LA-02, LA-03, LA-09 remain LOCKED. Selected feature remains **C2**. All five RICE scores unchanged and re-verified. LA-10–LA-18 remain **SET**.
**Status:** Requirements & compliance baseline COMPLETE. **Part A Task 1 LOCKED** (LA-01, LA-02, LA-03, LA-09). Tasks 2–5 not started.

> **v2.1 changelog**
> - **Part A Task 1 locked** by Gaurav, 15 Aug 2026: primary persona = mid-career household financial managers (33–45); secondary = young urban salaried professionals (24–32); primary segmentation factor = **Expected Retention**; AI approach = **Guided AI Q&A**. Final artifact: `PART_A_TASK1_segmentation_FINAL.md`.
> - **LA-09 re-scoped** to the primary *factor* (it previously mis-stated requirement A09); written persona justification moved to new row LA-09b.
> - **Evidence log extended** to EV-025, including three retractions/rejections (EV-023, EV-024, EV-025) that must not reappear downstream.
> - **CAC terminology fixed** — the required term "cost of acquisition (CAC)" is retained; an earlier working draft's renaming was reverted.
> - **Segment-sizing method fixed** — relative rank + order-of-magnitude band + visible derivation; no point estimates, because PhonePe publishes no MAU or category mix (EV-020).

> **v2.0 is a major revision.** I opened the actual Capstone document on the Masai Assessment Platform (with your approval). It differs materially from the LMS briefing Notes in **16 places**, several of which would have cost real marks. See §0.

---

# §0. WHAT CHANGED IN v2.0 — READ THIS SECTION FIRST

I now have the **real Capstone document** (Level 2 authority), not just the LMS briefing Notes (Level 3). They conflict. Per your source hierarchy, **the Capstone document wins every time.**

## 0.1 The 16 conflicts — and what they cost if you'd followed the Notes

| # | Item | LMS Briefing Notes (Level 3) | **CAPSTONE DOCUMENT (Level 2) — AUTHORITATIVE** | Cost if you'd used the Notes |
|---|---|---|---|---|
| **X1** | **Prioritization framework** | "scored on **reach, impact, and effort**" | **RICE — Reach, Impact, Confidence, Effort — and you must "show the arithmetic for each score"** | **Severe.** Missing Confidence + missing visible arithmetic fails an explicit acceptance criterion. |
| **X2** | **Funnel Stage 3** | "Logged in: **10,000**" | "Onboarding / transaction-linking completed: **11,200**" | **Severe.** Every conversion %, drop-off %, and absolute loss in Part C would be wrong. Acceptance criteria require them "arithmetically correct." |
| **X3** | **Segmentation factors** | "four segmentation factors" — never specified | **Named exactly: segment size, willingness to pay, cost of acquisition (CAC), expected retention** | **Severe.** You'd have invented four generic factors and missed all four required ones. |
| **X4** | **Marks split** | Not published | **Part A = 30 · Part B = 35 · Part C = 35** | Effort mis-allocation. *(Resolves OQ-03.)* |
| **X5** | **Required screens** | home, one-tap confirmation, edge case | **home entry, INSIGHT DETAIL, action confirmation, edge case** | Missing screen = fails "at least 4 screens" acceptance criterion. |
| **X6** | **Usability note format** | "a simple note-taking format" | **The four-part format: Errors / Hesitations / Successes / Quotes** — observations must span all four note types | **High.** Acceptance criterion: "at least 6 usability observations are recorded **across all four note types**." |
| **X7** | **Severity guide** | "the standard severity guide" — undefined | **Defined: High = blocks task completion for multiple users · Medium = causes hesitation but is recovered from · Low = minor or isolated** | *(Resolves OQ-04.)* |
| **X8** | **Pricing traps** | 2 — cost-plus, competitive | **3 — cost-plus, competitive, gut-feel** | Minor, but you'd have had a smaller menu. |
| **X9** | **Pricing decision shape** | Choose freemium / free trial / premium tier | **TWO decisions: (a) freemium vs free-trial, AND (b) packaging shape — tiered, usage-based, or hybrid** | **High.** Acceptance criterion requires *both* named. Packaging shape is absent from the Notes entirely. |
| **X10** | **A/B metrics** | primary + guardrail | **Full Metric Triad — primary + secondary + guardrail**, each a precise formula | **High.** You'd have submitted 2 of 3 required metrics. |
| **X11** | **A/B hypothesis format** | free-form example | **Exact template, four blanks:** *"We believe that \<change\> will result in \<measurable outcome\> because \<reason\>. We will measure \<primary metric\>."* | **High.** Acceptance criterion: "uses the exact hypothesis template with all four blanks filled." |
| **X12** | **A/B pitfalls** | one generic example | **Named list of 4: Early Judgment Error · Local Maxima Trap · Novelty Effect · HARKing** | Medium. Must name one *from this list*. |
| **X13** | **Bias types** | representation, measurement | **4 named: Representation · Measurement · Aggregation · Evaluation** — name exactly one | Medium. |
| **X14** | **AI evaluation frameworks** | Blurred together | **TWO DISTINCT FRAMEWORKS, and the brief explicitly warns not to restate one as the other:** Part B Task 2 = 4-dimension *per-feature risk* (accuracy, response speed/latency, token cost/efficiency, hallucination rate) · Part C Task 4 = 5-dimension *monitoring* (quality, cost, accuracy, operational efficiency, safety) | **High.** The brief calls this out by name — an examiner is clearly watching for people who conflate them. |
| **X15** | **Competitive table** | classify into 4 categories | ≥6 features classified across **at least 3 of the 4** categories | Slightly easier than feared. |
| **X16** | **Persona creation method** | "research can follow any method" | **Must use one of three named AI-assisted approaches (direct AI knowledge / guided AI Q&A / AI-plus-uploaded-notes) and state which, in one line** | Medium — an explicit, easily-missed deliverable line. |

**Everything below is now rebuilt on the Capstone document. The LMS Notes are retained only where they add colour that does not conflict.**

## 0.2 Deadline — resolved
You said 21 Aug. **It is 28 August 2026, 11:59 PM IST.**

| Source | Says | Authority |
|---|---|---|
| Capstone document, Submission Guidelines | "by the end of Day 14 of the project window" | Level 2 — **undated and internally inconsistent** (29 Jul + 14 days ≈ 11 Aug, already past) |
| LMS assignment #81471 instruction body | 21/08/2026, 11:59 PM | Level 1 — **stale text**, not updated after the extension |
| LMS assignment #81471 window header | 28 Aug 2026, 11:59 PM IST | Level 1 — live system state |
| **LMS Announcement #16057, 31 Jul 2026 (Prativa Brahma)** | **"extended from 21st August 2026 to 28th August 2026 (11:59 PM IST)"** | **Level 1 — most recent, explicitly overrides 21 Aug** |
| Assessment platform countdown (observed 15 Aug) | **"13 days"** | Live system state — agrees with 28 Aug |

**RESOLUTION:** Two independent live system states plus the most recent Level-1 announcement all agree. **Operative deadline = 28 Aug 2026, 11:59 PM IST.** The announcement adds: *"No further extension will be provided beyond this date"* and submissions after that time *"will not be accepted, irrespective of the reason."*

**PM recommendation (yours to accept):** internal target **21 Aug**; 22–27 Aug reserved for the compliance audit, incognito link testing, and the explainability rehearsal. Do not spend the extension on drafting.

## 0.3 The submission mechanism — now known
*Verified on the Masai Assessment Platform, assignment #81471 → Start Evaluation.*

- It is **one subjective question (Q:1)** with **one rich-text answer box** ("Enter your answer here"), autosaving ("All changes saved").
- The full Capstone document is displayed on the left; your answer goes on the right.
- Submission is finalised with the **"MARK AS COMPLETED"** button at the top.
- **I did not type anything and did not click MARK AS COMPLETED.** The tab is still open in your browser.
- **What goes in the box:** your single Google Doc link. Everything else lives inside that doc.

⚠️ The platform shows *"Correct answer: +1 / Wrong answer: -0"* — standard subjective-question chrome, not the real 100-mark scheme. Ignore it.

⚠️ The assessment link is described on-screen as *"a unique link generated only for you. Please do not share this link with anyone."* I have not recorded or shared it.

## 0.4 Your two "uploaded" documents
Neither reached this session — uploads folder empty, no connected folder, `/mnt/attach` empty. You chose to connect a folder; **I still can't see one.** Use **"Add folder"** in the desktop app (your `Documents` / `Desktop` folders aren't in the grantable list I can see — only `.copilot`, `.ms-ad`, `Contacts`, `Downloads`, `Favorites`, `Links`, `Music`, `Saved Games`, `Searches`, `Videos`, which suggests OneDrive redirection). Once connected I'll diff them against this matrix.

**Good news:** now that I have the real Capstone document from the assessment platform, those files are almost certainly redundant. This matrix is built from the authoritative source.

---

# §1. PROJECT OVERVIEW

**The case (verbatim framing from the Capstone document):** PhonePe's product organization is exploring an AI-powered **Smart Spend Coach** for the consumer app — it analyses a user's own transaction categories (bills, recharges, food delivery, transfers) and surfaces short, personalised nudges (*"you spent 28% more on food delivery this month than last month; here is a suggested weekly cap"*) with a one-tap way to act on each nudge.

**Leadership has not committed engineering time.** Before it goes near a sprint, a PM must prove the problem is real, design and validate a concrete version, and lay out how it would be priced, launched and measured. **You are that PM.**

| Fact | Value |
|---|---|
| Total marks | **100** (Part A 30 · Part B 35 · Part C 35) |
| Weightage in overall evaluation | **10%** |
| Deliverable | **One** written case document + two embedded tool links |
| Deadline | **28 Aug 2026, 11:59 PM IST** |
| Time remaining (from 15 Aug) | **13 days** |

**The relay-race rule — the spine of the whole project (Capstone document, verbatim in substance):**
> *"The persona and PRD you write first are the only persona and PRD your prototype is allowed to be built against. The usability findings from your prototype are the only usability findings your growth experiment is allowed to target."*

And, opening Part A: *"you may not introduce a different persona, a different chosen feature idea, or different success metrics once you reach Part B."*

The pre-read (LMS #163570) explains why this is the primary grading lens: *"A capstone checks whether your later decisions genuinely build on your earlier ones, not just whether each piece looks good on its own."* … *"That thread is what capstone grading is really looking for."*

---

# §2. OFFICIAL REQUIREMENTS
*Source: LMS Assignment #81471 — Evaluation / Graded-Evaluation / Module-6 / Mandatory / 10% Weightage. Window: 29 Jul 2026, 8PM – 28 Aug 2026, 11:59 PM IST.*

1. Carefully read and follow all the instructions provided in the Capstone document.
2. Submit the required links and details **only in their respective answer boxes**. Incorrect or incomplete submissions may lead to **disqualification or zero marks**.
3. Late submissions will not be accepted under any circumstances.
4. AI tools and online resources are permitted — **however, you must thoroughly understand everything you implement and be able to confidently explain your approach and design decisions if asked during evaluation.**
5. Ensure all links shared are **accessible and working** before submitting.
6. Avoid plagiarism or copying. Your submission must reflect your own understanding and effort.
7. Test everything thoroughly before submission.

---

# §3. SUBMISSION REQUIREMENTS
*Source: Capstone document, "Submission Guidelines (read first)" + closing "Submission" section — AUTHORITATIVE*

| # | Rule | Verbatim / detail |
|---|---|---|
| S1 | **One submission only** | "exactly one submission: a **Google Doc link only**" |
| S2 | **Sharing** | Set to **"Anyone with the link can view"** |
| S3 | **Contents** | Part A, Part B, Part C **in order, in the same document** |
| S4 | **Format exclusions** | "Any other link (**Notion, GitHub, OneDrive, PDF, etc.**) **will not be graded**" |
| S5 | **No per-part submission** | "There is no separate submission per Part" |
| S6 | **Airtable link** | Base's shareable view link, **pasted as plain text inside Part A**, at the point where it is first needed |
| S7 | **Figma link** | Prototype's shareable link, **pasted as plain text inside Part B**, at the point where it is first needed |
| S8 | **No uploaded media — at all** | "No images, screenshots, diagrams-to-upload, PDFs of slides, presentation decks, video, or audio are required **or accepted** anywhere" |
| S9 | **Describing is fine** | "You may of course describe a screen or flow in words — only uploaded media files are disallowed" |
| S10 | **No tool screenshots** | "Do not upload screenshots of either tool — **the live link is the deliverable**" |
| S11 | **Answer box** | One rich-text box on the assessment platform; finalise with **MARK AS COMPLETED** |
| S12 | **Deadline** | 28 Aug 2026, 11:59 PM IST (see §0.2) |

**Free-tier tool guarantees (Capstone document, verbatim in substance):**
- **Figma** — free Starter plan supports this project's single file: multiple screens, components, variants, and the Prototype tab all work on the free tier.
- **Airtable** — free tier's row and attachment limits are more than sufficient for two small tables.
- **Any AI chat assistant** — a free ChatGPT / Claude.ai / Gemini account is enough. **No paid API key or developer account is required anywhere**, since nothing needs to be deployed or run as live code.

**Originality clause (verbatim in substance):** *"Personas, competitive notes, prototype screens, usability write-ups, and all analysis must be your own work product for this specific brief. Do not submit another learner's Figma duplicate or Airtable base."* → drives §11.

---

# §4. MASAI LMS FINDINGS

## 4.1 What I verified, and where

| Item | Location | Status |
|---|---|---|
| **The full Capstone document** — 3 parts, all tasks, all acceptance criteria, marks split, submission guidelines | Masai **Assessment Platform**, via #81471 → Start Evaluation | ✅ **VERIFIED — this is the authoritative source** |
| Submission mechanism: 1 subjective question, 1 rich-text box, MARK AS COMPLETED | same | ✅ VERIFIED |
| Countdown showing **13 days** remaining on 15 Aug | same | ✅ VERIFIED |
| Assignment guidelines (7 rules), window, 10% weightage, Mandatory | `/learn/assignments/81471` | ✅ VERIFIED |
| **Deadline extension to 28 Aug 2026** | `/announcements/16057`, 31 Jul, Prativa Brahma | ✅ VERIFIED |
| Capstone briefing Notes — narrative walkthrough, worked examples | `/learn/resources/163692` (30 Jul) | ✅ VERIFIED — **but conflicts with the Capstone document in 16 places (§0.1). Lower authority.** |
| Capstone approach pre-read — the lock-in principle | `/learn/resources/163570` (28 Jul) | ✅ VERIFIED |
| Practice assignments: Briefing Q&A Subjective (#81663, auto-completed 15 Aug) and Objective | associated assignments | ✅ VERIFIED — LMS states *"Practice assignment score will not be considered"* |
| Briefing lecture, Sumant Malhotra, 29 Jul 8–10 PM | associated lecture, marked **Optional session** | ⚠️ Video — not transcribed. Recommend you watch it. |
| "Evaluation Format, Marking Scheme & Orientation Resources" (#16170) | announcement, 4 Aug | ✅ VERIFIED — **this is for the 23 Aug Offline Evaluation exam, NOT the Capstone.** Don't confuse the two. |

## 4.2 Still unverified

| Item | Status |
|---|---|
| The two documents you said you uploaded | Never reached this session (§0.4). Likely redundant now. |
| Briefing lecture recording contents | Video; may contain instructor colour not in the written brief. |
| Any grading rubric finer than the 30/35/35 split | Not found. The **acceptance criteria** in the Capstone document are the closest thing to a rubric and should be treated as one. |

## 4.3 Explicit requirement vs. my interpretation — kept separate

| Explicit (their words) | My interpretation — **[AI SUGGESTION]**, validate before relying on it |
|---|---|
| "by the end of Day 14 of the project window" | Internally inconsistent with every dated source; superseded by the 31 Jul announcement. Do not act on it. |
| "state segment size (a **reasoned estimate**, not a fabricated precise figure)" | The brief is pre-empting exactly the failure mode of quoting a confident number with no derivation. Show your reasoning chain; a round, defensible estimate beats a precise, unsourced one. |
| "**at least 3 of the 4** categories" (competitive table acceptance criterion) | Using all four is safer than the minimum and costs nothing — the Gap category is also what feeds your wedge statement. |
| "a rigorously simulated test where you personally walk through the flow acting as each of your Part A personas" | This is the sanctioned self-walkthrough route you chose. Note the word **"rigorously"** — the brief permits simulation but expects discipline. Record observations *as you go*, not reconstructed afterwards. |
| "note this 5-dimension monitoring framework is a **distinct, broader lens** from Part B Task 2's 4-dimension per-feature risk framework … **they are not the same list restated**" | The brief explicitly names this trap. Treat X14 as a graded checkpoint, not a stylistic note. |
| Funnel numbers | I independently verified the arithmetic: the largest-absolute-loss stage and the largest-percentage-drop stage **are indeed different stages**, exactly as the brief asserts. Do the computation yourself in Part C — I have deliberately not put the answers in this document. |

---

# §5. PART A REQUIREMENTS — Research, Persona & Feature PRD (30 marks)
Matrix rows **A01–A31**. Structural notes:

- **Five tasks.** Personas → competitive teardown → RICE-scored candidates → Airtable base → PRD-lite.
- **The four segmentation factors are fixed:** segment size, willingness to pay, cost of acquisition, expected retention. Use these four to justify which persona is primary.
- **RICE, with visible arithmetic.** Not just a final number.
- **PRD-lite must be in this order:** (a) problem statement citing the persona's frustration → (b) chosen solution + one rejected alternative and why → (c) 3–5 user stories, each checked against **every** INVEST letter in one line → (d) primary + guardrail metric as precise formulas → (e) two concrete edge cases + behaviour → (f) one explicit out-of-scope line.
- **The brief's own example of a good metric:** *"percentage of Smart-Spend-Coach users who take at least one recommended action within 7 days of viewing an insight"* — not a vague label like "engagement". Note the embedded time window.
- **Edge-case examples given:** a user with fewer than 5 transactions in a category; a user who opts out of transaction analysis mid-month.
- **Indirect competitor is defined for you:** one that "solves the same underlying job — *understand and control my spending* — through a different product form."

---

# §6. PART B REQUIREMENTS — Prototype, Usability Validation & Pricing (35 marks)
Matrix rows **B01–B26**. Structural notes:

- **Five tasks.** Figma prototype → AI classification & risk → usability test → ethics & bias pass → pricing & packaging.
- **Four screens minimum, all named:** (a) home-screen entry point where the insight first appears, (b) **insight detail screen**, (c) one-tap action-confirmation screen, (d) one edge-case screen matching one of your two Part A edge cases.
- **Interactions** = tap triggers with *navigate-to* or *change-to-variant* actions. At least 3.
- **The four-part note-taking format is mandatory:** Errors / Hesitations / Successes / Quotes. ≥6 observations **across all four types**.
- **Severity guide (now defined):** High = blocks task completion for multiple users · Medium = causes hesitation but is recovered from · Low = minor or isolated.
- **THE HARD GATE (B18):** at least one **High**-priority observation must describe friction *specifically* between viewing a personalised insight and completing the recommended action on it — the brief gives examples: too many taps, an unclear button, or the action screen not making the benefit obvious. The brief states plainly: *"this is the single most decision-relevant type of friction for a nudge-based feature, and Part C depends on it."*
- **Ethics:** one sentence per principle (Transparency, User Control, Privacy-by-Design, Fairness, Graceful Failure) naming a **concrete design choice your prototype makes or should make**. Acceptance criterion explicitly rejects *"we will be transparent"*-style statements without a stated mechanism.
- **Bias:** name exactly **one** of Representation / Measurement / Aggregation / Evaluation, for a spending-pattern feature tuned on existing transaction data. One paragraph.
- **Pricing = two decisions:** freemium **vs** free-trial, **and** packaging shape (tiered / usage-based / hybrid). Justify against persona WTP and name ≥1 of the three traps (cost-plus, competitive, gut-feel) you are avoiding. Decoy tier is optional — if used, name all three tiers and which one the decoy pushes toward.

---

# §7. PART C REQUIREMENTS — Growth Funnel, Experiment Design & AI Evaluation (35 marks)
Matrix rows **C01–C29**. Structural notes:

**⚠️ CASE DATA — the corrected pilot funnel (30-day pilot, eligible PhonePe users shown the entry banner). Use THESE numbers, not the LMS Notes version:**

| Stage | Users |
|---|---|
| 1. Entry banner shown | **40,000** |
| 2. Feature opened | **16,000** |
| 3. Onboarding / transaction-linking completed | **11,200** ⚠️ *(the LMS Notes said "Logged in: 10,000" — wrong)* |
| 4. First personalized insight viewed | **9,520** |
| 5. Recommended action taken | **2,856** |

- **Four transitions** to compute (1→2, 2→3, 3→4, 4→5), showing **both** % converted and % dropped at each step.
- **Then separately** report the single stage with the largest **absolute** users lost, and the single stage with the largest **percentage** drop-off. The brief states outright: *"These are not the same stage."*
- **The prioritization argument must explicitly invoke the intent-proximity principle** — prioritise drop-offs closer to the final action, since user intent is highest there — **and** explain why the other stage is lower priority *despite losing more raw users*.
- **A/B test:** must name **which specific Part B observation** it addresses. Hypothesis in the **exact template**: *"We believe that \<change\> will result in \<measurable outcome\> because \<reason\>. We will measure \<primary metric\>."* All four blanks filled.
- **Metric Triad:** primary + secondary + guardrail, each a **precise formula**, not a label.
- **Duration:** reasoned, explicitly covering ≥1 full 7-day behaviour cycle.
- **Pitfall:** name one of **Early Judgment Error / Local Maxima Trap / Novelty Effect / HARKing** that *this specific design* is at risk of, plus one concrete precaution.
- **Growth loop:** one of **Virality / Content / Paid**, justified in one paragraph referencing the Part A primary persona's **acquisition channel** and **willingness-to-pay**.
- **AI evaluation plan:** (a) 2 of the 5 monitoring dimensions (quality, cost, accuracy, operational efficiency, safety) + why — **and do not restate Part B's 4-dimension risk list here**; (b) one concrete token-cost optimisation applied to *this feature's insight-generation calls* (brief's examples: caching a repeated system/context prompt across users; tiering to a cheaper model for simple insights, stronger model only for complex ones); (c) a **5-3-1 dashboard spec in text** — 1 core insight metric, 5 supporting KPIs, 3 visualisations, **all specific to Smart Spend Coach, "not generic placeholders."**
- **Closing:** 3–5 lines confirming the free path for every AI-tool dependency across the whole project.

---

# §8. LOCKED DECISIONS
**Status: Part A Task 1 LOCKED (LA-01, LA-02, LA-03, LA-09) and Part A Task 2 LOCKED (LA-10 – LA-18) on 15 Aug 2026 — 13 locked decisions. Remaining Part A rows LA-04 – LA-08, LA-09b (supporting, SET) and LA-19 – LA-28 (PRD-lite, not started) are UNLOCKED. All Part B and Part C rows UNLOCKED.**

**Rules of this register**
1. A decision becomes **LOCKED** only when *you* say "LOCK". Not when I suggest it, not when it appears in a draft.
2. Once LOCKED I will not silently change it. If later work implies it was wrong, I **stop, name the conflict, show the cost of changing it, and wait.**
3. Every LOCKED row carries its evidence class (§9) and lock date.
4. Downstream artefacts may only draw on LOCKED upstream decisions.
5. **No LOCK without an unprompted verbal justification from you** (§11.4).

## 8.A — Part A (30 marks)

| # | Decision | Value | Evidence class | Locked? | Date | If changed, invalidates |
|---|---|---|---|---|---|---|
| LA-01 | AI-assisted persona approach used | **Guided AI Q&A (Approach 2)** | PM DECISION | 🔒 **LOCKED** | 15 Aug 2026 | A02 (one-line statement) |
| LA-02 | **Primary persona** | **Mid-career household financial managers, 33–45, tier-1/2** *(formerly candidate S2)* | PM DECISION | 🔒 **LOCKED** | 15 Aug 2026 | All of Part B; LC-08, LC-09 |
| LA-03 | Secondary persona | **Young urban salaried professionals, 24–32, tier-1/top tier-2** *(formerly candidate S1)* | PM DECISION | 🔒 **LOCKED** | 15 Aug 2026 | A08, Airtable Personas |
| LA-04 | Primary persona — segment size | **Medium-High** — order-of-magnitude "tens of millions"; **no point estimate** (PhonePe publishes no MAU or category mix) | DERIVED — anchored on EV-014/EV-015 | SET (supporting) | 15 Aug 2026 | RICE Reach |
| LA-05 | Primary persona — willingness to pay | **Medium** — higher ability to pay, lower perceived value | HYPOTHESIS | SET (supporting) | 15 Aug 2026 | LB-14 pricing, LC-08 |
| LA-06 | Primary persona — cost of acquisition (**term: CAC**) | **Low-Medium** — owned in-app distribution; greater permission hesitancy over household financial data | PM INFERENCE | SET (supporting) | 15 Aug 2026 | LC-08 growth loop |
| LA-07 | Primary persona — expected retention | **High** — permanent budgeting responsibility; regenerating household subscription base; low novelty decay | HYPOTHESIS | SET (supporting) | 15 Aug 2026 | **The basis of LA-09** |
| LA-08 | Secondary persona — size / WTP / CAC / retention | **Medium / Medium / Low / Medium** | DERIVED + HYPOTHESIS | SET (supporting) | 15 Aug 2026 | Primary-persona justification |
| **LA-09** | **Primary segmentation factor** *(row re-scoped — see note below)* | **Expected Retention** | PM DECISION | 🔒 **LOCKED** | 15 Aug 2026 | Everything downstream |
| LA-09b | Written justification of which persona is primary, using the four factors | Drafted in `PART_A_TASK1_segmentation_FINAL.md` §6, §11, §12 | PM DECISION | SET (supporting) | 15 Aug 2026 | A08 |

> **Row correction (v2.1):** LA-09 previously read *"Written justification of which persona is primary."* That mis-stated the requirement. Matrix row **A09** requires *"One-line justification of which **factor** is primary"* — so LA-09 is re-scoped to the primary **factor**, and the written persona justification moves to the new LA-09b. Matrix rows A08 and A09 were already correct; only this Locked-Decisions row was wrong.

> **On "SET (supporting)" vs LOCKED:** Gaurav explicitly locked four decisions (LA-01, LA-02, LA-03, LA-09). The four-factor ratings underpin them but were not independently locked, so they are recorded as **SET** — they may be revised, but only with a stated reason, and any revision that would change LA-02 or LA-09 must be surfaced as a conflict, not applied silently.
| LA-10 | Direct competitor | **Ask Google Pay** (primary evidence) · **CRED Money** · **Jupiter Money Manager**. Excluded with reasons: Fi Money (banking wound down Mar 2026, status unverified), ICICI My Money (unverifiable), Paytm/Axio/Money View/INDmoney (no primary capability doc) | SOURCE-BACKED FACT | 🔒 **LOCKED** | 15 Aug 2026 | Feature table |
| LA-11 | Indirect competitor (same job, different product form) | **I1 manual spreadsheet / self-maintained household budget** (evidenced by Jupiter's own "No more spreadsheets" positioning) · **I2 UPI AutoPay mandate management** (control without insight) | SOURCE-BACKED FACT + PM INFERENCE | 🔒 **LOCKED** | 15 Aug 2026 | Feature table |
| LA-12 | The ≥6 features compared | **10 features** (F1–F10): categorisation · multi-account aggregation · period-over-period variance · personalised insight · conversational AI · proactive push nudge · budget/cap · recurring-payment detection · **one-tap action on the insight** · household multi-member view. ⚠️ 7 cells `[NOT VERIFIED]` | FACT + NOT VERIFIED | 🔒 **LOCKED** | 15 Aug 2026 | Classification |
| LA-13 | Table-stakes / parity / differentiator / gap calls | **Table stakes:** F1, F4, F2 · **Parity:** F7 budget/cap, F6 nudge mechanism, F8 recurring detection · **Differentiators:** DIF-1 one-tap action on insight, DIF-2 push-not-pull, DIF-3 variance framing (weakest) · **Gaps:** GAP-1 broken insight→action loop on recurring commitments (strongest), GAP-2 household view (`[HYPOTHESIS]`, 4 unverified cells) | FACT + PM INFERENCE + HYPOTHESIS | 🔒 **LOCKED** | 15 Aug 2026 | **Wedge** |
| LA-14 | **Competitive wedge** — capability + unmet need + segment | **A one-tap action on recurring household commitments worth reviewing, surfaced from the user's own transactions, for mid-career household financial managers who can see the pattern today but cannot act on it where they see it.** ⚠️ **WORDING UPDATED 16 Aug 2026 by Gaurav's authorisation (§24.1)** — the original read *"wasteful … see the waste today"*, which contradicted the LA-19 core principle. Strategy, persona, solution and PRD unchanged | PM DECISION (pending) | 🔒 **LOCKED** | 15 Aug 2026 | Pricing value story |
| LA-15 | The ≥4 candidate feature versions | **5 candidates:** C1 Recurring Spend Digest · C2 Flagged Commitment + One-Tap Action · C3 Recurring Commitment Manager · C4 Pre-Debit Intervention · C5 Household Multi-Member View (**out of scope**) | PM DECISION (pending) | 🔒 **LOCKED** | 15 Aug 2026 | Opportunity_Backlog |
| LA-16 | RICE scale + arithmetic shown for each | Scale declared (Capstone prescribes none): Reach 1–10 ordinal *(not absolute — no PhonePe MAU, EV-020)* · Impact 3/2/1/0.5/0.25 · Confidence 100/80/50% *(confidence in the evidence for impact)* · Effort 1–10. Scores: **C2 2.800 · C1 1.800 · C3 1.286 · C4 1.000 · C5 0.450.** Arithmetic shown per candidate and independently recomputed | DERIVED from PM ESTIMATES | 🔒 **LOCKED** | 15 Aug 2026 | Selection defensibility |
| LA-17 | **The one selected feature** (named explicitly) | **C2 — Flagged Commitment + One-Tap Action.** Highest RICE by a full point; sits on GAP-1; **the one-tap interaction is specified by the brief, while the specific downstream control remains an open PRD question (U8)**; needs no data beyond the user's own transactions; scope-checked before selection | PM DECISION (pending) | 🔒 **LOCKED** | 15 Aug 2026 | **All of Part B and Part C** |
| LA-18 | HIPPO / vanity-metric rejection paragraph | HIPPO = C3 (most demoable, highest impact ceiling, 50% confidence, ~2× effort) · Vanity metric = C1 (highest reach, lowest effort, optimises insights-viewed while the funnel collapses at the action stage) | PM DECISION (pending) | 🔒 **LOCKED** | 15 Aug 2026 | Selection defensibility |

> **Task 2 status: 🔒 LOCKED by Gaurav, 15 Aug 2026.** Artifact: `PART_A_TASK2_COMPETITIVE_TEARDOWN.md`. All nine rows (LA-10 – LA-18) locked together after the pre-lock correction pass (v2.2).
>
> **Gaurav's verbal justification, recorded for the explainability requirement (Guideline 4):**
> *"I am locking Task 2 because the competitive analysis identifies a defensible insight-to-action gap, C2 has the highest RICE score with visible arithmetic, the selected interaction is explicitly supported by the Capstone, and the remaining uncertainty about the exact downstream control is correctly carried forward as a PRD question rather than being invented."*
>
> ⚠️ **Uncertainties that survive the lock and must be carried downstream, not treated as resolved:**
> - **U8 — UNRESOLVED, MUST BE RESOLVED IN THE PRD.** Which downstream control the one-tap action executes (cap / cancel / revoke) is **not** established by the Capstone. Locking LA-14 and LA-17 locks the *one-tap action*, which is `[CASE DATA]` — it does **not** lock or authorise cancellation.
> - **U2** — CRED Money evidence is ~2 years old with no official product page; the main residual risk to differentiator DIF-1.
> - **U1, U3, U5, U7** — seven unverified matrix cells, four unassessed Indian products, NPCI figures reported but not independently confirmed, Fi Money's current product status unknown.
>
> *Locking these rows fixes the decisions, not the evidence. Every `[NOT VERIFIED]` and `[HYPOTHESIS]` marker in the artifact remains in force.*
| **LA-18b** | **U8 RESOLVED — what the one-tap action does** | **"Stop future auto-debits from PhonePe for this commitment"**, reached via a one-tap action **entry** on the insight detail screen, then a mandatory confirmation. Eligibility rule: essential categories degrade to "remind me". **Confirmation must state the limitation: this does not cancel the user's account or subscription with the merchant.** Fallback: Option D, one-tap entry into mandate management. ⚠️ **`[DESIGN ASSUMPTION — PLATFORM CAPABILITY NOT VERIFIED]`** | **PM DECISION — design assumption, NOT case data** | 🔒 **LOCKED** | 15 Aug 2026 | LA-20, LA-22, LA-24, LB-04 confirmation screen |
| **LA-18c** | **Airtable base** (Part A Task 4 / A20–A24) | **"PhonePe Smart Spend Coach — Capstone (Part A)"** · baseId `appozPM3QfEc0ZJ7V` · workspace `wspBFqLe5HqrmPTfG` · **exactly 2 tables**, as the Capstone specifies. No extra tables, views, formulas or filters — none are required and none were invented | PM DECISION | SET — awaiting lock | 16 Aug 2026 | G06, A24 |
| **LA-18d** | Airtable **Personas** table | tableId `tblrrrjdevx96zuwa`. All 6 required columns, exact names: Persona Name · Segment/Age Range · Willingness-to-Pay Tier · Acquisition Channel · Top Frustration · Top Goal. **2 records** from LA-02 / LA-03. ⚠️ Persona Name uses the **locked segment label**, not an invented individual; Acquisition Channel is `[PM INFERENCE from CASE DATA]` — **both need Gaurav's confirmation** | PM DECISION + PM INFERENCE | SET — awaiting lock | 16 Aug 2026 | LC-09 growth loop |
| **LA-18e** | Airtable **Opportunity_Backlog** table | tableId `tblbQp9idh9CVMBiW`. All 7 required columns, exact names: Idea · Reach · Impact · Confidence · Effort · RICE Score · Decision. **5 records** (4+ required) matching locked LA-15/LA-16/LA-17 exactly: C2 2.800 **Selected** · C1 1.800 · C3 1.286 · C4 1.000 · C5 0.450, all "Not selected" | PM DECISION | SET — awaiting lock | 16 Aug 2026 | Selection defensibility |
| **LA-18f** | Airtable sharing = "Anyone with the link can view" | ⛔ **NOT DONE — REQUIRES GAURAV.** Airtable base sharing cannot be set through the connector. Must be set manually, then the link pasted **as plain text inside Part A** of the Google Doc. **Capstone warns Airtable share links can go stale — retest logged-out close to submission** | — | **BLOCKED — manual step** | 16 Aug 2026 | G06, CA-03 |

> **Numbering note:** the Locked Decisions register did not previously contain Airtable rows. Rather than invent a new scheme, these use the established suffix convention on **LA-18**, which is where Task 4 falls in sequence (immediately after Task 3, which ends at LA-18). **LA-18b is out of sequence** — it is a Task 5 decision — but it is **locked and has not been renumbered.**

| LA-19 | Problem statement (cites persona frustration) | Persona → recurring household commitments accumulate quietly → current experience shows transactions but never assembles the pattern; insight tools cannot act, mandate screens have no insight → noticing and acting become two tasks on two days → opportunity to close the distance. **PM-derived framing, no user research claimed** | PM INFERENCE + FACT | 🔒 **LOCKED** | 15 Aug 2026 | PRD |
| LA-20 | Chosen solution | **C2.** **Core principle: the product does not know a commitment is wasteful — it identifies patterns worth reviewing; the user decides.** Detection uses transaction-derived signals only: base condition (same merchant, regular interval, ≥3 consecutive occurrences) **plus** ≥1 trigger — T1 amount increased vs the user's own prior charges, or T2 charge resumed after a period with none. **Explicitly does NOT know:** service usage, merchant data, email/app activity, trial existence, or objective necessity. Flow: home entry card → insight detail (carries the one-tap action entry) → mandatory confirmation → acted-on state + undo | PM DECISION | 🔒 **LOCKED** | 15 Aug 2026 | Prototype |
| LA-21 | Rejected alternative + why | **C1 Recurring Spend Digest** (RICE 1.800 vs 2.800). Rejected on RICE (Impact 0.5 vs 2.0), user value (informs without removing the friction), scope (spends the build on the solved half), feasibility (cheaper — the honest cost of rejecting it), and strategy (competes with Gemini on explanation while declining the one thing it cannot do) | PM DECISION | 🔒 **LOCKED** | 15 Aug 2026 | — |
| LA-22 | 3–5 user stories | **5 stories:** US1 surfaced · US2 verify the flag · US3 one-tap stop · US4 confirmation + undo · US5 low-confidence state | PM DECISION | 🔒 **LOCKED** | 15 Aug 2026 | INVEST check |
| LA-23 | INVEST line per letter per story | **30 validations (5 × 6), all with justifications.** **Three honest partial-failures recorded rather than forced:** US3 Independent (dependent on data, not on another story's implementation), US3 Estimable (blocked on the LA-18b platform dependency), US4 Independent (independent as a unit of work, conceptually sequenced after US3). US1 Valuable rewritten so it no longer contradicts the C1 rejection | PM DECISION | 🔒 **LOCKED** | 15 Aug 2026 | — |
| LA-24 | **Primary success metric + precise formula** | **Insight-to-Action Completion Rate** = (nudges confirmed-actioned within 7 days of first view ÷ distinct nudges first viewed in the period) × 100. Rolling weekly. **No baseline or target invented** | PM DECISION | 🔒 **LOCKED** | 15 Aug 2026 | LC-03, LC-11 |
| LA-25 | **Guardrail metric + precise formula** | **Action Reversal Rate** = (confirmed actions reversed within 14 days ÷ total confirmed actions in the period) × 100. Weekly. 14-day window because regret surfaces at the next billing cycle | PM DECISION | 🔒 **LOCKED** | 15 Aug 2026 | LC-05 |
| LA-26 | Edge case 1 + behaviour | **Not enough history to judge** — <3 occurrences `[PM-SELECTED]` or <5 category transactions `[CAPSTONE-SUPPLIED]` → explicit low-confidence state showing the occurrence count, charge history + optional watch control, **no action entry offered**, excluded from the LA-24 denominator. **Designated Part B edge-case screen** | PM DECISION | 🔒 **LOCKED** | 15 Aug 2026 | **LB-05 edge-case screen** |
| LA-27 | Edge case 2 + behaviour | **Opt-out of transaction analysis mid-month** → analysis stops, nudges cleared, plain statement of what stopped; already-confirmed actions stand but remain undoable; no continued analysis, no silent reversal, no re-prompt | PM DECISION | 🔒 **LOCKED** | 15 Aug 2026 | LB-05 |
| LA-28 | Out-of-scope line | Any recurring commitment **not paid through the user's own PhonePe account** — other UPI apps, cards, net banking, cash, or another household member's account — is not detected, flagged or acted upon | PM DECISION | 🔒 **LOCKED** | 15 Aug 2026 | Bounds prototype scope |

> **Task 5 status: 🔒 LOCKED by Gaurav, 16 Aug 2026.** Artifact: `PART_A_TASK5_PRD_LITE.md` (revised v2, post-audit). All eleven rows — LA-18b and LA-19 – LA-28 — locked together.
>
> **Gaurav's verbal justification, recorded for the explainability requirement (Guideline 4):**
> *"I am locking Task 5 because the PRD preserves the locked persona and C2 feature, converts the competitive wedge into a defensible transaction-derived product specification without claiming that the system knows a commitment is wasteful, explicitly separates case data from PM assumptions, defines measurable success and guardrail metrics, carries the unverified platform capability with a documented fallback, and preserves the relay chain into Part B."*
>
> **EV-043 RESOLVED** `[PM DECISION — Gaurav, 16 Aug 2026]`: **LA-14 remains unchanged and is not reopened.** "Wasteful" is retained only in the competitive wedge / positioning language. The product must never claim it objectively knows a commitment is wasteful. Product language: *flagged for review · worth reviewing · recurring spending pattern · change in recurring spending pattern*. **The user makes the judgement.**
>
> ⚠️ **Surviving the lock, not resolved by it:** the platform capability behind LA-18b remains `[NOT VERIFIED]`, with **Option D as the documented fallback**. Locking fixes the decision, not the evidence.
>
> **U8 is now resolved as LA-18b — but resolved as a `[PM DECISION]`, not as case data.** The one-tap *interaction* remains `[CASE DATA]`; the control it executes is a design assumption with an unverified platform dependency and a documented fallback. **Nothing in this task presents a PhonePe capability as established that the Capstone does not establish.**
>
> ✅ **RESOLVED 16 Aug 2026 (v2.9): Part A Task 4 (Airtable, A20–A24) is now BUILT** — see rows LA-18c – LA-18f. Base `appozPM3QfEc0ZJ7V`. **Still outstanding within Task 4: LA-18f sharing (manual), plus Gaurav's confirmation of Persona Name and Acquisition Channel.**

## 8.B — Part B (35 marks)

> ⚠️ **STATUS BANNER (added 16 Aug 2026).** Rows **LB-11, LB-12, LB-13** below still show their ORIGINAL pre-work state (empty ☐, and LB-11 still naming the self-walkthrough method that was later abandoned). **Those rows are HISTORICAL. The current state of LB-11 – LB-20 is in §21.1–21.3 and supersedes them.** Preserved unrewritten per the no-rewriting-history rule; do not read the ☐ boxes below as current status.

| # | Decision | Value | Evidence class | Locked? | Date | If changed, invalidates |
|---|---|---|---|---|---|---|
| LB-01 | Prototype scope | Figma file **"PhonePe Smart Spend Coach — Capstone Prototype"**, fileKey `XhV4JoExaeeygvEG1LZGez`. **5 screens** at 390×844 (4 required) + a DESIGN SPEC annotation panel carrying the LA-18b platform assumption and the Option D fallback. Direct implementation of the locked PRD; no new persona, feature, metric or wedge introduced | PM DECISION | 🔒 **LOCKED** | 16 Aug 2026 | Walkthrough |
| LB-02 | Home-screen entry point design | **01 · Home entry** — Smart Spend Coach header, on-screen *"PROTOTYPE — illustrative data, not real user transactions"* banner, one Nudge Card instance (merchant, ₹ amount, interval, observed signal, review CTA), plus a low-confidence entry linking to the edge case | PM DECISION | 🔒 **LOCKED** | 16 Aug 2026 | Walkthrough |
| LB-03 | Insight detail screen design | **02 · Insight detail** — merchant summary, *"WHAT WE OBSERVED"* six-charge history showing the increase, *"WHY YOU'RE SEEING THIS"* (T1 trigger), explicit *"Smart Spend Coach does not know whether you still use this service"*, *"You decide whether this commitment is worth keeping"*, then the **one-tap action entry** + "Keep this charge" | PM DECISION | 🔒 **LOCKED** | 16 Aug 2026 | Walkthrough |
| LB-04 | One-tap action-confirmation screen design | **03 · Action confirmation** — bottom-sheet modal stating WHAT WILL STOP (from the next due date) and WHAT WILL NOT CHANGE, carrying the mandated limitation verbatim: *"Stopping future auto-debits prevents PhonePe from making further payments to this merchant. It does not cancel your account or subscription with the merchant."* Confirm + safe exit ("Go back") | PM DECISION | 🔒 **LOCKED** | 16 Aug 2026 | **LB-13 friction** |
| LB-05 | Edge-case screen (must match LA-26 or LA-27) | **04 · Edge case — not enough history.** Implements **LA-26 (Edge Case 1)**. Low-confidence chip, the 2 observed charges, *"That's not enough history for Smart Spend Coach to flag it for review"*, plus *"We are not saying this charge is fine, and we are not saying it is a problem."* **No action entry offered**; on-screen note that the stop action is absent in this state | PM DECISION | 🔒 **LOCKED** | 16 Aug 2026 | Alarm A3 ✅ matches LA-26 |
| LB-06 | Component(s) | **"Nudge Card"** component set, with a written component description recording that the card never asserts a commitment is wasteful | PM DECISION | 🔒 **LOCKED** | 16 Aug 2026 | Variants |
| LB-07 | Variant(s) | **State=Default** (flagged for review, observed signal, review CTA) and **State=Acted-on** (auto-debits stopped, undo) | PM DECISION | 🔒 **LOCKED** | 16 Aug 2026 | Interactions |
| LB-08 | The ≥3 interactions | **10 navigation interactions (3 required), all NAVIGATE; required flow paths have no dead ends.** *(Wording updated 16 Aug 2026, §24.4 — "Tell me if this repeats" on screen 04 remains deliberately unwired per EV-045, so the claim is scoped to required flow paths rather than to every visible control.)* 01→02 · 01→04 · 02→01 (back) · 02→03 · 02→01 (keep charge) · 03→05 (confirm) · 03→02 (safe exit) · 04→01 (back) · 04→01 (view history) · 05→01 (undo, implements US4). Flow starting point: *"Smart Spend Coach — core flow"*. ⚠️ **A CHANGE-TO-VARIANT shortcut was built then REMOVED in QA** — see EV-044 | PM DECISION | 🔒 **LOCKED** | 16 Aug 2026 | Walkthrough |
| **LB-08b** | Prototype sharing = "Anyone with the link can view" | ⛔ **NOT DONE — REQUIRES GAURAV.** Figma file sharing cannot be set through the Plugin API. **Must be set manually in Figma → Share → Anyone with the link → can view**, then the link pasted into Part B of the Google Doc | — | **BLOCKED — manual step** | 16 Aug 2026 | G07, CA-04 |
| LB-09 | AI-augmented **or** AI-native + justification | **AI-AUGMENTED.** The core observe → evidence → act flow survives without the AI layer: LA-20 detection is deterministic and transaction-derived (merchant/interval pattern + ≥3 occurrences + T1 amount increase or T2 resumed-after-gap), charge history remains available as evidence, and the LA-18b one-tap action remains available. Without AI the experience degrades in merchant recognition, category classification and personalised explanation — **`[PM DESIGN ASSUMPTION]`, the only ML-plausible components; none is specified by the Capstone** — but it does not stop functioning | PM DECISION | 🔒 **LOCKED** | 16 Aug 2026 | LB-10 |

> **Part B Task 1 status: 🔒 LOCKED by Gaurav, 16 Aug 2026.** Rows LB-01 – LB-08. Artifact: Figma file `XhV4JoExaeeygvEG1LZGez` — https://www.figma.com/design/XhV4JoExaeeygvEG1LZGez
>
> **Gaurav's verbal justification, recorded for the explainability requirement (Guideline 4):**
> *"I am locking Part B Task 1 because the prototype directly implements the locked C2 PRD, preserves the transaction-derived detection and user-judgement boundary, correctly handles the low-confidence edge case, and provides a safe insight-to-action flow with mandatory confirmation. QA caught and removed an unsafe variant shortcut and repaired dead prototype controls before usability testing, so the walkthrough will measure the intended product flow rather than prototype wiring defects."*
>
> ⚠️ **Carried forward, not resolved by this lock:**
> - **LB-08b (sharing) is BLOCKED** — the file is **not** publicly accessible until Gaurav sets it manually and verifies it logged-out. Until then requirement **G07 / CA-04 fails**.
> - **LA-18b's platform capability remains `[NOT VERIFIED]`**, with Option D as the documented fallback — recorded in the prototype's DESIGN SPEC panel, not in user-facing copy.
> - **One control is deliberately unwired:** screen 04 *"Tell me if this repeats"*. **Note this before the Part B walkthrough so it is not recorded as a usability finding** (EV-045).
> - **Essential-category treatment** (insurance / EMI / utilities degrade to "remind me") is specified in the locked PRD but **not depicted** in the prototype, which uses a discretionary example. Not a defect; be ready to explain it.
| LB-10 | Biggest **4-dimension** risk (accuracy / latency / token cost / hallucination) + why | **HALLUCINATION RATE.** The AI layer's most consequential role is explaining *why* a pattern was flagged. A fabricated explanation could assert what Smart Spend Coach explicitly does not know — service usage, trial status, objective necessity — violating the locked boundary that the system reports transaction-derived observations and the user judges. Charge history lets a user verify the observed *pattern*, but cannot verify a fabricated *explanation*. **Exactly one dimension named, per the acceptance criterion; the other three are not ranked** | PM DECISION | 🔒 **LOCKED** | 16 Aug 2026 | ⚠️ *Do NOT reuse in Part C — alarm A6* |
| LB-11 | Testing method — **self-walkthrough as each persona** *(your stated choice)* | | | ☐ | | Evidence class of LB-12 |
| LB-12 | ≥6 observations across Errors / Hesitations / Successes / Quotes | | | ☐ | | Severity assignment |
| LB-13 | **The High-priority insight→action friction observation** | | | ☐ | | **THE BATON — invalidates LC-01, LC-02, LC-03** |
| LB-14 | Five ethics design sentences | | | ☐ | | — |
| LB-15 | Bias type (exactly one of 4) + paragraph | | | ☐ | | — |
| LB-16 | Freemium **or** free-trial | | | ☐ | | LC-08 |
| LB-17 | Packaging shape (tiered / usage-based / hybrid) | | | ☐ | | — |
| LB-18 | Pricing trap named & avoided (cost-plus / competitive / gut-feel) | | | ☐ | | — |
| LB-19 | Decoy tier structure, if used | | | ☐ | | — |

## 8.C — Part C (35 marks)

> ⚠️ **STATUS BANNER (added 16 Aug 2026).** Every row below shows its ORIGINAL empty pre-work state. **All of LC-01 – LC-13 are now complete; the current state is in §21.4 and supersedes this table.** Preserved unrewritten; the ☐ boxes below are historical, not current.

| # | Decision | Value | Evidence class | Locked? | Date | If changed, invalidates |
|---|---|---|---|---|---|---|
| LC-01 | Prioritized stage + intent-proximity reasoning | | | ☐ | | LC-02 |
| LC-02 | Which **specific Part B observation** the test addresses | | | ☐ | | Baton 2 integrity |
| LC-03 | Hypothesis in the exact 4-blank template | | | ☐ | | — |
| LC-04 | Primary metric (formula) | | | ☐ | | Duration |
| LC-05 | Secondary metric (formula) | | | ☐ | | — |
| LC-06 | Guardrail metric (formula) | | | ☐ | | — |
| LC-07 | Duration + reasoning (≥1 full 7-day cycle) | | | ☐ | | Pitfall choice |
| LC-08 | Pitfall (one of the 4 named) + matching precaution | | | ☐ | | — |
| LC-09 | Growth loop (Virality / Content / Paid) + channel & WTP justification | | | ☐ | | — |
| LC-10 | The 2 monitoring dimensions (of 5) + why | | | ☐ | | Must not restate LB-10 |
| LC-11 | Token-cost optimisation technique | | | ☐ | | — |
| LC-12 | 5-3-1 dashboard: 1 insight / 5 KPIs / 3 visualisations | | | ☐ | | — |
| LC-13 | Free-path statement (3–5 lines) | | | ☐ | | — |

---

# §9. EVIDENCE SYSTEM

## 9.1 The six classes — never mixed

| Class | Definition | Use | Marker |
|---|---|---|---|
| **CASE DATA** | Supplied directly by the Capstone document or LMS | Quote / use as-is, cite location | `[CASE DATA]` |
| **SOURCE-BACKED FACT** | Supported by a named, checkable external source | Name the source inline | `[FACT: source]` |
| **USER OBSERVATION** | Something **you personally observed** in your own walkthrough | **The only admissible class for usability findings** | `[OBSERVED: date]` |
| **PM DECISION** | A strategic decision **you** made and can defend | State the reasoning, not just the choice | `[PM DECISION]` |
| **HYPOTHESIS** | Intended to be tested; not yet true | Must be labelled untested in the doc | `[HYPOTHESIS]` |
| **AI SUGGESTION** | Generated by me or another AI; unvalidated | **May not survive into the final document under this label** — promote to PM DECISION or delete | `[AI SUGGESTION]` |

**Promotion rule:** an `[AI SUGGESTION]` becomes a `[PM DECISION]` only when you can state, unprompted, *why* it is right — not when you agree with it.

## 9.2 Evidence log — established

| ID | Claim | Class | Source |
|---|---|---|---|
| EV-001 | Deadline is 28 Aug 2026, 11:59 PM IST | CASE DATA | LMS announcement #16057 (31 Jul); assessment countdown "13 days"; assignment window |
| EV-002 | Marks: 100 total — A 30, B 35, C 35; 10% weightage | CASE DATA | Capstone document; LMS #81471 |
| EV-003 | Pilot funnel: 40,000 / 16,000 / **11,200** / 9,520 / 2,856 | CASE DATA | **Capstone document** (supersedes LMS Notes' 10,000) |
| EV-004 | Submission = one Google Doc link, anyone-with-link view | CASE DATA | Capstone document |
| EV-005 | Airtable link inside Part A; Figma link inside Part B; both plain text | CASE DATA | Capstone document |
| EV-006 | Free-tier Figma / Airtable / AI assistant sufficient; no paid API anywhere | CASE DATA | Capstone document |
| EV-007 | Part B may use only Part A persona+PRD; Part C only Part B usability findings | CASE DATA | Capstone document; LMS #163692, #163570 |
| EV-008 | Personas, competitive notes, prototype screens, usability write-ups and all analysis must be own work | CASE DATA | Capstone document, Originality clause |
| EV-009 | Severity guide: High/Medium/Low, defined | CASE DATA | Capstone document, Part B Task 3 |
| EV-010 | Submission = 1 subjective question, 1 rich-text box, MARK AS COMPLETED | CASE DATA | Masai Assessment Platform, observed 15 Aug |
| EV-011 | LMS briefing Notes conflict with the Capstone document in 16 places | *(verified finding)* | §0.1 comparison |
| EV-012 | The two documents Gaurav reported uploading never reached this session | *(negative finding)* | empty uploads dir, no connected folder, empty /mnt/attach |
| EV-013 | Largest-absolute-loss stage ≠ largest-%-drop stage in the corrected funnel | *(verified by computation; answer withheld pending your Part C work)* | Capstone document funnel |
| EV-014 | PhonePe: **700M registered users; 50M merchants**; 56.25% CAGR FY23→FY25 | SOURCE-BACKED FACT (**primary**) | PhonePe press release, 29 Apr 2026 |
| EV-015 | **Over 65% of PhonePe's consumers come from beyond traditional urban hubs** (tier 2/3/4) | SOURCE-BACKED FACT | The Hans India quoting PhonePe, 19 Feb 2026 |
| EV-016 | India: 216M paid video subscription accounts across 143M households; digital subscription revenue +60% to ₹163bn; paid music +37% to 14.4M | SOURCE-BACKED FACT | FICCI-EY *Stories, scale and impact*, EY India newsroom, 24 Mar 2026 |
| EV-017 | ~14M paid music subscriptions despite ~96% of smartphone users consuming music; 38% ever paid for music vs 86% for video; n=15,373 | SOURCE-BACKED FACT | EY–IMI *How India listens, streams and pays for music*, 24 Jul 2026 |
| EV-018 | Gig and platform workers: 7.7M (2020-21) → 23.5M projected (2029-30) | SOURCE-BACKED FACT (**primary, Govt of India**) | NITI Aayog via Press Information Bureau |
| EV-019 | PhonePe FY25: revenue ₹7,115 cr, net loss ₹1,727 cr; financial-services distribution ~7–11% of revenue | SOURCE-BACKED FACT — **secondary** (DRHP summary, DRHP itself not read) | Finshots |
| EV-020 | **PhonePe publishes no monthly-active-user figure and no category-mix or city-tier transaction breakdown** | *(verified negative finding)* | Checked against PhonePe press release, DRHP coverage, multiple aggregators |
| EV-021 | **No credible source quantifying Indian consumer willingness to pay for personal-finance / budgeting / spend-tracking products** | *(verified negative finding)* | Multiple searches; results were SEO listicles and vendor marketing |
| EV-022 | **Source conflict:** paid video subscriptions in India — 216M (FICCI-EY) vs 148.2M (Ormax). Different definitions; neither adopted as settled | *(disclosed conflict)* | EV-016 vs EV-005 |
| EV-023 | **RETRACTED:** PhonePe 600M users / 40M merchants (Business Standard, Mar 2025) — superseded by EV-014 | *(retracted)* | Was used in Task 1 first pass |
| EV-024 | **RETRACTED:** PhonePe UPI market share ~48.6% — traced only to an aggregator blog and an X post; unverifiable against NPCI | *(retracted — deleted, supported no claim)* | Was cited in Task 1 first pass |
| EV-025 | **REJECTED REASONING:** "Indian consumers hold paid digital subscriptions, therefore this segment will pay for Smart Spend Coach" — conflates ability/habit with willingness; contradicted by EV-017 | *(rejected inference — must not reappear)* | Task 1 second-pass audit |
| EV-026 | **Ask Google Pay** launched in India: Gemini-powered conversational assistant; analyses spending patterns, gives savings tips, tailored offers, financial education; opt-in; 10 Indian languages; uses GPay transaction history + CIBIL credit reports | SOURCE-BACKED FACT (**primary**) | Google India official blog, 29 Jul 2026 |
| EV-027 | **Ask Google Pay "cannot initiate or complete payment transactions"**; informational only; not an investment advisor; "like all AI, it can make errors" | SOURCE-BACKED FACT (**primary — vendor-documented negative**) | Google Pay India official help page, retrieved 15 Aug 2026 |
| EV-028 | **Jupiter Money Manager**: categorises every spend; aggregates all bank accounts; "Set Budgets" with "get notified before you go over your budget"; tracks 10+ credit cards and pays bills directly; financial wellness report; tracks investments, EMIs, credit score | SOURCE-BACKED FACT (**primary**) | jupiter.money/money/, retrieved 15 Aug 2026 |
| EV-029 | **CRED Money**: consolidates data from all bank accounts via RBI Account Aggregator; look up transactions by merchant or category; tracks recurring payments (SIPs, rent, staff salaries); reminders; data-science-driven "brief, actionable insights"; not monetised at launch | SOURCE-BACKED FACT — independent; **~2 years old, no official CRED page located** | TechCrunch, 24 Jul 2024 |
| EV-030 | **UPI AutoPay**: 50M+ new mandate registrations Jul 2025 (vs 26M Jul 2024); 808M monthly mandate executions; **20M+ mandates revoked monthly, dominantly from insufficient balance**; ~74% average business declines across top 50 banks | SOURCE-BACKED FACT — reputable independent reporting NPCI data; **NPCI did not confirm before press time** | Business Standard, 7 Sep 2025 |
| EV-031 | **Fi Money (Epifi) wound down banking services in India, March 2026**, pivoting to AI for enterprises. Status of its spend-analysis product **NOT VERIFIED** | SOURCE-BACKED FACT | TechCrunch, 11 Mar 2026 |
| EV-032 | **Google Pay group expenses is split-expense settlement only** (owed by you / owed to you / settled) — **not** household-level spend insight | SOURCE-BACKED FACT (**primary**) | Google Pay India official help page |
| EV-033 | **Jupiter positions its Money Manager against spreadsheets** — "No more spreadsheets" — evidencing the manual spreadsheet as the incumbent indirect competitor | SOURCE-BACKED FACT (**primary**) | jupiter.money/money/ |
| EV-034 | **NOT VERIFIED (searched, no evidence located — absence NOT implied):** whether CRED Money or Jupiter can execute an action from inside an insight; whether Ask Google Pay categorises transactions, detects subscriptions or offers budgets; whether any Indian product offers household-level multi-member spend insight | *(verified negative-search finding)* | Task 2 teardown, §11 |
| EV-035 | **CORRECTION (Task 2 pre-lock audit):** the Capstone specifies *"a one-tap way to act on each nudge"* and *"a suggested weekly cap"* — it does **NOT** establish that PhonePe can cancel a subscription or revoke a UPI mandate. **Cancellation is a potential implementation option, not case data.** All wedge, candidate and selection wording now claims only the one-tap action | *(overclaim corrected — must not reappear)* | Capstone document; Task 2 correction, 15 Aug 2026 |
| EV-036 | **CORRECTION (Task 2 pre-lock audit):** the earlier inference *"commitments are being terminated by failure rather than by decision"* overstated EV-030. Corrected to: **the reported revocation pattern suggests a meaningful share of recurring commitments may end through payment failure rather than deliberate user action.** Suggestive, not conclusive | *(inference downgraded — PM INFERENCE, not FACT)* | Task 2 correction, 15 Aug 2026 |
| EV-044 | **PROTOTYPE QA DEFECT FOUND AND FIXED (Part B Task 1):** the Nudge Card Default variant's CTA carried a `CHANGE_TO` variant reaction. Inherited by the home-screen instance, it flipped the card to "auto-debits stopped" **without passing the mandatory confirmation screen** — contradicting LA-18b and the C10 one-tap-action-entry definition, and defeating the confirmation safety requirement. **Reaction removed.** Variant states are now demonstrated by screens 01 and 05. No change-to-variant interaction remains; the Capstone permits navigate-to *or* change-to-variant, and 10 navigate interactions satisfy the ≥3 requirement | *(prototype defect — locked PRD was correct, the wiring was wrong)* | Prototype QA, 16 Aug 2026 |
| EV-045 | **PROTOTYPE QA — dead controls wired (Part B Task 1):** 02 "← Back", 02 "Keep this charge", 04 "← Back" and 05 "Undo" had no reactions. Left unwired they would have produced **false usability errors** in the Part B walkthrough — prototype artifacts mistaken for product friction, contaminating the Part C baton. All four wired to their natural destinations. **05 "Undo" also implements locked US4.** One control remains deliberately unwired: 04 "Tell me if this repeats" (an opt-in toggle with no destination) — **note it before the walkthrough so it is not recorded as a finding** | *(prototype integrity)* | Prototype QA, 16 Aug 2026 |
| EV-039 | **CORRECTION (PRD audit):** *"no corresponding usage signal"* and *"past a trial period"* were **invented capabilities** — the feature analyses transaction categories and has no usage, merchant, email or app-activity data. **Removed.** Detection rebuilt on transaction-derived signals only, and the product no longer asserts waste: it flags patterns worth reviewing and the user judges | *(invented capability removed — must not reappear)* | Capstone `[CASE DATA]`; PRD audit, 15 Aug 2026 |
| EV-040 | **CORRECTION (PRD audit):** *"service access continues until the current paid period ends"* was an **invented claim about third-party merchant behaviour** shown on a user-facing screen. **Removed.** Replaced with the truthful product limitation: stopping auto-debits prevents PhonePe from paying the merchant; it does not cancel the user's account or subscription with the merchant | *(invented fact removed)* | PRD audit, 15 Aug 2026 |
| EV-041 | **CORRECTION (PRD audit):** "cancellation" had regressed into US3, against EV-035. **Removed.** US3 now describes completing the same supported action, with no cancellation claim | *(regression corrected)* | PRD audit, 15 Aug 2026 |
| EV-042 | **CORRECTION (PRD audit):** *"most capable AI assistant in the market"* and *"the market's most capable AI spend-insight product"* were **unverified superlatives**. **Removed.** Only the narrow verified claim remains: **Ask Google Pay is documented as unable to initiate or complete payment transactions** (EV-027) | *(superlatives removed)* | PRD audit, 15 Aug 2026 |
| EV-043 | ✅ **CLOSED 16 Aug 2026 — resolved by §24.1; the historical text below is preserved.** **⚠️ OPEN QUESTION AGAINST A LOCKED ROW:** LA-14 (locked) reads *"wasteful recurring household commitments"*; the corrected PRD removes "wasteful" from product language. **LA-14 has NOT been changed.** Proposed reconciliation: the wedge states user perception and offered value; the PRD states what the system may assert. **Requires Gaurav's acknowledgement or a decision to revise LA-14** | *(surfaced, not resolved)* | PRD revision, 15 Aug 2026 |
| EV-038 | **LOCK EVENT:** LA-10 – LA-18 locked by Gaurav on 15 Aug 2026 with a recorded verbal justification (see §8.A). **Locking fixes the decisions, not the evidence** — U1, U2, U3, U5, U7 and U8 remain live, and U8 must be resolved in the PRD | *(governance record)* | Gaurav, 15 Aug 2026 |
| EV-037 | **CLARIFICATION (Task 2 pre-lock audit):** RICE Reach values are **relative ordinal PM estimates on the declared 1–10 scale, never population figures.** C2's Reach = 7 sits below C1 (9, insight-only, no detection precondition) and above C4 (5, gated on an active mandate) and C5 (3, needs multi-member participation). No absolute user count is claimed anywhere — see EV-020 | *(scale clarification)* | Task 2 correction, 15 Aug 2026 |

---

# §10. RESEARCH LOG
*Empty by design — no research conducted yet (your Part 13 instruction).*

| ID | Question researched | Tool/source | Date | Finding | Evidence class | Used in |
|---|---|---|---|---|---|---|
| R-001 | | | | | | |

**Rules:** every competitor fact needs a named source logged here *before* it enters the doc. The Capstone document names competitive notes as your own work product — **an unsourced competitor claim is a fabrication risk, not a finding.** I can surface candidates; only you can certify them.

---

# §11. ORIGINALITY PROTECTION

## 11.1 What I MAY do
Structure research · explain frameworks · brainstorm ideas · analyse information you supply · organise findings · draft documents · challenge your reasoning · identify inconsistencies · help calculate metrics · build checklists · review your work · suggest improvements.

## 11.2 What you MUST personally validate and own
*(Bold = named verbatim in the Capstone document's Originality clause.)*
- **Personas**
- **Competitive notes**
- **Prototype screens**
- **Usability write-ups**
- **All analysis**
- Final product decisions · final strategic choices

Plus the explicit prohibition: *"Do not submit another learner's Figma duplicate or Airtable base."*

## 11.3 What I will NEVER fabricate — hard stops
User interviews · user quotes · tester behaviour · usability findings · survey responses · experiment results · A/B test results · product analytics · customer research · competitor facts without evidence · research participants.

**What this means operationally:** if you ask me for "six usability observations," I will not invent them. I will give you the four-part note template (Errors / Hesitations / Successes / Quotes), the severity definitions, and a walkthrough protocol — and you run it. Those six observations are the single thing an evaluator can most easily probe with "walk me through what you saw," and one real observation you noticed yourself is worth more than six invented ones.

**Note the "Quotes" category.** In a self-walkthrough there are no third-party quotes to record. Do not invent them — record your own first-reaction verbalisations as your own, clearly attributed to yourself-as-persona, or state plainly that this category is thin because the test was a simulated walkthrough. The Capstone document explicitly sanctions the simulated route; it does not sanction fictional testers.

## 11.4 The explainability test
Guideline 4 makes this a graded property: *"you must thoroughly understand everything you implement and be able to confidently explain your approach and design decisions if asked during evaluation."*

**Working rule:** before any decision is LOCKED, state the reasoning in your own words, unprompted. If you can't, it isn't ready to lock — however good it looks on the page.

## 11.5 Originality log

| ID | Item | Origin | Your validation | Date |
|---|---|---|---|---|
| O-001 | | | | |

---

# §12. OPEN QUESTIONS

| ID | Question | Why it matters | Owner | Blocking? |
|---|---|---|---|---|
| ~~OQ-01~~ | ~~May I open Start Evaluation?~~ | **RESOLVED 15 Aug — opened with your approval. Capstone document captured; 16 conflicts found (§0.1).** | — | ✅ closed |
| ~~OQ-03~~ | ~~Marks split across A/B/C?~~ | **RESOLVED — 30 / 35 / 35.** | — | ✅ closed |
| ~~OQ-04~~ | ~~Which severity guide?~~ | **RESOLVED — defined in the Capstone document: High = blocks task completion for multiple users; Medium = causes hesitation but is recovered from; Low = minor or isolated.** | — | ✅ closed |
| ~~OQ-07~~ | ~~Testing method?~~ | **RESOLVED — self-walkthrough as each persona (your decision, 15 Aug). Sanctioned by the Capstone document.** | — | ✅ closed |
| **OQ-02** | Connect the folder holding your two documents, or confirm they're redundant | I still see no connected folder. Given I now have the authoritative Capstone document, these are probably duplicates — but if they contain anything else, the matrix is incomplete. | Gaurav | Low |
| **OQ-05** | Have you watched the briefing lecture recording (Sumant Malhotra, 29 Jul, 8–10 PM)? | A 2-hour session may carry instructor guidance absent from the written brief. I cannot transcribe video. | Gaurav | No, recommended |
| **OQ-06** | Do you have free-tier Figma, Airtable and Google accounts ready? | Account setup on day 12 is a preventable failure. | Gaurav | Blocks Part A Task 4 / Part B Task 1 |
| **OQ-08** | Which RICE scoring scale will you use (and will you state it)? | The brief demands visible arithmetic. An unstated scale makes the arithmetic unverifiable. **Insufficient information — requires student decision.** | Gaurav | Blocks A15–A17 |
| **OQ-09** | Will you use all 4 competitive categories or the minimum 3? | Acceptance criterion allows 3; the Gap category is what feeds your wedge. | Gaurav | No |
| **OQ-10** | Decoy tier — in or out? | Optional in the brief. Adds a defensible-pricing talking point, adds scope. | Gaurav | No |

---

# §13. DELIVERABLES ARCHITECTURE

| # | Deliverable | Tool | Access | Lives where | Status |
|---|---|---|---|---|---|
| **D1** | **The case document** — Parts A, B, C in order | **Google Docs** | Anyone with link → **View** | Its link is the submission | NOT STARTED |
| **D2** | **Airtable base** — 2 tables | Airtable (free) | Anyone with link → View | Link plain-text **inside Part A** | NOT STARTED |
| D2a | ↳ **Personas** table — columns: Persona Name · Segment/Age Range · Willingness-to-Pay Tier · Acquisition Channel · Top Frustration · Top Goal | | | 2 personas | NOT STARTED |
| D2b | ↳ **Opportunity_Backlog** table — columns: Idea · Reach · Impact · Confidence · Effort · RICE Score · Decision ("Selected"/"Not selected") | | | all 4+ ideas | NOT STARTED |
| **D3** | **Figma prototype** — ≥4 named screens, ≥1 component, ≥1 variant, ≥3 interactions | Figma (free Starter) | Anyone with link → View | Link plain-text **inside Part B** | NOT STARTED |
| **D4** | **Submission** — Google Doc link in the single answer box, then MARK AS COMPLETED | Masai Assessment Platform via #81471 | — | — | NOT STARTED |
| **D5** | This Control Center | Markdown / Claude Project | Private | Not submitted | ✅ v2.0 |

**Explicitly NOT required and NOT accepted:** images, screenshots, diagrams-to-upload, PDFs of slides, decks, video, audio, PDF/document exports, GitHub, Notion, OneDrive, deployed apps, running code.

## 13.1 The Claude Project — your action, not mine
**I have no tool to create a Claude Project.** Do it manually:
1. claude.ai → **Projects → Create project**
2. Name: **PhonePe Smart Spend Coach — Capstone**
3. Add this Control Center file to **Project knowledge**
4. Custom instructions:
   > Source hierarchy: (1) Official Masai Capstone requirements, (2) the Capstone document on the Masai Assessment Platform, (3) Masai LMS content, (4) submission instructions, (5) case data, (6) validated research, (7) PM hypotheses, (8) AI suggestions. Where the LMS briefing Notes conflict with the Capstone document, the Capstone document wins. Never convert an AI suggestion into a fact. Never fabricate user interviews, quotes, tester behaviour, usability findings, survey responses, experiment results, analytics, customer research, competitor facts without evidence, or research participants. Label unvalidated output [AI SUGGESTION] or [HYPOTHESIS]. Never silently change a LOCKED decision — surface the conflict and stop. If sources are insufficient, say "Insufficient information — requires student decision."
5. Re-upload the Control Center whenever it materially changes.

This Cowork session is **not** that Project and shares no memory with it. This file is the portable carrier that preserves continuity between them.

---

# §14. DEPENDENCY MAP

## 14.1 The critical chain

```
AI-ASSISTED PERSONA APPROACH (LA-01)  ── state which of 3, in one line
   ↓
FOUR SEGMENTATION FACTORS per persona (LA-04…LA-08)
   size · willingness to pay · CAC · expected retention
   ↓
▶ PRIMARY PERSONA (LA-02) ◀ ─────────────────────┬── feeds → PRICING (LB-16/17) via WTP
   ↓                                             ├── feeds → GROWTH LOOP (LC-09) via channel + WTP
PROBLEM STATEMENT (LA-19)                        │
   ↓                                             │
COMPETITIVE TEARDOWN (LA-10…LA-13)               │
   ↓ gaps + differentiators                      │
WEDGE — capability + unmet need + segment (LA-14)┘
   ↓
4+ CANDIDATES → RICE with visible arithmetic (LA-15/16)
   ↓  + HIPPO / vanity-metric rejection (LA-18)
▶▶ THE ONE SELECTED FEATURE (LA-17) ◀◀
   ↓  ⚠ HARD LOCK — everything below dies if this moves
PRD-LITE (a)…(f): problem · solution+rejected · stories+INVEST ·
   primary & guardrail metrics · TWO EDGE CASES · out-of-scope   (LA-19…LA-28)
   ↓
╔══ BATON 1 → Part B may use ONLY this persona + this PRD ══╗
   ↓
FIGMA PROTOTYPE (LB-01…LB-08)
   home entry → INSIGHT DETAIL → one-tap confirmation → EDGE CASE (from LA-26/27)
   + ≥1 component + ≥1 variant + ≥3 interactions
   ↓
AI CLASSIFICATION (LB-09) → 4-DIM RISK CALL (LB-10)  ─── ⚠ do NOT restate in Part C
   ↓
SELF-WALKTHROUGH as each persona (LB-11)
   ↓
≥6 OBSERVATIONS across Errors / Hesitations / Successes / Quotes (LB-12)
   ↓  each rated High / Medium / Low per the defined guide
▶▶ THE HIGH-PRIORITY INSIGHT→ACTION FRICTION (LB-13) ◀◀
   ↓  ⚠ mandatory. Part C has no legitimate target without it.
╔══ BATON 2 → Part C may target ONLY this friction ══╗
   ↓
FUNNEL DIAGNOSIS  ←── CASE DATA 40,000 / 16,000 / 11,200 / 9,520 / 2,856
   four transitions · conv% and drop% each · largest ABS vs largest %
   ↓
PRIORITIZED STAGE (LC-01) ── must invoke INTENT-PROXIMITY explicitly
   ↓                          and explain why the bigger raw loss waits
A/B TEST — names the Part B observation (LC-02), exact 4-blank template (LC-03)
   ↓
METRIC TRIAD (LC-04/05/06) ← derived from LA-24 / LA-25
   ↓
DURATION ≥ one 7-day cycle (LC-07) → PITFALL + PRECAUTION (LC-08)
   ↓
GROWTH LOOP (LC-09) ← primary persona channel + WTP
   ↓
AI EVALUATION — 2 of the 5 MONITORING dims (LC-10) ⚠ distinct from LB-10
   ↓
TOKEN-COST OPTIMISATION (LC-11) → 5-3-1 DASHBOARD (LC-12) ← KPIs from LA-24/25
   ↓
FREE-PATH STATEMENT (LC-13)
```

## 14.2 Per-artefact dependency table

| Artefact | Depends on | Influences later |
|---|---|---|
| Persona approach statement | — | Nothing; but it's a scored deliverable line |
| Four segmentation factors | Candidate segments | Primary-persona justification, RICE Reach |
| **Primary persona** | The four factors | PRD, prototype target, walkthrough role, pricing WTP, growth loop channel |
| Secondary persona | The four factors | Airtable Personas, second walkthrough role |
| Problem statement | Primary persona's frustration | Candidate framing, primary metric |
| Direct + indirect competitors | Problem statement | Feature comparison table |
| Feature table + classification | Competitors | **Gaps → wedge** |
| **Wedge** | Gaps/differentiators + persona | Candidate framing, pricing value story |
| 4+ candidates | Problem + wedge | Opportunity_Backlog |
| **RICE + visible arithmetic** | Candidates + segment size | Selection defensibility (anti-HIPPO evidence) |
| **Selected feature** | RICE, not HIPPO, not vanity metric | **All of Part B and Part C** |
| User stories + INVEST | Selected feature + persona | — |
| **Primary + guardrail metrics** | Selected feature | Metric Triad, 5-3-1 KPIs |
| **Two edge cases** | Selected feature + data reality | **Edge-case screen (LB-05)** |
| Out-of-scope line | Selected feature | Bounds prototype scope |
| Airtable base | Personas + RICE table | Part A link deliverable |
| **Figma prototype** | Persona + PRD + edge cases | Walkthrough substrate |
| Component + variant | Prototype | Interactions, acted-on state |
| AI classification | Selected feature | 4-dim risk call |
| 4-dim risk call | AI classification | *(must NOT be reused as the Part C 5-dim answer)* |
| Self-walkthrough | Prototype + both personas | Observations |
| **≥6 observations, 4 note types** | Walkthrough | Severity ratings |
| **High-pri insight→action friction** | Observations | **A/B hypothesis — the whole Part C spine** |
| Ethics × 5 | Prototype specifics | — |
| Bias type | Transaction-data reality | Edge-case credibility |
| Pricing model + packaging shape | Persona WTP + wedge value | Growth loop WTP argument |
| Funnel diagnosis | CASE DATA | Prioritized stage |
| Prioritized stage | Abs vs % loss + intent proximity | A/B target |
| **A/B hypothesis** | Prioritized stage + **LB-13** | Metric Triad, duration |
| Metric Triad | Hypothesis + LA-24/25 | Duration |
| Duration | Metrics + 7-day cycle | Pitfall choice |
| Pitfall + precaution | Duration + design | — |
| Growth loop | Persona channel + WTP | — |
| 2 monitoring dimensions | LB-09/LB-10 context | Cost-monitoring focus |
| Token-cost technique | Monitoring dims | Free-path statement |
| 5-3-1 dashboard | All metrics above | Final recommendation |
| Free-path statement | Whole build | Submission compliance |

## 14.3 Dependency breakage alarms
I will stop and flag on any of these:

| Alarm | Trigger | Consequence |
|---|---|---|
| **A1** | Part B prototype built against a persona other than LA-02 | Breaks Baton 1 — explicitly forbidden by the Capstone document |
| **A2** | A/B hypothesis doesn't **name** a specific Part B observation | Fails an acceptance criterion outright |
| **A3** | Edge-case screen doesn't match LA-26 or LA-27 | Silent inconsistency; fails "matching one of the two edge cases" |
| **A4** | Metric Triad contradicts LA-24 / LA-25 | Internal inconsistency across parts |
| **A5** | Growth loop channel ≠ the Airtable Acquisition Channel field | Airtable and doc disagree |
| **A6** | Part C's 2 monitoring dimensions restate LB-10's 4-dim risk list | **The brief names this trap explicitly (X14)** |
| **A7** | A new idea, competitor or user need appears mid-document | *"you may not introduce a different persona, a different chosen feature idea, or different success metrics"* |
| **A8** | Funnel arithmetic uses 10,000 for stage 3 | Wrong source (LMS Notes). Correct value is **11,200** |
| **A9** | RICE shown as a bare score with no arithmetic | Fails an acceptance criterion |

---

# §15. FINAL COMPLIANCE AUDIT
*Run twice: on 21 Aug (internal target) and again before submitting.*

| # | Check | Method | ✓ |
|---|---|---|---|
| CA-01 | Every row in §17 marked DONE or consciously accepted | Line-by-line matrix walk | ☐ |
| CA-02 | Google Doc sharing = anyone with link, **View** | Open in a logged-out incognito window | ☐ |
| CA-03 | Airtable link opens for a logged-out viewer, both tables populated as specified | Incognito test | ☐ |
| CA-04 | Figma link opens logged-out; all 3 interactions actually fire | Incognito test, click every trigger | ☐ |
| CA-05 | Parts A, B, C in one doc, in order | Visual scan | ☐ |
| CA-06 | It is a **Google Doc** — not Notion, GitHub, OneDrive, or a PDF | Check file type | ☐ |
| CA-07 | Airtable link sits **inside Part A**; Figma link **inside Part B**; both plain text | Locate both | ☐ |
| CA-08 | **No uploaded media anywhere** in the doc | Scroll for embedded images | ☐ |
| CA-09 | Baton 1 intact: Part B persona/PRD == LA-02/LA-19…28 | Side-by-side compare | ☐ |
| CA-10 | Baton 2 intact: A/B hypothesis **names** the LB-13 observation | Text search | ☐ |
| CA-11 | All 4 segmentation factors present for **both** personas | Count them | ☐ |
| CA-12 | RICE arithmetic **visible** for all 4+ ideas | Check each row | ☐ |
| CA-13 | Every user story checked against **all six** INVEST letters | 3 stories × 6 = 18 lines minimum | ☐ |
| CA-14 | All metric formulas computable, with a time factor | Read each aloud — could you compute it from data? | ☐ |
| CA-15 | ≥6 observations spanning **all four** note types | Tally by type | ☐ |
| CA-16 | ≥1 **High**-priority observation is specifically insight→action friction | Read the High rows | ☐ |
| CA-17 | All 5 ethics principles name a **concrete mechanism**, not a promise | Read each sentence | ☐ |
| CA-18 | Exactly **one** bias type named, with a feature-specific paragraph | Count | ☐ |
| CA-19 | Pricing names **both** the model and the packaging shape, plus a trap avoided | Locate all three | ☐ |
| CA-20 | Funnel uses **11,200** at stage 3; all four transitions computed | Check the number | ☐ |
| CA-21 | Largest-absolute and largest-% stages both identified, and shown to differ | Read the two sentences | ☐ |
| CA-22 | Prioritization explicitly invokes **intent proximity** and explains the deferred stage | Text search | ☐ |
| CA-23 | Hypothesis uses the exact template, all four blanks filled | Compare word-for-word | ☐ |
| CA-24 | Metric **Triad** — three metrics, all as formulas | Count | ☐ |
| CA-25 | Duration explicitly covers ≥7 days, with reasoning | Read | ☐ |
| CA-26 | Pitfall is one of the four named, paired with a precaution | Check against the list | ☐ |
| CA-27 | Part C's 2 monitoring dimensions are **not** a restatement of LB-10 | Compare the two lists | ☐ |
| CA-28 | Dashboard = exactly 1 insight + 5 KPIs + 3 visualisations, all feature-specific | Count; check for generic placeholders | ☐ |
| CA-29 | Free-path statement present, 3–5 lines | Locate | ☐ |
| CA-30 | No `[AI SUGGESTION]` / `[HYPOTHESIS]` markers left un-promoted | Text search | ☐ |
| CA-31 | Every competitor claim has a source you personally checked | Cross-check §10 | ☐ |
| CA-32 | Nothing fabricated from the §11.3 list | Hard-stop scan | ☐ |
| CA-33 | You can explain every LOCKED decision unprompted | Verbal rehearsal, out loud, no notes | ☐ |
| CA-34 | Doc link pasted in the answer box; **MARK AS COMPLETED** clicked | Confirm on-screen state | ☐ |
| CA-35 | Submitted before 28 Aug 2026, 11:59 PM IST | Timestamp | ☐ |

---

# §16. FINAL SUBMISSION CHECKLIST

**T-7 (21 Aug — internal target)**
- ☐ Parts A, B, C fully drafted in the Google Doc
- ☐ Airtable base built, both tables populated to spec, sharing set
- ☐ Figma prototype complete: 4 named screens, component + variant, 3 interactions
- ☐ First Final Compliance Audit run (§15)

**T-3**
- ☐ All three links tested **in a logged-out incognito window**
- ☐ Full read-through for baton continuity (alarms A1–A9)
- ☐ Explainability rehearsal — every LOCKED decision, aloud, no notes
- ☐ Text-search the doc for `[AI SUGGESTION]` / `[HYPOTHESIS]` — none should survive

**T-1**
- ☐ Re-test all three links (Airtable share links can go stale)
- ☐ Second Final Compliance Audit
- ☐ Paste the Google Doc link into the assessment answer box
- ☐ **Click MARK AS COMPLETED.** Do not wait for the final day — the 31 Jul announcement explicitly warns that last-minute technical or connectivity issues may affect timely submission.
- ☐ Capture confirmation of submission

**Hard deadline: 28 Aug 2026, 11:59 PM IST. No further extension. No exceptions.**

---

# §17. COMPLETE REQUIREMENTS MATRIX

> ⚠️ **STATUS BANNER (added 16 Aug 2026).** The **Status** column throughout this matrix records the position **when the matrix was first built (15 Aug)** — 111 rows still read "NOT STARTED". **That column is HISTORICAL and is now wrong for almost every row.**
>
> **The authoritative current status is §21.6 and `FINAL_COMPLIANCE_AND_VIVA.md` Part 2: 93 PASS · 2 PARTIAL · 12 BLOCKED · 1 FAIL (B18).** The requirement TEXT, IDs, sources and dependencies in this matrix remain correct and authoritative — only the Status column is stale, and it is preserved rather than rewritten.

**Source key:** `CAP-DOC` = Capstone document on the Masai Assessment Platform (**authoritative**) · `CAP-AC` = its acceptance criteria · `LMS-ASSIGN` = assignment #81471 · `LMS-ANN` = announcement #16057 · `LMS-NOTE` = briefing Notes #163692 (lower authority)
**Mandatory:** M = explicitly required · AC = required by an acceptance criterion · C = conditional

## GLOBAL / SUBMISSION

| ID | Requirement | Part | Mand. | Source | Dependency | Deliverable | Status |
|---|---|---|---|---|---|---|---|
| G01 | Submit **one Google Doc link only** | All | M | CAP-DOC | — | D4 | NOT STARTED |
| G02 | Sharing = "Anyone with the link can view" | All | M | CAP-DOC | G01 | D1 | NOT STARTED |
| G03 | Parts A, B, C in order, same document | All | M | CAP-DOC | G01 | D1 | NOT STARTED |
| G04 | Any other link (Notion, GitHub, OneDrive, PDF) **will not be graded** | All | M | CAP-DOC | G01 | D1 | NOT STARTED |
| G05 | No separate submission per Part | All | M | CAP-DOC | — | D4 | NOT STARTED |
| G06 | Airtable view link, plain text, **inside Part A** at point of first need | A | M | CAP-DOC | A24 | D2 | NOT STARTED |
| G07 | Figma link, plain text, **inside Part B** at point of first need | B | M | CAP-DOC | B10 | D3 | NOT STARTED |
| G08 | **No uploaded media of any kind** — images, screenshots, diagrams, slide PDFs, decks, video, audio | All | M | CAP-DOC | — | D1 | NOT STARTED |
| G09 | No screenshots of Airtable/Figma — the live link is the deliverable | All | M | CAP-DOC | G06, G07 | D1 | NOT STARTED |
| G10 | Describing screens/flows in words is permitted | B | — | CAP-DOC | — | D1 | N/A |
| G11 | Free-tier Figma Starter is sufficient | B | — | CAP-DOC | — | D3 | N/A |
| G12 | Free-tier Airtable is sufficient | A | — | CAP-DOC | — | D2 | N/A |
| G13 | Free AI chat assistant sufficient; **no paid API key or developer account anywhere** | All | — | CAP-DOC | — | C29 | N/A |
| G14 | **Originality:** personas, competitive notes, prototype screens, usability write-ups and all analysis are your own work product for this brief | All | M | CAP-DOC | §11 | D1 | ONGOING |
| G15 | Do not submit another learner's Figma duplicate or Airtable base | All | M | CAP-DOC | — | D2, D3 | ONGOING |
| G16 | Links & details only in their respective answer boxes | All | M | LMS-ASSIGN | G01 | D4 | NOT STARTED |
| G17 | Submit before **28 Aug 2026, 11:59 PM IST** | All | M | LMS-ANN | all | D4 | NOT STARTED |
| G18 | All links accessible and working before submitting | All | M | LMS-ASSIGN | G02, G06, G07 | CA-02/03/04 | NOT STARTED |
| G19 | No plagiarism; own understanding and effort | All | M | LMS-ASSIGN | §11 | D1 | ONGOING |
| G20 | Able to confidently explain approach & design decisions at evaluation | All | M | LMS-ASSIGN | §11.4 | rehearsal | NOT STARTED |
| G21 | Test everything thoroughly before submission | All | M | LMS-ASSIGN | §15 | CA-01…35 | NOT STARTED |
| G22 | Relay rule: Part B uses **only** Part A persona + PRD; no different persona, feature idea, or success metrics | A→B | M | CAP-DOC | LA-02, LA-17 | CA-09 | NOT STARTED |
| G23 | Relay rule: Part C targets **only** Part B usability findings | B→C | M | CAP-DOC | LB-13 | CA-10 | NOT STARTED |
| G24 | Marks: 100 total — A 30 · B 35 · C 35; 10% weightage | All | — | CAP-DOC, LMS-ASSIGN | — | — | N/A |

## PART A — Research, Persona & Feature PRD (30 marks)

| ID | Requirement | Part | Mand. | Source | Dependency | Deliverable | Status |
|---|---|---|---|---|---|---|---|
| A01 | Build **two personas** for the Smart Spend Coach | A | M | CAP-DOC | — | D1, D2a | NOT STARTED |
| A02 | Use one of three AI-assisted persona approaches (direct AI knowledge / guided AI Q&A / AI-plus-uploaded-notes) and **state which, in one line** | A | M | CAP-DOC | A01 | D1 | NOT STARTED |
| A03 | Persona 1: state **segment size** — a reasoned estimate, not a fabricated precise figure | A | AC | CAP-AC | A01 | D1 | NOT STARTED |
| A04 | Persona 1: state **willingness to pay** | A | AC | CAP-AC | A01 | D1 | NOT STARTED |
| A05 | Persona 1: state **cost of acquisition** | A | AC | CAP-AC | A01 | D1 | NOT STARTED |
| A06 | Persona 1: state **expected retention** | A | AC | CAP-AC | A01 | D1 | NOT STARTED |
| A07 | Persona 2: all four factors above | A | AC | CAP-AC | A01 | D1 | NOT STARTED |
| A08 | Use the four factors to explain **in writing** why one persona is the primary target | A | M | CAP-DOC | A03–A07 | D1 | NOT STARTED |
| A09 | One-line justification of which factor is primary | A | AC | CAP-AC | A08 | D1 | NOT STARTED |
| A10 | Name ≥1 **direct competitor** for a spend-insight feature | A | M | CAP-DOC | — | D1 | NOT STARTED |
| A11 | Name ≥1 **indirect competitor** (same job — "understand and control my spending" — different product form) | A | M | CAP-DOC | — | D1 | NOT STARTED |
| A12 | Feature-comparison table with **≥6 relevant features** | A | M | CAP-DOC | A10, A11 | D1 | NOT STARTED |
| A13 | Classify them across **≥3 of the 4** categories: table stakes / parity / differentiator / gap | A | AC | CAP-AC | A12 | D1 | NOT STARTED |
| A14 | State one **competitive wedge**, drawn from gaps and differentiators, in the exact three-part form: unique capability + unmet need + target segment | A | M | CAP-DOC | A13 | D1 | NOT STARTED |
| A15 | Generate **≥4 candidate versions** of the feature idea (different scopes) | A | M | CAP-DOC | A14 | D1, D2b | NOT STARTED |
| A16 | Score each with **RICE — Reach, Impact, Confidence, Effort** | A | M | CAP-DOC | A15 | D2b | NOT STARTED |
| A17 | **Show the arithmetic** for each score — not just the final number | A | AC | CAP-AC | A16 | D1, D2b | NOT STARTED |
| A18 | Pick the highest-scoring, most build-appropriate idea and **explicitly name it** as the one feature the whole project is about | A | M | CAP-DOC | A16 | D1 | NOT STARTED |
| A19 | One paragraph explaining why the choice is not swayed by a **HIPPO-style opinion or a vanity metric** — explicitly naming and rejecting the temptation | A | AC | CAP-AC | A18 | D1 | NOT STARTED |
| A20 | Airtable **Personas** table — columns: Persona Name, Segment/Age Range, Willingness-to-Pay Tier, Acquisition Channel, Top Frustration, Top Goal | A | M | CAP-DOC | A01 | D2a | NOT STARTED |
| A21 | Populate it with **both** personas | A | AC | CAP-AC | A20 | D2a | NOT STARTED |
| A22 | Airtable **Opportunity_Backlog** table — columns: Idea, Reach, Impact, Confidence, Effort, RICE Score, Decision | A | M | CAP-DOC | A15, A16 | D2b | NOT STARTED |
| A23 | Populate with all 4+ ideas; Decision marked "Selected" / "Not selected" | A | AC | CAP-AC | A22 | D2b | NOT STARTED |
| A24 | Set base sharing to "Anyone with the link can view" and paste the link into the doc | A | M | CAP-DOC | A20, A22 | D2, G06 | NOT STARTED |
| A25 | PRD-lite **(a)** one-paragraph problem statement **citing your persona's frustration** | A | M | CAP-DOC | A02, A18 | D1 | NOT STARTED |
| A26 | PRD-lite **(b)** chosen solution + **one rejected alternative and why** | A | M | CAP-DOC | A18 | D1 | NOT STARTED |
| A27 | PRD-lite **(c)** 3–5 user stories: "As a [persona], I want to [goal], so that [benefit]" | A | M | CAP-DOC | A18 | D1 | NOT STARTED |
| A28 | Each story checked against **every letter of INVEST, one line per letter** | A | AC | CAP-AC | A27 | D1 | NOT STARTED |
| A29 | PRD-lite **(d)** one **primary success metric** + one **guardrail metric**, each a precise, unambiguous formula (not a vague label) | A | AC | CAP-AC | A18 | D1 | NOT STARTED |
| A30 | PRD-lite **(e)** **two concrete edge cases** and how the feature behaves in each | A | M | CAP-DOC | A18 | D1 | NOT STARTED |
| A31 | PRD-lite **(f)** one explicit **out-of-scope** line for this version | A | M | CAP-DOC | A18 | D1 | NOT STARTED |

## PART B — Prototype, Usability Validation & Pricing (35 marks)

| ID | Requirement | Part | Mand. | Source | Dependency | Deliverable | Status |
|---|---|---|---|---|---|---|---|
| B01 | Build a **clickable Figma prototype** of the selected feature's core flow — using the exact feature, personas and PRD-lite from Part A, **not a new idea** | B | M | CAP-DOC | A18, A27 | D3 | NOT STARTED |
| B02 | Screen (a): **home-screen entry point** where the insight first appears | B | AC | CAP-AC | B01 | D3 | NOT STARTED |
| B03 | Screen (b): **insight detail screen** | B | AC | CAP-AC | B01 | D3 | NOT STARTED |
| B04 | Screen (c): **one-tap action-confirmation screen** | B | AC | CAP-AC | B01 | D3 | NOT STARTED |
| B05 | Screen (d): **one edge-case screen matching one of the two Part A edge cases** | B | AC | CAP-AC | A30 | D3 | NOT STARTED |
| B06 | **≥1 component** | B | AC | CAP-AC | B01 | D3 | NOT STARTED |
| B07 | **≥1 variant** of that component (e.g. nudge card "default" / "acted-on") | B | AC | CAP-AC | B06 | D3 | NOT STARTED |
| B08 | **≥3 interactions** — tap triggers with navigate-to or change-to-variant actions | B | AC | CAP-AC | B02–B07 | D3 | NOT STARTED |
| B09 | Set prototype to "Anyone with the link can view" | B | M | CAP-DOC | B08 | D3 | NOT STARTED |
| B10 | Paste the Figma link into the document, inside Part B | B | M | CAP-DOC | B09 | D1, G07 | NOT STARTED |
| B11 | Classify the feature **AI-augmented or AI-native**, using the standard distinction | B | M | CAP-DOC | A18 | D1 | NOT STARTED |
| B12 | One-paragraph justification tied to how much of the experience stops functioning without the AI layer | B | AC | CAP-AC | B11 | D1 | NOT STARTED |
| B13 | State which **one** of the four AI evaluation dimensions — accuracy / response speed–latency / token cost–efficiency / hallucination rate — is the single biggest risk for this feature, and why | B | AC | CAP-AC | B11 | D1 | NOT STARTED |
| B14 | Run a usability test: 5 real testers, **or** a rigorously simulated walkthrough acting as each Part A persona *(your choice: self-walkthrough)* | B | M | CAP-DOC | B09, A01 | D1 | NOT STARTED |
| B15 | Use the **four-part note-taking format**: Errors / Hesitations / Successes / Quotes | B | M | CAP-DOC | B14 | D1 | NOT STARTED |
| B16 | Record **≥6 observations total, across all four note types** | B | AC | CAP-AC | B15 | D1 | NOT STARTED |
| B17 | Assign each a priority **High / Medium / Low** per the defined severity guide | B | AC | CAP-AC | B16 | D1 | NOT STARTED |
| B18 | ⚠ **≥1 High-priority observation must describe friction specifically between viewing a personalized insight and completing the recommended action** | B | AC | CAP-AC | B16 | D1 | NOT STARTED |
| B19 | Ethics pass: one sentence per principle stating a **concrete design choice** — Transparency | B | AC | CAP-AC | B01 | D1 | NOT STARTED |
| B20 | …User Control | B | AC | CAP-AC | B01 | D1 | NOT STARTED |
| B21 | …Privacy-by-Design | B | AC | CAP-AC | B01 | D1 | NOT STARTED |
| B22 | …Fairness | B | AC | CAP-AC | B01 | D1 | NOT STARTED |
| B23 | …Graceful Failure | B | AC | CAP-AC | B01 | D1 | NOT STARTED |
| B24 | Name **exactly one** bias type — Representation / Measurement / Aggregation / Evaluation — most realistic for a spending-pattern feature tuned on existing transaction data, + one-paragraph risk explanation | B | AC | CAP-AC | B01 | D1 | NOT STARTED |
| B25 | Choose **freemium or free-trial** | B | AC | CAP-AC | A04 | D1 | NOT STARTED |
| B26 | Choose a **packaging shape** — tiered / usage-based / hybrid | B | AC | CAP-AC | B25 | D1 | NOT STARTED |
| B27 | Justify against Part A personas' willingness-to-pay | B | AC | CAP-AC | B25, A04 | D1 | NOT STARTED |
| B28 | Explicitly name ≥1 of the three pricing traps being avoided — **cost-plus / competitive / gut-feel** | B | AC | CAP-AC | B25 | D1 | NOT STARTED |
| B29 | If a decoy tier is used: name all three tiers and which one the decoy pushes toward | B | C | CAP-DOC | B26 | D1 | NOT STARTED |

## PART C — Growth Funnel, Experiment Design & AI Evaluation (35 marks)

| ID | Requirement | Part | Mand. | Source | Dependency | Deliverable | Status |
|---|---|---|---|---|---|---|---|
| C01 | Use the funnel: 40,000 / 16,000 / **11,200** / 9,520 / 2,856 | C | M | CAP-DOC | — | D1 | CASE DATA |
| C02 | Compute conversion for transition **1→2** (% converted **and** % dropped) | C | AC | CAP-AC | C01 | D1 | NOT STARTED |
| C03 | …**2→3** | C | AC | CAP-AC | C01 | D1 | NOT STARTED |
| C04 | …**3→4** | C | AC | CAP-AC | C01 | D1 | NOT STARTED |
| C05 | …**4→5** | C | AC | CAP-AC | C01 | D1 | NOT STARTED |
| C06 | All four arithmetically correct | C | AC | CAP-AC | C02–C05 | D1 | NOT STARTED |
| C07 | Separately report the stage with the **largest absolute** number of users lost | C | M | CAP-DOC | C06 | D1 | NOT STARTED |
| C08 | Separately report the stage with the **largest percentage** drop-off | C | M | CAP-DOC | C06 | D1 | NOT STARTED |
| C09 | Correctly show these are **different stages** | C | AC | CAP-AC | C07, C08 | D1 | NOT STARTED |
| C10 | Explain, **using the intent-proximity principle explicitly**, which you would fix first | C | AC | CAP-AC | C09 | D1 | NOT STARTED |
| C11 | Explain why the other is lower priority **despite losing more raw users** | C | M | CAP-DOC | C10 | D1 | NOT STARTED |
| C12 | Design **one A/B test** targeting the prioritized stage | C | M | CAP-DOC | C10 | D1 | NOT STARTED |
| C13 | **Name which specific Part B observation** the hypothesis addresses | C | AC | CAP-AC | B18, C12 | D1 | NOT STARTED |
| C14 | Write the hypothesis in the **exact template**, all four blanks filled: *"We believe that \<change\> will result in \<measurable outcome\> because \<reason\>. We will measure \<primary metric\>."* | C | AC | CAP-AC | C13 | D1 | NOT STARTED |
| C15 | Metric Triad — **primary** metric as a precise formula | C | AC | CAP-AC | C14, A29 | D1 | NOT STARTED |
| C16 | …**secondary** metric as a precise formula | C | AC | CAP-AC | C14 | D1 | NOT STARTED |
| C17 | …**guardrail** metric as a precise formula | C | AC | CAP-AC | C14, A29 | D1 | NOT STARTED |
| C18 | Reasoned test duration explicitly covering **≥1 full 7-day behavior cycle** | C | AC | CAP-AC | C15 | D1 | NOT STARTED |
| C19 | Name **one** pitfall this specific design risks — Early Judgment Error / Local Maxima Trap / Novelty Effect / HARKing | C | AC | CAP-AC | C18 | D1 | NOT STARTED |
| C20 | State **one concrete precaution** against it | C | AC | CAP-AC | C19 | D1 | NOT STARTED |
| C21 | Select one growth loop — **Virality / Content / Paid** | C | AC | CAP-AC | A08 | D1 | NOT STARTED |
| C22 | Justify in one paragraph referencing the primary persona's **acquisition channel** | C | AC | CAP-AC | C21, A20 | D1 | NOT STARTED |
| C23 | …and their **willingness-to-pay** | C | AC | CAP-AC | C21, A04 | D1 | NOT STARTED |
| C24 | Name **2 of the 5** monitoring dimensions — quality / cost / accuracy / operational efficiency / safety — to monitor weekly, with reasons | C | AC | CAP-AC | B13 | D1 | NOT STARTED |
| C25 | ⚠ Do **not** restate Part B's 4-dimension risk list as the answer — the brief names them as distinct frameworks | C | M | CAP-DOC | B13, C24 | D1 | NOT STARTED |
| C26 | One concrete **token-cost optimization technique** applied specifically to this feature's insight-generation calls | C | AC | CAP-AC | C24 | D1 | NOT STARTED |
| C27 | 5-3-1 dashboard: exactly **1 core insight metric** | C | AC | CAP-AC | A29 | D1 | NOT STARTED |
| C28 | …exactly **5 supporting KPIs** | C | AC | CAP-AC | A29 | D1 | NOT STARTED |
| C29 | …exactly **3 visualizations** — all specific to Smart Spend Coach, **not generic placeholders**, described in text | C | AC | CAP-AC | C28 | D1 | NOT STARTED |
| C30 | **3–5 lines** stating the free path for every AI-tool dependency; confirm no paid API or account-gated service was required anywhere | C | AC | CAP-AC | — | D1 | NOT STARTED |

**Total: 114 tracked requirements — 24 global · 31 Part A · 29 Part B · 30 Part C.**

---

# §18. COMPLIANCE RISK REGISTER
Ranked by expected mark loss. Re-read this on 21 Aug.

| # | Risk | Likelihood | Severity | Why it costs marks | Mitigation |
|---|---|---|---|---|---|
| **R1** | **Using the LMS Notes instead of the Capstone document** | **Was near-certain before v2.0** | **Critical** | 16 divergences (§0.1), several fatal: wrong funnel number, missing Confidence in RICE, missing the four named segmentation factors, missing the insight-detail screen. | ✅ **Largely mitigated by v2.0.** Treat §17 as the single source. Re-open the assessment platform if in doubt. |
| **R2** | **Broken baton** — persona drift into Part B, or a Part C hypothesis not traceable to a Part B observation | **High** | **Critical** | The brief forbids it in two places and the acceptance criteria test for it. The pre-read says the thread *"is what capstone grading is really looking for."* | Lock LA-02/LA-17 and LB-13 before starting downstream work. Run alarms A1–A9 at every part boundary. |
| **R3** | **Fabricated usability observations** | **High** if rushed | **Critical** | Usability write-ups are named in the Originality clause. Invented tester behaviour collapses under "walk me through what you saw." | I will never generate them. Book the self-walkthrough as a real calendar slot; record as you go, not afterwards. |
| **R4** | **Missing the mandatory High-priority insight→action observation (B18)** | Medium | **Critical** | Explicit acceptance criterion in Part B, **and** Part C's hypothesis has no legitimate anchor without it. Damages both parts. | Design the confirmation flow so this friction is genuinely testable. Look for it deliberately. |
| **R5** | **Funnel arithmetic wrong** (using 10,000 at stage 3, or mis-computing) | **High** | **Critical** | Acceptance criterion demands all four transitions "arithmetically correct." One wrong input cascades through C02–C11. | Alarm A8. CA-20. Recompute from the Capstone document's table, not from memory or the Notes. |
| **R6** | **RICE without visible arithmetic**, or without Confidence | **High** | **High** | Two separate acceptance criteria. | CA-12. Show R, I, C, E and the formula per idea. State your scale (OQ-08). |
| **R7** | **Link access failure at submission** | Medium | **Critical** | Guideline 5 requires working links; guideline 2 says incorrect submissions may mean **zero**. | Test all three in a logged-out incognito window at T-3 **and** T-1. |
| **R8** | **Wrong submission format** — Notion, GitHub, OneDrive, PDF | Low | **Critical** | "will not be graded." | CA-06. Build in Google Docs from day one; never export. |
| **R9** | **Uploading any media** | Medium | High | Not merely unnecessary — *"not required **or accepted**"*. | CA-08. Describe screens in words; links only. |
| **R10** | **Restating Part B's 4-dim risk list as Part C's 2 monitoring dimensions** | **High** | High | The brief calls out this exact trap by name — a clear signal it is being marked. | Alarm A6. CA-27. Keep the two lists visibly separate in the doc. |
| **R11** | **Vague metrics without a time factor** | **High** | High | Affects A29, C15, C16, C17 — four requirements across two parts. The brief's own good example embeds "within 7 days." | CA-14. Write every metric as numerator ÷ denominator per unit time. Read it aloud: could you compute it? |
| **R12** | **Hypothesis not in the exact template** | **High** | High | Acceptance criterion: "uses the exact hypothesis template with **all four blanks filled**." | CA-23. Copy the template literally, then fill it. |
| **R13** | **Metric Triad submitted as a duo** | Medium | High | Three metrics required; the Notes only mentioned two. | CA-24. Count them. |
| **R14** | **Pricing missing the packaging shape** | **High** | High | The Notes omit it entirely; the acceptance criterion requires "**both** the free/paid model and the packaging shape." | CA-19. |
| **R15** | **Un-sourced competitor facts** | **High** | High | Competitive notes are named own-work. Unverifiable claims fail both originality and accuracy. | §10 row required before any claim enters the doc. |
| **R16** | **Reusing the brief's own worked examples as your answers** | **High** | High | The brief supplies examples for nearly every task (the four candidate scopes, the nudge-card variant, the <5-transactions edge case, the metric wording, the caching technique). They are *illustrations*. Every classmate reads the same page. | Use them to understand the shape of the answer; produce your own. Where you deliberately agree, say so and give your own reasoning. |
| **R17** | **Generic ethics statements** | **High** | Medium | Acceptance criterion explicitly rejects "we will be transparent" without a stated mechanism. | CA-17. Each sentence must name a specific screen element or system behaviour. |
| **R18** | **INVEST as a summary rather than letter-by-letter** | **High** | Medium | "each checked against **every letter** of INVEST in one line." 3 stories × 6 letters = 18 lines minimum. | CA-13. Build it as a table: rows = stories, columns = I/N/V/E/S/T. |
| **R19** | **Generic dashboard placeholders** | Medium | Medium | Acceptance criterion: "all specific to this feature (**not generic placeholders**)." | CA-28. Every KPI must name Smart Spend Coach behaviour. |
| **R20** | **Prioritization without naming intent proximity** | Medium | Medium | Acceptance criterion: "the prioritization reasoning **explicitly invokes** the intent-proximity principle." | CA-22. Use the phrase. |
| **R21** | **Cannot explain a decision at evaluation** | Medium | High | Guideline 4 makes explainability graded, independent of document quality. | No LOCK without unprompted verbal justification. Rehearse at T-3. |
| **R22** | **Running out of time on Figma** | Medium | High | Part B is 35 marks and the prototype is the only artefact requiring tool skill rather than writing, with 10 sub-requirements. | Start Figma before Part A is polished. 4 screens + component + variant + 3 interactions is the floor. |
| **R23** | **Relaxing because of the 28 Aug extension** | Medium | Medium | 13 days feels comfortable; the prototype and walkthrough are not compressible. | Internal target 21 Aug. Buffer is for audit and rehearsal only. |
| **R24** | **Accidentally clicking MARK AS COMPLETED early** | Low | **Critical** | Finalises the submission. The tab is currently open in your browser with an empty answer box. | Close that tab until you're ready, or leave it and be careful. Only click it at T-1 with the link pasted. |

---

# §19. READINESS ASSESSMENT

### What we know
- **The complete, authoritative Capstone document** — 3 parts, 15 tasks, every acceptance criterion. **114 requirements catalogued.**
- **The marks split: A 30 · B 35 · C 35**, out of 100, at 10% weightage.
- **The real deadline: 28 Aug 2026, 11:59 PM IST** — 13 days.
- **The submission mechanism**: one rich-text answer box, MARK AS COMPLETED.
- **The corrected funnel data** (stage 3 = 11,200, not 10,000).
- **The severity guide, the four note types, the RICE requirement, the exact hypothesis template, the two distinct AI frameworks** — all the things the LMS Notes got wrong or left vague.
- Where the LMS Notes conflict with the Capstone document, and which wins.

### What we still need to determine
- **Your RICE scoring scale** (OQ-08) — *Insufficient information — requires student decision.*
- Whether the briefing lecture recording adds anything (OQ-05).
- Whether your two documents contain anything beyond the Capstone document (OQ-02) — probably not.
- Whether you'll use 3 or 4 competitive categories (OQ-09), and whether a decoy tier is in scope (OQ-10).
- **Every substantive product decision** — all 60 rows in §8 are unlocked.

### What you must personally do
1. Create the Claude Project (§13.1) and load this file into it.
2. Confirm free-tier Figma, Airtable and Google accounts (OQ-06).
3. Decide your RICE scale (OQ-08).
4. Make and defend every LOCKED decision.
5. **Build the Figma prototype yourself** — prototype screens are named own-work.
6. **Run the self-walkthrough yourself and record the six observations yourself**, in the four-part format, as you go.
7. Personally verify every competitor fact before it enters the doc.
8. Do the funnel arithmetic yourself (I've verified my own copy; I've deliberately kept the answers out of this document).
9. Explainability rehearsal, out loud, at T-3.

### What I can help with
Structuring your research · explaining any framework here (RICE, INVEST, the four bias types, the four pitfalls, decoy pricing, growth loops) · pressure-testing your persona, wedge and RICE reasoning · checking INVEST letter by letter · auditing every metric formula for computability and time factors · **checking your** funnel arithmetic · red-teaming your A/B design · checking every part boundary for baton breakage (alarms A1–A9) · maintaining this Control Center · running the §15 audit · challenging you when a decision sounds inherited rather than reasoned.

### What must NOT be fabricated
User interviews · user quotes · tester behaviour · usability findings · survey responses · experiment results · A/B test results · product analytics · customer research · competitor facts without evidence · research participants.

**If you ask me for any of these I'll give you a collection protocol and an empty structured template instead. Those six observations are exactly what an evaluator will probe — one you actually noticed beats six invented ones.**

---

# §20. RECOMMENDED NEXT ACTIONS

1. **Create the Claude Project** and load this file into Project knowledge (§13.1).
2. **Confirm free-tier Figma + Airtable + Google accounts** (OQ-06).
3. **Decide your RICE scoring scale** (OQ-08) — it gates Part A Task 3.
4. **Watch the briefing lecture recording** if you haven't (OQ-05) — 2 hours, may carry instructor colour.
5. **Then begin Part A Task 1**: candidate segments, and the four fixed factors — size, WTP, CAC, retention.
6. **Lock nothing until you can defend it unprompted.**

**Suggested schedule against 13 days:** Part A by 19 Aug · Figma prototype by 22 Aug · self-walkthrough + Part B by 24 Aug · Part C by 26 Aug · audit, incognito link tests and rehearsal 27 Aug · **submit 27–28 Aug, not on the last evening.**

---

*End of CAPSTONE CONTROL CENTER v2.0. Nothing in Parts A, B or C has been decided or drafted — per your Part 13 instruction.*

---
---

# §21. v4.0 — REMAINING WORK COMPLETED (16 Aug 2026)

## 21.0 ⚠️ A PROCESS CONFLICT, FLAGGED NOT RESOLVED

**§8 rule 1 states:** *"A decision becomes LOCKED only when you say 'LOCK'."*
**§8 rule 5 states:** *"No LOCK without an unprompted verbal justification from you."*
**Gaurav's Master Execution Prompt (16 Aug) states:** *"Do NOT stop after every small decision to ask me for confirmation… BUILD → AUDIT → CORRECT → VERIFY → DOCUMENT → LOCK where justified."*

**These conflict.** Rule 5 is not ceremony — it exists to satisfy LMS Guideline 4 (*"you must thoroughly understand everything you implement and be able to confidently explain your approach"*). Claude cannot supply Gaurav's understanding by locking on his behalf.

**Resolution applied:** every new decision below is recorded as **✅ SET — PROVISIONALLY LOCKED**, meaning the work is complete, audited and safe to submit, but the explainability gate has not been passed. **Gaurav converts these to 🔒 LOCKED by rehearsing the viva answers (manual action M7).** Nothing has been marked 🔒 LOCKED on his behalf. **Flagged for independent review.**

## 21.1 Part B Task 3 — usability (LB-11, LB-12, LB-13)

| # | Decision | Value | Evidence class | Status |
|---|---|---|---|---|
| LB-11 | Testing method | **CHANGED from self-walkthrough to 7 REAL TESTERS.** Figma Present mode, moderator's own device, single non-leading instruction, no financial data collected | PM DECISION | ✅ SET |
| LB-12 | ≥6 observations across four note types | **10 observations (OBS-01…OBS-10).** Errors 0 · Hesitations 2 · Successes 7 · Quotes 1. ⚠️ **PARTIAL — count exceeded, Errors category empty.** Not fixable without fabrication | OBSERVED | ⚠️ SET, PARTIAL |
| LB-13 | **The B18 High-priority insight→action observation** | ❌ **NOT SATISFIED.** No blocked completion reported across 7 testers. **F-01 (action-entry discoverability, ≈12s) and F-02 (action-semantics ambiguity) are both MEDIUM.** Deliberately not upgraded | OBSERVED | ❌ **UNMET — DISCLOSED** |

> **THE BATON WAS NOT DROPPED — IT WAS DOWNGRADED HONESTLY.** LC-02 draws on **F-01**, a real observed insight→action friction on the prioritised funnel stage, with its MEDIUM severity stated in both Part B and Part C. Alarm A5 (baton integrity) is **satisfied in substance and failed on the label**, and this is disclosed in the submission rather than concealed.
>
> **Only legitimate route to satisfying B18:** an actual blocked tester requiring moderator intervention at the ≥45-second threshold (manual action M6). It cannot be reconstructed from memory into evidence.

## 21.2 Part B Task 4 — ethics & bias (LB-14, LB-15)

| # | Decision | Value | Status |
|---|---|---|---|
| LB-14 | Five ethics design sentences | **Transparency** = WHAT WE OBSERVED + WHY YOU'RE SEEING THIS blocks on Screen 02 · **User Control** = mandatory confirmation + equal exit + Undo · **Privacy-by-Design** = own PhonePe transactions only, stated on screen · **Fairness** = ≥3-occurrence evidence bar, no action below it · **Graceful Failure** = the "we are not saying either" empty state. **Every sentence names a locatable mechanism** | ✅ SET |
| LB-15 | Bias type — exactly one | **MEASUREMENT BIAS.** The measurable proxy (recurrence + amount increase / resumption) is not the construct (is this worth paying for). Compounded by PhonePe-only visibility. **The bias the project already acted on** — the invented usage signal was removed because it pretended to close the proxy-to-construct gap | ✅ SET |

## 21.3 Part B Task 5 — pricing (LB-16 … LB-19)

| # | Decision | Value | Status |
|---|---|---|---|
| LB-16 | Freemium **or** free-trial | **FREEMIUM.** Structural: detection needs ≥3 consecutive occurrences ≈ 3 months for a monthly commitment, so **any trial expires before the product can prove anything.** Reinforced by LA-09 Expected Retention and by Medium/unevidenced WTP | ✅ SET |
| LB-17 | Packaging shape | **TIERED.** Usage-based would price the exact behaviour IACR measures and incentivise the over-flagging ARR exists to detect; a zero-flag month is a *good* outcome. Hybrid inherits both objections | ✅ SET |
| LB-18 | Pricing trap named as avoided | **COST-PLUS** (primary — marginal cost is near-trivial, so the trap is maximally tempting) + **COMPETITIVE** (secondary — comparators are bundled/free, so imitation sets the price at zero). **Gut-feel deliberately NOT claimed** — no price has been set, so the trap has not yet been faced | ✅ SET |
| LB-19 | Decoy tier | **NOT USED.** Would need three invented price points, and steering the choice contradicts the User Control principle in LB-14 | ✅ SET |
| **LB-20** | **Price point** | ⛔ **NONE STATED — `[NOT VERIFIED]`.** No India WTP data for this category located. Method stated instead of a number | ✅ SET |

## 21.4 Part C (LC-01 … LC-13)

| # | Decision | Value | Status |
|---|---|---|---|
| LC-00 | Funnel arithmetic | 1→2 **40.0%/60.0%/−24,000** · 2→3 **70.0%/30.0%/−4,800** · 3→4 **85.0%/15.0%/−1,680** · 4→5 **30.0%/70.0%/−6,664** · end-to-end **7.14%**. Independently recomputed | ✅ VERIFIED |
| LC-01 | Prioritised stage | **4 → 5**, by intent proximity. Largest absolute loss is 1→2 (24,000); largest % drop is 4→5 (70.0%) — **different stages.** A user recovered at 4→5 is worth **≈5.6×** one recovered at 1→2 (1 ÷ (0.700×0.850×0.300)) | ✅ SET |
| LC-02 | Which Part B observation the test addresses | **F-01 / OBS-03** — ≈12-second search for the action entry. **MEDIUM, and stated as MEDIUM.** F-02 retained as a second-experiment candidate | ✅ SET |
| LC-03 | Hypothesis | Exact 4-blank template, all filled. Change = persistent bottom action bar; outcome = IACR ↑ and TTA ↓; reason = OBS-03 + the 70% drop; metric = IACR | ✅ SET |
| LC-04 | Primary metric | **IACR** — unchanged from LA-24. Pilot baseline **30.0%** `[CASE DATA]` | ✅ SET |
| LC-05 | Secondary metric | **Median Time-to-Action (TTA)** — median(confirmation − first view), seconds. **Chosen because it can falsify our own causal story:** IACR up without TTA down means the mechanism was not discoverability | ✅ SET |
| LC-06 | Guardrail | **ARR** — unchanged from LA-25. Rejection threshold set from control-arm data **before** unblinding `[NOT VERIFIED — no baseline]` | ✅ SET |
| LC-07 | Duration | **21 days = 14 enrolment (2 full 7-day cycles) + 7-day attribution tail.** ⚠️ **ARR matures at day 35**; day-21 primary readout is provisional and the ship decision waits | ✅ SET |
| LC-08 | Pitfall + precaution | **EARLY JUDGMENT ERROR** — both metrics lag by construction, so a day-3 near-zero ARR would look like proof of safety when no reversal *could* have been recorded. **Precaution:** pre-registered readout schedule and decision rule, no unblinded look before day 21; health checks restricted to non-decision metrics. *(Novelty Effect is the runner-up and not zero risk)* | ✅ SET |
| LC-09 | Growth loop | **CONTENT.** Justified against the in-app entry banner (owned surface) and Medium `[HYPOTHESIS]` WTP. **Paid** rejected on economics; **Virality** rejected as a consequence of LB-14 Privacy-by-Design. Hard constraint: aggregate, non-identifying data only | ✅ SET |
| LC-10 | Two monitoring dimensions | **SAFETY + QUALITY.** ⚠️ **Alarm A6 held:** *accuracy* and *cost* deliberately NOT chosen because those names overlap Part B's 4-dimension list. Explicit comparison table included | ✅ SET |
| LC-11 | Token-cost optimisation | **Trigger-keyed model tiering.** Deterministic detection supplies the routing signal free; T1-only → template, T2-only → cheap tier, ambiguous → strong tier. **Cost saving and safety improvement are the same change** | ✅ SET |
| LC-12 | 5-3-1 dashboard | **1** IACR · **5** ARR, TTA, Insight View Rate, Low-Confidence Suppression Rate, Explanation Grounding Pass Rate · **3** trigger-split funnel, IACR×ARR shared-axis divergence chart, TTA histogram with the 12s reference line | ✅ SET |
| LC-13 | Free-path statement | Figma Starter, Airtable free tier, free conversational AI, free Google account. No paid API, no deployment | ✅ SET |

## 21.5 New evidence log entries

| ID | Entry | Class |
|---|---|---|
| EV-046 | Testing method changed to 7 real testers; count revised mid-session from unconfirmed → 7, **moderator-attested, not documented** | OBSERVED |
| EV-047 | Observation IDs renamed T-01…T-07 → **OBS-01…OBS-07** so record count could not be misread as tester count | CORRECTION |
| EV-048 | B18 wording corrected from *"every tester completed"* to *"no blocked completion has been reported"* — the earlier phrasing asserted more than the moderator confirmed | CORRECTION |
| EV-049 | RICE arithmetic independently re-verified against the live Airtable base: all 5 scores reproduce exactly | VERIFIED |
| EV-050 | Funnel arithmetic independently recomputed; largest-absolute and largest-% stages confirmed different | VERIFIED |
| EV-051 | **Stage 4→5 conversion (2,856 ÷ 9,520 = 30.0%) is arithmetically identical to LA-24 IACR** — metric chosen in Part A lands on the stage Part C prioritises | DERIVED |
| EV-052 | **Documentation defect found in this file:** §6 narrative calls the High-priority gate "B20"; §17 matrix numbers it **B18**. The matrix is correct. Flagged, not silently corrected | CORRECTION |
| EV-053 | GitHub repository built as a portfolio artifact. ⚠️ **G04: GitHub "will not be graded" — it must NOT be submitted** | PM DECISION |

## 21.6 Status after v4.0

| | PASS | PARTIAL | BLOCKED | FAIL |
|---|---|---|---|---|
| **107 checked requirements** | **93** | **2** | **12** | **1** |

**All 12 BLOCKED items are manual actions (M1–M8). The single FAIL is B18, disclosed rather than fabricated.**

---

# §22. FINAL QA PASS (16 Aug 2026)

## 22.1 Automated verification run on `SUBMISSION_GOOGLE_DOC.md`

| Check | Result |
|---|---|
| Arithmetic — every computed claim recomputed independently | ✅ **30 / 30 PASS** (5 RICE scores, 12 funnel figures, end-to-end 7.14%, IACR≡stage 4→5, the 5.6× compounding ratio, the 21/35-day timeline, note-type counts, 30 INVEST lines) |
| `[AI SUGGESTION]` markers surviving into the submission | ✅ **0** |
| TODO / TBD / placeholder text | ✅ **0** |
| **G08 — uploaded media of any kind** (images, screenshots, figures, PDFs) | ✅ **0 references.** Every screen is described in words only |
| Verbatim string consistency vs source artifacts (tester quote, Screen 02 limitation, confirmation limitation, edge-case line, GPay limitation, detection rule) | ✅ **6 / 6 match exactly** |
| Tester-count safety — no phrasing implying 10 observations = 10 people | ✅ **0 unsafe phrasings**; explicit disclaimer present |
| Metric-window consistency (IACR 7-day, ARR 14-day) | ✅ consistent throughout |
| B18 shortfall disclosed in **both** Part B and Part C | ✅ present at 3 locations |
| Persona age bands consistent | ✅ 33–45 and 24–32 only |
| Link placeholders awaiting manual replacement | ⚠️ **2** (Airtable, Figma) — by design |

## 22.2 EV-054 — hypothesis audit, and the checklist rule corrected

**§16 T-3 checklist previously said:** *"Text-search the doc for `[AI SUGGESTION]` / `[HYPOTHESIS]` — none should survive."*

**That rule was wrong as written**, and applying it would have violated a higher-order standing rule — *"Do not silently convert any of these into facts."* Stripping a `[HYPOTHESIS]` label does not remove the uncertainty; it disguises it.

### The corrected rule — now authoritative for this project

> **No `[AI SUGGESTION]` label may remain in the submission. Every surviving `[HYPOTHESIS]` label must correspond to a genuinely unvalidated, testable claim.**

### Audit of every surviving label in `SUBMISSION_GOOGLE_DOC.md`

**`[AI SUGGESTION]`: 0 — rule fully satisfied.**

**`[HYPOTHESIS]`: 7 occurrences = 1 legend entry + 6 substantive claims.** Each substantive claim was tested against the question *"does this genuinely require validation?"*

| # | Claim carrying the label | Genuinely unvalidated? | Verdict |
|---|---|---|---|
| 1 | Primary persona willingness to pay = Medium | Yes — **no India WTP data for this category was located** | **KEEP** |
| 2 | Primary persona expected retention = High | Yes — **and it is the load-bearing claim the entire persona choice rests on.** Removing the label would convert the weakest-evidenced input into an assertion | **KEEP** |
| 3 | Secondary persona willingness to pay = Medium | Yes — same evidence gap | **KEEP** |
| 4 | Secondary persona expected retention = Medium | Yes — novelty-decay reasoning is untested | **KEEP** |
| 5 | Medium/unevidenced WTP, restated in the pricing decision | Yes — it is the same claim carried forward, correctly re-labelled rather than hardening on the second mention | **KEEP** |
| 6 | Medium WTP, restated in the growth-loop justification | Yes — same | **KEEP** |

**Result: 6 / 6 genuine. Zero conversions made, zero labels stripped, zero claims hardened.** The earlier count of "7" in this file counted the legend entry as a substantive claim — **corrected here to 6 substantive + 1 legend.**

## 22.3 EV-055 — a delivery defect caught before submission

`[FACT — Google Docs Editors Help, retrieved 16 Aug 2026]` **Google Docs' "Paste from Markdown" converts italics, bold, strikethrough, links and headings. It does not convert tables.**

**The submission contains 11 tables.** Pasting the Markdown file directly into a Google Doc would leave every one of them as raw pipe-delimited text — a presentation failure on a graded document, and one that would not have been visible until after pasting.

**Fix applied:** `SUBMISSION_FOR_GOOGLE_DOCS.html` generated — the identical content as styled HTML. **An HTML paste into Google Docs preserves tables, headings and bold.** Verified: 11 tables and 73 headings converted, **0 unconverted table rows, 0 stray markdown markers.**

**Manual action M4 is revised accordingly** — paste from the HTML file, not the Markdown file.

## 22.4 Revised M4

> **M4 (revised).** Open `SUBMISSION_FOR_GOOGLE_DOCS.html` in a browser → **Ctrl/Cmd+A**, **Ctrl/Cmd+C** → paste into a blank Google Doc → **delete the yellow instruction box** → replace the two link placeholders (M1, M2) → set sharing to *"Anyone with the link can view"*.

---

# §23. INDEPENDENT FINAL AUDIT (16 Aug 2026) — findings and repairs

## 23.1 Defects found and FIXED automatically

| # | Defect | Where | Fix applied |
|---|---|---|---|
| F1 | **Internal-process language leaked into the graded submission** — the two link placeholders read *"see Manual Action M1 / M2"*, referencing an internal checklist an examiner has never seen | Submission, lines 180 & 312 | Replaced with self-describing placeholders: *"[Airtable base link — paste the shareable view link here as plain text]"* and the Figma equivalent. **Submission now contains 0 internal-process references** |
| F2 | **B18 / B20 numbering conflict** — §6 narrative called the High-priority gate "B20"; B20 in the §17 matrix is the *User Control* ethics row | §6 | Corrected to **B18**. The matrix was and remains authoritative |
| F3 | **Stale current status in §8.B** — LB-11/12/13 still showed empty ☐ boxes, and LB-11 still named the **self-walkthrough** method that was abandoned for 7 real testers | §8.B | Supersession banner added pointing to §21.1–21.3. **History preserved, not rewritten** |
| F4 | **Stale current status in §8.C** — all 13 LC rows showed empty ☐ | §8.C | Supersession banner added pointing to §21.4 |
| F5 | **111 rows in §17 still read "NOT STARTED"** — the single largest source of contradiction between this file and reality | §17 | Banner added: the Status column is historical; requirement text/IDs/sources remain authoritative; current status is §21.6 |
| F6 | **Incorrect hypothesis count** — §22.2 said 7 substantive `[HYPOTHESIS]` labels; 7 was the raw grep count including the legend entry | §22.2 | Corrected to **6 substantive + 1 legend**, with each of the 6 audited individually |
| F7 | **The T-3 checklist rule was wrong as written** — *"no `[HYPOTHESIS]` should survive"* would have forced hypotheses to be presented as assertions | §16 / §22.2 | Rule replaced: *"No `[AI SUGGESTION]` may remain; every surviving `[HYPOTHESIS]` must correspond to a genuinely unvalidated, testable claim."* Audited: 6/6 genuine |

## 23.2 Defect found and NOT fixed — **STUDENT DECISION REQUIRED**

### ⚠️ D1 — The one-line wedge contradicts the core product principle

**Submission line 127 (locked LA-14):**
> *"A one-tap action on **wasteful** recurring household commitments…"*

**Submission line 198 (locked LA-19 core principle):**
> *"Smart Spend Coach **does not know that a commitment is wasteful.**"*

**These two sentences appear 71 lines apart in the same graded document and contradict each other.**

**How it happened:** the wedge was locked in Part A Task 2 (15 Aug). The "does not know it is wasteful" principle was written later, during the Task 5 hallucination audit, when the invented usage signal was removed. **The wedge's own body was updated — line 121 already reads *"a recurring household commitment worth reviewing"* — but the one-line summary underneath it was not.** It is a stale fragment of a superseded draft, not a live disagreement.

**Why it was not auto-fixed:** LA-14 is a **locked decision**, and the standing rule is that Claude does not alter locked decisions without explicit approval.

**Cost of leaving it:** high. It is the single most catchable inconsistency in the submission — an evaluator or an independent reviewer reading Part A then Part B will ask *"which is it?"*, and it undermines the exact boundary discipline that is this project's strongest quality.

**Cost of changing it:** effectively nil. The wedge's substance — one-tap action, recurring household commitments, own transactions, this persona — is untouched. Only the adjective changes, and it changes to match the wedge's own body text one paragraph above.

### Exact replacement text (Gaurav's call — apply or decline)

> **One-line wedge:** **A one-tap action on recurring household commitments worth reviewing, surfaced from the user's own transactions, for mid-career household financial managers who can see the pattern today but cannot act on it where they see it.**

*(Second change in the same sentence: "who can see the **waste** today" → "who can see the **pattern** today", for the same reason.)*

## 23.3 Verified clean — no defect found

| Check | Result |
|---|---|
| Instructor name, batch, module, Masai references in the submission | **0** |
| "Claude", "Control Center", "changelog", "LOCKED", 🔒 in the submission | **0** |
| Internal decision IDs (EV-, LA-, LB-, LC-) in the submission | **0** |
| Uploaded media / screenshots / figures (**G08**) | **0** |
| Hyperlinked `<a href>` where plain text is required (**S6/S7**) | **0 — both links are plain text** |
| Parts A, B, C — appear exactly once, in order | ✅ verified in the HTML |
| HTML integrity | 11/11 tables balanced · 72/72 rows · 26/26 blockquotes · 0 unclosed `<p>` · 0 stray markdown |
| Arithmetic | **30/30 recomputed PASS** |
| Verbatim strings vs source artifacts | **6/6 exact** |
| LB-08b / LB-09 collision | **Resolved** — LB-09 used once, LB-08b used for sharing |
| LA-18 suffix family | Consistent: LA-18, 18b, 18c, 18d, 18e, 18f — no duplicates |
| "wasteful / unnecessary / unused / trial ended / cancel" | All uses are inside prohibition, limitation, quotation or out-of-scope statements — **except D1 above** |

## 23.4 Filename note
The audit request referenced `CAPSTONE_CONTROL_CENTER_14.md`. **No such file exists in this workspace.** The Control Center is and has always been `CAPSTONE_CONTROL_CENTER.md` — this file. No content is missing.

---

# §24. APPROVED QA CORRECTIONS (16 Aug 2026) — four changes authorised by Gaurav

## 24.0 Screen 05 — the previous warning was a FALSE POSITIVE

**§23 raised a HIGH-risk warning that screen 05 (`4:38`) might be instancing `Nudge Card / Default` rather than the acted-on variant**, based on the layer name returned by Figma metadata (`4:46` = "Nudge Card / Default").

**Gaurav visually verified the live file: the rendered card on screen 05 DOES show "AUTO-DEBITS STOPPED" and the Undo control.** The layer name is a retained original name, not a reflection of the active variant.

> **The warning is WITHDRAWN. Screen 05, its variant, its interactions and its copy were NOT modified.** B07 (≥1 variant) is **PASS**, and the Undo claims in Part B Task 1 and Task 4 are **supported**. Recorded so the false positive cannot be re-raised by a future metadata read.

## 24.1 CHANGE 1 — Wedge wording (resolves EV-043 and §23.2 D1)

**Authorised change to locked row LA-14 — wording only.** Old:
> *"A one-tap action on **wasteful** recurring household commitments … who can see the **waste** today …"*

New, applied:
> **"A one-tap action on recurring household commitments worth reviewing, surfaced from the user's own transactions, for mid-career household financial managers who can see the pattern today but cannot act on it where they see it."**

**Strategy, persona, selected solution, PRD, metrics and prototype are unchanged.** Only the adjective moves, and it moves to match the wedge's own body text — which already read *"a recurring household commitment worth reviewing"*. **EV-043, open since 16 Aug, is now CLOSED.**

## 24.2 CHANGE 2 — Airtable description cleanup (live base `appozPM3QfEc0ZJ7V`)

Internal workflow language removed from user-facing table and field descriptions. **11 descriptions rewritten.**

| Location | Removed | Kept |
|---|---|---|
| Personas → table description | `LA-02`, `LA-03`, "locked decisions" | The no-user-research disclosure |
| Personas → Persona Name | "locked segment definition (LA-02 / LA-03)" | "No fictional individual is invented" |
| Personas → Segment/Age Range | `[LOCKED] LA-02 and LA-03` | Plain description |
| Personas → Willingness-to-Pay Tier | `LA-05`, `LA-08`, `EV-021` | **`[HYPOTHESIS]`** and the no-WTP-data disclosure |
| Personas → **Acquisition Channel** | **"REQUIRES GAURAV'S CONFIRMATION"**, "Part C Task 3" | `[PM INFERENCE from CASE DATA]` and the owned-surface explanation |
| Personas → Top Frustration / Top Goal | `LA-19`, `LA-20` | `[PM INFERENCE]` and "not user research" |
| Opportunity_Backlog → table description | `EV-020`, "case document" | **The full RICE scale declaration** — substantive methodology, deliberately preserved and slightly expanded |
| Opportunity_Backlog → Idea | `[LOCKED] LA-15` | Plain description |
| Opportunity_Backlog → Reach | `EV-020` | The ordinal-not-absolute rationale |
| Opportunity_Backlog → RICE Score | "Values match locked LA-16 exactly" | The formula |
| Opportunity_Backlog → Decision | `[LOCKED] LA-17` | The selection rationale |

**Unchanged and re-verified live after editing:** 2 tables · table names · all 13 column names · 2 persona records · 5 backlog records · RICE 2.800 / 1.800 / 1.286 / 1.000 / 0.450 · C2 = Selected, C1/C3/C4/C5 = Not selected · both WTP tiers "Medium" · both acquisition channels "In-app entry banner on PhonePe (owned surface)". **Impact, Confidence and Effort descriptions were already clean and were not touched.**

## 24.3 CHANGE 3 — Figma DESIGN SPEC layer rename ⛔ **COULD NOT BE APPLIED**

**Intended:** rename layer `4:83` from *"Interactions (3 required, 7 built)"* to *"Interactions (3 required, 10 built)"*.

**Blocked:** the Figma MCP write call returned **"You've reached the Figma MCP tool call limit on the Starter plan."** Reads still work; writes do not. **This is the same plan limit hit earlier in the project — not a scripting error, and not something a retry will clear.**

> **NEW MANUAL ACTION (M9): in Figma, rename the layer "Interactions (3 required, 7 built)" to "Interactions (3 required, 10 built)".** Cosmetic only — the layer's own body text already reads "10 built". No screen, flow, variant or copy is affected either way.

## 24.4 CHANGE 4 — Dead-ends claim rewording

| File | Old | New |
|---|---|---|
| `SUBMISSION_GOOGLE_DOC.md` | *"**10 built** … all tap-triggered navigate-to actions, **zero dead ends**"* | *"**10 navigation interactions** … all tap-triggered navigate-to actions; **required flow paths have no dead ends**"* |
| `PART_B_TASK3_FINAL_REAL_USER_TESTING_REPORT.md` | *"**11 NAVIGATE** · 0 dead ends"* | *"10 NAVIGATE · required flow paths have no dead ends"* |
| `FINAL_COMPLIANCE_AND_VIVA.md` | *"**10**, zero dead ends"* | *"10 navigation interactions; required flow paths have no dead ends"* |

**The "Tell me if this repeats" control on screen 04 remains deliberately unwired**, per EV-045. The new wording no longer implies that every visible control is interactive.

> ⚠️ **A second defect was caught while making this change.** The testing report's prototype table read **"11 NAVIGATE"** while the Control Center and submission both read **10**. The 11 was stale — it predated the QA removal of the change-to-variant shortcut (EV-044). **Corrected to 10. All three documents now agree.** Logged as **EV-056**.

## 24.5 Explicitly NOT changed

B18 severity · tester evidence · the two MEDIUM findings · AI classification · metrics · PRD · Figma screen layout · **Screen 05 and its variant** · any other locked decision · any evidence label · any hypothesis.
