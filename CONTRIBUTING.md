# 贡献指南 · CONTRIBUTING

## 唯一事实来源
一切以本 HQ 仓库文档为准。开工前先读 `AGENTS.md`、`ROADMAP.md`、`TODO.md`。

## 提交前检查
- [ ] 未包含任何密钥 / 凭证（见 `SECURITY.md`）。
- [ ] 已同步相关文档：README / TODO / ROADMAP / CHANGELOG / 相应 Architecture·Vision·Business·Prompt·Workflow。- [ ] 变更可运行、可维护、可扩展。

## 提交信息规范（Conventional Commits）
`type(scope): summary`，type ∈ feat / fix / docs / chore / refactor / test / ci。-例：`docs(hq): add Day 2 engineering foundation`。

## 分支
- `main`：稳定。- `feat/*`、`fix/*`：开发分支，经 PR 合入。

## HQ vs 产品
HQ 只放文档与治理。产品代码进各自独立仓库，并在 `products/README.md` 登记。
