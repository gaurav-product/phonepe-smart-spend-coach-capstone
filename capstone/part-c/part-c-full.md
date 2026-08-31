# PART C — GROWTH FUNNEL, EXPERIMENT DESIGN & AI EVALUATION
## PhonePe Smart Spend Coach · 35 marks

**Requirements covered:** C01 – C30
**Upstream locked and not reopened:** LA-02 persona · LA-09 Expected Retention · LA-17 C2 · LA-20 detection · LA-24 IACR · LA-25 ARR · LB-01–LB-08 prototype · LB-09 AI-augmented · LB-10 hallucination rate
**Part B evidence carried forward:** F-01 (MEDIUM) · F-02 (MEDIUM) · **B18 NOT SATISFIED** — see §3.1, which does not hide this

---

# TASK 1 — FUNNEL DIAGNOSIS

## 1.1 The pilot funnel `[CASE DATA — supplied by the Capstone]`

30-day pilot, eligible PhonePe users shown the entry banner.

| # | Stage | Users |
|---|---|---|
| 1 | Entry banner shown | 40,000 |
| 2 | Feature opened | 16,000 |
| 3 | Onboarding / transaction-linking completed | 11,200 |
| 4 | First personalized insight viewed | 9,520 |
| 5 | Recommended action taken | 2,856 |

**No number here is invented. All five are Capstone-supplied and are used exactly as given.**

## 1.2 The four transitions — arithmetic shown

### Transition 1 → 2 · Banner shown → Feature opened
```
Converted  =  16,000 ÷ 40,000  =  0.40  =  40.0%
Dropped    =  100% − 40.0%     =  60.0%
Users lost =  40,000 − 16,000  =  24,000
```

### Transition 2 → 3 · Feature opened → Onboarding completed
```
Converted  =  11,200 ÷ 16,000  =  0.70  =  70.0%
Dropped    =  100% − 70.0%     =  30.0%
Users lost =  16,000 − 11,200  =  4,800
```

### Transition 3 → 4 · Onboarding completed → First insight viewed
```
Converted  =  9,520 ÷ 11,200   =  0.85  =  85.0%
Dropped    =  100% − 85.0%     =  15.0%
Users lost =  11,200 − 9,520   =  1,680
```

### Transition 4 → 5 · First insight viewed → Recommended action taken
```
Converted  =  2,856 ÷ 9,520    =  0.30  =  30.0%
Dropped    =  100% − 30.0%     =  70.0%
Users lost =  9,520 − 2,856    =  6,664
```

### Summary

| Transition | Converted | Dropped | Users lost |
|---|---|---|---|
| 1 → 2 | 40.0% | **60.0%** | **24,000** |
| 2 → 3 | 70.0% | 30.0% | 4,800 |
| 3 → 4 | 85.0% | 15.0% | 1,680 |
| 4 → 5 | 30.0% | **70.0%** | 6,664 |

**End-to-end:** 2,856 ÷ 40,000 = **7.14%** of users shown the banner took the recommended action.

## 1.3 The two required separate reports

### ▶ Largest **ABSOLUTE** number of users lost: **Stage 1 → 2** — **24,000 users lost**
### ▶ Largest **PERCENTAGE** drop-off: **Stage 4 → 5** — **70.0% dropped**

## 1.4 These are different stages — and here is why the two measures disagree

**They are different stages, and the reason is arithmetic, not coincidence.**

Stage 1→2 loses more people in absolute terms because it operates on the largest population in the funnel: 60% of 40,000 is a bigger number than 70% of 9,520, even though it is a *smaller* proportion. Stage 4→5 is the harshest transition proportionally — it destroys **seven of every ten users who reach it** — but it only ever gets 9,520 users to work with, because three earlier stages have already filtered the population down.

**Absolute loss is a function of the drop rate *and* the size of the pool it is applied to. Percentage drop is a function of the drop rate alone.** Ranking by one and ranking by the other can only agree when the pools are equal, and here they differ by a factor of more than four.

> ### 1.4.1 The most important relay observation in Part C
>
> **Stage 4 → 5 is not merely a funnel stage. It *is* the locked primary success metric.**
>
> IACR (LA-24) = confirmed actions ÷ insights first viewed × 100. Stage 4→5 = 2,856 ÷ 9,520 = **30.0%**.
>
> **The pilot funnel's 4→5 conversion and Smart Spend Coach's primary metric are the same measurement.** The metric chosen in Part A, before this funnel was analysed, lands exactly on the stage Part C identifies as the priority. That is the relay working, not a coincidence arranged after the fact.

---

# TASK 2 — PRIORITIZATION (INTENT-PROXIMITY)

## ▶ Fix **Stage 4 → 5** first.

## 2.1 The intent-proximity principle, applied explicitly

**The principle:** prioritise drop-offs closer to the final action, because user intent is highest there. A user who has travelled further down the funnel has demonstrated more of the intent the product depends on, so recovering them is both more valuable per user and more achievable — you are removing an obstacle in front of someone already trying to get through, rather than manufacturing motivation in someone who has not yet shown any.

**Applied to this funnel:**

A user at Stage 4 has done **everything the product asked of them.** They saw the banner, opened the feature, granted transaction-linking permission — a real privacy decision, not a click — and read a personalised insight about their own money. Every one of those steps is a revealed signal of intent. Then **70% of them stop.**

That is not an intent problem. **These users wanted the outcome and did not complete it** — which by definition makes it a friction problem, and friction is what product design can actually fix.

## 2.2 Why Stage 1 → 2 is lower priority *despite losing 24,000 users* — more than three times as many

This is the part that must be argued rather than asserted, because 24,000 is a large number and ignoring it needs a reason.

**1. Those 24,000 never demonstrated any intent.** Stage 1 is a banner impression on an owned surface — the users did not seek the feature, it appeared in front of them while they were doing something else, usually a payment. A 40% open rate on an unsolicited in-app banner is a *discovery* outcome, not a rejection of the value proposition. Most of those 24,000 have no opinion about Smart Spend Coach at all; they were mid-task.

**2. The ceiling on recovery is much lower.** Improving a banner is a matter of copy, placement and timing — the intervention space is narrow and heavily constrained by the surrounding PhonePe payment experience. Improving an in-feature flow the user is already engaged with has a far larger design surface.

**3. The compounding argument runs the other way from the intuition.** Users recovered at Stage 1 must still survive Stages 2, 3 and 4 before they can act. Applying the pilot's own observed rates, an additional user recovered at Stage 1 converts to a completed action at 70.0% × 85.0% × 30.0% = **17.85%**. A user recovered at Stage 4→5 converts at **100%** — completing that stage *is* the action.

```
Value of +1 user recovered at Stage 1→2  =  0.700 × 0.850 × 0.300  =  0.1785 actions
Value of +1 user recovered at Stage 4→5  =                            1.0000 actions

One user recovered at the last stage is worth  1 ÷ 0.1785  ≈  5.6  users
recovered at the first.
```

**4. Stage 4→5 is where the product's actual claim lives.** Smart Spend Coach's competitive wedge is that the user can *finish* — `[FACT]` Ask Google Pay is documented as unable to initiate or complete payment transactions. A funnel that surfaces insights well and converts them to action 30% of the time is failing at the specific thing that differentiates it. Stage 1 failing is a marketing outcome. **Stage 4→5 failing is the product being wrong.**

**5. It is also where our own usability evidence sits.** Both real-user frictions found in Part B (F-01, F-02) occur between viewing the insight and completing the action — that is Stage 4→5 exactly. **We have observational evidence for this stage and none for Stage 1→2.**

**Stage 1→2 is not dismissed.** It is a real 24,000-user loss and is worth a separate workstream. It is second because each recovered user there is worth roughly a fifth of a recovered user at Stage 4→5, and because we have no evidence about why those users did not open.

---

# TASK 3 — A/B TEST DESIGN

## 3.1 Which specific Part B observation this addresses (C13)

## ▶ **Finding F-01 — Action-entry discoverability**, evidenced by observation **OBS-03**:
> *"Searched for approximately 12 seconds before locating the action entry"* — Screen 02, real-user testing, 7 distinct testers. **Severity: MEDIUM.**

### ⚠️ Required disclosure — the honest state of B18

The Capstone requires (B18) at least one **High**-priority observation describing friction between viewing an insight and completing the recommended action. **In our real-user testing, no such High-priority observation occurred.**

> **B18 HIGH-PRIORITY INSIGHT→ACTION FRICTION: NOT SATISFIED BY THE REAL-USER EVIDENCE.**
>
> Seven real users tested the prototype. **No blocked completion was reported.** Two MEDIUM insight→action frictions were observed. Under the locked severity guide — High = blocks task completion for multiple users — neither qualifies as High.

**This experiment is therefore built on the strongest MEDIUM finding, and says so.** A High-priority finding was not manufactured to satisfy the rubric. F-01 is nonetheless the correct target: it is a real, observed, insight→action friction, it lands on the prioritised funnel stage, and it is directly measurable.

**Why F-01 rather than F-02** (*"Is this cancelling the subscription?"*): F-01 has a measured behavioural signal (≈12 seconds) and a single-variable intervention. F-02 is about comprehension of the action's meaning and would require a copy change whose effect on the ARR guardrail is harder to isolate. **F-02 is a strong candidate for a second experiment** and is not being discarded.

## 3.2 The change being tested

| | |
|---|---|
| **Control (A)** | Screen 02 as built: merchant summary → "WHAT WE OBSERVED" six-charge history → "WHY YOU'RE SEEING THIS" → limitation line → **action entry below the evidence block** |
| **Variant (B)** | Identical content and identical copy, with the action entry presented as a **persistent action bar fixed to the bottom of the viewport**, visible from the moment the insight screen opens without scrolling or scanning |

**Only one variable changes: the position and persistence of the action control.** All copy, all evidence, the limitation sentence, the confirmation sheet and the undo path are byte-identical between arms — so any difference in IACR is attributable to discoverability and not to persuasion. **The confirmation gate is present in both arms**; the variant makes the action easier to *find*, never easier to *take by accident*.

## 3.3 Hypothesis — exact required template, all four blanks filled (C14)

> **We believe that** *making the recommended action a persistent action bar fixed to the bottom of the insight detail screen, visible on open without scrolling past the six-row charge history*
>
> **will result in** *an increase in the percentage of first-viewed flagged-commitment insights that reach a confirmed action within 7 days, and a reduction in the median time from first insight view to confirmed action*
>
> **because** *in real-user testing of the current design, testers searched for approximately 12 seconds before locating the action entry (finding F-01, observation OBS-03), and the pilot funnel shows that 70% of users who view a personalised insight never complete the recommended action — indicating the loss is at the point of acting, not at the point of understanding.*
>
> **We will measure** *Insight-to-Action Completion Rate (IACR).*

## 3.4 Metric Triad — precise formulas (C15, C16, C17)

### PRIMARY — Insight-to-Action Completion Rate (IACR) `[locked LA-24]`
```
          Number of distinct flagged-commitment insights for which the user
          completes and confirms the supported action within 7 days of first
          viewing that insight
IACR  =  ──────────────────────────────────────────────────────────────────  × 100
          Number of distinct flagged-commitment insights first viewed by
          users during the same measurement period
```
**Unit of analysis:** the insight, not the user. **Inclusion:** confirmed actions only — past the confirmation screen. **Exclusion:** low-confidence items (LA-26), on which no action is offered, are excluded from the denominator. **Window:** 7 days from that insight's first view.
**Pilot baseline from the supplied funnel:** 2,856 ÷ 9,520 = **30.0%**. `[CASE DATA]`

### SECONDARY — Median Time-to-Action (TTA)
```
TTA  =  median, across all confirmed actions in the period, of
        ( timestamp of action confirmation  −  timestamp of first view
          of that same insight ),  expressed in seconds
```
**Why this metric and not a generic engagement number:** it measures **the exact mechanism the hypothesis proposes**. If the action bar works by making the control easier to find, TTA must fall. If IACR rises but TTA does not, the improvement came from something other than discoverability and the causal story is wrong. **This is the metric that can falsify our own explanation** — which is why it is the secondary rather than a vanity count.
**Reference point from usability testing:** ≈12 seconds of searching before locating the action entry (OBS-03) — an observation, not a target. **No target value is set, because no baseline TTA has been measured.** `[NOT VERIFIED]`

### GUARDRAIL — Action Reversal Rate (ARR) `[locked LA-25]`
```
          Number of confirmed actions that the user reverses (in-flow undo,
          or re-authorising the same merchant commitment) within 14 days
          of confirmation
ARR   =  ──────────────────────────────────────────────────────────────────  × 100
          Total number of confirmed actions in the same period
```
**Why this is the correct guardrail for this specific change:** the intervention makes an irreversible-feeling financial action easier to reach. The failure mode it could cause is users acting **before** reading the evidence they scrolled past — stopping auto-debits the household needed. ARR is the direct detector of that harm.
**Stopping condition:** if ARR in the variant rises materially above control, the variant is rejected **even if IACR improves.** A conversion win bought with regretted financial actions is a loss. **No numeric threshold is pre-set here, because no ARR baseline exists yet** `[NOT VERIFIED]` — the threshold must be fixed from control-arm data before the test is unblinded, not after (see §3.6).

## 3.5 Duration (C18)

## ▶ **21 days total: 14 days of enrolment + a 7-day attribution tail.**

**The reasoning, which is driven by our own metric definition:**

1. **IACR attributes an action up to 7 days after the insight is first viewed.** An insight first viewed on the last day of enrolment therefore has a window that closes 7 days later. Ending the test on the last enrolment day would systematically under-count late-enrolled insights — a censoring error, not noise.
2. **≥1 full 7-day behaviour cycle is required by the brief, and is comfortably met.** 14 days of enrolment spans **two complete weekly cycles**, so weekday/weekend differences in when users open PhonePe are represented in both arms rather than sampled unevenly. Household financial attention is not uniform across the week; a 7-day-only enrolment would leave one arm exposed to a single weekend.
3. **Why not longer:** the flagged-commitment population is generated by an already-running detection process, so extending enrolment adds statistical precision but delays a decision on a change that is cheap to ship and cheap to revert.
4. **⚠️ The guardrail matures later than the primary metric.** ARR has a **14-day** window from confirmation. The last confirmed action can occur on day 21, so **the guardrail cannot be fully read until day 35.** The primary readout at day 21 is therefore **provisional**; the ship decision waits for the ARR readout at day 35. **Declaring a winner at day 21 on IACR alone would be shipping a conversion gain before the safety metric that governs it has matured.**

```
Day  0 ─────────────── Day 14        enrolment (2 full 7-day cycles)
                       Day 14 ─────── Day 21   attribution tail (IACR window closes)
                                      Day 21   PRIMARY readout — provisional
                                      Day 21 ────────────── Day 35  ARR window closes
                                                            Day 35   GUARDRAIL readout — decision
```

## 3.6 Pitfall + precaution (C19, C20)

## ▶ Pitfall this specific design risks: **EARLY JUDGMENT ERROR**

**Why this one, specifically for this test.** Both of our decision metrics are **lagging by construction** — IACR attributes over 7 days, ARR over 14. That means early results are not merely noisy, they are **systematically biased downward**: on day 3, most enrolled insights have not had time to convert, and almost no confirmed action has had time to be reversed. A day-3 dashboard would show a low IACR and a **near-zero ARR** in both arms. The near-zero ARR is the dangerous number, because it would look like proof the change is safe at exactly the moment when no reversal *could* yet have been recorded. **The temptation to call the test early is strongest precisely when the guardrail is structurally incapable of firing.**

**Why not the other three:**
- **Novelty Effect** — genuinely plausible for any visual change, and the runner-up. Rejected as the primary answer because the change is a permanent structural repositioning of an existing control rather than a new stimulus, and because the 14-day enrolment gives repeat exposure time to wash out short-lived attention effects. **Not zero risk** — the trend across the two weekly cycles should be inspected for decay.
- **Local Maxima Trap** — applies to a long series of small optimisations; this is a single first test on this surface.
- **HARKing** — this hypothesis was written **before** the test from a pre-existing Part B observation (F-01/OBS-03), which is the structural opposite of hypothesising after results are known.

### ▶ One concrete precaution

**Pre-register the readout schedule and the decision rule before enrolment opens, and take no unblinded look at either arm before day 21.**

Concretely: the analysis plan is written and fixed in advance — primary readout day 21, guardrail readout day 35, ARR rejection threshold set from **control-arm data only** and fixed before the arms are compared. Operational health checks during the run (crash rates, delivery of insights, arm balance) are permitted and are deliberately **restricted to metrics that are not the decision metrics**, so monitoring the test cannot become judging it.

---

# TASK 4 — GROWTH LOOP

## ▶ Selected: **CONTENT** `[PM DECISION]`

## 4.1 Justification — one paragraph, referencing acquisition channel and WTP (C21, C22, C23)

> Smart Spend Coach's primary persona — the mid-career household financial manager, 33–45 — is reached today through exactly one route: **the in-app entry banner on PhonePe, an owned surface** `[verified in the Airtable Personas table]`. That channel is the reason acquisition cost is Low, and it is also the reason the funnel starts where it does: 40,000 impressions produced 16,000 opens, which means the ceiling on this feature's reach is *whoever happens to already be inside PhonePe when the banner fires.* A **content loop** is the only one of the three options that raises that ceiling without abandoning the economics that make the channel attractive: people in this persona are already searching for how to stop a recurring charge they have noticed on a statement, and search-discoverable material answering that question brings in users who are actively looking for the outcome the feature delivers — which is a higher-intent entry than an unsolicited banner, and directly relevant given that 60% of banner impressions never convert to an open. It also fits a **willingness to pay assessed as Medium and, honestly, as a hypothesis rather than a finding** `[HYPOTHESIS — no India-specific WTP data for this category was located]`: a Medium-WTP user has to be convinced of value before being asked to pay, and content does that convincing before the user ever reaches the product, which is the same reason freemium rather than free-trial was chosen in Part B Task 5. The loop closes because the feature's own operation generates the raw material — the aggregate, non-identifying patterns of what kinds of recurring commitments users review and stop — which becomes the next piece of content, which is discovered by the next cohort. **`[PM DECISION]` — with one hard constraint: any such content may only ever use aggregate, non-identifying statistics. Publishing anything traceable to an individual's transactions would contradict the Privacy-by-Design commitment stated on the product's own insight screen, and would be a violation of the locked scope, not a growth tactic.**

## 4.2 Why not the other two

| Loop | Why rejected |
|---|---|
| **Paid** | Directly contradicts the acquisition economics of the locked persona. CAC is Low **because** distribution is an owned in-app surface with no paid media. Buying users for a feature whose WTP is an unevidenced Medium means spending certain money to acquire uncertain revenue — and it does not compound: the loop stops the moment the spend stops. |
| **Virality** | The only thing a user could share is **their own recurring financial commitments.** Sharing is structurally at odds with both the locked data scope (the user's own PhonePe transaction data) and the Privacy-by-Design principle stated on Screen 02. A referral mechanic detached from the product's actual output would be a bolt-on, not a loop. **Rejecting virality here is a consequence of the ethics position taken in Part B Task 4, not an independent judgement.** |

---

# TASK 5 — AI EVALUATION, COST & DASHBOARD

## 5.1 Two of the five monitoring dimensions (C24) — and why this is not Part B restated (C25)

> ### ⚠️ FRAMEWORK SEPARATION — stated explicitly, because the brief names this trap
>
> | | Part B Task 2 | Part C Task 5 *(here)* |
> |---|---|---|
> | Framework | **4-dimension per-feature risk** | **5-dimension operational monitoring** |
> | Members | accuracy · response speed/latency · token cost/efficiency · hallucination rate | quality · cost · accuracy · operational efficiency · safety |
> | Question asked | *What is the single biggest risk in this feature?* | *What do we watch every week once it is running?* |
> | Answer | **Hallucination rate** (LB-10) | **Safety + Quality** (below) |
>
> These are different questions. One is a design-time risk judgement about a feature; the other is an operating discipline. **The two dimensions chosen below are deliberately not "hallucination rate" restated**, and the two members whose names overlap with the Part B list — *accuracy* and *cost* — are **not** selected, so that no reader could mistake this answer for the earlier one.

### ▶ Dimension 1 — **SAFETY**

**Monitored weekly as:** a fixed-size random sample of generated insight explanations shown to users that week, each checked line-by-line against the transaction record that produced it, and marked as a boundary violation if it asserts anything the transaction data cannot support — most specifically the three claims the product explicitly does not have: that a service is unused, that a trial has ended, or that a commitment is unnecessary. The output is a weekly **boundary-violation count and rate**, with every violation retained verbatim.

**Why it earns a weekly slot:** this is the failure with the highest consequence and the **lowest chance of being caught by any other signal**. An inaccurate flag is visible to the user, who can check the six-row charge history and disagree. A fabricated *explanation* sits directly beside true data and carries identical authority — the user has nothing to check it against. It is the one failure mode where the product's design safeguards do not protect the user, which is why it needs a human in the loop every week rather than a threshold alert.

### ▶ Dimension 2 — **QUALITY**

**Monitored weekly as:** the pairing of **IACR** (are users acting on what we surface?) with **ARR** (are they regretting it afterwards?), read together on the same weekly time base, plus the sampled explanations from the safety review rated for whether the stated reason matches the rule that actually fired.

**Why it earns a weekly slot:** quality for this feature is not fluency, it is *earned action*. An explanation is high quality only when it moves a user to a decision they do not reverse. **IACR alone can be gamed by more assertive copy; ARR alone can be minimised by surfacing nothing. Only the pair describes quality**, and the pair is already instrumented — this dimension requires no new measurement infrastructure, which is a real operational argument for choosing it over dimensions that would.

**Why not the other three:**

| Dimension | Why not weekly |
|---|---|
| **Cost** | Genuinely matters and is addressed in §5.2 — but it is a **margin** risk, not a user-harm risk, it moves slowly and predictably with volume, and monthly review is sufficient. Also shares a name with a Part B dimension. |
| **Accuracy** | Structurally constrained already: detection is deterministic (LB-09), so the arithmetic deciding *whether* to flag cannot drift week to week. It also shares a name with a Part B dimension. |
| **Operational efficiency** | The strongest of the three rejected. Worth watching, but it is a second-order concern until safety and quality are stable — an efficiently-run pipeline producing unsafe explanations is worse than an inefficient safe one. |

## 5.2 One concrete token-cost optimization for this feature's insight-generation calls (C26)

## ▶ **Trigger-keyed model tiering: route formulaic explanations to the cheap path, escalate only ambiguous ones.**

**Applied specifically to Smart Spend Coach's insight-generation calls:**

Because detection is **deterministic** (LB-09), the system already knows — with no model call at all — exactly which rule fired before any explanation is generated. That routing signal is free, and it is what makes the tiering possible:

| Case | Route | Why |
|---|---|---|
| **T1 alone** — single merchant, clean normalisation, amount increased vs the user's own prior charges | **Cheapest path:** a fixed template populated from the transaction record — merchant, prior amount, new amount, dates | The explanation has exactly one shape: *"This charge has gone up from ₹X to ₹Y since <date>."* There is no reasoning to perform, so paying model tokens to reproduce a fixed sentence is pure waste — **and a template cannot hallucinate**, which reduces the §5.1 safety load at the same time |
| **T2 alone** — charge resumed after a gap, unambiguous | **Cheap model tier** | Slightly more variable phrasing; still low complexity |
| **Both triggers, or ambiguous merchant normalisation, or an unusual interval** | **Stronger model tier** | Genuine judgement about what to say and what not to claim — the minority of cases where model quality is actually load-bearing |

**Why this is the right technique for *this* feature rather than a generic one:** the expensive layer is already small, because deterministic detection means only *flagged* items ever reach a model, and Edge Case 1 (LA-26) suppresses low-confidence items entirely before that point. Tiering compounds those existing reductions. **The cost saving and the safety improvement come from the same change** — every insight moved onto the template path is one that cannot fabricate an explanation.

*(A second technique — caching the shared system/context prompt across users, since the instruction and boundary rules are identical for every insight — is available and complementary. **One technique is what the requirement asks for; trigger-keyed tiering is the answer.**)*

## 5.3 The 5-3-1 dashboard specification (C27, C28, C29)

> All items are specific to Smart Spend Coach. **No generic placeholder — no "DAU", "MAU", "engagement", "retention curve" or "NPS" appears anywhere below.**

### ▶ 1 CORE INSIGHT METRIC

> **Insight-to-Action Completion Rate (IACR)** — confirmed actions on flagged-commitment insights, divided by flagged-commitment insights first viewed, within 7 days of first view, × 100.
>
> **Why this is the one:** it is the only number that fails when the feature explains beautifully and changes nothing — which is precisely the failure this product exists to avoid, and precisely what the pilot funnel shows happening at 30.0%.

### ▶ 5 SUPPORTING KPIs

| # | KPI | Formula | What it tells us that IACR alone does not |
|---|---|---|---|
| **1** | **Action Reversal Rate (ARR)** | confirmed actions reversed within 14 days ÷ confirmed actions × 100 | Whether the actions we drove were *wanted*. The one KPI that can veto a rise in the core metric |
| **2** | **Median Time-to-Action (TTA)** | median of (confirmation timestamp − first-view timestamp) across confirmed actions, in seconds | Whether the insight→action path is *findable*. Directly tracks finding F-01 and the ≈12-second search observation |
| **3** | **Insight View Rate** | flagged-commitment insights first viewed ÷ flagged-commitment insights surfaced × 100 | Separates a delivery problem from an action problem. If IACR falls while this also falls, the issue is upstream of the insight screen |
| **4** | **Low-Confidence Suppression Rate** | recurring patterns detected but withheld under LA-26 ÷ all recurring patterns detected × 100 | Whether the honesty rule is calibrated. Near zero means the evidence bar is doing nothing; very high means users with thin history see an empty product |
| **5** | **Explanation Grounding Pass Rate** | sampled generated explanations with no claim unsupported by the transaction record ÷ sampled explanations × 100 | The weekly safety number from §5.1. The direct operational descendant of the LB-10 hallucination risk |

### ▶ 3 VISUALIZATIONS

**V1 · Insight→action funnel, split by trigger type**
A five-bar funnel of the pilot stages (banner shown → opened → onboarded → insight viewed → action taken), with the 4→5 transition visually emphasised as the priority stage, and each bar **split into T1 (amount-increased) and T2 (resumed-after-gap) segments.**
*What it is for:* to reveal whether one detection trigger converts materially worse than the other. If T2 insights are viewed as often but acted on far less, the problem is the trigger's persuasiveness, not the screen — a diagnosis no aggregate funnel can produce.

**V2 · Weekly IACR with ARR on a shared time axis**
A dual-axis weekly line chart, IACR on the left axis and ARR on the right, deliberately plotted on the same time base rather than in separate tiles.
*What it is for:* to make one specific pattern impossible to miss — **IACR rising while ARR rises with it.** That divergence is the signature of the product pushing users into actions they regret, and it is invisible when the two metrics live on separate dashboard tiles. This chart exists to catch our own primary metric being gamed.

**V3 · Time-to-action distribution histogram**
Seconds from first insight view to confirmed action, bucketed (0–5s, 5–10s, 10–20s, 20–60s, >60s, plus a "viewed, never acted" column), with a marked reference line at the **≈12-second search time observed in real-user testing (F-01 / OBS-03).**
*What it is for:* the A/B test in Task 3 predicts this distribution shifts left. The median alone hides *how* it shifts — a genuine discoverability fix should thin the long right tail and grow the 0–5s bucket, whereas a mere persuasion effect would move the mass without changing the shape. **This is the chart that tests our explanation, not just our outcome.**

---

# CLOSING — FREE-PATH STATEMENT (C30)

> Every tool used in this project has a free path, and **no paid API key, developer account or account-gated service was required at any point.** The prototype was built in **Figma on the free Starter plan**, which supports the single file, five screens, component, variant and prototype interactions used here. The persona and opportunity-backlog tables were built in **Airtable's free tier**, well within its row limits for two small tables. AI assistance was used through a **free-tier conversational AI assistant** for research support, drafting and adversarial review — never through a paid API, and nothing in this project runs as deployed code, so no hosting, inference or infrastructure billing exists. The submission document itself is a **Google Doc on a free Google account**, and the usability sessions required no software beyond Figma's own Present mode. **The token-cost optimisation described in §5.2 is a design specification for a production system, not a cost incurred by this project.**

---

# PART C — REQUIREMENT CHECK

| Req | Requirement | Where | Status |
|---|---|---|---|
| C01 | Use the supplied funnel | §1.1 | ✅ exact figures |
| C02–C05 | Four transitions, % converted **and** % dropped | §1.2 | ✅ all four, both figures, arithmetic shown |
| C06 | Arithmetically correct | §1.2 | ✅ independently recomputed |
| C07 | Largest **absolute** loss | §1.3 | ✅ 1→2, 24,000 |
| C08 | Largest **percentage** drop | §1.3 | ✅ 4→5, 70.0% |
| C09 | Shown to be different stages | §1.4 | ✅ + explanation of *why* they diverge |
| C10 | Intent-proximity invoked **explicitly** | §2.1 | ✅ named and applied |
| C11 | Why the other is lower priority despite more raw users | §2.2 | ✅ five reasons incl. quantified 5.6× argument |
| C12 | One A/B test on the prioritized stage | §3.2 | ✅ |
| C13 | Names the specific Part B observation | §3.1 | ✅ F-01 / OBS-03 — **with B18 status disclosed** |
| C14 | Exact hypothesis template, 4 blanks | §3.3 | ✅ verbatim template |
| C15 | Primary metric as formula | §3.4 | ✅ IACR |
| C16 | Secondary metric as formula | §3.4 | ✅ TTA |
| C17 | Guardrail metric as formula | §3.4 | ✅ ARR |
| C18 | Duration ≥1 full 7-day cycle, reasoned | §3.5 | ✅ 21 days = 2 cycles + attribution tail |
| C19 | One named pitfall | §3.6 | ✅ Early Judgment Error |
| C20 | One concrete precaution | §3.6 | ✅ pre-registered readout, no early unblinded look |
| C21 | Growth loop selected | §4 | ✅ Content |
| C22 | Justified vs acquisition channel | §4.1 | ✅ in-app entry banner, owned surface |
| C23 | …and willingness-to-pay | §4.1 | ✅ Medium `[HYPOTHESIS]` |
| C24 | 2 of 5 monitoring dimensions + why | §5.1 | ✅ Safety + Quality |
| C25 | **Not** a restatement of Part B's list | §5.1 | ✅ explicit comparison table; overlapping names deliberately avoided |
| C26 | One token-cost optimization, feature-specific | §5.2 | ✅ trigger-keyed model tiering |
| C27 | Exactly 1 core insight metric | §5.3 | ✅ IACR |
| C28 | Exactly 5 supporting KPIs | §5.3 | ✅ five, each with a formula |
| C29 | Exactly 3 visualizations, specific | §5.3 | ✅ three, each with a stated diagnostic purpose |
| C30 | 3–5 lines free-path statement | Closing | ✅ |

**No fabricated data. All funnel figures are Capstone-supplied. No baseline, target or threshold has been invented — where one would be needed it is marked `[NOT VERIFIED]` and the method for setting it is stated instead.**

---

*Part C complete. Figma unmodified. No decision locked without instruction.*
