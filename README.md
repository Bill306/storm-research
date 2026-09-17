# storm-research

用斯坦福 STORM 多视角研究法，对任意课题做 5–10 分钟的快速深度调研。以 Claude / Codex Skill 形式封装，复制到技能目录即可使用。

源自斯坦福大学 OVAL 实验室的 STORM（Synthesis of Topic Outlines through Retrieval and Multi-perspective Question Asking，NAACL 2024，经同行评审）：多视角调研产出的文稿，逻辑规整度高出 25%，内容覆盖广度提升 10%。本仓库将其核心思维框架落地为四段顺序提示词。

## 工作流程

在同一会话中按顺序执行四段提示词（完整原文见 [references/prompts.md](references/prompts.md)）：

| 阶段 | 提示词 | 产出 |
| --- | --- | --- |
| 1 | 多视角全景扫描 | 从业者 / 学术界 / 质疑派 / 经济学家 / 历史学家五个视角的核心立场与证据 |
| 2 | 矛盾冲突图谱 | 观点交锋点、证据强弱、全体共识（高可信度）、无人覆盖的盲区（往往最有价值） |
| 3 | 综合调研简报 | CEO 一分钟摘要、按可信度排序的 5 大发现、隐藏关联、针对你角色的行动建议、前沿问题 |
| 4 | 同行评审自检 | 1–10 可信度评分、最弱论断、偏见检查、缺失的第六视角、总评与修改建议 |

## 安装

```bash
git clone https://github.com/Bill306/storm-research.git
cp -R storm-research ~/.codex/skills/storm-research        # Codex
cp -R storm-research ~/.claude/skills/storm-research       # Claude Code
cp -R storm-research ~/.shared-agent-skills/storm-research # 共享 skills 库
```

## 使用

对 AI 说：「用 storm-research 调研 <你的课题>」。

提示词保持英文（跨模型更稳定），中文课题在提示词末尾加一行 `Answer in Chinese.`。替换提示词中的 `[YOUR TOPIC]` 和 `[YOUR ROLE]` 即可。

## 能力边界

该流程复刻的是 STORM 的多视角提问框架，不包含其检索模块：视角分析基于模型内部知识，涉及事实、数据、引用的结论必须另行核验。需要真实文献来源时，结合检索工具或官方在线工具 [storm.genie.stanford.edu](https://storm.genie.stanford.edu)（开源代码：[github.com/stanford-oval/storm](https://github.com/stanford-oval/storm)，MIT 协议）。

## 适用场景

写文章/报告前、重大商业决策前、求职面试前、投资研究前、学习新技能前、商务谈判前、公开演讲前。

## 许可

[MIT](LICENSE)
