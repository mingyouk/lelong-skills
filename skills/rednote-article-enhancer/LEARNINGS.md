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

**Audience profile (final, corrected):** 25–34 (55%) + 35–44 (25%) = 80%
homeowner band; female 57%; 海外 (overseas) 65%; interests: 家居家装 12% #1,
生活记录 11%, 科技数码 only 4% — **readers are homeowners, not techies. The
note worked because it's a HOME problem (lock, after-sales), not a tech topic.
Wrap home-tech content in life language; keep data-driven detail as the
"helping" layer, not the identity of the post.** Search traffic = precisely
matched readers who need the note.
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

---

## 2026-08-29 — Cross-note comparison: content type determines traffic path

Second note's 笔记诊断 data (travel note 昆达山+亚庇, 18-image itinerary) vs
the Philips tech-fix note — a controlled comparison of two content types
written with the same skill:

| Metric | Travel note | Tech-fix note | Takeaway |
|---|---|---|---|
| Traffic source | feed 87.7% | search 49.5% | Content type picks its own engine |
| 互动率 | 9.3% (beats 73%) | 1.3% | Travel invites interaction; problem-solving doesn't |
| Avg watch time | 23.1s (beats 90%) | 10.8s | Visual itineraries hold attention longer |
| 内容丰富度 | 5.0 (beats 99%) | 4.0 (beats 99%) | Documentation style scores top on BOTH |
| 涨粉 | 0 | 1 | Both ≈ median 0; follower growth is noise |

**Audience interest overlap (both notes, final):** 生活记录 = 11% on BOTH
notes — the ONLY interest shared across the two different topics. Travel
readers skew 美食 15% / 旅游 9%; home-tech readers skew 家居家装 12%.
**The documentation-style content attracts life-logging content consumers —
that is the audience base. 内容丰富度 99th percentile on both notes and the
11% 生活记录 overlap are the same fact in two views.** Protect the style.

**读者画像 final:** 80% homeowner band, 57% female, overseas 65%; interests
家居家装 12% #1, 生活记录 11%, 科技数码 only 4% — readers are homeowners not
techies; wrap home-tech in life language. 9/03 XHS AI diagnostic (内容深度
AI 诊断): watch 9.0s vs 同类中位 10.5s (超过 ±41% 同类). Its归因 & advice,
aligning with our own analysis:
- 强工具属性 content without visual anchors → reader gets the version number
  and leaves. First image for tool-type notes must lead with the ANSWER
  (关键版本号/联系邮箱), not context.
- Advice we're NOT acting on for live notes (documentation-first: note is
  done once recorded; updates only when new info/problems arise) — but the
  rules are kept for NEXT notes:
  1. 图文解说: annotate screenshots/emails (arrows/notes on 关键版本号,
     联系邮箱) to guide eye and hold attention.
  2. 避坑总结 ending: end tool notes with a 注意事项/避坑总结 para
     (升级前备份数据 / 注意蓝牙连接状态) — adds实用厚度, extends watch.

**Rules for the skill:**
1. **Judge a note by its own content type.** Engagement norms differ by
   category — never compare a how-to's 互动率 to a travel note's, or advise
   fixes based on a metric the format doesn't target.
2. **内容丰富度 is the stable signal.** Both notes hit the 99th percentile —
   the documentation-first style is the skill's core value. Protect it.
3. **Travel/visual notes can still gain from search keywords** (攻略-type
   searches exist) — adding searchable place names to title/desc helps more
   people find the note; that's "helping", not traffic-chasing.
4. Audience tags (海外 98% female 74% for travel; 69% overseas for tech) are
   useful to calibrate future topic choices — not to chase engagement.

---

## 2026-09-03 — Both notes' full XHS AI diagnostic (platform cross-validates methodology)

Ran XHS's built-in AI 笔记诊断 for BOTH notes (all 5 dimensions each).
The platform's diagnostics — their causes AND their advice — confirm our
methodology on nearly every point. That's the strongest external validation
the skill can get (platform AI, not our own analysis):

| Metric | 昆达山 (travel) | Philips (tool) | Platform takeaway |
|---|---|---|---|
| 内容丰富度 | **5.0 / 99%** | **4.0 / 99%** | Both 99th pct — doc-style flagged on BOTH |
| 内容深度 | 23.1s / 88% | 9.0s / 41% | Itinerary slows reading; tool note exits after answer |
| 互动率 | 9.3% / 72% | 1.2% / 9% | Collect/comments/people-photo vs solve-and-leave |
| 封面点击率 | 15.2% / 41% | 13.3% / 11% | Platform: use scenery photo cover for travel; bold/contrast for tool |
| 笔记涨粉 | 0 | 1 | Both independent notes; 人设/系列 is the catch |

**Explicit platform endorsements of the documentation-first style:**
- 昆达山: 「继续保持这种高信息密度的创作风格」 (时间轴+清单 structure praised)
- Philips: 「继续保持这种『提出问题-展示证据-给出结果』的清晰结构」(三图逻辑闭环 praised)
→ Platform AI says KEEP the style for both. That is the strongest signal the
skill's purpose (记录为主) is on the right track.

**Rules added (cross-validated with our earlier rules):**
1. **图片标注 rule confirmed by TWO independent diagnostics** (内容深度 +
   内容丰富度 both建议 箭头/圈注 for tool notes) — already in our rules.
2. **Cover design differs by content type**: tool notes → 识别 (model+symptom
   text); travel notes → 视觉冲击 (scenery photo, title overlay). One rule
   does NOT fit both formats. (This refines the earlier "cover serves
   recognition" rule — that's the tool-note variant.)
3. **互动引导 phrasing**: two independent diagnostics suggest文末互动提问
   ("大家去亚庇最推荐哪家海鲜楼?" / "有遇到类似蓝牙掉线吗?") as the ONLY
   content-level lever for low-engagement tool notes. Optional for doc-first
   style — engagement is not a goal; but for notes where interaction matters,
   a closing question is the cheap, one-line lever.
4. **人设/系列 is the only growth path** (both diagnostics): 强化「智能家居
   避坑 xxx」/「旅行攻略无踩雷」标签 + 关联系列笔记. Not a goal for doc-first,
   but relevant when a series (and the world wants one).

**Note on platform advice vs our principles:** some suggestions conflict with
doc-first style (加个人感悟/人设标签). Evaluate against the core principle,
not the metric: advices that help the note HELD its value (structure, saves,
clarity) → keep. Advices that optimize meta-metrics (涨粉/互动) → optional at
best. Following the principle, not the algorithm.

---

## 2026-08-29 — First-skill-output post-mortem (the 5-second rule)

The FIRST note written with this skill (Tromsø photo-spot guide, GPS
coordinates, published 2026-04) underperformed badly: <100 views after 4+
months, no analytics (platform threshold). Partial metrics received:

- 封面点击率 13.5% — essentially IDENTICAL to the other two notes (13.3%,
  15.2%). Cover was never the problem across all three.
- 平均观看时长 **5 秒** — vs 23.1s (travel) / 10.8s (tech-fix). People clicked
  and left instantly.
- 互动率 4.3% — not bad for the tiny sample; those who stayed found it useful.

**Root cause:** the note's VALUE wasn't visible in the first seconds. An
11-spot GPS guide led with ordinary first photos — readers couldn't tell
"this is a map of where to shoot" within 5 seconds.

**The 5-second rule (new skill rule):**
> 第一张图 = 笔记的开场白。The first image must communicate the note's value
> within 5 seconds. For spot-guides: first image = spot photo + coordinates /
> map overview, not a plain scenic shot. Cover gets the click; image #1 keeps
> the reader. When reviewing drafts, check image #1 through "would a stranger
> know what this note gives them in 5 seconds?"

**Also logged:** this note is the "skill v1 era" baseline. If rewritten with
current skill rules (search words, cover recognition, 5-sec first image) and
re-published, it becomes a natural A/B test of the skill's evolution.

---

## 2026-09-06 — Pre-skill control group calibration (skill ≠ reach)

User's 5 pre-skill notes (2024-05 → 2025-12, written WITHOUT the skill) as a
control group:

| Note | Views | Likes | Saves | 赞率 | 收藏/赞 |
|---|---|---|---|---|---|
| pre #1 | 2,046 | 32 | 25 | 1.6% | 0.78 |
| pre #2 | 5,186 | 44 | 32 | 0.85% | 0.73 |
| pre #3 | 416 | 2 | 0 | 0.48% | — |
| pre #4 | 267 | 9 | 1 | 3.4% | 0.11 |
| pre #5 | 25 | 3 | 0 | —* | — |
| Philips (skill) | 907 | 7 | 4 | 0.77% | 0.57 |
| 昆达山 (skill) | 462 | 11 | 20 | 2.4% | **1.8** |

*too small to read

**Honest calibration — corrects the implicit assumption in the Tromsø
post-mortem that "skill evolution raised the floor":**
1. **Skill ≠ reach.** The two top-viewed notes EVER (2,046 / 5,186) are both
   PRE-skill. Topic + feed luck dominate exposure; methodology has no
   measurable effect on raw views.
2. **Skill ≠ like-rate.** Both eras sit in the same 0.5–3% band.
3. **What the skill demonstrably improves:** platform-verified structure
   quality (内容丰富度 99th pct on both skill notes). The skill raises the
   note's quality CEILING and makes every note hit the bar consistently —
   that IS the documentation-first goal (每篇都达标), not one-hit virality.
4. 昆达山 收藏/赞 1.8 stays the outlier — reference-type content pulls saves
   (pre-skill best was 0.78).
5. By reach metrics every note (any era) sits at/below the 及格 line
   (≈1k views / 100+ likes for 小爆款). The ceiling is TOPIC + no
   系列/人设 stacking — NOT content quality (platform: 99th pct).
   When asked "did the skill improve performance?": honest answer = better
   structure/richness, not reach. Reach is out of the skill's hands.

**When advising on expected outcomes:** never promise views/followers from
skill-based rewriting. Promise: clearer structure, higher 内容丰富度, better
saves pull for reference content, and platform-recognized depth.

---

## 2026-09-07 — The 5,186-view note: decision-comparison content type (第三形态)

Best-performing note EVER (5,186 views / 44 likes / 32 saves, ~15 months):
「在🇸🇬办个🇨🇳电话号码」— SG telecoms compared for getting a China phone
number (CMLink ❌ / CUniq 300GB ❌ / CUniq 500GB ✅). Recovered via user
paste (note is private/hidden — share token dead, not in public profile).

**Why it outperformed everything:**
1. **刚需大题材** — SG Chinese needing a CN number for WeChat/Alipay/travel.
   Audience pool dwarfs the lock-fix niche. (Third confirmation: topic size
   decides reach, not skill.)
2. **❌❌✅ decision structure** — verdict-first comparison, zero homework for
   the reader → "save-and-use" content. Concrete S$ prices make it save-worthy.
3. **Evergreen maintenance** — date disclaimer (截至 2025.10.08) + closing
   "我会持续更新". The note was EDITED over months; updated notes get
   re-distributed by the feed and keep search value for years. ← NEW RULE
   candidate: for data/price/comparison notes, schedule updates and say
   "会持续更新"; freshness keeps the note alive.
4. **@brand mentions** (CMLinkSG/CUniqSG) — pulls brand-side traffic.

**Content-type lineage (important meta-fact):** the skill codified the
user's NATURAL pre-existing style — the 5 "pre-skill" notes already used the
format (date disclaimer, ━━━, 1️⃣, ✅❌) and 玩转🇨🇳 titles literally appear as
examples in the skill's own Title Rules. The skill was reverse-engineered
from a session that analyzed these high-view notes. Skill = formalized user
style, not an imposed one.

**Three high-value forms now documented:**
1. 旅行行程单 (itinerary) — feed-driven, high saves (昆达山 收藏/赞 1.8)
2. 教程/避坑 (how-to/fix) — search long-tail (Philips 907 views and climbing)
3. **决策对比 (decision-comparison)** — evergreen, biggest audience pool
   (电话号码 note 5,186 views) — ❌❌✅ verdicts + concrete prices +
   sustained updates + @brands

**Rules for the skill:**
1. When the topic is a recurring-purchase/service decision (telecom, banking,
   insurance, hotels), suggest the decision-comparison form: ❌❌✅ verdicts,
   concrete prices, date disclaimer, @brand mentions, "会持续更新" closing.
2. For data/price notes, note the date AND a maintenance cue — evergreen
   notes compound search value; a static price note rots.
