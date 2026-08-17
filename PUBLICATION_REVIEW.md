# WorkBuddy 法律专家市场发布核验记录

核验日期：2026-08-18

发布工作分支：`agent/publish-legal-experts`

状态：`READY_FOR_HUMAN_MERGE_REVIEW`

## 1. 仓库定位

本仓库是轻量 marketplace 索引，不内嵌专家本体：

- `jackcheng459/execution-counsel` 独立维护执行律师。
- `jackcheng459/litigation-counsel` 独立维护诉讼律师。
- `jackcheng459/workbuddy-legal-experts` 维护统一入口、来源声明和总体状态。

该结构允许两个专家独立更新、审核和回滚，同时保留一个统一的 WorkBuddy 添加入口。

## 2. 本仓库发布范围

- `.codebuddy-plugin/marketplace.json`
- `README.md`
- `CHANGELOG.md`
- `PUBLICATION_REVIEW.md`
- `.github/reviews/MARKETPLACE_VALIDATION-20260818.md`
- `.github/reviews/MARKETPLACE_SHA256SUMS-20260818.txt`
- `.gitignore`

本仓库不包含客户材料、案件原件、真实案件运行记录、密钥、账号令牌、备份或内嵌专家目录。

## 3. 远端事实

### execution-counsel

- 清单版本：1.2.0。
- Private `main`：`9b895b83167ad28704a88fbbf0d7fbc9ce8de19b`。
- 远端 `plugin.json` 版本：1.2.0。
- 状态：已完成审阅并合并；未公开、未创建标签或 GitHub Release，发布分支保留。

### litigation-counsel

- 清单版本：1.0.0。
- Private `main`：`5c44b769e5cd606f4176fc0eac3acd7ab0d81835`。
- 远端 `plugin.json` 版本：1.0.0。
- 状态：已完成整改、审阅并合并；未公开、未创建标签或 GitHub Release，发布分支保留。

## 4. 清单校验

- marketplace 清单为有效 JSON。
- 两个插件名称、版本、仓库和描述均完整。
- 两个插件来源均使用 GitHub 仓库对象，符合官方 marketplace 插件来源结构。
- 清单版本与两个远端 `plugin.json` 版本一致。
- 两个目标仓库均存在并保持 Private。
- 索引只引用默认分支，不提前引用未审阅的工作分支。

## 5. 边界说明

- “已合并 Private `main`”只说明仓库主分支已有经过审阅的专家包，不等于已经公开发布或在真实案件中完成验证。
- 专家结构校验、合成测试和独立复核不替代实际 WorkBuddy 安装测试或律师对具体案件的判断。
- Private marketplace 的访问依赖用户具有三个仓库的权限和有效 Git 凭证。
- 本仓库没有开源许可，Private 状态下不向不具备权限的用户提供安装能力。

## 6. 当前闸门

- 本市场仓库保持 Private。
- PR #1 保持 Draft，等待 Jack 单独审阅和合并授权。
- 不创建版本标签或 GitHub Release。
- 不删除任何发布分支。
- 不宣称三个仓库已公开发布或生产放行。
- 合并后如需实际安装测试、改为 Public、创建标签或 Release，分别取得新的明确授权。
