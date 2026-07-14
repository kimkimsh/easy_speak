# Audience calibration

Load this when you are unsure how much to explain, or when "make it simpler" is the request.

## Why this is step one and not step zero

There is no audience-independent simple version of anything. This is not a style opinion — it is a claim about where the cost is paid.

Working-memory capacity is limited over **chunks grounded in the receiver's long-term knowledge**, not over words on the page. Cowan's own framing turns on *"if you know it."* The same string is one chunk to someone who owns it and several to someone who does not. That is the entire mechanism by which jargon is expensive, and it is why "just write more simply" is an incomplete instruction: simpler *for whom*.

The U.S. Federal Plain Language Guidelines say it in their own voice:

> "The first rule of plain language is: write for your audience... Only write for 8th graders if your audience is, in fact, an 8th grade class."

## The expertise reversal effect — over-explaining is not a safe default

The instinct is that extra explanation is at worst harmless. It is not.

| Learner | Same high-assistance explanation |
|---|---|
| Low prior knowledge | **d = +0.505** (helps) |
| High prior knowledge | **d = −0.428** (hurts) |

The sign flips. Padding an expert's answer with background they already own does not slide off them — it degrades their performance. "Easy to understand" does not mean "maximally explained."

## How to fix the audience

**1. Ask once, cheaply.**

> "Quick calibration — how familiar are you with [X] already?"

One question, one time. Not every turn.

**2. If they don't answer, infer — then say the inference out loud.**

> "I'll assume you're solid on HTTP but new to OAuth. Correct me if that's off."

Stating the assumption converts a silent guess into something they can repair in one word. That is cheaper than being wrong for six paragraphs.

**3. Read the evidence already in front of you.**

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

The criterion is set by the consequence of misunderstanding, not by a fixed policy:

| They need to... | Depth |
|---|---|
| Recognize the term when it comes up again | A one-line frame. Stop. |
| Make a decision between options | The tradeoff, and what makes it flip. Not the internals. |
| Execute a procedure | The steps, and the failure mode of each. Not the theory. |
| Modify or debug the thing | The causal model. This is the expensive one — earn it. |
| Teach it to someone else | The causal model, plus the two examples that induce the schema. |

Aim for sufficient. Then stop talking.

## Anti-patterns

- **"Let me start from the basics"** to someone who did not ask for the basics. Check first.
- **Explaining the term they just used correctly.** They own it. Explaining it is not kindness; it is noise, and to an expert it is measurably harmful.
- **Asking the calibration question every turn.** Once. Then infer.
- **Treating "simplify" as a direction with no destination.** Ask: simpler for whom, to do what?
- **Using a readability score as the target.** No formula, and no LLM asked to judge readability, is a valid measure of difficulty. There is no score to hit.
