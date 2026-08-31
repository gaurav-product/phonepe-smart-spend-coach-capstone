# PART B TASK 3 — REAL-TESTER USABILITY PROTOCOL
## Moderator pack · PhonePe Smart Spend Coach
**Date:** 16 Aug 2026 · **Prototype:** Figma `XhV4JoExaeeygvEG1LZGez` · **Persona:** LA-02 primary
**Status: PROTOCOL ONLY. No tester findings created. Figma unmodified. Part C not started.**

**Method change recorded:** the Persona 1 self-walkthrough (U-01 – U-18) stands unaltered — 0 Errors, 0 Hesitations, 17 Successes, 1 Quote, no High-priority insight→action friction. Real testers **supplement** that evidence; they do not replace or reinterpret it.

---

# 1. TESTER RECRUITMENT CRITERIA

**Target: 5 testers** (the Capstone's stated number). **3 is a workable minimum** — see §9 for why the threshold matters.

### Must have
- **Has never seen this prototype, the PRD, or any Capstone decision.** This is the single most important criterion — it is precisely what the self-walkthrough could not provide.
- Uses a payments app (PhonePe, Google Pay, Paytm or similar) on their own phone.
- Pays at least one recurring charge — a subscription, a bill, an EMI, anything auto-debited.
- Comfortable thinking aloud in English or Hindi. *(If Hindi, record their words in Hindi and translate alongside — do not translate away their phrasing.)*

### Should have, if you can get it
- **At least 2 testers in the 33–45 band who manage household money.** These are the persona-matched testers and their observations carry the most weight.
- A spread of confidence with apps — an unusually confident tester and a less confident one surface different things.

### Must NOT have
- Any prior exposure to the prototype, the wedge, the metrics, or the phrase "insight to action".
- Any knowledge that a particular finding is needed.

### Acceptable sources
Friends and family are **explicitly permitted by the Capstone**. Parents, older siblings, cousins, neighbours, colleagues outside product roles.

### ⚠️ Practical setup note
**Figma sharing (LB-08b) is still not enabled.** You do not need to fix it for this. **Run the session on your own laptop or phone in Present mode and hand the device to the tester.** This avoids the sharing blocker entirely and lets you watch their hands, which is where hesitation actually shows.

---

# 2. EXACT MODERATOR SCRIPT
*Read the bracketed parts aloud. Say nothing else.*

### Opening — say this verbatim

> "Thanks for helping. This will take about fifteen minutes.
>
> I'm testing a design, **not you**. There are no right or wrong answers, and if something is confusing that's useful information for me — it means the design has a problem, not you.
>
> Everything on the screen is made-up example data. **I won't ask you for any real financial information, and you shouldn't share any.**
>
> One thing that will feel odd: **please think out loud.** Say whatever goes through your head, even if it seems obvious or silly. If you go quiet I'll just ask 'what are you thinking?' — that's not a hint, I'm only trying to hear you.
>
> This is an early prototype, so not everything is clickable. If something doesn't respond, just tell me and move on.
>
> Ready?"

### Handing over

> "This is a payments app. Here's the situation."

*Read the persona setup in §3, then hand the device over.*

### The only opening instruction

> **"Please look at this screen and tell me what you would do."**

Then **stop talking**. Let silence sit. Count to ten before you say anything.

### During the session

Say nothing except the neutral prompts in §4. If the tester asks you a direct question — *"is this the right one?"*, *"should I press this?"* — deflect:

> "What do you think?"

or

> "Whatever seems right to you."

### If a tester is completely stuck

Only after **at least 45 seconds** of visible searching with no progress:

> "Take your time. What are you looking for?"

**Record the full duration and exactly what they said.** A tester who searches for 45 seconds and then finds it has given you a Hesitation. A tester who never finds it has given you an Error. **Do not rescue them early — that destroys the evidence.**

### Closing

> "That's everything. Was there anything that felt unclear or awkward at any point?"
>
> "Anything you expected to happen that didn't?"
>
> "Thank you."

---

# 3. EXACT TASK INSTRUCTIONS
*Read once, verbatim. Do not paraphrase, do not add.*

> "You manage the money in your household.
>
> A few recurring payments come out of your own account every month — some of them for other people in the house.
>
> You opened your payments app for something unrelated, and the app has shown you something.
>
> **Have a look, and do whatever you would normally do.**"

**Do not say:** "review the charge", "take the action", "stop the payment", "decide whether it's worth keeping", "there's a subscription that went up". Every one of those tells them the answer.

---

# 4. NEUTRAL FOLLOW-UP QUESTIONS

### Allowed at any time
- "What are you thinking?"
- "What would you do next?"
- "What do you expect to happen?"
- "Can you tell me what you understand from this?"
- "What made you choose that?"
- "Was anything unclear?"

### Allowed at the end only
- "Was there anything that felt unclear or awkward?"
- "Anything you expected that didn't happen?"

### Screen-specific neutral probes
*Use sparingly — at most one or two per screen. Silence produces better data than questions.*

| Screen | Neutral probe |
|---|---|
| 01 Home | "What is this telling you?" |
| 02 Insight detail | "What do you make of this?" · after a pause: "What would you do now?" |
| 03 Confirmation | "What do you think will happen if you tap that?" |
| 05 Acted-on | "What happened just now?" |
| 04 Edge case | "What do you understand from this one?" |

---

# 5. OBSERVATION CAPTURE TEMPLATE

Capture **live**, during the session. Reconstructed notes are weaker evidence and you will lose the exact words.

| ID | Tester | Persona match | Category | Screen / Flow | Actual observation | Severity | Exact quote | Evidence |
|---|---|---|---|---|---|---|---|---|
| T1-01 | T1 | Yes / No | Error / Hesitation / Success / Quote | | *What they did or said — behaviour, not your interpretation* | High / Medium / Low / N/A | *their words, unedited* | [OBSERVED: date] |

### Rules for filling it in
- **Behaviour, not conclusion.** Write "tapped Keep this charge, then went back" — not "was confused by Keep this charge."
- **Quotes verbatim.** Do not tidy grammar, do not strengthen. "Hmm, what's this one?" stays as it is; it does not become "the tester found it unclear."
- **Time the pauses.** Anything over ~5 seconds of visible searching is worth a note with the duration.
- **Record wrong taps.** Which control, and what they did next.
- **Record clean passes too.** Successes are findings.
- **Keep a separate INTERPRETATION column or note.** Your explanation of *why* goes there — never in the observation cell.

### Also log, per tester
Total time · whether the action was completed unaided · whether they used the safe exit · anything about the two known prototype limitations *(Screen 04 "Tell me if this repeats" has no destination — **exclude from findings**)*.

---

# 6. SEVERITY DECISION GUIDE

The locked definitions:

| Severity | Locked definition |
|---|---|
| **HIGH** | **Blocks task completion for multiple users** |
| **MEDIUM** | Causes hesitation but is recovered from |
| **LOW** | Minor or isolated issue |

### Decision tree — apply per issue, across all testers

```
Did the issue prevent the tester finishing the task?
├─ YES → did it prevent completion for ≥2 testers?
│         ├─ YES → HIGH
│         └─ NO (only 1) → MEDIUM, and note it as isolated
└─ NO  → did it cause a visible pause, a wrong tap, or a question?
          ├─ YES, and they recovered → MEDIUM
          └─ Minor, or only 1 tester, no real delay → LOW
```

### Hard rules
- **"Blocks task completion for multiple users" means ≥2 testers.** One tester struggling is Medium at most, however striking it was. **This threshold is what makes a High finding real, and it is not negotiable.**
- Do not assign High because an issue is interesting, or because the Capstone wants one.
- Do not assign Low to a Success — a clean pass has **N/A** severity, not Low.
- Severity attaches to the **issue across testers**, not to one row.

---

# 7. WHAT THE MODERATOR MUST NOT SAY

### Never — these invalidate the finding
- ❌ "Now find the action button."
- ❌ "Scroll down."
- ❌ "Look for the CTA / the button / the purple one."
- ❌ Pointing, gesturing, or looking at the control
- ❌ "Did you find it?"
- ❌ "Was the button hard to see?"
- ❌ "Did you expect a confirmation?"
- ❌ "Did you understand that it stops auto-debits?"
- ❌ "Most people tap here."
- ❌ Anything about B18, Part C, insight→action friction, or what you hope to find

### Also never
- ❌ Explaining what a screen is for before they've read it
- ❌ Correcting a "wrong" interpretation — **a wrong interpretation is the finding**
- ❌ Filling silence
- ❌ Reacting — no "yes", "exactly", "hmm", raised eyebrows. Stay flat.
- ❌ Defending the design

### If you catch yourself leading
Note it in the log for that tester. A contaminated observation should be marked and given less weight, not quietly kept.

---

# 8. CONSOLIDATING ACROSS 5 TESTERS

**Step 1 — pool everything.** All rows from all testers into one table, tester ID preserved.

**Step 2 — cluster by issue, not by tester.** Group rows describing the same underlying thing, even where wording differs. Watch specifically for repeats at: the action entry on 02, the "Keep this charge" control, the WHAT WILL NOT CHANGE block on 03, Undo on 05, and the absence of an action on 04.

**Step 3 — build the frequency table.**

| Issue | Testers affected | Screen | Behaviour observed | Recovered? | Severity |
|---|---|---|---|---|---|

**Step 4 — assign severity per §6**, using the *cluster* count, not individual rows.

**Step 5 — check category coverage.** The Capstone requires observations across **all four** note types. Count Errors, Hesitations, Successes and Quotes separately. **If any category is still empty after real testing, report that honestly.**

**Step 6 — merge with the self-walkthrough.** Keep the two evidence sets **visibly separate** in the final document:
- Self-walkthrough (U-01 – U-18) — labelled as designer self-walkthrough
- Real testers (T1-xx …) — labelled as real testers, with n stated

Never blend them into a single undifferentiated list. An evaluator will read the method section, and the credibility of the real-tester findings comes from the fact that those people had never seen the prototype.

---

# 9. DETERMINING WHETHER A GENUINE B18 FINDING EXISTS

The Capstone requires **at least one High-priority observation describing friction specifically between viewing a personalised insight and completing the recommended action on it.**

### All four conditions must hold

| # | Condition | Test |
|---|---|---|
| **1** | **It sits in the insight→action transition** | The friction occurred on Screen 02 or in the 02 → 03 → confirm sequence. Friction on Screen 01, 04 or 05 does **not** qualify. |
| **2** | **It is about getting from insight to completed action** | Not about understanding the *evidence* — about locating, understanding, trusting, or completing the *action*. |
| **3** | **It reaches the locked HIGH bar** | It blocked task completion for **≥2 testers**. |
| **4** | **It is behavioural, not opinion** | Based on what testers *did* — searched, mis-tapped, abandoned, failed — not on what they said afterwards when asked. |

### Verdicts

**If all four hold** → you have a genuine B18 finding. Document the behaviour, the tester count, the exact quotes, and the severity reasoning.

**If conditions 1, 2 and 4 hold but only one tester was blocked** → **MEDIUM, not High.** Record it accurately. Do not promote it. State that B18 is not satisfied.

**If no friction emerged at all** → report verbatim:

> **"No High-priority insight→action friction was observed in the completed testing."**

Then state what was tested, how many testers, and that the requirement is unmet. **That is the honest outcome and it is not a failure of method — it is a result.**

### ⚠️ The trap to avoid
After five sessions you will have invested real effort and will *want* a High finding. The pressure to round a Medium up will be strongest at exactly the moment your judgement is most tired. **The tester count is the guard: two blocked testers, or it isn't High.**

---

# 10. HOW FINDINGS BECOME THE PART C BATON

**Not designing Part C here — only the relay mechanism.**

The chain the Capstone requires:

```
Real observed behaviour during testing
   ↓
A named, specific product friction in the insight→action transition
   ↓
The Part C A/B test hypothesis, which must NAME that observation
```

**What the baton must be to work:**

| Requirement | Why |
|---|---|
| **A specific observation, not a theme** | Part C's acceptance criterion requires the hypothesis to name *which* Part B observation it addresses. "Users found it confusing" cannot be named; "3 of 5 testers scrolled past the action entry and returned to Home without acting" can. |
| **Located in the insight→action transition** | Because it must map onto the Part C funnel's *first insight viewed → recommended action taken* stage. |
| **Behavioural** | An experiment can change a design; it cannot change an opinion. |
| **Measurable by the locked primary metric** | It must be the kind of friction whose removal would move **LA-24 Insight-to-Action Completion Rate**. |

**Where it will attach downstream:** the observation becomes the *because* clause of the Part C hypothesis template — *"We believe that \<change\> will result in \<measurable outcome\> **because \<this observed friction\>**."*

**If no qualifying observation emerges**, Part C has no legitimate baton. The options at that point are to test more people, or to document the gap and accept the mark impact — **not to invent a finding**, which would break the relay the Capstone is actually grading.

---

## BEFORE YOUR FIRST SESSION — CHECKLIST

- [ ] Prototype open in **Present mode**, starting at **01 · Home entry**
- [ ] Reset to Screen 01 between testers
- [ ] Capture template open on a second device or on paper
- [ ] Tester has **never** seen the prototype
- [ ] You have read §7 and know what you must not say
- [ ] Timer or clock visible for pause durations
- [ ] You are prepared to sit through silence without rescuing

---

*Protocol complete. No tester findings created. No fabricated testers, quotes, errors, hesitations, successes or severities. Figma unmodified. Part C not started.*
