# 方法论调研笔记

调研日期：2026-08-04。以下为设计「AI 赋能检测」判断框架时查证的主要来源与要点，用于维护 README 背书素材。

## IBM AI Ladder（AI 阶梯）

- 来源：IBM Cloud Architecture 官方参考架构文档
- URL：https://ibm-cloud-architecture.github.io/refarch-data-ai-analytics/data/
- 要点：企业 AI 落地的四个阶梯——
  1. Collect：让数据简单、可访问
  2. Organize：可信、有治理的分析基础（数据可发现、可编目、可复用）
  3. Analyze：按需洞察（从报表 BI 到深度学习）
  4. Infuse：把 AI 运营化，嵌入业务流程，可信、透明
- 与本 skill 的关联：数据基础维度对应 Collect/Organize——没有留存的数据，AI 没有土壤。

## Gartner AI 成熟度模型

- 来源：Gartner 报告 *AI Maturity & Roadmap – Accelerate Your Journey to AI Excellence*
- 参考摘要：https://www.the-digital-insurer.com/library/library-gartner-ai-maturity-roadmap-report-accelerate-your-journey-to-ai-excellence/
- 要点：五级成熟度——ad hoc（临时）、basic（基础）、standardized（标准化）、collaborative（协同）、adaptive（自适应）。模型诊断组织在战略、治理、数据管理、工程能力上的差距。
- 与本 skill 的关联：投入意愿、业务确定性维度——AI 成败首先取决于组织（人）与数据准备度，而非技术。

## McKinsey Global Institute：生成式 AI 的经济价值

- 来源：MGI 2023-06，《The economic potential of generative AI》
- 参考：https://www.mckinsey.com/mgi/overview/in-the-news/ai-could-increase-corporate-profits-by-4-trillion-a-year-according-to-new-research
- 要点：
  - 生成式 AI 每年可为全球经济贡献相当于 2.6~4.4 万亿美元的价值（63 个用例、16 类业务职能）
  - 可每年提升劳动生产率 0.1%~0.6%（至 2040）
- 用途：背书话术中"AI 赋能是有真实经济价值"的数据支撑。

## Gartner GenAI 预测

- 来源：Gartner
  - 到 2026 年，超过 80% 的企业将使用 GenAI API/模型或部署 GenAI 应用（2023 年初不足 5%）
  - 30% 的生成式 AI 项目将在概念验证后被放弃，主因：数据质量差、风险控制不足、成本失控、商业价值不清晰
- URL：https://gcom.pdo.aws.gartner.com/en/articles/generative-ai-can-democratize-access-to-knowledge-and-skills
- 用途："先检测、后投入"的价值论证——盲目上马失败率高，检测先行能避开常见坑。

## SAS × IDC：中小企业 AI Readiness Index

- 来源：SAS/IDC 报告（2026-05）
- URL：https://blogs.sas.com/content/sascom/2026/05/13/sas-idc-ai-readiness-small-and-midsize-businesses/
- 要点：面向中小企业的 AI 就绪度框架，四维度——planning（规划）、building（构建）、enabling（使能）、executing（执行）。
- 与本 skill 的关联：佐证"中小企业做 AI 前应先评估就绪度"的方向。

## 学术参考：SME AI 就绪度多维评估

- 来源：*A Preliminary multidimensional AI readiness assessment model for SME's*（Procedia Computer Science, 2025）
- URL：https://www.sciencedirect.com/science/article/pii/S1877050925001474
- 要点：提出 TOEH 框架（Technology-Organization-Environment-Human），认为中小企业 AI 就绪度是多维构造。
- 与本 skill 的关联：印证六维度中同时包含"技术/数据（T）"与"人/组织（O-H）"的必要性。

## 备注

- 背书措辞统一口径："融合 IBM AI Ladder、Gartner AI 成熟度模型等国际框架与多年一线实战经验"——只表述为"借鉴/融合框架"，不写成"官方认证"。
- 所有引用保持真实可查；不虚构企业数量、客户案例与奖项。
