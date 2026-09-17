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

---

# When there is no receiver at all

For a document, the check above is unavailable. There is no one to produce anything. **The replacement is not a weaker version of the same check** — it is a different act, plus an explicit statement of where verification stopped.

## First, the two things that are not evidence

**Your own reread is not evidence a reader will understand.** That is the curse of knowledge and it does not respond to effort. **An LLM rereading its own draft is not a naive audience either** — it has read the internet, and it wrote the draft.

**And the numbers above do not transfer.** Self-explanation's **g = 0.55 [0.45, 0.65], k = 69, N = 5,917** is the effect of an intervention *on a learner's learning*. Teach-back's **19 of 20 studies** spans heterogeneous outcomes including adherence and readmissions. Neither measures whether a given text is comprehensible. Quoting them as a licence for a clarity verdict is the exact overreach pattern this knowledge base exists to catch — see `never-say-this.md`.

## Second, inspect the text — and call it what it is

A reread is useless for "will they understand" and genuinely useful for defects that are **properties of the text**, checkable against a named reader and task:

| Defect | What to look for |
|---|---|
| Unintroduced term | A load-bearing term used before it is introduced, judged against the named reader — not against a word list |
| Dangling referent | "this", "the above", "it" with no antecedent inside the section a reader could have entered at |
| Unreachable precondition | A step whose prerequisite is **not identified and reachable before the step that depends on it**. Location is not the test: a prerequisite named up front with a link is fine; one that only appears afterwards, or is never named, is not |
| Undelivered promise | The opening says the document covers X; the body never does |
| Conversation-only context | A term, decision or constraint that exists only in the thread the reader was not in |
| Load-bearing jump | The reader cannot complete the document's own task without leaving it. **A named, reachable prerequisite is fine** — "you need an admin token; see Access" is a dependency the reader can satisfy. What this flags is a jump standing in for a sentence you did not write, and a chain of them: learning tends to be better with fewer links |
| Self-contradiction | Two statements in the same document that cannot both be true |

**HEURISTIC.** This is a list of defect types, not a validated instrument. No study in this knowledge base scores it, and **finding none of them is not evidence of anything.**

## Third, report corrections and name the edge

Say what changed, observably:

> "Added the required permission before the deployment steps; defined `tenant scope` at first use; removed the forward reference to §6."

Not: *"this should be much clearer now."*

And when you claim verification, say where it stopped:

> "Checked prerequisites, terminology and references. Reader comprehension has not been tested."

## Fourth, for consequential material, prepare the real check

The real check is a reader protocol, and **the author runs it, not you.** Schriver's protocol-aided revision is the field's own answer: "actual reader feedback is the most sensible and effective criterion for deciding whether a text is written in plain language," and the method is "helping writers see problems in text that they might otherwise miss."

Her stated practice: **five participants per cycle**, two or three cycles, with *"a rough rule of thumb"* that the first pass finds about half of the reader's problems and the second half of the remainder. Those are her labels — a rule of thumb and a reported practice, and she is explicit that "it is important not to confuse protocol-aided revision with an experiment."

What you can hand over is a test someone could actually run:

| Field | Example |
|---|---|
| Reader | Someone who has used the CLI but never touched the replica commands |
| Task | Recover a replica after a failed upgrade, using only this page |
| Materials | This page, a terminal, no one to ask |
| Success looks like | They reach a healthy replica without opening another document, and can say why the `--force` step is safe here |

Keep the success criteria **separate from the prompt** you give the reader. And match the test to the document — **HEURISTIC**, a working scheme rather than a validated mapping: a guide is tested by someone doing the task in a new situation; a design document by someone explaining why an alternative was rejected and when that reasoning would stop holding; a reference page is tested with the page open, because memorizing it was never the point.

## The four refusals

1. **A reread, a fresh model context, or a "novice persona" is not reader testing.** Stating it as one is a fabricated result.
2. **A command that ran is not an explanation that landed.** Execution success says nothing about the prose around it.
3. **The requester's approval is not the audience's**, unless that relationship was actually established. Usually it has not been.
4. **Preparing a reader test is not running one.** An exercise embedded in a document may help a reader learn; its presence is no evidence that anyone completed it.

## And the outcome that is allowed

**Finishing a document with reader comprehension untested is complete and normal.** Do not block delivery on a reader who is not available. Do not manufacture a substitute. Say what was inspected, say what was not, and stop.

Do not attach a verification notice or a test package to every artifact. The calibration table above still governs: a three-line commit message gets none of this.

---

## What this does NOT license

1. **"Teach-back has an effect size of d = ..."** — Fabrication if attributed to the 20-study review, which states it could not conduct a meta-analysis. It is a narrative synthesis.
2. **"People cannot self-assess comprehension."** Restricted to *explanatory/mechanistic* knowledge. There was **no drop** for facts, procedures, or narratives.
3. **"Their confidence drops even further after a diagnostic question."** The source marks this **non-significant**.
4. **"Preparing to teach is worthless — it wears off after a week."** Refuted by a 28-study meta-analysis: the *delayed* effect (g = 0.53) was **larger** than the immediate one.
5. **"Never use a multiple-choice check."** Contradicted by the source usually cited for it: no significant differences among formats survived post-hoc testing.
6. **"Open-ended checks beat closed-ended checks."** The closed Yes/No scored numerically *higher* than the open directive tell-back. The lever is collaborative framing.
7. **English backchannel tokens** ("uh huh", "yeah") as a universal diagnostic. They are English-specific.
8. **The tell-back wording as culturally portable.** The practice is evidenced across the USA, Iran, Australia, China and India — but **zero** studies adapted or tailored the wording, and "explain it back to me" is a face-threatening request whose acceptability varies. Treat the *practice* as portable and the *phrasing* as untested.
9. **"The document has been checked for clarity."** Nothing available to an author or a language model produces that verdict. Name what was inspected and name what was not.
10. **The defect list as a score.** It is a prompt for a human decision. Zero hits means zero hits of those seven types, not a clear document.
11. **Schriver's "half the problems per pass" as a measurement.** She calls it a rough rule of thumb and says the method is not an experiment. The five-readers figure is reported practice at one center, not an optimum.
