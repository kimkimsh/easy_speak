# easy-speak

**A Claude Code plugin that makes Claude explain things so you actually understand them.**

Not "sound simple." *Understand.* Those are different targets, and the research is fairly brutal about the difference.

Works in any language.

---

## Install

```bash
/plugin marketplace add kimkimsh/easy_speak
/plugin install easy-speak@easy-speak
```

Then restart Claude Code (or start a new session).

## Use

| Command | What happens |
|---|---|
| `/easy-speak` | Turns on easy-speak mode for the session. Every answer from here follows the loop. |
| `/easy-speak <question>` | Explains that one thing, properly. Mode stays off. |
| `/easy-speak off` | Back to normal. |

The skill also activates on its own when you say things like *"I don't understand this"*, *"explain it simply"*, or *"what does this even mean"*.

---

## Why this isn't just "write simpler"

Three findings shaped the whole design.

**1. There is no simple version of anything — only a version that fits a particular head.**

Cost is paid in *chunks in the receiver's memory*, not in words on the page. The same sentence is one unit to an expert and twelve to a novice.

Which means "simplify" is not a direction you can move in until you know who is listening. Worse, over-explaining is not a safe default — the **expertise reversal effect** flips the identical explanation from **d = +0.505** (helps a novice) to **d = −0.428** (measurably *hurts* an expert). Padding an expert's answer makes them perform worse.

So easy-speak's first move is not "write simply." It is **fix the audience** — ask once, or infer and say the assumption out loud so you can correct it in one word.

**2. Claude cannot judge its own clarity. Neither can you.**

In Newton's study, people tapped out a famous song and predicted how many listeners would name it. They guessed ~50%. The real answer was **3 out of 120** — *below every single prediction anyone made*. Not one person was pessimistic enough.

This doesn't respond to effort. Paying people to be accurate didn't fix it. Telling them the outcome didn't fix it.

So the skill never asks *"does that make sense?"* — a question that cannot be answered by someone who misunderstood, and that people answer "yes" to under social pressure anyway. When getting it wrong actually costs something, it asks you to **put it back in your own words**, with the burden of failure on Claude rather than on you.

**3. Give the frame before the details — and know that "frame" is not "conclusion."**

Adding one sentence naming the topic *before* a passage roughly doubled both comprehension and recall on word-for-word identical text. Adding the same sentence *afterwards* was **no better than never adding it** — you cannot pay that debt retroactively.

But answer-first (BLUF) is a different claim, and it does **not** have the same evidence. It is a triage convention for skimmable documents. In the one direct head-to-head, a chronological narrative beat the inverted pyramid on both comprehension and cognitive load. This plugin will give you a frame; it will not pretend that leading with the conclusion is a comprehension technique.

---

## What it actually does

```
1. Fix the audience      →  ask once, or infer and state the assumption
2. Frame before detail   →  one sentence naming the topic, first
3. Build the explanation →  relations not resemblances; two examples, not one
4. Make structure visible→  signposting (g+ = 0.53 retention, k = 103 studies)
5. Verify, if it matters →  make you produce something back; never "any questions?"
```

Steps 1, 2 and 4 always run. Step 3 scales with difficulty. Step 5 fires only when a misunderstanding would actually cost you something — it does not staple a quiz onto every trivial answer.

**It also refuses to do some things.** It will not pad an expert's answer, perform simplicity with forced whimsy, cap bullets at a magic number, chase a readability score, or tell you that something "reduces cognitive load" (no standardized instrument backs that sentence, and for split-attention specifically, 41 comparisons found load measures *do not* support the explanation).

---

## The research

`docs/background/` is the knowledge base the skill is built on — 13 documents, ~83,000 words, 74 sources.

It was built with two multi-agent research passes and then **adversarial verification**: every claim was sent to three independent verifiers *instructed to refute it* — retrieve the primary source themselves, confirm the quote appears verbatim, and hunt for contradicting evidence. Two refutations out of three kill a claim.

| | Sources | Claims extracted | Adjudicated | Confirmed | **Refuted** |
|---|---|---|---|---|---|
| Pass 1 — broad | 28 | 139 | 60 | 32 | **28** |
| Pass 2 — targeted gaps | 10 topics | 70 | 70 | 48 | **22** |

**Half the claims died.** That is the interesting part, and the refuted ones were kept rather than deleted — they are what [`09-myths-and-contested-claims.md`](docs/background/09-myths-and-contested-claims.md) is made of, and they are why the skill knows what *not* to say.

Casualties include Mayer's famous multimedia effect sizes (self-review vote-counts; independent meta-analyses land at a third of the size), the Nielsen Norman scanning statistics (~10 participants per cell, largest effect **reversed** in an independent test), and the claim that the Federal Plain Language Guidelines mandate answer-first ordering (they *recommend* it; the document calls itself advice).

Plus the three that everyone repeats:

- **Mehrabian 7-38-55** — the numbers were never measured. They appear once, as a *suggested* extrapolation in a discussion paragraph, combining two studies neither of which compared all three channels. Mehrabian's own caveat restricts them to *inconsistent* communications about *feelings and attitudes*.
- **The 8-second attention span** — the citation chain runs Microsoft → "Statistic Brain" → nothing. The BBC contacted every source listed; none had any record of it. The only real study in the chain measured *web-page dwell time*.
- **Learning styles** — the *meshing hypothesis* fails, and essentially no study meets the design that would validate it. (Note the scope: preferences are real. It is the pedagogical inference that dies.)

Start with [`docs/background/README.md`](docs/background/README.md).

---

## Language neutrality

Every rule in the skill is about processing order and knowledge structure, not about English.

The things that *are* English-specific are named and forbidden as targets — readability formulas, word counts, syllable counts, "one idea per sentence" (Korean, Japanese and Turkish encode multiple ideas per orthographic sentence as the unmarked norm).

The one mechanically-checkable difficulty signal with genuine cross-linguistic support is **surprisal**, validated across 11 languages in 5 families. Even that is only usable to *locate* hard passages — never as a rewrite target, which is exactly the Goodhart failure that discredited readability formulas in the first place.

---

## Repo layout

```
.claude-plugin/marketplace.json   # marketplace manifest
plugins/easy-speak/               # the plugin
  ├── .claude-plugin/plugin.json
  ├── commands/easy-speak.md      # /easy-speak
  └── skills/easy-speak/
      ├── SKILL.md                # the operational loop
      └── references/             # loaded on demand
docs/background/                  # the research (13 docs, 74 sources)
```

## License

MIT
