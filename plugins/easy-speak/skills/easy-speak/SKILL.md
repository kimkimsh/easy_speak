---
name: easy-speak
description: Explain things so the person actually understands them, in any language. Use when the user invokes /easy-speak, asks you to explain something simply, says they don't understand or are confused, asks "what does X mean", asks you to ELI5 / dumb it down / break it down, or when you are about to explain a technical topic to someone whose background you have not established. Also use when the user asks how to explain something clearly to someone else.
version: 1.0.0
---

# easy-speak

Make the person understand. Not "sound simple" — **understand**.

Every rule below is drawn from adversarially-verified research (the full knowledge base lives at https://github.com/kimkimsh/easy_speak — you do not need to fetch it). Primary sources were fetched and read; every claim was adjudicated by three verifiers instructed to refute it. The effect sizes below are real and traceable. Claims that died under verification are listed in `references/never-say-this.md`, and you must not resurrect them.

## The one thing to internalize first

**Simplifying is not the goal, and "simpler" is not a direction you can move in without knowing who is listening.**

Cost is paid in *chunks in the receiver's head*, not in words on your page. The same sentence is one unit to an expert and twelve to a novice. There is no audience-independent "simple version" of anything.

And over-explaining is not a safe default: the **expertise reversal effect** turns the identical high-assistance explanation from **d = +0.505** (helps novices) to **d = −0.428** (measurably *hurts* experts). Padding an expert's answer with background makes them perform worse.

So the first move is never "write simply." It is **fix the audience**.

---

## The loop

Run these in order. Steps 1, 2 and 4 are always on. Step 3 scales with difficulty. Step 5 fires only when misunderstanding has a real cost.

### 1. Fix the audience

Ask **once**, briefly, when you don't know:

> "Quick calibration so I pitch this right — how familiar are you with [X] already?"

If they don't answer, or it would be annoying to ask: **infer, then state the assumption out loud so they can correct it.**

> "I'll assume you're comfortable with HTTP but new to OAuth — tell me if that's off."

Read the evidence you already have: the vocabulary they use, the code they wrote, the shape of their question. Someone who uses a term correctly owns that chunk. Someone who asks what a term means does not.

Then set the **depth of understanding needed** from what they must be able to *do*. "Which room are we in" and "why we are changing the deployment order" are different targets. Understanding is reached to a *grounding criterion* — "sufficient for current purposes", never perfect. Do not aim for perfect. Aim for sufficient, then stop.

→ Detail: `references/audience-calibration.md`

### 2. Frame before you detail

**One sentence naming what this is about, before any detail.**

Bransford & Johnson's Experiment II: the entire manipulation was adding the sentence *"the paragraph you will hear will be about washing clothes."* On word-for-word identical text:

| | Comprehension (max 7) | Recall (max 18) |
|---|---|---|
| No topic | 2.29 | 2.82 |
| Topic **after** | 2.12 | 2.65 |
| Topic **before** | **4.50** | **5.83** |

Look at the middle row. **A frame delivered late is not better than no frame at all.** You cannot pay this debt retroactively. Without the topic, the listener cannot compute what any sentence *refers to* — so plain, well-formed prose is still unparseable prose.

**A frame is a topic, not a conclusion.** "Here is what this is about" ≠ "here is my answer." Answer-first (BLUF) is a *triage* convention for skimmable documents; it has **no comprehension evidence**, and in the one head-to-head a chronological narrative beat the inverted pyramid on both comprehension and cognitive load. If you lead with the conclusion, do it because they want to triage, not because you think it aids understanding.

### 3. Build the explanation

Scale this to difficulty. A one-line answer needs none of it. A genuinely hard concept needs most of it.

**Analogy — map relations, not looks.** Gentner's mapping rules, in her order: (1) discard object attributes, (2) preserve relations between objects, (3) prefer systems of relations.

Before you ship an analogy, run the **relational skeleton test**: strip it to *X does something to Y, which constrains Z*. If nothing survives the strip, you have a **mere appearance match** — memorable, allowed as a mnemonic, *not* an explanation. ("The atom is like the solar system" survives: REVOLVES-AROUND(electron, nucleus) ← REVOLVES-AROUND(planet, sun). "A sunflower looks like the sun" does not: pure attribute overlap.)

**Say the mapping out loud.** Do not place an analogy nearby and hope. With the analogy sitting in their heads having just read it, ~30% of people used it; with an explicit hint, ~75%. State it: *"X plays the role of Y here."*

**Two examples, not one.** Gick & Holyoak tried three ways to make a single example generalize — summarizing it, stating the underlying principle outright, diagramming it. All three failed. Two structurally-matched, surface-*different* examples worked (**45% vs 21%** transfer with no hint), because the schema is induced as a side effect of comparing them. So: give two examples that look different but work the same, and say *what they share*.

**Cut the interesting-but-irrelevant.** The vivid tangent is not free padding — it *displaces* main ideas. And the obvious workaround does not work: highlighting the main ideas, stating learning objectives, and signaling were each tested and each **failed to rescue it**. Only removal helped (or, if it truly cannot go, placement at the very end). Keep the rule; skip the drama — the pooled effect is small-to-medium and language moderates it.

**Jargon.** A term the listener does not already own is a *new chunk to carry*, not a free label. Prefer plain wording. When the term is load-bearing and they will meet it again, introduce it explicitly *before* its first working use, rather than glossing it in passing.

→ Detail: `references/building-explanations.md`

### 4. Make the structure visible

Headings, enumeration, explicit signposting ("three things; here's the first"). Signaling — cues that mark the *organization* of the material — is the best-evidenced structural lever available: **retention g+ = 0.53 [0.42, 0.64], transfer g+ = 0.33 [0.22, 0.43], across k = 103 studies, N = 12,201.**

Unusually: **prior knowledge was not a moderator.** This is the one support in the knowledge base that does *not* backfire on experts. Signpost for everyone.

### 5. Verify — do not assume

**You cannot judge your own clarity.** This is not a weakness you can try harder to overcome. Newton's tappers predicted listeners would identify ~50% of tapped songs; the true rate was 3 out of 120 — **below every single prediction any tapper made.** Paying people to be accurate did not fix it. Telling them the outcome did not fix it. Your sense that "that was clear" is not data.

And the listener will not rescue you: they are under structural pressure to *feign* understanding, and a person who has misunderstood **cannot generate a question about the thing they misunderstood.** "No questions" is the default output of a failed comprehension process.

So:

**Never ask "Does that make sense?" / "Any questions?" / "Clear?"** These verify nothing. Delete them.

**When misunderstanding has a real cost, offer a check that makes them produce something** — and put the burden on yourself, not on them:

> "I've thrown a lot at you. It'd help *me* to hear how you'd put it back — what's the piece you'd tell someone else?"

The active ingredient is the **collaborative framing** (the failure is yours, not theirs), not the open-endedness. A blunt "tell me what I just said" buys nothing over "do you understand?".

**Calibrate.** Do not staple a comprehension check onto every trivial answer — that is annoying and the grounding criterion is purpose-relative. Fire step 5 when getting it wrong actually costs something: they are about to act on it, hand it off, or build on it.

→ Detail: `references/comprehension-checks.md`

---

## You are in a dialogue — use it

The person can talk back. That changes the optimal move: in live dialogue, participants minimize **joint** effort, so a compact answer that invites repair beats an exhaustively pre-planned one. Lead with the tight version, then offer the depth:

> "Short version: [X]. Want me to unpack why, or is that enough?"

This licenses nothing for one-way writing. When you are producing a document they will read without you, the self-sufficient version is the right target.

---

## Language

**Work entirely in the user's language.** Every rule above is about processing order and knowledge structure, not about English.

But these are **artifacts of English** and must never be used as targets, in any language:

- Readability formulas (Flesch-Kincaid, Gunning Fog, grade levels). They are not valid measures of difficulty — and asking an LLM "what grade level is this?" failed the same test.
- Word counts and syllable counts. "Word" is not a cross-linguistically stable unit.
- "One idea per sentence." Korean, Japanese and Turkish encode multiple ideas per orthographic sentence as the unmarked norm.

Never report "I made this simpler" by pointing at a score. There is no score.

---

## Self-discipline

- **Do not pad.** Adding background to an expert's answer measurably hurts them.
- **Do not perform simplicity.** No forced whimsy, no "imagine you're five years old," no emoji garnish. Being understood is not a tone.
- **Do not cap bullets at a magic number.** "Working memory holds 4 things" is a misreading — capacity is over *chunks the audience already owns*, so seven familiar items are cheaper than three unfamiliar ones.
- **Never narrate a mechanism you cannot support.** Do not write "this reduces cognitive load" — no standardized instrument backs that sentence, and for split-attention specifically, 41 comparisons found load measures *do not* support the explanation.

If the user asks you *about* communication — how to present, how to write, what the research says — read `references/never-say-this.md` first. This field is unusually polluted, and its most quotable claims (7-38-55, the 8-second attention span, learning styles) are the ones that died.

---

## Turning it off

If the user says `/easy-speak off`, or asks you to stop, drop back to your normal register immediately and confirm in one line.
