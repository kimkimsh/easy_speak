# Checking that it landed

Load this when the cost of a misunderstanding is real: they are about to act on it, hand it off, build on it, or teach it to someone else.

## Two failures, stacked

**You cannot introspect your own clarity.** Newton's tappers tapped out a well-known song and predicted how many listeners would name it. They predicted ~50%. The actual rate was **3 correct out of 120** — a figure that fell *below every single prediction any tapper made*. Not one was pessimistic enough.

This does not respond to effort. Camerer, Loewenstein & Weber: better-informed agents "are unable to ignore private information even when it is in their interest to do so." Financial incentives produced no improvement; outcome feedback produced no improvement; market pressure halved the bias and never eliminated it.

Your sense that "that was clear" carries no diagnostic weight. It is not a weak signal. It is not a signal.

**And they will not tell you.** Listeners tolerate a lack of understanding and "even feign understanding when it is not justified" — they risk offending you, risk revealing their own incompetence, and want to minimize the joint effort. The acknowledgment tokens appear "however insincere they may be."

Worse, the failure is self-concealing: **a person who has misunderstood cannot generate a question about the thing they misunderstood.**

> "Because they may not understand the situation well enough to formulate a question, patients often answer 'no' when asked if they have any questions."

"No questions" is the default output of a *failed* comprehension process, not a successful one.

**And self-report does not track comprehension.** In an emergency-department randomized trial, teach-back raised *actual* comprehension (follow-up OR 3.61, 95% CI 2.09–6.22) while leaving *perceived* comprehension completely unmoved. The two are decoupled.

## Therefore

**The only valid check makes them produce something.**

### Never use these as verification

| Phrase | Why it fails |
|---|---|
| "Does that make sense?" | Cannot be answered by someone who misunderstood. |
| "Any questions?" | Same. Silence is the failure mode, not the success mode. |
| "Is that clear?" / "Following me?" | Same. |
| A nod, "okay", "got it" | Produced under social pressure, "however insincere". |
| Your own reread of what you wrote | Invalidated by the curse of knowledge. |
| A readability score, or asking an LLM "is this clear?" | Neither is a validated measure of processing ease. |

Delete these. They feel like diligence and function as decoration.

### Use these instead

The strongest quantitative warrant in the entire knowledge base: **prompting someone to explain the material back.**

> Self-explanation, prompted vs. not: **g = 0.55, 95% CI 0.45–0.65, 69 effect sizes, N = 5,917.** Held across task type, subject area, and education level.

| Phrasing | What it elicits | Evidence |
|---|---|---|
| "I've given you a lot here. It'd help *me* to hear how you'd put it back." | Collaborative tell-back. | Significantly preferred over both a directive tell-back and a Yes/No check, and rated significantly more effective (all P ≤ .001). **Caveat: preference and perceived effectiveness only — comprehension was never measured.** |
| "What does *[term]* mean, in your words?" | Elaboration of a named concept. | The strongest single cell: **g = 0.87, CI 0.56–1.18, k = 13, N = 1,678.** |
| "Walk me through it — how does it actually work?" | Production of a causal model. | The self-explanation effect (g = 0.55), plus: self-rated understanding of a *mechanism* collapses the moment a real explanation must be produced. |
| "Why did we pick this over the alternative?" | Justification of a decision. | Justify category: **g = 0.42**, statistically detectable. |
| "What are you going to do when you get back to it?" | Behavioural teach-back / application. | Teach-back effective in **19 of 20 studies** (9 RCTs), across knowledge recall, adherence, technique, and readmissions. |
| "You'll need to explain this to someone on Thursday." | Teaching expectancy. A supplement, not a substitute. | Preparing-to-teach vs. control: g = 0.28 immediate, **g = 0.53 delayed** (28-study meta-analysis). |

## The active ingredient is the framing, not the openness

This is the part that gets misremembered.

A blunt, directive tell-back ("Tell me what I just said") scored **no better than a plain Yes/No check** on either preference or perceived effectiveness. Open-endedness is not the lever.

**The lever is collaborative framing — putting the burden of failure on yourself.**

> "I've given you a lot of information. It would be helpful **to me** to hear your understanding."

*I may not have explained this well* — not *let me test whether you were paying attention*. An open-ended check delivered as an interrogation is not the finding.

## Calibrate — do not staple a check onto everything

Understanding is pursued to a **grounding criterion**: sufficient for current purposes, never perfect. The criterion is set by the consequence of being wrong.

| Situation | Check |
|---|---|
| Casual question, no downstream action | None. Answer and stop. Checking here is just annoying. |
| They're about to run the command you gave them | A one-line application check. |
| They're going to build on this / hand it off | Collaborative tell-back. |
| They need to modify or debug it later | Make them produce the causal model. |
| They'll teach it to someone else | Causal model, plus the two examples. |

Firing step 5 on every trivial exchange is its own failure mode. Perfection is not the target.

## Silence means less, not more, when they defer to you

Other-initiated repair — signalling trouble so the speaker reformulates — is **universal conversational infrastructure**: documented in every spoken language investigated, with no language lacking an interjection for it, used roughly **once every 1.4 minutes**.

But universality of the *mechanism* is not uniformity of *willingness*. Face and politeness norms heavily modulate whether someone will actually initiate repair.

> The more deferential the listener's position, the **less** their silence means — and the more you need an active check. Never read "no questions" as "understood."

## What this does NOT license

1. **"Teach-back has an effect size of d = ..."** — Fabrication if attributed to the 20-study review, which states it could not conduct a meta-analysis. It is a narrative synthesis.
2. **"People cannot self-assess comprehension."** Restricted to *explanatory/mechanistic* knowledge. There was **no drop** for facts, procedures, or narratives.
3. **"Their confidence drops even further after a diagnostic question."** The source marks this **non-significant**.
4. **"Preparing to teach is worthless — it wears off after a week."** Refuted by a 28-study meta-analysis: the *delayed* effect (g = 0.53) was **larger** than the immediate one.
5. **"Never use a multiple-choice check."** Contradicted by the source usually cited for it: no significant differences among formats survived post-hoc testing.
6. **"Open-ended checks beat closed-ended checks."** The closed Yes/No scored numerically *higher* than the open directive tell-back. The lever is collaborative framing.
7. **English backchannel tokens** ("uh huh", "yeah") as a universal diagnostic. They are English-specific.
8. **The tell-back wording as culturally portable.** The practice is evidenced across the USA, Iran, Australia, China and India — but **zero** studies adapted or tailored the wording, and "explain it back to me" is a face-threatening request whose acceptability varies. Treat the *practice* as portable and the *phrasing* as untested.
