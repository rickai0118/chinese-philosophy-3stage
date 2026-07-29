# Changelog

## v7.1 (2026-07-29) — SOTA publication release

**Status**: Released publicly. darwin 9-dim score **88.5/100** (SOTA threshold).

### Added
- `references/quotes-en.md` — 22 canonical English translations covering all four classics (道德经 9 / 论语 6 / 孙子兵法 4 / 周易 3)
- `references/quotes-en-candidates.md` — Translator selection process (D.C. Lau, Arthur Waley, Thomas Cleary, Richard Wilhelm as canonical authorities)
- `examples-en.md` — Full English worked examples mirroring `examples.md`
- R6.5 金句四档协议 (确信档 / 模糊档 / 无金句档 / 英文档) for quote verification
- R6.5.4.5 **语言匹配硬规则** — Chinese question → Chinese quotes; English question → English translations with translator attribution
- 🔴 **Red-line check** — pauses for mental-health crisis / legal exposure / major financial risk signals
- 🚫 **反例与黑名单** — R1-R10 anti-patterns with "why forbidden + correct alternative" pairs
- **失败兜底** — 5 explicit failure branches (trigger conflict, missing stage, quote uncertainty, user interruption, scope overflow)
- 11-item self-check protocol (R1-R11)

### Changed
- 触发钩子 — automatic Confucian-precedence when ethical subjects appear (Chinese or English)
- 场景调用优先级 — life decisions → 道德→儒家→兵家; power struggles → 兵家→道→儒; creative writing → parallel
- 11 English ethical trigger words added (family / parents / guilt / being there / responsibility / obligation / I owe / I should / at peace / children / spouse)

### Quality metrics
- 6 independent judge reviews using darwin 9-dimension rubric
- 3 dimensions at full marks (10/10): failure-mode encoding, actionable specificity, anti-pattern blacklist
- 4 language tests passed: Chinese question → Chinese quotes, English question → English quotes, bilingual request → bilingual format, mental-health crisis → red-line interception

---

## v6 (2026-07-29) — Bug fix pass

- Fixed `quotes-en.md` header count mismatch (孙子 header was "3 句" but actually 4)
- Added cross-link in SKILL.md from R6.5 英文档 to `references/quotes-en.md`

## v5 (2026-07-29) — Full internationalization

- 22-quote canonical translation library (finalized)
- English worked examples
- English description in frontmatter
- English ethical trigger words

## v4 (2026-07-29) — English quote protocol

- R6.5 第四档 (English tier) — explicit translator attribution, publisher, year

## v3 (2026-07-29) — Anti-hallucination

- R6.5 三档协议 — 确信 / 模糊 / 无金句 — prevents quote fabrication

## v2 (2026-07-29) — Safety & robustness

- P0: 🔴 Red-line check for crisis inputs
- P1: 失败兜底 (failure recovery)
- P2: 🚫 反例与黑名单 (anti-pattern blacklist)

## v1 (2026-07-29) — Initial release

- Three-stage reasoning: Daoist → Military → Confucian
- Worked example: life decision
- Trigger logic: scenario-based order switching

---

## Design philosophy

The skill was built iteratively with **adversarial review**. Each version was scored on 9 dimensions (structure + effectiveness + meta-skill blacklists) by independent judge agents. Improvements were accepted only when they strictly raised the score.

The goal was not maximum score — it was **safety + rigor + non-trivial insight**. The skill exists to give honest multi-perspective analysis, not reassurance.

Source: Created with Claude (Anthropic) under MIT license.