# easy-speak (plugin)

Makes Claude explain things — and write documents — so people actually understand them. Language-neutral.

Full documentation, install instructions, and the research behind it: **https://github.com/kimkimsh/easy_speak**

## Contents

All paths are relative to this plugin root.

| Component | Path | Purpose |
|---|---|---|
| Slash command | `commands/easy-speak.md` | `/easy-speak` — mode on, one-shot request, or off |
| Skill | `skills/easy-speak/SKILL.md` | The operational loop, plus the artifact rules. Auto-activates on "I don't understand", "explain simply", etc. — **not** on a routine documentation task |
| Reference | `skills/easy-speak/references/audience-calibration.md` | How much to explain, why over-explaining hurts experts, and how to fix an audience you cannot ask |
| Reference | `skills/easy-speak/references/building-explanations.md` | Analogies, examples, jargon, signposting, and what changes when the reader enters part-way through |
| Reference | `skills/easy-speak/references/comprehension-checks.md` | Verifying understanding instead of assuming it — and what to do when there is no receiver at all |
| Reference | `skills/easy-speak/references/never-say-this.md` | Communication claims that died under verification |

References are loaded on demand, not up front.

## The loop

1. **Fix the audience** — there is no audience-independent simple version of anything, and over-explaining is not a safe default: pooled across high-assistance designs, the effect for high-prior-knowledge learners is negative (d = −0.428).
2. **Frame before detail** — one sentence naming the topic, *first*. A frame delivered late bought nothing.
3. **Build the explanation** — analogies must map relations, not looks. Two examples, not one.
4. **Make structure visible** — signposting is the one support where the expertise-reversal pattern was not detected. Signpost for everyone.
5. **Verify, if it matters** — never "does that make sense?". Make them produce something back.

## Answer, or artifact

Cutting across the loop is one question decided per deliverable: can this reader answer back right now?

- **Answer** — they are here. A compact reply that invites repair beats an exhaustive one.
- **Artifact** — a README, design doc, spec, report, guide, commit message or PR description. Nothing may depend on this conversation; sections a reader can enter directly orient before they detail; and **step 5 has no receiver**, so it is replaced by a text inspection plus an explicit statement of what was *not* checked. The skill never claims a document is clear, because no instrument available to it produces that verdict.

The artifact rules apply only while easy-speak is active. It becomes active through `/easy-speak`, through session mode, or through its own automatic trigger — a comprehension complaint ("nobody can follow this README") or a question about the communication research. **Asking for documentation does not switch it on.**

## Install

```bash
/plugin marketplace add kimkimsh/easy_speak
/plugin install easy-speak@easy-speak
```

## License

MIT
