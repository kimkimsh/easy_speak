# The rule set: what the skill actually does

> **What this is.** The operational file. Everything else in `docs/background/` is the evidence behind it. Every rule below traces to a peer document by tag; nothing is added from memory.
>
> **How to read a tag.** `[03 §2]` = document 03, section 2. `3-0` = unanimous under adversarial verification. `2-1` = split. `HEURISTIC` = no evidence in this knowledge base — say so out loud if you use it.
>
> **Default stance.** Language-neutral. Every English-only artifact is flagged as such and may never be used as a target. When a rule and a number are both available, ship the rule and leave the number behind unless the number is asked for.

---

## 1. The four rules that matter most

If the skill could do only four things, these are the four — ranked, with the reason for the ranking.

### R1 — Clarity is not self-observable. Verify it on the receiver, by making them produce something.

An informed person's estimate of how well they are being understood is not data. Newton's tappers predicted ~50% listener success; the true rate was 3 hits in 120 tries, **outside the entire range of all forty predictions** — no tapper was pessimistic enough `[02 §1] Newton 1990, 3-0`. The miscalibration is not repaired by wanting to be accurate, by being paid to be accurate, or by being told the outcome; markets at best halve it `[02 §2] Camerer, Loewenstein & Weber 1989, 3-0`. And the listener will not rescue you: listeners are under structural pressure to feign understanding, and produce coordinating signals "however insincere they may be" `[03 §2b] Clark & Wilkes-Gibbs 1986, 3-0`.

The replacement is not a better opinion. It is a production task. Prompting someone to explain the material back is the single strongest quantitative warrant in the whole knowledge base: **g = 0.55, 95% CI 0.45–0.65, 69 effect sizes, N = 5,917**, holding across task type, subject area, and education level `[08 §4] Bisra et al. 2018, 2-1`. Teach-back was effective in **19 of 20 studies (9 RCTs)** across five outcome domains `[08 §5] Talevski et al. 2020` and raised *actual* comprehension in an ED RCT (follow-up OR 3.61, 95% CI 2.09–6.22) while leaving *perceived* comprehension unmoved `[08 §1] Griffey et al.`.

**Why first.** It is the gate on everything else. Without it, the coach's instrument — the speaker's own sense that "that was clear" — is the broken thing being measured. Every other rule in this file is an improvement you cannot confirm you made.

**Boundary.** An LLM reviewing a draft is not a naive audience; it has read the internet. It can flag markers and unexplained terms. It cannot certify comprehension `[02 §3]`.

### R2 — The unit of cost is a chunk in the receiver's head, not a word on your page. Fix the audience before you fix the text.

Working-memory capacity applies to *chunks grounded in prior knowledge*, not to raw surface items — Cowan's own example turns on "**if you know it**" `[01 §1] Cowan 2015, 3-0`. Cognitive Load Theory says the same thing from the other side as element interactivity: "Dog" is three elements for a beginning reader and one for a fluent one `[01 §1]`. This is why jargon is expensive — not because it is ugly, but because an unowned term consumes several slots instead of one, silently `[01 §1]`, `[05 §8]`.

Two consequences the skill must actually enforce:

- **There is no audience-independent "plain" version of anything.** "The first rule of plain language is: write for your audience... **Only write for 8th graders if your audience is, in fact, an 8th grade class**" `[07 §1.1–1.2] FPLG, 3-0`.
- **"Always simplify" is not safe.** The expertise reversal effect turns the same high-assistance design from **d = +0.505** for low-prior-knowledge learners to **d = −0.428** for high-prior-knowledge learners `[01 §4]`. Over-explaining to an expert measurably degrades their performance. "Simplify for whom" is the only well-formed question.

**Why second.** It is the mechanism that makes every other rule audience-conditional, and it is the rule that kills the magic numbers ("4 bullets", "grade 8", "7±2"). A skill that gets this wrong ships confident, wrong advice everywhere else.

**What it does NOT license.** Not "working memory holds 4 slots." Not "never more than N bullets." The ~4 figure is a pure-capacity estimate observable only under lab conditions engineered to block rehearsal, recoding and long-term-memory grouping — the exact mechanisms real communication runs on `[01 §2–3]`. A slide with 7 bullets naming things the audience already owns is cheaper than a slide with 3 bullets of unexplained terms.

### R3 — The frame arrives before the first detail.

One sentence naming what the thing is *about*, delivered first. In Bransford & Johnson's Experiment II the entire manipulation was one added sentence — *"The paragraph you will hear will be about washing clothes"* — and it roughly doubled both measures on word-for-word identical text `[04 §1] Bransford & Johnson 1972, 3-0`:

| Experiment II | Comprehension (max 7) | Recall (max 18) |
|---|---|---|
| No Topic | 2.29 | 2.82 |
| Topic **After** | 2.12 | 2.65 |
| Topic **Before** | **4.50** | **5.83** |

Note the middle row. **A topic delivered late is not better than no topic at all** — numerically worse on both measures here, and confirmed again in Experiment IV, where a late topic left recall (3.18) indistinguishable from no topic (3.22) `[04 §1, §6.3]`. Retrospective framing does not repay the debt. The mechanism: the topic is what lets the listener compute the antecedent for *any* sentence, so plain prose without a frame is still unparseable prose `[04 §2] Clark & Haviland 1977, 3-0`.

**Why third.** Cheapest structural intervention in the evidence base, largest documented swing on identical content, and it costs one sentence.

**Critically: a frame is a topic, not a conclusion.** Do not launder BLUF through this citation. See §5.

### R4 — Make the structure visible.

Headings, an outline, enumeration, explicit signposting ("three things; here is the first"). Signaling — cues that highlight the *organization* of the material — is the best-evidenced structural lever available: **retention g+ = 0.53 [0.42, 0.64], transfer g+ = 0.33 [0.22, 0.43], k = 103 studies, N = 12,201** `[04 §3]`, `[06 §4] Schneider et al. 2018, 3-0`.

**Why fourth, and why it earns the slot.** Two things make it unusual. First, the scale — 103 studies, 46 years, 145 pairwise comparisons. Second: **prior knowledge was NOT a moderator**, contrary to the expertise-reversal prediction. This is the one instructional support in the knowledge base that does not appear to backfire on experts. Signpost for everyone.

Report retention and transfer as different sizes; do not quote one number for both. Do not extrapolate the no-moderator result to other supports — expertise reversal is real elsewhere `[06 §4]`.

---

## 2. Rules by context

The **Check** column is what an LLM can mechanically execute. Where a check requires a human or an audience, it says so.

### 2a. Explaining to a non-expert

| Rule | How to check it | Evidence |
|---|---|---|
| Fix the audience profile *before* editing anything. Name who they are and what they already own. | Refuse to proceed without a named audience. If the request is "make this clearer", answer "clearer to whom?" | `[07 §1.1]` FPLG 3-0; `[01 §4]` expertise reversal |
| Every load-bearing term the audience does not already own is introduced before its first working use, or replaced with plain wording. | Enumerate technical terms and acronyms. For each, mark owned / not-owned against the audience profile. Flag any not-owned term used before it is introduced. | `[01 §1]` Cowan 3-0 (chunk cost); `[05 §8]` Bullock 2019 (jargon → lower processing fluency, η²=.11, N=650) |
| An analogy must map **relations**, not looks. | Write the relational skeleton: `REL(a,b) ← REL(x,y)`. If nothing survives the strip, it is a **mere appearance match** — allowed as a mnemonic, not as the explanation. | `[05 §2–3]` Gentner 1983, 3-0 |
| State the mapping out loud. Do not place an analogy nearby and hope. | Search for an explicit correspondence sentence ("X plays the role of Y here"). If absent, flag. | `[05 §4]` Gick & Holyoak 1983, 3-0 — ~75% solved with a hint vs ~30% without, same analog in their heads |
| Give **two** structurally-matched, surface-different examples, then ask what they share. | Count examples. One example plus a statement of the principle is the intervention that was tested three ways and **failed**. | `[05 §4]` Gick & Holyoak, 3-0 — two analogs 45% vs one 21% (no hint) |
| Cut the interesting-but-irrelevant. You cannot buy it back with emphasis. | For each vivid aside, ask: does deleting it change what the audience must end up able to do? If no, cut. If it truly cannot be cut, the only placement with evidence is **the very end**. | `[05 §7]` Harp & Mayer 1998, 2-1 — highlighting, learning objectives and signaling all failed to rescue it |
| Put the load-bearing fact near the point where it is needed. | Trace each critical proposition to its first use. Flag any separated from its use by intervening irrelevant material. | `[01 §5]` Kintsch 1988, 3-0 (buffer eviction); Fuchs et al., irrelevant info d = 0.73, n = 701 |
| Set the depth of the explanation from what they must end up able to **do**. | Ask for the task. "Which room are we in" and "why we are changing the deployment order" are different criteria. | `[03 §1]`, `[08 §9]` Clark & Brennan 1991, 3-0 — the grounding criterion is "sufficient for current purposes", never perfect |

### 2b. Presenting and reporting

| Rule | How to check it | Evidence |
|---|---|---|
| Frame before details, at the deck level and at the section level. | First slide / first line of each section: does it name the topic before any detail? Binary. | `[04 §1]` B&J 1972, 3-0 |
| Signpost the structure explicitly. | Count organizational cues per section (heading, enumeration, "three things", importance markers). Zero cues in a multi-part section = flag. | `[06 §4]` Schneider et al. 2018, 3-0 |
| Put the label on the thing. Speak alongside the visual, not before or after it. | For each diagram: is every label adjacent to its referent, or is it in a legend? Is narration synchronized with the visual it describes? | `[06 §2]` Schroeder & Cenkci 2018, g = 0.63, k = 58; Ginns 2006, 3-0 |
| Spend contiguity effort where the material is **complex and interdependent**. | Rate element interactivity. High-EI d = 0.78; low-EI d = 0.28, **p > .05**. On a simple slide, moving a caption is a rounding error. | `[06 §2b]` Ginns 2006, 3-0 |
| Do **not** minimize whitespace. Integrate what mutually refers; extreme proximity backfires. | Flag any layout where unrelated elements have been crammed together with related ones. | `[06 §2c]` Beege et al. 2019, 3-0 |
| Text on slides is **not** banned. The harmful case is narrow. | Flag only the conjunction: *verbatim full-sentence script + read aloud + over a diagram + to an experienced audience*. Otherwise, prefer **key terms extracted from the narration** over verbatim text. | `[06 §5]` Adesope & Nesbit 2012, 3-0 — spoken+written **beats** spoken-only for low-prior-knowledge audiences, system-paced material (every live talk), and picture-free material; adding audio to text was null (g = −0.04) |
| BLUF is a **triage** convention. Label it as such when you recommend it. | If the rationale given is "comprehension", reject it. There is no comprehension evidence for conclusion-first in this knowledge base. | `[04 §5]` — Kieras never ran the BLUF manipulation (refuted 0-3); the one head-to-head went *against* the inverted pyramid, with small effects, in German |
| Never narrate a load mechanism. | Delete any clause of the form "…because it reduces cognitive load". | `[06 §3]` Schroeder & Cenkci 2020 — 41 comparisons; load measures "largely do not support the extraneous cognitive load explanation"; `[01 §4]` de Jong 2010, 3-0 — no standardized instrument |

### 2c. 1:1 conversation

| Rule | How to check it | Evidence |
|---|---|---|
| Never infer understanding from the absence of confusion. Seek positive evidence. | Nods, "okay", continued attention = weakest tier. **The relevant next turn** is the diagnostic one: does their next contribution display the understanding? | `[03 §2a]` Clark & Brennan 1991, 3-0 |
| Silence is not evidence of understanding — **in any language**. | The quieter and more deferential the listener's position, the *less* their silence means. | `[03 §5]`, `[08 §2]` Dingemanse et al. 2013/2015, 3-0 — other-initiated repair documented in every spoken language investigated, used ~once per 1.4 minutes; but *willingness* to initiate repair is modulated by face norms |
| Ask them to restate or apply. Never "any questions?". | Grep the transcript for `any questions` / `does that make sense` / `do you understand` / `clear?`. Every hit is a defect; propose a production check in its place. | `[08 §2]` Kemp et al. 2008 — "they may not understand the situation well enough to formulate a question" |
| Frame the check **collaboratively** — put the burden on yourself. | "I've given you a lot of information. It would be helpful **to me** to hear your understanding." The active ingredient is the framing, not open-endedness: a bluntly directive tell-back scored *no better* than a Yes/No check. | `[08 §7]` Kemp et al. 2008, 2-1 — **preference and perceived effectiveness only; comprehension was never measured** |
| A repairable draft beats a perfect utterance — **only where the listener can repair in real time**. | Ask: can this addressee interrupt right now? If yes, name it briefly and let repair do the work. If no, see 2d. | `[03 §4a]` Clark & Brennan / Clark & Wilkes-Gibbs, 2-1 (contested; Davies 2007, Pickering & Garrod 2004 dissent) |
| Audit your team's compressed vocabulary before using it on an outsider. | Flag short label-like noun phrases whose meaning depends on prior shared episodes. | `[03 §3]` Clark & Wilkes-Gibbs 1986, 3-0 — referring expressions fell from 41 words to 8, and turns from 3.7 to ~1, across six trials. **The 8-word label is a receipt for grounding work, not clarity.** |
| Do not use brevity as a diagnostic of shared understanding. | Use the acceptance/repair test instead: name it briefly; if they proceed without repair, it was grounded. | `[03 §3]` — the causal mechanism of compression is contested (Bangerter et al.) |
| If they must hold a **causal model**, make them produce the causal model. | Self-rated understanding of *how or why* something works collapses the moment a real explanation must be produced. Not demonstrated for facts, procedures, or narratives — do not over-apply. | `[08 §3]` Rozenblit & Keil 2002 — the T1→T2 drop survives; the universal reading does not |

### 2d. Writing (one-way: docs, email, reports, specs)

| Rule | How to check it | Evidence |
|---|---|---|
| Where the reader cannot repair, the **self-sufficient utterance is the right target**. Polish it. | Classify the channel first. Novel, letter, broadcast, sermon, large lecture, shipped doc → no repair channel → "ship a rough draft and let them fix it" is **forbidden**. | `[03 §4b]` Clark & Wilkes-Gibbs explicitly exclude these. **Semi-interactive media (async chat, PR comments, commentable docs) sit between the columns and are NOT resolved by any source — do not fabricate a rule for them.** |
| Frame before details, per document and per section. | First sentence names the topic. Binary check. | `[04 §1]` B&J 1972, 3-0 |
| Anchor first, new last, within the sentence. | Open each sentence with what the reader already holds; end with what is new. | `[04 §2]` Clark & Haviland 1977, 2-1. **This is an argument, not a demonstration** — write "Clark & Haviland *argue*". **ENGLISH-ONLY:** the surface machinery (end-of-sentence focal stress, clefts, definite-NP-first) does not port. Coach the processing order only. |
| Cut irrelevant material; do **not** cut repetition that gives a second way to refer to the same thing. | Kintsch declines the blanket rule: overspecification "may even facilitate problem solving". The cost is carried by **irrelevant** material specifically. | `[01 §5]` Kintsch 1988, 3-0; Fuchs et al. d = 0.73 |
| Do not make the reader bridge a gap you could have closed. | Direction only. **Never quote a millisecond cost** — the authors said the absolute differences "cannot be taken very seriously". | `[04 §6.2]` Haviland & Clark 1974, refuted as a magnitude 1-2 |
| Strip boosterism / marketese. | Say **"readers report preferring objective phrasing"**. Never "it degrades comprehension" or "it destroys trust". | `[07 §4.1]` Morkes & Nielsen 1997, refuted 0-3 on the comprehension half — only subjective satisfaction reached significance; trust was never measured |
| Topic sentence per paragraph; one topic per paragraph or section. | Present as a **reasonable convention**, not a validated finding. The famous "readers only read the first sentence" evidence is an unquantified anecdote from an exploratory arm and was refuted 0-3. | `[07 §1.4]` FPLG's own voice (p.68); `[07 §4.1]` NN/g refutation |
| Do not enforce paragraph or sentence length numbers. | The FPLG's 150/250 figures are attributed to "**writing experts**", sourced to two legal-writing style manuals with **no empirical study**, and sit next to "there is nothing wrong with an occasional one-sentence paragraph" and a warning that uniform lengths are "choppy". **ENGLISH-ONLY: "word" is not a cross-linguistically stable unit.** | `[07 §1.4]` FPLG, 3-0 |

---

## 3. Anti-patterns

Six moves that actively hurt. Each with what the evidence does and does not support.

**1. Seductive details — the interesting-but-irrelevant tangent.**
Readers given expository passages with interesting-but-irrelevant adjuncts recalled significantly fewer main ideas and produced fewer transfer solutions (N = 357). **The workaround is what makes this an anti-pattern rather than a preference:** highlighting the main ideas, stating learning objectives, and signaling were each tested and each **failed to reduce the effect** `[05 §7] Harp & Mayer 1998, 2-1`. Only removal, or placement at the very end, helped.
*Do not oversell it.* Pooled effect is small-to-medium (retention d = 0.30; transfer d = 0.48); 11 of 39 studies supported it and 15 did not; there is a failed replication on the identical material; and **language moderates the effect size** `[05 §7]`, Rey 2012.

**2. Jargon — an unowned term used as if it were free.**
An unexplained term the receiver has not chunked consumes several slots instead of one, and it does so invisibly to the person who wrote it `[01 §1] Cowan, 3-0`. Empirically, jargon-laden English text produced significantly lower self-reported processing fluency (F(1,636) = 76.03, η² = .11, N = 650) `[05 §8] Bullock et al. 2019`.
*Two hard limits.* **Do not say "definitions don't help."** What was tested was an *optional hover-to-reveal* definition, and what was measured was *how hard the text felt*, not comprehension — the paper's own results show the definition condition mattering on at least one other outcome `[05 §8]`, `[09 B14]`. And **do not port the magnitude:** English scientific vocabulary is opaque Greco-Latinate borrowing; the fluency penalty may be smaller in languages whose technical vocabulary is built from transparent native morphemes. The *direction* survives via the chunk argument, which is language-neutral.

**3. Expert shorthand used with a newcomer.**
Grounding compresses language: the same referent went from 41 words and 3.7 turns to 8 words and ~1 turn across six trials with the same partner `[03 §3] Clark & Wilkes-Gibbs 1986, 3-0`. The eight-word label is not clearer writing — it is a **receipt for grounding work both parties already did**. Using it with someone who was not present for that work is guaranteed failure, because the label's entire meaning is the common ground it points at. Audit the internal vocabulary before it leaves the room.

**4. "Any questions?" / "Does that make sense?" / a nod.**
A person who has misunderstood cannot generate a question about the thing they misunderstood: "they may not understand the situation well enough to formulate a question" `[08 §2] Kemp et al. 2008`. Listeners are under systematic pressure to feign understanding and produce acknowledgment tokens "however insincere they may be" `[03 §2b], 3-0`. And self-report is decoupled from comprehension: teach-back raised *actual* comprehension while leaving *perceived* comprehension flat `[08 §1] Griffey RCT`. Base rate for how often anyone does better: physicians checked comprehension for **12% of new concepts**, and **99.7%** of self-selected "best" videotapes failed to confirm understanding consistently `[08 §2]`.
*Do not condemn these using Bisra's g = 0.19 metacognitive cell* — that category means "self-explain your planning or performance", and confidence questions were never tested in it `[08 §8]`.

**5. Readability-score chasing.**
Traditional formulas, modern ML systems, commercial systems (Lexile, TextEvaluator) **and six frontier LLMs** are all poor predictors of reading ease against eye-tracking data — **in English** `[07 §2.2] Gruteke Klein et al., 3-0`. The formulas' linguistic criteria "do not constitute a satisfactory basis for assessing reading difficulty" `[07 §2.2] Bailin & Grafstein 2001, 3-0`, and the ISO 24495-1 working group declined to endorse them.
*State it narrowly.* Readability scores may **never** be a target metric or proof of clarity. They are **not** thereby proven to have zero predictive validity — Flesch-Kincaid explains ~57% of variance in a cloze-comprehension criterion over 330 passages `[07 §2.3]`. They are the wrong instrument, not a random number generator. Reporting "readability improved" is never an acceptable result.

**6. Boosterism / marketese.**
Readers **report** disliking hyped, promotional phrasing and **report** higher satisfaction with objective phrasing. That is a legitimate reason to strip it. It is **not** a comprehension finding: in the source study, the only statistically significant difference on the objective-vs-promotional contrast was subjective satisfaction — task time, task errors, memory and sitemap time all failed to reach significance, and **trust was never measured** `[07 §4.1] Morkes & Nielsen 1997, refuted 0-3`. Say "readers report preferring it." Never "it degrades comprehension."

---

## 4. Mechanically checkable signals — an honest inventory

Three tiers. Do not let a tier-b or tier-c signal be reported as if it were tier-a.

### (a) Real cross-linguistic support — usable as a *locator*, never as a *target*

**Surprisal** — the negative log-probability of a word given its prefix, under any autoregressive language model. It needs no syllable counting, no word-length proxy, no English-tuned regression constants; it needs only a next-token distribution, which any LM supplies **for any language** `[07 §3] Hale 2001, 3-0`.

The cross-linguistic warrant is the decisive one: on the MECO eye-tracking corpus (the same article content translated into each language), **"in all languages tested, regression models that include surprisal are significantly better predictors of reading times over baselines which do not include surprisal"** — **11 languages across 5 families** (Korean/Koreanic; Turkish/Turkic; Hebrew/Semitic; Finnish/Uralic; Dutch, English, German, Greek, Italian, Russian, Spanish/Indo-European) `[07 §3] Wilcox et al. 2023, TACL, 3-0`. This is the **only** signal in the knowledge base that carries genuine cross-linguistic support.

Its own limits, which travel with it:
- 7 of 11 languages are Indo-European; no African, Austronesian or signed languages.
- Predictive power **varies by language** and the variation is not explained by training-data size.
- The unit is the orthographic word, which is not commensurable across Korean *eojeol*, Turkish agglutination, or Chinese.
- **The link function is contested** — linear, sublinear and superlinear conclusions all exist in the published literature `[07 §3.1]`.
- Very large LMs are reported to be *worse* predictors of human reading, so a frontier model's own logprobs may be a mis-calibrated estimator `[07 §3.1]`.

**Operational rule.** Compute surprisal; surface the high-surprisal spans; show them to a human. **Do not rewrite to lower surprisal.** No study in this knowledge base tests whether rewriting to reduce surprisal improves anything, and reading time is not understanding. Turning a correlational measure into a writing target is precisely the Goodhart failure that discredited readability formulas `[07 §3.1], [09 B9.3]`.

### (b) English-only artifacts — computable, and forbidden as targets

Each of these is mechanically computable. Each is an **artifact of English** and must never be used as a target, a success criterion, or evidence that a rewrite worked.

| Signal | Why it is English-only | Where it is prohibited |
|---|---|---|
| Flesch Reading Ease, Flesch-Kincaid, Dale-Chall, Gunning Fog, ARI, Coleman-Liau, Lexile, TextEvaluator | Count syllables and word lengths with English-tuned regression constants | `[07 §2]`, `[09 B9]` |
| An LLM asked "what grade level is this?" | Evaluated only against English eye-tracking; poor predictor there | `[07 §2.2]` |
| Word counts (150-word paragraphs, 250-word ceilings) | "Word" is not a cross-linguistically stable unit; Korean, Turkish, Finnish and German pack into one orthographic word what English spreads over several | `[07 §1.4]` |
| Syllable counts | Same | `[07 §2]` |
| "One idea per sentence" as a segmentation target | An English-prose heuristic from U.S. federal regulatory English; languages with clause-chaining or converb morphology (Korean, Japanese, Turkish) encode multiple ideas per orthographic sentence as the **unmarked norm** | `[07 §1.6]` |
| Dependency length | Effect size varies **~6×** with head-directionality (Japanese/Korean/Turkish minimize much less than Italian/Indonesian/Irish). No fixed cross-language threshold is valid; it is production evidence, not comprehension evidence | `[07 §3.1]`, `[09 B9.4]` |

Also on the English-only list and never to be generalized: end-of-sentence focal stress; cleft/pseudocleft/passive information-packaging; the FBICIAUSA chunking illustration; English backchannel tokens ("uh huh", "yeah"); Bell's /t/-voicing variable; the "initial mention = theme" convention of English expository prose (contrast *ki-shō-ten-ketsu*, *qǐ-chéng-zhuǎn-hé*) `[09 "language scope"]`.

### (c) Heuristic smell-tests — no validation behind them. Label them every time.

These are useful for *surfacing* things a human should look at. **None has a study behind it in this knowledge base. None may be reported as a score. None may be cited to research.**

| Smell-test | Status |
|---|---|
| Self-certifying language: "obviously", "simply", "just", "as you know", "of course", "trivially", "clearly", "it goes without saying" | **HEURISTIC — explicitly labelled non-evidence-backed in `[02 §3.1]`.** No study validates these markers, no effect size exists for them, and no test shows that removing them improves comprehension. Protocol: delete the marker; if the sentence still stands, it was doing no work; if it does not, the marker was carrying an unstated step — **and that step is the thing the audience is missing**. Never report a count. Also: these are **English lexical items**; another language needs its own list. |
| Counting bullets, clauses, or list items | **HEURISTIC AT BEST.** The real unit is the audience's chunk, which is not countable from your message. Any per-slide or per-sentence count is a weak proxy `[01 §3, §"does not license" 12]`. |
| Flagging in-group compressed vocabulary by shortness | **HEURISTIC.** Brevity is not a diagnostic of shared understanding — the causal mechanism of grounding-driven compression is contested `[03 §3]`. Use the repair test instead. |
| Scanning-oriented formatting (bullets, subheads, keywords) | **HEURISTIC.** Scanning is a real and common online reading mode, but the famous numbers behind it (58/47/27/124%) are ~10 participants per cell, one fictitious site, never peer-reviewed, never replicated, and the largest effect **reversed** in an independent test `[07 §4]`. |
| Rating text on "directness", "warmth", "harmony", "solidarity", "informality" | **PROHIBITED, not merely heuristic.** These are unanalysed English labels that have produced "paradoxical and contradictory conclusions"; scoring on them is scoring against Anglo concepts while claiming universality `[03 §7b] Wierzbicka 1991, 3-0`. |

---

## 5. The prohibition list — never assert these

Verification killed each of these. They are the sentences a confident coach most wants to say.

| Never say | Why |
|---|---|
| **"Communication is 7% words, 38% tone, 55% body language"** (Mehrabian 7-38-55) | The three-way model appears once, as a **suggested, proposed extrapolation** in a Discussion paragraph, flagged by its own author as still needing testing. No single study ever compared all three channels. "Body language" was head-only **still photographs**; 20 subjects produced the .55/.38 weights. Mehrabian's own standing caveat: the equations apply **only** to communications of **feelings and attitudes** *and* where the channels are **inconsistent** — "Unless a communicator is talking about their feelings or attitudes, these equations are not applicable." He calls the general reading "absurd": "the verbal part is nearly 100% of the message." **Do not replace it with a different channel-weighting constant — none is supported.** `[09 A1]` |
| **"The average attention span is 8 seconds — shorter than a goldfish"** | The chain runs Microsoft Canada 2015 → "Statistic Brain" → a void. BBC *More or Less* contacted every listed source; none had any record of the research. The number is not even stable across archived snapshots (8s "in 2013" → 8.25s "in 2015", citation unchanged). The only real study in the chain measured web-page **stay time**, not attention, and its authors warned it is an upper bound. **Do not substitute another number of seconds.** The defensible construct is the **vigilance decrement** — attention to a demanding task degrades over **tens of minutes to hours**, faster under higher demand. `[09 A2]` |
| **"Match the explanation to their learning style"** (meshing) | Pashler et al. require a crossover interaction, found essentially no study meeting the bar, and found sound studies **contradicting** it. Rogowsky et al. 2020 (n = 125 K-12): no interaction, no crossover, group means in the **wrong direction** for meshing, and **68% of students had no clear style preference at all**. **But do not say "learning styles don't exist"** — preferences are reported and aptitudes do differ; it is the *pedagogical inference* that fails. Adding a diagram is fine; justifying it by their style is not, and withholding text because of it is not. `[09 A3]` |
| **Any Mayer box-score effect size** ("23 of 23, d = 0.86"; "22 of 22, d = 1.10"; "16 of 16"; "9 of 9, d = 1.22") | Vote-counts from a self-review by the theory's own author. No random-effects pooling, no heterogeneity test, no publication-bias correction, no CIs. **Unstable across editions of the same chapter.** The "23 of 23 supported" tally contains a **d = −0.17** entry favouring the embellished lesson. Independent meta-analyses land at half to one-third the size. Use instead: all principles pooled **g = 0.38**; spatial contiguity **g = 0.63**; signaling **g+ = 0.53 / 0.33**; verbal redundancy **g = 0.15**. `[06 §7]`, `[09 B3]` |
| **"Teach-back has an effect size of d = ..."** citing Talevski | Fabrication. The review states verbatim: "given the heterogeneity of outcome measures, **it was not possible to conduct a meta-analysis**." It is a narrative synthesis. **Equally, do not say "there is no pooled effect size for teach-back anywhere"** — a narrow one exists (heart-failure readmission), and this knowledge base does not carry its value, so no number may be quoted here at all. What you may say: **19 of 20 studies, 9 RCTs, five outcome domains.** `[08 §5]`, `[09 B6.4]` |
| **"Working memory holds N slots, so use N bullets"** | Three independent reasons. (i) The ~4 figure is a *pure-capacity* estimate observable only under conditions that deliberately block rehearsal, recoding and LTM grouping — conditions a listener in a meeting is not in. (ii) The slot-vs-resource mechanism is **contested**. (iii) Capacity is over **knowledge-relative chunks**, so the number of presentable things is a function of the audience's prior knowledge, not a constant. Miller himself called seven "a pernicious, Pythagorean coincidence". **Correcting 7 to 4 while keeping the habit of budgeting by raw item count reproduces the original error with a smaller number.** `[01 §2–3]`, `[09 B2]` |
| **"This reads at grade X, therefore it is understandable"** | No readability score — traditional, ML, commercial, or LLM-produced — is validated as evidence of clarity, and all are English artifacts by construction. "The score improved" is never the report. **But do not overreach in the other direction either:** they do not have zero predictive validity (FK r² ≈ .57 against cloze comprehension), and "LLMs cannot assess readability" is a broader claim than the evidence supports. `[07 §2]`, `[09 B9]` |

### Also prohibited (same standard, less famous)

- **"This reduces cognitive load."** No standardized instrument exists behind the sentence; the extraneous/germane distinction is tautological by CLT's own critical literature; and for spatial split-attention, 41 comparisons found load measures "largely do not support the extraneous cognitive load explanation" `[01 §4]`, `[06 §3]`. Say what you did to the chunk structure instead. *(Do not flatten this into "load theory is dead": load* was *significantly reduced for signaling.)*
- **"Closer is always better."** Falsified — maximum proximity underperformed medium proximity `[06 §2c]`.
- **"Never put text on your slides."** Backwards in three named conditions `[06 §5]`.
- **"Experts are literally unable to imagine not knowing."** The paper always cited for this explicitly **rejects** its own w = 1 (pure-bias) hypothesis. The finding is **insufficient adjustment, not incapacity**. Say "systematically and persistently miscalibrated" `[02 §4.4]`.
- **"The expert hears the full orchestration in their head."** Newton never measured vividness; her own informed-observer condition contradicts it; and fluency misattribution alone produces a curse of knowledge **in the absence of knowledge** `[02 §4.3]`.
- **"The audience knows when it doesn't understand."** Both parties are miscalibrated: uninformed listeners overestimated their **own** understanding by 41 percentage points `[02 §4.2]`.
- **"The FPLG mandates BLUF."** It *recommends* it. It self-describes as advice; the words "binding" and "mandatory" appear zero times in 118 pages; and the Plain Writing Act expressly forecloses judicial review and enforceability `[07 §1.5–1.6]`.
- **"Kieras proved conclusion-first doesn't work."** Refuted 0-3 — his "bad" versions **deleted** the conclusion rather than **moving** it. You get no valid evidence *for* BLUF and no valid evidence *against* it `[04 §5.2]`.
- **"Users don't read, they scan"** / **"screen readers scan."** The second is a category error that would encode a false accessibility claim — screen readers **linearize** `[07 §4.1]`, `[09 B5.1]`.
- **"Marketese degrades comprehension and destroys trust."** Only subjective satisfaction reached significance; trust was never measured `[07 §4.1]`.
- **"Concreteness fading is evidence-backed."** The authors' own words are "**theoretical** benefits" and "we recommend"; a later experiment found constantly-concrete matched or beat fading `[05 §6]`.
- **"Concrete beats abstract"** (birds and worms). In the study Kintsch cites, concreteness was the **control** variable, held constant while performance swung ~60 points on question wording alone `[01 §5]`.
- **"Preparing to teach wears off after a week."** A 28-study meta-analysis names and rejects this: delayed **g = 0.53 > immediate g = 0.28** `[08 §6]`.
- **"The comprehension check must not be multiple-choice."** Contradicted by the source: "post-hoc tests found no significant differences among them" `[08 §8]`.
- **"People cannot self-assess comprehension."** Restricted to **explanatory/mechanistic** knowledge; there was **no drop** for procedures or narratives. Self-report is **weak** (metacomprehension gamma ≈ .27), not **invalid** `[08 §3]`, `[09 B4.4]`.
- **"Bridging an inference costs ~150 ms."** The authors said "the absolute differences between conditions cannot be taken very seriously." Direction only `[04 §6.2]`.
- **Gricean maxims as a style checklist or a politeness rubric.** Grice himself excludes "Be polite" from the conversational maxims and calls his own scheme "too narrow". They are expectations hearers exploit, not instructions writers follow — and paraphrasing them as "be clear, be brief, be honest, be relevant" silently deletes the second Quantity maxim (**do not be *more* informative than required**) `[03 §6]`.

---

## 6. Confidence tiers

Brutally honest. A skill that presents weak advice as strong is worse than no skill.

### STRONG — multiple primary sources and/or unanimous verification. Coach these without hedging the direction.

| Advice | Warrant |
|---|---|
| Verify understanding by making the person produce something (restate, explain, apply) | Self-explanation **g = 0.55 [0.45, 0.65], k = 69, N = 5,917**, robust across task type, subject and education level `[08 §4]`; teach-back 19/20 studies, 9 RCTs `[08 §5]`; Griffey ED RCT, OR 3.61 `[08 §1]` |
| Passive checks ("any questions?", nods, "okay") do not verify anything | Clark & Wilkes-Gibbs 3-0 (feigned understanding); Clark & Brennan 3-0 (positive evidence); Kemp et al.; perceived comprehension did not move even when actual comprehension did `[03 §2]`, `[08 §1–2]` |
| Your own sense of your clarity is not evidence | Newton 3-0 (outside the entire prediction range); CLW 3-0 (incentives and feedback fail; markets halve) `[02 §1–2]` |
| Cost is over chunks in the receiver's head; there is no audience-independent "plain" | Cowan 3-0 ×2; element interactivity 3-0; expertise reversal d = +0.505 / **−0.428** 3-0; FPLG 3-0 `[01 §1–4]`, `[07 §1.1]` |
| Frame (topic) before details; a late frame does not repay the debt | Bransford & Johnson 3-0, replicated in Exps III and IV; Clark & Haviland 3-0; the Topic-After null independently corroborated by schema theory's own critics `[04 §1–2]` |
| Make structure visible (headings, signposts, enumeration) — for experts too | Schneider et al. 2018, 3-0: **k = 103, N = 12,201**, retention g+ = 0.53, transfer g+ = 0.33, **prior knowledge not a moderator** `[04 §3]`, `[06 §4]` |
| An analogy must map relations, not looks | Gentner 1983, 3-0 (the "mere appearance match" is named in the source) `[05 §2–3]` |
| Two structurally-matched, surface-different examples + an explicit "what do they share?"; state the mapping out loud | Gick & Holyoak 1983, 3-0 — hint 75% vs no hint 30%; two analogs 45% vs one 21% `[05 §4]` |
| Put the label on the thing; synchronize speech with the visual — most of all for complex, interdependent material | Ginns 2006, 3-0 (high-EI d = 0.78 vs low-EI d = 0.28 n.s.); Schroeder & Cenkci 2018 g = 0.63, k = 58 `[06 §2]` |
| Silence is not evidence of understanding, in any language | Dingemanse et al. 2013/2015, 3-0 — repair documented in every spoken language investigated, ~once per 1.4 min `[03 §5]` |
| Readability scores may never be a target or proof of clarity | Bailin & Grafstein 3-0; Gruteke Klein et al. 3-0; ISO 24495-1 WG declined to endorse them `[07 §2]` |
| Surprisal is the one cross-linguistically supported difficulty **locator** | Wilcox et al. 2023, TACL, 3-0 — 11 languages, 5 families, "in all languages tested" `[07 §3]` |

### MODERATE — split votes, single primary sources, or a solid direction with a contested magnitude. Coach the direction; do not sell the number.

| Advice | What weakens it |
|---|---|
| Cut the interesting-but-irrelevant tangent | Harp & Mayer **2-1**. Pooled d = 0.30 / 0.48 (small-to-medium); 11 of 39 studies supported, 15 did not; a failed replication on the identical material; **language moderates the effect size**. The *workaround-failure* half (highlighting/objectives/signaling do not rescue it) is what keeps this actionable `[05 §7]` |
| Prefer plain wording over an unowned technical term | Direction carried by the chunk argument (language-neutral, 3-0). The empirical study is **one** English experiment, N = 650, measuring *processing fluency*, not comprehension; the magnitude is an English-specific artifact `[05 §8]` |
| Text on slides helps in the named conditions; the harmful case is narrow | Adesope & Nesbit 3-0, **but** the redundancy benefit concentrates in L2 learners, non-fluent L1 readers and struggling readers; the literature is overwhelmingly English-language postsecondary `[06 §5–6]` |
| In live dialogue, a repairable draft beats an over-planned utterance | Both least-collaborative-effort claims passed **2-1**. Davies (2007) argues "effort" is under-operationalized; Pickering & Garrod explain the same coordination via automatic priming `[03 §4a]` |
| Verbosity is not free — distance evicts the load-bearing proposition | Kintsch is a **simulation**, not an experiment; his own hedges say "could have been maintained" and "far from an unequivocal prediction of failure". Human corroboration exists (Fuchs et al., d = 0.73 for **irrelevant** info) `[01 §5]` |
| Audit compressed in-group vocabulary before using it outside | Numbers 3-0, but the **causal mechanism** of compression is contested (Bangerter et al. found reduction even where object-specific pacts cannot form) `[03 §3]` |
| Frame the comprehension check collaboratively (burden on the speaker) | Kemp **2-1**, and it is the **weakest evidence in the knowledge base**: a video-vignette analog study measuring **preference and perceived effectiveness only** — comprehension was never measured. 100 adults, US, English, 94/100 white `[08 §7]` |
| "You'll need to explain this later" is a legitimate supplement | One meta-analysis (Kobayashi 2019, 28 studies): delayed g = 0.53, immediate g = 0.28. A supplement, **not** a substitute for the act of explaining `[08 §6]` |
| Make them produce a causal model when a causal model is what they need | The surviving core of a claim **refuted as usually stated**. Restricted to explanatory/mechanistic knowledge; no drop for procedures or narratives `[08 §3]` |
| "Who is listening" is a real lever on how you speak | Bell's role *hierarchy* statement is 3-0, but the newscaster evidence is n = 4, 1974, no inferential statistics, plausible institutional confound; Bell walked back the topic/setting derivation himself; the overreach ("audience is *the* primary lever") was refuted `[03 §8]` |

### WEAK / HEURISTIC — practitioner sources that wobbled, or rules with no evidence in this knowledge base. Say so out loud when you use them.

| Advice | Honest status |
|---|---|
| BLUF / answer-first ordering | **No comprehension evidence exists here.** The FPLG *recommends* it but is non-binding advice; Kieras never ran the manipulation; the one direct head-to-head went *against* the inverted pyramid (small effects, German). It bought **early interest**, not understanding. **Coach it as a triage/scanning convention and label it as one** `[04 §5]` |
| Topic sentence leading each paragraph | A reasonable convention in the FPLG's own voice. The famous NN/g "readers only read the first sentence" validation is an unquantified anecdote from an exploratory arm, refuted 0-3 `[07 §1.4, §4.1]` |
| Paragraph length 150 / 250 words; "one idea per sentence" | Attributed to "**writing experts**", sourced to two legal-writing style manuals with **no empirical study**. Not automatable ("idea" and "topic" have no operational definition in the source). **English-only artifacts** `[07 §1.4, §1.6]` |
| Strip boosterism | A **preference/satisfaction** finding from a non-peer-reviewed 1997 vendor report, ~10 participants per cell, never replicated, whose largest effect **reversed** in an independent test. Legitimate reason to strip it; not a comprehension claim `[07 §4]` |
| Start concrete, then say the general rule out loud | The authors' own words are "**theoretical** benefits" and "we recommend"; refuted 0-3 as evidence-backed; a later experiment found constantly-concrete matched or beat fading. **If you want a rule with data behind the same goal, use the two-example rule instead** `[05 §6]` |
| Flagging "obviously" / "simply" / "just" / "as you know" | **HEURISTIC — explicitly non-evidence-backed.** No validating study, no effect size, no test that removing them helps. A prompt for a human decision, never a score, never cited to research. English lexical items only `[02 §3.1]` |
| Designing for scanning online | **HEURISTIC.** Scanning is a real mode; the numbers behind the advice are not usable `[07 §4]` |
| Where the collaborative-dialogue rules stop in semi-interactive media (async chat, PR comments, commentable docs) | **OPEN QUESTION — no source resolves it.** Do not fabricate a rule `[03 §4b]` |

---

## The meta-rule

**Never let a rule inherit more confidence than its source.** The academic layer in this knowledge base is strong — primary, peer-reviewed, quote-verified against actual PDFs. The practitioner layer is much weaker: the two most-cited practitioner sources both wobbled badly. When you cannot cite it, do not assert it. When it is a heuristic, say the word "heuristic".
