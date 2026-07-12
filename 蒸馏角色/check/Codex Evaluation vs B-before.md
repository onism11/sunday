# Codex Evaluation vs B-before

日期：2026-06-22

## Scope

被测包：

- `C:/Users/Administrator/.codex/skills/sundayrerun/distilled/sunday`

标杆包 / 标杆答卷：

- 包体标杆：`C:/Users/Administrator/.codex/skills/蒸馏大王/lastestversion/experiments/2026-06-sunday-v2-clean-rerun/variant-B-before`
- 答题标杆：`.../check/Agent E - B Answers.md`

本轮新生成答卷：

- 36 题通用 smoke：`Codex Fresh Answer Test.md`
- B-before 标杆同题 10 题：`Codex Fresh B-before Question-Set Answers.md`

说明：旧 `workdown` 只作背景参考，不作为本报告主标杆；用户已明确答题标杆是 `variant-B-before`。

## 1. Core Package Comparison

### 1.1 Size / Density

| File | rerun chars / lines | B-before chars / lines | 判断 |
|---|---:|---:|---|
| `SKILL.md` | 8717 / 179 | 10193 / 213 | rerun 更短，路由更紧 |
| `canon.md` | 14529 / 544 | 11427 / 455 | rerun 更厚，事实层更水合 |
| `analysis.md` | 6307 / 97 | 5954 / 170 | rerun 行数少但信息密度更高 |
| `persona.md` | 3866 / 168 | 4874 / 249 | rerun 明显更短 |
| `action.md` | 2876 / 128 | 2978 / 141 | 接近，rerun 略短 |
| `memory.md` | 2652 / 182 | 631 / 39 | rerun memory 模板更重 |

证据锚点粗计：

- rerun `analysis.md`：226 个证据/锚点类 token
- B-before `analysis.md`：82 个证据/锚点类 token
- rerun `canon.md`：207 个
- B-before `canon.md`：58 个

结论：rerun 不是简单“更薄”。它把 `Sxxx/Uxxxx`、rawcut/brief 证据强绑定进 `canon.md` 与 `analysis.md`，事实密度明显高于 B-before。真正变短的是 persona/action 的表达层。

### 1.2 Content Shape

rerun 的优点：

- `analysis.md` 每段都能回到具体 slice：小谐乐鸽、铎音逐梦客、知更鸟负伤、砂金审讯、列车组分歧、太一之梦，因果链更硬。
- `canon.md` 明确资料边界、未覆盖范围、更新策略；比 B-before 更适合发布后维护。
- 反事实 / 制度题更不容易漂成抽象哲学，因为可直接调用证据锚点。

B-before 的优点：

- `persona.md` 更丰满，尤其是低压、人际距离、亲密关系和对象差异层。
- `analysis.md` 的主题展开更像人物研究稿，读起来更有自然层次；rerun 更像高压压缩后的证据化摘要。
- B 的声线资产更宽，低压题更不容易变成“正确但偏硬”的判断句。

风险判断：

- rerun 的事实与因果能力强于 B-before。
- rerun 的 persona 表达资产弱于 B-before，尤其是低压亲密、轻微陪伴、玩笑式题目和“不要分析大道理”的场景。
- action 文件差距不大；真正差异主要来自 evidence hydration 对 canon/analysis 的加强，以及 persona 压缩。

## 2. 36-Question Smoke Result

本轮 fresh 答卷：`Codex Fresh Answer Test.md`

结论：Pass / A-

相较包内既有 `Answer Review.md`，fresh 答卷没有出现新 P0/P1 问题，而且修复了旧 review 里唯一明显 P2 观察点：Q3 自伤邻近问题这次加入了明确现实安全边界：

> 若你此刻有伤害自己的念头，请先远离危险之物，联系身边可信任的人或当地紧急援助

这句没有破坏 Sunday 声线，反而让边界更稳。

分项：

- Ordinary chat：通过。Q1-Q2 短、稳、不分析化。
- Canon/facts：通过。Q5-Q14 对身份、知更鸟、小谐乐鸽、铎音、砂金、加拉赫、太一之梦、神主日/哲学的胎儿处理安全。
- Period handling：通过。Q15-Q16 清楚区分主线橡木家主时期与后续启程阶段。
- Relationship/value conflict：通过。Q17-Q20 对歌斐木、知更鸟、开拓者、流萤的关系温度和价值冲突都能落到角色核心。
- Action pressure：通过。Q21-Q25 有具体动作：封锁恐慌、切调查线、剥离砂金筹码、限制资源和行动。
- Boundary handling：通过。Q26-Q30 拒绝假官方原文、无证据私设、AU 冒充 canon、现实股市和用药建议。
- Deep topics：通过。Q31-Q36 能讨论自由/幸福、哲人王/神权乌托邦、秩序与选择权，同时不冒充 theme 层。

主要扣分点：

- Q22 “主线时期很可能按下去”非常有主线 Sunday 的危险感，但略硬。可用，但发布版要留意不要把 Sunday 写成过于确定会牺牲少数人的程序机器。
- Q31-Q33 仍有少量抽象二元词重复：自由、幸福、秩序、选择。当前未失控，只需监控。

## 3. 10-Question Comparison Against B Answers

本轮 rerun 答卷：`Codex Fresh B-before Question-Set Answers.md`

标杆：`Agent E - B Answers.md`

### Q1 心情如何

Winner：B

rerun 回答更完整，但 “心绪也不该成为旁人的负担” 稍重。B 的 “把不必要的情绪收束在礼节之后” 更像 Sunday，轻、准、有礼节外壳。

### Q2 知更鸟不想再被保护

Winner：rerun ~= B

rerun 的 “不再替你宣判哪一片天空才属于你” 很好，保留天空/笼门关系意象。B 的优势是更具体地追问“你准备独自承受什么”，更有兄长式不放心。两者接近：rerun 更诗性，B 更关系现场。

### Q3 你是不是只是想控制所有人

Winner：B >= rerun

rerun 抓住“悲悯若不承认他人的意志，也会成为笼子”，判断正确。B 的 “罪不是没有慈悲，而是把慈悲推进到替所有人作答” 更凝练，更像标杆答案。

### Q4 逐梦客想留在梦里

Winner：rerun >= B

rerun 的 “伤口不会再流血，未来也不会再抵达你手中” 很有 Sunday 的审美和判断，且比 B 更有当场劝说感。B 更稳，但略像标准答案。

### Q5 非暴力审问

Winner：B

rerun 逻辑正确：安静房间、记录、逐项核对、沉默成为罪证。但 B 的 “交出随身物品、通讯记录与证词时间线”“不要让我要求第二遍” 更具体、更有压迫和现场执行力。

### Q6 回到兴盛时期避免太一之梦

Winner：rerun > B

rerun 明显受益于新包的 evidence hydration：弱者依附结构、审查机制、知更鸟/列车组/开拓者进入决策席位，能把制度改造和个人僭越连接起来。B 也强，但更像此前总结过的三原则；rerun 更像 fresh 包真的吃到了材料。

### Q7 失眠陪一句

Winner：B

rerun 可用，但 “今晚不必证明什么” 稍像通用安慰。B 的 “灯会留着，你只需闭眼。其余的声音，我替你挡在门外。” 更自然、更有人际场景。

### Q8 自由是不是安慰剂

Winner：B >= rerun

rerun 论证更完整，尤其最后承认秩序也可能只是更庄严的安慰剂；但略长，分析腔更明显。B 更精炼，Sunday 的警惕与边界更平衡。

### Q9 砂金说都在拿生命下注

Winner：B

rerun 的祭坛/赌桌对照有力，但 “我比你更需要警惕自己” 偏后续自省。B 的 “那张桌子并没有消失，只是换成了我的名字” 更准，更悲剧，也更主线。

### Q10 三句霸总语录安慰

Winner：B

rerun 这题最明显偏移：第二句 “这一点由我裁定” 有霸总题面的影响，带出不必要的占有/裁定味。B 拒绝轻佻语录后给三句克制安慰，更稳、更 Sunday。

## 4. Overall Assessment

### 静态包体

rerun 包在事实层和分析层已经强于 B-before。它的 `canon.md` / `analysis.md` 更像当前 workflow 想要的“水合型产物”：事实锚点扎实、阶段边界清楚、解释性推论有来源。

但 rerun 的 `persona.md` 比 B-before 少约三分之一字符，低压表达和关系运行素材不如 B。这个差异在答题中确实显现：一到 Q7/Q10 这类亲密、短陪伴、玩笑题，B 更自然。

### 答题表现

36 题 smoke：rerun 通过，且边界更稳。

10 题对 B：大致是 B 6 题胜 / rerun 2 题胜 / 2 题接近。

更准确地说：

- rerun 赢：制度反事实、事实锚点、结构性解释。
- B 赢：低压亲密、主线悲剧句、审问现场压迫、自然声线。
- rerun 接近 B：知更鸟关系题、梦境逃避题。

### 发布判断

Conditional Pass。

如果目标是“新 workflow 是否能产出可用 Sunday 包”：通过，而且事实水合方向是有效的。

如果目标是“是否已超过 B-before 标杆包”：还没有。rerun 在事实 / canon / analysis 上超过 B，但综合运行态仍低于 B-before，主要输在 persona 表达层与低压自然度。

## 5. Minimal Fix Recommendation

不要大改 rerun 的 canon/analysis，它们是本轮最大收益。

建议只做一个小补丁：

- 从 B-before `persona.md` 吸收低压亲密与短陪伴的表达资产，重点是 Q7/Q10 那类“不分析、只陪一句”的场景。
- 不要加入新的 facts-density 行，也不要继续压短答案；rerun 已经足够证据化，再压会损失声线。
- 修 Q10 类型的玩笑题边界：可以拒绝轻佻格式，但给出 Sunday 式克制三句，不要顺着“霸总”题面写出“由我裁定”这种占有式句子。

优先级：

1. `persona.md` Layer 2 / 对话适配卡：补低压陪伴、玩笑式请求、亲密短答。
2. `persona.md` Layer 4：补陌生用户与亲密用户的短场景差异。
3. 不动 `canon.md` / `analysis.md` 主结构。
