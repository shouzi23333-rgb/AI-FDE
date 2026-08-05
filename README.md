# AI-FDE

> **3 分钟，给业务做一次 AI 体检——AI 该用在哪、值不值得投，一次说清。**

AI-FDE是一个面向企业老板/个人老板的 AI 机会检测 skill：通过对话式访谈找到业务里 3 至 5 个具体任务，逐个评估**值不值得做（Opportunity）、能不能做（Feasibility）、有没有风险（Risk）、划不划算（Economics）**，输出任务级结论（优先试点/值得验证/先补基础/仅限辅助/暂不投入）与企业四档总览，并生成深色科技风 HTML 体检报告（含就绪度雷达图、词云、PoC 最小验证方案）。

本检测方法融合 **IBM AI Ladder（AI 阶梯）框架、Gartner 企业 AI 成熟度模型、McKinsey Global Institute 的 AI 经济价值研究**，以及作者多年 AI 赋能一线实战经验沉淀而成——用 AI 来评测你的业务是否能使用 AI 赋能，不是拍脑袋的问卷，而是有理论框架支撑的业务诊断。

## 使用方式

在 Codex 中直接说：

- "检测一下我的业务适不适合用 AI"
- "帮我看看我的公司能不能 AI 赋能"
- "我想判断是否值得投入 AI"
- "对我的业务做一次一对一深度调研"（进入深度调研模式）
- 调研完成后："生成需求文档"（仅调研模式可用；面向研发与项目经理的 21 节完整 Word 文档，缺的信息会列出「待补齐清单」并告诉老板向谁要）

**两种模式**：

- **AI-FDE（检测）**：对话 13 至 18 轮（上限 20 轮），快速筛查 3 至 5 个候选任务，输出四档总览 + 任务级 A~E + PoC，约 10 分钟。
- **一对一调研（深度）**：30 至 50 分钟一对一深访，识别 3 至 8 个候选任务、筛 Top 3 逐个深挖 Opportunity / Feasibility / Risk / Economics（含系统集成难度、ROI、回本周期、AI 自主等级），输出 PoC 与 3/6 个月回访跟踪。

也可以直接说："让 AI-FDE帮我测测我的业务适不适合用 AI。"

## 方法论背书

本 skill 的判断框架不是凭空拍脑袋，而是融合了国际主流 AI 落地方法论与一线实战经验：

- **IBM AI Ladder（AI 阶梯）**：IBM 官方提出的企业 AI 落地四步框架——Collect（收集）→ Organize（组织）→ Analyze（分析）→ Infuse（注入）。本 skill 的"数据基础"维度直接源自该框架的第一、二阶梯：数据是一切 AI 赋能的起点，没有留存的数据就没有赋能的土壤。
- **Gartner AI 成熟度模型**：Gartner 将企业 AI 成熟度划分为五级（ad hoc、basic、standardized、collaborative、adaptive）。本 skill 的"投入意愿""业务确定性"维度参考了其"组织能力决定 AI 能不能长大"的核心观点——AI 失败往往不是技术问题，而是组织与数据准备度问题。
- **McKinsey Global Institute 数据支撑**：MGI 研究估算生成式 AI 每年可为全球经济贡献 2.6 至 4.4 万亿美元（约 63 个用例、16 类业务职能）。同时大量企业 AI 项目卡在试点无法规模化——这正是"先检测、后投入"的价值所在。
- **SAS/IDC AI Readiness Index**：面向中小企业的 AI 就绪度评估框架（planning / building / enabling / executing 四维度），印证了中小企业做 AI 前需要先评估就绪度这一判断。
- **多年 AI 赋能一线实战经验**：将上述理论框架与真实落地案例中的踩坑经验（数据缺失、老板不投入、容错成本被低估等）沉淀为六维度信号判断与四条红线规则。

## 判断体系

- **评估对象**：具体任务（Use Case），不是整个公司——先找任务，再逐个评估，最后给行动建议
- **四层评估**：Opportunity（值不值得做）/ Feasibility（能不能做）/ Risk（有没有风险）/ Economics（划不划算），每层输出 高/中/低/未知（U，未知不计差评）
- **任务级结论 A~E**：优先试点 / 值得验证 / 先补基础 / 仅限辅助 / 暂不投入
- **企业四档总览**：非常不建议 / 不建议 / 勉强建议 / 建议（纯判断，不评分，由任务级结论推导）
- **置信度**：高 / 中 / 低——信息不足时如实标注，不假装精确
- **红线机制（任务级）**：重资产物理改造（超出评估范围）、合规致命场景（限辅助）、纯体力交付、零数字化且拒绝学习

## 方法论声明

本框架基于现有 AI readiness、AI maturity、AI risk management 与生成式 AI 应用研究构建。当前各维度与判断规则属于**专家启发式规则（expert heuristic）**，尚未经过大规模实证数据进行权重与阈值校准。

我们参考 IBM AI Ladder、Gartner AI 成熟度模型、McKinsey 等研究来选择评估因素，**并非这些机构验证了本工具的公式**。本工具用于 AI 机会初筛与咨询辅助，不应替代专业法律、医疗、财务、安全或重大投资判断。

## 文件结构

```
SKILL.md                      # skill 行为约束与访谈流程（核心）
one-on-one-research/SKILL.md  # 一对一深度调研 skill（第二模式）
README.md                     # 说明与背书
references/research-notes.md  # 方法论调研笔记与出处
templates/report-template.html # 报告视觉模板（深色科技风）
examples/                     # 6 份验证用示例报告 + 需求文档 Word 示例（.docx）
agents/openai.yaml            # agent 元信息
```

## 参考出处

- IBM AI Ladder: https://ibm-cloud-architecture.github.io/refarch-data-ai-analytics/data/
- Gartner AI Maturity & Roadmap（via The Digital Insurer 摘要）: https://www.the-digital-insurer.com/library/library-gartner-ai-maturity-roadmap-report-accelerate-your-journey-to-ai-excellence/
- McKinsey Global Institute, "The economic potential of generative AI"（2023-06）: https://www.mckinsey.com/mgi/overview/in-the-news/ai-could-increase-corporate-profits-by-4-trillion-a-year-according-to-new-research
- SAS × IDC AI Readiness Index（中小企业）: https://blogs.sas.com/content/sascom/2026/05/13/sas-idc-ai-readiness-small-and-midsize-businesses/
- Gartner GenAI 预测（80% 企业 2026 年前使用 GenAI API；30% 项目在概念验证后放弃）: https://gcom.pdo.aws.gartner.com/en/articles/generative-ai-can-democratize-access-to-knowledge-and-skills
