# Changelog

All notable changes to this skill are documented here.

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
