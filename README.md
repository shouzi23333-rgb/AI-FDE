# AI 赋能体检（AI Empowerment Checkup）

> **3 分钟，给生意做一次 AI 体检——该不该上 AI，一次说清。**

AI 赋能体检是一个面向企业老板/个人老板的 AI 适配度检测 skill：通过对话式访谈深度挖掘业务真实运转情况，判断这门生意适不适合 AI 赋能，输出四档纯判断结论，并生成深色科技风 HTML 体检报告（含雷达图、词云、机会点与第一步行动）。

本检测方法融合 **IBM AI Ladder（AI 阶梯）框架、Gartner 企业 AI 成熟度模型、McKinsey Global Institute 的 AI 经济价值研究**，以及作者多年 AI 赋能一线实战经验沉淀而成——用 AI 来评测你的生意是否能使用 AI 赋能，不是拍脑袋的问卷，而是有理论框架支撑的业务诊断。

## 使用方式

在 Codex 中直接说：

- "检测一下我的生意适不适合用 AI"
- "帮我看看我的公司能不能 AI 赋能"
- "我想判断是否值得投入 AI"

Codex 会按 `SKILL.md` 的约束与你对话 12~18 轮，摸清业务基本盘与六个关键维度，随后给出结论并生成单文件 HTML 报告。

## 方法论背书

本 skill 的判断框架不是凭空拍脑袋，而是融合了国际主流 AI 落地方法论与一线实战经验：

- **IBM AI Ladder（AI 阶梯）**：IBM 官方提出的企业 AI 落地四步框架——Collect（收集）→ Organize（组织）→ Analyze（分析）→ Infuse（注入）。本 skill 的"数据基础"维度直接源自该框架的第一、二阶梯：数据是一切 AI 赋能的起点，没有留存的数据就没有赋能的土壤。
- **Gartner AI 成熟度模型**：Gartner 将企业 AI 成熟度划分为五级（ad hoc、basic、standardized、collaborative、adaptive）。本 skill 的"投入意愿""业务确定性"维度参考了其"组织能力决定 AI 能不能长大"的核心观点——AI 失败往往不是技术问题，而是组织与数据准备度问题。
- **McKinsey Global Institute 数据支撑**：MGI 研究估算生成式 AI 每年可为全球经济贡献 2.6~4.4 万亿美元（约 63 个用例、16 类业务职能）。同时大量企业 AI 项目卡在试点无法规模化——这正是"先检测、后投入"的价值所在。
- **SAS/IDC AI Readiness Index**：面向中小企业的 AI 就绪度评估框架（planning / building / enabling / executing 四维度），印证了中小企业做 AI 前需要先评估就绪度这一判断。
- **多年 AI 赋能一线实战经验**：将上述理论框架与真实落地案例中的踩坑经验（数据缺失、老板不投入、容错成本被低估等）沉淀为六维度信号判断与四条红线规则。

## 判断体系

- **六维度**：业务确定性、数据基础、容错成本、业务规模、客户关系、投入意愿
- **四档结论**：非常不建议 / 不建议 / 勉强建议 / 建议（纯判断，不评分）
- **红线机制**：重资产物理改造、合规致命场景、纯体力交付、零数字化且拒绝学习——命中任一直接判"非常不建议"

## 文件结构

```
SKILL.md                      # skill 行为约束与访谈流程（核心）
README.md                     # 说明与背书
references/research-notes.md  # 方法论调研笔记与出处
templates/report-template.html # 报告视觉模板（深色科技风）
examples/                     # 4 份验证用示例报告
agents/openai.yaml            # agent 元信息
```

## 参考出处

- IBM AI Ladder: https://ibm-cloud-architecture.github.io/refarch-data-ai-analytics/data/
- Gartner AI Maturity & Roadmap（via The Digital Insurer 摘要）: https://www.the-digital-insurer.com/library/library-gartner-ai-maturity-roadmap-report-accelerate-your-journey-to-ai-excellence/
- McKinsey Global Institute, "The economic potential of generative AI"（2023-06）: https://www.mckinsey.com/mgi/overview/in-the-news/ai-could-increase-corporate-profits-by-4-trillion-a-year-according-to-new-research
- SAS × IDC AI Readiness Index（中小企业）: https://blogs.sas.com/content/sascom/2026/05/13/sas-idc-ai-readiness-small-and-midsize-businesses/
- Gartner GenAI 预测（80% 企业 2026 年前使用 GenAI API；30% 项目在概念验证后放弃）: https://gcom.pdo.aws.gartner.com/en/articles/generative-ai-can-democratize-access-to-knowledge-and-skills
