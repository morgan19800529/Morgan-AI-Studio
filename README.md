# Morgan AI Studio · 摩根人工智能工作室 — HQ

> 让每一个普通人，都能轻松表达、持续创作、建立自己的品牌。

**本仓库是 Morgan-AI-Studio 的总部（HQ）**，不是产品代码仓库。
它只负责统筹整个 **AI Creator Operating System** 的：文档、路线、Prompt 库、工作流、知识库、商业与仪表盘。
大型产品代码一律放独立仓库（见 [`products/README.md`](products/README.md)）。

由 Morgan 发起，现居清迈。这里既是产品的中枢，也是一个 47 岁普通人重新学习、重新创作的公开记录。

---

## 这是什么

一个面向中文创作者的 **AI 创作者操作系统**。目标不是帮你"念稿"，而是陪你走完创作的完整闭环，并让数据在环里沉淀、自我迭代：

```
灵感 → 市场分析 → 选题 → 脚本 → 提词 → 直播 → 剪辑 → 发布 → 复盘 → AI优化 → 持续成长
```

## 现状

| 模块 | 状态 | 说明 |
| --- | --- | --- |
| 🎬 镜头说（提词器） | ✅ 已上线 | 面向手机的 AI 提词器 PWA，脚本库 / TXT·MD 导入 / 防息屏 / AI 生成直播·口播稿 |

在线体验：<https://morgan19800529.github.io/iphone-teleprompter/> · 源码：<https://github.com/morgan19800529/iphone-teleprompter>

## 仓库导航

| 目录 | 作用 |
| --- | --- |
| [`AGENTS.md`](AGENTS.md) | AI 角色 / 协作契约（CTO 等身份的操作规范） |
| [`ROADMAP.md`](ROADMAP.md) | 产品与技术路线 |
| [`TODO.md`](TODO.md) | 当前待办（Sprint 级） |
| [`CHANGELOG.md`](CHANGELOG.md) | 变更记录 |
| [`docs/`](docs/) | Vision / Architecture / Business |
| [`prompts/`](prompts/) | 模块化 Prompt Library |
| [`workflow/`](workflow/) | Idea→Research→…→Automation 工作流 |
| [`database/`](database/) | 数据表 / schema 约定 |
| [`dashboard/`](dashboard/) | 指标与看板 |
| [`products/`](products/) | 各独立产品仓库登记表 |
| [`knowledge/`](knowledge/) | 知识库 |
| [`assets/`](assets/) | 品牌与素材 |
| [`projects/`](projects/) | Sprint 日志与实验 |

## 开发原则

MVP First · Documentation First · Automation First · Reusable First · Scalable First · Evidence First · Low Cost First。
任何功能必须：**能运行、能维护、能扩展**。不为代码而代码。

## ⚠️ 安全须知

本仓库为**公开**仓库。**任何密钥 / API Key / 密码都不得提交**。
AI 功能所需密钥只存使用者本机浏览器，或经服务端代理处理，绝不写入代码库。详见 [`SECURITY.md`](SECURITY.md)。

---

*《1000 天生活方式观察》与本工作室同步进行 —— 一边记录，一边查证，一边分享。*
# Morgan AI Studio · 摩根人工智能工作室

> 让每一个普通人，都能轻松表达、持续创作、建立自己的品牌。

一个面向中文创作者的 AI 创作工作台。目标不是帮你"念稿"，而是陪你走完创作的每一步：**想内容 → 写内容 → 讲内容 → 剪内容 → 发布 → 复盘 → 持续成长**，最终形成一个能自我迭代的创作闭环。

由 Morgan 发起，现居清迈。这个仓库既是产品，也是一个 47 岁普通人重新学习、重新创作的公开记录。

---

## 现状

闭环里的第一个能跑起来的模块已经上线：

| 模块 | 状态 | 说明 |
|---|---|---|
| 🎬 镜头说（提词器） | ✅ 已上线 | 面向手机的 AI 提词器 PWA，支持脚本库、TXT/Markdown 导入、防息屏、AI 生成直播/口播稿 |

**在线体验**：https://morgan19800529.github.io/iphone-teleprompter/
**源码仓库**：https://github.com/morgan19800529/iphone-teleprompter

---

## 产品路线（务实版）

不追求一次做完，而是**一个能独立站住的模块跑通，再长出下一个**。

- **V1 · 智能提词器** — 直播和录制时能流畅表达 ✅ 进行中
- **V2 · AI 直播助手** — 输入主题，AI 写出带留人节点的直播稿，直接进提词器开播
- **V3 · AI 内容分发** — 一次直播，自动切成短视频、图文、多平台内容
- **V4 · 创作者工作台** — 热点 → 选题 → 脚本 → 直播 → 提词 → 剪辑 → 发布 → 复盘 → 优化，形成闭环

> 每一步都先自己用真实内容跑通，验证有人愿意用，再往下做。

---

## 设计原则

- **先解决真痛点**：创作者卡的不是"不会提词"，是"不知道讲什么、怎么坚持、什么内容有效"。
- **闭环才是护城河**：单个工具都有强对手，真正稀缺的是数据在环里的沉淀——复盘回流到选题，选题带着经验进入脚本。
- **隐私优先**：脚本、数据默认只存本机，不做无谓的账号和上传。

---

## 目录结构（规划）

```
Morgan-AI-Studio/
├─ README.md          项目说明（本文件）
├─ apps/              各功能模块（提词器、写稿、复盘……）
├─ docs/              愿景、路线图、设计笔记
└─ scripts/           口播稿与内容归档
```

> 目录随进度逐步填充，不预先造空壳。

---

## ⚠️ 安全须知

本仓库为**公开**仓库。**任何密钥、API Key、密码都不能提交到这里**，任何人都能看到。
AI 功能所需的密钥只存在使用者本机浏览器，或通过服务端代理处理，绝不写入代码库。

---

*《1000 天生活方式观察》与本工作室同步进行中 —— 一边记录，一边查证，一边分享。*
