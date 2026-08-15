# WorkBuddy Legal Experts

程建都律师维护的 WorkBuddy 法律专家市场，目前收录执行律师与诉讼律师两个 Agent 型专家。

## 收录内容

| 专家 | 版本 | 当前状态 | 主要用途 |
| --- | --- | --- | --- |
| `execution-counsel` | 1.2.0 | 发布候选 | 申请执行人侧的谈案、接案评估、建项、材料增量更新、财产线索行动化和执行底稿 |
| `litigation-counsel` | 1.0.0 | 预览 | 民事诉讼分析、证据整理、文书起草、庭审策略和调解评估 |

两个专家只生成候选意见和待律师复核成果，不替代律师完成案件承接、程序选择、法源核验、金额核算、文书签发或其他专业决定。

## 添加市场

在 WorkBuddy 或 CodeBuddy 的命令入口执行：

```text
/plugin marketplace add jackcheng459/workbuddy-legal-experts
```

添加后，从该市场选择需要的专家插件安装。私有仓库阶段仅仓库授权用户可访问；改为公开仓库后，可直接通过上述仓库标识添加。

## 质量状态

- `execution-counsel` 已通过 WorkBuddy `expert-manager` 结构校验，当前仅有展示描述长度警告。
- `litigation-counsel` 同样通过基础结构校验，但 README 仍含占位内容，Skill 引用了尚未随包提供的 references，并依赖外部 `ai-legal-case-workflow`。在这些问题闭合前，不应标记为正式放行版本。
- 仓库不包含本地备份目录、升级审计目录、`.DS_Store`、客户材料、案件原件、密钥或账号令牌。

详细核验见 [PUBLICATION_REVIEW.md](PUBLICATION_REVIEW.md)。

## 作者与联系

北京海润天睿（郑州）律师事务所 程建都律师

公众号「程律进化论」

微信：`wx1811985798`

## 许可

本仓库暂未授予开源许可。未经权利人另行书面授权，不当然取得复制、修改或再分发权利。
