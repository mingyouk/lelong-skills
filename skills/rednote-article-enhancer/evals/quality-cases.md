# Quality Evals

Test whether the skill's output follows formatting and content rules.

**How to test:** Invoke the skill with the given input. Check the output against
each item in the checklist. Record pass/fail.

---

## Case 1: Trip report with missing details

**Input:** A draft trip report with no title, long paragraphs, some unverified
price claims, and no hashtags.

```
上周去了重庆，三天两夜，整体体验不错。
第一天去了洪崖洞，门票好像88元（不太确定），人很多但是夜景真的很美。
第二天去了磁器口，买了些火锅底料，推荐桥头牌。
第三天去了李子坝看轻轨穿楼，挺震撼的。
住宿在解放碑附近的民宿，大概300多一晚。
吃饭推荐佩姐火锅，人均150左右，不过排队要很久。
交通建议买轻轨三日票，好像是45元。
```

**Check:**
- [ ] Title ≤20 chars with flag emoji (🇨🇳)
- [ ] Lines flush left (no indentation)
- [ ] Sections separated by `━━━━━━━━━━━━━━`
- [ ] `→` used for options/steps, `·` for bullet points
- [ ] Unverified prices flagged with `（未经验证）`
- [ ] Time-sensitive info noted with date disclaimer
- [ ] Double empty lines between sections, single between list items
- [ ] No decorative emoji (🌸✨🎉 etc.)
- [ ] Header/tip emoji functional only (⚠️📅 etc.)
- [ ] Output in Chinese, English only for brand names ("洪崖洞", "桥头牌", "佩姐火锅")
- [ ] Hashtags at end, relevant, no target count
- [ ] Filler removed, content concise

---

## Case 2: Short post (no dividers needed)

**Input:** A very short post.

```
今天在机场拿到了重庆机场的文创周边，只要关注公众号就可以免费领取。在T3航站楼出发大厅，靠近麦当劳那边。
```

**Check:**
- [ ] No `━━━━━━━━━━━━━━` dividers (short post rule)
- [ ] Title ≤20 chars with flag emoji
- [ ] Just natural text flow, no section break

---

## Case 3: Post with collaborator credits

**Input:** A review post tagging others.

```
周末和 @摄影师小王 合作拍了一组照片，在金沙酒店顶楼无边泳池。
后期修图 @小李
设备的话用iPhone 15 Pro就够用了，人像模式效果很好。
出镜：@小美 @阿强
```

**Check:**
- [ ] Collaborator credits preserved as-is (摄影：/ 后期：/ 出镜： format)
- [ ] No reformatting of @names
- [ ] Title ≤20 chars with flag emoji
- [ ] Short enough to skip dividers? Or formatted as review type?

---

## Case 4: Procedural how-to (numbered steps)

**Input:** A draft how-to guide about Alipay setup.

```
怎么在中国用支付宝
首先下载支付宝app
然后绑定你的国际信用卡
注意有些地方只收现金
有些小店可能不支持外卡
绑定后可以在打车和外卖使用
建议备一些现金以防万一
```

**Check:**
- [ ] Numbered steps with 1️⃣2️⃣3️⃣ emoji (procedural article type)
- [ ] Tips section with ⚠️
- [ ] "以下信息均基于截至 YYYY.MM.DD 的资料" date note at top
- [ ] "请以官网为准" note for rules that may change
- [ ] Title ≤20 chars with flag emoji 🇨🇳

---

## Case 5: Article with ranking / comparisons

**Input:** A draft comparing transport options.

```
重庆有三种交通方式：轻轨、公交和出租车。
轻轨最快最便宜，公交最便宜但是慢，出租车最方便但是贵。
如果要赶飞机，建议坐轻轨或者打车。
```

**Check:**
- [ ] Options presented with `→`, NOT ranked unless user explicitly asked
- [ ] No "best" or "recommended" language unless input requested ranking
- [ ] Neutral presentation: `轻轨 → 适合赶时间；公交 → 最经济；出租车 → 最方便`
