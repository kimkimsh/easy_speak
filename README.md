# easy-speak

**A Claude Code plugin that aims Claude at being understood — in conversation and in the documents it writes.**

Not "sound simple." *Understand.* Those are different targets, and the research is fairly brutal about the difference.

The honest framing, since this repo holds itself to it: every rule here is evidence about a *component* — framing, signposting, two examples, production-based checks, document revision. **Nobody has tested the assembled package**, including me. Treat it as a discipline with traceable reasons, not a measured outcome.

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
| `/easy-speak` | Turns on easy-speak mode for the session. Answers follow the loop, and **documents follow the artifact rules**. |
| `/easy-speak <question>` | Explains that one thing, properly. Session state is unchanged. |
| `/easy-speak <write the README>` | Writes that one thing, properly. Session state is unchanged. |
| `/easy-speak off` | Back to normal. |

The skill also activates on its own when you say things like *"I don't understand this"*, *"explain it simply"*, or *"nobody can follow this README"*.

**It does not activate just because you asked for documentation.** "Write a README" is a normal request and gets a normal answer. That is deliberate: a comprehension complaint is a signal, a documentation task is not, and a plugin that fires on every writing request is a plugin you uninstall.

---

## Why this isn't just "write simpler"

Three findings shaped the whole design.

**1. There is no simple version of anything — only a version that fits a particular head.**

Cost is paid in *chunks in the receiver's memory*, not in words on the page. The same sentence is one unit to an expert and twelve to a novice.

Which means "simplify" is not a direction you can move in until you know who is listening. Worse, over-explaining is not a safe default — the **expertise reversal effect** flips the identical explanation from **d = +0.505** (helps a novice) to **d = −0.428** (measurably *hurts* an expert). Padding an expert's answer makes them perform worse.

The same reversal shows up in text. McNamara and colleagues varied a science text's coherence and found low-knowledge readers did better on the coherent version while **high-knowledge readers did better on the sparser one** — the gaps forced the inference that produced understanding. So "add more connective tissue" is not safe for a document either.

So easy-speak's first move is not "write simply." It is **fix the audience** — ask once, or infer and say the assumption out loud so you can correct it in one word.

**2. Claude cannot judge its own clarity. Neither can you.**

In Newton's study, people tapped out a famous song and predicted how many listeners would name it. They guessed ~50%. The real answer was **3 out of 120** — *below every single prediction anyone made*. Not one person was pessimistic enough.

This doesn't respond to effort. Paying people to be accurate didn't fix it. Telling them the outcome didn't fix it.

So the skill never asks *"does that make sense?"* — a question that cannot be answered by someone who misunderstood, and that people answer "yes" to under social pressure anyway. When getting it wrong actually costs something, it asks you to **put it back in your own words**, with the burden of failure on Claude rather than on you.

**3. Give the frame before the details — and know that "frame" is not "conclusion."**

Adding one sentence naming the topic *before* a passage roughly doubled both comprehension and recall on word-for-word identical text. Adding the same sentence *afterwards* bought nothing — you cannot pay that debt retroactively.

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

## When the reader isn't in the room

Version 1.2 extends the same loop to documents: README, design doc, spec, report, guide, commit message, PR description.

It is not a second mode you have to remember. It is one question, asked per deliverable: **can this reader answer back right now?** A turn that produces a draft *and* a conversation about the draft is both, and they get different treatment.

Four things change when the answer is no.

**The reader is not the person who asked.** A staff engineer requesting a getting-started guide tells you nothing about who will follow it. And a wrong guess runs the entire document instead of one turn.

**Nothing may depend on this conversation.** A term, a decision, a constraint that lives only in the thread the reader was never in has to be in the artifact. Where the reader can't repair, "ship it and they'll ask" is forbidden — that finding's own source explicitly excludes letters, broadcasts and anything else the audience can't interrupt.

Self-sufficient does *not* mean inlining everything. A linked issue they can open is a fine dependency. A conversation they weren't in is not.

**Readers arrive in the middle.** Someone landing on section 7 from a search result never saw your introduction, so "frame first" has to mean *before the reader meets the details*, not before page one. A heading usually does the job: "Recover a replica after a failed upgrade" orients; "Recovery" followed by "run this after the previous step" does not.

This one is labelled as an inference in the source material, because it is one. Bransford & Johnson tested linear reading of a single passage. They never tested hyperlink entry — and "repeat the introduction under every heading" has real costs and no measured benefit.

**Step 5 breaks, and nothing replaces it.** This is the interesting part.

The strongest rule in the whole knowledge base is that you cannot check your own clarity — only the receiver can, by producing something. A document has no receiver. So the skill does three things and refuses a fourth:

- **Inspects the text** for defects that are checkable without a reader — a term used before it's introduced, a referent with no antecedent, a step whose precondition appears later, a promise the opening makes and the body never delivers. It calls this a heuristic, because that is what it is, and finding nothing proves nothing.
- **Reports corrections, not impressions.** "Defined `tenant scope` at first use" is observable. "This is much clearer now" is not.
- **States where verification stopped:** *"Checked prerequisites, terminology and references. Reader comprehension has not been tested."*
- **Refuses to claim a clarity verdict** that no instrument produced. A reread isn't reader testing. Neither is a fresh model context, a "novice persona", or your approval standing in for your users'. And preparing a reader test is not running one.

Finishing a document with comprehension untested is the normal outcome, and the skill says so rather than papering over it. If it actually matters, it will hand you a test someone could run — who the reader is, a realistic task, what they may consult, what success looks like — because the real instrument is readers thinking aloud while they use it, and that is your job, not Claude's. (Five per cycle is the plain-language field's reported practice, and the "first pass finds about half the problems" figure is that field's own stated rule of thumb — not a measured optimum.)

---

## The research

`docs/background/` is the knowledge base the skill is built on — 15 documents, 74 adjudicated sources plus 18 more entries at a lower tier.

**Documents 01–12** were built with two multi-agent research passes and then **adversarial verification**: every claim was sent to three independent verifiers *instructed to refute it* — retrieve the primary source themselves, confirm the quote appears verbatim, and hunt for contradicting evidence. Two refutations out of three kill a claim.

| | Sources | Claims extracted | Adjudicated | Confirmed | **Refuted** |
|---|---|---|---|---|---|
| Pass 1 — broad | 28 | 139 | 60 | 32 | **28** |
| Pass 2 — targeted gaps | 10 topics | 70 | 70 | 48 | **22** |

**Roughly 38% of the adjudicated claims died** — 50 of 130. That is the interesting part, and the refuted ones were kept rather than deleted — they are what [`09-myths-and-contested-claims.md`](docs/background/09-myths-and-contested-claims.md) is made of, and they are why the skill knows what *not* to say.

Casualties include Mayer's famous multimedia effect sizes (self-review vote-counts; independent meta-analyses land at a third of the size), the Nielsen Norman scanning statistics (~10 participants per cell, largest effect **reversed** in an independent test), and the claim that the Federal Plain Language Guidelines mandate answer-first ordering (they *recommend* it; the document calls itself advice).

Plus the three that everyone repeats:

- **Mehrabian 7-38-55** — the numbers were never measured. They appear once, as a *suggested* extrapolation in a discussion paragraph, combining two studies neither of which compared all three channels. Mehrabian's own caveat restricts them to *inconsistent* communications about *feelings and attitudes*.
- **The 8-second attention span** — the citation chain runs Microsoft → "Statistic Brain" → nothing. The BBC contacted every source listed; none had any record of it. The only real study in the chain measured *web-page dwell time*.
- **Learning styles** — the *meshing hypothesis* fails, and essentially no study meets the design that would validate it. (Note the scope: preferences are real. It is the pedagogical inference that dies.)

**Documents 13 and 14 are a weaker tier, and they say so on their first screen.** They were added for the writing extension, after both verification passes had closed. Their sources — 18 catalogued entries, none overlapping the 74 — were fetched and quote-checked once, opened and read with the numbers taken from the paper, but **never sent to three verifiers instructed to break them.** Two are weaker still and say so: one whose full text could not be retrieved, from which no number is quoted, and one listed purely as a lead. Given that 38% of everything that *was* adjudicated died, and that the typical casualty was a real finding stretched one step past its source, that gap is not cosmetic. Nothing in 13 or 14 carries a `3-0`.

One illustration of how easily that slips, and it is this repo's own near-miss. A secondary summary of Carroll's Minimal Manual study reports that its learners scored "better by a factor of eight." That phrase is not in the Minimal Manual paper, and it was nearly quoted as if it were. It is not invented either — Carroll & Rosson's *Paradox of the Active User* reports exactly that figure, for a different comparison: learners moved on to a commercial manual's advanced sections, where "their performance on learning achievement tests was better by a factor of eight." Right number, wrong paper, wrong phase. **Misattribution, not fabrication** — which is the commoner failure and the harder one to catch, because the number survives every check except opening the source.

Four writing-mode claims did not survive even that lighter check, and are recorded as refutations: *a harder-to-read font helps retention* (four experiments, memory equivalent or worse); *text-structure research proves you should structure your document* (that meta-analysis trained **readers**, and never manipulated the text); *plain language is proven, so this rule is evidence-backed* (the results are real, the collection is an advocate's, and every intervention is a bundle — so no individual rule inherits the number); and *a better PR description makes reviewers understand* (the source's own interviewees say "the description is not enough").

Start with [`docs/background/README.md`](docs/background/README.md).

---

## Language neutrality

Every rule in the skill is about processing order and knowledge structure, not about English.

The things that *are* English-specific are named and forbidden as targets — readability formulas, word counts, syllable counts, "one idea per sentence" (Korean, Japanese and Turkish encode multiple ideas per orthographic sentence as the unmarked norm).

The one mechanically-checkable difficulty signal with genuine cross-linguistic support is **surprisal**, validated across 11 languages in 5 families. Even that is only usable to *locate* hard passages — never as a rewrite target, which is exactly the Goodhart failure that discredited readability formulas in the first place.

A search for a **Korean** evidence base comparable to the English plain-language literature turned up policy infrastructure and language-policy scholarship, and did not locate a comparable body of controlled revision studies. **What this search did not find is recorded rather than papered over** — it is not a claim that no such literature exists, in Korean or in any other language. It is one reason the skill stays language-neutral instead of translating English rules, and the transfer it does assume — that processing order carries across languages while surface prescriptions do not — is itself labelled an inference in the source material.

---

## Repo layout

```
.claude-plugin/marketplace.json   # marketplace manifest
plugins/easy-speak/               # the plugin
  ├── .claude-plugin/plugin.json
  ├── commands/easy-speak.md      # /easy-speak
  └── skills/easy-speak/
      ├── SKILL.md                # the loop, and the artifact rules
      └── references/             # loaded on demand
docs/background/                  # the research (15 docs, 74 adjudicated + 18 quote-checked entries)
docs/acceptance-cases.md          # 13 prompts that decide whether the rules select the right behaviour
```

## License

MIT
