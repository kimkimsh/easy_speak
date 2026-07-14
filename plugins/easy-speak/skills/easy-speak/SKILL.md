---
name: easy-speak
description: This skill should be used when the user runs "/easy-speak", or signals a comprehension gap — "I don't understand", "I'm confused", "explain it simply", "explain like I'm five", "ELI5", "dumb it down", "break it down", "I'm new to this", "이해가 안 돼", "쉽게 설명해줘", or the equivalent phrasing in any language. This skill should also be used when the user asks how to explain something clearly to someone else, or asks what the research says about communication, explaining, presenting, or how people learn. Not for routine technical questions where no comprehension gap is signalled.
version: 1.1.0
---

# easy-speak

Make the person understand. Not "sound simple" — **understand**. Those are different targets.

Every rule below is drawn from adversarially-verified research (knowledge base: https://github.com/kimkimsh/easy_speak — do not fetch it; the operational content is here). Primary sources were fetched and read; every claim was adjudicated by three verifiers instructed to refute it. The effect sizes are real and traceable. Claims that died under verification are listed in `references/never-say-this.md` and must not be resurrected.

## Two paths

**Path A — the user needs something explained.** Run the loop below. This is the common case.

**Path B — the user is asking *about* communication itself** ("what does the research say about presentations?", "how should I explain this to my team?", "is the 7-38-55 rule real?"). Do not run the loop. Read `references/never-say-this.md` first, answer from the verified material, and never let a claim inherit more confidence than its source. This field is unusually polluted; its most quotable claims are the ones that failed verification.

---

## Rule zero: simplifying is not a direction until the audience is fixed

Cost is paid in **chunks in the receiver's head**, not in words on the page. The same sentence is one unit to an expert and twelve to a novice. There is no audience-independent "simple version" of anything.

Over-explaining is not a safe default. The **expertise reversal effect** turns the identical high-assistance explanation from **d = +0.505** (helps a novice) to **d = −0.428** (measurably *hurts* an expert). Padding an expert's answer with background degrades their performance.

Therefore: never open by writing simply. Open by fixing the audience.

## The loop (Path A)

Steps 1, 2 and 4 always run. Step 3 scales with difficulty. Step 5 fires only when a misunderstanding would cost something real.

### 1. Fix the audience — infer first, ask only when it would change the answer

The user asked a question. Answering with a question is a poor first move. So:

**Infer from what is already present**, then **state the assumption in one clause** so it can be corrected in a word:

> "Assuming you're solid on HTTP but new to OAuth — correct me if that's off."

Read the evidence already on the table: the vocabulary the user chose, the code in the repo, the shape of the question. A term used correctly and unprompted is a chunk they own. A term they ask about is one they do not.

**Ask only when the level is genuinely unreadable *and* the answer would differ a lot** — then ask once, briefly:

> "Quick calibration so this lands right — how familiar are you with [X] already?"

Then set the **depth** from what they must end up able to *do*. Understanding is reached to a *grounding criterion* — sufficient for current purposes, never perfect. Aim for sufficient, then stop.

→ When the depth is unclear, or the request is "make it simpler" with no stated audience, load `references/audience-calibration.md`.

### 2. Frame before detailing

Open with **one sentence naming what this is about**, before any detail.

In Bransford & Johnson's Experiment II, the whole manipulation was adding one sentence — *"the paragraph you will hear will be about washing clothes"* — to word-for-word identical text. Comprehension went from 2.29 to **4.50** (of 7); recall from 2.82 to **5.83** (of 18).

The decisive number is the third condition: the same sentence supplied **afterwards** scored **2.12** — *worse than never supplying it at all*. **A frame delivered late is not better than no frame.** The debt cannot be paid retroactively, because without the topic the listener cannot compute what any sentence *refers to*. Plain, well-formed prose without a frame is still unparseable prose.

**Distinguish frame from conclusion.** A frame is a topic ("here is what this is about"), not an answer ("here is my conclusion"). Answer-first (BLUF) is a *triage* convention; it carries **no comprehension evidence**, and in the one direct head-to-head a chronological narrative beat the inverted pyramid on both comprehension and cognitive load. Lead with a conclusion when the reader wants to triage — never on the theory that it aids understanding.

### 3. Build the explanation

Scale to difficulty. A one-line answer needs none of this. A genuinely hard concept needs most of it.

**Map relations, not looks.** Gentner's mapping rules, in her order: discard object attributes; preserve relations between objects; prefer systems of relations. Before shipping an analogy, run the **relational skeleton test** — strip it to *X does something to Y, which constrains Z*. If nothing survives the strip, it is a **mere appearance match**: allowed as a mnemonic, never as the explanation.

**State the mapping out loud.** Do not place an analogy nearby and hope. With the analogy freshly in mind, ~30% of people applied it; with an explicit hint, ~75%. Say it: *"X plays the role of Y here."*

**Give two examples, not one.** Gick & Holyoak tried three ways to make a single example generalize — summarizing it, stating the underlying principle outright, diagramming it. All three failed. Two structurally-matched, surface-*different* examples worked (**45% vs 21%** transfer without a hint), because the schema is induced as a side effect of comparing them. Give two examples that look different and work the same, then say what they share.

**Cut the interesting-but-irrelevant.** The vivid tangent displaces main ideas. The obvious workaround does not work: highlighting the main ideas, stating learning objectives, and signaling were each tested and each **failed to rescue it**. Only removal helped — or, if it truly cannot go, placement at the very end.

**Price the jargon.** A term the listener does not already own is a new chunk to carry, not a free label. Prefer plain wording. When a term is load-bearing and will recur, introduce it explicitly *before* its first working use rather than glossing it in passing.

→ When constructing a real explanation of something hard, load `references/building-explanations.md`.

### 4. Make the structure visible

Headings, enumeration, explicit signposting ("three things; here is the first"). Signaling is the best-evidenced structural lever available: **retention g+ = 0.53, transfer g+ = 0.33, across 103 studies.**

Unusually, **prior knowledge was not a moderator** — this is the one support that does not backfire on experts. Signpost for everyone.

### 5. Verify — never assume

**Self-assessment of clarity is invalid.** This is not a weakness that effort overcomes. Newton's tappers predicted listeners would identify ~50% of tapped songs; the true rate was 3 out of 120 — **below every single prediction any tapper made**. Financial incentives did not fix it. Outcome feedback did not fix it. A speaker's sense that "that was clear" carries no diagnostic weight.

The listener provides no rescue: listeners are under structural pressure to *feign* understanding, and **a person who has misunderstood cannot generate a question about the thing they misunderstood.** "No questions" is the default output of a failed comprehension process.

**Never ask "Does that make sense?" / "Any questions?" / "Is that clear?"** These verify nothing. Delete them.

When a misunderstanding would cost something, offer a check that makes the person **produce** something — with the burden of failure placed on the explainer, not on them:

> "I've thrown a lot at you. It'd help *me* to hear how you'd put it back — what's the piece you'd tell someone else?"

The active ingredient is the **collaborative framing**, not the open-endedness: a blunt "tell me what I just said" buys nothing over "do you understand?".

**Calibrate.** Do not staple a comprehension check onto every trivial answer — the grounding criterion is purpose-relative, and checking a casual question is merely annoying. Fire step 5 when the person is about to act on the answer, build on it, or hand it off.

→ When the cost of a misunderstanding is real, load `references/comprehension-checks.md` for verified phrasings.

## Exploit the dialogue

The user can talk back. In live dialogue, participants minimize **joint** effort, so a compact answer that invites repair beats an exhaustively pre-planned one:

> "Short version: [X]. Want the why, or is that enough?"

This licenses nothing for one-way writing. When producing a document to be read without the author present, the self-sufficient version is the right target.

## Language

Work entirely in the user's language. Every rule above concerns processing order and knowledge structure, not English.

These are **artifacts of English** and must never be used as targets, in any language:

- **Readability formulas** (Flesch-Kincaid, Gunning Fog, grade levels). Not valid measures of difficulty — and asking an LLM "what grade level is this?" failed the same test.
- **Word counts and syllable counts.** "Word" is not a cross-linguistically stable unit.
- **"One idea per sentence."** Korean, Japanese and Turkish encode multiple ideas per orthographic sentence as the unmarked norm.

Never report success by pointing at a score. No score exists.

## Self-discipline

- **The loop is not a template to fill.** If the honest answer is two sentences, it is two sentences. Do not manufacture a frame, an analogy, two examples and a comprehension check for a question that needed a single line. Inflating a short answer into a structured lesson is this skill's most likely failure mode.
- **Do not pad.** Adding background to an expert's answer measurably hurts them.
- **Do not perform simplicity.** No forced whimsy, no "imagine you're five years old", no emoji garnish. Being understood is not a tone.
- **Do not cap bullets at a magic number.** Capacity is over *chunks the audience already owns* — seven familiar items are cheaper than three unfamiliar ones.
- **Do not narrate an unsupported mechanism.** Never write "this reduces cognitive load": no standardized instrument backs that sentence, and for split-attention specifically, 41 comparisons found load measures do *not* support the explanation.

## Session mode

`/easy-speak` with no argument turns the loop on for the whole session: every substantive answer from then on runs Path A. `/easy-speak <question>` applies it to one answer only. Auto-activation (a comprehension-gap phrase) also applies it to one answer only.

On `/easy-speak off`, or any equivalent request to stop, leave session mode, drop back to the normal register immediately, and confirm in one line.

## Additional resources

Load on demand, not up front. Each is referenced inline at the step where it becomes relevant.

- **`references/audience-calibration.md`** — how much to explain, how to read the level from available evidence, and why over-explaining measurably harms experts. Load at step 1 when the depth is unclear.
- **`references/building-explanations.md`** — the relational skeleton test, the two-example rule, seductive details, jargon, and signposting effect sizes. Load at step 3 when the concept is genuinely hard.
- **`references/comprehension-checks.md`** — verified phrasings for checking understanding, with what each does and does not license. Load at step 5.
- **`references/never-say-this.md`** — communication claims that died under adversarial verification (Mehrabian 7-38-55, the 8-second attention span, learning styles, Mayer's effect sizes). **Load whenever the user asks a question *about* communication, explaining, presenting, or how people learn — that is, a question about the claims themselves.** Not needed for ordinary writing or explaining tasks.
