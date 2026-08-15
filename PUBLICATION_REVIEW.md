# WorkBuddy 法律专家市场发布核验记录

核验日期：2026-08-15

发布工作分支：`agent/publish-legal-experts`

## 1. 仓库定位

本仓库是轻量 marketplace 索引，不再内嵌专家本体：

- `jackcheng459/execution-counsel` 独立维护执行律师。
- `jackcheng459/litigation-counsel` 独立维护诉讼律师。
- `jackcheng459/workbuddy-legal-experts` 只维护统一入口、来源声明和总体状态。

该结构允许两个专家独立更新、审核、发布和回滚，同时保留一个统一的 WorkBuddy 添加入口。

## 2. 本仓库发布范围

- `.codebuddy-plugin/marketplace.json`
- `README.md`
- `PUBLICATION_REVIEW.md`
- `.gitignore`

已从本分支移除原先内嵌的 `plugins/execution-counsel` 与 `plugins/litigation-counsel`。这些内容已经复制到各自独立私有仓库的发布工作分支，原始 Git 提交仍可恢复。

## 3. 机械校验

- marketplace 清单为有效 JSON。
- 两个插件来源均使用 GitHub 仓库对象，不再使用本仓库相对路径。
- 目标仓库 `jackcheng459/execution-counsel` 与 `jackcheng459/litigation-counsel` 已创建，当前保持 Private。
- 本仓库不包含专家本体、客户材料、案件原件、密钥、账号令牌、备份或内部审计运行记录。

## 4. 专家状态

### execution-counsel

- 版本：1.2.0。
- 独立仓库分支：`agent/publish-v1.2.0`。
- 状态：发布候选，等待 Draft PR 审阅。

### litigation-counsel

- 版本：1.0.0。
- 独立仓库分支：`agent/publish-v1.0.0-preview`。
- 状态：预览候选，README、references、依赖声明、数据边界和发布文档仍待整改。

## 5. 合并顺序

1. 先审阅并决定是否合并 `execution-counsel` 的发布 PR。
2. 完成 `litigation-counsel` 整改、复核，再决定是否合并其发布 PR。
3. 两个专家仓库的 `main` 均存在可安装内容后，再合并本市场索引 PR。
4. 公开可见性、版本标签和 GitHub Release 分别取得 Jack 明确授权后执行。

## 6. 当前闸门

- 三个仓库保持 Private。
- 三个发布 PR 保持 Draft。
- 不直接写入任何仓库的 `main`。
- 不创建版本标签或 GitHub Release。
- 不宣称两个专家已经公开发布或正式放行。
