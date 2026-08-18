# Trigger Evals

Test whether the skill activates for the right inputs.

**How to test:** Paste the prompt into a fresh Claude Code conversation. The skill
should load (visible as "Loading rednote-article-enhancer…" or auto-triggering
the workflow). If the skill loads for a negative case, or doesn't load for a
positive case, the description needs adjustment.

---

## Positive (should trigger)

| # | Prompt | Notes |
|---|--------|-------|
| 1 | 帮我改进这篇小红书文章 + paste article text | Direct enhancement request |
| 2 | review my rednote post + paste URL | English trigger with URL |
| 3 | 帮我改一下这篇XHS笔记 + paste text | Shortened trigger phrase |
| 4 | improve this post + paste text | Short English trigger |
| 5 | 帮我看看这篇写得怎么样 + paste text | Borderline — asks for review |
| 6 | 帮我review这篇小红书 + paste text | Code-switching trigger |
| 7 | paste a rednote.com URL by itself | URL-only trigger (no explicit "review") |

---

## Negative (should NOT trigger)

| # | Prompt | Why |
|---|--------|-----|
| 1 | 帮我写一篇小红书帖子 | New article, not enhancement |
| 2 | 帮我分析小红书上的热门趋势 | Trend analysis, not article review |
| 3 | translate this post to English | Translation, outside scope |
| 4 | 帮我做小红书封面设计 | Design task |
| 5 | 帮我查一下重庆旅游攻略 | Information research |
| 6 | 这篇小红书文章的数据怎么样 | Analytics, not content review |
| 7 | write a new post about my trip to Japan | New article creation |
| 8 | 帮我总结这篇小红书 | Summarization ≠ enhancement |
