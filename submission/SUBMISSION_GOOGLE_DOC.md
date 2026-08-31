```{=openxml}
<w:p><w:pPr><w:spacing w:before="2600" w:after="0"/></w:pPr><w:r><w:rPr><w:b/><w:sz w:val="60"/><w:color w:val="5F259F"/></w:rPr><w:t>PhonePe Smart Spend Coach</w:t></w:r></w:p>
<w:p><w:pPr><w:spacing w:before="120" w:after="360"/><w:pBdr><w:bottom w:val="single" w:sz="12" w:space="6" w:color="5F259F"/></w:pBdr></w:pPr><w:r><w:rPr><w:sz w:val="30"/><w:color w:val="444444"/></w:rPr><w:t>Feature Design, Validation and Growth Case</w:t></w:r></w:p>
<w:p><w:pPr><w:spacing w:after="600"/></w:pPr><w:r><w:rPr><w:sz w:val="24"/><w:color w:val="666666"/></w:rPr><w:t>Product Management Capstone</w:t></w:r></w:p>
<w:p><w:pPr><w:spacing w:after="160"/></w:pPr><w:r><w:rPr><w:b/><w:sz w:val="24"/></w:rPr><w:t xml:space="preserve">Prepared by  </w:t></w:r><w:r><w:rPr><w:sz w:val="24"/></w:rPr><w:t>Gaurav Kumar Singh</w:t></w:r></w:p>
<w:p><w:pPr><w:spacing w:after="160"/></w:pPr><w:r><w:rPr><w:b/><w:sz w:val="24"/></w:rPr><w:t xml:space="preserve">Feature  </w:t></w:r><w:r><w:rPr><w:sz w:val="24"/></w:rPr><w:t>Flagged Commitment and One-Tap Action</w:t></w:r></w:p>
<w:p><w:r><w:rPr><w:b/><w:sz w:val="24"/></w:rPr><w:t xml:space="preserve">Contents  </w:t></w:r><w:r><w:rPr><w:sz w:val="24"/></w:rPr><w:t>Parts A, B and C in a single document</w:t></w:r></w:p>
```
```{=openxml}
<w:p><w:r><w:br w:type="page"/></w:r></w:p>
```

## Contents

**Part A — Research, Persona and Feature PRD**

- Task 1. Persona development and segmentation
- Task 2. Competitive analysis and feature positioning
- Task 3. Opportunity generation and RICE prioritisation
- Task 4. Airtable opportunity backlog
- Task 5. Mini-PRD

**Part B — Prototype, Usability Validation and Pricing**

- Task 1. Figma prototype
- Task 2. AI classification and biggest risk
- Task 3. Usability validation
- Task 4. Ethics, bias and safety
- Task 5. Pricing and packaging

**Part C — Growth Funnel, Experiment Design and AI Evaluation**

- Task 1. Funnel diagnosis
- Task 2. Prioritisation
- Task 3. A/B experiment
- Task 4. Growth loop
- Task 5. AI evaluation, cost and dashboard

**Closing sections**

- Tool access and cost statement
- Limitations and open questions

## A note on evidence labelling

Claims in this document are labelled so that established fact can be distinguished from reasoning. `[CASE DATA]` is supplied by the Capstone brief. `[FACT]` is verified against a named external source. `[DERIVED]` is computed from a stated input. `[PM INFERENCE]` is my own reasoning. `[HYPOTHESIS]` is a belief that would require testing. `[DESIGN ASSUMPTION]` is an implementation assumption. `[NOT VERIFIED]` was searched for and could not be established. Where a claim could not be established, it is marked as such rather than asserted.

```{=openxml}
<w:p><w:r><w:br w:type="page"/></w:r></w:p>
```
# PART A — RESEARCH, PERSONA & FEATURE PRD

## TASK 1 — PERSONA DEVELOPMENT & SEGMENTATION

**AI-assisted approach used:** Guided AI Q&A — I directed the analysis through structured questioning and fact-checking rounds, supplying the decisions and the evidence standard myself.

### Persona 1 (PRIMARY) — Mid-Career Household Financial Manager

Married adults aged **33–45** in tier-1 and tier-2 India, typically with dependants, who are the designated money-manager of their household — carrying fixed obligations (EMIs, insurance, school fees, utilities) alongside family-wide discretionary spend across several people.

**Top frustration:** Recurring commitments accumulate quietly across the household — subscriptions and services paid from their own PhonePe account on behalf of different household members. Each charge is individually small and debits automatically, so none becomes urgent enough to deal with, and nothing assembles them into a single view they can act on. Noticing a charge and doing something about it are two separate tasks on two different days.

**Top goal:** Keep household recurring commitments under control without auditing them manually, and act on a questionable charge at the moment they notice it rather than somewhere else later.

**Acquisition channel:** In-app entry banner on PhonePe (owned surface).

**The four segmentation factors:**

| Factor | Rating | Reasoning |
|---|---|---|
| **Segment size** | Medium-High — plausibly in the tens of millions | `[DERIVED]` From PhonePe's 700M registered users `[FACT]`, of which over 65% are non-metro `[FACT]`, narrowed to tier-1/2 household money-managers across a 12-year age band. PhonePe publishes no MAU and no category-mix breakdown, so the step from registered users to addressable users is my assumption. Read as order-of-magnitude only — I have deliberately not published a point estimate, because that would be arithmetic performed on guesses. |
| **Willingness to pay** | **Medium** | `[HYPOTHESIS]` Higher absolute income and an established habit of paying for financial products support *ability* to pay; working against it, this cohort is the most likely to believe it already knows where its money goes, which suppresses perceived value. No credible source quantifying Indian consumer willingness to pay for a personal-finance product was located. |
| **Cost of acquisition** | **Low-Medium** | `[PM INFERENCE]` Low in absolute terms because distribution is an owned in-app surface to an existing base — there is no paid-media cost. The Medium component reflects likely greater hesitancy about granting transaction analysis over household-level financial data. |
| **Expected retention** | **High** | `[HYPOTHESIS]` The strongest retention case of any candidate: the need is structural and permanent rather than life-stage-bound. Household budgeting is an ongoing role with no natural end point; bills, renewals, EMIs and school-fee cycles recur on their own schedules; and a household's subscription base regenerates as family members add services, so the feature does not run out of material. |

### Persona 2 (SECONDARY) — Young Urban Salaried Professional

Salaried adults aged **24–32** in tier-1 and top tier-2 cities, three to eight years into a career, living alone or flat-sharing, with most discretionary spend flowing through UPI apps.

**Top frustration:** Discretionary spend and forgotten recurring subscriptions leak money each month. The waste is visible in their own transaction history, but stopping it is a separate task completed in a different place, so it is easy to defer indefinitely.

**Top goal:** Remove avoidable recurring spend quickly, with the least possible effort between noticing a charge and acting on it.

**Acquisition channel:** In-app entry banner on PhonePe (owned surface).

| Factor | Rating | Reasoning |
|---|---|---|
| **Segment size** | Medium — plausibly tens of millions, smaller than the primary | `[DERIVED]` PhonePe states over 65% of its consumers are from beyond traditional urban hubs `[FACT]`, so a tier-1-skewed cohort is a minority of the base. Same unverifiable step as above applies. |
| **Willingness to pay** | **Medium** | `[HYPOTHESIS]` Composed differently from the primary: lower ability to pay, higher perceived value. Net rating comparable. |
| **Cost of acquisition** | **Low** | `[PM INFERENCE]` Owned in-app distribution, and the lowest expected hesitancy about granting transaction-analysis permissions of any candidate. |
| **Expected retention** | **Medium** | `[HYPOTHESIS]` Monthly spend cycles regenerate material, but the largest wins are one-time structural fixes — cancel two dead subscriptions, set one cap — after which the feature has structurally less to say. Novelty decay is a live risk, with a self-defeating dynamic: if the nudges work, spending normalises and the variance signal the feature depends on shrinks. |

### Which persona is primary, and why — using the four factors

| Factor | Primary (Household Manager) | Secondary (Young Professional) | Favours |
|---|---|---|---|
| Segment size | Medium-High | Medium | Primary, slightly |
| Willingness to pay | Medium | Medium | **Tie** |
| Cost of acquisition | Low-Medium | Low | Secondary, slightly |
| **Expected retention** | **High** | **Medium** | Primary, clearly |

The two finalists are close or tied on three of the four factors. **Expected retention is the only factor that separates them cleanly**, and it is therefore the factor on which the decision properly turns.

**A trade-off accepted:** the primary persona does not have the most addressable wallet. A significant share of its spend is fixed — EMIs, school fees, insurance — and is not reducible by a nudge. I am deliberately accepting a narrower addressable share of wallet in exchange for a more durable need. The secondary persona actually has the *better* product–problem fit; it is secondary on economics, not on fit.

### One-line justification of the primary factor

> **Expected retention is the primary segmentation factor, because Smart Spend Coach creates value only through repeated cycles of insight and action — a segment that produces one burst of value and then goes quiet cannot sustain the feature, however well it fits at first contact.**

**Why not willingness to pay,** the commercially obvious choice: WTP does not separate the two finalists — both rate Medium — and it is the least-evidenced of the four factors. A factor that ties the finalists and has the weakest evidence cannot be the factor that decides between them. It remains important and it drives the pricing decision in Part B.

---

## TASK 2 — COMPETITIVE ANALYSIS & FEATURE POSITIONING

### Direct competitors

**D1 · Ask Google Pay (Google, India).** A conversational AI assistant powered by Gemini inside Google Pay India. Users can *"understand your spending patterns"*, get savings tips, and explore tailored offers; it draws on Google Pay transaction history, CIBIL credit reports and saved payment methods, is opt-in, and supports 10 Indian languages. `[FACT — Google India official blog; Google Pay India help page]`
> **The decisive verified limitation, in the vendor's own words:** *"Ask GPay cannot initiate or complete payment transactions."* `[FACT]`

**D2 · CRED Money (CRED).** A personal financial manager on India's RBI Account Aggregator framework. Consolidates financial data across banks, supports merchant/category lookup, and tracks recurring payments including SIPs, rent and salaries. `[FACT — TechCrunch launch reporting, corroborated by Business Standard and Inc42]` Caveat carried forward: this rests on independent launch reporting rather than a primary vendor page, and is roughly two years old.

**D3 · Jupiter Money Manager (Jupiter).** Categorises every spend, aggregates bank accounts, and offers budgets with a proactive over-budget notification. `[FACT — Jupiter official product page, primary source]`

### Indirect competitor
**I1 · The manual spreadsheet / self-maintained household budget** — it solves the same underlying job (*understand and control my spending*) through an entirely different product form, and it is the only option verified as genuinely multi-user.
**I2 · UPI AutoPay mandate management screens.** The mechanism that actually stops a recurring charge, with no insight attached to it.

### Feature comparison matrix — 10 features

**Legend.** Yes = verified present. Partial = verified with a stated limit. No = verified absent and documented by the vendor. Not verified = searched for, no evidence located; absence is not implied.

| # | Feature | Smart Spend Coach | D1 Ask GPay | D2 CRED Money | D3 Jupiter | I1 Spreadsheet | I2 AutoPay screens |
|---|---|---|---|---|---|---|---|
| F1 | Transaction categorisation | Yes | Not verified | Yes | Yes | Partial manual | n/a |
| F2 | Multi-bank aggregation | Out of scope | Partial GPay + CIBIL | Yes | Yes | Partial manual | n/a |
| F3 | Period-over-period variance detection | Yes | Partial | Partial | Partial | Partial manual | n/a |
| F4 | Personalised spending insight | Yes | Yes | Yes | Partial | No | No |
| F5 | Conversational AI explanation | Out of scope | Yes Gemini, 10 languages | Not verified | Not verified | No | No |
| F6 | Proactive, system-initiated nudge | Yes | No — opt-in assistant → pull, not push | Partial reminders | Yes over-budget alert | No | Not verified |
| F7 | Budget / spending cap | Yes | Not verified | Not verified | Yes | Partial manual | No |
| F8 | Recurring payment detection | Yes | Not verified | Yes | Not verified | Partial manual | Partial shows mandates, no disuse detection |
| **F9** | One-tap action attached to the insight | Yes | No — vendor-documented | Not verified | Partial pays bills, not from an insight | No | Partial revoke a mandate, no insight attached |
| F10 | Household / multi-member visibility | Out of scope | No — group expenses is split settlement only | Not verified | Not verified | Yes | No |

### Classification — all four categories

**TABLE STAKES.** F1 transaction categorisation · F4 personalised spending insight · F2 multi-account visibility. Verified across the direct competitors; expected of any product in this category.

**PARITY.** F7 budget/spending cap (Jupiter verified *"Set Budgets"*) · F6 the *mechanism* of a proactive nudge (Jupiter verified) · F8 recurring-payment detection (CRED verified). Detecting a recurring charge is parity, not innovation — saying otherwise would be the easiest overclaim in this analysis.

**DIFFERENTIATOR.** A one-tap action attached to the insight itself (F9). This is the strongest claim available because it rests on the only vendor-documented absence in the entire matrix. Stated precisely: *verified absent in D1; not verified either way in D2 and D3.* Secondary differentiator: push, not pull — D1 is documented as an opt-in assistant the user queries.

**GAP.** The insight→action loop on a recurring commitment is broken across the whole compared market. The two halves exist in *different products*: the understanding sits in D1/D2/D3, the control sits in a mandate screen with no insight. Nothing verified connects *"this recurring charge is no longer worth paying"* to *"act on it, here, now."*
> Supporting market-scale symptom `[FACT — reported]`: over 20 million UPI AutoPay mandates are revoked monthly, with insufficient balance the dominant reported cause (NPCI data via Business Standard; not independently confirmed by NPCI). `[PM INFERENCE]` This suggests a meaningful share of recurring commitments may end through payment failure rather than deliberate user action — consistent with what a broken insight→action loop looks like at scale, though it does not on its own prove one.

### Competitive wedge

**Unique capability:** detecting a recurring household commitment worth reviewing from the user's own PhonePe transaction history, and attaching a one-tap action on that flagged commitment inside the same screen as the insight.

**Unmet need:** household money-managers can already *see* that a recurring charge is questionable, but cannot *act* on it where they see it — the most advanced AI insight tool in the market states outright that it cannot transact, while the mechanism that actually stops a charge is a mandate screen with no insight attached.

**Target segment:** mid-career household financial managers, 33–45, tier-1/2.

> **One-line wedge:** A one-tap action on recurring household commitments worth reviewing, surfaced from the user's own transactions, for mid-career household financial managers who can see the pattern today but cannot act on it where they see it.

---

## TASK 3 — OPPORTUNITY GENERATION & RICE PRIORITIZATION

### Five candidate versions of the feature

| ID | Candidate | Scope |
|---|---|---|
| **C1** | Recurring Spend Digest | Insight only — a periodic summary of recurring commitments and how they changed. No action. |
| **C2** | Flagged Commitment + One-Tap Action | One flagged commitment at a time, surfaced as a nudge, with a supported one-tap action available in the same screen. |
| **C3** | Recurring Commitment Manager | A full standing list of every detected commitment, each with variance flags and one-tap act. |
| **C4** | Pre-Debit Intervention | A proactive nudge before a recurring charge executes, with one-tap act. |
| **C5** | Household Multi-Member View | Commitments across multiple family members' accounts. Out of scope — requires other members' transaction data; the brief specifies the user's own transactions. Scored and rejected transparently rather than quietly dropped. |

### Scales declared before scoring — because the Capstone prescribes none

| Input | Scale |
|---|---|
| **Reach** | 1–10 ordinal — share of the primary persona plausibly touched in one quarter. Deliberately not expressed in absolute users: PhonePe publishes no MAU and no category-mix breakdown, so an absolute reach figure would be fabricated precision. |
| **Impact** | Massive 3 · High 2 · Medium 1 · Low 0.5 · Minimal 0.25 |
| **Confidence** | 100% / 80% / 50% — my confidence in the evidence supporting the impact estimate, not confidence that the product will succeed |
| **Effort** | 1–10 relative person-months across design + engineering |

**Formula: RICE = (Reach × Impact × Confidence) ÷ Effort**

### Full arithmetic — every candidate

| ID | Candidate | R | I | C | E | Arithmetic | **RICE** |
|---|---|---|---|---|---|---|---|
| **C2** | Flagged Commitment + One-Tap Action | 7 | 2 | 0.8 | 4 | (7 × 2 × 0.8) ÷ 4 = 11.2 ÷ 4 | **2.800** |
| C1 | Recurring Spend Digest | 9 | 0.5 | 0.8 | 2 | (9 × 0.5 × 0.8) ÷ 2 = 3.6 ÷ 2 | 1.800 |
| C3 | Recurring Commitment Manager | 6 | 3 | 0.5 | 7 | (6 × 3 × 0.5) ÷ 7 = 9 ÷ 7 | 1.286 |
| C4 | Pre-Debit Intervention | 5 | 2 | 0.5 | 5 | (5 × 2 × 0.5) ÷ 5 = 5 ÷ 5 | 1.000 |
| C5 | Household Multi-Member View | 3 | 3 | 0.5 | 10 | (3 × 3 × 0.5) ÷ 10 = 4.5 ÷ 10 | 0.450 |

### Selected feature

## **C2 — Flagged Commitment + One-Tap Action**

**This is the one feature the entire remainder of this project is about.** It wins on the arithmetic (2.800, a 56% margin over the runner-up), it sits directly on the one gap this teardown could evidence, and it stays inside the scope the Capstone defines.

### Guarding against opinion-led and vanity-metric selection

> A senior stakeholder at PhonePe could reasonably push for C3, the full Recurring Commitment Manager — it is the most visible piece of work, it demos impressively, and it carries the highest impact ceiling of any candidate. That preference would be a HIPPO argument rather than an evidence-based one: C3's impact score of 3 is an unevidenced ceiling, its confidence is only 50% because nothing located in this analysis suggests household money-managers will sit down and conduct a commitment audit, and its effort is nearly double the selected candidate's. It scores 1.286 against C2's 2.800, and seniority does not change that arithmetic. Equally, C1, the Recurring Spend Digest, is the vanity-metric temptation: it has the highest reach of any candidate at 9, the lowest effort at 2, and would generate the most impressive top-line numbers — digest opens, insights viewed, feature "engagement". Those are precisely the metrics that would look strongest in a review deck while leaving the actual problem untouched, because the Part C pilot funnel shows the collapse occurring at the action stage, not the insight stage — and the most advanced competitor in this market already proves that insight without action is the market default rather than a differentiator. Optimising for insights-viewed would mean optimising for the number that moves most easily rather than the one that reflects value delivered. The selection therefore follows the RICE framework and build appropriateness: C2 wins on the arithmetic, sits directly on the one gap this teardown could evidence, and stays inside the product scope the Capstone defines.

---

## TASK 4 — AIRTABLE OPPORTUNITY BACKLOG

**Airtable base link (Anyone with the link can view):**

https://airtable.com/appozPM3QfEc0ZJ7V/shrrHyVTT1sIrYcP2

**Table 1 — Personas** (2 records): Persona Name · Segment/Age Range · Willingness-to-Pay Tier · Acquisition Channel · Top Frustration · Top Goal.
Both personas above are populated, each with WTP tier Medium and acquisition channel In-app entry banner on PhonePe (owned surface).

**Table 2 — Opportunity_Backlog** (5 records): Idea · Reach · Impact · Confidence · Effort · RICE Score · Decision.
All five candidates are populated with the exact values in the RICE table above. **C2 is marked "Selected"; C1, C3, C4 and C5 are marked "Not selected".**

---

## TASK 5 — MINI-PRD (PRD-LITE)

### (a) Problem statement

The mid-career household financial manager pays for a growing set of recurring commitments on behalf of several people — subscriptions, services and renewals that debit automatically from their PhonePe account. Each charge is small enough that none is urgent, and because they debit automatically there is no moment that forces a decision. Their frustration is not that they cannot *see* these charges; it is that **noticing a charge and doing something about it are two separate tasks completed in two different places on two different days** — so a commitment that stopped being worth paying for continues being paid for, quietly, indefinitely. The evidence is already sitting in their own transaction history; what is missing is a moment where seeing it and acting on it are the same moment.

### The core product principle — the boundary this feature never crosses

> **Smart Spend Coach does not know that a commitment is wasteful. It identifies transaction patterns that may indicate a commitment is worth reviewing. The user decides whether the commitment is actually unnecessary.**

The feature makes **no** claim about service usage, email activity, merchant-side account status, trial status, objective necessity, or whether a subscription is genuinely unwanted. It cannot know any of those things, and it says so on screen.

**Detection logic:** a base condition — same merchant, regular interval, ≥3 consecutive occurrences — plus at least one trigger: T1 the charge amount has increased against the user's own prior charges, or T2 the charge resumed after a period with none.

### (b) Chosen solution, and one rejected alternative

**Chosen: C2 — Flagged Commitment + One-Tap Action.** One flagged commitment surfaced on the home entry point; tapping it opens an insight detail screen showing the charge history that produced the flag; the action entry sits on that screen and opens a mandatory confirmation before anything changes.

> **On "one tap":** the insight detail screen contains a one-tap action *entry*, which opens a confirmation screen. This is a one-tap action entry, not a claim that the whole financial operation completes from a single tap. The confirmation step is a deliberate safety requirement, not friction to be removed.

**Rejected alternative: C1 — Recurring Spend Digest.**
**Why rejected:** it was the runner-up at 1.800 and scores *higher* on Reach (9 vs 7) and *lower* on Effort (2 vs 4) — it is genuinely cheaper and faster, which is what makes it tempting. It loses on Impact, 0.5 against 2.0, and that single input carries the argument: C1 delivers the half of the job that already works. The problem is not that the household manager cannot *see* a commitment; a digest adds a fourth thing to read and a fifth to remember. `[FACT]` Ask Google Pay is documented as unable to initiate or complete payment transactions — building C1 would mean competing with a Gemini-powered assistant on explanation while declining the one thing it is documented as unable to do. C1 is the strategically weakest candidate precisely because it is the safest.

> **`[DESIGN ASSUMPTION — PLATFORM CAPABILITY NOT VERIFIED]`** The design assumes PhonePe can execute a payer-side auto-debit stop from this flow. This is not established by the Capstone. A documented fallback is retained: a one-tap entry into mandate management with the commitment pre-selected. I have carried this as a stated dependency rather than assuming the capability exists.

### (c) User stories

| ID | Story |
|---|---|
| **US1** | As a household financial manager, I want to be shown a specific recurring charge that has been flagged for review, so that I find out about it without having to go looking through my transaction history. |
| **US2** | As a household financial manager, I want to see the charge history that caused a commitment to be flagged, so that I can judge for myself whether it is worth acting on before I do anything. |
| **US3** | As a household financial manager, I want to start the supported action on a flagged commitment from the screen where I saw it, so that I do not have to find and complete the same action somewhere else later. |
| **US4** | As a household financial manager, I want a clear confirmation of exactly what was stopped and what was not, so that I can act on a flag without worrying I have broken something the household depends on. |
| **US5** | As a household financial manager, I want the feature to tell me when it does not have enough history to judge a charge, so that I am not pushed into acting on the basis of thin evidence. |

### (c continued) INVEST validation — one line per letter, per story

**US1 — Be shown a flagged recurring charge**
- **I** — Fully independent; a flag can be built and tested before any action exists on it.
- **N** — The *what* is fixed; trigger thresholds, card copy, placement and frequency are all open.
- **V** — Valuable as a necessary build increment toward C2. Deliberately not claimed as sufficient standalone — insight-only is exactly what C1 was, and C1 was rejected.
- **E** — Bounded: a recurrence rule plus two triggers over existing transaction data, and one card surface.
- **S** — One detection rule and one card component; fits a single iteration.
- **T** — Given a seeded history meeting the base condition and one trigger, a card either appears with the correct merchant, amount, interval and trigger, or it does not.

**US2 — See the charge history behind the flag**
- **I** — Independent of US3 and US4; buildable against a stubbed flag.
- **N** — Open on presentation: a charge list, a timeline or plain-language explanation are all viable.
- **V** — Standalone value in trust: it converts an unexplained recommendation into a verifiable pattern, which is the mechanism by which judgement stays with the user.
- **E** — A read-only view over data already retrieved for detection; low uncertainty.
- **S** — One screen, no writes, no new data.
- **T** — The charges shown must be exactly those that produced the flag, and no others.

**US3 — Start the supported action where the insight appears**
- **I** — Partially dependent. It needs a flag to act on, but not US2 or US4, and is buildable against a stub — so the dependency is on data rather than another story's implementation. The dependency is recorded rather than removed.
- **N** — Deliberately open: the action may execute in place or enter mandate management. The action *entry* is fixed; the mechanism is not.
- **V** — The highest-value story in this set — it is the differentiator, and the capability a verified competitor is documented as lacking.
- **E** — Estimable only once the platform dependency above is answered. Flagged as a dependency rather than assumed.
- **S** — Small under either option: one action entry plus one confirmation, scoped to one commitment. Bulk action is C3, rejected.
- **T** — The action entry produces a confirmation, and confirming produces a recorded stop on that specific commitment and no other.

**US4 — Confirmation of what was and was not stopped**
- **I** — Independent as a unit of work and testable against a stubbed stopped state; conceptually sequenced after US3. Recorded rather than smoothed over.
- **N** — Open: undo window length, wording, and whether undo lives on the card or a separate screen.
- **V** — Valuable specifically for this persona: household commitments affect other people, so knowing precisely what did and did not change is what makes acting reasonable at all.
- **E** — A state change plus a time-bounded reversal; inherits the same platform dependency as the stop itself.
- **S** — One confirmation state and one reversal path.
- **T** — Sharply testable, and it defines the guardrail metric below: an action confirmed then reversed inside the window is directly countable.

**US5 — Be told when there is not enough history**
- **I** — Fully independent; an alternative output of the same detection rule as US1.
- **N** — Threshold, wording, and whether a low-confidence item is shown at all are open.
- **V** — Protects the judgement principle the whole feature rests on. For someone managing other people's commitments, being pushed into a wrong action is worse than not being told.
- **E** — A threshold check on the existing rule plus one alternative card state.
- **S** — One conditional branch and one screen state — the smallest story in this set.
- **T** — Given a history below the threshold, the low-confidence state must appear and the action entry must be absent.

### (d) Success metrics — precise formulas

**PRIMARY — Insight-to-Action Completion Rate (IACR)**
```
          Number of distinct flagged-commitment insights for which the user
          completes and confirms the supported action within 7 days of first
          viewing that insight
IACR  =  ──────────────────────────────────────────────────────────────────  × 100
          Number of distinct flagged-commitment insights first viewed by users
          during the same measurement period
```
**Unit of analysis:** the insight, not the user. Numerator: insights reaching a *confirmed* state, past the confirmation screen, counted once. Denominator: insights first viewed in the period — surfaced-but-never-viewed insights are excluded, because this measures the insight→action gap and not delivery. Low-confidence items are excluded, since no action is offered on them. Window: 7 days from first view, reported as a rolling weekly figure. *(The 7-day window follows the Capstone's own worked example of a precise metric.)*
**Why this metric:** `[FACT]` Ask Google Pay is documented as unable to initiate or complete payment transactions — so the value Smart Spend Coach claims is not that the user is *informed* but that the user *finishes*. IACR is the metric that fails when the feature explains beautifully and changes nothing. No baseline or target is proposed; setting one before measurement would be an invented number.

**GUARDRAIL — Action Reversal Rate (ARR)**
```
          Number of confirmed actions that the user reverses (in-flow undo, or
          re-authorising the same commitment) within 14 days of confirmation
ARR   =  ──────────────────────────────────────────────────────────────────  × 100
          Total number of confirmed actions in the same period
```
**Window:** 14 days — longer than the primary window because regret on a recurring commitment typically surfaces at the next billing cycle rather than immediately.
**Why this metric:** the primary metric rewards getting users to act; unguarded, that incentive rewards pushing users into stopping commitments they needed — especially serious for someone whose commitments affect other people. ARR is the direct test of the judgement principle: if the product genuinely leaves the decision with the user, reversals should be rare.

### (e) Two edge cases

**Edge Case 1 — Fewer than three occurrences / insufficient history.**
The pattern does not meet the base condition. Behaviour: the item is shown as low confidence with the charges observed so far, in plain language — *"That's not enough history for Smart Spend Coach to flag it for review"* and *"We are not saying this charge is fine, and we are not saying it is a problem. We do not have enough to say either."* No flag-for-review claim is made, no action entry is offered, and the item does not enter the IACR denominator — it is not an actionable insight.

**Edge Case 2 — The user opts out of transaction analysis mid-month.**
**Behaviour:** detection stops immediately; no new flags are generated; commitments already flagged are no longer surfaced. Any action the user already confirmed remains in effect and remains reversible — opting out of analysis does not silently re-start a payment the user chose to stop. The feature states what has stopped, rather than degrading quietly.

### (f) Out of scope for this version

> **Out of scope: any view of, or action on, transactions belonging to another household member's account.** Smart Spend Coach operates exclusively on the user's own PhonePe transaction history — that is what C5 was rejected for, and it is not smuggled back in through this version.

---
---

```{=openxml}
<w:p><w:r><w:br w:type="page"/></w:r></w:p>
```

# PART B — PROTOTYPE, USABILITY VALIDATION & PRICING

## TASK 1 — FIGMA PROTOTYPE

**Figma prototype link (Anyone with the link can view):**

https://www.figma.com/proto/XhV4JoExaeeygvEG1LZGez/PhonePe-Smart-Spend-Coach-%E2%80%94-Capstone-Prototype?node-id=4-38&t=Nw77AZhLZGNvFuHc-1&scaling=min-zoom&content-scaling=fixed&page-id=0%3A1&starting-point-node-id=2%3A2

The prototype implements the C2 feature and the PRD above — the same persona, the same feature, the same metrics. No new idea is introduced.

**Five screens at 390 × 844** (four required):

**(a) Home-screen entry point.** The Smart Spend Coach surface where the insight first appears. Carries an on-screen *"PROTOTYPE — illustrative data, not real user transactions"* banner, one Nudge Card instance (merchant, ₹ amount, interval, the observed signal, and a "Review this charge →" CTA), plus a second, low-confidence entry that leads to the edge-case screen.

**(b) Insight detail screen.** Merchant summary, a "WHAT WE OBSERVED" block listing six dated charges with the increase marked, a separate "WHY YOU'RE SEEING THIS" block naming the trigger that fired, the explicit limitation *"Smart Spend Coach does not know whether you still use this service. It only sees your payments,"* the line *"You decide whether this commitment is worth keeping,"* then the one-tap action entry and a "Keep this charge" alternative.

**(c) One-tap action-confirmation screen.** A bottom-sheet modal stating WHAT WILL STOP (from the next due date) and WHAT WILL NOT CHANGE, carrying the limitation verbatim: *"Stopping future auto-debits prevents PhonePe from making further payments to this merchant. It does not cancel your account or subscription with the merchant."* Confirm, plus a safe exit.

**(d) Edge-case screen.** Implements Edge Case 1 from the PRD: a low-confidence chip, the two observed charges, *"That's not enough history for Smart Spend Coach to flag it for review,"* and *"We are not saying this charge is fine, and we are not saying it is a problem."* No action entry is offered in this state, and the screen says so.

**(e) Home — acted-on state.** The state after confirmation, showing what changed and offering Undo.

**Component:** a "Nudge Card" component set, carrying a written component description recording that the card never asserts a commitment is wasteful.
**Variants:** State = Default (flagged for review, observed signal, review CTA) and State = Acted-on (auto-debits stopped, undo available).
**Interactions:** 11 navigation interactions against a required minimum of 3 — all tap-triggered navigate-to actions, and every visible control on every screen is wired, so there are no dead ends and no unresponsive taps: home→insight, home→edge case, insight→home (back), insight→confirmation, insight→home (keep charge), confirmation→acted-on (confirm), confirmation→insight (safe exit), edge case→home (back), edge case→home (view history), edge case→home (remind me if this repeats), acted-on→home (undo, implementing US4).

> **A prototype revision made during QA.** a change-to-variant shortcut was built during prototyping that allowed a single tap to flip the card to its acted-on state without passing through the confirmation screen. It was removed, because it contradicted the User Control commitment in Task 4 and the mandatory confirmation in the PRD. The prototype is deliberately one interaction "less impressive" as a result.

---

## TASK 2 — AI CLASSIFICATION & BIGGEST RISK

### Classification: **AI-AUGMENTED**

> Smart Spend Coach is AI-augmented, not AI-native. Its detection logic is deterministic: a recurring charge is identified by matching merchant, interval and at least three consecutive occurrences, and it is flagged for review only when the amount has increased against the user's own previous charges or has resumed after a gap — all arithmetic over the user's own transaction history, requiring no model. Remove the AI layer entirely and the feature still detects the commitment, still shows the charge history as evidence, and still offers the one-tap action; what degrades is the *presentation* — raw merchant descriptors instead of recognisable names, weaker discretionary-versus-essential classification, and templated rather than personalised nudge copy. Because the core value chain of observe → evidence → act survives without the model and only the explanation layer depends on it, this is AI enhancing an experience that already works rather than AI constituting it.

**Why not AI-native:** it would be easy — and wrong — to classify this AI-native because the brief calls it *"an AI-powered feature."* AI-powered and AI-native are not the same claim. The test the Capstone actually sets is *how much of the experience stops functioning without the AI layer*, and here the answer is: the polish, not the function.

`[PM DESIGN ASSUMPTION]` The components where a model is plausibly used are merchant normalisation, discretionary-vs-essential category classification, and nudge copy generation. No model, provider, API or architecture is named anywhere, because none is specified by the brief.

> A consequence of a mid-project correction: an earlier PRD draft had detection depending on a "usage signal" — knowing whether a service was still being used. PhonePe has no such capability; I had invented it, and I removed it. That removal left detection deterministic, which is what makes this feature AI-augmented rather than AI-native. The classification follows from the correction.

### Single biggest AI risk: **HALLUCINATION RATE**

> Hallucination rate is the single biggest AI risk for Smart Spend Coach, because the AI layer's only real job in this feature is explanation. Detection is deterministic, so the arithmetic that decides *whether* to flag a charge cannot hallucinate; what the model produces is the sentence telling the user *why*. If that sentence asserts something the transaction data does not support — that the service is unused, that a trial has ended, that a commitment is unnecessary — it does not merely mislead, it **breaks the feature's core principle** that the system reports observed patterns and the user decides. Worse, the design safeguard that protects against inaccuracy does not protect against this: the insight screen shows the charge history so a user can verify a *pattern*, but a fabricated *explanation* appears alongside that true data with identical authority, giving the user nothing to check it against. For a household financial manager acting on commitments that affect other people, a confident false explanation is the failure most likely to produce an irreversible wrong action and a permanent loss of trust.

*(Exactly one dimension is named, as required. Accuracy is the serious alternative — it is what the ARR guardrail measures — but deterministic detection structurally lowers it and the on-screen evidence already mitigates it.)*

---

## TASK 3 — USABILITY VALIDATION

### Method

**Real-user testing with 7 distinct people.** Each session ran the Figma prototype in Present mode on my own device, with a single non-leading instruction — *"Please look at this screen and tell me what you would do"* — and no explanation of what the feature does. No tester was asked for real transaction history, bank credentials, PhonePe credentials or any private financial information at any point.

> **Three evidence sets were kept strictly separate throughout this project and are never merged:** (A) real tester evidence — the only set reported below; (B) my own designer self-walkthrough as each persona; (C) an independent heuristic/cognitive review of the prototype. Only Set A appears in the findings, the counts, or the severity ratings. Neither B nor C is presented as user evidence anywhere.

### Observations recorded

**10 observations recorded, against a required minimum of 6.** Observation IDs are records of a recurring pattern, not one per tester — individual attribution was not retained, and I have not split an aggregate into seven invented session histories.

| ID | Category | Screen / Flow | Observation | Priority |
|---|---|---|---|---|
| OBS-01 | **Success** | Home entry | First noticed the ₹499 StreamCo Premium card | Low |
| OBS-02 | **Success** | Home → insight | Tapped "Review this charge →" immediately | Low |
| OBS-03 | **Hesitation** | Insight detail | Searched for approximately 12 seconds before locating the action entry | **MEDIUM** |
| OBS-04 | Hesitation + Quote | Insight → action | Asked a question about what the action would do — verbatim: "Is this cancelling the subscription?" | **MEDIUM** |
| OBS-05 | **Success** | Insight → confirmation | Eventually tapped the action | Low |
| OBS-06 | **Success** | Confirmation | Confirmation screen reported as understood *(behavioural basis not recorded)* | Low |
| OBS-07 | **Success** | Full flow | Completed the flow | Low |
| OBS-08 | **Success** *(aggregate)* | Overall | All 7 users were able to use the prototype | Low |
| OBS-09 | **Success** *(aggregate)* | Overall | Overall feedback was generally positive; testers considered the design fine | Low |
| OBS-10 | *(negative finding)* | Overall | No task-blocking failure was reported | Low |

**Note-type coverage: Errors 0 · Hesitations 2 · Successes 7 · Quotes 1.**

Every observation carries a priority. The severity guide grades *friction* — High blocks task completion for multiple users, Medium causes hesitation that is recovered from, Low is minor or isolated. Observations recording successful completion contain no friction and are therefore recorded at the lowest band, Low. The two Medium ratings are the only observations describing friction.

> **No error was reported or retained in the supplied session record.** The approximately 12-second search is recorded as a hesitation, and the clarifying question is recorded as a hesitation with verbalisation. Neither is being reclassified as an error to fill the required category.

### Findings and severity

**Severity guide applied:** High = blocks task completion for multiple users · Medium = causes hesitation but is recovered from · Low = minor or isolated.

**F-01 · Action-entry discoverability — MEDIUM.** Screen: insight detail. Evidence: OBS-03, ≈12-second search.
*Interpretation, kept separate from the observation:* the action entry sits within the visible screen area, but sixth in a vertical stack beneath three dense content cards. The control therefore has to be found by scanning rather than seen immediately. This is a *finding-the-control* problem, not an *understanding-the-content* problem, and not a reach problem.
*Not High* — no blocked completion was reported. *Not Low* — it recurred and sits directly on the insight→action path.

**F-02 · Action-semantics ambiguity — MEDIUM.** Screen: insight → action. Evidence: OBS-04, *"Is this cancelling the subscription?"*
*Interpretation:* suggests ambiguity between stopping future PhonePe auto-debits and cancelling the underlying merchant subscription — precisely the distinction the product's boundary rests on.
*Not High* — the flow was completed. *Not Low* — it touches the core boundary, and it is the exact failure mode the ARR guardrail exists to detect.

**F-03 · Home-entry comprehension — positive finding, no defect.** Evidence: OBS-01, OBS-02.

### High-priority insight-to-action friction: finding

> **No High-priority insight→action friction was observed in this testing.**
>
> Seven real users tested the prototype. No blocked task completion was reported. Two MEDIUM insight→action frictions were observed, but under the severity guide — High = blocks task completion for multiple users — the evidence does not justify a High classification.

The finding is reported at its observed severity rather than reclassified to satisfy the requirement. A manufactured High finding would have propagated directly into the Part C experiment design, which is built on observed friction; a fabricated observation at this point would corrupt everything downstream of it. Part C therefore targets F-01, the strongest observed finding, and says so explicitly.

---

## TASK 4 — ETHICS, BIAS & SAFETY

### Five principles — each naming a concrete design choice

**Transparency.** Smart Spend Coach shows the user the evidence before the conclusion: the insight detail screen carries a "WHAT WE OBSERVED" block listing the six dated charges that triggered the flag, and a separate "WHY YOU'RE SEEING THIS" block naming the specific rule that fired, so the user can check the reasoning rather than being asked to trust a verdict.

**User Control.** No auto-debit is ever stopped by a single tap: the action entry opens a mandatory confirmation sheet stating exactly what will stop and what will not change, offering "Go back" as an equal exit, and after confirmation the home screen carries an Undo control on the acted-on card — so the user confirms deliberately and can reverse the decision afterwards.

**Privacy-by-Design.** Detection reads only the user's own PhonePe transaction record (merchant, amount, date, interval), and the product states this limitation to the user on the insight screen itself: *"Smart Spend Coach does not know whether you still use this service. It only sees your payments"* — an on-screen commitment that no email, app-usage, merchant-side or third-party source is used.

**Fairness.** A commitment is only flagged after at least three consecutive occurrences at a regular interval, and a pattern that does not clear that evidence bar receives no stop action at all — it is shown as low-confidence — so users with short or sparse PhonePe histories are not pushed toward acting on weak evidence that would be treated as strong for a heavier user.

**Graceful Failure.** When the system has insufficient history it says so in plain language and declines to draw a conclusion in either direction — *"We are not saying this charge is fine, and we are not saying it is a problem. We do not have enough to say either"* — rather than hiding the item or guessing a verdict from thin data.

### Bias type: **MEASUREMENT BIAS**

> Smart Spend Coach is exposed to measurement bias: the thing it can measure is not the thing it actually cares about. The construct that matters to the user is *"this commitment is no longer worth paying for"* — but nothing in a transaction record contains that. What the feature can observe is a proxy: a charge that recurs at a regular interval, whose amount has increased against the user's own prior charges, or which resumed after a gap. Tuning the feature on existing transaction data risks quietly treating that proxy as if it were the construct, so that a price rise on a service the household uses every day scores identically to a price rise on a service nobody has opened in a year — the data cannot distinguish them, because usage is not in the data. The bias is compounded by which transactions are visible at all: a commitment paid through PhonePe is measurable, while the same household's commitments paid by card, net-banking or another app are invisible, so the feature's picture of a user's recurring spend is systematically partial in a direction it cannot detect. The concrete harm is that the flag reads as a judgement about *worth* when it is only a measurement of *pattern*, and a user who trusts it as the former may stop a commitment they needed.

**Why this one and not the other three:** representation bias is real but bites hardest on models that generalise across people — this feature judges every user against their own history. Aggregation bias needs a pooled model; the detection rule is applied per user. Evaluation bias needs a benchmark, and there is none — naming it would mean inventing an evaluation set that does not exist. Measurement bias is the one the project has already acted on: the invented "usage signal" was removed precisely because it pretended to close the proxy-to-construct gap.

---

## TASK 5 — PRICING & PACKAGING

### Decision 1: **FREEMIUM**, not free-trial

**The reason is structural to this feature.** Detection requires at least three consecutive occurrences before a commitment can be flagged. For a monthly commitment that is roughly three months of history before the first flag can exist. A 7-, 14- or 30-day free trial therefore expires before the evidence threshold that makes the product work has been met — the user would experience the trial as an empty screen and correctly conclude the feature did nothing. Freemium has no such expiry: the free tier accumulates history quietly and produces its first genuine flag whenever the pattern actually matures, which is the only moment the product can prove anything.

**Reinforcing:** the primary segmentation factor is Expected Retention — the persona was chosen because the need is permanent and recurs. A pricing model whose entire mechanism is a countdown to expiry is misaligned with a segmentation decision made on sustained repeat use. Freemium and retention-first segmentation are the same bet. And with both personas at Medium WTP `[HYPOTHESIS]`, freemium degrades gracefully if the true figure is lower — the free tier still delivers — whereas a trial-and-paywall model fails hard at exactly the moment the trial ends.

### Decision 2: Packaging shape — **TIERED**

**Usage-based is actively wrong here.** Charging per action taken would put a price on exactly the behaviour the primary metric measures — the product would be charging for the thing it exists to produce. Charging per insight surfaced would create an incentive to over-flag, which is the failure the ARR guardrail exists to detect; a pricing model must not be structurally opposed to the guardrail metric of the same feature. And the product's honest value is not volume: a good month may produce zero flags because nothing warranted review — usage-based pricing would make the product's best outcome its lowest-revenue outcome. Hybrid inherits every one of these objections through its usage component.

**Tiered** separates on capability rather than on quantity of financial activity: Free carries the honest core — detection, the full charge-history evidence, the one-tap action, confirmation and undo — and a Paid tier adds breadth and continuity (longer history depth for detection; proactive notification ahead of an upcoming flagged charge rather than in-app discovery only).

> **No price point is stated, deliberately.** `[NOT VERIFIED]` No willingness-to-pay data for this category in India was located — this is a recorded research gap, not an oversight. Naming a rupee figure would be exactly the kind of fabricated precision the brief warns against elsewhere. The method is stated instead: a price-sensitivity study on the primary persona against the specific free/paid split above, run before any price is committed.

### Pricing trap explicitly avoided: **COST-PLUS**

Smart Spend Coach's marginal cost per user is close to trivial — detection is deterministic arithmetic over data the platform already holds, and the only variable cost is the model call generating the explanation sentence, which the Part C tiering optimisation reduces further. Pricing from that cost base would produce a number near zero and would say nothing about what the feature is worth to a household that stops a ₹499 monthly charge it no longer wants. This feature is *most* exposed to cost-plus precisely because its costs are so low that the number feels defensible. The free/paid split above is drawn on user value, and the price is deferred to research rather than derived from cost.

**Also avoided: competitive pricing.** The nearest comparators are bundled and free — Ask Google Pay ships inside Google Pay at no separate charge, and CRED Money was stated as not monetised at launch. Anchoring to them would set the price at zero by imitation. Naming a competitor's price is not a valuation.

**No decoy tier is used.** A decoy would require three invented price points with no WTP data behind any of them, and it is a deliberate choice-architecture nudge toward a tier the user might not otherwise pick — which would contradict the User Control and Transparency commitments made one section above. It is optional, so declining it costs nothing.

---
---

```{=openxml}
<w:p><w:r><w:br w:type="page"/></w:r></w:p>
```

# PART C — GROWTH FUNNEL, EXPERIMENT DESIGN & AI EVALUATION

## TASK 1 — FUNNEL DIAGNOSIS

### The pilot funnel `[CASE DATA]`

| # | Stage | Users |
|---|---|---|
| 1 | Entry banner shown | 40,000 |
| 2 | Feature opened | 16,000 |
| 3 | Onboarding / transaction-linking completed | 11,200 |
| 4 | First personalised insight viewed | 9,520 |
| 5 | Recommended action taken | 2,856 |

### The four transitions — arithmetic shown

| Transition | Converted | Dropped | Users lost |
|---|---|---|---|
| **1 → 2** | 16,000 ÷ 40,000 = **40.0%** | **60.0%** | 40,000 − 16,000 = **24,000** |
| **2 → 3** | 11,200 ÷ 16,000 = **70.0%** | **30.0%** | 16,000 − 11,200 = **4,800** |
| **3 → 4** | 9,520 ÷ 11,200 = **85.0%** | **15.0%** | 11,200 − 9,520 = **1,680** |
| **4 → 5** | 2,856 ÷ 9,520 = **30.0%** | **70.0%** | 9,520 − 2,856 = **6,664** |

End-to-end: 2,856 ÷ 40,000 = **7.14%**.

### The two required reports — and they are different stages

> **Largest ABSOLUTE number of users lost: Stage 1 → 2 — 24,000 users.**
> **Largest PERCENTAGE drop-off: Stage 4 → 5 — 70.0%.**

**Why the two measures disagree:** Stage 1→2 loses more people in absolute terms because it operates on the largest population in the funnel — 60% of 40,000 exceeds 70% of 9,520, even though it is a *smaller proportion*. Stage 4→5 is the harshest transition proportionally, destroying seven of every ten users who reach it, but it only ever gets 9,520 users to work with. **Absolute loss depends on the drop rate *and* the size of the pool; percentage drop depends on the rate alone.** The two rankings can only agree when the pools are equal, and here they differ by more than fourfold.

> **Stage 4→5 is not merely a funnel stage — it *is* the primary success metric defined in Part A.** IACR = confirmed actions ÷ insights first viewed. Stage 4→5 = 2,856 ÷ 9,520 = **30.0%**. The metric chosen before this funnel was analysed lands exactly on the stage identified as the priority.

## TASK 2 — PRIORITIZATION

### Fix **Stage 4 → 5** first.

**The intent-proximity principle, stated and applied:** prioritise drop-offs closer to the final action, because user intent is highest there — a user further down the funnel has demonstrated more of the intent the product depends on, so recovering them is both more valuable per user and more achievable. You are removing an obstacle in front of someone already trying to get through, rather than manufacturing motivation in someone who has shown none.

A user at Stage 4 has done everything the product asked: saw the banner, opened the feature, granted transaction-linking permission — a real privacy decision, not a click — and read a personalised insight about their own money. Every step is a revealed signal of intent. Then 70% of them stop. That is not an intent problem; these users wanted the outcome and did not complete it, which by definition makes it a friction problem — and friction is what product design can actually fix.

### Why Stage 1→2 is lower priority *despite losing 24,000 users* — more than three times as many

1. **Those 24,000 never demonstrated any intent.** Stage 1 is a banner impression on an owned surface; users did not seek the feature, it appeared while they were mid-payment. A 40% open rate on an unsolicited in-app banner is a discovery outcome, not a rejection of the value proposition.
2. **The ceiling on recovery is lower.** Improving a banner means copy, placement and timing, heavily constrained by the surrounding payment experience. Improving an in-feature flow the user is already engaged with has a far larger design surface.
3. **The compounding argument runs opposite to the intuition.** A user recovered at Stage 1 must still survive Stages 2, 3 and 4. At the pilot's own rates, an extra user at Stage 1 converts to a completed action at 0.700 × 0.850 × 0.300 = 17.85%. A user recovered at Stage 4→5 converts at 100% — completing that stage *is* the action.
> **One user recovered at the last stage is worth 1 ÷ 0.1785 ≈ 5.6 users recovered at the first.**
4. **Stage 4→5 is where the product's actual claim lives.** The wedge is that the user can *finish* — `[FACT]` Ask Google Pay is documented as unable to transact. A funnel that surfaces insights well and converts them 30% of the time is failing at the specific thing that differentiates it. Stage 1 failing is a marketing outcome; Stage 4→5 failing is the product being wrong.
5. **It is where our usability evidence sits.** Both observed frictions (F-01, F-02) occur between viewing the insight and completing the action — Stage 4→5 exactly. We have evidence for this stage and none for Stage 1→2.

**Stage 1→2 is not dismissed.** It is a real 24,000-user loss deserving a separate workstream. It is second because each recovered user is worth roughly a fifth as much, and because we have no evidence about *why* those users did not open.

## TASK 3 — A/B EXPERIMENT

### The specific Part B observation this addresses

**Finding F-01 — action-entry discoverability**, evidenced by OBS-03: *"Searched for approximately 12 seconds before locating the action entry"* — insight detail screen, real-user testing with 7 testers, severity MEDIUM.

> No High-priority insight→action observation occurred in testing (Part B Task 3). This experiment is built on the strongest MEDIUM finding rather than on a High finding that did not exist. F-01 is nonetheless the correct target: it is a real, observed, insight→action friction, it lands on the prioritised funnel stage, and it is directly measurable. F-02 (*"Is this cancelling the subscription?"*) is a strong candidate for a second experiment and is not discarded.

### The change

**Control (A):** the insight detail screen as built — merchant summary → six-charge history → why-you're-seeing-this → limitation → action entry below the evidence block.
**Variant (B):** identical content and identical copy, with the action entry as a persistent action bar pinned to the bottom of the viewport and visually separated from the content stack, so it reads as the screen's primary action on open rather than as the sixth element in a vertical sequence.

**Only one variable changes: the position and persistence of the action control.** All copy, all evidence, the limitation sentence, the confirmation sheet and the undo path are identical across arms, so any IACR difference is attributable to discoverability, not persuasion. The confirmation gate is present in both arms — the variant makes the action easier to *find*, never easier to take by accident.

### Hypothesis

> **We believe that** pinning the recommended action to the bottom of the insight detail screen as a visually separated action bar, rather than placing it sixth in a vertical stack beneath three dense content cards, will result in an increase in the percentage of first-viewed flagged-commitment insights that reach a confirmed action within 7 days, and a reduction in the median time from first insight view to confirmed action, because in real-user testing of the current design testers searched approximately 12 seconds before locating the action entry (finding F-01, observation OBS-03) even though that control was already within the visible screen area, which points to a salience problem rather than a reach problem, and the pilot funnel shows that 70% of users who view a personalised insight never complete the recommended action — indicating the loss is at the point of acting, not the point of understanding. We will measure Insight-to-Action Completion Rate (IACR).

### Metric Triad — precise formulas

**PRIMARY — IACR**
```
IACR = (distinct flagged-commitment insights reaching a confirmed action within
        7 days of first view) ÷ (distinct flagged-commitment insights first viewed
        in the same period) × 100
```
Unit of analysis: the insight. Low-confidence items excluded. **Pilot baseline from the supplied funnel: 2,856 ÷ 9,520 = 30.0%.**

**SECONDARY — Median Time-to-Action (TTA)**
```
TTA = median, across all confirmed actions in the period, of
      (timestamp of action confirmation − timestamp of first view of that insight),
      in seconds
```
**Why this and not a generic engagement count:** it measures the exact mechanism the hypothesis proposes. If the bar works by making the control easier to find, TTA must fall. If IACR rises but TTA does not, the improvement came from something else and our causal story is wrong — this is the metric that can falsify our own explanation.

**GUARDRAIL — ARR**
```
ARR = (confirmed actions reversed within 14 days of confirmation)
      ÷ (total confirmed actions in the period) × 100
```
**Why this guardrail for this change:** the intervention makes an irreversible-feeling financial action easier to reach. The harm it could cause is users acting before reading the evidence above it. If ARR in the variant rises materially above control, the variant is rejected even if IACR improves — a conversion win bought with regretted financial actions is a loss. The threshold is set from control-arm data and fixed before the arms are compared. `[NOT VERIFIED — no ARR baseline exists yet]`

### Duration: **21 days — 14 days of enrolment plus a 7-day attribution tail**

1. **IACR attributes up to 7 days after first view.** An insight first viewed on the last enrolment day has a window closing 7 days later; ending at day 14 would systematically under-count late-enrolled insights — a censoring error, not noise.
2. **≥1 full 7-day behaviour cycle is required and comfortably met:** 14 days of enrolment spans two complete weekly cycles, so weekday/weekend differences in when users open PhonePe are represented in both arms. A 7-day-only enrolment would expose one arm to a single weekend.
3. **Not longer**, because extending enrolment buys precision at the cost of delaying a decision on a change that is cheap to ship and cheap to revert.
4. **The guardrail matures later than the primary metric.** ARR has a 14-day window and the last confirmed action can occur on day 21, so ARR cannot be fully read until day 35. The day-21 primary readout is therefore provisional; the ship decision waits for the guardrail. Declaring a winner on IACR alone at day 21 would mean shipping a conversion gain before the safety metric governing it has matured.

### Pitfall and precaution

**Pitfall: EARLY JUDGMENT ERROR.**
Both decision metrics are lagging by construction — IACR over 7 days, ARR over 14. Early results are therefore not merely noisy but systematically biased downward: on day 3, most enrolled insights have not had time to convert and almost no confirmed action has had time to be reversed. A day-3 dashboard would show a low IACR and a near-zero ARR in both arms — and the near-zero ARR is the dangerous number, because it would look like proof the change is safe at exactly the moment when no reversal *could* yet have been recorded. The temptation to call the test early is strongest precisely when the guardrail is structurally incapable of firing.

*(Novelty Effect is the runner-up and is not zero risk; it is not chosen because the change is a permanent structural repositioning rather than a new stimulus, and the two-cycle enrolment gives short-lived attention effects time to decay. Local Maxima Trap applies to a long series of small optimisations, not a first test. HARKing is structurally excluded — this hypothesis was written before the test, from a pre-existing observation.)*

**Precaution: pre-register the readout schedule and the decision rule before enrolment opens, and take no unblinded look at either arm before day 21.** The analysis plan is fixed in advance — primary readout day 21, guardrail readout day 35, ARR rejection threshold set from control-arm data only. Operational health checks during the run are permitted and are restricted to metrics that are not the decision metrics, so monitoring the test cannot become judging it.

## TASK 4 — GROWTH LOOP: **CONTENT**

> Smart Spend Coach's primary persona — the mid-career household financial manager, 33–45 — is reached today through exactly one route: the in-app entry banner on PhonePe, an owned surface. That channel is why acquisition cost is Low, and it is also why the funnel starts where it does: 40,000 impressions produced 16,000 opens, meaning the ceiling on reach is *whoever happens to already be inside PhonePe when the banner fires.* A content loop is the only one of the three options that raises that ceiling without abandoning the economics that make the channel attractive: people in this persona are already searching for how to stop a recurring charge they have noticed on a statement, and search-discoverable material answering that question brings in users actively looking for the outcome the feature delivers — a higher-intent entry than an unsolicited banner, which matters given that 60% of banner impressions never convert to an open. It also fits a willingness to pay assessed as Medium, and honestly as a hypothesis rather than a finding `[HYPOTHESIS — no India-specific WTP data for this category was located]`: a Medium-WTP user must be convinced of value before being asked to pay, and content does that convincing before the user reaches the product — the same reasoning that made freemium rather than free-trial the right call in Part B. The loop closes because the feature's own operation generates the raw material: the aggregate, non-identifying patterns of what kinds of recurring commitments users review and stop become the next piece of content, discovered by the next cohort. One hard constraint: any such content may only ever use aggregate, non-identifying statistics — publishing anything traceable to an individual's transactions would contradict the Privacy-by-Design commitment stated on the product's own insight screen, and would be a scope violation, not a growth tactic.

**Why not Paid:** it contradicts the acquisition economics of the locked persona. CAC is Low because distribution is owned with no paid media; buying users for a feature whose WTP is an unevidenced Medium means spending certain money for uncertain revenue — and it does not compound, because the loop stops when the spend stops.
**Why not Virality:** the only thing a user could share is their own recurring financial commitments. Sharing is structurally at odds with both the data scope and the Privacy-by-Design principle stated on the insight screen. Rejecting virality here is a consequence of the ethics position taken in Part B Task 4, not an independent judgement.

## TASK 5 — AI EVALUATION, COST & DASHBOARD

### Two of the five monitoring dimensions: SAFETY and QUALITY

> **These are deliberately not Part B's four-dimension risk list restated.** Part B Task 2 asked *what is the single biggest risk in this feature* and answered hallucination rate. This is a different question — *what do we watch every week once it is running* — under a different, broader framework. I have specifically not chosen *accuracy* or *cost*, the two members whose names overlap with the Part B list, so that this answer cannot be mistaken for the earlier one.

**SAFETY.** Monitored weekly as a fixed-size random sample of generated insight explanations shown to users that week, each checked against the transaction record that produced it and marked as a boundary violation if it asserts anything the data cannot support — most specifically the three claims the product does not have: that a service is unused, that a trial has ended, or that a commitment is unnecessary. Output: a weekly boundary-violation rate, with every violation retained verbatim.
*Why weekly:* this is the failure with the highest consequence and the lowest chance of being caught by any other signal. An inaccurate flag is visible to the user, who can check the charge history and disagree. A fabricated *explanation* sits beside true data with identical authority — the user has nothing to check it against. It is the one failure mode where the product's own design safeguards do not protect the user, which is why it needs a human in the loop rather than a threshold alert.

**QUALITY.** Monitored weekly as IACR paired with ARR on the same time base (are users acting on what we surface, and are they regretting it?), plus the sampled explanations rated for whether the stated reason matches the rule that actually fired.
*Why weekly:* quality for this feature is not fluency, it is earned action — an explanation is high quality only when it moves a user to a decision they do not reverse. IACR alone can be gamed by more assertive copy; ARR alone can be minimised by surfacing nothing. Only the pair describes quality — and the pair is already instrumented, so this dimension needs no new measurement infrastructure.

*(Cost is a margin risk rather than a user-harm risk and moves predictably with volume — monthly review suffices. Accuracy is structurally constrained already, because deterministic detection means the arithmetic deciding whether to flag cannot drift week to week. Operational efficiency is the strongest of the three rejected, but is second-order until safety and quality are stable.)*

### One concrete token-cost optimisation: **trigger-keyed model tiering**

Because detection is deterministic, the system already knows — **with no model call at all** — exactly which rule fired before any explanation is generated. That routing signal is free, and it is what makes tiering possible:

- **T1 alone** (single merchant, clean normalisation, amount increased): served by a fixed template populated from the transaction record. The explanation has exactly one shape — *"This charge has gone up from ₹X to ₹Y since [date]."* Paying model tokens to reproduce a fixed sentence is pure waste — and a template cannot hallucinate, which reduces the safety-review load at the same time.
- **T2 alone** (resumed after a gap, unambiguous): cheap model tier.
- **Both triggers, ambiguous merchant normalisation, or an unusual interval:** stronger model tier — the minority of cases where model quality is genuinely load-bearing.

**Why this technique for this feature specifically:** the expensive layer is already small, because deterministic detection means only *flagged* items reach a model at all, and the low-confidence edge case suppresses items before that point. Tiering compounds those existing reductions — and the cost saving and the safety improvement come from the same change, since every insight moved onto the template path is one that cannot fabricate an explanation.

### 5-3-1 Dashboard

**1 CORE INSIGHT METRIC — Insight-to-Action Completion Rate (IACR).** Confirmed actions on flagged-commitment insights ÷ flagged-commitment insights first viewed, within 7 days of first view, × 100.
*Why this one:* it is the only number that fails when the feature explains beautifully and changes nothing — which is exactly what the pilot funnel shows happening at 30.0%.

**5 SUPPORTING KPIs**

| # | KPI | Formula | What it adds beyond IACR |
|---|---|---|---|
| 1 | Action Reversal Rate | confirmed actions reversed within 14 days ÷ confirmed actions × 100 | Whether the actions we drove were *wanted*. The one KPI that can veto a rise in the core metric |
| 2 | Median Time-to-Action | median (confirmation timestamp − first-view timestamp) across confirmed actions, seconds | Whether the path is *findable*. Directly tracks F-01 and the ≈12-second observation |
| 3 | Insight View Rate | insights first viewed ÷ insights surfaced × 100 | Separates a delivery problem from an action problem — if IACR falls and this falls too, the issue is upstream |
| 4 | Low-Confidence Suppression Rate | patterns detected but withheld under the edge-case rule ÷ all patterns detected × 100 | Whether the honesty rule is calibrated. Near zero means the evidence bar does nothing; very high means thin-history users see an empty product |
| 5 | Explanation Grounding Pass Rate | sampled explanations with no claim unsupported by the transaction record ÷ sampled explanations × 100 | The weekly safety number — the operational descendant of the hallucination risk named in Part B |

**3 VISUALIZATIONS**

**V1 · Insight→action funnel, split by trigger type.** The five pilot stages as a funnel with the 4→5 transition emphasised, each bar split into T1 (amount-increased) and T2 (resumed-after-gap) segments. *Purpose:* to reveal whether one detection trigger converts materially worse than the other — if T2 insights are viewed as often but acted on far less, the problem is the trigger's persuasiveness, not the screen. No aggregate funnel can produce that diagnosis.

**V2 · Weekly IACR with ARR on a shared time axis.** A dual-axis weekly line chart, deliberately on the same time base rather than in separate tiles. *Purpose:* to make one pattern impossible to miss — IACR rising while ARR rises with it. That divergence is the signature of the product pushing users into actions they regret, and it is invisible when the two metrics live on separate dashboard tiles. This chart exists to catch our own primary metric being gamed.

**V3 · Time-to-action distribution histogram.** Seconds from first insight view to confirmed action, bucketed (0–5s, 5–10s, 10–20s, 20–60s, >60s, plus a "viewed, never acted" column), with a marked reference line at the ≈12 seconds observed in real-user testing. *Purpose:* the A/B test predicts this distribution shifts left, and the median alone hides *how*. A genuine discoverability fix should thin the long right tail and grow the 0–5s bucket, whereas a mere persuasion effect would move the mass without changing the shape. This is the chart that tests our explanation, not just our outcome.

---

## TOOL ACCESS AND COST STATEMENT

Every tool used in this project has a free path, and no paid API key, developer account or account-gated service was required at any point. The prototype was built in Figma on the free Starter plan, which supports the single file, five screens, component, variant and prototype interactions used here. The persona and opportunity-backlog tables were built in Airtable's free tier, well within its row limits for two small tables. Drafting the persona text, the PRD-lite content and the insight-nudge copy, along with research support and review, was done throughout using a free-tier conversational AI chat assistant — never through a paid API integration — and nothing in this project runs as deployed code, so no hosting, inference or infrastructure billing exists anywhere. The submission document is a Google Doc on a free Google account, and the usability sessions required no software beyond Figma's own Present mode. The token-cost optimisation described above is a design specification for a production system, not a cost incurred by this project.

---

## LIMITATIONS AND OPEN QUESTIONS

Three limitations affect the strength of this submission. Each is recorded here rather than left implicit.

1. **No High-priority insight→action friction was observed in usability testing.** Two MEDIUM findings were. Neither was reclassified to satisfy the requirement, because Part C's experiment is built on that evidence and a manufactured finding would have corrupted everything downstream of it.
2. **No price point is proposed**, because no willingness-to-pay data for this category in India could be located.
3. **The platform capability behind the one-tap action is not verified** by the Capstone, and is carried as a stated design assumption with a documented fallback rather than assumed into existence.

An earlier draft of this PRD contained a capability — knowing whether a service was still being used — that PhonePe does not have and I had invented. It was removed, and its removal is what makes the AI classification in Part B Task 2 come out as *augmented* rather than *native*. The relay held because the correction was made, not because the first version was right.
