# WorkBuddy Legal Experts

程建都律师维护的 WorkBuddy 法律专家市场，目前收录执行律师与诉讼律师两个 Agent 型专家。

本仓库只维护市场索引。两个专家分别保存在独立仓库中，可以独立开发、审核、更新和回滚。

## 收录内容

| 专家 | 版本 | 当前状态 | 主要用途 |
|---|---:|---|---|
| [`execution-counsel`](https://github.com/jackcheng459/execution-counsel) | 1.2.0 | 已合并 Private `main` | 申请执行人侧的谈案、接案评估、建项、材料增量更新、财产线索行动化和执行底稿 |
| [`litigation-counsel`](https://github.com/jackcheng459/litigation-counsel) | 1.0.0 | 已合并 Private `main` | 民商事诉讼的案情分析、证据争点映射、文书起草、庭审准备和调解评估 |

两个专家只生成候选意见和待律师复核成果，不替代律师完成案件承接、程序选择、法源核验、金额核算、文书签发或其他专业决定。

## 添加市场

在 WorkBuddy 或 CodeBuddy 的命令入口执行：

```text
/plugin marketplace add jackcheng459/workbuddy-legal-experts
```

添加后，从该市场选择需要的专家插件安装。当前三个仓库均为 Private，只有具备相应 GitHub 仓库权限且本地 Git 凭证可用的用户才能访问。

本仓库尚未在真实 WorkBuddy 环境完成 Private marketplace 添加和插件安装测试，因此当前状态是“索引结构已核验，等待实际安装验证”，不是公开发布或生产放行。

## 仓库分工

- `workbuddy-legal-experts`：维护市场清单、统一入口和总体状态。
- `execution-counsel`：独立维护执行律师的代码、CHANGELOG、验证、版本标签和 Release。
- `litigation-counsel`：独立维护诉讼律师的代码、CHANGELOG、验证、版本标签和 Release。

市场索引引用各专家仓库的默认分支。专家每次更新时，应先在独立仓库完成审查和合并，再同步本索引版本与状态。

## 当前质量状态

- `execution-counsel` v1.2.0 已完成结构校验、Skill 检查、合成烟测和独立复核，并合并至 Private `main`。
- `litigation-counsel` v1.0.0 已完成整改、隔离校验与注册、Skill Lint 和独立复核，并合并至 Private `main`。
- 清单版本与两个远端 `plugin.json` 版本一致。
- GitHub 对象来源结构已经按官方 marketplace 规范核对。
- 本索引仓库不包含专家本体、客户材料、案件原件、密钥、账号令牌或本地备份目录。

详细核验见 [PUBLICATION_REVIEW.md](PUBLICATION_REVIEW.md) 和 [市场索引校验回执](.github/reviews/MARKETPLACE_VALIDATION-20260818.md)。

## 作者与联系

北京海润天睿（郑州）律师事务所 程建都律师

公众号「程律进化论」

微信：`wx1811985798`

## 许可

本仓库暂未授予开源许可。未经权利人另行书面授权，不当然取得复制、修改或再分发权利。
