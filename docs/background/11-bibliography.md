# Bibliography

> **What this is.** The complete source list behind the `easy_speak` knowledge base — 74 URLs, grouped by source quality and, within the primary tier, by topic area, each with its adjudicated verdicts and a note on what it may and may not be cited for.
> **Evidence base.** 209 distinct claims went through 3-vote adversarial verification against these 74 sources: **80 CONFIRMED**, **50 REFUTED**, **79 UNVERIFIED** (extracted but never adjudicated). Every one of the 74 URLs carries at least one adjudicated claim.
> **Load this when.** The coaching task involves citing a source, re-sourcing a rule, checking whether a specific number is safe to quote, or deciding whether a famous finding survives contact with its primary literature.

---

## Citation hygiene — read this before citing anything below

These are errors that downstream readers reliably re-introduce. Each one was found during verification against the actual documents.

**1. `plainlanguage.gov/guidelines/` is a dead citation.**
It 301-redirects to a digital.gov landing page, and **the redirect target does not contain the quoted text**. Anything sourced to that URL is unverifiable at that URL. Cite instead the archived Federal Plain Language Guidelines PDF (the wid.org copy, entry **P-53** below) or `https://digital.gov/guides/plain-language/principles`. Four claims keyed to the dead URL failed verification on exactly this basis — the dossier notes this is "likely a citation problem, not necessarily a falsity problem," which is why re-sourcing matters rather than deletion.

**2. Two of the hosted PDFs are image-only scans and cannot be quote-checked.**
The CMU-hosted Clark & Brennan 1991 PDF (**P-07**) and the Stanford-hosted Bell 1984 PDF (**P-16**) have no text layer. No downstream verifier can confirm a quotation against them. For Clark & Brennan, prefer the Stanford author copy:
`https://web.stanford.edu/~clark/1990s/Clark,%20H.H.%20_%20Brennan,%20S.E.%20_Grounding%20in%20communication_%201991.pdf`
(The dossier records no text-layer replacement for Bell 1984; its claims were read from rendered page images.)

**3. Newton (1990) is mis-titled and mis-attributed almost everywhere.**
Its real title is **"The rocky road from actions to intentions"** — *not* the widely-cited "Overconfidence in the communication of intent." It is an **unpublished Stanford doctoral dissertation, never peer-reviewed, with no located direct replication**. The label **"curse of knowledge" was attached to it by Heath & Heath's *Made to Stick* (2007)** — not by Newton, and not by Camerer, Loewenstein & Weber. Cite the headline behavioural result; do not inherit the popular framing.

**4. The Bransford & Johnson topic manipulation is in the 1972 paper, not the 1973 chapter.**
The topic-before / topic-after / no-topic experiment is reported in **Bransford & Johnson (1972), *Journal of Verbal Learning and Verbal Behavior* 11:717–726** (**P-40**). Clark & Haviland's own secondary reference points at a 1973 chapter; the numbers live in the 1972 JVLVB paper.

**5. Hedges travel with the rule (Federal Plain Language Guidelines).**
The FPLG's most-quoted rules are routinely stripped of the qualifiers that sit next to them in the document. Verified against the archived PDF (**P-53**):
- The 150-word paragraph figure is **not asserted in the FPLG's own voice** — it is attributed to third parties ("Writing experts recommend"), and the section's source list cites only two legal-writing style manuals, no empirical readability study (CONFIRMED-G10, 3-0).
- The paragraph rule ships with an explicit exception that is almost always dropped: **"There is nothing wrong with an occasional one-sentence paragraph"** — which is *below* the document's own "three to eight sentences" band. Quoting the band as a floor is a misquote (CONFIRMED-G11, 3-0).
- The FPLG **does not describe itself as binding**. Its introduction calls itself "advice"; the strings "Plain Writing Act," "Act of 2010," "binding," and "mandatory" occur **zero times in all 118 pages** (CONFIRMED-G13, 3-0).
- The FPLG **does not say "write to an 8th-grade level" is a myth.** The myth it names is the *universal dumbing-down* claim. It makes the 8th-grade target strictly **audience-conditional** — required when the audience genuinely is 8th graders, wrong when it is not (CONFIRMED-G14, 3-0). This refines the coarser statement in CONFIRMED-R26 (3-0), which was adjudicated against the dead URL.

---

## How to read the entries

| Field | Meaning |
| --- | --- |
| **Tier** | The dossier's own source-quality tag: `primary` / `secondary` / `unreliable`. There is **no `blog` tier** — the dossier contains no source tagged as a blog. |
| **Good for** | What the source may be cited for, with the claim ID and vote. `3-0` = unanimous; `2-1` = split. |
| **Do not cite for** | A REFUTED claim attached to this source. **REFUTED is almost never "wholly false"** — it is typically an *overreach* on a real finding. The note says what survives. |
| **UNVERIFIED-ONLY** | Every adjudicated claim keyed to this source is UNVERIFIED. Do not rely on it; see the dedicated section below. |
| **EN** | The source, or the finding drawn from it, is an **English-specific artifact**. Do not generalize across languages. |

Area grouping follows the dossier's own topic files (`curse-of-knowledge.md`, `foundations.md`, `grounding-dialogue.md`, `measuring-comprehension.md`, `structure-ordering.md`, `explaining.md`, `multimedia-presentations.md`, `plain-language-writing.md`, `myths.md`). The dossier's `measuring-comprehension.md` cluster is folded into **Grounding & pragmatics**, because Clark & Brennan's positive-evidence requirement is its theoretical anchor; the brief's eight areas have no separate slot for it.

---

# Primary sources (69)

## Curse of knowledge (2)

**P-01 — Newton, E. (1990), *The Rocky Road from Actions to Intentions*, Stanford doctoral dissertation.**
https://gwern.net/doc/psychology/cognitive-bias/illusion-of-depth/1990-newton.pdf
*Good for:* the canonical tapping demonstration — N = 40 tappers, 40 listeners, 120 songs; tappers predicted a mean **50%** listener success rate (range 10–95%), actual identification was **3 hits in 120 tries = 2.5%**, an overestimate falling entirely outside the range of every individual prediction (CONFIRMED-R1, 3-0).
*Do not cite for:* the three mechanistic elaborations popularly attached to it — that mere possession of the tune is *sufficient* to produce the bias (REFUTED-R33, 1-2; the dissertation's own Table 2 shows equally-informed non-tapping listeners predicted only 3%); that uninformed people model other uninformed people *accurately* (REFUTED-R34, 0-3); that the mechanism is a vivid internal representation crowding out awareness of the thin signal (REFUTED-R35, 0-3). **Keep the headline; drop the story.** See citation-hygiene note 3 for the title/attribution problem.

**P-02 — Camerer, Loewenstein & Weber (1989), "The Curse of Knowledge in Economic Settings: An Experimental Analysis," *J. Political Economy* 97(5).**
https://www.cmu.edu/dietrich/sds/docs/loewenstein/CurseknowledgeEconSet.pdf
*Good for:* the curse is a **cognitive, not motivational** failure — better-informed agents cannot ignore private information even when it is financially against their interest (CONFIRMED-R2, 2-1); and **outcome feedback and financial incentives do not reduce it** — only market forces did, and only by roughly 50%, never eliminating it (CONFIRMED-R3, 3-0).
*Do not cite for:* the `w`-parameter framing with both endpoints rejected in market prices (REFUTED-R36, 0-3); or the claim that experts are **"literally unable"** to act inscrutably / reason as if they did not know (REFUTED-R37, 0-3). The defensible statement is that they are *systematically and persistently miscalibrated*, and that markets/feedback/incentives at best halve the bias.

## Memory & load (4)

**P-03 — Cowan, N. (2001), "The Magical Number 4 in Short-Term Memory," *Behavioral and Brain Sciences* 24:87–114.**
https://www.cambridge.org/core/services/aop-cambridge-core/content/view/44023F1147D4A1D44BDC0AD226838496/S0140525X01003922a.pdf/the-magical-number-4-in-short-term-memory-a-reconsideration-of-mental-storage-capacity.pdf
*Good for:* pure short-term storage is **about four chunks (three to five), not Miller's seven** (CONFIRMED-R4, 3-0); the ~4 figure is observable **only under four stated boundary conditions** where rehearsal, recoding and LTM grouping are blocked (CONFIRMED-R5, 3-0); and Miller himself treated "seven" as a coincidence, his substantive contribution being **chunking** (CONFIRMED-R6, 3-0).

**P-04 — Cowan, Morey & Chen, "George Miller's Magical Number of Immediate Memory in Retrospect: Obsolete and Nonmagical" (PMC, open access).**
https://pmc.ncbi.nlm.nih.gov/articles/PMC4486516/
*Good for:* the limit is over **chunks grounded in the receiver's prior knowledge, not raw surface items** — so the same message costs a novice many chunks and an expert one (CONFIRMED-R7, 3-0). This is the mechanism by which jargon inflates load.
*Do not cite for:* "the usable working-memory budget is ~3–4 units" as a design constant (REFUTED-R38, 1-2), or "in a live audience with no rehearsal time the limit is ~3 items" (REFUTED-R39, 0-3). **Never derive "never more than 4 bullets" from this source.**

**P-05 — de Jong, T. (2010), "Cognitive load theory, educational research, and instructional design: some food for thought," *Instructional Science* 38:105–134.**
https://link.springer.com/article/10.1007/s11251-009-9110-0
*Good for:* CLT's intrinsic/extraneous/germane split is **not cleanly separable** and the extraneous-vs-germane definition has a "quite tautological character" (CONFIRMED-R8, 3-0); load is frequently **inferred backwards from post-test scores** rather than measured (CONFIRMED-R9, 3-0); the dominant Paas one-item mental-effort scale is **non-standardized and not comparable across studies** (CONFIRMED-R10, 3-0). This is the source that makes "reduce extraneous load" unusable as an audience-independent rule.

**P-06 — Kintsch, W. (1988), "The Role of Knowledge in Discourse Comprehension: A Construction-Integration Model," *Psychological Review* 95(2):163–182.**
https://condor.depaul.edu/dallbrit/extra/hon207/readings/kintsch-1988-construction-integration.pdf
*Good for:* comprehension runs in **cycles with a small short-term buffer**, so redundant or irrelevant wording is not cost-free — it lengthens the text and raises the chance a critical earlier proposition is no longer in active memory when needed (CONFIRMED-R22, 3-0). Note this is a **simulation result, not an experiment**, and Kintsch himself refuses the blanket "redundancy is bad" — overspecification "may be quite harmless, or may even facilitate problem solving."
*Do not cite for:* "comprehension is not primarily expectation-driven; initial processing is strictly bottom-up" (REFUTED-R45, 0-3); or "embedding formal content in a concrete familiar context makes it dramatically easier" (REFUTED-R46, 0-3).

## Grounding & pragmatics (17)

**P-07 — Clark, H. H. & Brennan, S. E. (1991), "Grounding in Communication."** **[IMAGE-ONLY SCAN — cannot be quote-checked; see hygiene note 2]**
https://www.cs.cmu.edu/~illah/CLASSDOCS/Clark91.pdf
*Good for:* the **grounding criterion** — understanding is pursued to a mutually-believed threshold "sufficient for current purposes," never to perfection, so a speech act is not accomplished by uttering the sentence (CONFIRMED-R13, 3-0); speakers **do not infer understanding from the absence of confusion** but actively seek positive evidence, of which there are three forms — acknowledgments, initiation of a relevant next turn, continued attention (CONFIRMED-R14, 3-0); the **principle of least collaborative effort** replaces the speaker-centric principle of least effort (CONFIRMED-R15, 2-1).
*Do not cite for:* the "installments" claim (REFUTED-R41, 1-2) or the eight-medium-constraints enumeration (REFUTED-R42, 1-2).
**EN:** the backchannel tokens used to illustrate acknowledgments ("uh huh," "yeah") are English-specific. The *mechanism* is not.

**P-08 — Clark, H. H. & Wilkes-Gibbs, D. (1986), "Referring as a Collaborative Process," *Cognition* 22:1–39** (author's PDF, Stanford).
http://www.web.stanford.edu/~clark/1980s/Clark,%20H.H.%20_%20Wilkes-Gibbs,%20D.%20_Referring%20as%20a%20collaborative%20process_%201986.pdf
*Good for:* the tangram matching task — 8 pairs, 12 figures, 6 trials, 9,792 words transcribed: directors used **41 words per figure on trial 1 and 8 by trial 6** (F(1,35)=44.31, p<.001); turns per figure fell **3.7 → ~1** (F(1,35)=79.59, p<.001) (CONFIRMED-R16, 3-0). Also the **principle of mutual responsibility** (CONFIRMED-R17, 3-0); the falsifiable predictions of least collaborative effort (CONFIRMED-R18, 2-1); and the finding that **listeners are under systematic social pressure to feign understanding** — they risk offending the speaker, risk revealing their own incompetence, and want to minimize collaborative effort, so coordinating signals appear "however insincere they may be" (CONFIRMED-R19, 3-0).
*Scope:* the paper explicitly excludes novels, letters, broadcasts, sermons and large lectures — contexts where the addressee cannot repair.

**P-09 — Dingemanse, M., Torreira, F. & Enfield, N. J. (2013), "Is 'Huh?' a Universal Word?", *PLoS ONE* 8(11):e78273.**
https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0078273
*Good for:* **other-initiated repair is universal conversational infrastructure** — repair sequences are documented in every spoken language investigated so far, and no language appears to lack an interjection for open repair initiation (CONFIRMED-R23, 3-0). Evidence base: 10 languages studied in depth from field recordings across 5 continents (196 corpus tokens) plus 21 from published sources. **This is the language-neutrality warrant for "signal trouble → speaker reformulates."**
*Do not cite for:* the convergent-cultural-evolution *explanation* of the cross-linguistic similarity (REFUTED-R47, 1-2). Also note: universality of the *mechanism* does not entail cross-cultural uniformity in *willingness* to initiate repair.

**P-10 — Grice, H. P. (1975), "Logic and Conversation," in *Syntax and Semantics 3: Speech Acts*, pp. 41–58** (excerpt pp. 45–47).
http://www.sfu.ca/~jeffpell/Cogs300/GriceLogicConvers75.pdf
*Good for:* the Cooperative Principle is a principle of **rational cooperation toward the accepted purpose of a talk exchange — not a set of writing or style rules** (CONFIRMED-G31, 3-0); and Grice **explicitly excludes politeness/style maxims** from the conversational maxims and flags his own scheme as too narrow (CONFIRMED-G48, 3-0). Cite this whenever someone tries to turn "be brief" into a Gricean mandate.

**P-11 — Grice, H. P. (1975), "Logic and Conversation," p. 49** (full-chapter scan, UCL Pragmatic Theory course licence). *Duplicate work, different hosting; used for a different claim.*
https://lawandlogic.org/wp-content/uploads/2018/07/grice1975logic-and-conversation.pdf
*Do not cite for:* the four-ways-of-failing-a-maxim taxonomy as a communication rule (violation / opting out / clash / flouting) (REFUTED-G61, 1-2).

**P-12 — Keenan (Ochs), E. (1976), "The universality of conversational postulates," *Language in Society*.**
https://www.cambridge.org/core/journals/language-in-society/article/abs/universality-of-conversational-postulates/4E0D5F41B8D53C28FADFB5A0E04BD534
*Good for:* the **universality of the Gricean maxims is contested by primary ethnographic fieldwork** — Keenan's Malagasy village data show the maxims are not cross-culturally universal (CONFIRMED-G32, 2-1). The empirical basis is a two-community contrast (US English vs Malagasy), so it is a **falsifier of universality, not a survey of all cultures**.

**P-13 — Wierzbicka, A. (1991), *Cross-Cultural Pragmatics: The Semantics of Human Interaction*, Ch. 1 §11** (publisher preview PDF).
https://api.pageplace.de/preview/DT0400.9783112329764_A41028527/preview-9783112329764_A41028527.pdf
*Good for:* the **anglocentrism charge stated as a central thesis**, not an aside — the supposedly universal maxims encode Anglo conversational norms (CONFIRMED-G33, 3-0). This is the load-bearing source for the skill's language-neutrality discipline.

**P-14 — Leiden University repository — critique of Western-centrism in pragmatics (Grice's maxims and Brown & Levinson politeness across cultures).** **[UNVERIFIED-ONLY]**
https://scholarlypublications.universiteitleiden.nl/access/item%3A2979130/view
*Status:* all five adjudicated claims keyed to this source are UNVERIFIED (R81, R82, R128, R129, R130). Do not rely on it. It is the natural place to look for the Manner-maxim and politeness-indirectness critiques, but nothing here has been adjudicated.

**P-15 — Horton, W. S. & Keysar, B. (1996), "When do speakers take into account common ground?", *Cognition* 59(1):91–117** (abstract via Europe PMC).
https://europepmc.org/article/MED/8857472
*Do not cite for:* "audience design is not part of initial utterance planning and degrades under time pressure" as a settled result (REFUTED-G62, 0-3). The source remains the standard citation for **egocentric anchoring in production** — treat the strong form as unestablished here.

**P-16 — Bell, A. (1984), "Language Style as Audience Design," *Language in Society* 13(2):145–204.** **[IMAGE-ONLY SCAN; claims read from rendered page images]**
https://web.stanford.edu/~eckert/PDF/bell1984.pdf
*Good for:* the **implicational, distance-graded audience-role hierarchy** defined by three binary attributes (known / ratified / addressed): addressee > auditor > overhearer > eavesdropper (CONFIRMED-R24, 3-0); and the New Zealand newscaster natural experiment — the **same newscasters reading the same news from the same studios** shifted intervocalic /t/-voicing between a higher-status and a lower-status station audience (CONFIRMED-R25, 2-1).
*Do not cite for:* the core Audience Design thesis in its strong form — that intraspeaker style variation is *primarily* a response to the audience (REFUTED-R48, 1-2).
**EN:** the /t/-voicing variable is English/New Zealand-specific. n = 4 newscasters, 1974 data, no inferential statistics on the key figure. "Only the audiences differ" is **Bell's inference**, not an independently validated fact.

**P-17 — Keysar, Barr, Balin & Brauner (2000), "Taking Perspective in Conversation: The Role of Mutual Knowledge in Comprehension," *Psychological Science* 11(1):32–38.**
https://thegricean.github.io/xprag-ling247/readings/keysar2000.pdf
*Do not cite for:* the strong claim that egocentric anchoring is measurable in listeners in real time via eye-tracking, as established (REFUTED-G63, 0-3).

### Checking understanding (adjudicated in `measuring-comprehension.md`)

**P-18 — Bisra, Liu, Nesbit, Salimi & Winne (2018), "Inducing Self-Explanation: a Meta-Analysis," *Educational Psychology Review* 30(3):703–725.**
https://gwern.net/doc/psychology/spaced-repetition/2018-bisra.pdf
*Good for:* **the strongest single quantitative warrant for "make them explain it back"** — prompting learners to self-explain beats not prompting, pooled **Hedges g = 0.55, 95% CI [0.45, 0.65]**, 69 effect sizes from 64 reports, N = 5,917, random-effects; no moderator killed it (CONFIRMED-G20, 2-1).
*Do not cite for:* the ranking of check types — that **metacognitive** prompts ("explain your own understanding") are the weakest at g = 0.19 (n.s., k = 3) while **conceptualize** prompts ("explain the actual concept") reach g = 0.87 (k = 13) (REFUTED-G55, 1-2). Directionally interesting, not established here.

**P-19 — Kemp, Floyd, McCord-Duncan & Lang (2008), "Patients Prefer the Method of 'Tell Back-Collaborative Inquiry' to Assess Understanding of Medical Information," *J Am Board Fam Med* 21(1):24–30.**
https://www.jabfm.org/content/21/1/24
*Good for:* **the phrasing of the check matters, and closed-ended checks are the ones people neither prefer nor find effective.** In a 100-adult video-vignette study, a collaborative tell-back request was significantly preferred over both a directive tell-back and a Yes/No check ("Do you understand? / Any questions?"), t = 4.71, P ≤ .001 (CONFIRMED-G21, 2-1). The authors' stated mechanism: patients "may not understand the situation well enough to formulate a question."

**P-20 — Rozenblit, L. & Keil, F. (2002), "The misunderstood limits of folk science: an illusion of explanatory depth," *Cognitive Science* 26(5):521–562.**
https://cogdevlab.yale.edu/sites/default/files/files/rozenblit%20&%20keil%20%202002.pdf
*Do not cite for:* "people cannot self-assess comprehension" in its strong, unrestricted form (REFUTED-G53, 0-3). The illusion-of-explanatory-depth phenomenon is the natural mechanistic story for why "Do you understand?" is invalid — but at 0-3 the claim as written did not survive. Re-source before asserting.

**P-21 — Schillinger, D. et al. (2003), "Closing the loop: physician communication with diabetic patients who have low health literacy," *Arch Intern Med* 163(1):83–90.**
https://pubmed.ncbi.nlm.nih.gov/12523921/
*Do not cite for:* the paired claim that comprehension-checking is both **rare in practice** (physicians assessed recall for only 12% of new concepts, 15 of 124) **and one of the strongest predictors of outcome** (adjusted OR 15.15 for good glycemic control) (REFUTED-G54, 0-3). The numbers are striking and the direction is the one the skill wants — which is exactly why they must be re-verified before use.

**P-22 — Fiorella, L. & Mayer, R. E. (2013), "The relative benefits of learning by teaching and teaching expectancy," *Contemporary Educational Psychology* 38(4):281–288.**
https://www.sciencedirect.com/science/article/abs/pii/S0361476X13000209
*Do not cite for:* "the protégé effect is carried by the act of explaining, not the intention to explain" — preparing to teach helps immediately (d = 0.59) but evaporates after a week (d = 0.24, n.s.), while actually explaining holds (d = 0.82 immediate, d = 0.79 delayed) (REFUTED-G56, 0-3).

**P-23 — Talevski, Wong Shee, Rasmussen, Kemp & Beauchamp (2020), "Teach-back: A systematic review of implementation and impacts," *PLoS ONE* 15(4):e0231350.**
https://journals.plos.org/plosone/article?id=10.1371%2Fjournal.pone.0231350
*Do not cite for:* a **pooled effect size for teach-back — there isn't one.** The review found teach-back effective in 19 of 20 studies (9 RCTs), but reviewers explicitly **could not meta-analyse**: outcome heterogeneity made pooling impossible (REFUTED-G57, 0-3). Cite teach-back's evidence base as *narrative*, never as meta-analytic.

## Comprehension & ordering (6)

**P-24 — Clark, H. H. & Haviland, S. E. (1977), "Comprehension and the Given-New Contract"** (author's PDF, Stanford).
http://www.web.stanford.edu/~clark/1970s/Clark,%20H.H.%20_%20Haviland,%20S.E.%20_Comprehension%20and%20the%20given-new%20contract_%201977.pdf
*Good for:* the **given-before-new ordering argument** — when new precedes given, the listener must hold the new material "in abeyance" while searching for an antecedent, increasing memory load (CONFIRMED-R20, 2-1); and the **"negligent violation"** result — failing to supply the topic up front destroys comprehension of otherwise plain, well-formed sentences, because without a topic the reader cannot compute the intended antecedents for *any* sentence (CONFIRMED-R21, 3-0).
*Do not cite for:* the "maxim of antecedence" formalization (REFUTED-R43, 1-2); or the 140–180 ms bridging-inference cost as a replicated ordering effect (REFUTED-R44, 1-2 — and note those milliseconds measure **bridging**, not ordering).
*Critical:* **no experiment in the chapter manipulates given/new order.** Write "Clark & Haviland argue," not "demonstrated."
**EN:** end-of-sentence focal stress, cleft/pseudocleft/passive information-packaging, and the definite-NP-first tendency are **English-specific** — the authors scope them to English themselves. The 3-step processing argument is language-general; the surface evidence is not.

**P-25 — Bransford, J. D. & Johnson, M. K. (1972), "Contextual prerequisites for understanding," *Journal of Verbal Learning and Verbal Behavior* 11:717–726** (Tables 2–3, p. 723).
https://memlab.yale.edu/sites/default/files/files/1972_Bransford_Johnson_JVLVB.pdf
*Good for:* the exact "washing clothes" numbers — 52 students; **No Topic (n=17): comprehension 2.29, recall 2.82 of 18 idea units; Topic After (n=17): 2.12 / 2.65; Topic Before (n=18): 4.50 / 5.83.** The manipulation was **one sentence of topic** (CONFIRMED-G28, 3-0). This is the frame-before-details warrant.
*Do not cite for:* the felt-clarity / actual-retention dissociation from Experiment IV ("making and flying a kite," 31 Ss), where topic-after raised *subjective* comprehension to near topic-before levels while leaving recall unchanged (REFUTED-G69, 0-3). Directionally the most useful result in the paper for a coaching skill — and not established here.
*Generalization ceiling:* the passages were deliberately engineered referent-free "bizarre texts"; the magnitude does not transfer to ordinary well-referenced prose. See hygiene note 4.

**P-26 — Kieras, D. E. (1980), "Abstracting Main Ideas from Technical Prose: A Preliminary Study of Six Passages," Technical Report No. 5 (DTIC ADA089910).**
https://apps.dtic.mil/sti/tr/pdf/ADA089910.pdf
*Good for:* **the frame-before positive result and its moderator.** Passages of the *generalization* type (general statement then specific examples) benefited strongly from an explicit first-sentence main idea — **but only when the content was unfamiliar** (timekeeping 52.1s vs 81.3s, t(30)=2.437, p<.05; instruments 65.6s vs 89.9s, t(30)=2.579, p<.05). For the **familiar** passage the benefit vanished (50.9s vs 57.4s, n.s.) (CONFIRMED-G27, 3-0).
*Do not cite for:* **the BLUF-specific negative result** — Kieras tested exactly the BLUF manipulation (conclusion stated in the first sentence vs never stated) and found **no reading-time benefit** (transportation 53.9s vs 55.4s, n.s.) (REFUTED-G60, 0-3). This is the single most load-bearing "do not overreach" citation for anyone who wants to sell BLUF as evidence-based; at 0-3 it did not survive as written, so **neither the pro-BLUF nor the anti-BLUF strong claim is available from this source.**

**P-27 — Luiten, Ames & Ackerson (1979/1980), "The Advance Organizer: A Review of Research Using Glass's Technique of Meta-Analysis" (ERIC ED171803; AERJ 17(2):211–218).**
https://files.eric.ed.gov/fulltext/ED171803.pdf
*Good for:* **the advance-organizer evidence is real but small — and it is not evidence for BLUF.** Meta-analysis of 135 published and unpublished studies (1960–1979): 110 learning effect sizes, mean **ES = .21 (SE .04)**; 50 retention effect sizes, .19 / .20 / .23 / .30 / .38 at increasing delays. The authors' own gloss: the average organizer subject performed better than 58% of controls (CONFIRMED-G29, 3-0).

**P-28 — Ameseder, Devetak & Skubic (2025), "Incidental Learning From Science Journalism: The Effects of a Narrative Writing Style...", *CEPS Journal*.**
https://www.cepsj.si/index.php/cepsj/article/view/1899
*Good for:* **the inverted pyramid does not win on comprehension.** With 461 Austrian adult non-experts, science-journalism articles written as **chronological narratives produced significantly higher comprehension and significantly lower cognitive load** than the same content in inverted-pyramid form. The inverted pyramid's one advantage was **early situational interest** (CONFIRMED-G30, 2-1). This is the direct counterweight to conclusion-first dogma.

**P-29 — Schneider, Beege, Nebel & Rey (2018), "A meta-analysis of how signaling affects learning with media," *Educational Research Review* 23:1–24** (DOI form). *Same work as P-36; the dossier keyed different claims to each URL.*
https://doi.org/10.1016/j.edurev.2017.11.001
*Good for:* **what is robustly supported is signaling (marking structure), not ordering by conclusion.** 103 studies, N = 12,201: cues highlighting the organization of relevant information improve **retention g+ = 0.53 [0.42, 0.64]** and **transfer g+ = 0.33 [0.22, 0.43]**, and significantly reduce cognitive load. **Prior knowledge was not a moderator** (CONFIRMED-G47, 3-0).

## Analogy & explanation (6)

**P-30 — Gentner, D. (1983), "Structure-Mapping: A Theoretical Framework for Analogy," *Cognitive Science* 7(2):155–170** (author-hosted PDF, Northwestern).
https://groups.psych.northwestern.edu/gentner/papers/Gentner83.2b.pdf
*Good for:* an analogy works by mapping **relations** between objects and deliberately **discarding the objects' surface attributes**. Gentner's mapping rules are ordered: (1) discard attributes of objects, (2) preserve relations between objects, (3) prefer systems of relations (CONFIRMED-G22, 3-0). Operational: base and target must share **causal/structural relations** — what does what to what — not looks, size, colour or domain feel.

**P-31 — Gentner, D. (1983), same paper** (scanned PDF of the published article). *Duplicate work, different hosting; a different claim was keyed here.*
http://matt.colorado.edu/teaching/highcog/readings/g83.pdf
*Good for:* **the named failure mode** — a comparison with strong *surface* overlap but no *relational* overlap is a **"mere appearance match"**: it feels apt and is memorable, but its explanatory power is "sharply limited" (CONFIRMED-G23, 3-0). This yields the falsifiable test: strip the analogy to its relational skeleton (X causes Y, which constrains Z); if nothing survives the strip, it is decoration, not explanation.

**P-32 — Gick, M. L. & Holyoak, K. J. (1983), "Schema Induction and Analogical Transfer," *Cognitive Psychology* 15:1–38** (Michigan Deep Blue PDF).
https://deepblue.lib.umich.edu/bitstream/handle/2027.42/25331/0000776.pdf
*Good for:* **spontaneous analogical transfer is near-catastrophically bad** — ~75% solved Duncker's radiation problem when **given a hint** to use the fortress/army story; without a hint only ~30% did (baseline with no analog ~10%). So of those who could have applied the analogy, only about a third noticed it unprompted (CONFIRMED-G24, 3-0). **An analogy left implicit is mostly wasted — you must explicitly signal the mapping.** Also: **one example plus an explicit statement of the principle does not reliably produce transferable understanding; two analogous examples do** (CONFIRMED-G25, 3-0). Summarization instructions, a verbal statement of the principle, and a diagram layered on a *single* analog all failed.

**P-33 — Harp, S. F. & Mayer, R. E. (1998), "How seductive details do their damage," *Journal of Educational Psychology* 90(3):414–434** (APA abstract).
https://doi.org/10.1037/0022-0663.90.3.414
*Good for:* **seductive details actively hurt learning — they are not neutral padding.** Across 4 experiments (357 undergraduates, lightning-formation text), readers given seductive details recalled fewer main ideas and generated fewer transfer solutions. Critically for anyone tempted to "keep the fun bit but flag the important part": **highlighting the main ideas, stating learning objectives, and signaling all failed to rescue the effect** (CONFIRMED-G26, 2-1).

**P-34 — Fyfe, McNeil, Son & Goldstone (2014), "Concreteness Fading in Mathematics and Science Instruction: A Systematic Review," *Educational Psychology Review* 26(1):9–25** (ERIC record).
https://eric.ed.gov/?id=EJ1036777
*Do not cite for:* the concreteness-fading sequence recommendation — start concrete, then explicitly and gradually fade to the abstract (REFUTED-G58, 0-3). The concrete-vs-abstract framing as a false dichotomy is appealing and the source is real; the claim as written did not survive.

**P-35 — Bullock, Colon Amill, Shulman & Dixon (2019), "Jargon as a barrier to effective science communication: Evidence from metacognition," *Public Understanding of Science* 28(7):845–853** (author-hosted PDF, Ohio State).
https://comm.osu.edu/sites/comm.osu.edu/files/PUS%202019-%20Bullock%20et%20al..pdf
*Do not cite for:* **"defining jargon does not rescue it."** In a 2×2 (jargon × definitions) experiment (N = 650, U.S. general-population panel), jargon significantly depressed processing fluency (M = 4.57 vs 5.27, η² = .11), with **no main effect of providing definitions and no interaction** — the damage is metacognitive, not comprehension-based (REFUTED-G59, 1-2). This is the most counterintuitive and most useful claim in the explaining cluster, and it is **one vote short**. Re-verify before the skill asserts it.

## Multimedia (8)

**P-36 — Ginns, P. (2006), "Integrating information: A meta-analysis of the spatial contiguity and temporal contiguity effects," *Learning and Instruction* 16(6):511–525.**
https://www.sciencedirect.com/science/article/abs/pii/S0959475206000806
*Good for:* **50 independent effects, 2,375 students, weighted mean d = 0.85, 95% CI [0.68, 1.02]** for integrating related information in space or time (CONFIRMED-R11, 3-0) — the effect-size warrant for "put the label next to the thing it labels." And **the benefit is conditional**: moderated by element interactivity, so contiguity discipline pays off precisely where content is complex and interdependent; for simple content, separation is comparatively inconsequential (CONFIRMED-R12, 3-0).
*Do not cite for:* the extraneous-cognitive-load **mechanism** (REFUTED-R40, 1-2); or the pooled d = 0.85 as a stable transferable constant (REFUTED-G68, 1-2 — heterogeneity is severe and significant, **Q = 117.77, df = 49, p < .001**).

**P-37 — Mayer & Fiorella, "Principles for Reducing Extraneous Processing in Multimedia Learning" (Cambridge Handbook of Multimedia Learning, ch. 12).**
https://edtechuvic.ca/wp-content/uploads/sites/11/2022/09/principles-for-reducing-extraneous-processing-in-multimedia-learning-coherence-signaling-redundancy-spatial-contiguity-and-temporal-contiguity-principles.pdf
*Do not cite for:* **the box-score effect sizes.** These are the single most-quoted numbers in slide-design advice and **none of them survived verification**: coherence 23/23 tests, median d = 0.86 (REFUTED-R58, 0-3); redundancy 16/16, d = 0.86 (REFUTED-R59, 1-2); spatial contiguity 22/22, d = 1.10 and temporal contiguity 9/9, d = 1.22 (REFUTED-R60, 0-3). The popular slide rules ("never read your slides," "no decorative images," "labels not legends") remain **directionally supported** by the independent meta-analyses below — but **must not be sold with these numbers.**

**P-38 — Mayer, R. E. (2017), "Using multimedia for e-learning," *Journal of Computer Assisted Learning* 33(5).** **[UNVERIFIED-ONLY]**
https://onlinelibrary.wiley.com/doi/abs/10.1111/jcal.12197
*Status:* all five adjudicated claims (R62–R66) are UNVERIFIED — including the frequently-quoted per-principle effect sizes (coherence d = 0.70, redundancy d = 0.87, personalization d = 0.79, segmenting d = 0.70). **Do not rely on any of them.**

**P-39 — Noetel, Griffith, Delaney, Harris, Sanders, Parker, del Pozo Cruz & Lonsdale (2022), "Multimedia Design for Learning: An Overview of Reviews With Meta-Meta-Analysis," *Review of Educational Research* 92(3):413–454.**
https://doi.org/10.31234/osf.io/pynzr
*Good for:* **the real, independently-pooled number that should replace Mayer's box-score figures.** An overview of 29 reviews / 1,189 studies / 78,177 participants puts the average effect of multimedia design principles on **learning at g = 0.38, 95% CI [0.27, 0.49]**, pooled over 808 effect sizes from 66,553 participants (CONFIRMED-G15, 3-0).
*Do not cite for:* the quantitative mechanism gap — design interventions barely move cognitive load (overall **g = 0.22 [0.04, 0.40], k = 68**) even though they clearly move learning (REFUTED-G52, 0-3).

**P-40 — Schroeder & Cenkci (2020), "Do Measures of Cognitive Load Explain the Spatial Split-Attention Principle...?", *Journal of Educational Psychology* 112(2):254–270** (publisher record; full text paywalled).
https://www.ovid.com/journals/jedup/pdf/10.1037/edu0000372~do-measures-of-cognitive-load-explain-the-spatial
*Good for:* **the mechanism is unsupported.** A systematic review of 41 comparisons found cognitive-load measures **do not** support the extraneous-cognitive-load explanation of spatial contiguity, and found no compelling evidence that integrated designs significantly move *any* measure of cognitive load (CONFIRMED-G16, 2-1). **The behavioural effect holds; the load story does not.** Put the label on the diagram — but do not explain *why* using cognitive load.

**P-41 — Schroeder & Cenkci (2018), "Spatial Contiguity and Spatial Split-Attention Effects in Multimedia Learning Environments: A Meta-Analysis," *Educational Psychology Review* 30(3):679–701** (ERIC EJ1186641; full text paywalled).
https://eric.ed.gov/?id=EJ1186641
*Good for:* the newer, larger random-effects estimate — **58 independent comparisons, n = 2,426, g = 0.63, p < 0.001** (Noetel's re-extraction gives the CI: **[0.55, 0.71], k = 58**). Moderator analyses found the benefit held broadly; no strong boundary condition was isolated on the behavioural side (CONFIRMED-G17, 2-1). **Prefer this to Ginns' d = 0.85 when a single number is needed.**

**P-42 — Adesope & Nesbit (2012), "Verbal redundancy in multimedia learning environments: A meta-analysis," *Journal of Educational Psychology* 104(1):250–263.**
https://doi.org/10.1037/a0026147
*Good for:* **the "redundancy can help" boundary conditions.** Across 57 independent studies, spoken+written beat spoken-only **only** for (a) low-prior-knowledge learners, (b) system-paced materials, and (c) picture-free materials; and **partial** redundancy (key terms lifted from the narration) beat verbatim on-screen text. Spoken+written did **not** beat written-only. Noetel's re-extraction quantifies it: overall **g = 0.15 [0.08, 0.22], k = 57** (CONFIRMED-G18, 3-0). This is the source that stops "never put text on your slides" from being stated as a universal.

**P-43 — Schneider, Beege, Nebel & Rey (2018), signaling meta-analysis** (publisher article page). *Same work as P-29.*
https://www.sciencedirect.com/science/article/abs/pii/S1747938X17300581
*Good for:* **103 studies, N = 12,201, 145 pairwise comparisons, 46 years of research: retention g+ = 0.53 [0.42, 0.64]; transfer g+ = 0.33 [0.22, 0.43].** Cognitive load was significantly reduced. **Prior knowledge was not a moderator — directly contradicting the expertise-reversal prediction of cognitive load theory.** Signaling works, but not in the way CLT predicts (CONFIRMED-G19, 3-0).

## Plain language & readability (15)

**P-44 — Federal Plain Language Guidelines (PLAIN / Digital.gov).** **[DEAD CITATION — see hygiene note 1]**
https://plainlanguage.gov/guidelines/
*Good for:* nominally, that plain language is **audience-relative, not universal simplification** (CONFIRMED-R26, 3-0) — but **this claim was adjudicated against a URL that no longer serves the text**, and it is refined by CONFIRMED-G14 (3-0) read from the archived PDF: the FPLG rejects a *fixed universal grade-level target*, not grade-level targeting as such.
*Do not cite for:* a BLUF/answer-first mandate (REFUTED-R49, 0-3); the mechanically checkable structural limits — one idea per sentence, 150-word paragraphs, 250-word ceiling (REFUTED-R50, 0-3); or paraphrase testing with 6–9 participants plus the VBA case study (REFUTED-R51, 0-3). **All three failed on citation grounds. Re-source to P-45 before using any of them.** Note the asymmetry: answer-first ordering has an *independent* psycholinguistic rationale (see P-24/P-25/P-26), and paraphrase/teach-back testing has *independent* support (P-18/P-19) — the practices may be defensible even where these particular citations are not.

**P-45 — Federal Plain Language Guidelines, March 2011, Rev. 1, May 2011 — archived PDF (wid.org copy).** *This is the citation to use.*
https://wid.org/wp-content/uploads/2022/03/FederalPLGuidelines.pdf
*Good for:* the verbatim, page-anchored rules **with their hedges intact** — "Express only one idea in each sentence" (printed p.50) with **no numeric word limit anywhere on the page** (CONFIRMED-G9, 3-0); the 150/250-word paragraph numbers on p.66, **attributed to "Writing experts recommend," not asserted in the FPLG's own voice**, and backed by two legal-writing style manuals rather than any empirical readability study (CONFIRMED-G10, 3-0); the two adjacent hedges — the warning against uniform paragraph length and **"There is nothing wrong with an occasional one-sentence paragraph"** (CONFIRMED-G11, 3-0); "Cover only one topic in each paragraph" (p.68) with its usually-omitted **topic-sentence requirement**, scoped to "each paragraph **or section**" (CONFIRMED-G12, 3-0); the document's **non-binding, self-described "advice"** status (CONFIRMED-G13, 3-0); and the precise scope of the 8th-grade myth (CONFIRMED-G14, 3-0).
*Do not cite for:* main-message-first as a sentence-level rule — it **is** explicitly stated, but only as a **document-organization** instruction (all of Section II, "Organize," is four sentences on printed p.5) (REFUTED-G51, 1-2).

**P-46 — ISO 24495-1:2023 — Plain language — Part 1: Governing principles and guidelines.**
https://www.iso.org/standard/78907.html
*Good for:* plain language has a **formal published International Standard** (ISO/TC 37, edition 1, 14 pages, published 2023-06-20, stage 60.60), so plain-language guidance is standards-backed rather than style-guide folklore (CONFIRMED-R27, 3-0). And the language-scope statement: **ISO claims its principles are language-neutral while conceding all its illustrative examples are English-only** — the principles may be generalized, the worked examples may not (CONFIRMED-R28, 3-0).
**EN:** the examples. Not the principles.

**P-47 — Gruteke Klein, Frenkel, Shubi & Berzak (2025), "Readability Formulas, Systems and LLMs are Poor Predictors of Reading Ease" (arXiv abstract page).**
https://arxiv.org/abs/2502.11150
*Good for:* **asking an LLM to judge readability does not fix the problem** — frontier LLMs were evaluated alongside the formulas and also failed, so an LLM-based "readability check" is not trustworthy evidence that a rewrite is easier to read (CONFIRMED-R29, 3-0).
*Do not cite for:* the full enumeration of failing methods across traditional formulas, ML systems, frontier LLMs and commercial systems (REFUTED-R52, 0-3); or the positive claim that word length, word frequency and **surprisal outperform** the formulas (REFUTED-R53, 1-2) — for surprisal, cite P-53 to P-56 instead.
**EN:** the paper's own abstract restricts its finding to English. Do not generalize the negative result to other languages from this source.
*Time-sensitivity:* this is a preprint using current-generation frontier models; it will need re-checking.

**P-48 — Same paper, arXiv HTML v4.** **[UNVERIFIED-ONLY]** *Duplicate work, different URL.*
https://arxiv.org/html/2502.11150v4
*Status:* all five adjudicated claims (R83, R84, R131, R132, R133) are UNVERIFIED. Use P-47.

**P-49 — Bailin & Grafstein (2001), "The linguistic assumptions underlying readability formulae: A critique," *Language & Communication* 21(3):285–301** (ERIC record).
https://eric.ed.gov/?id=EJ629584
*Good for:* **readability formulas' linguistic criteria are not a valid basis for measuring text difficulty** — the surface features they rely on (word/syllable length, sentence length) do not constitute an adequate measure of reading difficulty, so a Flesch-Kincaid / Lexile-type score **cannot be treated as a measurement of comprehensibility** (CONFIRMED-R30, 3-0). And: the formulae's scientific authority is framed as an open question **answered in the negative**, despite institutional entrenchment in schools and publishing — **widespread adoption is not evidence of validity** (CONFIRMED-R31, 3-0).
*Operational:* readability scores may be used as a rough smell-test but **never as a target metric or as proof of clarity.**
*Do not cite for:* the two-named-failure-points formulation (REFUTED-R54, 0-3).
**EN:** the formulae's core variables were developed on English.

**P-50 — Nielsen Norman Group (Morkes & Nielsen), "Concise, SCANNABLE, and Objective: How to Write for the Web."** *(Tagged `primary` by the dossier; it is a self-published, non-peer-reviewed vendor report — treat its confidence accordingly.)*
https://www.nngroup.com/articles/concise-scannable-and-objective-how-to-write-for-the-web/
*Good for:* the widely-quoted numbers, **with their weakness stated** — a sample website scored **58% higher** in measured usability when written concisely, **47% higher** when scannable, **27% higher** when objective, and **124% higher** combining all three (approximately additive, not multiplicative). These are **single-site, single-study effect sizes on a composite score, never independently replicated** (CONFIRMED-R32, 2-1).
*Do not cite for:* "readers scan rather than read" (REFUTED-R55, 0-3); "marketese degrades comprehension and trust" (REFUTED-R56, 0-3); or "scanners read only the first sentence of each paragraph," offered as validation of topic-sentence conventions (REFUTED-R57, 0-3). **These are exactly the rules an LLM-coachable skill most wants, and they are the ones that failed.**
*Why confidence is low:* 5-condition between-subjects design, n = 51 total (~10 per cell), one fictitious 7-page site, one-tailed t-tests; "measured usability" is a geometric mean of five normalized measures, not a comprehension measure; the 27% figure rests mostly on non-significant differences. **Independent tests went the other way** — Elgin et al. (2001, HFES, n = 80) found *fewer* idea units correctly recalled for the concise style, reversing the single largest Nielsen effect.

**P-51 — Google developer documentation style guide — Jargon** (and companion Voice/tone + Word list pages). **[UNVERIFIED-ONLY]**
https://developers.google.com/style/jargon
*Status:* all five adjudicated claims (R67, R68, R69, R118, R119) are UNVERIFIED — including the ordered jargon decision procedure and the active-voice/agent-recoverability rationale. Do not rely on them.

**P-52 — Microsoft Writing Style Guide — Lists / Scannable content.** **[UNVERIFIED-ONLY]**
https://learn.microsoft.com/en-us/style-guide/scannable-content/lists
*Status:* all five adjudicated claims (R70, R71, R72, R120, R121) are UNVERIFIED — including the "at least two, preferably no more than seven items" range and the parallelism mandate. Do not rely on them.
**EN:** the source's own warning is worth noting even unverified — the "items complete an introductory fragment" list pattern is a **language-specific construction that breaks under translation**.


**P-53 — Hale, J. (2001), "A Probabilistic Earley Parser as a Psycholinguistic Model," NAACL** (ACL Anthology).
https://aclanthology.org/N01-1021.pdf
*Good for:* **a mechanical, formula-free difficulty metric that predates LLMs** — per-word cognitive load as **surprisal**, the negative log probability of a word given the preceding context. Unlike Flesch-Kincaid it needs **no syllable counting, no word-length proxy, and no English-tuned regression constants** — only a probability distribution over next words, which any autoregressive LM supplies **for any language** (CONFIRMED-G34, 3-0).

**P-54 — Levy, R. (2008), "Expectation-based syntactic comprehension," *Cognition* 106:1126–1177** (author PDF, MIT).
https://www.mit.edu/~rplevy/papers/levy-2008-cognition.pdf
*Good for:* **surprisal's language-neutrality is not an accident of English.** Levy proves that if processing difficulty is the KL-divergence "work" of updating a belief distribution over parses at each word, the difficulty is **exactly** the word's surprisal — independently of the underlying structures. The metric makes **no commitment to English syntax, word order, or morphology** (CONFIRMED-G35, 2-1).

**P-55 — Smith, N. J. & Levy, R. (2013), "The effect of word predictability on reading time is logarithmic," *Cognition* 128:302–319.**
https://vorpus.org/papers/smith-levy-2013-predictability-logarithmic.pdf
*Good for:* the surprisal→reading-time link is **logarithmic in probability (equivalently, linear in surprisal)** across six orders of magnitude of predictability — so per-token surprisal can legitimately be **averaged** to score a passage, with no nonlinear transform needed (CONFIRMED-G36, **1-1** — note the unusual split vote; treat with corresponding caution).
**EN:** established on **English corpora only** (Dundee eye-tracking + a self-paced-reading corpus). On its own it licenses nothing outside English — for cross-linguistic warrant use P-56.

**P-56 — Wilcox, Pimentel, Meister, Cotterell & Levy (2023), "Testing the Predictions of Surprisal Theory in 11 Languages," *TACL* 11:1451–1470.**
https://arxiv.org/html/2307.03667v4
*Good for:* **surprisal does generalize cross-linguistically.** On the MECO eye-tracking corpus (the same article content translated into each language), surprisal significantly improves reading-time prediction over baseline in **all eleven languages tested, spanning five families (Koreanic, Turkic, Semitic, Uralic, Indo-European)** (CONFIRMED-G37, 3-0). **This is the strongest available warrant for an LLM coach using surprisal as a language-neutral difficulty signal.**
*Do not cite for:* the cross-linguistic survival of the *linear* linking function specifically (REFUTED-G70, 0-3).

**P-57 — Futrell, Mahowald & Gibson (2015), "Large-scale evidence of dependency length minimization in 37 languages," *PNAS* 112(33):10336–10341.**
https://sites.socsci.uci.edu/~rfutrell/papers/futrell2015largescale.pdf
*Do not cite for:* dependency length as a language-neutral, probability-model-free structural red flag (REFUTED-G64, 0-3). The underlying observation — real sentences have shorter dependency lengths than random-linearization baselines across 37 hand-parsed languages from 10 families — is attractive precisely because it needs no LM; it did not survive as a coaching rule.

**P-58 — Levy & Keller (2013/2012), "Expectation and Locality Effects in German Verb-final Structures," *Journal of Memory and Language* 68(2):199–222** (PMC author manuscript).
https://pmc.ncbi.nlm.nih.gov/articles/PMC3928089/
*Do not cite for:* the crucial falsifier as stated — that **"shorten your dependencies" is not a safe universal coaching rule**, because in German verb-final main clauses *lengthening* the subject–verb dependency makes the final verb **faster** to read (anti-locality) (REFUTED-G65, 1-2). One vote short, but it is the reason the skill must not ship a universal dependency-shortening rule on the strength of P-57.

## Myths (11)

**P-59 — Mehrabian, A. & Ferris, S. R. (1967), "Inference of attitudes from nonverbal communication in two channels," *Journal of Consulting Psychology* 31(3):248–252.**
https://ibralc.com.br/wp-content/uploads/sites/5/2026/01/mehrabian-1967-inference-of-attitudes-from-nonverbal-communication.pdf
*Good for:* **the 7/38/55 numbers were never measured in any experiment.** They appear exactly once in the primary literature — as a **speculative extrapolation in the final discussion paragraph**, combining results across two separate studies, which **explicitly flags the model as untested** (CONFIRMED-G1, 2-1). And the sample: **62 subjects total, all female University of California undergraduates** fulfilling a course requirement — 25 used only to pre-select the neutral word, 17 to rate single-channel stimuli, and **just 20** to judge the combined facial-vocal conditions that produced the .55/.38 weights. **There was no "body language" channel at all** (CONFIRMED-G43, 3-0).
*Do not cite for:* the inference that the "7% words" figure is *therefore an artifact* of holding the verbal channel constant at the single pre-tested neutral word "maybe" (REFUTED-G49, 0-3); or that the measured coefficients (facial 1.50, vocal 1.03 — a ~3:2 ratio, not 55:38) *therefore* refute the formula (REFUTED-G50, 0-3). **The descriptive facts in both verify** — the word "maybe" never varied across the 36 conditions, and the regression really is A_T = 1.50·A_F + 1.03·A_V — but the load-bearing *inference* attached to each overreached. Quote the facts; do not quote the conclusion.

**P-60 — Mehrabian, A. & Wiener, M. (1967), "Decoding of inconsistent communications," *Journal of Personality and Social Psychology* 6(1):109–114.**
https://ibralc.com.br/wp-content/uploads/sites/5/2026/01/mehrabian1967-decoding-of-inconsistent-communications.pdf
*Good for:* the source of the "38% tone" half of the formula tested **only inconsistent single-word messages** — isolated English words (HONEY, DEAR, MAYBE, DON'T, BRUTE, TERRIBLE) spoken in positive/neutral/negative tone; main experiment **N = 30, only 10 subjects per instruction condition**. **The paper itself restricts its generalization** (CONFIRMED-G2, 3-0).
**EN:** the stimuli are isolated English words.

**P-61 — Mehrabian, A., *Silent Messages* — description and ordering information (author's own site).**
http://www.kaaj.com/psych/smorder.html
*Good for:* **Mehrabian's own standing caveat, in his own words, on his own site, printed alongside the formula** — the equation is restricted to **communications of feelings and attitudes (like/dislike)**, and outside that domain **the equations simply do not apply** (CONFIRMED-G3, 3-0). This is the cleanest possible refutation source: the author disowning the popular reading.

**P-62 — Pashler, McDaniel, Rohrer & Bjork (2008), "Learning Styles: Concepts and Evidence," *Psychological Science in the Public Interest* 9(3).**
https://journals.sagepub.com/doi/full/10.1111/j.1539-6053.2009.01038.x
*Good for:* the **exact experimental design required** to validate learning-styles instruction — classify by style, randomly assign within style group to instructional methods, give all learners the same test, and show a **style-by-method interaction** where the best method for one style is *not* the best for another (CONFIRMED-G5, 3-0). Their verdict on how many studies clear that bar: **essentially zero** — in a literature they call "enormous" they found exactly **one** potentially qualifying study (Sternberg et al., 1999) and reject even that (CONFIRMED-G6, 3-0).
*The scope distinction almost every retelling botches:* Pashler et al. do **not** claim modality preferences are fictitious, nor that people are cognitively identical. They affirm that people **reliably report presentation preferences** and that people **genuinely differ in aptitudes**. What fails is the **meshing hypothesis** (CONFIRMED-G7, 3-0). **Never state "learning styles don't exist" — state that matching instruction to them does not improve learning.**

**P-63 — Willingham, Hughes & Dobolyi (2015), "The Scientific Status of Learning Styles Theories," *Teaching of Psychology* 42(3):266–271.**
https://career.ucsf.edu/sites/g/files/tkssra15591/files/Article%20UCSF%20SEJC%20January%202017.pdf
*Good for:* the theory fails on **both** of its testable predictions, not just the pedagogical one. Prediction 1 (a learning style is a stable attribute of a person) **fails at the measurement layer** — "although there are a multitude of inventories and models for assessing learning styles, most are not reliable" (CONFIRMED-G8, 3-0).

**P-64 — Rogowsky, Calhoun & Tallal (2015), "Matching Learning Style to Instructional Method: Effects on Comprehension," *Journal of Educational Psychology* 107(1):64–78.**
https://core.ac.uk/download/pdf/144844129.pdf
*Do not cite for:* the framing that this was **the first** direct experimental test built to Pashler's specification (REFUTED-G67, 0-3). The **null result itself is verbatim in the abstract** — 121 college-educated adults, classified by a standardized commercial inventory, randomly assigned to audiobook vs e-text: "no statistically significant relationship between learning style preference and instructional method... failed to statistically support the meshing hypothesis." Cite the null; drop the "first."

**P-65 — Rogowsky, Calhoun & Tallal (2020), "Providing Instruction Based on Students' Learning Style Preferences Does Not Improve Learning," *Frontiers in Psychology* 11:164.**
https://pmc.ncbi.nlm.nih.gov/articles/PMC7033468/
*Good for:* **the null replicates in the population learning-styles instruction actually targets — K-12 children.** The entire 5th-grade cohort of a Pennsylvania public middle school (n = 125, ages 10–11), age-matched Dunn & Dunn inventory, counterbalanced crossover of reading vs listening instruction: **no instruction-by-style effect** (CONFIRMED-G45, 3-0).

**P-66 — Newton & Salvi (2020), "How Common Is Belief in the Learning Styles Neuromyth, and Does It Matter? A Pragmatic Systematic Review," *Frontiers in Education* 5:602451.**
https://cronfa.swansea.ac.uk/Record/cronfa55948/Download/55948__19073__020e8797d9b54dfda1831503535621d2.pdf
*Good for:* **the belief persists at near-universal rates despite ~16 years of published refutation.** PRISMA systematic review, 37 samples, 15,405 educators, 18 countries, 2009–early 2020: a weighted **89.1% of educators endorse matching instruction to learning styles, with no downward trend over time** (CONFIRMED-G46, 3-0). Cite this to explain why the myth must be *actively* refuted rather than assumed dead.

**P-67 — Haubert et al. (2018), "Relationship of Event-Related Potentials to the Vigilance Decrement," *Frontiers in Psychology* 9:237.**
https://www.frontiersin.org/journals/psychology/articles/10.3389/fpsyg.2018.00237/full
*Good for:* **the defensible replacement for the "attention span" myth.** What attention science actually measures is the **vigilance decrement** — a gradual decline in the probability of detecting rare critical signals with time-on-task, operating over **tens of minutes to hours, not seconds** (Mackworth 1948: ~10–15% drop after roughly 30 min) (CONFIRMED-G4, 3-0).

**P-68 — Weinreich, Obendorf, Herder & Mayer (2008), "Not Quite the Average: An Empirical Study of Web Use," *ACM Transactions on the Web* 2(1), Article 5.**
https://www.eelcoherder.com/images/publications/2008/not_quite_the_average.pdf
*Good for:* **the only real study anywhere in the "8-second attention span" citation chain — and it measured web-page dwell time, not attention.** Median stay time on Google search-result pages was **8.0 seconds** (the likely origin of "8 seconds"; 12.4s for new pages, plausibly the "12 seconds"). **The authors explicitly warn their stay times are an upper bound on attention, not a measure of it** (CONFIRMED-G44, 3-0).

**P-69 — Lapakko, D., "Communication is 93% Nonverbal: An Urban Legend Proliferates," *Communication and Theater Association of Minnesota Journal*.** **[UNVERIFIED-ONLY]**
https://cornerstone.lib.mnsu.edu/cgi/viewcontent.cgi?article=1000&context=ctamj
*Status:* all five adjudicated claims (R76, R77, R78, R124, R125) are UNVERIFIED — including the 79-website content analysis and the citation-decay figures. Do not rely on them. **For Lapakko's adjudicated content, use S-03 instead.**

---

# Secondary sources (4)

**S-01 — Nielsen Norman Group, "Inverted Pyramid: Writing for Comprehension."** **[UNVERIFIED-ONLY]**
https://www.nngroup.com/articles/inverted-pyramid/
*Status:* all five adjudicated claims (R85, R86, R87, R134, R135) are UNVERIFIED. Do not rely on it. Note that the *substantive* question it addresses — whether conclusion-first ordering aids comprehension — is answered **negatively** by adjudicated primary sources (P-26, P-28).

**S-02 — BBC News / *More or Less*, "Busting the attention span myth" (2017).**
https://www.bbc.com/news/health-38896790
*Good for:* **the citation chain terminates in a void.** *More or Less* chased the 8-second figure to its end: the two organisations Statistic Brain names as verification sources **could find no record of any such research**, Statistic Brain never responded, and the attention researchers consulted did not recognise the numbers (CONFIRMED-G40, 3-0). And: **researchers reject the premise, not merely the number** — there is no such quantity as an "average attention span" to measure; attention is task-dependent and psychologists would not attempt to quantify it as a fixed scalar (CONFIRMED-G41, 2-1). **The claim is not "wrong by a few seconds" — it is not the kind of thing that has a value.**

**S-03 — Lapakko, D. (1997), "Three cheers for language: A closer examination of a widely cited study of nonverbal communication," *Communication Education* 46:63–67** (p. 65, quoting A. Mehrabian, personal communication, 1995).
http://www.communicationcache.com/uploads/1/0/8/8/10887248/three_cheers_for_language_-_a_closer_examination_of_a_widely_cited_study_of_nonverbal_communication.pdf
*Good for:* **in peer-reviewed correspondence Mehrabian called the general reading "absurd"**, and said that for a non-attitudinal message the **verbal part is nearly 100% of the message**. Lapakko additionally establishes that the formula was **pieced together from two studies with no study comparing all three channels** (CONFIRMED-G38, 3-0). *(Despite the `secondary` tag, this is a peer-reviewed journal article — it is the strongest Lapakko citation available in this dossier.)*

**S-04 — "Attention spans" — Consumer Insights, Microsoft Canada (Spring 2015), full report PDF.**
https://static1.squarespace.com/static/59bf2bf68fd4d28e59627113/t/5ab01bdff950b70546a08167/1521490918597/265348695-Microsoft-Attention-Spans-Research-Report.pdf
*Good for:* **the 8-second figure did not come from Microsoft's own research.** The report presents 12s (2000) / 8s (2013) / 9s (goldfish) on a single infographic page whose **only attribution is "Source: Statistic brain"** — imported wholesale from a third-party aggregator, not measured by the report's own survey or EEG work (CONFIRMED-G39, 3-0).
*Do not cite for:* the claim that the report **repudiates** the scalar "attention span in seconds" framing (REFUTED-G66, 0-3). The report *does* adopt Sohlberg & Mateer's three-part attention model (verbatim, p.10) and its foreword *does* read "Think digital is killing attention spans? Think again." — **but page 7 of the same PDF reprints the 8-second figure**, so the report cannot be cited as repudiating what it also reproduces.

---

# Blog sources (0)

**None.** The dossier contains no source tagged as a blog. This section exists so its emptiness is explicit rather than an oversight.

---

# Unreliable sources (1) — cited only as objects of study

> The entry below is **not evidence**. It is cited **only as the object under investigation** — the thing whose unreliability is the finding. Never cite it in support of any proposition.

**U-01 — "Attention Span Statistics" — Statistic Brain (Wayback snapshot, 4 May 2015).** **[UNRELIABLE]**
http://web.archive.org/web/20150504135207/http://www.statisticbrain.com/attention-span-statistics/
*What it is good for — and only this:* **demonstrating that the source of the "8-second attention span" is untraceable.** The archived page offers **no study, no author, no methodology, no sample** — only a "Statistic Verification" line naming two institutions and a wire service. Worse, **the figure is unstable across versions**: the Jan-2014 / Jan-2015 snapshots read "8 seconds" labelled 2013, while the May-2015 snapshot silently reads "8.25 seconds" (CONFIRMED-G42, 3-0).
*This is the terminal node of the citation chain* traced by S-02 and S-04. Its evidential value is exactly zero and its forensic value is high.

---

# Unverified — do not rely on

Seven sources have **no** CONFIRMED or REFUTED claim keyed to them; every adjudicated claim is UNVERIFIED (extracted but never adjudicated, for verification-budget reasons). **Absence of adjudication is not evidence of correctness.** They may be cited only with an explicit "unverified" label, or re-verified first.

| # | Source | Unverified claims |
| --- | --- | --- |
| P-14 | Leiden repository — Western-centrism in pragmatics | R81, R82, R128, R129, R130 |
| P-38 | Mayer (2017), *Using multimedia for e-learning* (JCAL) | R62, R63, R64, R65, R66 |
| P-48 | arXiv 2502.11150 HTML v4 (readability/LLMs) | R83, R84, R131, R132, R133 |
| P-51 | Google developer style guide — Jargon | R67, R68, R69, R118, R119 |
| P-52 | Microsoft Writing Style Guide — Lists | R70, R71, R72, R120, R121 |
| P-69 | Lapakko, CTAMJ — "Communication is 93% Nonverbal" | R76, R77, R78, R124, R125 |
| S-01 | NN/g — Inverted Pyramid | R85, R86, R87, R134, R135 |

Note the pattern: **the practitioner style guides are the least-verified tier in the whole dossier.** The rules a coaching skill most wants to enforce mechanically (list-length ranges, jargon decision procedures, inverted-pyramid ordering) are precisely the ones with no adjudicated support here.

---

# Effect sizes that survived verification

Only these may be quoted as numbers. Everything else in the dossier's numeric inventory is either REFUTED as written or UNVERIFIED.

| Effect | Value | CI | k / N | Source | Verdict |
| --- | --- | --- | --- | --- | --- |
| Spatial + temporal contiguity | d = 0.85 | [0.68, 1.02] | 50 effects / 2,375 students | Ginns 2006 (P-36) | CONFIRMED-R11, 3-0 — **but Q = 117.77, df = 49, p < .001; not a transferable constant** |
| Spatial contiguity (newer, larger) | g = 0.63 | [0.55, 0.71] | k = 58 / n = 2,426 | Schroeder & Cenkci 2018 (P-41) | CONFIRMED-G17, 2-1 |
| Multimedia design principles → learning | g = 0.38 | [0.27, 0.49] | 808 effects / 66,553 participants | Noetel et al. 2022 (P-39) | CONFIRMED-G15, 3-0 |
| Multimedia design principles → cognitive load | g = 0.22 | [0.04, 0.40] | k = 68 | Noetel et al. 2022 (P-39) | REFUTED-G52, 0-3 — the **mechanism gap**; load pathway too small to carry the learning effect |
| Signaling → retention | g+ = 0.53 | [0.42, 0.64] | 103 studies / N = 12,201 | Schneider et al. 2018 (P-43, P-29) | CONFIRMED-G19 / G47, 3-0 |
| Signaling → transfer | g+ = 0.33 | [0.22, 0.43] | 103 studies / N = 12,201 | Schneider et al. 2018 (P-43, P-29) | CONFIRMED-G19 / G47, 3-0 |
| Verbal redundancy (spoken+written vs spoken) | g = 0.15 | [0.08, 0.22] | k = 57 | Adesope & Nesbit 2012 (P-42) | CONFIRMED-G18, 3-0 — helps **only** for low-prior-knowledge, system-paced, picture-free |
| Self-explanation prompts | g = 0.55 | [0.45, 0.65] | 69 effects / 64 reports / N = 5,917 | Bisra et al. 2018 (P-18) | CONFIRMED-G20, 2-1 |
| Advance organizers → learning | ES = .21 | SE .04 | 110 effects / 135 studies | Luiten et al. 1979/80 (P-27) | CONFIRMED-G29, 3-0 |
| Advance organizers → retention | .19–.38 | — | 50 effects | Luiten et al. 1979/80 (P-27) | CONFIRMED-G29, 3-0 |
| Analogical transfer, hint vs no hint | ~75% vs ~30% (baseline ~10%) | — | Duncker radiation problem | Gick & Holyoak 1983 (P-32) | CONFIRMED-G24, 3-0 |
| Topic-before vs no-topic (recall, of 18 idea units) | 5.83 vs 2.82 | SE .49 / .60 | n = 18 / 17 | Bransford & Johnson 1972 (P-25) | CONFIRMED-G28, 3-0 |
| Frame-first, unfamiliar content (reading time) | 52.1s vs 81.3s | t(30) = 2.437, p < .05 | 32 Ss | Kieras 1980 (P-26) | CONFIRMED-G27, 3-0 — **vanishes for familiar content (50.9s vs 57.4s, n.s.)** |
| Grounding compression (words per figure) | 41 → 8 | F(1,35) = 44.31, p < .001 | 8 pairs / 12 figures / 6 trials | Clark & Wilkes-Gibbs 1986 (P-08) | CONFIRMED-R16, 3-0 |
| Curse of knowledge (tapping) | predicted 50% vs actual 2.5% | range 10–95% | 40 tappers / 40 listeners / 120 songs | Newton 1990 (P-01) | CONFIRMED-R1, 3-0 |
| Jargon → processing fluency | M = 4.57 vs 5.27, η² = .11 | — | N = 650 | Bullock et al. 2019 (P-35) | REFUTED-G59, 1-2 — **one vote short; re-verify** |

---

# Sources cited inside adjudications but not in the 74

The dossier's verification notes and synthesis cite ~44 further URLs as **counter-sources, replications and qualifications** inside individual adjudications (for example: Miller 1956 at psychclassics.yorku.ca; Thalmann, Souza & Oberauer on chunk size; Ericsson & Kintsch's long-term working memory revision; Hawkins et al. 2020 and Davies 2007 on least collaborative effort; Arnold et al. 2000 on given-new as a gradient preference; Sadoski, Paivio & Goetz on the "bizarre texts" generalization ceiling; Dingemanse et al. 2015 on 12 languages; Elgin et al. 2001 reversing the NN/g concise effect; the Stanford author copy of Clark & Brennan; digital.gov and the ies.ed.gov FPLG mirror).

**These are not part of the 74-source list and are not independently adjudicated here.** They are named so that a reader who finds them quoted in a sibling document knows where they came from and that they carry the status of *supporting citation inside a verification note*, not *verified source*.

---

## What this does NOT license

Every item below is an overreach a reader of this bibliography might be tempted into. Each is blocked by a REFUTED verdict or an explicit language caveat in the dossier.

**Memory and load**
- **"Working memory holds 4 slots" / "never more than 4 bullets."** The ~4 figure is a *pure-capacity* estimate valid only under Cowan's boundary conditions (rehearsal and recoding blocked); the slot-vs-resource mechanism is contested; and capacity is over **knowledge-relative chunks**, so the number of presentable things is a function of the audience's prior knowledge, not a constant (REFUTED-R38, R39). The correct move is to **reduce the chunk count for this audience** (pre-teach labels, group by familiar structure), never to enforce a magic number.
- **"Reduce extraneous load"** as an audience-independent rule. The construct is not cleanly separable, is often measured backwards from post-tests, and its instrument is non-standardized (CONFIRMED-R8/R9/R10). You must first fix *who* is listening.

**Curse of knowledge**
- **"Experts are literally unable to simulate ignorance."** Refuted (R37, 0-3). They are *systematically and persistently miscalibrated*; markets/feedback/incentives at best halve the bias.
- **"The expert hears the full orchestration in their head, which is why they can't hear how thin the signal is."** Refuted (R35, 0-3). Keep the behavioural headline; drop the mechanistic story.

**Ordering**
- **"Clark & Haviland validate BLUF."** They validate **frame-before-details** — a different construct from conclusion-first. And **no experiment in the chapter manipulates given/new order** (write "argue," not "demonstrated").
- **"BLUF is evidence-based."** The one study that tested exactly the BLUF manipulation found **no reading-time benefit** (Kieras, P-26), and the one that pitted inverted-pyramid against chronological narrative found narrative produced **higher comprehension and lower load** (Ameseder, P-28). What *is* robustly supported is **signaling** — making structure visible — not ordering by conclusion (P-29/P-43).
- **"The Federal Plain Language Guidelines mandate BLUF."** Refuted (R49, 0-3). Main-message-first appears only as a **document-organization** instruction, in a four-sentence section (REFUTED-G51, 1-2), in a document that **never once uses the words "binding" or "mandatory"** (CONFIRMED-G13).

**Plain language and readability**
- **"Ship 150-word paragraphs, max 250, three to eight sentences."** The numbers are real but the FPLG **does not assert them in its own voice** and **explicitly permits one-sentence paragraphs** — below its own band (CONFIRMED-G10, G11). Quoting the band without the exception is a **misquote**.
- **"Write to an 8th-grade level"** — or its mirror, **"grade-level targeting is a myth."** Both are wrong. The FPLG rejects a **fixed universal** grade-level target while making the 8th-grade target **audience-conditional** (CONFIRMED-G14).
- **"Optimize the Flesch-Kincaid / Lexile score."** Readability formulas are not a valid measure of difficulty (CONFIRMED-R30/R31). Scores may serve as a rough smell-test; **never as a target metric or as proof of clarity.**
- **"LLMs cannot assess readability."** Too broad. The surviving claim is narrower: **LLM readability judgments are not validated against real-time processing ease** and must not be the sole evidence a rewrite is easier (CONFIRMED-R29).
- **"Readers scan, not read" / "marketese hurts comprehension" / "people read only first sentences."** All refuted at 0-3 (R55, R56, R57) against a non-peer-reviewed vendor report whose largest effect was **reversed** in independent testing.

**Presentations and multimedia**
- **"Closer is always better" for labels.** Falsified by the documented **spatial-contiguity failure** (maximum proximity underperformed medium proximity). And the contiguity benefit is **moderated by material complexity** — for simple content, separation is comparatively inconsequential (CONFIRMED-R12).
- **Quoting Mayer's box scores** ("23 of 23 tests, median d = 0.86"; "22 of 22, d = 1.10"). None survived (R58, R59, R60). Use the independently-pooled g = 0.38 (P-39) and g = 0.63 (P-41) instead.
- **"Never put text on your slides."** Redundancy **helps** for low-prior-knowledge learners, system-paced material, and picture-free material, and **partial** redundancy (key terms) beats verbatim text (CONFIRMED-G18).
- **"Reducing cognitive load is why these design rules work."** The load pathway is **far too small to carry the behavioural effect** (g = 0.22 vs g = 0.38) and load measures **do not support** the extraneous-load explanation of contiguity (CONFIRMED-G16, REFUTED-G52).

**Dialogue and grounding**
- **"Least collaborative effort means ship imperfect drafts."** Clark & Wilkes-Gibbs **explicitly exclude** novels, letters, broadcasts, sermons and large lectures. Where the addressee **cannot repair, the self-sufficient utterance is the right target.** The licence applies to live dialogue only.
- **"Silence means understanding."** In no language. Listeners are under systematic pressure to **feign understanding** (CONFIRMED-R19), and repair infrastructure exists everywhere but its **use** is modulated by face and politeness norms.

**Myths**
- **"Communication is 93% nonverbal."** The numbers were **never measured** (CONFIRMED-G1); the author himself calls the general reading **"absurd"** and restricts the equation to **feelings and attitudes** (CONFIRMED-G3, G38). But note the discipline required here too: the *inference* that the 7% figure is a mere artifact was itself refuted (REFUTED-G49/G50). **State what the studies did and did not measure; do not overclaim the debunking.**
- **"People have an 8-second attention span."** The chain terminates in an untraceable aggregator page whose number **changed silently between snapshots** (CONFIRMED-G42); the only real study in the chain measured **web-page dwell time** and warned it was an upper bound on attention (CONFIRMED-G44). Researchers reject **the premise, not just the number** (CONFIRMED-G41).
- **"Learning styles don't exist."** Not the claim. Pashler et al. affirm that people **reliably report presentation preferences** and **genuinely differ in aptitudes**. What fails is the **meshing hypothesis** — matching instruction to style does not improve learning (CONFIRMED-G7, G45, G67).

**Language scope — never generalize these beyond English**
End-of-sentence focal stress; cleft / pseudocleft / passive information-packaging; definite-NP-first tendencies (P-24). All readability formulas — the 2025 eye-tracking paper restricts its own finding to English (P-47, P-49). ISO 24495-1's worked examples — ISO says so itself (P-46). Bell's /t/-voicing variable (P-16). English backchannel tokens "uh huh," "yeah" (P-07). Mehrabian's isolated English word stimuli (P-60). Microsoft's "items complete an introductory fragment" list pattern, which **breaks under translation** (P-52). Smith & Levy's logarithmic linking function, established on English corpora only (P-55).

**Language scope — established cross-linguistically**
The curse of knowledge. Chunk-relative capacity. Grounding and positive-evidence-seeking. Repair infrastructure (documented across 8+ language families, ~10+21 languages in 2013 and 12 in 2015 — an **inductive** generalization over ~7,000 languages, hedged by its own authors as "likely to be attested"). Audience design as a principle. Frame-before-details. Spatial and temporal contiguity. **Surprisal** — significantly improving reading-time prediction in **all eleven languages across five families** tested (P-56), and provably independent of the underlying syntax (P-54).
