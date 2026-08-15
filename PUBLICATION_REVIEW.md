# GitHub 发布核验记录

核验日期：2026-08-15

发布工作分支：`agent/publish-legal-experts`

## 1. 发布范围

本次仅纳入以下现行目录：

- `plugins/execution-counsel`
- `plugins/litigation-counsel`
- `.codebuddy-plugin/marketplace.json`

明确排除：

- `execution-counsel-v1.0.0-backup-20260813`
- `execution-counsel-20260811-v1.2.0`
- 所有 `.DS_Store`
- 本地审计运行记录和安装候选 ZIP

## 2. 机械校验

使用 WorkBuddy 内置 `expert-manager` v0.1.0 的 `validate_expert.py` 对两个专家逐一校验：

| 专家 | 结果 | 警告 |
| --- | --- | --- |
| `execution-counsel` | 通过 | `displayDescription.zh` 为 114 字，超过建议的 40 至 50 字 |
| `litigation-counsel` | 通过 | `displayDescription.zh` 为 112 字，超过建议的 40 至 50 字 |

同时确认：

- marketplace 与两个 plugin 清单均为有效 JSON。
- 两张头像均为 512 x 512 PNG。
- 发布范围内未发现软链接或可执行文件。
- 文本扫描未发现 API Key、Token、密码、真实案号或客户材料。
- 公开联系方式统一为 `wx1811985798`。
- GitHub 工作副本仅机械删除了 6 处空列表项的行尾空格，不改变文字和运行语义。

## 3. 待闭合问题

### execution-counsel

- 基础结构有效。
- 版本为 1.2.0，含 CHANGELOG 和完整 references。
- 展示描述长度不符合当前 40 至 50 字建议，但不阻断结构校验。

### litigation-counsel

- README 仍有 5 处 `[TODO]` 占位。
- `skills/legal-collab-toolkit/SKILL.md` 声明了两个 references，但包内没有对应文件。
- Agent frontmatter 引用了 `ai-legal-case-workflow`，该 Skill 未随本专家包提供，也未在 plugin 清单中声明。
- 仍采用“红级仅本地处理”的旧数据口径，与当前绿色、黄色、红色、红线四类链路准入规则不完全一致。
- 缺少独立 CHANGELOG 和公开发布前的完整复核回执。

因此，`litigation-counsel` 当前状态为预览，不应宣称已经正式放行。

## 4. 发布闸门

- GitHub 私有仓库和 Draft PR：允许，用于 Jack 终审。
- GitHub 公开可见：等待 Jack 明确授权。
- 合并至 `main`：等待 Jack 审阅 Draft PR 后决定。
- `litigation-counsel` 正式放行：等待上述待闭合问题完成修订和复核。
