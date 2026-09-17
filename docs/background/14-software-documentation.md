# Software documentation: READMEs, API docs, commit messages, code review

> **What this is.** The empirical software-engineering evidence about the documents developers actually write — what readers of them are trying to do, what is missing from them in the wild, and where the literature stops. This is the domain layer under `13-writing-documents.md`.
> **Evidence base.** Entries **W-13 to W-18** in `11-bibliography.md` — 6 catalogued entries covering 8 papers, since Robillard appears twice (2009, 2011) and Aghajani twice (2019, 2020). Fetched and quote-checked in this session. **None went through the three-verifier adversarial adjudication.** And the tier below that matters more here than anywhere else: most of this literature is *descriptive* — it counts what exists and what practitioners complain about. Almost none of it measures whether a reader understood anything.
> **Load this when.** The artifact is a README, an API reference, a getting-started guide, a commit message, or a PR description.

---

## The standing caveat for this whole document

Read this before using any number below.

Empirical software engineering answers a different question from the psycholinguistics in documents 01–08. Those studies manipulate a text and measure comprehension. These studies **survey developers, mine repositories, and classify artifacts.** They establish what people say they struggle with and what documents currently contain. They do not establish that any writing change improves understanding.

So: a finding here tells you **where to aim**. It does not price the shot. When a rule in this knowledge base cites a source from this document, the warrant for *doing the thing* has to come from document 13 or earlier; what this document supplies is the target.

Tags are as in document 13: `QUOTE-CHECKED` (read in the fetched primary source, one pass), `INFERENCE`, `HEURISTIC`.

---

## 1. What readers of API documentation are actually stuck on

Robillard & DeLine (2011), "A field study of API learning obstacles", *Empirical Software Engineering* 16(6):703–732 ([McGill PDF](https://www.cs.mcgill.ca/~martin/papers/ese2011.pdf), `QUOTE-CHECKED`). The earlier, shorter report is Robillard (2009), "What Makes APIs Hard to Learn? Answers from Developers", *IEEE Software* 26(6) ([McGill PDF](https://www.cs.mcgill.ca/~martin/papers/software2009a.pdf)).

Abstract, excerpted (the ellipsis marks an omitted sentence):

> "We conducted a mixed approach, multi-phased study of the obstacles faced by Microsoft developers learning a wide variety of new APIs. The study involved a combination of surveys and in-person interviews, and collected the opinions and experiences of over 440 professional developers. We found that some of the most severe obstacles faced by developers learning new APIs pertained to the documentation and other learning resources. … Our qualitative analysis elicited five important factors to consider when designing API documentation: documentation of intent; code examples; matching APIs with scenarios; penetrability of the API; and format and presentation."

The five factors, in the paper's order:

1. **Documentation of intent** — what the API is for, and why it is shaped this way.
2. **Code examples** — and the 2009 paper's framing of the problem is specifically the difficulty of finding *credible* usage examples *at the right level of complexity*.
3. **Matching APIs with scenarios** — the reader arrives with a task, not with a class name.
4. **Penetrability of the API** — defined in the paper, quoting Clarke's cognitive dimensions, as "how the API facilitates exploration, analysis, and understanding of its components". Over 18 participants raised penetrability issues; the recurring complaints were inability to reason about performance and unclear error-handling behaviour.
5. **Format and presentation.**

**Note what is on the list at all — the order is not a ranking.** These five came out of qualitative analysis; the paper presents them as factors to consider, not as a severity ordering, and nothing here licenses calling intent "the top obstacle". What the list does establish is that **intent is one of the five**, and it is the one a signature does not carry; a generator emits it only if an author wrote it. The paper's own severity claim is at the category level: the most severe obstacles "pertained to the documentation and other learning resources."

**Limits.** One company. Surveys and interviews, so this is self-reported severity, not measured failure. 2009–2011. No comprehension outcome anywhere in it.

---

## 2. What READMEs contain, and what they are missing

Prana, Treude, Thung, Atapattu & Lo (2019), "Categorizing the Content of GitHub README Files", *Empirical Software Engineering* 24:1296–1327 ([arXiv](https://arxiv.org/abs/1802.06997), `QUOTE-CHECKED`).

Method: manual annotation of **4,226 README sections** from **393 randomly sampled GitHub repositories**, into **eight** categories — *what, why, how, when, who, references, contributions, other*. A multi-label classifier over those categories reached **F1 = 0.746**.

**The sample is narrower than "GitHub READMEs".** It was restricted to English-language `README.md` files of at least 2 KB in software repositories. So it describes that slice, not the population of all README files.

The finding that matters:

> "Information discussing the 'What' and 'How' of a repository is very common, while many README files lack information regarding the purpose and status of a repository."

**Read against the API result above, the two point at the same hole.** Intent is one of the five documentation factors Robillard & DeLine elicited; purpose and status were often absent from the READMEs Prana et al. sampled. Neither study ranks anything, so this is a connection between two descriptive results, not a measured priority.

`INFERENCE` — that pairing is a reasonable reading of two independent descriptive studies. Neither study tested it, and neither measured whether adding a "why" section helps anyone.

**Limits.** Descriptive: it describes what exists in the sampled slice, not what is good. The paper does include a survey of **20 professionals** on the perceived usefulness and findability of its categories — that is **reader-response data, not comprehension data**, and it should be reported as opinion. Published 2019; the preprint is 2018, and neither is the sampling date, which is not quoted here because it was not checked.

---

## 3. Commit messages

Tian, Zhang, Stol, Jiang & Liu (2022), "What Makes a Good Commit Message?", ICSE 2022 ([arXiv 2202.02974](https://arxiv.org/abs/2202.02974), `QUOTE-CHECKED` against the arXiv abstract).

The paper's operational definition is two-part: a good commit message conveys **What** — a summary of the change — and **Why** — the motivation for it.

**The rubric's exceptions are the part that protects short commits, and they get dropped constantly.** The study accepts a message without an explicit Why when the reason is trivial or implicit; accepts a message without an explicit What when the change is readily inferable from the diff; and accepts an issue or PR link that supplies the Why. "States both" is a misquote of "conveys both".

Abstract, verbatim in the load-bearing part:

> "In this multi-method study, we first define what constitutes a 'good' commit message, and then establish what proportion of commit messages lack information using a sample of almost 1,600 messages from five highly active open source projects. We find that an average of circa 44% of messages could be improved... We also observe that prior work has not considered semantics of commit messages, and there is surprisingly little guidance available for writing good commit messages."

**Citation hygiene.** The ICSE conference listing for this paper states **circa 40%**; the arXiv abstract states **circa 44%**. Quote whichever version you actually cite, and say which. Do not average them.

**Limits.** Five projects. "Could be improved" is the authors' rubric applied by annotators, not a measured cost to any reader. The paper has **two** motivations and both matter: it opens from communication between developers and derives its criteria from human-oriented guidance, *and* it is aimed at the quality of training data for automatic commit-message generators. Read the rubric as human-derived and machine-applicable, not as either alone.

**Why this artifact is archival, not conversational.** A commit message encountered through `git log` a year later has no repair channel at all: the author may be gone, the thread may be gone, and there is no one to ask. It sits on the far side of the line in `13 §1.1`, further than a PR description does.

---

## 4. Code review: the reader's problem is *why*, not *what*

Bacchelli & Bird (2013), "Expectations, Outcomes, and Challenges of Modern Code Review", ICSE 2013:712–721 ([Microsoft Research PDF](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/02/ICSE202013-codereview.pdf), `QUOTE-CHECKED`).

Method: observed **17 industrial developers** doing code review across **16 separate product teams**; semi-structured interviews with those developers; surveys of developers and managers; manual classification of **570 comments** inside code reviews.

Abstract, verbatim:

> "Our study reveals that while finding defects remains the main motivation for review, reviews are less about defects than expected and instead provide additional benefits such as knowledge transfer, increased team awareness, and creation of alternative solutions to problems. Moreover, we find that code and change understanding is the key aspect of code reviewing and that developers employ a wide range of mechanisms to meet their understanding needs, most of which are not met by current tools."

From the body, on what reviewers are actually struggling with:

> "Many interviewees eventually acknowledged that understanding is their main challenge when doing code reviews."

> a senior developer: "the most difficult thing when doing a code review is understanding the reason of the change"

> a tester: "the biggest information need in code review: what instigated the change"

**And the counterweight, from the same page — do not drop it.** The paper immediately records that the description often does not solve this:

> "Although the textual description should help reviewers understanding, some developers do not find it useful: 'people can say they are doing one thing, while they are doing many more of them,' or 'the description is not enough;'"

and that "not knowing files (or [dealing with] new ones) is a major reason for not understanding a change."

**What survives.** In the paper's own words, "no other code review challenge emerged as clearly as understanding the submitted change" — and the interview quotes point specifically at **why the change was made** — which a diff may well not carry, since the reason lives outside the code unless someone put it there. That is a reason for a PR description to carry the motivation. It is interview data, not a measured ranking of information needs.

**What does not survive.** "Write a better PR description and reviewers will understand." The paper's own interviewees say descriptions are frequently insufficient, and that unfamiliarity with the files is a major independent cause. A description is one input to understanding, not the mechanism.

**Limits.** One company, 2013, 17 observed developers. Interview and classification data. No measurement of whether a better description improved review outcomes.

---

## 5. What practitioners report as broken

Aghajani, Nagy, Vega-Márquez, Linares-Vásquez, Moreno, Bavota & Lanza (2019), "Software Documentation Issues Unveiled", ICSE 2019:1199–1210 ([record](https://2019.icse-conferences.org/details/icse-2019-Technical-Papers/49/Software-Documentation-Issues-Unveiled), `QUOTE-CHECKED` at the level of method and headline findings), and the follow-up Aghajani et al. (2020), "Software Documentation: The Practitioners' Perspective", ICSE 2020.

The 2019 study mined and classified **878 documentation-related artifacts** from four sources — mailing lists, Stack Overflow, issue trackers and pull requests — producing a taxonomy of **162 documentation issue types**. Its own framing of why it did not survey developers is worth keeping: prior studies relied on surveys, "which naturally leads to a somewhat biased view."

The 2020 follow-up validated the taxonomy through two surveys totalling **146 practitioners** (78 answered the issue-relevance survey, 68 the documentation-types survey). Its abstract states the purpose precisely — to investigate "the documentation issues they perceive as more **relevant**" — and its tables label the column accordingly: "% important" reports "the percentage of surveyed practitioners that indicated the related issue as an important one." That is a separate column from "% frequently faced".

So quote it this way, in the paper's own words, and keep the sentence's scope — it sits inside the discussion of the **Correctness** subcategory, not the whole taxonomy:

> "inappropriate installation instructions was the most frequently encountered issue and, together with faulty tutorial, the one considered relevant by most practitioners (65% of them)."

**Three things to carry with that number.**

1. **It is an importance rating, not a frequency.** The table legend reads: "'% important' reports the percentage of surveyed practitioners that indicated the related issue as an important one", and "% frequently faced" is a separate column. Secondary summaries render the 65% as "65% of practitioners usually *encounter* faulty tutorials" — wrong column.
2. **The denominator is one survey, not 146.** 146 is the combined total across the two surveys; the issue-relevance survey had **78** respondents.
3. **The paper's prose and its figure do not quite agree.** The prose groups installation instructions with faulty tutorials at 65%; Figure 2 lists faulty tutorial at **65%** and inappropriate installation instructions at **63%**. Quote the discrepancy rather than resolving it. And 65% is not unique — missing user documentation, accessibility/findability and lack of time to write documentation all sit there too.

**What this is good for.** A catalogue of failure modes drawn from the wild rather than from intuition, and a reminder of which end of a document breaks first: the part where a reader tries to *start*.

**What it is not.** A taxonomy of complaints is not a taxonomy of measured harm, and issue-tracker mining over-samples the things people bother to file.

---

## 6. Minimalism as the field's practitioner framework

The minimalist approach to documentation — Carroll's, from the IBM work — is the closest thing this area has to a design theory, and its foundational experiment is the one genuinely task-outcome study in this knowledge base (see `13 §2.3`: 40% less learning time, 2.7× subtasks, *t*(17) = 3.06 and *t*(16) = 3.63).

The heuristics practitioners actually use are van der Meij & Carroll's (1995, 1998). Virtaluoto, Suojanen & Isohella (2021), "Minimalism Heuristics Revisited: Developing a Practical Review Tool" ([open copy](https://osuva.uwasa.fi/bitstreams/e96bd3f9-c878-49ae-9cc0-e5774f840bdf/download), `QUOTE-CHECKED`), state of them: "The heuristics, i.e., general principles, are based on solid empirical research, and are intended as a tool for developing documentation." They also observe that the heuristics "do not seem to be applied in everyday practice", and that the context minimalism was designed for — software new to most people, rarely shipping with a tutorial — "is very different" today.

**How to use this.** The four principles from the 1987 paper — focus on real tasks, slash the verbiage, support error recognition and recovery, guided exploration — are worth following, and the first experiment behind them is real. But the heuristics that grew out of them are a **practitioner framework**, and the gap between "the 1987 experiment" and "these 10+ heuristics" is unmeasured. Cite the experiment for the experiment; call the heuristics heuristics.

---

## What this does NOT license

1. **Do not treat anything in this document as a comprehension finding.** Every source here is descriptive, self-reported, or classificatory. The warrant for any writing rule comes from document 13 or earlier.
2. **Do not quote any of it as adversarially verified.** Single-pass quote-checking only.
3. **Do not say "44% of commit messages are bad."** Say: in a sample of almost 1,600 messages from five highly active open-source projects, circa 44% were judged improvable against the authors' What/Why rubric — and note that the conference listing says circa 40%.
4. **Do not say "a good PR description makes reviewers understand the change."** Bacchelli & Bird's own interviewees say descriptions are often not enough, and that unfamiliarity with the files is an independent major cause.
5. **Do not turn the eight README categories into a mandatory template.** Prana et al. classified what exists; they did not test that a README with all eight sections serves anyone better. The defensible reading is narrower: *why* and *status* are the commonly missing ones, and *intent* is one of the five documentation factors named elsewhere.
6. **Do not generalize the API findings past their sample.** One company, self-reported severity, 2009–2011.
7. **Do not cite the minimalism heuristics as experimentally validated.** The 1987 experiment is; the derived heuristic set is a practitioner framework, and its own revisitors note it is largely unapplied in practice and was designed for a different era.
8. **Do not let a documentation-issue taxonomy imply a priority order.** Issue-tracker mining over-samples what gets filed.
