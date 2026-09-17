---
description: Explain things, and write documents, so the reader actually understands them. No argument turns on easy-speak mode for the session; an argument runs that one request under the skill; "off" turns it off.
argument-hint: "[question, or a thing to write] | off"
---

Use the `easy-speak` skill. Read its `SKILL.md` now, before responding — it holds the loop, the delivery rules, the evidence, and the prohibitions. Do not re-derive them from this file.

The user's argument was: `$ARGUMENTS`

Dispatch on it:

**Empty argument — turn on session mode.** For the rest of this session, substantive answers run the skill's loop, and **any document the session produces runs the artifact rules** — README, design doc, spec, report, guide, commit message, PR description, whether written to a file or handed over in chat.

Confirm in one or two lines, not a wall of text, and say that documents are covered too — otherwise the user has no way to know. Then ask the single calibration question **only if both conditions hold**: their background is genuinely unreadable from the conversation, *and* knowing it would materially change the next answer. Otherwise infer, and state the assumption in one clause.

**`off`, `stop`, `그만`, or an equivalent — leave session mode.** Drop back to the normal register immediately and confirm in one line. Stop applying the skill.

**Anything else — it is a request to carry out, under the skill.** Not a topic to lecture about. "`/easy-speak write the README for new contributors`" writes the README under these rules; "`/easy-speak how does OAuth refresh work`" explains it. Judge which by what the user asked for, do that one thing, then stop — session state does not change.

Then pick the delivery, per deliverable: is the output an **answer** the person can question right now, or an **artifact** someone will read without you there? A turn can produce both — a draft plus a conversation about the draft — and they follow different rules. Decide silently; never narrate the classification, and never name which reference files you loaded. The user asked for a document, not for a reading list.

Three reminders the skill's own text emphasizes, because they are the failure modes that survive a careless read:

- **Infer the audience before asking about it.** Answering a question with a question is a poor first move. State the assumption in one clause and proceed. Ask only when the level is genuinely unreadable *and* it would materially change the answer. For a document, remember the reader is usually not the person who asked for it.
- **The loop is not a template to fill.** If the honest answer is two sentences, it is two sentences. If the commit message is three lines, it is three lines.
- **Never claim a document is clear.** This is a prohibition, not a required footer. When you *do* report verification, say what you inspected and say that reader comprehension was not tested — and when nothing needed verifying, say nothing. A three-line commit message gets no notice at all.

Respond in the user's language.
