# database · 复盘数据 schema

支撑数据闭环：**发布表现 → 复盘 → 回流选题 → 进入脚本**。这是愿景里的护城河。
仓库只放 schema 与空模板，**真实数据存本机**（Google Sheet / 本地），不入库、不含隐私。

## 表一 · 选题库 topics

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| id | string | 选题编号 |
| title | string | 选题一句话 |
| source | enum | 来源：灵感 / 热点 / 复盘回流 / 对标拆解 |
| platform | enum | 目标平台 |
| status | enum | 待做 / 进行中 / 已发布 / 已复盘 |
| score | number | 选题评分 1–5（可选） |
| created_at | date | 建立日期 |

## 表二 · 内容表现 performance

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| content_id | string | 内容编号（关联 topics.id） |
| platform | enum | 发布平台 |
| type | enum | 直播 / 短视频 / 图文 |
| publish_date | date | 发布日期 |
| views | number | 曝光 / 播放 |
| watch_rate | number | 完播率 / 平均观看时长 |
| interactions | number | 点赞 + 评论 + 转发 |
| new_followers | number | 涨粉 |
| conversions | number | 转化（扣1 / 加微 / 购买） |
| hook_kept | bool | 留人节点是否有效（主观判断） |

## 表三 · 复盘 review

| 字段 | 类型 | 说明 |
| --- | --- | --- |
| content_id | string | 关联内容 |
| what_worked | string | 有效的点 |
| what_failed | string | 失效的点 |
| next_experiment | string | 下一步实验 |
| feedback_to_prompt | string | 回流给哪个 Prompt 优化 |

## 回流逻辑（闭环怎么转）
1. 内容发布后填 `performance`。
2. 每周对表现 top / bottom 各做一次 `review`。
3. `review.next_experiment` 变成新的 `topics`（source = 复盘回流）。
4. `feedback_to_prompt` 汇总后，用于迭代 `prompts/直播`、`prompts/分发`。

## 约定
- 字段命名 snake_case；一条内容一个 content_id，贯穿三表。
- Evidence First：先手动填几周，验证指标有用，再谈自动化与 dashboard。
- 配套空模板见 `database/复盘模板.csv`。
