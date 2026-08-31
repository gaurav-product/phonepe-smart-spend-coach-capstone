# FINAL COMPLIANCE MATRIX · RELAY AUDIT · VIVA PREPARATION
## PhonePe Smart Spend Coach Capstone · compiled 16 Aug 2026

---

# PART 1 — MASTER RELAY-CHAIN AUDIT

Every arrow in the dependency chain was checked for contradiction. **Findings, not reassurance.**

| # | Link in the chain | Consistent? | Check performed |
|---|---|---|---|
| 1 | Persona → Segmentation factor | ✅ | Expected Retention is the factor the primary persona wins on; the persona is chosen *because* the need is permanent. Not circular — the four-factor table shows the other three tie or favour the secondary |
| 2 | Segmentation factor → Problem | ✅ | The problem statement is about commitments that *recur*, which is what makes retention the right factor |
| 3 | Problem → Competitive analysis | ✅ | The teardown's decisive row (F9, one-tap action attached to the insight) is the same gap the problem statement names |
| 4 | Competitive analysis → Opportunity set | ✅ | All five candidates address the identified gap at different scopes; C5 is included specifically to be scored and rejected transparently |
| 5 | RICE arithmetic | ✅ | **Independently recomputed against the live Airtable base.** All five scores reproduce exactly: C2 2.800 · C1 1.800 · C3 1.286 · C4 1.000 · C5 0.450. Scales were declared before scoring |
| 6 | RICE → Selected feature | ✅ | C2 is the highest score and is explicitly named as the one feature the project is about |
| 7 | Selected feature → PRD | ✅ | PRD implements C2 only. No scope creep into C3 (bulk action) or C5 (household view) |
| 8 | PRD → User stories | ✅ | US1–US5 map to detection, evidence, action, confirmation, edge case. **US3's partial dependency is declared rather than glossed** |
| 9 | PRD → Metrics | ✅ | IACR measures the insight→action gap the problem statement describes; ARR guards the harm the solution can cause |
| 10 | PRD → Prototype | ✅ | 5 screens implement the PRD flow. **One deliberate mismatch is documented:** essential-category degradation is specified in the PRD but not depicted, since the prototype uses a discretionary example. Labelled, not hidden |
| 11 | Prototype → AI classification | ✅ | AI-augmented follows from deterministic detection, which is itself the result of removing the invented usage signal. **Traceable** |
| 12 | AI classification → Usability findings | ✅ | No usability finding depends on an AI capability the classification denies |
| 13 | Usability findings → Ethics | ✅ | F-02 (cancellation ambiguity) and the Transparency/User-Control choices concern the same boundary. No contradiction |
| 14 | Ethics → Pricing | ✅ | The no-decoy decision is justified *by* the User Control principle. The reasoning propagates rather than repeating |
| 15 | Pricing → Part C growth loop | ✅ | Freemium (value before payment) and Content (convince before arrival) rest on the same Medium-WTP reasoning |
| 16 | Usability findings → Part C experiment | ⚠️ **CONSISTENT, WITH A DISCLOSED GAP** | The experiment targets F-01, a real observed finding on the prioritised stage. **But B18 requires a HIGH finding and none exists.** The gap is disclosed in Part B Task 3 *and* in Part C Task 3, not papered over |
| 17 | Funnel → Prioritisation | ✅ | Arithmetic independently verified. Largest absolute (1→2, 24,000) and largest percentage (4→5, 70.0%) are genuinely different stages |
| 18 | Prioritisation → Experiment | ✅ | The experiment targets Stage 4→5, the prioritised stage |
| 19 | Metrics: Part A → Part C | ✅ | IACR and ARR are carried **unchanged**, same formulas, same windows. **Stage 4→5 conversion (30.0%) *is* IACR** — the strongest single piece of relay evidence in the project |
| 20 | Part B AI risk → Part C AI monitoring | ✅ **TRAP AVOIDED** | Part B = hallucination rate (4-dimension risk). Part C = Safety + Quality (5-dimension monitoring). **The two overlapping names, *accuracy* and *cost*, were deliberately not selected** so the answer cannot read as a restatement. A comparison table states the distinction explicitly |
| 21 | Growth loop → Ethics | ✅ | Virality is rejected *because* of the Privacy-by-Design commitment. The content loop carries an explicit aggregate-only constraint |
| 22 | Scope boundary, end to end | ✅ | No document claims usage data, email access, merchant-side data, trial status, or another household member's transactions |

### Contradictions actively searched for and NOT found
Persona drift · feature substitution · metric redefinition · RICE values changing between documents · prototype depicting something absent from the PRD · Part C targeting a problem with no usability support · the two AI frameworks being conflated · a locked decision silently altered.

### The one live inconsistency found — in my own tracking, not in the work

**The Control Center's §6 narrative calls the High-priority insight→action gate "B20"; the requirements matrix in §17 numbers it "B18".** The matrix is the precise record and B18 is correct. **This is a documentation defect in my tracking file, not a requirement conflict, and it does not affect any deliverable.** Flagged rather than silently corrected.

---

# PART 2 — REQUIREMENT COVERAGE MATRIX

**Status key:** **PASS** = acceptance criterion actually verified · **PARTIAL** = substantially met with a stated shortfall · **BLOCKED** = requires an action only Gaurav can perform · **FAIL** = criterion not met

> **Nothing is marked PASS merely because a document exists.** Each row was checked against the acceptance criterion, not against the presence of a heading.

## Global / submission

| Req | Requirement | Where | Status | Risk |
|---|---|---|---|---|
| G01 | One Google Doc link only | `SUBMISSION_GOOGLE_DOC.md` ready to paste | **BLOCKED — M4** | Doc not yet created in Google Docs |
| G02 | Sharing = anyone with link can view | — | **BLOCKED — M4** | Zero marks if wrong |
| G03 | Parts A, B, C in order, same document | Submission doc | **PASS** | — |
| G04 | No other link will be graded | GitHub repo explicitly marked non-submittable | **PASS** | Do not submit the repo |
| G05 | No separate submission per part | — | **PASS** | — |
| G06 | Airtable link, plain text, inside Part A | Placeholder in position | **BLOCKED — M1** | — |
| G07 | Figma link, plain text, inside Part B | Placeholder in position | **BLOCKED — M2** | — |
| G08 | No uploaded media of any kind | Submission doc is text-only; every screen described in words | **PASS** | — |
| G09 | No screenshots of Airtable/Figma | None anywhere | **PASS** | — |
| G14/G19 | Originality — own work product | All artifacts authored for this brief | **PASS** | — |
| G16 | Links in respective answer boxes | — | **BLOCKED — M5** | — |
| G17 | Submit before 28 Aug 2026, 11:59 PM IST | — | **BLOCKED — M5** | **Hard deadline** |
| G18 | All links accessible and working | — | **BLOCKED — M3** | Must be tested logged-out |
| G20 | Able to explain every decision at evaluation | Viva section, Part 3 below | **PARTIAL** | Rehearsal is Gaurav's |
| G22 | Part B uses only Part A persona + PRD | Relay row 7, 10 | **PASS** | — |
| G23 | Part C targets only Part B usability findings | Relay row 16 | **PASS** | Targets F-01, disclosed as MEDIUM |

## Part A — 30 marks

| Req | Requirement | Status | Note |
|---|---|---|---|
| A01 | Two personas | **PASS** | |
| A02 | Name the AI-assisted approach in one line | **PASS** | Guided AI Q&A |
| A03–A06 | Persona 1: all four factors | **PASS** | Size stated as a reasoned estimate with the unverifiable step named — exactly what the brief asks for |
| A07 | Persona 2: all four factors | **PASS** | |
| A08 | Use the four factors to explain the primary choice, in writing | **PASS** | Four-factor comparison table + narrative |
| A09 | One-line justification of the primary factor | **PASS** | Expected Retention |
| A10 | ≥1 direct competitor | **PASS** | 3 named |
| A11 | ≥1 indirect competitor | **PASS** | 2 named |
| A12 | Feature table, ≥6 features | **PASS** | **10 features** |
| A13 | ≥3 of 4 classification categories | **PASS** | **All 4 used** |
| A14 | Wedge in three-part form | **PASS** | Capability + unmet need + segment |
| A15 | ≥4 candidate versions | **PASS** | **5** |
| A16 | RICE on each | **PASS** | |
| A17 | Show the arithmetic | **PASS** | Every candidate, full expression, scales declared first |
| A18 | Name the selected feature explicitly | **PASS** | C2 |
| A19 | HIPPO / vanity-metric paragraph | **PASS** | Both named (C3 = HIPPO, C1 = vanity) and rejected |
| A20/A21 | Airtable Personas table, 6 columns, both personas | **PASS** | Verified live |
| A22/A23 | Opportunity_Backlog, 7 columns, all ideas, Decision set | **PASS** | Verified live, 5 records |
| A24 | Base sharing set + link pasted | **BLOCKED — M1** | |
| A25 | Problem statement citing persona frustration | **PASS** | |
| A26 | Solution + one rejected alternative and why | **PASS** | C1 rejected on Impact 0.5 vs 2.0 |
| A27 | 3–5 user stories | **PASS** | 5 |
| A28 | Every INVEST letter, one line each | **PASS** | 6 letters × 5 stories = 30 lines |
| A29 | Primary + guardrail as precise formulas | **PASS** | IACR, ARR |
| A30 | Two concrete edge cases + behaviour | **PASS** | |
| A31 | One explicit out-of-scope line | **PASS** | |

## Part B — 35 marks

| Req | Requirement | Status | Note |
|---|---|---|---|
| B01 | Clickable prototype of the selected feature | **PASS** | |
| B02–B05 | Four named screens | **PASS** | **5 built**; edge case matches PRD Edge Case 1 |
| B06/B07 | ≥1 component, ≥1 variant | **PASS** | Nudge Card, 2 states |
| B08 | ≥3 interactions | **PASS** | **10** navigation interactions; required flow paths have no dead ends |
| B09/B10 | Sharing set + link pasted in Part B | **BLOCKED — M2** | |
| B11/B12 | AI-augmented or AI-native + justification | **PASS** | AI-augmented, tied to what stops functioning |
| B13 | Exactly one of four dimensions as biggest risk + why | **PASS** | Hallucination rate; others not ranked |
| B14 | 5 real testers **or** rigorous self-walkthrough | **PASS** | **7 real testers** — exceeds |
| B15 | Four-part note format | **PASS** | All four categories used as the recording format |
| B16 | ≥6 observations across all four note types | ⚠️ **PARTIAL** | **10 observations recorded — count exceeded.** But **Errors = 0**, so one of the four categories is empty. **Not fixable without fabrication.** See risk R1 |
| B17 | Priority High/Medium/Low per the severity guide | **PASS** | F-01 MEDIUM, F-02 MEDIUM, applied strictly |
| **B18** | **≥1 HIGH-priority observation of insight→action friction** | ❌ **FAIL — DISCLOSED** | **No blocked completion was reported across 7 testers, so no observation qualifies as High.** Deliberately not manufactured. See risk R2 |
| B19–B23 | Five ethics principles, each naming a concrete design choice | **PASS** | Each names a specific mechanism on a specific screen; no "we will be transparent" phrasing |
| B24 | Exactly one bias type + paragraph | **PASS** | Measurement bias; other three discussed only to justify the choice |
| B25 | Freemium or free-trial | **PASS** | Freemium |
| B26 | Packaging shape | **PASS** | Tiered |
| B27 | Justified vs persona WTP | **PASS** | |
| B28 | ≥1 pricing trap named as avoided | **PASS** | Cost-plus (primary) + competitive |
| B29 | Decoy tier — conditional | **PASS (N/A)** | Not used, with stated reason |

## Part C — 35 marks

| Req | Requirement | Status | Note |
|---|---|---|---|
| C01 | Use the supplied funnel | **PASS** | Exact figures, incl. 11,200 |
| C02–C05 | Four transitions, % converted **and** % dropped | **PASS** | Both figures, arithmetic shown |
| C06 | Arithmetically correct | **PASS** | Independently recomputed |
| C07 | Largest absolute loss | **PASS** | 1→2, 24,000 |
| C08 | Largest percentage drop | **PASS** | 4→5, 70.0% |
| C09 | Shown to be different stages | **PASS** | Plus an explanation of *why* the measures diverge |
| C10 | Intent-proximity invoked explicitly | **PASS** | Named and applied |
| C11 | Why the other is lower priority despite more raw users | **PASS** | Five reasons, incl. the quantified 5.6× argument |
| C12 | One A/B test on the prioritised stage | **PASS** | |
| C13 | Names the specific Part B observation | **PASS** | F-01 / OBS-03, with the B18 shortfall disclosed in place |
| C14 | Exact hypothesis template, four blanks | **PASS** | Verbatim template |
| C15–C17 | Primary, secondary, guardrail as formulas | **PASS** | IACR, TTA, ARR |
| C18 | Duration ≥1 full 7-day cycle, reasoned | **PASS** | 21 days = 2 cycles + attribution tail; guardrail maturity at day 35 flagged |
| C19 | One named pitfall | **PASS** | Early Judgment Error |
| C20 | One concrete precaution | **PASS** | Pre-registered readout, no early unblinded look |
| C21 | Growth loop selected | **PASS** | Content |
| C22 | Justified vs acquisition channel | **PASS** | In-app entry banner, owned surface |
| C23 | …and willingness to pay | **PASS** | Medium `[HYPOTHESIS]` |
| C24 | 2 of 5 monitoring dimensions + why | **PASS** | Safety + Quality |
| C25 | **Not** Part B's list restated | **PASS** | Comparison table; overlapping names deliberately avoided |
| C26 | One token-cost optimisation, feature-specific | **PASS** | Trigger-keyed model tiering |
| C27–C29 | 1 core metric · 5 KPIs · 3 visualisations, all specific | **PASS** | Each visualisation states its diagnostic purpose; no generic placeholder |
| C30 | 3–5 lines free-path statement | **PASS** | |

## Tally

| | PASS | PARTIAL | BLOCKED | FAIL |
|---|---|---|---|---|
| Global (17 tracked) | 7 | 1 | 9 | 0 |
| Part A (31) | 30 | 0 | 1 | 0 |
| Part B (29) | 26 | 1 | 2 | **1** |
| Part C (30) | 30 | 0 | 0 | 0 |
| **Total (107 checked)** | **93** | **2** | **12** | **1** |

**Every BLOCKED item is a manual action, not missing work.** All 12 are listed in Part 4 and can be cleared in well under an hour.

---

# PART 3 — CRITICAL RISKS

Only real risks. Ranked by expected mark loss.

### R1 · B18 is not satisfied — the single largest scoring risk
**What it is:** the brief calls this *"the single most decision-relevant type of friction for a nudge-based feature, and Part C depends on it."* We have two MEDIUM findings and no HIGH.
**Exposure:** one acceptance criterion in Part B, plus a possible knock-on to how C13 is read.
**Why it was not fixed:** upgrading a MEDIUM to HIGH would require asserting that testers were blocked from completing the task. **No tester was.** That assertion would be a fabricated usability finding feeding a fabricated experiment premise.
**What mitigates it:** the shortfall is disclosed in **both** Part B Task 3 and Part C Task 3, with the reasoning shown. Part C still targets a real observed insight→action friction on the prioritised stage. **An examiner sees a candidate who understood the requirement, met the harder underlying goal, and refused to fake the label.**
**Still open to Gaurav:** if any of the 7 sessions involved a tester who could not proceed and required moderator intervention at the protocol's ≥45-second threshold, **that is a genuine HIGH and B18 becomes satisfiable honestly.** This is the only legitimate route. It cannot be reconstructed from memory into evidence — but if it happened, it should be recorded.

### R2 · Errors = 0 leaves one of the four note-type categories empty
**Exposure:** B16 reads *"≥6 observations across all four note types."* Ten observations were recorded — the count is exceeded — but Errors is empty.
**Why not fixed:** no wrong tap, wrong path, backtrack or task failure was reported. Recording one would be fabrication.
**Mitigation:** the submission states plainly *"Errors are not represented in the supplied sessions"* and explains why a 12-second search and a clarifying question are hesitations rather than errors — which demonstrates the candidate understands the taxonomy, rather than appearing to have missed it.

### R3 · Both live links are still private — a zero-mark risk on two requirements
Figma and Airtable sharing are unset. **The brief warns that incorrect or incomplete submissions may lead to disqualification or zero marks.** Fully fixable in minutes (M1, M2), but **must be verified logged-out**, not just toggled.

### R4 · The one-tap platform capability is unverified
Carried as a stated design assumption with a documented fallback. **This is a strength if asked about and a weakness only if an examiner reads it as an unnoticed hole** — the viva answer in Part 4 addresses it directly.

### R5 · Tester count rests on recollection, not a record
The count of 7 is attested by Gaurav; no session log, notes file or recording has been produced, and session dates were not retained. **Low risk for grading, real risk if probed in the viva.** Answer prepared below.

### NOT risks — checked and dismissed
Part A quality · RICE arithmetic · funnel arithmetic · the two AI frameworks being conflated · persona or feature drift · media in the submission · originality.

---

# PART 4 — VIVA PREPARATION

**Why this persona?**
> Because Smart Spend Coach only creates value through repeated cycles of insight and action, and this segment's need is structural rather than life-stage-bound — household budgeting has no natural end point, and the commitment base regenerates as family members add services. I'll be honest that the *secondary* persona actually has the better product fit: denser addressable waste, faster demonstrable saving. I chose the household manager on economics, not on fit, and I'm accepting a narrower share of wallet in exchange for a more durable need.

**Why Expected Retention as the primary factor?**
> Two reasons. Substantively, a feature that depends on repeat cycles cannot be built on a segment that produces one burst of value and goes quiet. Practically, retention was the only factor that separated my two finalists — they tie on WTP, and CAC and size split marginally in opposite directions. A factor that ties can't be the deciding factor.

**Why not willingness to pay, the commercially obvious choice?**
> Because it doesn't discriminate here — both personas came out Medium — and it's the factor I have the least evidence for; I could not locate any credible source on Indian consumer willingness to pay for a personal-finance product. It still matters, and it drove the pricing decision in Part B. It just wasn't the thing that decided this.

**Why C2, and why not C1, C3, C4 or C5?**
> C2 scores 2.800, a 56% margin over the runner-up. C1 (1.800) is insight-only — it delivers the half of the job that already works, and the most advanced competitor in this market proves insight without action is the default rather than the differentiator. C3 (1.286) is the impressive-demo temptation: highest impact ceiling, but only 50% confidence because nothing suggests household managers will sit down and audit commitments, and nearly double the effort. C4 (1.000) bets on pre-debit timing, which is unproven and carries the highest annoyance risk. C5 (0.450) is out of scope — it needs other household members' transaction data, and the brief specifies the user's own. I scored it anyway so the rejection is on the record rather than quietly dropped.

**Why RICE, and how were the values calculated?**
> RICE because I was comparing candidates that differ on all four axes — some are broad and shallow, some narrow and deep — and RICE forces confidence to be priced in rather than assumed. I declared my scales before scoring: Reach 1–10 ordinal, Impact on the standard 3/2/1/0.5/0.25 ladder, Confidence 100/80/50%, Effort 1–10 relative person-months. C2 is (7 × 2 × 0.8) ÷ 4 = 11.2 ÷ 4 = 2.800. One deliberate choice: **Reach is ordinal, not absolute users** — PhonePe publishes no MAU or category-mix data, so an absolute figure would have been fabricated precision.

**Why AI-augmented rather than AI-native?**
> Because the test is how much stops functioning without the AI layer, and here the answer is the polish, not the function. Detection is arithmetic: same merchant, regular interval, three occurrences, plus an amount increase or a resumption. Strip the model out and the feature still detects the commitment, still shows the evidence, still offers the action — you lose merchant name recognition, category classification and personalised copy. Worth adding: an earlier draft of my PRD had detection depending on a usage signal, which would have made this look far more AI-native. **PhonePe has no such capability — I'd invented it, and I removed it. The classification follows from that correction.**

**Why is hallucination the biggest AI risk?**
> Because the AI layer's only real job in this feature is explanation. Detection is deterministic, so the arithmetic deciding *whether* to flag can't hallucinate — what the model produces is the sentence telling you *why*. If that sentence claims the service is unused or the commitment is unnecessary, it breaks the product's core principle. And critically, my design safeguard doesn't help: the charge history lets you verify a *pattern*, but a fabricated *explanation* sits right beside that true data with the same authority and you have nothing to check it against.

**What did usability testing actually show?**
> Seven real users. All seven could use it and gave generally positive feedback. Two frictions still showed up, both in the same narrow band between seeing the insight and acting on it: users searched about twelve seconds before finding the action entry, and at least one asked "Is this cancelling the subscription?" Everything before and after that band held — the home entry, the evidence display, the confirmation, the completion.

**Why MEDIUM rather than HIGH?**
> Because the severity guide defines HIGH as *blocking task completion for multiple users*, not *affecting multiple users*. Frequency and severity are different axes. No user was blocked, so both are MEDIUM. Upgrading would make the rubric look satisfied while making the evidence false.

**Your B18 requirement isn't satisfied. Isn't that a failure?**
> It's an unmet acceptance criterion and I'm not hiding it — I state it in Part B and again in Part C. No High-priority insight→action friction was observed, so I report that there wasn't one. The alternative was to invent a blocked tester, and that fabrication would have flowed straight into my Part C experiment premise. A reported null is a result. A manufactured HIGH is a defect in the whole relay. I'd rather lose the criterion than corrupt everything downstream of it.

**Why is Errors zero — didn't you find anything wrong?**
> I found two things wrong, they just weren't errors. An error is a wrong action taken or a task failed. A twelve-second search is a hesitation; a clarifying question is a hesitation with a verbalisation. Classifying either as an error would have inflated my evidence to fill a category.

**What does Smart Spend Coach actually know? What does it not know?**
> It knows what's in your own PhonePe transaction record: merchant, amount, date, interval. From that it can tell that a charge recurs, that the amount went up against your own earlier charges, or that it resumed after a gap. It does **not** know whether you still use the service, whether a trial ended, whether the commitment is necessary, what any merchant's policy is, or anything about commitments you pay by card or another app. It says the first of those on the insight screen itself, in those words.

**Why doesn't stopping auto-debits equal cancelling the subscription?**
> Because they're actions on two different systems. Stopping auto-debits is a payer-side control — it prevents PhonePe from making further payments to that merchant. It doesn't touch your account with the merchant, because PhonePe has no relationship with the merchant's billing system and can't know their access or refund policy. I put that limitation verbatim on the confirmation screen — and my usability testing found a user asking exactly this question, which tells me the distinction needs to be clearer earlier, not just at confirmation.

**Why this A/B test?**
> It targets the funnel stage I prioritised and the friction I actually observed. It changes exactly one variable — the position and persistence of the action control — with identical copy in both arms, so a difference in conversion is attributable to discoverability rather than persuasion. And the confirmation gate stays in both arms: the variant makes the action easier to *find*, never easier to take by accident.

**Why IACR as the primary metric?**
> Because it's the only metric that fails when the feature explains beautifully and changes nothing — which is precisely the failure mode of this product category. And it's the same measurement as the funnel stage I prioritised: stage four-to-five is 2,856 over 9,520, which *is* IACR at 30%. I chose that metric in Part A before I analysed the funnel.

**Why ARR as the guardrail?**
> Because my primary metric rewards getting users to act, and unguarded that incentive rewards pushing people into stopping commitments they needed — especially serious for someone whose commitments affect other people. ARR is the direct detector. It's also why the experiment's decision waits for day 35: ARR has a fourteen-day window, so it matures after the primary metric does. Shipping on IACR at day 21 would mean shipping a conversion gain before the safety metric governing it had matured.

**Why the Content growth loop?**
> Because my persona's only current acquisition route is an in-app banner on an owned surface — which is why CAC is low, and also why reach is capped at whoever happens to be inside PhonePe when it fires. Content raises that ceiling without paid spend and brings in people actively searching for how to stop a recurring charge, which is higher intent than an unsolicited banner. Paid contradicts the economics that make the channel attractive. Virality would require users to share their own recurring financial commitments, which contradicts the Privacy-by-Design commitment I put on my own insight screen.

**How will AI cost be monitored?**
> Cost is monitored monthly rather than weekly — it's a margin risk, not a user-harm risk, and it moves predictably with volume. The concrete optimisation is trigger-keyed model tiering: because detection is deterministic, the system already knows which rule fired *before* any model call, for free. A simple amount-increase insight has exactly one shape, so it's served by a template; ambiguous cases escalate to a stronger model. The saving and the safety improvement come from the same change, because a template can't hallucinate.

**Why Safety and Quality for weekly monitoring, and not accuracy or cost?**
> Partly substance, partly discipline. Safety, because a fabricated explanation is the one failure my design safeguards don't protect against. Quality, because for this feature quality means *earned action* — IACR paired with ARR — and both are already instrumented. And deliberately not accuracy or cost, because those two names also appear in Part B's four-dimension risk list, and the brief is explicit that the two frameworks are not the same list restated. I didn't want my answer to read as a restatement even accidentally.

**What are the biggest remaining uncertainties?**
> Three. First, expected retention — the factor my entire persona choice rests on — is a hypothesis, not a finding, and it's the first thing I'd test. Second, the platform capability behind the one-tap action isn't established by the brief; I've carried it as a stated assumption with a documented fallback rather than assuming it exists. Third, I have no willingness-to-pay data for this category in India, which is why I specify a pricing *structure* but no price.

**Your tester count — can you evidence it?**
> Seven distinct people, and I ran the sessions myself. I should be straight with you: I didn't retain individual session records or dates, so what I have is an aggregate pattern plus the outcomes, and that's exactly how I've written it up — I haven't split it into seven invented session histories. If I ran this again, per-tester notes with timestamps would be the first thing I'd fix.

---

# PART 5 — MANUAL ACTIONS ONLY GAURAV CAN PERFORM

| # | Action | Why it can't be automated | Blocks |
|---|---|---|---|
| **M1** | **Airtable → Share → set base to "Anyone with the link can view"**, copy the link, paste it into Part A of the doc | Sharing cannot be set through the Airtable API/MCP | A24, G06, G18 |
| **M2** | **Figma → Share → "Anyone with the link" → can view**, copy the link, paste it into Part B of the doc | Sharing cannot be set through the Figma Plugin API | B09, B10, G07, G18 |
| **M3** | **Test both links in a logged-out incognito window** | Requires a real browser session outside this environment | G18, G21 |
| **M4** | **Create the Google Doc**, paste the submission content, set sharing to "Anyone with the link can view" | Requires your Google account | G01, G02 |
| **M5** | **Paste the Doc link into the assessment answer box and click MARK AS COMPLETED** | Requires your authenticated Masai session | G16, G17 |
| **M6** | **Check your usability session notes for a blocked/rescued tester** (≥45s, moderator intervention). If one exists, tell me — B18 becomes satisfiable honestly | Only you have that memory or record | B18 |
| **M7** | **Rehearse the viva answers aloud, without notes** | Guideline 4 requires *your* understanding | G20 |
| **M8** | *(Optional)* Push the GitHub repo to your own account | No GitHub credentials in this environment; **and the repo must never be submitted** | — |

**Deadline: 28 August 2026, 11:59 PM IST.** Do M4 and M5 several days early — the extension announcement explicitly warns about last-minute technical issues.
