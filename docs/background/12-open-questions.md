# Open questions, unverified material, and known limits of this knowledge base

> **What this is.** The audit trail for every other document in this knowledge base: how the evidence was gathered and adjudicated, which of its rules are weaker than they look, which questions are still open, and which extracted material was never checked and therefore may not be used.
> **Evidence base.** 80 confirmed claims and 50 refuted claims across two adversarial verification passes (pass 1: 32 confirmed / 28 refuted; pass 2: 48 confirmed / 22 refuted). A further 79 pass-1 claims were extracted but never adjudicated.
> **Load this when.** The coaching task involves citing a number, quoting a rule as authoritative, generalizing a finding to a new language, deciding how much confidence a recommendation deserves, or answering "how do you know that?"

---

## 1. How this was built

### The method

Two multi-agent research passes.

1. **Retrieval.** Agents fetched primary sources — journal PDFs, dissertations, standards documents, style guides — rather than working from summaries or memory.
2. **Claim extraction.** Each claim was extracted with a verbatim quote from the fetched source and the source URL attached.
3. **Adversarial adjudication.** Each adjudicated claim was sent to **three independent verifiers whose instruction was to REFUTE it**, not to confirm it. Each verifier was required to **retrieve the source independently** and check the quote verbatim against the actual document — not against the extracting agent's rendering of it.
4. **Voting.** Two refutations out of three kill a claim. Votes are recorded and reported: `3-0` is unanimous confirmation, `2-1` is a split confirmation, `0-3` is unanimous refutation.

### The counts

| Pass | Scope | Claims extracted | Adjudicated | Confirmed | Refuted |
| --- | --- | --- | --- | --- | --- |
| Pass 1 | 28 sources | 139 | 60 | 32 | 28 |
| Pass 2 | 10 gap topics | 70 | 70 | 48 | 22 |
| **Total** | | **209** | **130** | **80** | **50** |

Refutation rate across both passes: 50 of 130 adjudicated claims, or roughly 38%. That number is the strongest single argument for having run the process at all: more than a third of what plausible-sounding, source-attributed extraction produced did not survive contact with the source.

### What this method buys — and what it does not

**What it buys.** A claim that survived three skeptical verifiers, each of whom independently pulled the primary document and checked the quote against it, is materially stronger than a citation nobody opened. The process caught concrete, load-bearing errors that would otherwise have shipped:

- Newton's dissertation is titled *"The rocky road from actions to intentions"* — **not** the widely-repeated *"Overconfidence in the communication of intent"* — it is unpublished and never peer-reviewed, and the "curse of knowledge" label was attached to it by *Made to Stick* (2007), not by Newton ([Newton 1990, primary PDF](https://gwern.net/doc/psychology/cognitive-bias/illusion-of-depth/1990-newton.pdf)).
- `plainlanguage.gov/guidelines/` now 301-redirects to a landing page that **does not contain** the text everyone quotes from it — so a whole family of "federal plain-language rules" failed verification on citation grounds ([digital.gov principles page](https://digital.gov/guides/plain-language/principles)).
- Two of the most-cited PDFs in this literature — the CMU-hosted Clark & Brennan (1991) and the Stanford-hosted Bell (1984) — are **image-only scans with no text layer**, so no downstream verifier can quote-check them at all. Cite the [Stanford author copy of Clark & Brennan](https://web.stanford.edu/~clark/1990s/Clark,%20H.H.%20_%20Brennan,%20S.E.%20_Grounding%20in%20communication_%201991.pdf) instead.

**What it does not buy.** This is **not peer review.** Read the following as binding limits on how much confidence any rule in this knowledge base may inherit:

- **The verifiers are LLMs.** Three LLM verifiers reading the same document can share a blind spot that three human referees in the field would not. A unanimous `3-0` means three skeptical readers failed to break it, not that the finding is true.
- **A refutation is usually an overreach-detection, not a falsity-detection.** The typical refuted claim is a *real finding stretched past what its source supports* — a mechanism attached to a behavioural result, a box-score inflated into a universal constant, a document-level instruction rescaled to sentence level. This is why refuted claims are preserved in this knowledge base as content rather than deleted: the refutation tells you precisely where the real finding stops.
- **A `2-1` confirmation is a weak confirmation.** It means one of three adversaries found grounds to kill it. Where a document below reports a split vote, treat the claim as directional rather than settled.
- **Budget, not judgment, decided what got adjudicated.** 79 of 139 pass-1 claims were never voted on at all (see §4).
- **Verification checks the claim against its source. It does not check the source.** A quote can be verbatim-correct and the underlying study still small, dated, unreplicated, or vendor-authored. §2 is about exactly that failure mode.

---

## 2. Known weaknesses

### 2.1 Source-quality asymmetry: the academic layer is strong, the practitioner layer is weak

**The academic layer is strong** — primary, peer-reviewed, quote-verified against actual PDFs: Cowan (2001, *BBS*), Miller (1956), Camerer, Loewenstein & Weber (1989, *JPE*), Clark & Wilkes-Gibbs (1986, *Cognition*), Clark & Brennan (1991), Clark & Haviland (1977), Kintsch (1988, *Psych Review*), Ginns (2006), de Jong (2010), Dingemanse et al. (2013/2015), Bell (1984).

**The practical layer is much weaker, and the two biggest practitioner sources both wobbled.**

*What people believe:* Nielsen Norman Group measured that web writing is 58% better when concise, 47% better when scannable, 27% better when objective, and 124% better when all three are combined.

*What the evidence actually says:* the figures are quoted correctly, but the study cannot carry the weight put on it ([Morkes & Nielsen 1997](https://www.nngroup.com/articles/concise-scannable-and-objective-how-to-write-for-the-web/), rated **low confidence, confirmed 2-1**). It is a 5-condition **between**-subjects design, n=51 total (≈10 per cell), one fictitious 7-page site, one-tailed t-tests. "Measured usability" is a geometric mean of five normalized measures (task time, errors, memory, sitemap-drawing time, satisfaction) with control = 100 — **not a comprehension measure**. The 27% "objective" figure rests mostly on non-significant differences. It is a self-published vendor report, not peer-reviewed. And the independent test went the other way: Elgin, Jones, Anders & Farris (2001, HFES, n=80) found "fewer idea units were correctly recalled for the concise writing style than the scannable, objective, and combined writing styles" — **the opposite direction for Nielsen's single largest effect** ([HFES 2001](https://doi.org/10.1177/154193120104501513)).

*What people believe:* Mayer's multimedia principles come with clean box-score effect sizes — coherence supported in 23 of 23 tests (median d = 0.86), redundancy 16 of 16 (d = 0.86), spatial contiguity 22 of 22 (d = 1.10), temporal contiguity 9 of 9 (d = 1.22).

*What the evidence actually says:* **these specific numbers did not clear adversarial verification** (**refuted 0-3 / 1-2 / 0-3 / 1-2**), and neither did the extraneous-cognitive-load *mechanism* usually offered to explain them ([Mayer & Fiorella chapter PDF](https://edtechuvic.ca/wp-content/uploads/sites/11/2022/09/principles-for-reducing-extraneous-processing-in-multimedia-learning-coherence-signaling-redundancy-spatial-contiguity-and-temporal-contiguity-principles.pdf)). They are the most-quoted numbers in slide-design advice, and they are exactly what failed. What survived is the independently meta-analysed contiguity effect: Ginns (2006), 50 effects, 2,375 students, **d = 0.85, 95% CI [0.68, 1.02]** ([Learning and Instruction](https://www.sciencedirect.com/science/article/abs/pii/S0959475206000806)), and Schroeder & Cenkci (2018), 58 comparisons, n = 2,426, **g = 0.63** ([Educ Psych Rev](https://doi.org/10.1007/s10648-018-9435-9)) — but *with* moderation by material complexity and *without* the load mechanism, since Schroeder & Cenkci (2019) found "measures of cognitive load largely do not support the extraneous cognitive load explanation" ([J. Educ. Psych.](https://doi.org/10.1037/edu0000372)).

**The binding instruction: do not let the skill's rules inherit more confidence than their sources.** The popular slide rules are *directionally* supported and must not be sold with these effect sizes.

### 2.2 Pass 1's own synthesis contains at least one error that pass 2 caught

This is worth stating plainly, because it is the clearest evidence that the knowledge base is not self-certifying.

*What pass 1 recorded:* the Federal Plain Language Guidelines "explicitly designate 'dumb it down / write to an 8th-grade level' a myth."

*What pass 2 established:* **partially false as stated** ([Federal Plain Language Guidelines, March 2011 Rev. 1, printed p.1](https://wid.org/wp-content/uploads/2022/03/FederalPLGuidelines.pdf), **confirmed 3-0**). The FPLG does *not* call the 8th-grade target a myth. The myth it names is the **universal-dumbing-down** claim: "One of the most popular plain language myths is that you have to 'dumb down' your content so that everyone everywhere can read it. That's not true. The first rule of plain language is: write for your audience... Don't write for an 8th grade class if your audience is composed of PhD candidates, small business owners, working parents, or immigrants. **Only write for 8th graders if your audience is, in fact, an 8th grade class.**" The 8th-grade target is therefore **audience-conditional — permitted, indeed required, when the audience genuinely is 8th graders**. The FPLG rejects a *fixed universal* grade-level target, not grade-level targeting as such.

A second pass-2 correction of the same source: **the FPLG does not describe itself as binding** (**confirmed 3-0**, same PDF). Its introduction calls itself "advice"; the strings "Plain Writing Act", "Act of 2010", "binding" and "mandatory" occur **zero times in all 118 pages**. Do not cite it as a mandate.

### 2.3 Citation hygiene problems found (fix before shipping anything downstream)

1. `plainlanguage.gov/guidelines/` 301-redirects to a digital.gov landing page that **does not contain** the quoted text. Cite [digital.gov/guides/plain-language/principles](https://digital.gov/guides/plain-language/principles) or the [archived FPLG PDF](https://ies.ed.gov/sites/default/files/rel-central/document/2024/10/Federal%20Plain%20Language%20Guidelines.pdf).
2. The CMU-hosted Clark & Brennan (1991) PDF and the Stanford-hosted Bell (1984) PDF are **image-only scans** and cannot be quote-checked by any downstream verifier. Cite the [Stanford author copy](https://web.stanford.edu/~clark/1990s/Clark,%20H.H.%20_%20Brennan,%20S.E.%20_Grounding%20in%20communication_%201991.pdf) for Clark & Brennan.
3. Newton's dissertation title, publication status, and the provenance of the "curse of knowledge" label — see §1.
4. The Bransford & Johnson topic manipulation is primarily reported in the **1972 JVLVB paper**, not the 1973 chapter ([JVLVB 1972](https://memlab.yale.edu/sites/default/files/files/1972_Bransford_Johnson_JVLVB.pdf)).

### 2.4 The DO-NOT-OVERREACH list

Each row is a defensible claim that becomes a **false** one if stated in the tempting form.

| Tempting form (do not say this) | What is actually supported |
| --- | --- |
| "Working memory holds 4 slots" / "never more than 4 bullets" | Capacity is ~3–5 **chunks**, and only under Cowan's stated boundary conditions (rehearsal and recoding blocked). Chunks are relative to the receiver's long-term knowledge, so the number of presentable "things" is a function of the audience, not a constant ([Cowan 2001, confirmed 3-0](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/44023F1147D4A1D44BDC0AD226838496/S0140525X01003922a.pdf/the-magical-number-4-in-short-term-memory-a-reconsideration-of-mental-storage-capacity.pdf)). The "usable budget is ~3-4 units" and "in a live audience the limit is ~3 items" framings were **refuted 0-3**. |
| "Reduce extraneous load" as a standing rule | The extraneous/germane distinction is, in de Jong's words, of "quite tautological character (what is good is good, what is bad is bad)", and Paas et al. concede "a cognitive load that is germane for a novice may be extraneous for an expert" ([de Jong 2010, confirmed 3-0](https://link.springer.com/article/10.1007/s11251-009-9110-0)). The rule has **no audience-independent definition**; you must fix who is listening first. |
| "LLMs cannot assess readability" | Overbroad. The surviving claim is narrower: readability formulas, ML systems, commercial systems **and** frontier LLMs "are all poor predictors of reading ease in English" when validated against eye-tracking ([Gruteke Klein et al. 2025, confirmed 3-0](https://arxiv.org/abs/2502.11150)). LLM scores are *not validated against real-time processing ease* — that is not the same as "LLMs cannot assess readability", and peer-reviewed evidence contradicts the broad form. |
| "Closer is always better" for labels and diagrams | Falsified by the documented **spatial-contiguity failure**: maximum proximity underperformed *medium* proximity, because cramming related and unrelated elements together causes interference (Beege et al. 2019; see [Frontiers in Education](https://www.frontiersin.org/journals/education/articles/10.3389/feduc.2019.00086/full)). Contiguity also barely pays for low-element-interactivity material: Ginns' own confirmed Hypothesis 2 gives high-EI **d = 0.78** vs low-EI **d = 0.28, p > .05**, and he writes that with low intrinsic load "lack of integration of related elements may be inconsequential." |
| "Grounding / least-collaborative-effort means it's fine to ship an imperfect draft" | **Only in live dialogue.** Clark & Wilkes-Gibbs explicitly exclude novels, letters, broadcasts, sermons and large lectures. Where the addressee cannot repair, the **self-sufficient utterance IS the right target** ([Clark & Wilkes-Gibbs 1986, confirmed 2-1](http://www.web.stanford.edu/~clark/1980s/Clark,%20H.H.%20_%20Wilkes-Gibbs,%20D.%20_Referring%20as%20a%20collaborative%20process_%201986.pdf)). |
| "Clark & Haviland validate BLUF" | They validate **frame-before-details**, a different construct. Topic/schema-first (an advance organizer) is not conclusion-first. Say "provides a psycholinguistic rationale for frame-before-details" ([Clark & Haviland 1977, confirmed 3-0](https://web.stanford.edu/~clark/1970s/Clark,%20H.H.%20_%20Haviland,%20S.E.%20_Comprehension%20and%20the%20given-new%20contract_%201977.pdf)). |
| "Experts are literally unable to reason as if they didn't know" | **Refuted 0-3.** The defensible statement is that they are *systematically and persistently miscalibrated*, and that markets, feedback and incentives at best **halve** the bias, never eliminating it ([Camerer, Loewenstein & Weber 1989](https://www.cmu.edu/dietrich/sds/docs/loewenstein/CurseknowledgeEconSet.pdf)). |
| "The expert hears the full orchestration in their head, which is why they can't hear how thin their signal is" | **Refuted 1-2 / 0-3 / 0-3.** The vivid-internal-representation mechanism, the "informed observers were identically overconfident" elaboration, and the "listeners predicted ~3% while tappers predicted 50%, so the expert is the sole locus of error" story are all popular retellings (largely downstream of *Made to Stick*) that could not be substantiated from Newton's dissertation at the strength claimed. **Keep the headline** (tappers predicted 50%, actual was 2.5% — 3 hits in 120 tries) and **drop the mechanism**. |

### 2.5 LANGUAGE SCOPE — what may and may not be generalized

The skill must work across languages. This list is binding.

**ENGLISH-SPECIFIC ARTIFACTS — never generalize these to another language:**

- End-of-sentence focal stress.
- Cleft / pseudocleft / passive information-packaging.
- Definite-noun-phrase-first tendencies.
- **All readability formulas.** (The 2025 eye-tracking paper's own abstract restricts its finding to English.)
- ISO 24495-1's worked examples — ISO itself states: *"This document applies to most, if not all, written languages, but it provides examples only in English"* ([ISO 24495-1:2023](https://www.iso.org/standard/78907.html)).
- Bell's intervocalic /t/-voicing variable.
- The `FBICIAUSA` chunking illustration.
- English backchannel tokens ("uh huh", "yeah").

**CROSS-LINGUISTICALLY SUPPORTED — safe to apply beyond English:**

- The curse of knowledge.
- Chunk-relative working-memory capacity.
- Grounding, and the seeking of positive evidence of understanding.
- **Repair infrastructure**, documented across 8+ language families: "Sequences of other-initiated repair have been identified in every spoken language investigated so far"; "no language appears to lack an interjection for this function" — 10 languages studied in depth across 5 continents plus 21 from published sources, and 12 languages from 8 families in the follow-up, used on average about **once every 1.4 minutes** in every language ([Dingemanse, Torreira & Enfield 2013, confirmed 3-0](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0078273); [Dingemanse et al. 2015](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0136100)). **Carry the hedges:** this is an inductive generalization over ~30 languages out of ~7,000 and the authors themselves hedge with "likely to be attested"; and universality of the *mechanism* does **not** entail cross-cultural uniformity in *willingness* to initiate repair — face and politeness norms modulate that heavily.
- Audience design as a principle (though Bell's specific variable is not).
- Frame-before-details.
- Spatial and temporal contiguity.
- **Surprisal as a difficulty signal** — added in pass 2, see §3.1.

### 2.6 Time-sensitivity

The Cognitive Load Theory critiques are dated 2010; differentiated load instruments and physiological measures are more common now, and **post-2010 CLT is a two-load theory** — germane load was demoted by Sweller himself in 2010 and called redundant by Kalyuga in 2011. The LLM-readability finding uses current-generation frontier models but is **a preprint** and will need re-checking. Everything else (Miller, Cowan, Clark, Kintsch, Bell) is foundational literature in slow-moving fields.

---

## 3. Open questions

### 3.1 Closed by pass 2 — do not re-open these as unknowns

Pass 1 ended with five open questions. Pass 2 was run specifically to close them, and **four are now closed**. The results live in the sibling documents of this knowledge base, not here.

| Pass-1 open question | Status | Where the answer lives |
| --- | --- | --- |
| Do the Federal Plain Language Guidelines actually mandate BLUF and the 150/250-word paragraph limits, or was that an artifact of the dead URL? | **CLOSED.** It was a citation problem, not a falsity problem. The archived FPLG PDF was retrieved and the rules were adjudicated against it — including the finding that the FPLG is self-described **advice**, not a mandate, and that the 150/250-word numbers, while real, are **not asserted in the FPLG's own voice** (both **confirmed 3-0**). | The plain-language document |
| What are the real, currently-defensible effect sizes for Mayer's coherence, signaling, redundancy and modality principles? | **CLOSED.** Re-verified against independent meta-analyses rather than box-scores. Note the durable result: the behavioural effects hold, the **cognitive-load mechanism does not**. | The multimedia / presentations document |
| Mehrabian 7-38-55, the "8-second attention span", learning styles — what are the primary sources and the actual refutations? | **CLOSED.** All three were researched and adjudicated in pass 2, with primary sources retrieved. | The myths document |
| Does surprisal-based difficulty transfer cross-linguistically? | **CLOSED — YES.** On the MECO eye-tracking corpus (same article content translated into each language), models including surprisal are significantly better predictors of reading times than baselines **in all eleven languages tested**, spanning five families — Koreanic, Turkic, Semitic, Uralic, Indo-European ([Wilcox, Pimentel, Meister, Cotterell & Levy 2023, TACL, **confirmed 3-0**](https://arxiv.org/html/2307.03667v4)). **Carry the authors' own limits:** 7 of 11 languages are Indo-European; no African, Austronesian or signed languages; predictive power varies by language and the variation is not explained by training-data size. | The measurement / readability documents |

### 3.2 Still genuinely open

**(1) Can an LLM reliably estimate its own token surprisal, well enough to use as a coaching signal?**

Nothing in this knowledge base answers this. The pieces that *are* verified stop short of it:

- Surprisal is **definitionally** language-neutral and formula-free: per-word cognitive load is the negative log probability of word *wᵢ* given its prefix, requiring no syllable counting, no word-length proxy, and no English-tuned regression constants — only a probability distribution over next words, which any autoregressive LM supplies for any language ([Hale 2001, NAACL, **confirmed 3-0**](https://aclanthology.org/N01-1021.pdf)). **The definition is language-neutral; Hale's 2001 evidence is English-only.**
- Levy proved the metric is representation-agnostic: under a resource-allocation formulation of difficulty, "regardless of the form of complete structures T or the preference distribution P_T, the predicted difficulty of the ith word, wᵢ, is precisely equal to the surprisal of wᵢ" ([Levy 2008, *Cognition*, **confirmed 2-1**](https://www.mit.edu/~rplevy/papers/levy-2008-cognition.pdf)). **The split vote is the whole point here.** The dissenting verifier's objection is on the record and directly targets our use case: Levy's proof is conditioned on a *true* generative process, so it proves the formula is well-defined, **not that an approximate LLM estimator is valid or calibrated** — which is exactly what decides whether a Korean or Turkish coach works. The proof is also silent on morphology rather than neutral to it: it presupposes a fixed word segmentation.
- The shape of the surprisal→reading-time link is **contested**. Smith & Levy (2013) established it is "logarithmic over six orders of magnitude in estimated predictability" — which is what would license a coach to simply *average* per-token surprisal across a passage ([Smith & Levy 2013, **confirmed on a 1-1 vote**](https://vorpus.org/papers/smith-levy-2013-predictability-logarithmic.pdf)). That is the weakest confirmation in this knowledge base, and the contradiction is on the record: Brothers & Kuperberg (2021, *JML*) is titled in direct opposition — "Word predictability effects are linear, not logarithmic" — across three datasets with roughly 20× the participant counts. Both papers' evidence is English.

So the open question is precise: **the theory says surprisal is the right signal and it transfers across languages; nobody in this evidence base has shown that a language model can introspect its own next-token distribution accurately enough, or aggregate it correctly enough, to hand a writer a trustworthy difficulty score.** Until that is tested, treat any LLM-computed surprisal score the way §2.4 tells you to treat a readability score: a smell test, never a target metric, never proof of clarity.

**(2) Where exactly does the collaborative-repair machinery stop being available in semi-interactive media?**

This is the sharpest practical gap in the knowledge base, and it is unresolved.

The literature draws its line at **whether the audience can talk back**. On one side, live dialogue: speakers optimize *least collaborative effort* — the combined work of speaker and addressee — and therefore rationally emit imperfect utterances (self-repairs, try markers, invited completions) and let the listener help refashion them ([Clark & Brennan 1991](https://web.stanford.edu/~clark/1990s/Clark,%20H.H.%20_%20Brennan,%20S.E.%20_Grounding%20in%20communication_%201991.pdf), **confirmed 2-1**). On the other side, Clark & Wilkes-Gibbs explicitly exclude novels, letters, broadcasts, sermons and large lectures — where the addressee cannot repair, the self-sufficient utterance is the target.

**Modern artifacts sit in between and the literature does not tell us where they fall.** Async chat, PR review comments, and documents with comment threads all *have* a repair channel, but a slow, costly, publicly-visible, and optional one.

What the knowledge base does supply is the **dimensions**, not the rule. Clark & Brennan enumerate eight medium constraints — **copresence, visibility, audibility, cotemporality, simultaneity, sequentiality, reviewability, revisability** — and eleven costs that shift across media — **formulation, production, reception, understanding, start-up, delay, asynchrony, speaker change, display, fault, repair**. Both lists were **verified verbatim** against the primary text. Nevertheless the surrounding claim was **REFUTED (1-2)**, and the reason matters: the claim asserted that this framework "yields a falsifiable prediction confirmed by Cohen (1984)", and the verifiers found that framing to be a misread of the source. The counter-source is blunt about the state of the art — Monk (2003) writes that the framework "has yet to be fleshed out in sufficient detail" to yield mechanical predictions ([Monk 2003](https://www-users.york.ac.uk/~am1/Monk2003CommonGrnd.pdf)).

**Operational consequence, stated honestly:** for async chat, PR comments and commented docs, the skill has a vocabulary (which constraints hold? which costs are high?) but **no validated rule**. The conservative default — which this knowledge base recommends *as a default, not as a finding* — is to treat any medium where the reader may not answer as a writing medium, and target the self-sufficient utterance.

### 3.3 Open in the literature itself (not merely unverified here)

These are live scientific disputes flagged inside confirmed claims. The skill must not pretend they are settled in either direction.

| Dispute | State of play |
| --- | --- |
| **Slot vs. flexible-resource models of working memory** | Open (Bays & Husain; Ma, Husain & Bays). Relatedly, Thalmann, Souza & Oberauer (2019, *JEP:LMC*) show "WM capacity is not limited to a fixed number of chunks regardless of their size" — chunking discounts load substantially, but **a large familiar chunk is not perfectly free** ([DOI](https://doi.org/10.1037/xlm0000578)). |
| **The mechanism of the curse of knowledge** | Contested. Tullis (2022, *Mem & Cogn*) finds estimators fail not from over-reliance on their own knowledge but from **lacking diagnostic cues about others** ([PMC](https://pmc.ncbi.nlm.nih.gov/articles/PMC9794110/)); Ryskin & Brown-Schmidt (2014, *PLoS ONE*, 7 experiments) **failed to replicate** Birch & Bloom's adult false-belief curse ([PLoS ONE](https://journals.plos.org/plosone/article/file?id=10.1371/journal.pone.0092406&type=printable)). The *behavioural* finding is robust; the *why* is not. |
| **Joint vs. individual effort in dialogue** | Contested. Davies (2007) argues "effort" is under-operationalized (utterance length ≠ effort) and the data may reflect individual motivation ([PDF](https://www.latl.leeds.ac.uk/wp-content/uploads/sites/49/2019/05/Davies_2007.pdf)); Pickering & Garrod (2004, *BBS*) explain the same coordination via **automatic priming** with no joint-effort minimization ([PDF](https://www.pure.ed.ac.uk/ws/files/11823730/Toward_a_mechanistic_psychology_of_dialogue.pdf)); Horton & Keysar (1996) show common ground is **not** used in initial planning under time pressure. |
| **Why contiguity works** | The behavioural effect survives; the extraneous-cognitive-load explanation does not ([Schroeder & Cenkci 2019](https://doi.org/10.1037/edu0000372)). Design your slides on the effect, not on the story. |
| **What causes the compression of grounded language** | Contested. Bangerter et al. found lexical diversity also drops in a "new cards" condition where object-specific conceptual pacts cannot form — so entrainment may partly reflect shared *interactional history* or speaker-side accessibility rather than mutual knowledge per se ([JML](https://www.sciencedirect.com/science/article/abs/pii/S0749596X20300437)). **Consequence:** do not use brevity alone as a diagnostic of common ground; use the acceptance/repair mechanism instead. |
| **Bell's audience-role hierarchy** | Empirically contested; and the newscaster study is n = 4, 1974 data, with no inferential statistics on the key figure. "Only the audiences differ" is **Bell's inference**, not an independently validated fact. |

---

## 4. Unverified backlog — do not rely on any of this

**79 of the 139 pass-1 extracted claims were never adjudicated.** They fell outside the verification budget. They are not "probably fine"; they are **unknown**, and a third of everything comparable that *was* checked did not survive.

The unverified backlog includes, among other material:

- Claims extracted from the **Google developer documentation style guide** (jargon, voice and tone, word list).
- Claims extracted from the **Microsoft Writing Style Guide** (lists, scannable content, global-communications writing tips).
- Several **BBC**, **Wiley** and **SAGE** sources.

**The rule for anything drawn from that backlog:** it may not be asserted, cited, or used to justify a coaching rule until it has been through the same three-verifier adjudication as everything else. If a downstream document quotes one of these, it must sit under an explicit "Unverified — do not rely on" heading and carry no vote, because it has none.

Note the asymmetry that makes this survivable: several *practices* whose usual citations failed verification have **independent** support elsewhere in this knowledge base. Answer-first ordering has a psycholinguistic rationale via the given-new/topic finding, and paraphrase/teach-back testing has strong independent RCT support from the health-literacy literature. **The practice can be defensible while the citation is not.** Fix the citation; do not silently keep quoting the dead one.

---

## What this does NOT license

A reader who has absorbed the rest of this knowledge base may be tempted into each of the following. None of them is supported.

1. **"Never more than 4 bullets / 3 things."** No verified claim licenses a magic number. Capacity is over knowledge-relative *chunks*; the correct move is to reduce the chunk count *for this audience* (pre-teach labels, group by familiar structure), never to enforce a constant. The "3-4 usable units" and "~3 items for a live audience" formulations were **refuted 0-3**.
2. **"Reduce extraneous load" as a standalone instruction.** It has no audience-independent meaning. Fix who is listening and what they must end up able to do, first.
3. **"Aim for grade 8" / "hit a readability target."** Readability formulas are not a valid measure of text difficulty and must never be a target metric or proof of clarity — and the FPLG's actual position is that the 8th-grade target is *audience-conditional*, correct precisely when the audience is 8th graders and wrong otherwise.
4. **"An LLM can score clarity."** Frontier LLMs were tested alongside the formulas against eye-tracking and were also poor predictors of reading ease **in English**. Do not upgrade this into "LLMs cannot assess readability" (overbroad, and contradicted), and do not downgrade an unvalidated LLM score into a target metric.
5. **"Put the label as close as physically possible."** Maximum proximity has been documented to *underperform* medium proximity. And for simple, low-interactivity material, integration may be "inconsequential" — Ginns' own words.
6. **"Ship the rough draft, they'll ask if they're confused."** Valid in live dialogue only. In writing, broadcast, and any medium where the reader cannot cheaply repair, the self-sufficient utterance is the target. And in **every** medium, silence is not evidence of understanding: listeners are under systematic pressure to feign it.
7. **"BLUF is validated by psycholinguistics."** Frame-before-details is. Conclusion-first is a different construct, and the study everyone cites for it does not test ordering at all.
8. **"The expert literally cannot imagine not knowing."** They are persistently miscalibrated, and incentives and feedback do not fix it — but "literally unable" was refuted, and the vivid-internal-representation mechanism is a popular retelling, not a finding.
9. **"These effect sizes are real: d = 0.86, 22 of 22 tests…"** Those box-scores did not survive verification. Use the independently meta-analysed figures (Ginns d ≈ 0.85 with severe heterogeneity; Schroeder & Cenkci g = 0.63) and say which one you are using.
10. **"Nielsen proved concise writing is 58% better."** One non-peer-reviewed vendor study, ~10 participants per cell, on a composite non-comprehension score — whose largest effect **reversed** in an independent replication.
11. **Generalizing an English artifact to another language.** Focal stress, clefts, definite-NP-first, readability formulas, /t/-voicing, `FBICIAUSA`, and "uh huh" are English. The curse of knowledge, chunk-relative capacity, grounding, repair, audience design, frame-before-details, contiguity, and surprisal are not.
12. **Quoting a rule without its adjacent hedge.** The FPLG offers "advice," not a mandate. ISO 24495-1 says its examples are English-only. Ginns says integration may be inconsequential for simple material. Kintsch refuses the blanket "redundancy is bad" and says overspecification "may be quite harmless, or may even facilitate problem solving." **A rule quoted without its qualifier is a misquote.**
