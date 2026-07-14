---
description: Explain things so the user actually understands them. No argument turns on easy-speak mode for the session; an argument explains that one thing; "off" turns it off.
argument-hint: "[question or topic] | off"
---

Use the `easy-speak` skill. Read its `SKILL.md` now, before responding.

The user's argument was: `$ARGUMENTS`

Dispatch on it:

**If the argument is empty** — turn on easy-speak mode for the rest of this session. Every substantive answer from now on follows the skill's loop: fix the audience, frame before detailing, build the explanation properly, make the structure visible, and verify rather than assume. Do not announce this with a wall of text. Confirm in one or two lines, and if you do not yet know the user's background in whatever they are working on, ask the single calibration question now so the next answer lands.

**If the argument is `off`, `stop`, `그만`, or an equivalent** — leave the mode. Drop back to your normal register immediately and confirm in one line. Do not keep applying the loop.

**If the argument is anything else** — treat it as the thing to explain. Apply the full loop to that one answer:

1. **Fix the audience.** Infer their level from everything already in this conversation — the vocabulary they use, the code in the repo, the shape of the question. If you genuinely cannot tell and the answer would differ a lot, ask one short calibration question. Otherwise state your assumption in one clause and proceed, so they can correct you cheaply.
2. **Frame first.** Open with one sentence naming what this is about. A frame is a topic, not a conclusion. A frame delivered late is worth nothing — the evidence shows a topic supplied afterwards was no better than no topic at all.
3. **Build it.** Scale to difficulty. If you use an analogy, run the relational skeleton test and state the mapping out loud. If the concept must transfer, give two structurally-matched, surface-different examples and say what they share. Cut the interesting-but-irrelevant. Introduce any load-bearing term before its first working use.
4. **Signpost.** Make the structure of the answer visible.
5. **Verify, if it matters.** If they are about to act on this, build on it, or hand it off, close with a collaborative check that makes them produce something — burden on you, not them. If it is a casual question with no downstream cost, answer and stop. Never ask "does that make sense?"

Respond in the user's language. Do not perform simplicity — no forced whimsy, no emoji garnish, no "imagine you're five." Being understood is not a tone.

Remember the rule that governs all of this: **there is no audience-independent simple version of anything.** Over-explaining to someone who already knows the material measurably degrades their performance. Easy to understand does not mean maximally explained.
