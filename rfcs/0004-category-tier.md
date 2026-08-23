# RFC-0004：Index 品类坐标（category_tier 与渗透三维）

- 状态：已批准（2026-08-24，吸收弯弓白皮书评审通过）
- 影响：data schema 新增可选字段；首批 30 品牌选样方案

## 规格
每条基准记录可选携带：
- `category_tier`：`main_battlefield`（主战场）| `breakthrough`（突破口）| `latent`（后置市场）——分带口径转述自弯弓研究院白皮书渗透矩阵，标注出处；
- `penetration`：`{search_concentration, ai_coverage, roi_readiness}` 各取 `high|mid|low`（评估三维）。

对外指标使用 RFC-0002 行业通用指标（提及率/首推率/前三率/正面率/准确率），六维分数作为附注。

## 首批 30 品牌选样（杭州）
主战场 2 类（教育培训、美妆或家电3C 之一）× 各 6 品牌 + 突破口 2 类（本地生活、工业制造）× 各 8 品牌 + 后置 1 类（零食饮料细分）× 2 品牌。默认匿名哈希（D3 决议）。
