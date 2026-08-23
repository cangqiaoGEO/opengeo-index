# Index 数据行 schema（v0.1）

每条记录 = 一次复测（品牌 × 引擎 × 题集 × 日期），匿名聚合后发布。

| 字段 | 说明 |
| --- | --- |
| `date` | 复测日期 YYYY-MM-DD |
| `industry` | 行业（本地生活 / 制造业 To B / 教育培训 / 电商 / 服务业 …） |
| `city` | 城市（可为「全国」） |
| `engine` | doubao / yuanbao / deepseek / kimi / qwen / chatgpt … |
| `brand_hash` | 品牌匿名哈希（允许品牌方选择实名） |
| `queries` | 题集条数 |
| `visibility` / `recommendation` / `citation_quality` / `coverage` / `sentiment` / `foundation` | 六维分 0–100 |
| `total` / `grade` | 综合分与等级 |
| `source` | 提交者（org / community）与 audit 版本 |

提交方式：PR 一个 `data/YYYY-MM/<slug>.json` 或 `.md`；维护者聚合为行业基准表。数据许可 CC BY 4.0。

## 品类坐标字段（RFC-0004，可选）

| 字段 | 取值 | 说明 |
| --- | --- | --- |
| `category_tier` | `main_battlefield` / `breakthrough` / `latent` | 主战场 / 突破口 / 后置市场（分带口径转述自弯弓研究院《2026中国GEO行业实战白皮书》） |
| `penetration.search_concentration` | `high/mid/low` | 搜索集中度 |
| `penetration.ai_coverage` | `high/mid/low` | AI 搜索覆盖度 |
| `penetration.roi_readiness` | `high/mid/low` | GEO 投入产出比 |

对外发布使用行业通用指标（提及率 / 首推率 / 前三率 / 正面率 / 准确率，见 opengeo-audit RFC-0002）；六维合成分作为附注。
