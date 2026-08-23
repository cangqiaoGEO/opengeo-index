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
