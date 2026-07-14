# easy-speak (plugin)

Makes Claude explain things so you actually understand them. Language-neutral.

Full documentation, install instructions, and the research behind it: **https://github.com/kimkimsh/easy_speak**

## Contents

| Component | Path | Purpose |
|---|---|---|
| Slash command | `commands/easy-speak.md` | `/easy-speak` — mode on, one-shot explain, or off |
| Skill | `skills/easy-speak/SKILL.md` | The operational loop. Auto-activates on "I don't understand", "explain simply", etc. |
| Reference | `references/audience-calibration.md` | How much to explain, and why over-explaining hurts experts |
| Reference | `references/building-explanations.md` | Analogies, examples, jargon, signposting |
| Reference | `references/comprehension-checks.md` | Verifying understanding instead of assuming it |
| Reference | `references/never-say-this.md` | Communication claims that died under verification |

References are loaded on demand, not up front.

## The loop

1. **Fix the audience** — there is no audience-independent simple version of anything, and over-explaining measurably degrades an expert's performance (d = −0.428).
2. **Frame before detail** — one sentence naming the topic, *first*. A frame delivered late is worth nothing.
3. **Build the explanation** — analogies must map relations, not looks. Two examples, not one.
4. **Make structure visible** — signposting is the one support that does not backfire on experts.
5. **Verify, if it matters** — never "does that make sense?". Make them produce something back.

## Install

```bash
/plugin marketplace add kimkimsh/easy_speak
/plugin install easy-speak@easy-speak
```

## License

MIT
