# Writing documents: when the reader is not in the room

> **What this is.** The evidence for one-way written artifacts — documents, reports, specs, guides — as distinct from live explanation. What changes when the receiver cannot answer back, what a non-linear reader needs, what the medium costs, whether revising a document measurably helps anyone, and what an author can and cannot check alone.
> **Evidence base.** Entries **W-01 to W-12** in `11-bibliography.md` (12 catalogued entries; some cover more than one paper, and the document links 22 URLs in total). Each was fetched and quote-checked against the primary document in this session, **except** the two marked `RECORD-ONLY` and `NOT CHECKED` where it says so. **None of them went through the three-verifier adversarial adjudication** that produced the `3-0` / `2-1` verdicts elsewhere in this knowledge base. See "Evidence status" immediately below — this is a weaker tier and must be reported as one.
> **Load this when.** The deliverable is a document rather than a conversational answer: a README, a design document, a spec, a report, a guide, a commit message, a PR description.

---

## Evidence status — read before quoting anything here

Documents 01–12 carry verdicts from a specific process: each claim was sent to three verifiers instructed to refute it, each retrieved the source independently, and two refutations killed the claim. **This document did not go through that process.**

What most of it did go through: the source was fetched, opened, and the quoted text read in the primary document, with numbers taken from the paper rather than from an abstract service, a blog, or a search summary. **Not all of it did**, and the exceptions are marked where they occur.

| Tag used here | Means |
|---|---|
| `QUOTE-CHECKED` | The quote and the numbers were read in the fetched primary source. One pass, no adversarial round. |
| `RECORD-ONLY` | The full text could not be retrieved. Only design, direction and bibliographic detail are reported, from a catalogue record or the paper's own abstract. **No internal number is quoted.** |
| `NOT CHECKED` | A lead, listed so the next person knows where to go. Nothing from it is quoted anywhere. |
| `INFERENCE` | A rule this knowledge base derives from a source that did not test it. Never cite the source as if it did. |
| `HEURISTIC` | No study behind it in this knowledge base. Say the word "heuristic" out loud when using it. |

**Do not upgrade a `QUOTE-CHECKED` claim to `3-0` by proximity.** The refutation rate in the adjudicated passes was roughly 38%, and the typical casualty was a real finding stretched one step past its source. Nothing *new* here has been through that filter, so the stretching has not been checked for.

**Findings already adjudicated elsewhere keep their verdicts.** Where this document cites something carrying a `3-0` from documents 01–12 — the signaling meta-analysis, for instance — that verdict belongs to the original finding. **The writing application built on top of it does not inherit the verdict**, and is tagged separately.

One concrete illustration of how easily this slips, and it is this document's own near-miss: a secondary summary of Carroll et al. (1987) reports that Minimal Manual learners scored "better by a factor of eight." That phrase does not appear in the Minimal Manual paper, and it was almost quoted here as if it did. It is not invented — Carroll & Rosson's *Paradox of the Active User* reports exactly that figure, for a **different comparison**: learners transferred to the advanced-topics sections of a commercial manual, where "their performance on learning achievement tests was better by a factor of eight." So the error would have been **misattribution**, not fabrication: right number, wrong paper, wrong phase of the experiment. That is the commoner and more dangerous failure, because the number survives every check except opening the source.

---

## Part 1 — The line: repair available, or not

### 1.1 Where the dialogue rules stop

This knowledge base's dialogue findings — least collaborative effort, the repairable draft, compact utterances that invite refashioning — are explicitly bounded by their own source. Clark & Wilkes-Gibbs exclude novels, letters, broadcasts, sermons and large lectures `[03 §4b]`, `[12 §2.4]`. Where the addressee cannot repair, **the self-sufficient utterance is the target**, and "ship a rough draft, they'll ask" is forbidden.

That is the whole structural difference. Everything in Part 2 and Part 3 follows from it.

### 1.2 What "self-sufficient" does not mean

**Self-sufficient means sufficient for the stated reader and the stated task, with prerequisites named and reachable.** It does not mean inlining a knowledge base into every document.

A document may depend on material the reader demonstrably has: the diff attached to the PR, the issue it links, the file it sits beside. What it may not do is depend on a conversation the reader was not in, or on a reply that may never arrive.

`HEURISTIC` — this boundary is a chosen service level, not a measured optimum. No source here establishes how much context is the right amount. The failure mode it guards against is real and observable, though: see §4.2 on "as discussed".

### 1.3 Semi-interactive media — the default, labelled as a default

`12-open-questions.md` §3.2(2) states the gap and does not close it: async chat, PR comments and commentable documents all have a repair channel, but a slow, costly, publicly visible and optional one, and no source in this knowledge base places them on either side of the line. Clark & Brennan supply the dimensions — copresence, visibility, audibility, cotemporality, simultaneity, sequentiality, reviewability, revisability — and Monk (2003) notes the framework "has yet to be fleshed out in sufficient detail" to yield mechanical predictions.

The operating rule, and its status:

> `HEURISTIC` — **For a persistent artifact or an asynchronous message, carry what the intended reader needs for their task without requiring a future reply.** Use discussion to resolve uncertainty and improve the artifact. Do not make essential context depend on that discussion happening.

**Do not flatten "asynchronous" into one case.** A commit message read from `git log` eighteen months later has no repair channel at all and is archival. A PR description serves reviewers who *can* ask and future readers who cannot; its comment thread is an extra channel, not a guarantee that every reader shares it. A narrow reply inside an active thread may legitimately depend on that thread — inflating every comment into a standalone report is its own failure.

---

## Part 2 — Does revising a document actually help a reader?

This is the load-bearing question for a writing mode, and it is worth being exact about how good the answer is: **the direction is corroborated across many independent documents, organizations and countries; study quality and design vary widely, from field reports to controlled experiments; and almost every intervention is a bundle, so no individual rule inherits any of the numbers.**

### 2.1 The field evidence (Kimble)

Joseph Kimble collected the empirical studies of plain-language document revision. The version checked here is the article — *Writing for Dollars, Writing to Please*, *The Scribes Journal of Legal Writing* 6 (1996–97) — whose own words are "Behold, then, the **25 studies and reports** that follow" ([Scribes PDF](https://scribes.org/wp-content/uploads/2022/12/Scribes_vol6_04_Writing_for_Dollars.pdf), `QUOTE-CHECKED`). Later book editions carry more; **their counts were not checked here and no number from them is quoted.**

His own summary of what the second section shows, verbatim:

> "readers strongly prefer plain language in public and legal documents, they understand it better than legalistic style, they find it faster and easier to use, they are more likely to comply with it, and they are much more likely to read it in the first place."

Four entries with numbers, all read in the article:

| Study | Measure | Result |
|---|---|---|
| U.S. Department of Veterans Affairs letter | % of veterans who **failed to understand** the letter | **56% → 11%** after revision. Average reading time 8 min → 6 min. Judged "somewhat difficult" 44% → **0%**. |
| Suchan & Colucci (1989), *Management Communication Quarterly* 2:454 — 262 naval officers, "high-impact" vs "traditional bureaucratic" memo | correct answers, reading time, rereading | Higher percentage correct **on each of seven questions**; memo read in **17% less time** (23% less for the D.C. group); **half as many** felt the need to reread. |
| Kimble's South African Human Rights Commission Bill test — 43 law students + 24 staff | accuracy, speed, rated difficulty | **~19% more accurate**, **7% faster**; difficulty rating 6.52 → 4.35 on a 1–10 scale (~33% improvement). |
| Preference survey, Michigan / Florida / Louisiana / Texas — **1,462** judges and lawyers | preference for plain vs traditional version of six paragraphs | Plain-language version preferred by margins of **80% to 86%** in all four states. |

Plus, from the Law Reform Commission of Victoria's redraft of Australia's Takeovers Code: lawyers and law students "comprehended the plain-language version in half to a third of the average time needed to comprehend the original version."

**The limits, which travel with every one of these numbers:**

- **This is an advocate's collection, not a meta-analysis.** Kimble opens by stating the purpose: "We who extol plain language need to show, conclusively, that it works." There is no pooling, no heterogeneity test, no publication-bias correction, and no stated inclusion protocol that would let someone else reproduce the set.
- **Several entries are agency reports and conference handouts**, cited as "on file with author", not peer-reviewed studies.
- **Every intervention is a bundle.** The documents were reorganized, rewritten, and often visually redesigned at the same time. **No single writing rule can claim credit for any of these numbers.** A rule that cites one of them as its own warrant is misattributing a bundle.
- Overwhelmingly English, overwhelmingly legal and governmental prose.

**What survives.** Revising a real document for a real audience has repeatedly and measurably improved comprehension, speed, compliance and preference, across many independent organizations. That is enough to establish that document revision is not decoration. It is not enough to price any individual rule.

### 2.2 The controlled version (Charrow & Charrow)

Charrow & Charrow (1979), "Making Legal Language Understandable: A Psycholinguistic Study of Jury Instructions", *Columbia Law Review* 79:1306–1374 ([Semantic Scholar record](https://www.semanticscholar.org/paper/c3f30985e21414d02f80fe057b0a7ee46e940234)). **`RECORD-ONLY`** — the full text was not retrievable in this session, so only design and direction are reported here, from the catalogue record. **No internal number from this study is quoted anywhere in this knowledge base**, and the summary below should be treated as a pointer, not as a result.

Fourteen California pattern civil jury instructions; subjects heard a recording and paraphrased each instruction; comprehension was scored from the paraphrase. Rewriting to remove specific linguistic features raised comprehension.

**Limits:** oral delivery, English legalese, 1979, and the identified villains (long complex sentences, particular grammatical structures, specialized terms) are English constructions. **The design generalizes; the rewrite list does not.**

### 2.3 Task-based documentation: the strongest single experiment available

Carroll, Smith-Kerker, Ford & Mazur-Rimetz (1987), "The Minimal Manual", *Human–Computer Interaction* 3(2):123–153 ([PDF](http://swcarpentry.github.io/swc-releases/2017.02/instructor-training/files/papers/carroll-minimal-manual-1987.pdf), `QUOTE-CHECKED`).

This matters because almost everything else in this knowledge base measures *remembering* an explanation. This measures *doing the task the document exists for*.

Abstract, verbatim:

> "The Minimal Manual was designed to address difficulties people have with state-of-the-art self-instruction manuals in learning to use powerful computing devices. It is briefer; it helps learners to coordinate their attention between the system and the manual; it specifically trains error recognition and recovery; it better supports reference use after training. In two experiments, the Minimal Manual was shown to afford more efficient learning progress than an otherwise comparable, commercially developed self-instruction manual, and was superior in the specific areas predicted by its design."

The four design principles, as the paper's own contents list names them:

1. **Focus on Real Tasks and Activities**
2. **Slash the Verbiage**
3. **Support Error Recognition and Recovery**
4. **Guided Exploration**

Experiment 1 results, read from the paper:

| Measure | Result |
|---|---|
| Learning time | **40% less** for Minimal Manual subjects, *t*(17) = 3.06, *p* < .01 |
| Performance subtasks completed | **2.7×** as many, *t*(16) = 3.63, *p* < .01 |
| Basic tasks only | Minimal Manual group ahead by **50%**, *t*(16) = 2.11, *p* = .05 |

The time advantage also held for the advanced material — which **both groups read from the same commercial manual** — which is the paper's evidence that the minimal manual improved subsequent learning rather than merely being shorter.

**Limits, stated by the paper's own statistics:**

- Experiment 1 is roughly 19 subjects (about 10 and 9 per condition), recruited through a temporary agency.
- In **Experiment 2**, the getting-started differences were mostly **not significant**: Minimal Manual learners were "almost twice as fast to start the system up, and 20% to 40% faster to load diskettes, to reach the typing area, and to print out their first document," but "these differences were statistically significant only in the case of time to start the system up, *F*(1,28) = 5.92, *p* < .05."
- 1987, word processors, paper manuals, novice office workers.
- **Bundled again.** Four principles varied together. "Slash the Verbiage" cannot be credited on its own — and the paper's own framing puts error recovery and attention coordination alongside brevity, not beneath it.

Replicated: Lazonder & van der Meij (1993), "The minimal manual: is less really more?", *International Journal of Man–Machine Studies* 39:729–752 — 64 first-year Dutch university students, randomly assigned; the results resembled the original, with minimalist users learning faster and better ([Semantic Scholar record](https://www.semanticscholar.org/paper/d5373fcf6f523a84022a16fef32f2a3b0ed3c810)). **Note what the replication buys and does not buy:** it is a second language and a second population, which is real corroboration; it is still the same bundled manipulation.

**Operational consequence.** For a document whose purpose is *doing* rather than *knowing* — a guide, a runbook, a getting-started page — organize by the reader's real task, and include what happens when it goes wrong. The error-recovery half is the part that gets dropped, and it is named in the paper's own design list.

---

## Part 3 — Structure for a reader who did not start at the top

### 3.1 The inference, marked as one

`04 §1` establishes frame-before-details on *linear* reading: Bransford & Johnson's Experiment II, one added topic sentence, comprehension 2.29 → **4.50** and recall 2.82 → **5.83** on identical text.

Two corrections that must travel with that finding when it is applied to documents:

**(a) The late-topic condition is numerically lower, not demonstrated to be harmful.** Topic After scored 2.12 against No Topic's 2.29 (comprehension) and 2.65 against 2.82 (recall). The significance tests reported are Topic Before against each of the other two. **No test of Topic After against No Topic was run.** The defensible sentence is "a late frame bought nothing"; "a late frame is worse than no frame" is one step past the data. Note also that the comprehension measure was a *subjective rating*, and the passages were deliberately vague.

**(b) Bransford & Johnson did not test hyperlink entry, independently reachable sections, repeated headings, or the cost of duplicated context.** Applying it at section level is an inference.

The rule, with its status attached:

> `INFERENCE` — **"Before" means before the reader meets the details, not before page one.** At a point where a reader can plausibly enter the document directly, name the subject, the scope that applies, and the prerequisites, before details that depend on them. A heading may already do this.

A section headed "Recovery" whose first line is "Run this after the previous step" is unusable to someone arriving from a search result. "Recover a replica after a failed upgrade", followed by the state it assumes, is inspectable.

**What this explicitly does not license:** repeating the introduction under every heading. Some subsections genuinely depend on their parent and can say so; some headings already orient. Repetition costs reading time and maintenance, and **no source here shows a benefit that pays for it.**

### 3.2 Headings and overviews — what was actually measured on text

| Source | Finding | Status |
|---|---|---|
| Schneider, Beege, Nebel & Rey (2018) — signaling meta-analysis, k = 103, N = 12,201 `[04 §3]`, `[06 §4]` | retention **g+ = 0.53** [0.42, 0.64], transfer **g+ = 0.33** [0.22, 0.43]; **prior knowledge was not a moderator** | Already adjudicated **3-0** in this knowledge base |
| Lorch & Lorch, signaling topic structure | Signals produced recall better organized by topic. Subjects **remembered more topics but recalled less about each accessed topic** ([University of Kentucky record](https://scholars.uky.edu/en/publications/effects-of-signaling-topic-structure-on-text-recall/)) | `QUOTE-CHECKED` |
| Sanchez, Lorch & Lorch (2001), *Contemporary Educational Psychology* 26(3):418–428 | College students, 12-topic expository text. Participants who read the text **with headings** and/or received mental-outline training remembered topics and their organization better ([PubMed](https://pubmed.ncbi.nlm.nih.gov/11414729/)) | `QUOTE-CHECKED` |
| Lorch et al., headings vs preview sentences ([ScienceDirect](https://www.sciencedirect.com/science/article/pii/S1135755X13700113)) | Memory for subtopics was better with **headings**; no difference between headings and preview sentences on memory for facts. When the task was outlining, signals beat no signals, but previews and headings did not reliably differ. Previews "do not elicit readers' attention to topic information as readily as headings do" | `QUOTE-CHECKED` |
| Dee-Lucas & Larkin (1995), "Learning From Electronic Texts: Effects of Interactive Overviews for Information Access", *Cognition and Instruction* 13(3):431–468 ([record](https://www.tandfonline.com/doi/abs/10.1207/s1532690xci1303_4)) | Both a structured overview (a hierarchical map) and an unstructured one (a menu-like listing) produced better memory for topics and better breadth of recall than continuous text. **The structured overview was easier to recall and use**; without specific study goals, the unstructured overview produced a more fragmented knowledge structure | `QUOTE-CHECKED` |
| Hartley (2004), "Current findings from research on structured abstracts: an update" ([PDF](https://www.researchgate.net/profile/James-Hartley-4/publication/8464870_Current_findings_from_research_on_structured_abstracts_an_update/links/54a1387a0cf257a6360263a6/Current-findings-from-research-on-structured-abstracts-an-update.pdf)) | Structured abstracts were more informative, more readable and judged clearer, and **significantly longer**. **His own limits:** no search-speed advantage in the realistic MEDLINE comparisons; no recall advantage once length and readability were equated; no whole-article studies. | `QUOTE-CHECKED` at review level; the reviewer is the format's principal advocate. A later third-party overview of the programme is [Zhang & Liu 2011](https://journals.sagepub.com/doi/10.1177/0165551511420217) — **a different document, not Hartley's review** |

**Read these together and the operational rule is narrower than "add headings".**

- Headings are the strongest lever available in written text, and the signaling meta-analysis is the one instructional support in this knowledge base where **prior knowledge was not identified as a moderator**. A non-detection is not a proof of no harm; it is the best reason available to signpost for everyone.
- A heading beats a preview sentence at *capturing attention to structure*. When the reader is already attending to structure, they are equivalent. So: use a heading rather than relying on a lead sentence to do a heading's job.
- **Signaling redistributes recall, it does not only add to it.** More topics reached, less retained per topic. For a reference document that is the right trade. For a document whose one idea must land deeply, it is not obviously the right trade, and no source here resolves which case you are in.
- A structured overview beats a flat list of links.
- Per-section framing costs length. Hartley's structured abstracts were longer and were still judged more informative and clearer — but that is **not** a licence for per-section framing in a document. Different genre, and the review's own limits cut against the easy reading: no search-speed advantage in the realistic MEDLINE comparisons, no recall advantage once length and readability were equated, and no whole-article studies at all. Treat "a per-section frame is worth its length" as `INFERENCE`, untested.

### 3.3 The reverse cohesion effect — Rule Zero, for text

McNamara, Kintsch, Songer & Kintsch (1996), "Are Good Texts Always Better? Interactions of Text Coherence, Background Knowledge, and Levels of Understanding in Learning from Text", *Cognition and Instruction* 14(1):1–43 ([JSTOR](https://www.jstor.org/stable/3233687), `QUOTE-CHECKED`).

Experiment 2 orthogonally varied local and global coherence of a science text. The result: **readers who knew little about the domain benefited from a coherent text; high-knowledge readers benefited from a *minimally* coherent one.**

**The outcome distinction is the finding, not decoration.** The title's question turns on *levels of understanding*: the advantage for high-knowledge readers appears on the deeper measures of understanding, not uniformly on recalling what the text said. Collapsing this into "experts learn more from worse text" loses the result.

**The mechanism is the authors' interpretation.** They propose that the gaps force the reader to infer unstated relations, and that this compensatory processing is what produces the deeper understanding. That is their account of why, offered alongside the result — not an independently established mechanism. Say "the authors propose".

This is the written-text sibling of the expertise reversal effect the skill already runs on `[01 §4]`. It says the same thing from the text side: **adding connective scaffolding is not a safe default.**

**Scope, which must not be dropped:** junior-high students; "high knowledge" is relative within that sample; it is an interaction, not a main effect; one text, one domain.

**And the interaction is itself conditional.** O'Reilly & McNamara (2007), "Reversing the reverse cohesion effect: Good texts can be better for strategic, high-knowledge readers", report that **reading skill changes it** — skilled high-knowledge readers benefited from *high* coherence ([record](https://www.researchgate.net/publication/233347242_Reversing_the_Reverse_Cohesion_Effect_Good_Texts_Can_Be_Better_for_Strategic_High-Knowledge_Readers)). So domain knowledge alone is **not** a licence to strip connections. Turn the whole thing into "who is reading decides how much connective tissue to supply" — which is the rule this knowledge base already holds — and not into a rule keyed on expertise.

### 3.4 Links are not free

DeStefano & LeFevre (2007), "Cognitive load in hypertext reading: A review", *Computers in Human Behavior* 23:1616–1641 ([record](https://www.semanticscholar.org/paper/200304b3639d5ac8382419099efda8a22b822bd1), `QUOTE-CHECKED`).

The review's conclusion: the added demands of decision-making and visual processing in hypertext impaired reading performance; learning tends to be better with **fewer** links per page; reader differences in working memory capacity and prior knowledge moderate the effect; networked hypertext structures impair navigation efficiency.

**Operational consequence.** A cross-reference is a cost charged to the reader, not a way of avoiding writing a sentence. A document that cannot be used without following six links is a worse document than one that states the two facts inline. **Counterweight:** this is a review, not a pooled estimate, and it predates modern documentation tooling. Do not turn it into a link budget.

---

## Part 4 — The medium, and what the author cannot check

### 4.1 Documents are read on screens, and that is measurably worse

Delgado, Vargas, Ackerman & Salmerón (2018), "Don't throw away your printed books: A meta-analysis on the effects of reading media on reading comprehension", *Educational Research Review* ([author PDF](https://www.uv.es/lasalgon/papers/Delgado%202018%20dont%20throw%20away%20your%20printed%20books.pdf), `QUOTE-CHECKED` — read from the primary manuscript).

Abstract, verbatim on the numbers:

> "We included studies with between-participant (*n* = 38) and within-participant designs (*n* = 16) involving 171,055 participants. Both designs yielded the same advantage of paper over digital reading (Hedge's *g* = -.21; *d<sub>c</sub>* = -.21). Analyses revealed three significant moderators: (1) time frame: the paper-based reading advantage increased in time-constrained reading compared to self-paced reading; (2) text genre: the paper-based reading advantage was consistent across studies using informational texts, or a mix of informational and narrative texts, but not on those using only narrative texts; (3) publication year: the advantage of paper-based reading increased over the years."

Read the moderators exactly. Screen-versus-paper is the **comparison**, not a moderator. The three moderators are time frame, text genre and **publication year** — and the year trend is over studies published **2000–2017**, which is a fact about that literature, not a forecast about documentation use now.

`INFERENCE` — technical documentation is informational text, and is often read on a screen under time pressure, so two of the three moderator conditions plausibly apply to it. **Delgado et al. did not test that joint case**, and separate moderator findings do not establish a combined effect. Do not call it a documented worst case.

**What this does and does not license.** It does not license telling anyone to print the document — the medium is almost never the writer's choice. What it licenses is a refusal: **do not assume the reader has the attention budget a calm linear reader would have.** That structure is the remedy is also an inference; the meta-analysis did not test it. And its own scope is study texts and reading-comprehension tests, not runbooks.

### 4.2 The author cannot certify the document. The author can inspect it.

This knowledge base's strongest rule is that clarity is not self-observable `[02]`, and that the valid check makes the *receiver* produce something `[08]`. A document has no receiver present. Three things follow, and the third is the one usually got wrong.

**(1) An author's reread cannot establish that a reader understood.** Newton's tappers predicted ~50% and the true rate was 3 in 120 `[02 §1]`; incentives and feedback do not repair it `[02 §2]`. An LLM reviewing its own draft is not a naive audience `[10 R1 Boundary]`.

**(2) The effect sizes for self-explanation and teach-back do not transfer to certifying a draft.** Self-explanation is **g = 0.55, 95% CI 0.45–0.65, k = 69, N = 5,917** `[08 §4]` — the effect of an *intervention on a learner's learning*. Teach-back's "19 of 20 studies, 9 RCTs" `[08 §5]` spans heterogeneous outcomes including adherence and readmissions. **Neither number says anything about whether a given document is comprehensible**, and quoting them as though they license a clarity verdict is precisely the overreach pattern this knowledge base was built to catch.

**(3) A reread is nevertheless useful — for a different question.** It cannot tell you whether a reader will understand. It can find a term used before it was introduced, a referent with no antecedent, a step whose precondition appears later, a promise the body never delivers, and a claim contradicted elsewhere in the same document. Those are properties of the text, checkable without a reader. Calling that inspection a comprehension check is the error; refusing to do it because it is not a comprehension check is the opposite error.

### 4.3 The real check exists, and the author is the one who can run it

Schriver's protocol-aided revision is the plain-language field's own answer ([Schriver, *Plain Language for Expert or Lay Audiences: Designing Text Using Protocol-Aided Revision*](https://www.karenschriverassociates.com/wp-content/uploads/2020/03/12-Schriver-Plain-language-for-experts-or-lay-audiences-Designing-w-Protocol-aided-Revision.pdf), `QUOTE-CHECKED`).

Verbatim from the paper:

> "protocol-aided revision—a procedure which employs readers' responses to texts to guide revision activity—and demonstrates why actual reader feedback is the most sensible and effective criterion for deciding whether a text is written in plain language."

> "Protocol-aided revision is a method for helping writers see problems in text that they might otherwise miss."

Practicalities, in her words:

> "In practice, document designers at the Communications Design Center have found that five participants per cycle has proved a useful number in conducting protocol-aided revision."

> "A rough rule of thumb is that the first pass finds about half of the reader's problems, the second pass half of the remaining problems, and so on. Most documents can be revised to meet the reader's needs in two or three cycles."

And the scoping sentence that stops this being read as an experiment:

> "the goal in recruiting participants is to gather a variety of responses to the text rather than to ensure statistical reliability. It is important not to confuse protocol-aided revision with an experiment— its goal is neither hypothesis testing nor verification."

**Note the labels are the author's own.** "A rough rule of thumb" is a heuristic by the source's own admission, and the five-participant figure is reported practice at one center, not a measured optimum. Quote them as such.

Related, and distinct: Schriver (1992), "Teaching Writers to Anticipate Readers' Needs: A Classroom-Evaluated Pedagogy", *Written Communication* 9(2):179–208 — an intervention that trained writers using real readers' think-aloud transcripts. The full text was not retrievable in this session, so **no number from it is quoted here.** It is listed because it is the right next source, not because it has been checked.

**What an assistant may therefore do, and what it may never claim.**

| May do | May never claim |
|---|---|
| Inspect the artifact against a named reader and task, and report concrete corrections | That the inspection is a comprehension test |
| Say what was checked and what was not: "checked prerequisites, terminology and references; reader comprehension has not been tested" | That a reread, a fresh model context, or a simulated novice constitutes reader testing |
| Prepare a small reader test for the author to run — naming the reader, a realistic task, the materials they may use, and what a successful response would look like | That preparing a test is the same as administering it |
| Note that the requester approved the draft | That the requester's approval represents the downstream audience, unless that relationship was established |
| — | That the average effect sizes above predict this document's improvement |

**Finishing a document with reader comprehension unverified is a legitimate, complete outcome.** It is the normal one. What is not legitimate is reporting a clarity verdict that no instrument produced.

---

## Part 5 — Things that look like clarity levers and are not

### 5.1 Highlighting and rereading

Dunlosky, Rawson, Marsh, Nathan & Willingham (2013), "Improving Students' Learning With Effective Learning Techniques", *Psychological Science in the Public Interest* 14(1):4–58 ([PSPI](https://journals.sagepub.com/doi/abs/10.1177/1529100612453266), `QUOTE-CHECKED` at the level of the utility ratings).

Five of the ten techniques reviewed were rated **LOW utility**, including **highlighting and rereading** (with summarization, the keyword mnemonic, and imagery for text learning).

**Read the unit of analysis before using this.** Dunlosky et al. rate **study techniques a learner applies to material** — a student running a highlighter over a textbook. It is **not** a study of an author's typographic emphasis, and it cannot be cited to show that an author's bolding is ineffective. The review itself discusses memory benefits for material marked by experimenters, which is closer to the authoring case and points the other way.

**What it does support, stated narrowly:** if someone asks whether highlighting is a good way to *study*, the answer is that it is rated low utility. That is the claim. `HEURISTIC` is the right label for any advice about an author's emphasis — nothing in this knowledge base measures it.

**Keep the distinction that does have evidence.** Signaling `[04 §3]` is cues that reveal *organization*: headings, enumeration, explicit "three things; here is the first". That is what carries g+ = 0.53. Emphasis scattered through prose is a different thing and is simply untested here — not disproven, untested.

**One note on the review's own scale, since it is easy to misread.** The same review rates **self-explanation MODERATE**. That is a *utility* rating, which folds in generalizability across materials and learners, durability, and ease of implementation. It is **not** a competing effect-size estimate and does not contradict Bisra et al.'s g = 0.55 `[08 §4]`. The two can both be true; cite each for what it measures.

### 5.2 Making the text harder does not make it stick

The disfluency claim — Diemand-Yauman, Oppenheimer & Vaughan (2011), that a harder-to-read font improves retention as a "desirable difficulty" — has largely failed to replicate.

- Taylor et al. (2020), "Disfluent difficulties are not desirable difficulties: the (lack of) effect of Sans Forgetica on memory", *Memory* 28(7): across four experiments, subjects rated the font harder to read, and memory was **equivalent or worse** ([Taylor & Francis](https://www.tandfonline.com/doi/full/10.1080/09658211.2020.1758726)).
- Wetzler, Pyke & Werner (2021), "Sans Forgetica is Not the 'Font' of Knowledge", *SAGE Open* ([article](https://journals.sagepub.com/doi/full/10.1177/21582440211056624)).
- Huff, Maxwell & Mitchell (2022), "Distinctive Sans Forgetica font does not benefit memory accuracy in the DRM paradigm", *Cognitive Research: Principles and Implications* — four experiments, ~300 participants, no effect on correct or false memory versus Arial ([article](https://link.springer.com/article/10.1186/s41235-022-00448-9)).
- A meta-analysis (Xie, Zhou & Liu, 2018) reports that perceptual disfluency produced no effect on later recall relative to undistorted controls. **Carry its own correction:** Weissgerber, Brunmair & Rummer published a reanalysis identifying sign and coding errors and questioning the recall and moderator results, while finding the transfer results comparatively robust ([reanalysis](https://pmc.ncbi.nlm.nih.gov/articles/PMC7854329/)). Do not report that recall null as settled.

`QUOTE-CHECKED` at the level of the replication outcomes.

**State this at the right width.** The Sans Forgetica results are about **one font**, and they are consistent and clear: harder to read, no memory benefit, sometimes a cost. They do **not** establish that every perceptual-disfluency manipulation fails, and the meta-analysis that would have generalized them has a published reanalysis against it. The honest summary is **inconsistent evidence, with no support for the popular version of the claim.**

**Consequence, unchanged:** do not add difficult formatting as a default. If a document is hard, treat that as a cost. (And keep the boundary with §3.3: McNamara's effect is about *conceptual gaps for a knowledgeable reader*, not *perceptual difficulty*. Different claims, different literatures.)

### 5.3 Text-structure instruction is not evidence that you should structure your document

Hebert, Bohaty, Nelson & Brown (2016), "The effects of text structure instruction on expository reading comprehension: A meta-analysis", *Journal of Educational Psychology* 108(5):609–629 ([preprint PDF](https://files.eric.ed.gov/fulltext/ED648909.pdf), `QUOTE-CHECKED`).

Abstract, verbatim in the relevant part:

> "In this meta-analysis of 45 studies involving students in grades 2 - 12, the authors present evidence on the effects of text structure instruction on the expository reading comprehension of students... Overall, the results indicated that text structure instruction improves expository reading comprehension, but the effects were tempered when text structure instruction was compared to stronger comparison groups."

**Read the intervention carefully. This is training the reader, not structuring the text.** It is strong evidence that text structure is something readers use and can be taught to use. It is **not** evidence that adding structure to a document improves comprehension — that claim belongs to the signaling meta-analysis `[04 §3]`, which manipulated the text.

It is listed here because it is the citation most likely to be grabbed for the wrong rule. Note also its own hedge: the effects shrank against stronger comparison conditions.

### 5.4 The measurement rules from `07` all still apply

Nothing in this document creates an exception to the prohibitions in `07-plain-language-and-writing.md`. Restated because a writing mode is exactly where they get broken:

- **No readability score is a target or proof of clarity** — not Flesch-Kincaid, not Lexile, not a grade level, not an LLM asked how readable something is `[07 §2]`.
- **Word counts, syllable counts, and "one idea per sentence" are English artifacts** and are not segmentation targets in any language `[07 §1.6]`.
- **Surprisal locates, it never prescribes** `[07 §3.1]`. Newly noted, not adjudicated: Černý, Kvapilíková & Cinková (2026), "Glitter: Visualizing Lexical Surprisal for Readability in Administrative Texts" ([arXiv 2601.05411](https://arxiv.org/abs/2601.05411)) builds a visualization of per-token surprisal over bureaucratic text. **It is not corroboration that high surprisal finds hard passages** — the paper itself raises the opposite failure mode, that legal boilerplate can be *low*-surprisal to a model and still hard for a reader, because model predictability and reader knowledge are different things. An unrefereed preprint and a tool paper: it shows a visualization, not a validated difficulty detector, and it adds no warrant for using surprisal as a rewrite target.

### 5.5 Non-English writing guidance: an absence, reported

A search for an empirical base comparable to the FPLG/Kimble literature in Korean returned policy infrastructure — the National Institute of Korean Language's public-language programme, and Korean-language policy scholarship — but no body of controlled revision studies of the kind Kimble collected for English.

**What this search did not find is the finding — and it is a statement about this search, not about the field.** It is not evidence that no such literature exists, in Korean or in any other language; one search that came up empty establishes only that.

It is nevertheless a reason this knowledge base stays language-neutral rather than translating English rules. `INFERENCE`, and it should be read as one: the processing-order argument is assumed to transfer — frame before the details a reader meets, name a term before its first working use, make organization visible — because it is about knowledge structure rather than about English. **That transfer has not been tested here for any of these writing rules.** What certainly does *not* transfer is any surface prescription — sentence length, word count, clause structure — because those were derived from and validated on English.

---

## What this does NOT license

1. **Do not quote anything *new* in this document as adversarially verified.** No claim originating here carries a `3-0`. It is single-pass quote-checking, which is weaker, and the difference is roughly a 38% historical refutation rate. Findings cited from documents 01–12 keep their own verdicts; the writing applications built on them do not inherit those verdicts.
2. **Do not attribute a bundled result to one rule.** Kimble's documents and Carroll's manual were changed along several dimensions at once. "The failure-to-understand rate fell from 56% to 11%" is a fact about a rewrite; it is not a fact about any sentence-level rule — and note it is a failure rate, so lower is better.
3. **Do not say "a late frame is worse than no frame."** The Topic-After scores were numerically lower and that contrast was never tested. Say **"no advantage was observed for a late frame here"** — and note the comprehension measure was a subjective rating. An untested contrast establishes neither harm nor equivalence.
4. **Do not say Bransford & Johnson show you should repeat the frame in every section.** They tested linear reading of one passage. Section-level framing is an `INFERENCE` and must be labelled.
5. **Do not turn signaling into emphasis.** Headings and enumeration reveal organization; bolding inside prose does not, and is untested here. Do not settle it with Dunlosky et al.'s LOW rating for highlighting — that rates a learner's study technique, not an author's typography (§5.1).
6. **Do not cite Hebert et al. for "structure your document."** That meta-analysis taught readers to use structure; it did not manipulate the text.
7. **Do not claim a document has been verified as clear.** No instrument available to an assistant produces that verdict. State what was inspected, and state that reader comprehension was not tested.
8. **Do not claim preparing a reader test is running one.** And do not treat a fresh model context, a "novice persona", or the requester's approval as a reader.
9. **Do not tell anyone to print it.** The screen finding is a reason to lean harder on structure, not a medium recommendation, and the medium is rarely the writer's choice.
10. **Do not make the text harder on purpose.** Perceptual disfluency did not replicate. McNamara's reverse cohesion effect is about conceptual gaps for a knowledgeable reader, and is an interaction in one study with junior-high students.
11. **Do not read "self-sufficient" as "inline everything."** It means sufficient for the stated reader and task, with prerequisites named. A linked issue the reader can open is a legitimate dependency; a conversation they were not in is not.
12. **Do not treat all asynchronous artifacts as one case.** An archival commit message and a live PR description have different readers and different repair channels.
13. **Do not present the self-explanation g = 0.55 as uncontested.** Dunlosky et al. rate the same technique MODERATE utility. Both assessments are in the record.
