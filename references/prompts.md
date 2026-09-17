# STORM 四段提示词（完整原文）

按顺序在同一会话中粘贴执行。将 `[YOUR TOPIC]` 替换为研究主题，`[YOUR ROLE]` 替换为使用者角色（如 `a fund analyst`、`a product manager`）。

## 提示词一：多视角全景扫描

```text
I need to research [YOUR TOPIC].

Simulate 5 different expert perspectives on this topic:

1. THE PRACTITIONER: works with this daily.
What do they know that academics miss?
What practical realities are usually ignored?

2. THE ACADEMIC: has studied this for years.
What does the peer reviewed evidence actually say?
Where does the evidence contradict popular belief?

3. THE SKEPTIC: thinks the mainstream view is wrong.
What is the strongest counterargument?
What evidence do proponents conveniently ignore?

4. THE ECONOMIST: follows the money.
Who profits from the current narrative?
What financial incentives shape the research?

5. THE HISTORIAN: has seen similar patterns before.
What historical parallels exist?
What can we learn from how those played out?

For each perspective give me:
- Their core position in 2 sentences
- The strongest evidence supporting their view
- The one thing they would tell me that no other perspective would
```

预期产出：五个完全不同的课题解读。从业者指出学术界的脱离实际之处，质疑派推翻固有认知，经济学家揭露利益诱因，历史学家提炼发展规律。

## 提示词二：矛盾冲突图谱

```text
Based on the 5 perspectives above, map the contradictions:

1. Where do two or more perspectives directly contradict each other? List each conflict with the specific claims that clash.
2. Which perspective has the strongest evidence? Which has the weakest? Why?
3. What is the one question that, if answered, would resolve the biggest contradiction?
4. What does EVERY perspective agree on? (This is likely true. Even opponents confirm it.)
5. What topic did NONE of the perspectives address? (This is the blind spot in the whole field. Often the most valuable finding.)
```

判读要点：全体达成共识的内容可信度极高；没有任何视角覆盖的方向，就是该领域现存的研究空白。

## 提示词三：综合调研简报

```text
Synthesize everything from the 5 perspectives and the contradiction map into a research briefing:

1. THE ONE PARAGRAPH SUMMARY: explain this topic as if briefing a CEO who has 60 seconds and needs nuance, not just the headline.
2. THE 5 KEY FINDINGS: most important things I now know, ranked by reliability. For each, note which perspectives support it and which challenge it.
3. THE HIDDEN CONNECTION: one non obvious link between findings that only shows up when you look at all 5 perspectives together.
4. THE ACTIONABLE INSIGHT: based on all the evidence, what should someone in [YOUR ROLE] actually DO differently? Be specific.
5. THE FRONTIER QUESTION: the one question that, if answered, would change everything about how we understand this topic.
```

## 提示词四：同行评审自检

斯坦福团队指出 STORM 原生缺少自我批判环节，容易出现资料来源偏差、事实错配。本段补上这一环。

```text
Now peer review your own research briefing:

1. CONFIDENCE SCORES: rate each of the 5 key findings on a 1 to 10 scale for reliability. Explain each score.
2. WEAKEST LINK: which claim are you least confident in? What specific info would you need to verify it?
3. BIAS CHECK: which perspective might be overrepresented in your synthesis? Did one voice dominate?
4. MISSING PERSPECTIVE: is there a 6th angle I should have included that would change the conclusions?
5. OVERALL GRADE: if a Stanford professor reviewed this briefing, what grade would they give and why? What would they tell me to fix?
```

## 角色设定（可选，置于会话开头）

```text
你是一名深度研究者，擅长提出尖锐问题，不需要看似高大上却空洞无物的两百字空话总结。
你希望快速、依托权威资料看透事物本质，拥有斯坦福研究生级别的调研能力，却不用付出六年高昂的学费。
```

## 典型落地场景

| 场景 | 五视角的价值 |
| --- | --- |
| 写文章/报告前 | 覆盖绝大多数人想不到的分析角度 |
| 重大商业决策前 | 从业者讲落地现实，质疑派预判风险，经济学家理清利益格局 |
| 求职面试前 | 从业者视角提供行业内行话术，质疑视角生成犀利提问 |
| 投资决策前 | 多空逻辑、历史相似案例、利益诱因、学术论据一次集齐 |
| 学习新技能前 | 从业者定优先级，学术界搭框架，质疑派过滤炒作 |
| 商务谈判前 | 摸清对手利益诉求、短板与行事规律 |
| 公开演讲前 | 提前预判并回应观众质疑 |

## 来源

- 原始研究：Stanford OVAL Lab, STORM（NAACL 2024），代码开源（MIT）：github.com/stanford-oval/storm，在线工具：storm.genie.stanford.edu
- 提示词文本：整理自公众号文章《斯坦福STORM研究法：用Claude5分钟内完成博士级深度调研》
