# WorkBuddy 法律专家市场索引校验回执

- 日期：2026-08-18
- 仓库：`jackcheng459/workbuddy-legal-experts`
- 分支：`agent/publish-legal-experts`
- 状态：`READY_FOR_HUMAN_MERGE_REVIEW`

## 来源核验

| 专家 | 清单版本 | 远端 `main` | 仓库状态 | 远端 plugin 版本 |
|---|---:|---|---|---:|
| `execution-counsel` | 1.2.0 | `9b895b83167ad28704a88fbbf0d7fbc9ce8de19b` | Private | 1.2.0 |
| `litigation-counsel` | 1.0.0 | `5c44b769e5cd606f4176fc0eac3acd7ab0d81835` | Private | 1.0.0 |

两个远端 `main` 均由已审阅 PR 合并形成，清单中的仓库名称、版本和 `plugin.json` 相互一致。

## 清单结构

- `.codebuddy-plugin/marketplace.json` 为有效 JSON。
- 两个插件名称唯一。
- 两个版本均为三段式语义版本号。
- 两个 `source` 均为 GitHub 对象，`repo` 使用 `owner/repo` 格式。
- `repository` 使用对应 HTTPS 仓库地址。
- 市场索引不再内嵌专家本体。

GitHub 对象来源的结构依据 Claude Code 官方 marketplace 规范核对。WorkBuddy 仍须在用户实际环境中完成添加市场和安装插件测试；本记录不把结构校验包装成真实安装完成。

## 内容与安全

- 索引仓库未发现客户材料、案件原件、真实案号、密钥、Token 或账号密码。
- 未发现软链接或可执行文件。
- 公开联系方式仅保留微信 `wx1811985798`。
- 本仓库未授予开源许可。

## 未执行

- 未合并本市场索引 PR。
- 未改为 Public。
- 未创建标签或 GitHub Release。
- 未删除任何发布分支。
- 未在真实 WorkBuddy 中添加本 Private marketplace 或安装两个插件。
