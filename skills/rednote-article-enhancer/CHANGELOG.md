# Changelog

All notable changes to this skill are documented here.

## 2026-08-19 — v3

### Changed
- **Description:** Added long-form trigger — rewriting/converting an existing
  article into 长文 (long-form) format; "Do NOT load" boundary unchanged
- **Description:** "Load when" → "Use when" per writing-skills CSO
  (superpowers v5.1.0)

### Added
- **Formatting Rules:** New "Long-form notes（长文）" subsection — when to use
  (>~1000 chars), platform constraints (title ≤20, body ≤6000 incl. spaces,
  partial Markdown, 「一键排版」 image splitting; unverified items flagged
  （未经验证）/（以实际编辑器为准）), `#`/`-` formatting guidance
- **Evals:** Case 6 — long-form trip report (~1500-char input) with a
  long-form-specific checklist

---

## 2026-06-17 — v2

### Changed
- **Description:** Rewrote as trigger boundary ("Load when… / Do NOT load for…")
  per Anthropic/Perplexity guidelines — replaces old keyword list
- **Core Principle:** Trimmed redundancy — kept only what the model wouldn't know
- **Workflow:** Simplified from rigid 5-stage structure to inline numbered list
- **Content Rules:** Merged 3 sub-sections into 3 bullet points
- **Language Rules:** Cut from 5 lines to 2
- **Hashtags:** Cut from 6 lines to 3
- **Article Type Tips:** Removed (model already knows format conventions)
- **Quality Checklist:** Compressed from 5 priority tiers to 2 (Critical + Guidelines)

### Added
- `evals/` directory with trigger and quality test cases

### Removed
- ~90 lines of redundancy and over-instruction (32% file reduction)

---

## Initial — v1

Original skill created for reviewing and enhancing 小红书/RedNote articles.
