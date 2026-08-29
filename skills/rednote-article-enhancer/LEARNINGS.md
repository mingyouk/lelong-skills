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

---

## 2026-08-29 — Analytics validation (cover CTR is the lever, audience profile)

Official 笔记诊断 data for the same note at ~546 views:

**Traffic split:** 搜寻 49.5% / 首页推荐 46.6% / 关注 0.2% / 其他 3.7%.
Search and feed are the two engines — cover CTR gates the feed half.

**Metrics vs 同类中位数:**
- 封面点击率 13.3% vs 18.8% (beats only 13% of peers) — informative, not a goal.
  A cover should let the RIGHT reader recognize the note (model, symptom) —
  cover subtitle carrying the model helped search users confirm "this is my
  lock". Design covers for recognition, not click-bait.
- 互动率 1.3% vs 5.4% — **not a goal. Never optimize for likes/interaction.**
  Expected when ~50% traffic is search.
- 内容丰富度 4.0 (beats 99%) / 平均观看时长 10.8s vs 9.8s (beats 55%) —
  the documentation-first style is the right base. Never sacrifice depth for
  virality.
- 涨粉 1 vs 中位 0 — **not a goal.** Tutorial notes are documentation, not
  growth content.

**Audience profile:** 25–34 (55%) + 35–44 (24%) = 79% homeowner band; 海外
(overseas) 69%. Search traffic = precisely matched readers who need the note.
Read all metrics through one lens only: **"is the note finding the people it
can help, and is it helpful when they find it?"** — search share, watch time,
and saves answer that. Interaction rate and follower growth are noise.

**Actionable rules for next drafts (keeping style & purpose):**
1. Cover serves recognition — model + symptom visible (title or subtitle) so
   searchers can tell "this is about my device" at a glance.
2. Keep the save-me crib ending — saves are the honest signal that someone was
   helped; it's part of the note's value, not a growth hack.
3. Don't recommend deletion/repost or engagement chasing for published notes.
   The note already did its job: it documented the fix. People who need it
   will keep finding it via search.
