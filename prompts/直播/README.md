# prompts/直播 · 直播 Prompt 分类

面向"直播/口播"场景的模块化 Prompt。服务 V2「AI 直播助手」：输入主题 → 输出带留人节点、可直接进提词器的稿件。

| Prompt | 用途 |
| --- | --- |
| [直播稿生成.md](直播稿生成.md) | 主题 → 完整直播稿（含留人节点、提词器友好排版） |
| [留人开场.md](留人开场.md) | 单独生成 3~5 个高留存开场钩子 |

## 约定
- 每个 Prompt 顶部带 front-matter：title / category / version / inputs / outputs。
- 输出默认"提词器友好"：短句、口语、每句独立成行，不用 Markdown 语法符号。
