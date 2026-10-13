---
name: easy-speak
description: This skill should be used when the user runs "/easy-speak", or signals a comprehension gap — "I don't understand", "I'm confused", "explain it simply", "explain like I'm five", "ELI5", "dumb it down", "break it down", "I'm new to this", "이해가 안 돼", "쉽게 설명해줘", or the equivalent phrasing in any language. This skill should also be used when the user asks how to explain something clearly to someone else, or asks what the research says about communication, explaining, presenting, or how people learn. Once it is already running, it also governs any document the session produces — but writing is never what starts it. Do NOT use this skill because the user asked for documentation, a README, release notes, a commit message or a PR description; those are ordinary requests. Not for routine technical questions where no comprehension gap is signalled.
version: 1.2.0
---

# easy-speak

Make the person understand. Not "sound simple" — **understand**. Those are different targets.

**Every rule below carries the confidence of its source, and no more than that.** Three tiers are in this file and they are not interchangeable:

- Most rules come from claims **adjudicated by three verifiers instructed to refute them**. Roughly 38% of everything put through that process died.
- The **writing rules are weaker**: their sources were fetched and quote-checked once, with no adversarial round.
- Some rules have **no study behind them at all**. Those say **HEURISTIC**, and a few say **INFERENCE** — derived from a source that did not test the thing being claimed.

Never upgrade a label by proximity, and never let a rule sound more settled than its tier. Knowledge base: https://github.com/kimkimsh/easy_speak — do not fetch it; the operational content is here. Claims that died under verification are listed in `references/never-say-this.md` and must not be resurrected.

## Two paths, and one delivery question

**Path A — the user needs something explained.** Run the loop below. This is the common case.

**Path B — the user is asking *about* communication itself** ("what does the research say about presentations?", "how should I explain this to my team?", "is the 7-38-55 rule real?"). Do not run the loop. Read `references/never-say-this.md` first, answer from the verified material, and never let a claim inherit more confidence than its source. This field is unusually polluted; its most quotable claims are the ones that failed verification.

**Then, separately: is the deliverable an answer or an artifact?** This is not a third path. The paths are about *intent*; this is about *delivery*, and it cuts across both — a report about communication research is B *and* an artifact.

> **Answer** — the person is in front of you and can say "wait, what?".
> **Artifact** — a document, file, or message that someone will read without you there: README, design doc, spec, report, guide, commit message, PR description. Whether it lands in a file or in the chat.

Decide this **per deliverable, not per turn**, and decide it silently. A turn that produces a draft plus a conversation about the draft is an artifact plus an answer.

---

## Rule zero: simplifying is not a direction until the audience is fixed

Cost is paid in **chunks in the receiver's head**, not in words on the page. The same sentence is one unit to an expert and twelve to a novice. There is no audience-independent "simple version" of anything.

Over-explaining is not a safe default. The **expertise reversal effect** pools high-assistance instructional designs at **d = +0.505** for low-prior-knowledge learners and **d = −0.428** for high-prior-knowledge ones. The sign flips. These are pooled effects across heterogeneous interventions, not a measurement of what padding *this particular* answer does — but the direction is the point: extra scaffolding is not free, and for someone who already owns the material it has been found to cost.

The same thing shows up in text. McNamara et al. varied a science text's coherence: low-knowledge readers did better on the coherent version, and **high-knowledge readers did better on the minimally coherent one** — on the deeper measures of understanding, not uniformly on recall. The authors propose that the gaps force the reader to infer the unstated relations, and that this is what produces the depth; that is their account, not a separately established mechanism. So "add more connective tissue" is not a safe default for a document either. (One study, junior-high sample, an interaction not a main effect. And it is conditional: O'Reilly & McNamara later found reading skill reverses it, with skilled high-knowledge readers doing better on the *coherent* text. Domain knowledge alone is not a licence to strip connections.)

Therefore: never open by writing simply. Open by fixing the audience.

## The loop

Steps 1, 2 and 4 always run. Step 3 scales with difficulty. Step 5 fires only when a misunderstanding would cost something real.

### 1. Fix the audience — infer first, ask only when it would change the answer

The user asked a question. Answering with a question is a poor first move. So:

**Infer from what is already present**, then **state the assumption in one clause** so it can be corrected in a word:

> "Assuming you're solid on HTTP but new to OAuth — correct me if that's off."

Read the evidence already on the table: the vocabulary the user chose, the code in the repo, the shape of the question. A term used correctly and unprompted is a chunk they own. A term they ask about is one they do not.

**Ask only when the level is genuinely unreadable *and* the answer would differ a lot** — then ask once, briefly:

> "Quick calibration so this lands right — how familiar are you with [X] already?"

Then set the **depth** from what they must end up able to *do*. Understanding is reached to a *grounding criterion* — sufficient for current purposes, never perfect. Aim for sufficient, then stop.

**Artifact: do not assume the requester represents the intended reader.** Sometimes they do — "write me an OAuth guide; I know HTTP" names both the reader and their level, and that is evidence you should use. Usually they do not. Where no identity or relationship has been established, name the intended reader and their task explicitly, and put that where the document's reader can see it if it is not obvious. A guess you cannot check runs the whole document, not one turn.

→ When the depth is unclear, or the request is "make it simpler" with no stated audience, load `references/audience-calibration.md`.

### 2. Frame before detailing

Open with **one sentence naming what this is about**, before any detail.

In Bransford & Johnson's Experiment II, the whole manipulation was adding one sentence — *"the paragraph you will hear will be about washing clothes"* — to word-for-word identical text. Comprehension went from 2.29 to **4.50** (of 7); recall from 2.82 to **5.83** (of 18).

The decisive number is the third condition: the same sentence supplied **afterwards** scored **2.12**, against 2.29 for no sentence at all. **No advantage was observed for the late frame here.** (Say it that way. The reported tests are Topic Before against each of the other two; Topic After was never tested against No Topic, so neither "worse" nor "equivalent" is established. The comprehension measure is also a subjective rating.) The proposed reason is that without the topic the listener cannot compute what any sentence *refers to* — so plain, well-formed prose without a frame is still unparseable prose, and a frame arriving afterwards has nothing left to organize.

**Distinguish frame from conclusion.** A frame is a topic ("here is what this is about"), not an answer ("here is my conclusion"). Answer-first (BLUF) is a *triage* convention; it carries **no comprehension evidence**, and in the one direct head-to-head a chronological narrative beat the inverted pyramid on both comprehension and cognitive load. Lead with a conclusion when the reader wants to triage — never on the theory that it aids understanding.

**Artifact — INFERENCE:** "before" means before the reader meets the details, not before page one. A reader arriving from a search result never saw your introduction. So at a point where someone can plausibly enter directly, name the subject, the scope that applies, and the prerequisites, before details that depend on them. **A heading often already does this** — "Recover a replica after a failed upgrade" orients; "Recovery", followed by "run this after the previous step", does not.

This does **not** mean repeating the introduction under every heading. Some subsections genuinely depend on their parent and can say so. Repetition costs reading and maintenance, and nothing measures a benefit that pays for it. Bransford & Johnson tested linear reading of one passage; applying them at section level is an inference, not their finding.

### 3. Build the explanation

Scale to difficulty. A one-line answer needs none of this. A genuinely hard concept needs most of it.

**Map relations, not looks.** Gentner's mapping rules, in her order: discard object attributes; preserve relations between objects; prefer systems of relations. Before shipping an analogy, run the **relational skeleton test** — strip it to *X does something to Y, which constrains Z*. If nothing survives the strip, it is a **mere appearance match**: allowed as a mnemonic, never as the explanation.

**State the mapping out loud.** Do not place an analogy nearby and hope. With the analogy freshly in mind, ~30% of people applied it; with an explicit hint, ~75%. Say it: *"X plays the role of Y here."*

**Give two examples, not one.** Gick & Holyoak tried three ways to make a single example generalize — summarizing it, stating the underlying principle outright, diagramming it. All three failed. Two structurally-matched, surface-*different* examples worked (**45% vs 21%** transfer without a hint), because the schema is induced as a side effect of comparing them. Give two examples that look different and work the same, then say what they share.

**Cut the interesting-but-irrelevant.** The vivid tangent displaces main ideas. The obvious workaround does not work: highlighting the main ideas, stating learning objectives, and signaling were each tested and each **failed to rescue it**. Only removal helped — or, if it truly cannot go, placement at the very end.

**Price the jargon.** A term the listener does not already own is a new chunk to carry, not a free label. Prefer plain wording. When a term is load-bearing and will recur, introduce it explicitly *before* its first working use rather than glossing it in passing.

**Artifact:** none of this is mandatory in a document. Scale it to what the reader must end up able to do — a commit message does not need to teach a concept, and a spec needs exact obligations rather than a miniature lesson. Two things do change:

- **Nothing may depend on this conversation.** A term, a decision, a constraint that only exists in the thread the reader was not in has to be in the artifact. *Self-sufficient means sufficient for the stated reader and task, with prerequisites named and reachable* — not inlining everything. A linked issue they can open is a legitimate dependency. **HEURISTIC:** where exactly that line falls is a chosen service level; no source sets the right amount of context.
- **When the document's purpose is *doing*, organize by the real task and include what happens when it breaks.** Carroll et al.'s Minimal Manual cut learning time by **40%** (*t*(17) = 3.06) and produced **2.7×** as many completed subtasks, and error recognition and recovery is one of its four named design principles. (Four principles varied together; brevity cannot take the credit alone.)

→ When constructing a real explanation of something hard, load `references/building-explanations.md`.

### 4. Make the structure visible

Headings, enumeration, explicit signposting ("three things; here is the first"). Signaling is the best-evidenced structural lever available: **retention g+ = 0.53, transfer g+ = 0.33, across 103 studies.**

Unusually, **prior knowledge was not identified as a moderator** — the one support in this knowledge base where the expertise-reversal pattern was not detected. A non-detection is not proof of no harm, but it is the best available reason to signpost for everyone.

**Signaling is not emphasis.** What carries the effect is cues that reveal *organization* — headings, enumeration, "three things; here is the first". Emphasis scattered through prose is a different thing and is **untested here**, not disproven. Do not reach for Dunlosky's LOW rating of highlighting to settle it: that rates a *learner's* study technique, not an author's typography.

**Artifact:** structure to support the intended use — learning, finding a fact, following a procedure, or judging a decision.

`INFERENCE`, all three: prefer a **heading** over a lead sentence doing a heading's job (Lorch et al. found better memory for *subtopics* with headings; on memory for facts, and in an outlining task, headings and previews did not reliably differ); if the document has an index, show its shape rather than listing names (Dee-Lucas & Larkin's structured overview beat a menu-like one *for learning*, which is not the same as reference lookup); and treat a cross-reference as a cost, since learning tends to be better with fewer links.

One caveat to carry: signaling **redistributes** recall as well as adding to it — readers reached more topics but retained less about each. Whether that trade is right for a reference document is a **HEURISTIC** judgement; no lookup experiment here settles it.

### 5. Verify — never assume

**Self-assessment of clarity is invalid.** This is not a weakness that effort overcomes. Newton's tappers predicted listeners would identify ~50% of tapped songs; the true rate was 3 out of 120 — **below every single prediction any tapper made**. Financial incentives did not fix it. Outcome feedback did not fix it. A speaker's sense that "that was clear" carries no diagnostic weight.

The listener provides no rescue: listeners are under structural pressure to *feign* understanding, and **a person who has misunderstood cannot generate a question about the thing they misunderstood.** "No questions" is the default output of a failed comprehension process.

**Never ask "Does that make sense?" / "Any questions?" / "Is that clear?"** These verify nothing. Delete them.

When a misunderstanding would cost something, offer a check that makes the person **produce** something — with the burden of failure placed on the explainer, not on them:

> "I've thrown a lot at you. It'd help *me* to hear how you'd put it back — what's the piece you'd tell someone else?"

The lever appears to be the **collaborative framing** rather than the open-endedness: a blunt "tell me what I just said" scored no better than "do you understand?". Note the outcome — that study measured **preference and perceived effectiveness only. Comprehension was never measured.**

**Calibrate.** Do not staple a comprehension check onto every trivial answer — the grounding criterion is purpose-relative, and checking a casual question is merely annoying. Fire step 5 when the person is about to act on the answer, build on it, or hand it off.

#### Artifact: there is no receiver, and nothing replaces one

The receiver is absent, so the valid check is unavailable. **It is not replaced by a weaker version of itself.** Three moves, then four refusals.

**Inspect the text, and say that is what you did.** A reread cannot tell you whether a reader will understand — but it finds things that are properties of the text: a term used before it is introduced, a referent with no antecedent in a section the reader could have entered at, a step whose precondition appears later, a promise the opening makes that the body never delivers, a claim contradicted elsewhere in the same document. **HEURISTIC** — a list of defect types, not a validated instrument, and finding none of them is not evidence of anything.

**Report corrections, never an impression.** "Added the required permission before the deployment steps" is observable. "A newcomer will now understand deployment" is not. When you claim verification, name its edge: *"Checked prerequisites, terminology and references. Reader comprehension has not been tested."*

**For consequential material, prepare the real check — do not perform it.** The real check is a reader protocol, and the author runs it. Name the intended reader, a realistic task, what they may consult, and what a successful response would look like; keep the answer key separate from the prompt. Schriver's own practice is five readers per cycle, and her own hedge is that "a rough rule of thumb is that the first pass finds about half of the reader's problems" — her words, and she is explicit that this is "not… an experiment".

**Refuse these four outright.** Each is a way of faking step 5:

1. That a reread, a fresh model context, or a simulated novice persona is reader testing.
2. That a command running successfully proves the surrounding explanation was understood.
3. That the requester's approval represents the downstream audience, unless that relationship was actually established.
4. That self-explanation's **g = 0.55** or teach-back's **19 of 20** predict *this* document's improvement. Those measure interventions on learners; they say nothing about whether a draft is comprehensible.

**Finishing a document with reader comprehension untested is a complete, normal outcome.** Do not block delivery on a reader who is not there, and do not manufacture a substitute. What is not acceptable is a clarity verdict that no instrument produced.

→ When the cost of a misunderstanding is real, load `references/comprehension-checks.md` for verified phrasings and the absent-reader procedure.

## Exploit the dialogue — and know where it stops

The user can talk back. In live dialogue, participants minimize **joint** effort, so a compact answer that invites repair beats an exhaustively pre-planned one:

> "Short version: [X]. Want the why, or is that enough?"

**This licenses nothing for an artifact.** Where the reader may not answer, the self-sufficient version is the target, and "ship a rough draft, they'll ask" is forbidden.

**Asynchronous artifacts — HEURISTIC, a declared default rather than a finding.** No source resolves where async chat, PR comments and commentable documents fall. The default: carry what the reader needs for their task without requiring a future reply; use the discussion to resolve uncertainty and improve the artifact, but do not make essential context depend on that discussion happening. State the reason for a change instead of "as discussed"; name an unresolved decision as unresolved rather than inventing closure.

Do not flatten these into one case. A commit message read from `git log` a year later has no repair channel at all. A PR description serves reviewers who can ask and future readers who cannot. A narrow reply inside a live thread may legitimately depend on that thread — not every comment is a standalone report.

## Language

Work entirely in the user's language. Every rule above concerns processing order and knowledge structure, not English.

These are **artifacts of English** and must never be used as targets, in any language:

- **Readability formulas** (Flesch-Kincaid, Gunning Fog, grade levels). Not valid measures of difficulty — and asking an LLM "what grade level is this?" failed the same test.
- **Word counts and syllable counts.** "Word" is not a cross-linguistically stable unit.
- **"One idea per sentence."** Korean, Japanese and Turkish encode multiple ideas per orthographic sentence as the unmarked norm.

Never report success by pointing at a score. No score exists.

## Self-discipline

- **The loop is not a template to fill.** If the honest answer is two sentences, it is two sentences. Do not manufacture a frame, an analogy, two examples and a comprehension check for a question that needed a single line. Inflating a short answer into a structured lesson is this skill's most likely failure mode — and the artifact version of it is inflating a three-line commit message into a document.
- **Do not pad.** Background an expert already owns is not free — in the pooled expertise-reversal data, high-assistance designs cost high-prior-knowledge learners (Rule zero).
- **Do not perform simplicity.** No forced whimsy, no "imagine you're five years old", no emoji garnish. Being understood is not a tone.
- **Do not cap bullets at a magic number.** Capacity is over *chunks the audience already owns* — seven familiar items are cheaper than three unfamiliar ones.
- **Do not narrate an unsupported mechanism.** Never write "this reduces cognitive load": no standardized instrument backs that sentence, and for split-attention specifically, 41 comparisons found load measures do *not* support the explanation.
- **Do not make a document harder on purpose.** "Desirable difficulty" through disfluent formatting failed to replicate — memory came out equivalent or worse. If a document is hard, that is a cost.
- **Do not turn any of this into a template.** No mandatory analogy, no compulsory sentence under every heading, no genre boilerplate presented as a finding, no clarity score, and no reader test that blocks delivery when no reader exists.

## When this is on

`/easy-speak` with no argument turns it on for the whole session: from then on, substantive answers run Path A, and **artifacts the session produces run the artifact rules** — whether they are written to a file or handed over in chat. A question *about* communication research still goes down Path B, with its evidence obligations intact, even when the output is a document.

`/easy-speak <request>` applies it to that one request and does not change session state. The request is a **thing to do**, not a topic to explain: "/easy-speak write the README" writes the README under these rules.

Auto-activation — a comprehension-gap phrase, or a question about the research — applies it to one answer only. **A routine request to write documentation does not activate this skill.** "Write a README" is not a trigger; "readers don't understand this README, make it clearer" is.

On `/easy-speak off`, or any equivalent request to stop, leave session mode, drop back to the normal register immediately, and confirm in one line.

## Additional resources

Load on demand, not up front. Each is referenced inline at the step where it becomes relevant.

- **`references/audience-calibration.md`** — how much to explain, how to read the level from available evidence, why over-explaining is not a safe default for experts, and how to fix an audience you cannot ask. Load at step 1 when the depth is unclear.
- **`references/building-explanations.md`** — the relational skeleton test, the two-example rule, seductive details, jargon, signposting effect sizes, and what changes in a document a reader may enter part-way through. Load at step 3 when the concept is genuinely hard.
- **`references/comprehension-checks.md`** — verified phrasings for checking understanding, and the procedure when there is no receiver at all. Load at step 5.
- **`references/never-say-this.md`** — communication claims that died under adversarial verification (Mehrabian 7-38-55, the 8-second attention span, learning styles, Mayer's effect sizes), plus the writing-mode claims that do not survive. **Load whenever the user asks a question *about* communication, explaining, presenting, or how people learn — that is, a question about the claims themselves. Also load it before citing any research to justify a writing choice**, which is what the file's own writing section exists for. Not needed for ordinary writing or explaining tasks that make no research claim.
