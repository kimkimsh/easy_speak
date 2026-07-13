# The curse of knowledge: why you cannot judge your own clarity

> **What this is.** The evidence that a person who knows something systematically and persistently overestimates how well their message lands on someone who does not — and that trying harder, being paid, or getting feedback does not fix it.
> **Evidence base.** 3 confirmed claims, 5 refuted claims, 2 unverified claims, from the adversarial verification pass. The refuted block is the most valuable part of this document: this is the most over-told story in the whole field, and most of what circulates about *why* the curse happens did not survive verification.
> **Load this when.** The coaching task involves an expert, author, or insider explaining something to a non-expert; when someone asks "is this clear?" about their own draft; when deciding whether self-review is an acceptable substitute for an external check; or when someone cites the tapping study.

---

## 1. The headline finding

**Rule: an informed person's estimate of how well they are being understood is worthless as a measurement. Treat it as a prior with a known ~20x inflation, not as data.**

Newton's tapping study is the canonical quantitative demonstration. Tappers tapped a tune's rhythm on a table; listeners tried to name the tune.

| Quantity | Value | Source |
|---|---|---|
| Tappers | N = 40 | Newton 1990, [confirmed 3-0](https://gwern.net/doc/psychology/cognitive-bias/illusion-of-depth/1990-newton.pdf) |
| Listeners | N = 40 | same |
| Trials (songs) | 120 | same |
| Tappers' mean *predicted* listener success | **50%** (individual predictions ranged 10–95%) | same |
| *Actual* listener identification | **3 hits in 120 tries = 2.5%** | same |
| Overestimate | **~20x** | same |
| Position of the true value relative to predictions | **Outside the entire range** — below every single tapper's estimate | same |

> VERBATIM: "When asked to estimate the likelihood that their listeners correctly guessed the name of the tune that they had just tapped, subjects' guesses averaged 50%, and ranged from 10 to 95. ... In reality, however, there were only 3 hits in 120 tries, a success rate of only 2.5 perccnt-a rate that was outside the entire range o f the tapper's estimates" (Newton 1990, [confirmed 3-0](https://gwern.net/doc/psychology/cognitive-bias/illusion-of-depth/1990-newton.pdf); *sic* — OCR artifacts in the primary PDF).

The operationally important number is not "50 vs 2.5". It is **"outside the entire range"**: not one of the forty tappers was pessimistic enough. There was no self-aware minority. You cannot select yourself into the calibrated group by being careful, because in this study the calibrated group did not exist.

### 1.1 Citation hygiene — mandatory, and routinely violated

Anyone repeating this study, including this skill, must carry these three corrections ([synthesis caveat, citation hygiene block](https://gwern.net/doc/psychology/cognitive-bias/illusion-of-depth/1990-newton.pdf)):

1. **The real title is "The rocky road from actions to intentions"** (Newton, Elizabeth Louise, Ph.D., Stanford University, June 1990; UMI Order Number 9102821) — **not** the widely-cited "Overconfidence in the communication of intent", which is how the dissertation is misnamed across the secondary literature.
2. **It is an unpublished PhD dissertation.** Never peer-reviewed. The verification pass located **no direct replication**. The adversarial search for failed replications, critiques or disputes returned only secondary retellings (*Made to Stick* derivatives) — meaning the study has neither been overturned *nor* independently confirmed. Confidence in the direction of the effect is high because it is corroborated by the peer-reviewed economics literature below (Camerer, Loewenstein & Weber 1989); confidence in *this study's* exact magnitude should not be.
3. **The label "curse of knowledge" was attached to the tapping study by Heath & Heath's *Made to Stick* (2007) — not by Newton.** Newton does not call it that. (The term itself is used by Camerer, Loewenstein & Weber in the economics literature — "a systematic violation of this assumption that we call the 'curse of knowledge'" — but the *application of the label to the tapping study* is a popularizer's move, not the source's.)
4. **The dissertation is internally inconsistent about its own headline denominator.** The abstract says listeners identified "two out of one hundred fifty tunes" (1.3%); the Results say "3 hits in 120 tries ... 2.5 percent"; the Discussion says "3 out of 150 tunes" (2.0%). ([Verifier reading of the primary PDF, in the refutation of the listener-asymmetry claim, 0-3](https://gwern.net/doc/psychology/cognitive-bias/illusion-of-depth/1990-newton.pdf).) Popular retellings propagate 2.5% without noting that the source disagrees with itself. **Never build an argument that depends on the precision of "2.5%".** The direction and rough order of magnitude are robust; the exact denominator is not.

---

## 2. It is a cognitive failure, not a motivational one — but say that carefully

**Rule: do not coach "care more about your audience" as a fix. Motivation is not the broken part.**

> VERBATIM: "Better-informed agents are unable to ignore private information even when it is in their interest to do so; more information is not always better." (Camerer, Loewenstein & Weber, "The Curse of Knowledge in Economic Settings: An Experimental Analysis," *Journal of Political Economy* 97(5):1232-54, 1989, [confirmed 2-1](https://www.cmu.edu/dietrich/sds/docs/loewenstein/CurseknowledgeEconSet.pdf))

The cognitive-not-motivational reading is **the paper's own experimental design, not a gloss**. The authors explicitly named the motivational alternative as the hypothesis to be tested — "The curse may result from careless thinking by subjects who have no financial incentive to respond accurately. Given the right incentives, it could be conjectured, individuals would exert sufficient cognitive effort to overcome the curse" — then ran incentivized individual-level and market experiments to test it.

Result:

| Condition | n | Effect on the bias | Source |
|---|---|---|---|
| Financial incentives, no feedback | 19 (Chicago MBA students) | **No reduction** | CLW 1989, [confirmed 3-0](https://www.cmu.edu/dietrich/sds/docs/loewenstein/CurseknowledgeEconSet.pdf) |
| Incentives **+ outcome feedback** | 13 (Chicago MBA students) | **No reduction** — "no difference between the biases of subjects in the incentives and feedback conditions" | same |
| Market forces (lab asset market, Wharton students) | — | **~50% reduction. Not elimination.** | same |

> VERBATIM: "We find that feedback alone has little effect, while market forces reduce the magnitude of the curse by approximately 50 percent... There is no difference between the biases of subjects in the incentives and feedback conditions; feedback apparently did not reduce bias." ([confirmed 3-0](https://www.cmu.edu/dietrich/sds/docs/loewenstein/CurseknowledgeEconSet.pdf))
>
> And the authors' own summary of results: "Our objective has been to test whether incentives, experience, and market forces reduce or eliminate the curse of knowledge. The experimental data suggest that incentives and feedback do not reduce the bias, but market forces do." (same)

### 2.1 The exact wording you are allowed to use

Report: **"the bias persists under incentives and outcome feedback."**
Never report: **"motivation is irrelevant"** or **"caring doesn't help."** The tested proposition was narrow — *financial incentives to be accurate*, and *outcome feedback*, in these two conditions, did not move the bias. That is not a general finding about all forms of motivation, effort, or intent. The 2-1 split vote on the definitional claim also means one verifier dissented; the claim survived, but not unanimously.

### 2.2 Known limits of the market result (must travel with the number)

- **The market-vs-individual comparison confounds treatment with subject pool** (Chicago MBAs in the individual conditions; Wharton students in the markets). ([synthesis F0 limits](https://www.cmu.edu/dietrich/sds/docs/loewenstein/CurseknowledgeEconSet.pdf))
- **The market reduction was statistically significant for only 3 of 8 companies.** (same)
- **These were not real markets and not experienced traders.** The setting was a laboratory double-oral auction: informed subjects endowed with two assets and $50 cash, 4-minute trading periods, nine Wharton students, shouting bids. ([refutation of the w-parameter claim, 0-3](https://www.cmu.edu/dietrich/sds/docs/loewenstein/CurseknowledgeEconSet.pdf))

So: "markets halve it" is a lab result about a lab market, with a confounded comparison and a minority of significant company-level cells. Use it to say *the bias is stubborn*, not to say *deploy a market*.

---

## 3. The practical payload: self-assessment of your own clarity is invalid

This is the operational core of the document.

**Rule 1 — Clarity is not self-observable. It is a property of the receiver, and must be measured on the receiver.**
Justification chain, entirely from confirmed claims: informed people massively overestimate how well their message lands (Newton, [confirmed 3-0](https://gwern.net/doc/psychology/cognitive-bias/illusion-of-depth/1990-newton.pdf)); the miscalibration is not repaired by wanting to be accurate, by being paid to be accurate, or by being told the outcome (CLW 1989, [confirmed 3-0](https://www.cmu.edu/dietrich/sds/docs/loewenstein/CurseknowledgeEconSet.pdf)). Therefore an author's own judgment — "this is clear", "anyone can follow this" — carries no evidential weight about clarity. It is a report about the author's internal state, not about the reader's.

**Rule 2 — Never accept "I reread it and it's clear" as a clarity check.** Rereading is performed by the person holding the private information. It re-measures the same broken instrument. The confirmed evidence says outcome feedback did not even fix it; introspection is weaker than outcome feedback.

**Rule 3 — Substitute an external check.** The defensible statement is that informed people are *systematically and persistently miscalibrated*, and that incentives and feedback at best fail and markets at best halve the bias ([synthesis F17](https://www.cmu.edu/dietrich/sds/docs/loewenstein/CurseknowledgeEconSet.pdf)) — so verification has to come from outside the informed head. Where a real naive audience is available, that audience *is* the measurement. (The evidence on *which* external checks actually measure understanding — passive checks like a nod or "any questions?" fail; restate/apply checks work — lives in the grounding and positive-evidence document, not here.)

**Rule 4 — For an LLM coach: refuse the question "is this clear?" as posed.** The only answerable versions are "clear *to whom*, and how would we find out?" An LLM reviewing a draft is not a naive audience either — it has read the internet. It can flag *markers* of the curse (below) and it can flag unexplained terms; it cannot certify comprehension.

### 3.1 LLM-checkable markers of the curse

**Status: heuristic, NOT evidence-backed.** The evidence dossier contains no study validating these markers, no effect size for them, and no test of whether removing them improves comprehension. They are an operational device for surfacing the *shape* of the bias in text — treat them as prompts for a human decision, never as a clarity score, and never cite research for them.

The common thread is **self-certifying language**: a word that asserts the reader's understanding instead of producing it. The author is reporting their own fluency and projecting it onto the reader — which is exactly the failure mode the confirmed evidence describes.

| Marker | What it asserts on the reader's behalf |
|---|---|
| "obviously" | that the inference is already available to them |
| "simply" / "just" | that the step is cheap for them |
| "as you know" / "of course" | that the prior knowledge is shared |
| "trivially" / "clearly" | that no work is required |
| "it goes without saying" | that the content need not be transmitted at all |

Flagging protocol for the coach:
1. Locate each marker.
2. Ask: **does the sentence still stand if the marker is deleted?** If yes, delete it — it was doing no work. If no, the marker was carrying an unstated step, and **that step is the thing the audience is missing**. Write the step out.
3. Do not report a count as a metric. Two markers in a paragraph addressed to genuine peers may be fine; one "obviously" in front of the load-bearing inference is the whole failure.

*Illustrative only — the dossier supports no validated before/after examples:* "Obviously you just wire it through the adapter" hides the step. Deleting "obviously" and "just" leaves "you wire it through the adapter", which now visibly begs the question the reader actually has: *which adapter, and wire what through it?*

---

## 4. What people believe vs what the evidence actually says

Every item below was killed on adversarial verification. Each is an **overreach on a real finding** — the underlying datum usually survives; the story built on top of it does not. These are reproduced with their refutation reasoning because a coach that repeats them is repeating folklore with a citation stapled to it.

### 4.1 "Mere possession of the knowledge is enough — informed observers who never tapped were just as overconfident, so knowing the answer is *sufficient* to destroy your model of the audience"

**Verdict: REFUTED ([1-2](https://gwern.net/doc/psychology/cognitive-bias/illusion-of-depth/1990-newton.pdf)).**

**What survives.** The descriptive numbers are real and verified against the primary PDF. Table 3 (p.45): informed observers — people who knew which tune would be tapped but who never tapped and never listened — predicted **50%** audience accuracy (MD = 52, range **2–98**, SD = 25) across **240 songs**, N = 80 observers. Newton's abstract: "Informed observers—people who knew what tune was being tapped but who had never served as tappers or listeners themselves—were also overconfident. They also estimated that fifty percent of listeners would be able to identify the tune." **So authorship/tapping is not NECESSARY for the overconfidence.** That much is supported.

**What does not survive.** The causal upgrade — *knowing the answer is SUFFICIENT, independent of authorship* — is contradicted **inside the same dissertation**. In the experimenter-taps round (procedure, p.38), the experimenter told **both the listeners and the tappers** which tune she would tap, and asked both to estimate what percentage of an audience of 100 would name it. Those listeners therefore (a) possessed the answer, (b) did no tapping, (c) heard the identical stimulus — the exact profile the sufficiency claim says must produce the bias. **They predicted 3%** (Table 2, p.43). Equally-informed non-tapping listeners were *not* overconfident. Possession of the knowledge is therefore not sufficient.

**Note the tension, and do not paper over it.** The dossier's own refutations pull in different directions here: the informed-observer condition is used to argue that mere knowledge suffices (killing the vividness story, §4.3), while the informed-listener condition is used to argue that mere knowledge does *not* suffice (killing this one). Both refutations were adjudicated against the same primary source. **The honest reading is that Newton's conditions do not add up to a single clean mechanistic story, and this is precisely why the mechanism is treated as contested below.** Do not pick the half you like.

### 4.2 "The miscalibration is asymmetric: uninformed people model other uninformed people accurately (~3%, near the true 2.5%), so the expert is the sole locus of error"

**Verdict: REFUTED ([0-3](https://gwern.net/doc/psychology/cognitive-bias/illusion-of-depth/1990-newton.pdf)) — unanimous.**

**What survives.** The quote and the raw figures. Newton p.42: "We note that the listeners themselves recognized that other listeners, focusing on a similarily impoverished stimulus, would be equally unlikely to guess the tapper's tune. Accordingly, they gave a mean estimate of only 3%." Table 2 reports tappers 50% and listeners 3% in the same (experimenter-taps) condition.

**What does not survive, on four independent grounds:**

1. **Cross-condition splice.** The 50% and the 3% come from the *experimenter-taps* round (Table 2), **in which nobody's guesses were ever scored — there is no measured accuracy for that round at all.** The "true 2.5%" comes from a *different* round (Table 1, tappers tapping for listeners). So the rhetorically powerful "3% ≈ the true 2.5%" compares a prediction made in one condition against a hit rate measured in another.
2. **The ground truth is internally inconsistent.** As above: 2/150 (1.3%), 3/120 (2.5%), 3/150 (2.0%) — three different figures in one document. Any claim whose force depends on "3% is remarkably close to 2.5%" is resting on a denominator the source itself reports three ways.
3. **"Uninformed people model other uninformed people accurately" is false in the peer-reviewed literature.** Lau, Geipel, Wu & Keysar (2022), "The extreme illusion of understanding," *J Exp Psychol Gen* 151(11):2957-2962 ([counter-source](https://doi.org/10.1037/xge0001213)): "Though speakers and listeners monitor communication success, they systematically overestimate it." Uninformed **listeners overestimated their own understanding by 41 percentage points.** The audience is *not* a reliable instrument about itself.
4. Consequently the tidy corollary — *the expert is the only broken party, the audience's self-report is trustworthy* — is exactly backwards in its second half.

**What you may still say.** The informed party is a demonstrated, large locus of error (§1) and a legitimate target of intervention. **You may not say** that the uninformed party is calibrated, and you must not treat the listener's *self-reported* understanding as a clean measurement — it isn't one.

### 4.3 "The mechanism is vivid internal representation: the tapper phenomenologically *hears* the full orchestration, which crowds out awareness of the thin signal actually transmitted"

**Verdict: REFUTED ([0-3](https://gwern.net/doc/psychology/cognitive-bias/illusion-of-depth/1990-newton.pdf)) — unanimous.** This is the single most repeated mechanistic story in popular retellings, and it is the least supported.

**What the quote actually is.** Newton's line — "the tapper and observer subjects in this study were so embedded in their own imaginations-so caught up in the richness o f the melodies they were 'hearing'~that they could not recognize how impoverished the same stimulus was from the perspective of the listener" — is **interpretive prose from her Discussion section**. It is a rhetorical gloss, not a tested mediator.

**Why it fails:**

1. **Newton never measured vividness.** No vividness manipulation, no vividness measure, no vividness-to-overconfidence correlation exists anywhere in the data. "Crowding out awareness" has no corresponding attentional or awareness measure in the study.
2. **Her own data cut against it.** Informed observers who *never tapped* — no self-generated performance, no motor imagery of an act they performed — were **equally overconfident (~50%, across 240 songs)**. If performer-generated phenomenological richness were the mechanism, non-performers should have been measurably less biased. They were not.
3. **The peer-reviewed mechanism literature contradicts it.** Birch, Brosseau-Liard, Haddock & Ghrear (2017), "A 'curse of knowledge' in the absence of knowledge? People misattribute fluency when judging how common knowledge is among their peers," *Cognition*, n = 359 ([counter-source](https://doi.org/10.1016/j.cognition.2017.04.015)): **fluency misattribution alone is sufficient to induce a curse of knowledge in the ABSENCE of knowledge.** A vivid-representation-of-the-known-content story cannot explain a curse produced without the knowledge.
4. An alternative framing named in the refutation is **epistemic egocentrism / anchoring-and-insufficient-adjustment** (Epley, Keysar, Van Boven & Gilovich 2004, *JPSP*, [doi:10.1037/0022-3514.87.3.327](https://doi.org/10.1037/0022-3514.87.3.327)) — people *do* adjust away from their own perspective, just insufficiently. This is a candidate, not a settled answer.

**The forbidden sentence.** Do **not** tell a user: *"the expert literally hears the orchestration in their head, which is why they can't hear how thin their signal is."* It is not an established experimental finding ([synthesis F16](https://gwern.net/doc/psychology/cognitive-bias/illusion-of-depth/1990-newton.pdf)). **The defensible version is behavioural and blunt: informed people massively overestimate how well their message lands, and cannot correct it by trying harder.** That is all you get. It is enough.

### 4.4 "Experts are literally unable to act inscrutably — they cannot reason as if they did not know what they know"

**Verdict: REFUTED ([0-3](https://www.cmu.edu/dietrich/sds/docs/loewenstein/CurseknowledgeEconSet.pdf)) — unanimous.**

The seductive quote is real: "Agents are unable to act 'inscrutably'; they cannot ignore their better information when they should." (CLW 1989, p.1244.) It is also the most misused sentence in the paper.

**Why "literally unable" is refuted by its own paper:**

1. **"Literally unable" is the paper's w = 1 hypothesis, which the paper explicitly rejects.** CLW formalize the curse as a *degree* parameter: "If w = 0, an agent is applying the law of iterated expectations correctly. If w = 1, agents who know I1 think that all other agents know I1 too. The parameter w thus measures the degree of curse of knowledge." Then: **"We can strongly reject both the no-bias (w = 0) and pure-bias (w = 1) hypotheses."** Rejecting w = 1 means informed agents **do** partially discount their private information. The finding is **insufficient adjustment, not incapacity**.
2. **A bias that context halves is not a hard-wired inability.** The abstract itself: "market forces reduce the curse by approximately 50 percent but do not eliminate it."
3. **The quote is severed from its own hedge.** It sits in Section V ("Asymmetric Information"), immediately preceded by hedged framing ("Our data and earlier studies ... suggest"). Quoting the assertion without the hedge is a misquote.
4. **Domain mismatch.** The paper is an economics experiment on asymmetric information — informed subjects predicting less-informed subjects' valuations. Extrapolating it into a universal statement about experts explaining things is an unsupported jump.

**What survives, and it is the payload of this whole document.** The conclusion "self-assessment of your own clarity is unreliable, so use external checks" **does not need the incapacity claim and must not be justified by it.** It is fully carried by the confirmed evidence: a ~20x overestimate outside the entire range of predictions (Newton, [confirmed 3-0](https://gwern.net/doc/psychology/cognitive-bias/illusion-of-depth/1990-newton.pdf)), a bias that incentives and outcome feedback fail to reduce and markets only halve (CLW, [confirmed 3-0](https://www.cmu.edu/dietrich/sds/docs/loewenstein/CurseknowledgeEconSet.pdf)). **Say "systematically and persistently miscalibrated". Never say "literally unable".** ([synthesis F17](https://www.cmu.edu/dietrich/sds/docs/loewenstein/CurseknowledgeEconSet.pdf))

### 4.5 "The w parameter: bias quantified 0–1, both endpoints rejected, so even incentivized, experienced traders in real markets show partial knowledge projection"

**Verdict: REFUTED ([0-3](https://www.cmu.edu/dietrich/sds/docs/loewenstein/CurseknowledgeEconSet.pdf)) — unanimous. Partial refutation: the econometric core is verbatim-supported; the conclusion built on it is false.**

**What survives (verbatim in the paper):** the w model as described in §4.4 above; the rejection of both endpoints ("Regressions show that equilibrium prices are between the pure-bias and no-bias predictions... the estimates are extremely precise; standard errors are typically a penny or two. We can strongly reject both the no-bias (w = 0) and pure-bias (w = 1) hypotheses"); and "partial but robust" as a characterization of the market result.

**What does not survive: "experienced traders in real markets."** There were no real markets and no experienced traders. The setting is a **laboratory double-oral-auction asset market**: "informed subjects" endowed with two assets and $50 in cash, trading in 4-minute periods, **nine Wharton students**, shouting bids and offers. The paper's own title is "*An Experimental Analysis*".

**Operational consequence.** Do **not** ship the w-framing as a coaching claim ([synthesis F17](https://www.cmu.edu/dietrich/sds/docs/loewenstein/CurseknowledgeEconSet.pdf)). It is a modelling device from one lab experiment, and its main use in the wild is to lend spurious precision to the incapacity story that §4.4 refutes. If you need the point, make it without the parameter: *the bias is partial, not total, and it is stubborn.*

---

## 5. The mechanism is contested — say so

There is no settled account of *why* the curse happens. A coach that offers one is exceeding the evidence.

| Position | Source |
|---|---|
| Mechanisms are explicitly **not** understood: "Despite its pervasiveness and robustness, we [do not understand the mechanisms]" | Tullis & Feder (2022), "The 'curse of knowledge' when predicting others' knowledge," *Memory & Cognition*, [doi:10.3758/s13421-022-01382-3](https://doi.org/10.3758/s13421-022-01382-3) |
| Estimators fail **not** from over-reliance on their own knowledge but from **lacking diagnostic cues about others** | Tullis (2022), [synthesis F0](https://doi.org/10.3758/s13421-022-01382-3) |
| **Fluency misattribution alone suffices** to induce a curse of knowledge *in the absence of knowledge* (n = 359) | Birch, Brosseau-Liard, Haddock & Ghrear (2017), *Cognition*, [doi:10.1016/j.cognition.2017.04.015](https://doi.org/10.1016/j.cognition.2017.04.015) |
| Anchoring-and-insufficient-adjustment / epistemic egocentrism — people adjust, just not enough | Epley, Keysar, Van Boven & Gilovich (2004), *JPSP*, [doi:10.1037/0022-3514.87.3.327](https://doi.org/10.1037/0022-3514.87.3.327) |
| **Failed replication:** 7 experiments failed to replicate Birch & Bloom's adult false-belief curse | Ryskin & Brown-Schmidt (2014), *PLoS ONE*, [doi:10.1371/journal.pone.0092406](https://doi.org/10.1371/journal.pone.0092406) |

**Coaching consequence.** The *phenomenon* is well enough evidenced to act on. The *explanation* is not. This asymmetry is load-bearing: it means the intervention must target the **output** (get an external check) rather than the **cause** (there is no agreed cause to target, and every "fix the cause" story on offer — visualize the audience's ignorance, remember they can't hear your inner orchestra — is downstream of a refuted mechanism).

---

## 6. Language neutrality

The curse of knowledge is classified as **language-neutral** in the synthesis's language-scope caveat, alongside chunk-relative capacity, grounding, repair infrastructure, audience design, frame-before-details, and contiguity. Nothing in this document is an English-specific artifact: there is no readability formula, no word count, no focal-stress claim, no cleft construction, no English backchannel token here. The markers in §3.1 are the one thing that will not port cleanly — they are English lexical items, and a coach working in another language must find that language's equivalent self-certifying hedges rather than translating this list word for word. (That instruction is an operational note, not a research finding; the dossier contains no cross-linguistic study of self-certifying language.)

Two honest limits on the "language-neutral" label: the studies in this document were run at English-language institutions (Stanford; Chicago MBAs; Wharton students), and **no cross-linguistic replication of the tapping study exists in the evidence base** — indeed no direct replication of any kind was located. The classification rests on the effect being a general property of informed-agent judgment, not on demonstrated cross-linguistic testing. Do not upgrade it to "replicated across languages."

---

## 7. Unverified — do not rely on

The following two claims were extracted from the primary sources but **never adjudicated** in the verification pass (budget). They are quotable only with this label attached, and must not be used to support a coaching rule.

- **[UNVERIFIED] The effect may extend beyond stimulus-poor tapping to ordinary face-to-face conversation.** Newton Study 2 (N = 50 Stanford undergraduates, paired strangers, 10-minute unscripted interaction): subjects were reportedly more confident their partner could read *their* intentions (M = 73%, SD = 15) than that they could read their partner's (M = 53%, SD = 23), t = 6.47, p < .0001. Verbatim: "Thus, subjects showed significantly more confidence in their partners ability to read their preferences than in their own ability to read their partners (t= 6.47, jk.0001)." ([unverified — not adjudicated](https://gwern.net/doc/psychology/cognitive-bias/illusion-of-depth/1990-newton.pdf)) *Note the tension with §4.2: this framing again casts the uninformed party as calibrated, which the peer-reviewed Lau et al. (2022) evidence contradicts.*
- **[UNVERIFIED] Market experience reduces but does not remove the bias, slowly.** Of the 131 judgment changes that moved directionally, 83 (63%) decreased bias and 48 (37%) increased it (different from 50% at the 1% level); 54% of judgments did not move at all. Verbatim: "In the remaining 131 cases, 83 (63 percent) indicated a decrease in bias and 48 (37 percent) indicated an increase in bias. (These fractions are different from 50 percent at the 1 percent level.) Market experience does reduce bias." ([unverified — not adjudicated](https://www.cmu.edu/dietrich/sds/docs/loewenstein/CurseknowledgeEconSet.pdf))

---

## What this does NOT license

- **Do not say experts are "literally unable" to simulate an ignorant audience.** The paper that is always cited for this explicitly rejects w = 1. The finding is insufficient adjustment, not incapacity. (§4.4)
- **Do not say "motivation is irrelevant" or "caring doesn't help."** What was tested and failed was *financial incentives for accuracy* and *outcome feedback*, in two small conditions (n = 19, n = 13). Report **"persists under incentives and outcome feedback"** and stop there. (§2.1)
- **Do not tell the vivid-representation story.** "The expert hears the full orchestration in their head" is Newton's Discussion prose, was never measured, is contradicted by her own informed-observer condition, and is undercut by Birch et al. (2017), where fluency misattribution produced a curse *without* the knowledge. (§4.3)
- **Do not claim the audience is calibrated about itself.** The "listeners predicted 3%, close to the true 2.5%" story splices two different conditions, leans on a denominator the dissertation reports three different ways, and is contradicted by Lau et al. (2022), where listeners overestimated their *own* understanding by 41 percentage points. Both parties are miscalibrated. (§4.2)
- **Do not claim "knowing the answer is sufficient" to produce the bias.** Newton's own experimenter-taps listeners knew the tune, did no tapping, and predicted 3%. (§4.1)
- **Do not cite the w parameter, and do not say "experienced traders in real markets."** Nine Wharton students in a 4-minute lab double-oral auction. (§4.5)
- **Do not cite the dissertation under the wrong title, and do not present it as peer-reviewed or replicated.** It is "The rocky road from actions to intentions" (Stanford, 1990), unpublished, never replicated. The "curse of knowledge" label was pinned on it by *Made to Stick*, not by Newton. (§1.1)
- **Do not build an argument on the precision of "2.5%."** The source reports 1.3%, 2.0% and 2.5% in three different places. Direction: robust. Denominator: not. (§1.1)
- **Do not present any mechanism as established.** Tullis & Feder (2022) state outright that the mechanisms are not understood; Ryskin & Brown-Schmidt (2014) failed to replicate the adult false-belief curse across 7 experiments. Target the output, not the cause. (§5)
- **Do not treat the §3.1 markers as evidence-based, and never turn them into a score.** No study in the evidence base validates them, measures them, or shows that removing them improves comprehension. They are a flagging heuristic; the judgment stays with the human. (§3.1)
- **Do not let an LLM's own read of a draft stand in for an external check.** The rule is that clarity is measured on the receiver. A model that has already read everything is not a naive receiver. (§3)
