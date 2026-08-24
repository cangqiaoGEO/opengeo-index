# 研究选题池

> L5 的另一半产出是研究报告（对标 Profound Research Hub）。本文件是弹药库：每个选题标注数据来源、可行性与预期产出。认领方式：开 issue 关联本文件条目。

## R1 · 中文品牌 AI 可见度基线报告（首发，对应路线图 v1.0 前置）

- **问题**：中文品牌在豆包/千问/DeepSeek/元宝中的可见度分布是什么样的？行业中位数在哪？
- **数据**：opengeo-audit 对 10+ 品牌的诊断（RFC-0005 观测记录聚合，匿名哈希上报）
- **可行性**：高——采集与评分链路已通（`npm run demo` 同款管线）
- **产出**：公开报告 + index 首批基准行；双周 release note 与公众号/知乎首发

## R2 · 中文引擎内容偏好规则挖掘（AutoGEO 复跑）

- **问题**：AutoGEO（ICLR 2026, arXiv:2510.11438, MIT）的 Rule Extraction 在 Gemini 上挖出的内容偏好规则，在豆包/千问上成立吗？中文引擎有哪些独有偏好？
- **数据**：AutoGEO 管线（GEO/opensource/AutoGEO）+ 自建中文查询集；GEO-Bench 做海外对照
- **可行性**：中——需 API 预算与规则评估人力；**九仓无人做过中文版，独家空间**
- **产出**：规则清单进 agentready CHECKLIST D 类；论文式报告

## R3 · scraped vs api 双通道答案差异量化

- **问题**：同一引擎同一问题，消费者界面答案与 API 答案的品牌提及/引用差异有多大？（RFC-0005 双通道解耦原则的实证基础）
- **数据**：audit 双通道采集已支持（official_api / official_app_browser 对照，`channel_compare.py` 已有雏形）
- **产出**：方法论报告，支撑「聚合不得跨通道混算」条款

## R4 · 引用源生态图谱：中文引擎到底信谁

- **问题**：豆包/元宝的引用集中在哪些域？知乎/百家号/官网/百科的占比结构？（elmo 的 citation 分类法 + 我们的中文数据）
- **数据**：观测记录 citations 字段聚合（`citation_utils.mjs` 分类器）
- **产出**：Top 信源榜——本身就是可传播的内容资产

## R5 · GEO-Bench 中文子集

- **问题**：GEO 学术评测没有中文基准；能否按 GEO-Bench（HuggingFace, cx-cmu）协议构建中文子集？
- **可行性**：低（远期）——工作量大，但做成即是标准制定权
- **产出**：数据集 + 评测协议 RFC
