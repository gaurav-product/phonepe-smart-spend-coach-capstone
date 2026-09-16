# PhonePe Smart Spend Coach — Product Management Capstone

**Author:** Gaurav Kumar Singh
**Programme:** Masai School — Product Management Capstone (Module 6)
**Feature:** Smart Spend Coach — *Flagged Commitment + One-Tap Action*

---

## Result

**95 / 100 · 9.5 / 10**

| Section | Score | |
|---|---|---|
| Part A — Research, persona & feature PRD | **29 / 30** | 97% |
| Part B — Prototype, usability validation & pricing | **32 / 35** | 91% |
| Part C — Funnel, experiment & growth | **34 / 35** | 97% |

The two Part B deductions were the two things this project deliberately refused to invent: no High-severity insight→action friction was found in usability testing, and the Errors category came back empty. Both are documented below under *Known limitations*. Manufacturing either one would have scored better and made everything downstream false.

---

## What this project is

A single feature, taken from segmentation through to a growth experiment, under one constraint carried on every page:

> **Smart Spend Coach does not know that a commitment is wasteful. It identifies transaction patterns that may indicate a commitment is worth reviewing. The user decides whether the commitment is actually unnecessary.**

The feature detects a recurring charge from the user's own PhonePe transaction history — same merchant, regular interval, **≥3 consecutive occurrences**, plus either an **amount increase** against the user's own prior charges or a **resumption after a gap** — presents the charge history as evidence, and offers a one-tap entry to stop future auto-debits behind a mandatory confirmation.

**It makes no claim about service usage, email activity, merchant-side account status, trial status, or objective necessity.** It cannot know those things, and it says so on screen.

The graded artifact was a Google Doc assembled from [`submission/SUBMISSION_GOOGLE_DOC.md`](submission/SUBMISSION_GOOGLE_DOC.md). This repository is the working record behind it — every source document, the decision register, and the evidence log.

## Repository map

```
├── README.md                                    ← you are here
├── capstone/
│   ├── part-a/                                  Research, persona & feature PRD (30 marks)
│   │   ├── task-1-segmentation.md
│   │   ├── task-1-segmentation-AUDIT.md
│   │   ├── task-2-competitive-analysis.md
│   │   ├── task-5-prd-lite.md
│   │   └── task-5-prd-lite-AUDIT.md
│   ├── part-b/                                  Prototype, usability validation & pricing (35 marks)
│   │   ├── task-1-prototype-audit.md
│   │   ├── task-2-ai-classification.md
│   │   ├── task-3-tester-protocol.md
│   │   ├── task-3-usability-testing.md          ← Set A, real users
│   │   ├── task-3-evidence-record-v2-superseded.md
│   │   ├── task-3-heuristic-walkthrough-SET-C.md ← Set C, NOT user evidence
│   │   ├── task-4-ethics-bias-safety.md
│   │   └── task-5-pricing-packaging.md
│   └── part-c/
│       └── part-c-full.md                       Funnel, A/B test, growth loop, AI evaluation (35 marks)
├── decisions/
│   └── CAPSTONE_CONTROL_CENTER.md               Locked-decision register, evidence log, requirements matrix
└── submission/
    ├── SUBMISSION_GOOGLE_DOC.md                 ← the graded case document (source)
    └── FINAL_CAPSTONE_SUBMISSION.docx           ← the same document, formatted
```

**Part A Task 3 and Task 4** (RICE prioritisation and the Airtable base) do not have standalone files: the RICE scoring lives inside `task-2-competitive-analysis.md`, and the Airtable base is a live artifact, not a document. Both are reproduced in full in the submission document.

## Live artifacts

| Artifact | Contents | Link status |
|---|---|---|
| **Figma prototype** | 5 screens · 1 component set · 2 variants · 11 navigation interactions · every visible control wired | ✅ **Public — Anyone with the link can view** |
| **Airtable base** | `Personas` (2 records) · `Opportunity_Backlog` (5 scored ideas) | ✅ **Public — read-only share** |

**Live links**

- Airtable base (read-only): <https://airtable.com/appozPM3QfEc0ZJ7V/shrrHyVTT1sIrYcP2>
- Figma prototype: <https://www.figma.com/proto/XhV4JoExaeeygvEG1LZGez/PhonePe-Smart-Spend-Coach-%E2%80%94-Capstone-Prototype?node-id=4-38&starting-point-node-id=2%3A2>

## Evidence discipline

Every claim in every document carries a class, so a reader can tell what is established from what is reasoned:

`[CASE DATA]` supplied by the brief · `[FACT]` verified against a named external source · `[DERIVED]` computed from a stated input · `[PM INFERENCE]` reasoning · `[PM DECISION]` a choice made · `[DESIGN ASSUMPTION]` an implementation assumption · `[HYPOTHESIS]` a belief requiring a test · `[NOT VERIFIED]` searched for, not established · `[NOT SPECIFIED BY CAPSTONE]` outside the brief

**Three usability evidence sets are kept permanently separate and are never merged:**

| Set | What it is | May be cited as user evidence? |
|---|---|---|
| **A** | Real-user testing, 7 distinct people | ✅ Yes — the only set that may |
| **B** | Designer self-walkthrough as each persona | ❌ No |
| **C** | Independent heuristic / cognitive review | ❌ No |

## Known limitations

These are stated because they are real, not because a section required them.

1. **No High-priority insight→action friction was observed in usability testing.** Two MEDIUM findings were. The finding was **not** upgraded to satisfy the rubric — Part C's experiment is built on that evidence, and a manufactured finding would have corrupted everything downstream.
2. **Individual tester attribution was not retained.** The Set A record is an aggregate pattern plus confirmed aggregate facts, and is presented as such. Session dates were not recorded.
3. **The platform capability behind the one-tap action is `[NOT VERIFIED]`** — the brief does not establish that PhonePe can execute a payer-side auto-debit stop. Carried as a stated design assumption with a documented fallback (a one-tap entry into mandate management with the commitment pre-selected).
4. **No price point is proposed.** No willingness-to-pay data for this category in India could be located. The method for setting a price is stated instead of a number.
5. **Segment sizes are order-of-magnitude only.** PhonePe publishes no MAU and no category-mix breakdown, so the step from registered users to addressable users is an assumption.
6. **Competitor coverage is bounded by evidence.** Paytm, Walnut/Axio, Money View and INDmoney are absent because no primary product documentation of a spend-insight capability was verified for them — an acknowledged limitation, not a judgement about those products.
7. **Willingness-to-pay and expected-retention ratings are `[HYPOTHESIS]`**, including the retention rating on which the entire persona choice rests.

## Decision log

The full register — 34+ locked decisions with lock dates, evidence classes, and what each invalidates if changed — is in [`decisions/CAPSTONE_CONTROL_CENTER.md`](decisions/CAPSTONE_CONTROL_CENTER.md). The headline chain:

| Decision | Value |
|---|---|
| Primary persona | Mid-career household financial managers, 33–45, tier-1/2 |
| Secondary persona | Young urban salaried professionals, 24–32 |
| Primary segmentation factor | **Expected Retention** |
| Selected feature | **C2 — Flagged Commitment + One-Tap Action** (RICE 2.800) |
| Primary metric | IACR — insight-to-action completion, 7-day window |
| Guardrail metric | ARR — action reversal, 14-day window |
| AI classification | **AI-augmented** |
| Biggest AI risk (Part B) | **Hallucination rate** |
| Usability findings | F-01 MEDIUM · F-02 MEDIUM · B18 **not satisfied** |
| Prioritised funnel stage | **4 → 5** (70.0% drop) |
| Growth loop | **Content** |
| Weekly AI monitoring (Part C) | **Safety + Quality** |

### Corrections that changed the outcome

Recorded because they are the reason the later decisions hold:

- **A "usage signal" was invented and removed.** An early PRD draft had detection depending on knowing whether a service was still being used. PhonePe has no such capability. Removing it left detection deterministic — **which is why the AI classification comes out as *augmented* rather than *native*.**
- **An unsafe prototype interaction was removed in QA.** A change-to-variant shortcut let a single tap bypass the mandatory confirmation. The prototype is one interaction "less impressive" as a result.
- **An A/B hypothesis premise was corrected.** The experiment originally assumed the action button required scrolling to reach. Measuring the frame showed it was always on screen — the 12-second search was a *salience* problem, not a reach problem. The hypothesis was rewritten to match.
- **A merchant-behaviour claim was removed** from a user-facing screen — the product cannot know a merchant's billing or access policy.
- **The stale 600M/40M PhonePe figures were corrected to 700M/50M** against the official press release.
