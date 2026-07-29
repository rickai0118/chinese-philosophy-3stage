# chinese-philosophy-3stage

> A reasoning skill that uses Chinese philosophy (Dao De Jing, Sun Tzu, Confucius, I Ching) to analyze hard decisions and complex situations.

## What it is

`chinese-philosophy-3stage` (a.k.a. **ACPTE-TOD**, 三阶推演法) is a Claude Code skill that applies classical Chinese philosophy as a **structured reasoning framework** for complex problems. It forces every analysis through three sequential lenses before reaching a conclusion:

1. **Daoist (道家)** — Read the *trend*. Where is the situation in its life cycle? Is there a reversal point approaching?
2. **Military (兵家)** — Read the *game*. Who are the players? What's the information asymmetry? What's the radical path vs. the conservative path?
3. **Confucian (儒家)** — Read the *ethic*. Is the strategy aligned with 仁 and 义? What will people feel afterward?

A 4th optional lens — **I Ching (易家)** — adds the time-position reading: *Is this the right moment? Are you in an active or passive position?*

The skill is **engineered for safety**: it cannot give you a hollow "you can do it" pep talk. It cannot pretend psychology is philosophy. When the input signals mental-health crisis, legal exposure, or major financial risk, it stops and points you to professional resources before any analysis begins.

## When to use it

Use `/acpte-tod` (slash command) when you face:

- A **complex decision** with multiple stakeholders and competing values
- A **story design** problem (especially power struggles, reversals, moral dilemmas)
- A **human insight** question about why someone is behaving a certain way
- A moment when you suspect the obvious answer is wrong and want a **multi-perspective pushback**

Do *not* use it for:
- Standard operational decisions (use a checklist)
- Code questions, math, or technical lookup
- Mental health crises (the skill will redirect you to professional resources — but please don't rely on it for that)

## How it works

### Three-stage structure (forced)

Every analysis goes through the three lenses in the order determined by the *type* of problem:

| Scenario | Order |
|---|---|
| Life choices / values | Daoist → Confucian → Military |
| Power struggles / competition | Military → Daoist → Confucian |
| Story design / writing craft | All three in parallel (with yin/yang concepts) |
| Time-spanning / fate questions | + I Ching fourth lens |

### Bilingual

The skill supports **Chinese and English** with the same rigor:
- **Chinese question → Chinese quotes** with plain-language interpretation
- **English question → English translations** from authoritative sources (D.C. Lau, Arthur Waley, Thomas Cleary, Richard Wilhelm) with translator + year attribution
- **Explicit bilingual request** → side-by-side format

It will never silently switch languages — there's a hard rule preventing "Chinese question → English quote" mistakes.

### Safety first

Before any analysis, the skill runs a **red-line check** for:
- Mental-health crisis signals (suicidal ideation, panic attacks, prolonged insomnia)
- Major legal exposure (criminal, divorce, contract disputes)
- Major financial loss (> 50% of stated annual income)

If any of these are present, it pauses and asks you to confirm before continuing. This is non-negotiable.

## Repository structure

```
chinese-philosophy-3stage/
├── SKILL.md          ← the engineering spec (Claude reads this)
├── README.md         ← this file (humans read this)
├── cp3/
│   └── SKILL.md      ← short alias `/cp3` → identical behavior
├── examples.md       ← Chinese-language worked examples
├── examples-en.md    ← English-language worked examples
├── LICENSE           ← MIT
├── CHANGELOG.md      ← v1 → v7 evolution
└── references/
    ├── quotes-en.md  ← 22 canonical English translations
    └── quotes-en-candidates.md  ← translator selection process
```

## Quick start

### For Claude Code users

The skill has two slash commands — pick whichever you prefer:

| Command | Length | Use case |
|---|---|---|
| `/cp3` | 4 chars | Quick invocation, terse prompts |
| `/acpte-tod` | 9 chars | Full name, explicit reference |

Both commands trigger **identical** behavior — `/cp3` is a thin alias to `/acpte-tod`.

```
/cp3 I'm facing a decision about whether to take a higher-paying job that requires relocation.
```

or

```
/acpte-tod I'm facing a decision about whether to take a higher-paying job that requires relocation.
```

The skill will automatically detect:
- Language (Chinese vs. English)
- Scenario type (decision / story / insight)
- Trigger Confucian calibration first if ethical subjects appear
- Apply red-line check if crisis signals are present

### For other AI agents

The skill format follows the Claude Code skill spec. To adapt it:
1. Read `SKILL.md` for the complete reasoning rules
2. Read `examples.md` or `examples-en.md` for format reference
3. Use `references/quotes-en.md` for English quote lookups

## What makes this different from "another AI wisdom bot"

Most AI assistants will give you a single-frame answer to a complex question:
- *"You should X because Y."*

This skill **refuses** to do that. It will give you:
- The tension between paths
- The reversal points you're missing
- The ethical cost you haven't priced in
- The time-position you're in
- The risk that the "winning move" accelerates the fall

It will end with a question, not an answer. Because **the answer is for you to discover** — the skill's job is to show you the landscape clearly enough that you can choose.

## License

MIT — see [LICENSE](LICENSE).

## Origin

Built with Claude (Anthropic) using iterative design + adversarial review (darwin skill 9-dimension rubric, 6 review cycles).