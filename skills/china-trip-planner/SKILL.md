---
name: china-trip-planner
description: >
  Use when planning, reviewing, or updating a multi-city China family trip —
  daily itineraries, hotel selection, restaurant verification, booking/reservation
  logistics, or keeping trip notes in sync across vault/long-form/Google Doc.
  Do NOT load for single-hotel booking with no itinerary context, or for writing
  小红书 articles (use rednote-article-enhancer).
---

# China Trip Planner

Planning methodology for multi-city China family trips, distilled from the 2026
宁绍杭 (Nanjing–Shaoxing–Hangzhou) trip. This skill carries **standards and trap
knowledge only** — no workflow engine, no orchestration.

> v0.1.0 — RED-GREEN passed 2026-08-31 (see evals/results/). Content from real
> trip experience; verdicts recorded in the trip vault.

---

## Core Principles

- **Record-only**: never call anything 定案 / final until the user says so. Present
  options with status labels (已订 / 未排除 / 已排除 / 待确认).
- **Public-transit-first** unless the user opts otherwise (metro/bus/高铁; taxi only
  when tired, tight, or carrying luggage).
- **Confirm parameters once, apply everywhere**: 忌口 (dietary), hotel hard
  standards, budget.
- **Desensitize** anything public: no family @accounts, `[Private]` tags.

---

## Hotel Selection Protocol（老规矩）

### Parameters (confirm once per trip)

Hard standards:
1. ① Bathroom partitions/doors are **not glass** (浴室隔断非玻璃) — applies to the
   partition between the bathroom and the room/bed side, and bathroom doors.
   **Internal shower↔toilet glass (干湿分离) is NOT governed by ①** — it belongs
   to ③ only. (RED eval 2026-08-31: no-skill agents read ① broadly and wrongly
   exclude on internal wet-room glass.)
2. ② The partition between **bathroom/toilet and the bed** is not
   transparent/semi-transparent (浴室厕所与床之间的隔断) — **this is the privacy
   gate, NOT the shower↔toilet partition**
3. ③ Toilet and shower in **separate rooms** (马桶淋浴分间): HARD when 4 people
   share one room; **SOFT preference when 2 people per room** (2 rooms → 2 卫并发
   counts as satisfied)

Preferences: metro convenience, quiet nights (avoid 商圈核心), near gov/hospital.
Breakfast is NOT a factor.

### Screening flow

1. **Identity** — confirm exact branch. Same-brand traps: 君亭湖滨's 4.6 score
   belongs to the 萧山 store; 西子裏「东站店」is 5.1 km from 东站; names lie.
2. **差评 filter first** — hygiene (虫/霉/异味), noise (临街/空调), safety, 前台.
   High 差评率 → exclude outright, no further work.
   - **Cross-platform**: check Tripadvisor + Agoda too — positive-skewed aggregators
     (360地图/trivago/Google) hide the red flags (RED eval 2026-08-31: baseline
     agent saw 360地图 4.7 + trivago 8.x and concluded 保留; real scores were
     TA 3.5 / Agoda 7.2)
   - **Noise red flags (空调噪音大/被迫关机, 临街公交站) are hard exclusions** —
     do NOT rationalize them away as "个体体验差异"; the noise complaints and the
     positive reviews are both real (different floors/rooms), the flag still stands
3. **Bathroom three gates** — check review photos + 房型图:
   - 磨砂 (frosted glass: light passes, no silhouette) = **PASS** (仁和 / 猫的远方
     precedent) — do not re-litigate
   - 「干湿分离」in listings = glass partition inside one room = **NOT compliant**
   - Semi-wall (卫生间墙未到顶) = **pending**, needs confirmation
   - Transparent glass anywhere bed→bathroom sightline = **exclude**
4. **Photo verification** — the main model often lacks vision: spawn a subagent
   with the vision model slot to read bathroom photos. One interior photo cannot
   judge the bed-side partition — cross-check the album for bed↔bathroom angles.
5. **Price** — compare 3-night totals per room config (1 room for 4 vs 2 rooms),
   watch per-occupant pricing on Trip.com.
6. **Output** — 未排除 / 已排除 table (酒店|房型/床|价|浴室|地铁|状态), excluded
   hotels collapsed to a one-line archive with reasons.

### Traps

- 「干湿分离」≠ compliant; glass between shower & toilet is NOT the bed-privacy
  gate
- 磨砂 door **half-open** reveals interior — note it, don't exclude on it
- Hotel branch names mislead (东站/西湖 in name ≠ actual location)
- High platform score (9.6) doesn't clear the bathroom gate — only photos do

---

## Restaurant Verification Protocol

1. **Hygiene red flags first**: search 黑猫投诉 (tousu.sina.com.cn) — food
   poisoning with hospitalization, 馊菜, insects in food, flies = **exclude**
   (小厨娘淮扬菜 case: 急性肠胃炎+肾衰竭住院)
2. **Filter by 忌口** (per-trip param; this trip: no beef, no offal, no duck blood;
   皮肚 unconfirmed)
3. **Location fit**: day + meal slot + transit; prefer the recommended branch when
   one store scores higher (庙东排骨: 老门东店 > 夫子庙店)
4. **New store, no review data** = 到店自核 (verify on arrival), not exclusion
5. Output: 店名｜推荐菜｜位置适配｜卫生核查结果｜忌口备注

---

## Itinerary Construction Rules

- **Ticket-uncertainty → Plan A/B/C** keyed to reservation outcomes (南博 7-day
  lottery pattern); pick on the day, don't pressure-test every hour
- **Museum Mondays**: 南博/中山陵 closed — scheduling 德基 (mall + art) on Monday
  is intentional, not a mistake
- **Metro-annotate** every stop (站名+线路); 黄昏优先 for sunset sights
  (Dec sunset ≈ 17:00, 明孝陵石象路)
- **Meal slots** per day, dietary-filtered, with 备选
- **Luggage**: 动车 luggage limit = 130 cm three-sum; 28" (152–157 cm) over-limit →
  carry-on gamble (enforcement lenient) + 中铁快运 on-the-spot; 高铁急送 is
  same-city only (35 km), NOT cross-city
- **Reservations need a CN mobile number** — virtual CN number or 亲友代约;
  12306 only, never third-party booking apps

---

## Sync Discipline

- **Vault markdown** = live source of truth (update in real time)
- **小红书 long-form** = publish copy; update only at finalize (per Codex opinion),
  not on every working change
- **Google Doc** = family preview; batch-sync before commit (gws batchUpdate/+write)
- Commit → push at session end; keep a handoff file for next session

---

## Pre-trip Confirmation Checklist

千古情 showtime · 宋城 opening · 老爷爷书店 still open · 围炉煮茶 price
(price-sensitive member) · 95572 高铁快运 · 乌篷船 price/capacity · 雷峰塔
winter closing time · 同心楼生煎 open

---

## TODO

- [x] RED-GREEN evals (2026-08-31): Case 1 浴室判读 & Case 2 分店身份 RED 全败 →
      skill 修复 → GREEN 全过；Case 3/4 负例 description 级通过
- [ ] Register in plugin marketplace + bump version
