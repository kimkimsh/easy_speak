# Building an explanation

Load this when constructing a real explanation of something hard: choosing an analogy, deciding how many examples to give, deciding what to do with a technical term, or deciding whether to keep a colorful aside.

## 1. The frame, before anything else

One sentence naming what this is *about*. Not what your conclusion is — what the subject is.

Bransford & Johnson gave people a paragraph describing, in perfectly ordinary sentences, a procedure that was impossible to follow without knowing its topic. Adding *"this will be about washing clothes"* — one sentence, before the passage — roughly doubled both comprehension and recall on identical text.

| | Comprehension (max 7) | Recall (max 18) |
|---|---|---|
| No topic | 2.29 | 2.82 |
| Topic **after** the passage | 2.12 | 2.65 |
| Topic **before** the passage | **4.50** | **5.83** |

**The middle row is the finding.** A topic supplied afterwards was *numerically worse than nothing*. Retrospective framing does not repay the debt, because the damage happens during reading: without a topic, the reader cannot compute what any given sentence refers back to. The prose was never the problem.

**Frame ≠ conclusion.** Answer-first (BLUF) is a scanning and triage convention. It has no comprehension evidence behind it, and in the one direct head-to-head, chronological narrative beat the inverted pyramid on both comprehension *and* cognitive load. Lead with your answer when the reader wants to triage. Do not tell yourself it aids understanding.

## 2. Analogy: relations, not resemblance

Gentner's mapping rules are numbered in the source, and the order is the instruction:

1. **Discard attributes of objects.**
2. **Preserve relations between objects.**
3. **Prefer systems of relations.**

> "An analogy is a comparison in which relational predicates, but few or no object attributes, can be mapped from base to target."

### The relational skeleton test

Strip the candidate analogy to its relations — *X does something to Y, which constrains Z*. If nothing survives the strip, it is a **mere appearance match**.

| Candidate | Skeleton | Verdict |
|---|---|---|
| "The atom is like the solar system" | REVOLVES-AROUND(electron, nucleus) ← REVOLVES-AROUND(planet, sun). Discarded: YELLOW(sun), MASSIVE(sun). | Explanatory |
| "A sunflower looks like the sun" | Nothing survives. Round, yellow, radiating — attributes only. | Mere appearance match |

Gentner's own hedge, which you must keep: appearance matches **"can be appealing and locally useful"** — their *explanatory* power is what is sharply limited. A vivid surface match is allowed to be a mnemonic. It is not allowed to be your explanation.

The trap is that a mere appearance match **feels apt**. Your sense of aptness is exactly the instrument the curse of knowledge has broken. Run the test; do not trust the feeling.

### Say the mapping out loud

Do not place the analogy nearby and hope it lands.

| Condition | Solved the structurally-identical problem |
|---|---|
| Analogy read moments earlier, no hint | **~30%** |
| Same analogy, explicit hint to use it | **~75%** |
| No analogy at all (baseline) | ~10% |

People who had just read the analogy mostly failed to reach for it. State the correspondence: *"X plays the role of Y here."*

## 3. Two examples, not one

This is the most concrete, most counterintuitive rule in the set.

Gick & Holyoak tried three separate ways to make a **single** worked example generalize: summarization instructions, an explicit verbal statement of the underlying principle, and a diagram of it.

> "None of these devices achieved a notable degree of sucess [sic]. In contrast, the experiments in Part II demonstrated that if two prior analogs were given, subjects often derived a problem schema as an incidental product of describing the similarities of the analogs."

| Condition (no hint) | Transfer |
|---|---|
| One example | 21% |
| **Two examples** | **45%** |

The schema is induced **as a side effect of comparing two cases** — not by you announcing the principle. Announcing the principle over one example is precisely the intervention that was tested, three ways, and failed.

**Operational rule:** give two examples that *look different* and *work the same*, then say what they share — or better, ask.

## 4. Cut the interesting-but-irrelevant

The vivid tangent is not free. Readers given expository text with interesting-but-irrelevant adjuncts recalled significantly fewer main ideas and produced fewer transfer solutions.

**The workaround does not work.** The instinct is "keep the fun bit, but emphasize the important part harder." That exact fix was tested three ways — highlighting the main ideas, stating learning objectives, and signaling — and **all three failed to reduce the effect**. Only removal helped. If it truly cannot be cut, the only placement with evidence behind it is **the very end** (putting it first made things worse).

The proposed mechanism (the source says *suggest*, so say *proposed*): the tangent primes the wrong schema, and the reader hangs the whole passage on it.

**Keep the rule, drop the drama.** The pooled effect across 39 experiments is small-to-medium (retention d = 0.30; transfer d = 0.48), 11 of 39 studies supported it and 15 did not, there is a failed replication on the same material, and **language moderates the effect size**. Cut the tangent. Do not claim it is catastrophic.

## 5. Jargon

A term the listener does not already own is a **new chunk to carry**, not a free label. That is the whole argument, and it is language-neutral: capacity is over chunks grounded in *their* long-term memory.

What survives from the empirical work, stated narrowly: in one English-language experiment (N = 650), jargon-laden text produced significantly lower **self-reported processing fluency** (η² = .11), and making **hover-to-reveal** definitions available did not restore it.

**Do not overreach on that.** It does not show that "definitions don't help" — what was tested was an optional, opt-in mouseover, and what was measured was how hard the text *felt*, not whether it was understood. An inline plain-wording gloss was never tested.

Practically:

- Prefer the plain wording when the term is not load-bearing.
- When the term *is* load-bearing and they will meet it again, **introduce it explicitly before its first working use.** Do not gloss it in passing and keep going.
- Jargon is audience-relative, not a word list. A term that is jargon to one reader is a free, pre-grounded chunk to another.

## 6. Make the structure visible

Headings, enumeration, explicit signposting. This is the best-evidenced structural lever available:

| Signaling | Effect | 95% CI | k | N |
|---|---|---|---|---|
| Retention | **g+ = 0.53** | 0.42 – 0.64 | 103 studies | 12,201 |
| Transfer | **g+ = 0.33** | 0.22 – 0.43 | 103 studies | 12,201 |

**Prior knowledge was not a moderator.** Unlike almost every other instructional support, signaling does not appear to backfire on experts. Signpost for everyone.

Report retention and transfer as different sizes. Do not quote one number for both.

**Signaling is not emphasis.** What carries the effect is cues that reveal *organization* — headings, enumeration, "three things; here is the first". Bolding phrases inside prose is a different act and is **untested in this knowledge base**, not disproven. Dunlosky et al.'s LOW rating for highlighting does not settle it either: that rates a *learner's* study technique, not an author's typography, and the review notes memory benefits for material marked by experimenters. Treat advice about emphasis as **HEURISTIC**.

**And signaling redistributes as well as adds.** In Lorch & Lorch's signaling experiments, subjects "remembered more topics but recalled less about each accessed topic" when the text carried signals. For a reference document that is the right trade. For a document with one idea that has to land deeply, it is not obviously right, and nothing here tells you which case you are in.

## 7. When it is a document

Everything above still holds. Four things change, because the reader is not there and did not necessarily start at the top.

### 7.1 Scale to the document's job, not to the loop

A commit message does not teach a concept. A spec communicates exact obligations. A reference page is used with the page open. **None of them needs an analogy and two examples**, and manufacturing one is this skill's most familiar failure mode wearing different clothes.

### 7.2 "Before" means before the reader meets the details — INFERENCE

A reader who arrived from a search result never saw your introduction. So at any point where someone can plausibly enter directly, name the subject, the scope that applies, and the prerequisites, before the details that depend on them.

A heading often already does it:

| Fails on direct entry | Works |
|---|---|
| **Recovery** — "Run this after the previous step." | **Recover a replica after a failed upgrade** — "Assumes the upgrade aborted and the replica is in `degraded`." |

**Label it.** Bransford & Johnson tested linear reading of a single passage. They did not test hyperlink entry, independently reachable sections, repeated headings, or the cost of duplicated context. Section-level framing is an inference from their finding, not their finding.

**And it is not "repeat the introduction under every heading."** Some subsections genuinely depend on their parent and can say so. Repetition costs reading time and maintenance, and nothing here measures a benefit that pays for it.

### 7.3 Prefer a heading, and show the shape

- **A heading beats a preview sentence** at drawing attention to topic structure. In Lorch et al.'s comparison, memory for subtopics was better with headings; on memory for facts, and in a task that already forced attention to structure, the two did not reliably differ — and previews "do not elicit readers' attention to topic information as readily as headings do." So do not ask a lead sentence to do a heading's job.
- **A structured overview beats a menu.** Dee-Lucas & Larkin found both overview types beat continuous text on memory for topics and breadth of recall, and the **structured** one (a hierarchical map) was easier to recall and use; the unstructured, menu-like listing produced a more fragmented knowledge structure when readers had no specific goal.
- **Links are a cost charged to the reader.** Learning tends to be better with fewer links per page, and the added decision-making and visual processing impaired reading performance. A cross-reference is not a way of avoiding writing a sentence.
- **Per-section framing makes the document longer, and that can still be worth it.** Hartley's review of ~31 structured-abstract studies found them more informative, more readable, judged clearer, and faster to search — and significantly longer. That is the closest thing here to a licence for the cost, and it is a different genre.

### 7.4 If the document's purpose is *doing*, organize by the task — and write the failure path

Carroll et al.'s Minimal Manual is the one task-outcome experiment in this knowledge base. Its four design principles, in the paper's own words: **focus on real tasks and activities; slash the verbiage; support error recognition and recovery; guided exploration.**

| Measure (Experiment 1) | Result |
|---|---|
| Learning time | **40% less**, *t*(17) = 3.06, *p* < .01 |
| Performance subtasks completed | **2.7×**, *t*(16) = 3.63, *p* < .01 |
| Basic tasks only | **+50%**, *t*(16) = 2.11, *p* = .05 |

**Carry the limits.** n ≈ 19 in Experiment 1; 1987, word processors, paper manuals; and in Experiment 2 the getting-started differences were significant only for time to start the system up. Most importantly, **four principles were varied together** — brevity cannot take the credit alone, and the paper puts error recovery and attention coordination beside it, not beneath it. Replicated with 64 Dutch students by Lazonder & van der Meij (1993).

The half that gets dropped is **error recognition and recovery**. A guide with only the happy path is a guide that abandons the reader exactly when they need it.

### 7.5 Do not make it harder on purpose

The "desirable difficulty" argument for disfluent formatting failed to replicate: across four experiments readers rated the font harder and memory came out **equivalent or worse**, and a meta-analysis found perceptual disfluency produced no recall effect. If a document is hard, that is a cost, not a feature.

(This does not contradict the reverse-cohesion finding in `audience-calibration.md`. McNamara's effect is about *conceptual* gaps a knowledgeable reader can fill — a different claim and a different literature, and itself conditional on reading skill. And state the disfluency result at its real width: the failed replications are about **one font**, and the meta-analysis that would generalize them has a published reanalysis against it. No support for the popular claim; inconsistent evidence underneath.)

## What this does NOT license

1. **"One good example plus a clear statement of the principle is enough."** That is the exact intervention that failed, three ways.
2. **"Put the analogy in and they'll apply it."** ~30% did.
3. **"Mere appearance matches are worthless."** Gentner: they "can be appealing and locally useful." It is their *explanatory* power that is limited.
4. **"Defining jargon doesn't help."** Not shown. One optional-mouseover manipulation, one felt-difficulty measure.
5. **"Concreteness fading is evidence-backed."** It is not. The authors' own words are "*theoretical* benefits" and "we recommend"; a later experiment found constantly-concrete matched or beat fading. You may still say "start concrete, then state the general rule out loud" — as a recommendation, not a finding. If you want a rule with data behind the same goal, use the two-example rule.
6. **"Seductive details are catastrophic."** Small-to-medium, contested, language-moderated. Cut the tangent anyway; the *workaround-failure* is what makes it actionable.
7. **"Working memory holds ~4 things, so give at most 4."** Capacity is over knowledge-relative chunks. Reduce the chunk count *for this audience*; never enforce a magic number.
8. **A readability score as evidence the jargon is gone.** Never a target metric.
9. **"Bransford & Johnson show you should repeat the frame in every section."** They tested linear reading of one passage. Section-level framing is an inference, and "repeat the introduction everywhere" is not even that — it has costs and no measured benefit.
10. **"A late frame is worse than no frame."** Numerically lower (2.12 vs 2.29 comprehension, 2.65 vs 2.82 recall), and that contrast was never tested. Say **"a late frame bought nothing."**
11. **"Signaling means emphasis."** It means cues that reveal organization. Highlighting is rated LOW utility next to rereading.
12. **"Headings always increase recall."** They change its distribution — more topics reached, less retained per topic.
13. **"The Minimal Manual proves shorter is better."** Four principles varied together, n ≈ 19, 1987, and most Experiment 2 differences were not significant. Error recognition and recovery is one of the four, and it is the one people drop.
14. **"Text-structure research proves you should structure your document."** Hebert et al. (2016) taught *readers* to use structure; the text was not the manipulation, and the effect shrank against stronger comparison groups. The rule you want is signaling.
15. **"Make it a bit harder so they engage."** Perceptual disfluency did not replicate — memory equivalent or worse across four experiments, and no recall effect in meta-analysis.
