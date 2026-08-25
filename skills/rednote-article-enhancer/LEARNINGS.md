# Learnings & Evolution Log

Captures feedback from real usage to inform future revisions of this skill.
When the skill gets something wrong — formatting, trigger boundary, rule
misapplication — log it here so the next revision can fix it.

## How to use

After a session where the skill was used:
- Log what went wrong (or what could be better)
- Reference the specific rule or section if applicable
- Propose a fix for next revision

---

## 2026-06-17 — Skill revision v2

Applied Anthropic principles (gotchas-only, trigger boundary description, soften
rigid instructions). Created evals and changelog. Initial log entry.

### Known gaps to observe
- [ ] Does the new trigger boundary description prevent false loads?
- [ ] Is the softened workflow still providing enough guardrails?
- [ ] Are there any gotchas missing from the formatting rules?

---

## 2026-08-25 — Learnings from Philips EasyKey note (model-in-title, evidence pairs)

Field-tested on a tech-fix note (Philips EasyKey AlphaWM-5HB weekend dropout).
Post-24h: 189 views → 424 views over a week, saves≈likes (3:4) — typical
long-tail search pattern for a niche how-to. Insights to carry into future drafts:

1. **Model name = search entry** — Self-invented title phrasing ("掉线自救") gets
   outranked by symptom searches ("EasyKey 掉线", "门锁网关失联"). If the model
   doesn't fit in the 20-char title, put it in the cover subtitle (worked well:
   cover subtitle carried "AlphaWM-5HB · 周末实测").
2. **Keyword-dense opening line** — First line should pack model + symptom +
   scenario so the search-hit line is the first thing read.
3. **"Save-me" crib at the end** — A copy-pasteable mini-summary (contact,
   version numbers, steps) boosts saves; saves matter more than likes for
   tutorial value. Saves≈likes ratio is the health signal for how-tos.
4. **Before/after evidence pair** — Side-by-side version comparison screenshot
   was the highest-value image. Use for any fix/repair-type note.
5. **24h data ≠ verdict** — Niche how-to notes ride search long-tail; flat
   engagement with growing views is normal (problem-solvers don't like, they
   leave). Don't advise deletion or aggressive re-posting for documentation-
   first posts.
