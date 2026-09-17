# easy_speak — background knowledge base

The research behind the skill: what actually makes a listener or reader understand you, what the evidence supports, and — just as important — what it does not.

Every factual line in these documents is traceable to a source that was fetched and read. Nothing was written from memory.

## Start here

If you read one file, read **[10-actionable-rules.md](10-actionable-rules.md)**. It is the operational file; the rest is the evidence behind it.

If you are about to assert something confident about communication, read **[09-myths-and-contested-claims.md](09-myths-and-contested-claims.md)** first. This field is unusually polluted, and the most quotable claims are the least sound.

## The one-paragraph answer

Being understood is not a property of a well-formed message. It is a state you and the other person reach together, and it has to be engineered against two hard constraints. The first is that **you cannot perceive your own clarity** — knowing a thing destroys your ability to model not knowing it, and no amount of effort, incentive, or feedback repairs that. The second is that **the cost of your message is paid in the receiver's chunks, not in your words** — the same sentence is one unit to an expert and a dozen to a novice, which is why there is no audience-independent "simple" version of anything. Everything else follows: give the frame before the details, make the structure visible, build explanations from relations rather than resemblances, and — because the first constraint means you will never feel the failure — **make the other person produce something back**, because their restatement is the only instrument that measures what actually landed.

## The documents

| # | Document | What it answers |
|---|---|---|
| 01 | [How understanding works](01-how-understanding-works.md) | Memory, chunks, cognitive load — and why the famous capacity numbers are not a bullet-point budget |
| 02 | [The curse of knowledge](02-curse-of-knowledge.md) | Why your sense of your own clarity is not evidence, and what the tapping study really showed |
| 03 | [Grounding and dialogue](03-grounding-and-dialogue.md) | Understanding as joint work; why nods and "any questions?" are worthless; Grice and his limits |
| 04 | [Structure and ordering](04-structure-and-ordering.md) | Frame-before-details is strongly supported. BLUF is not. They are not the same claim |
| 05 | [Explaining to non-experts](05-explaining-to-non-experts.md) | Analogy, worked examples, concreteness, and what jargon actually costs |
| 06 | [Presentations and multimedia](06-presentations-and-multimedia.md) | Real effect sizes from independent meta-analyses — not the author's own vote-counts |
| 07 | [Plain language and writing](07-plain-language-and-writing.md) | The standards, the readability trap, and the one signal that survives cross-linguistically |
| 08 | [Checking comprehension](08-checking-comprehension.md) | The only move that verifies understanding instead of assuming it |
| 09 | [Myths and contested claims](09-myths-and-contested-claims.md) | 7-38-55, the 8-second attention span, learning styles, and 20+ claims that died under verification |
| 10 | [The rule set](10-actionable-rules.md) | The distilled, checkable rules, each traceable to its evidence and its confidence tier |
| 11 | [Bibliography](11-bibliography.md) | All 74 adjudicated sources plus the 18 quote-checked writing-mode entries, with citation-hygiene warnings |
| 12 | [Open questions](12-open-questions.md) | How this was built, what is still unknown, and what must not be relied on |
| 13 | [Writing documents](13-writing-documents.md) | When the reader is not in the room: does revising help, what a non-linear reader needs, what the medium costs, what an author can check alone |
| 14 | [Software documentation](14-software-documentation.md) | READMEs, API docs, commit messages, code review — and why this layer is descriptive rather than causal |

**Documents 13 and 14 are a weaker evidence tier and say so on their first screen.** They were added after the two verification passes, so their sources — 18 catalogued entries linking 29 URLs — were fetched and quote-checked once, not sent to three verifiers instructed to refute them. Nothing in them carries a `3-0`. Given that 38% of everything comparable that *was* adjudicated did not survive, treat the difference as real.

## Five findings that change how you'd build this skill

**You cannot check your own clarity, so the skill must not let you try.** Newton's tappers predicted listeners would identify ~50% of tapped songs. The true rate was 3 out of 120 — a figure below every single prediction any tapper made. Paying people to be accurate does not fix it; telling them the outcome does not fix it. The only instrument that works is the receiver producing something back.

**"Frame first" and "conclusion first" are different claims with very different evidence.** Stating the topic before the details roughly doubled both comprehension and recall on word-for-word identical text — and a topic delivered *late* was no better than no topic at all. But BLUF (conclusion before reasoning) has no comprehension evidence here, and in the one head-to-head, a chronological narrative beat the inverted pyramid on both comprehension and cognitive load. BLUF may still be right for triage. It should not be sold as a comprehension rule.

**Readability formulas are the wrong instrument — and asking an LLM to judge readability is no better.** Both were tested against eye-tracking data and both failed. The one signal with genuine cross-linguistic support is **surprisal**, validated across 11 languages in 5 families (including Korean). Use it to *locate* hard passages. Never use it as a rewrite target — that is exactly the Goodhart failure that discredited the formulas.

**Most "debunked" claims are not lies; they are one step of overreach on a real finding.** Mayer's design principles do work — but the famous effect sizes are the author's own vote-counts, and independent meta-analyses land at a third of the size. The behavioural effects are real while the cognitive-load explanation everyone gives for them is *not* supported. Flattening this into "true" or "false" loses the thing you actually needed to know.

**When you write a document, the only valid check is gone, and nothing replaces it.** Revising documents demonstrably helps real readers — for one U.S. Department of Veterans Affairs letter, the share of veterans who *failed to understand* it fell from 56% to 11% — but every one of those results came from changing several things at once, so none of them prices an individual rule. And the instrument that produced them was *readers*, not the author. An author can inspect a draft for undefined terms, dangling referents and missing preconditions; an author cannot certify that anyone will understand it, and neither can a language model rereading its own output. Finishing a document with reader comprehension untested is the normal outcome. Claiming otherwise is the failure. See [13-writing-documents.md](13-writing-documents.md).

## How this was built

Two multi-agent research passes, then adversarial verification.

Claims were extracted only from primary sources that were actually fetched. Each claim was then sent to **three independent verifiers instructed to refute it** — to retrieve the source themselves, confirm the quote appeared verbatim, and hunt for contradicting evidence. Two refutations out of three kill a claim.

| | Sources | Claims extracted | Adjudicated | Confirmed | Refuted |
|---|---|---|---|---|---|
| Pass 1 — broad | 28 | 139 | 60 | 32 | 28 |
| Pass 2 — targeted gaps | 10 topics | 70 | 70 | 48 | 22 |

Refuted claims were **kept, not discarded** — they are the raw material of document 09, and they are the reason this knowledge base can tell you what *not* to say.

**The honest limit:** a claim that survived three skeptical readers who each opened the primary source is stronger than an unchecked citation. It is not peer review. See [12-open-questions.md](12-open-questions.md).

## Conventions used throughout

- **`3-0`** — unanimous under adversarial verification. **`2-1`** — split; the direction is likely sound, the magnitude is not.
- **REFUTED** — killed on merit. The refutation reasoning is preserved, because it is usually the more useful half.
- **UNVERIFIED** — extracted but never adjudicated. Never rely on it.
- **QUOTE-CHECKED** — documents 13 and 14 only. The source was fetched and the quote read in the primary document, one pass, no adversarial round. Weaker than `3-0`, stronger than UNVERIFIED.
- **INFERENCE** — a rule derived from a source that did not test it. Never cite the source as if it did.
- **HEURISTIC** — a useful smell-test with no study behind it. Labelled as such every time it appears.
- **ENGLISH-ONLY** — an artifact of English that must not be generalized (readability formulas, word counts, focal stress, cleft constructions, English backchannels).

The default stance is language-neutral. Where a finding is cross-linguistically established, it says so. Where it is not, it says that too.
