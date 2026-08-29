# CLAUDE.md — opengeo-index（L5 · 行业基准）

本仓是 OpenGEO 可见度指数（对外名 OpenGEO Index；内部代号不对外）。**schema 未冻结、聚合脚本未写、目前仅 1 条数据**——回答现状时如实说。

## 研发流程

按 [OpenGEO/docs/ai-native-sdlc.md](https://github.com/cangqiaoGEO/OpenGEO/blob/main/docs/ai-native-sdlc.md)。`data/SCHEMA.md` 变更必须走 RFC（治理条款 4）。

## 地图

- `data/SCHEMA.md` v0.1 + `data/2026-08/` 首条基线记录
- `rfcs/0004-category-tier.md`（已批准）：品类坐标 + 渗透三维 + 首批 30 品牌选样
- `research/TOPICS.md` 研究选题池

## 约定（隐私与命名，不可违）

- 自有产品客户默认列名进公开基准（合同附列名条款兜底）；**非客户一律 `brand_hash` 匿名**；任何第三方不得代他人实名
- 只发聚合分与等级，**不发原始问答与引用明细**
- 上游数据形态 = RFC-0005 ObservationRecord；聚合不跨通道混算
- 永不做服务商榜单（Index 只测品牌可见度）

## 验证

python3 tools/check_links.py（CI 强制）；schema 变更过 RFC 后须同步 data/ 现有记录。
