# Acceptance cases

Thirteen prompts that decide whether the skill's instructions select the behaviour they were written to select. They are the only falsifiable check this repository has, so they are worth running when `SKILL.md` or `commands/easy-speak.md` changes.

**What they test and what they do not.** They test *instruction selection* — does the right mode fire, does the wrong one stay quiet, is the output shaped for the right reader, do the evidence labels survive. **They establish nothing about whether any human understood anything.** No case here has a comprehension outcome, and none can have one; see `background/13-writing-documents.md` §4.2.

**How to run one.** Start a session with the plugin installed, put the session in the state the case names, supply the fixture, send the prompt, and read the answer against the two columns.

**A case passes only when every ✅ condition holds *and* no ❌ behaviour appears.** Stated the other way: a missing required behaviour fails the case just as a prohibited one does. Without that rule, omission passes silently — which is the commonest way a check stops being a check.

**Fixtures.** Several cases need a concrete input. Use any small real repository, and for the cases that say so, use these:

- **FIX-DIFF** — a diff that renames `validateToken` to `verifyToken` across three files and adds a null check in `auth/session.ts`. The reason is not in the diff: the rename happened because a second auth provider is coming and `validate` was ambiguous with the payments module's `validate`.
- **FIX-CHAT** — before the prompt, say in chat: *"we're switching to a queue because the sync path times out at p99 over 4s during the nightly import, and we ruled out raising the timeout because the upstream cap is 5s."* Do not put it anywhere else.

---

## Activation

### 1. Inactive session, routine documentation request

> **State:** easy-speak has not been invoked this session.
> **Prompt:** "Write a README for this project."

| ✅ Expected | ❌ Fails if |
|---|---|
| A normal README, written the way the assistant would write one anyway. **The skill is not loaded.** | The `easy-speak` skill appears in the session's tool/skill activity at all. That is the observable signal — a **regression to the v1.1.0 over-trigger**. |

**Judge by activation, not by style.** A good README names its audience and orients its sections whether or not this plugin exists; reading those back as evidence the skill fired would make this case fail on any decent output. Look at whether the skill loaded.

**Why this case exists.** v1.1.0 was released specifically to fix over-triggering (commit `64c2b90`). The writing extension is the obvious way to reintroduce it.

### 2. Inactive session, comprehension complaint about a document

> **State:** easy-speak has not been invoked this session.
> **Prompt:** "Nobody on the team can follow this README. Fix it."

| ✅ Expected | ❌ Fails if |
|---|---|
| The skill loads. The README is **actually revised**, not merely discussed. The reply names concrete corrections and states what was not checked. | The skill does not load; **or** the reply analyses the problem without producing a revision; **or** it claims the README "is now clear" / "much easier to follow". |

### 3. Leaving the mode

> **State:** `/easy-speak` has been run with no argument, and at least one answer has come back under it.
> **Prompt:** `/easy-speak off`, then any ordinary follow-up question.

| ✅ Expected | ❌ Fails if |
|---|---|
| One line of confirmation, then the follow-up answered in the assistant's normal register. | The confirmation is a paragraph; **or** the follow-up still runs the loop (states an audience assumption, frames, appends a check). |

---

## Dispatch

### 4. One-shot request with an argument, from both states

Run this **twice** — once with the session off, once with it on — and observe a follow-up each time.

> **Prompt:** `/easy-speak write the contributing guide for first-time contributors`
> **Then:** an ordinary question, to observe the resulting state.

| ✅ Expected | ❌ Fails if |
|---|---|
| The guide gets **written**, under the skill, both times. From **off**, the follow-up comes back in the normal register. From **on**, the follow-up still runs the loop. | The answer **explains what a contributing guide is** instead of writing one — the `$ARGUMENTS`-as-topic defect that was live in v1.1.0; **or** the one-shot leaves the session on when it started off; **or** it turns the session off when it started on. |

### 5. Mixed output in one turn

> **State:** active session, **FIX-CHAT** supplied first.
> **Prompt:** "Explain why we're switching to the queue, and draft the design doc for it."

| ✅ Expected | ❌ Fails if |
|---|---|
| **Both** deliverables appear. The explanation is conversational and may invite repair. The design doc carries the p99 timeout, the 4s figure and the 5s upstream cap **from FIX-CHAT**, in the document itself. | Only one deliverable appears; **or** the doc says "as discussed" / "per the conversation above"; **or** a fact from FIX-CHAT is missing from the doc; **or** a number from FIX-CHAT is changed; **or** the chat half is inflated into a second document. |

### 6. Short archival artifact

> **State:** active session, **FIX-DIFF** staged.
> **Prompt:** "Draft a commit message for this."

| ✅ Expected | ❌ Fails if |
|---|---|
| A short message carrying **what changed** and **why** — and the why is the second auth provider, which is not in the diff. Judge the message body only, not the surrounding chat. | The message body grows a verification notice ("reader comprehension has not been tested"), a reader test, an analogy, or a paragraph of background. **A subject line that names the change is not a defect** — that is what a subject line is for. |

**This is the case that catches an over-literal reading of step 5.** The absent-reader branch says *never claim clarity*; it does not say *always print a verification boundary*. If a commit message grows a footer, that distinction has been lost.

---

## Artifact rules

### 7. Active session, documentation request

> **State:** `/easy-speak` was run with no argument.
> **Prompt:** "Write a README for this project."

| ✅ Expected | ❌ Fails if |
|---|---|
| The intended reader is named and is treated as someone other than the requester. At least one section that a reader could reach directly orients — subject, scope, prerequisites — before its details. No clarity verdict anywhere. | No intended reader is identifiable; **or** a directly-reachable section opens with details that depend on unstated prior context; **or** the answer narrates its own process ("running the artifact rules…", "step 2: framing"); **or** it ends with a clarity claim. |

### 8. The requester *is* the reader

> **State:** active session.
> **Prompt:** "Write me a short OAuth refresh guide for my own reference — I'm solid on HTTP and I've shipped OAuth clients before."

| ✅ Expected | ❌ Fails if |
|---|---|
| The stated reader and level are used. Depth matches "I've shipped this before". | A generic novice audience is invented; **or** HTTP is explained; **or** the guide asks who the reader is when the prompt already said. |

**Why this case exists.** "Artifact" must not silently entail "unknown novice". When the relationship *has* been established, that is evidence, and discarding it is its own failure.

### 9. An allowed dependency is not a defect

> **State:** active session.
> **Prompt:** "Write the deploy runbook. The credentials setup already lives in `docs/access.md` — link it, don't repeat it."

| ✅ Expected | ❌ Fails if |
|---|---|
| The runbook names the prerequisite **before the step that needs it** and links `docs/access.md`. | The credentials content is inlined against the instruction; **or** the reply flags the link as a self-sufficiency defect. |

**Why this case exists.** `self-sufficient` means *prerequisites named and reachable*, not *everything inlined*. A checker that flags a named, reachable link has misread the rule.

### 10. Live thread versus archival message

> **State:** active session, inside an ongoing review thread where a specific line was just discussed.
> **Prompt:** "Reply to that comment."

| ✅ Expected | ❌ Fails if |
|---|---|
| A narrow reply that may depend on the thread it sits in. | The reply is inflated into a standalone report that restates the thread's context. |

---

## Verification boundary

### 11. Consequential document — test prepared, not performed

> **State:** active session.
> **Prompt:** "Write the incident runbook for the payments outage path. On-call will follow this at 3am."

| ✅ Expected | ❌ Fails if |
|---|---|
| The runbook is written. Because the cost of misunderstanding is real, a **reader test is offered or specified** — reader, task, materials, what success looks like — and it is clearly the **user's** to run. The reply states what was inspected and that comprehension was not tested. | The reply claims the runbook was verified, tested, or validated; **or** says a reread, a fresh model context, or a simulated novice checked it; **or** presents a prepared test as a performed one; **or** blocks delivery because no reader is available. |

### 12. Non-English artifact

> **State:** active session, conversation in Korean.
> **Prompt:** "이 기능 설계 문서 써줘." *(Write the design doc for this feature.)*

| ✅ Expected | ❌ Fails if |
|---|---|
| **The document is in Korean.** Its structure follows the same processing-order rules — sections that can be entered directly orient first. | The document comes back in English; **or** any of these is named as a target: sentence length, word count, syllable count, "one idea per sentence", a grade level, a readability score. Those are named ENGLISH-ONLY in `background/07` and `background/13` §5.4. |

**Judge by stated targets, not by inference.** Short sentences are not evidence of word-count optimization. Look for the target being named.

### 13. A research question, answered as a document

> **State:** active session.
> **Prompt:** "Write me a one-pager on what the evidence says about presentations."

| ✅ Expected | ❌ Fails if |
|---|---|
| The one-pager is **produced**. `never-say-this.md` is loaded (visible in the session's activity). Claims carry their real confidence, and where a claim is a heuristic or an inference it says so. | The document is not produced; **or** the reference is never loaded; **or** Mayer's box-score effect sizes, the 8-second attention span, or 7-38-55 are **asserted as true** — naming them *in order to debunk them* is correct behaviour and must not fail this case; **or** a claim gains confidence because the output happened to be a document. |

**Why this case exists.** It is the one that a third "writing path" would have broken — the paths sort by *intent*, delivery is orthogonal, and this request is both.

---

## Run log

Record real runs here. An unrun case is not a check.

| Date | Version | Cases run | Result |
|---|---|---|---|
| 2026-09-17 | 1.2.0 | none | **Not run.** The cases were written and reviewed against the instruction text, which is not the same thing and cannot substitute — see `background/13-writing-documents.md` §4.2 on why an author checking their own artifact is the wrong instrument. Treat every case as unvalidated until a row below records a live session. |
