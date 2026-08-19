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

---

## Case 6: Long-form post（长文）

**Input:** ~1500 characters of raw trip notes; user asks to write it as a 长文
long-form post.

```
帮我把这些行程写成一篇小红书长文。

上个月（2026年7月）去了成都四天三夜，回来后朋友一直在问攻略，干脆写成一篇长文分享，方便大家收藏。

【第一天】
中午落地天府机场，在机场随便吃了碗担担面，28元，味道一般，建议到市区再吃。坐地铁18号线进市区，大概40分钟，票价11元左右，可以用天府通刷码进站。下午逛宽窄巷子，人很多，小吃价格偏游客价，看看就好，不建议在里面吃正餐。傍晚去天府广场和人民公园转了转，晚上打车去九眼桥附近的社区老店吃火锅，人均80左右，味道比网红店好太多，排队也不用太久。吃完在九眼桥河边走了走，夜景不错。

【第二天】
一早去成都大熊猫繁育研究基地，一定要赶在8点开门前到，晚了熊猫都在睡觉，只能看到背影。门票55元，不确定今年有没有调价，园区里还有观光车可以坐，10元。看完熊猫，中午去建设路小吃街吃午饭，烤苕皮和糖油果子都不错，很多店要排队，建议一人排一家分工买。下午回市区逛春熙路和太古里，IFS那只爬墙熊猫是必打卡点，太古里有裸眼3D大屏，拍照很出片，两个地方离得很近，步行就能到，太古里偏高端，春熙路接地气一些。晚上去玉林路的小酒馆坐坐，《成都》那首歌里唱的就是这一带，巷子里有很多独立小酒吧，氛围很好。

【第三天】
包车去了都江堰和青城山，包车一天500左右，司机是本地人，一路聊了不少。都江堰门票80元，真的震撼，两千多年前的水利工程到今天还在运行，值得单独留半天慢慢看，建议请个讲解，听完才知道鱼嘴、飞沙堰、宝瓶口各自的作用。青城山前山门票90元，爬上去大概3小时，路上有几个道观可以进去看看，天气好能看到云海，一定要穿运动鞋，山下也有索道可以坐，单程60元。晚上回市区吃了一顿串串，两个人100出头。

【第四天】
上午去人民公园的鹤鸣茶社喝茶，体验成都的慢生活，一碗盖碗茶20-30元，可以坐一整个上午，人多的时候要拼桌，找个阴凉的位置坐下就行。还有采耳师傅在边上揽客，30元一次，挺舒服的。中午去文殊院附近吃了素斋，下午去机场返程。

住宿：住在春熙路附近的地铁站旁边，四天三晚一共700多。一定要选地铁口附近的，成都打车很堵，高峰期地铁反而快。民宿和酒店价格差不多，建议直接选连锁酒店，卫生更有保障。节假日一定要提前订，价格会翻倍。

交通：成都地铁很方便，大部分景点地铁都能到。建议提前在支付宝里开通成都乘车码，或者买天府通卡，比排队买票省时间。天府机场到市区除了地铁还有机场大巴，25元，可以比较一下再选。市区里短途可以骑共享单车，骑行体验很好。打车用滴滴或者高德，高峰期会加价，能地铁就地铁。

美食：火锅、串串、担担面、蛋烘糕、冰粉都值得试。原则就是不要在景区吃，往居民区里走，随便一家小店都不容易踩雷。网红店提前看看排队情况，排队超过一小时就换一家。早上还有豆花和锅盔，早餐可以换着花样吃。

通讯：中国移动有30元左右的短期流量包，机场到达层就能买。小红书、高德地图、大众点评这几个App基本够用，导航用高德比百度准。

预算：机票往返1200左右，住宿700多，门票加交通500左右，吃喝人均一天150左右，四天三晚总花费大概人均2500-3000，丰俭由人。

注意事项：熊猫基地必须早去，周末人更多；都江堰和青城山放在同一天会比较赶，时间充裕的话建议拆成两天；成都很潮，雨季记得带伞；现金基本用不上，支付宝和微信全覆盖；高铁票和熊猫基地门票建议提前一周在App上约好；夏天太阳很晒，防晒霜和帽子要带。
```

**Check:**
- [ ] Output as 长文 long-form — Markdown `#` subheadings or `-` lists, no `━━━━━━━━━━━━━━` dividers
- [ ] Title ≤20 chars with flag emoji (🇨🇳)
- [ ] Body ≤6000 characters (including spaces)
- [ ] Time-sensitive info noted with date disclaimer (以下信息均基于截至 YYYY.MM.DD 的资料)
- [ ] No fabricated details — unverified claims flagged with `（未经验证）`
- [ ] Functional emoji only (⚠️📅 etc.), no decorative emoji (🌸✨🎉)
- [ ] Hashtags restrained and reusing existing tags (e.g., `#准备去中国旅行`)
