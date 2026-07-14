---
description: Explain things so the user actually understands them. No argument turns on easy-speak mode for the session; an argument explains that one thing; "off" turns it off.
argument-hint: "[question or topic] | off"
---

Use the `easy-speak` skill. Read its `SKILL.md` now, before responding — it holds the loop, the evidence, and the prohibitions. Do not re-derive them from this file.

The user's argument was: `$ARGUMENTS`

Dispatch on it:

**Empty argument — turn on session mode.** Every substantive answer for the rest of this session runs the skill's Path A loop. Confirm in one or two lines, not a wall of text. If the user's background in whatever they are working on is not yet readable from the conversation, ask the single calibration question now so the next answer lands.

**`off`, `stop`, `그만`, or an equivalent — leave session mode.** Drop back to the normal register immediately and confirm in one line. Stop applying the loop.

**Anything else — treat it as the thing to explain.** Apply the skill's loop to that one answer, then stop; do not enter session mode.

Two reminders that the skill's own text emphasizes, because they are the failure modes that survive a careless read:

- **Infer the audience before asking about it.** The user asked a question; answering with a question is a poor first move. State the assumption in one clause and proceed. Ask only when the level is genuinely unreadable *and* it would materially change the answer.
- **The loop is not a template to fill.** If the honest answer is two sentences, it is two sentences.

Respond in the user's language.
