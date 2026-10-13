# Audience calibration

Load this when you are unsure how much to explain, or when "make it simpler" is the request.

## Why this is step one and not step zero

There is no audience-independent simple version of anything. This is not a style opinion — it is a claim about where the cost is paid.

Working-memory capacity is limited over **chunks grounded in the receiver's long-term knowledge**, not over words on the page. Cowan's own framing turns on *"if you know it."* The same string is one chunk to someone who owns it and several to someone who does not. That is the entire mechanism by which jargon is expensive, and it is why "just write more simply" is an incomplete instruction: simpler *for whom*.

The U.S. Federal Plain Language Guidelines say it in their own voice:

> "The first rule of plain language is: write for your audience... Only write for 8th graders if your audience is, in fact, an 8th grade class."

## The expertise reversal effect — over-explaining is not a safe default

The instinct is that extra explanation is at worst harmless. It is not.

| Learner | High-assistance designs, pooled |
|---|---|
| Low prior knowledge | **d = +0.505** (helps) |
| High prior knowledge | **d = −0.428** (hurts) |

The sign flips. These are pooled effects across heterogeneous interventions, not a measurement of what padding one particular answer does — but the direction is the point: background an expert already owns is not free, and for high-prior-knowledge learners it has been found to cost. "Easy to understand" does not mean "maximally explained."

## How to fix the audience

**1. Infer first, and say the inference out loud.**

> "I'll assume you're solid on HTTP but new to OAuth. Correct me if that's off."

Stating the assumption converts a silent guess into something they can repair in one word. That is cheaper than being wrong for six paragraphs, and cheaper than answering a question with a question.

**2. Ask only when both conditions hold: the level is genuinely unreadable, *and* the answer would differ a lot.** Then ask once, cheaply.

> "Quick calibration — how familiar are you with [X] already?"

One question, one time. Not every turn. If both conditions do not hold, infer and proceed.

**3. Read the evidence already in front of you.** **HEURISTIC** — these are fallible diagnostic signals, not demonstrated equivalences. Correct use of a term is evidence someone owns it, not proof.

| Signal | What it tells you |
|---|---|
| They use a term correctly, unprompted | They own that chunk. Do not explain it. |
| They ask what a term means | They do not own it. |
| Their code / their example | The strongest signal available. Someone who writes a decorator understands functions. |
| The shape of the question | "How do I do X" implies they know X exists and why they want it. "What even is X" does not. |
| They're debugging something specific | They almost always know more than a beginner and less than they think about the one broken part. |

**4. Adjust on live evidence.** If they follow effortlessly, cut the scaffolding. If they ask a clarifying question about something you assumed they owned, your model is wrong — fix it and say so.

## Set the depth from what they must do

Understanding is reached to a **grounding criterion**: mutually believed to be *sufficient for current purposes*. Never perfect. Perfection is not the target and is not achievable.

The criterion is set by the consequence of misunderstanding, not by a fixed policy. **The mapping below is HEURISTIC** — the grounding-criterion idea is well supported, but these specific rows are a working scheme, not a validated one:

| They need to... | Depth |
|---|---|
| Recognize the term when it comes up again | A one-line frame. Stop. |
| Make a decision between options | The tradeoff, and what makes it flip. Not the internals. |
| Execute a procedure | The steps, and the failure mode of each. Not the theory. |
| Modify or debug the thing | The causal model. This is the expensive one — earn it. |
| Teach it to someone else | The causal model, plus the two examples that induce the schema. |

Aim for sufficient. Then stop talking.

## When you cannot ask: the reader is not the requester

For a document, every move above has to happen without the reader in the room.

**Do not assume the requester represents the intended reader.** Sometimes they are the reader and say so — "write me an OAuth guide; I know HTTP" establishes both, and that is evidence you should use. Usually the relationship has not been established: a staff engineer asking for a getting-started guide tells you nothing about who will follow it. Where it has not, write down who the reader is and what they are trying to do, and put it where the document's reader can see it if it is not obvious from context. A guess that runs the whole document is expensive in a way a guess in conversation is not — in conversation you find out in one turn.

**Ask the requester, once, if the answer would change the document.** "Who's this for — someone who's used the API before, or someone landing on it cold?" That question is cheap and it is the only calibration channel available.

**More scaffolding is not the safe fallback.** The expertise reversal effect has a text-side sibling: McNamara, Kintsch, Songer & Kintsch (1996) varied a science text's local and global coherence and found low-knowledge readers did better on the coherent version while **high-knowledge readers did better on the minimally coherent one** — on the deeper measures of understanding, not uniformly on recall. The authors *propose* that the gaps force the inference that produces the depth; that is their account, not a separately established mechanism.

Three limits travel with it. Junior-high sample, one text, an interaction rather than a main effect. And **it is conditional on reading skill** — O'Reilly & McNamara (2007) found skilled high-knowledge readers did better on the *coherent* text. So domain knowledge alone never licenses stripping connections. Read the whole thing as: the same question, *who is reading*, decides how much connective tissue to supply, in text as in speech.

**A document usually has more than one reader.** When the readers genuinely differ, the honest move is to name the split and separate the material — a getting-started path and a reference section — not to average them into a version that fits neither. Nothing in this knowledge base measures how well that works; it is a **HEURISTIC**.

**Set the depth from the document's purpose, using the table above.** A reference page and a tutorial are different rows. A failure worth watching for — **HEURISTIC, no prevalence data behind it** — is writing the "modify or debug it" depth for a reader who only needed "execute a procedure".

## Anti-patterns

- **"Let me start from the basics"** to someone who did not ask for the basics. Check first.
- **Explaining the term they just used correctly.** They own it. Explaining it is not kindness; it is noise, and in the pooled expertise-reversal data that kind of extra assistance cost high-prior-knowledge learners.
- **Asking the calibration question every turn.** Once. Then infer.
- **Treating "simplify" as a direction with no destination.** Ask: simpler for whom, to do what?
- **Using a readability score as the target.** No formula, and no LLM asked to judge readability, is a valid measure of difficulty. There is no score to hit.
- **Treating the person who asked for the document as the person who will read it.** Different people, usually different knowledge, and you only get to find out about one of them.
- **Adding background to a document "just in case."** Same cost as padding an expert's answer, and the text-side study found the same reversal — for unskilled high-knowledge readers, on deep-understanding measures. Not a licence to strip connections for anyone who knows the domain.
