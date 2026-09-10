# Contributing to CodeLab

本文件定义 CodeLab 在 GitHub 上的最低协作要求，默认适用于组织内所有代码与技术文档仓库。

成员管理、组织制度、权限申请、会议、考勤、奖惩和成果管理制度以飞书 CodeLab 成员手册为准；详细技术规范、代码规范和协作流程统一以 [docs](https://github.com/nynu-codelab/docs) 为准。

## 核心原则

- **单一来源**：GitHub 不复制飞书中的人事和制度内容，只维护技术与协作实现。
- **小步提交**：一个 Issue 对应一个清晰目标，一个 PR 尽量只解决一个问题。
- **全程留痕**：需求、设计、评审、测试、发布和复盘都应有可追踪的 GitHub 记录。
- **自动优先**：能用 Lint、测试、构建或 CI 检查的规则，不依赖口头约定。
- **最小权限**：仓库和团队权限按项目需要授予，不扩散账号、密钥和内部数据。

## 标准工作流

```text
Issue
  -> 从 develop 或 main 创建分支
  -> 开发与本地验证
  -> Commit
  -> Push
  -> Pull Request
  -> CI
  -> Code Review
  -> Merge
  -> Release
```

1. 先创建或认领 Issue，明确目标、范围和验收标准。
2. 从 `develop` 创建分支；没有 `develop` 的短周期项目从 `main` 创建。
3. 完成开发后先执行本地 Lint、测试和构建。
4. Push 分支并创建 Pull Request，关联 Issue。
5. 等待 CI 通过，按 [Code Review 规范](https://github.com/nynu-codelab/docs/blob/main/software/github/code-review.md)完成评审。
6. 满足合并条件后合并，并删除已合并分支。

## 分支模型

```text
main             稳定分支，始终可运行、可发布
  └── develop    集成分支，多人或持续迭代项目使用
       ├── feature/*   新功能
       ├── fix/*       缺陷修复
       ├── docs/*      文档
       ├── refactor/*  重构
       ├── test/*      测试
       └── chore/*     构建、依赖或杂项
```

- `main` 和 `develop` 禁止直接推送。
- 分支名使用小写字母、数字和短横线，例如 `feature/user-login`。
- 长期分支合并前先同步目标分支，减少冲突范围。

## Commit 与 PR 标题

格式：

```text
type(scope): description
```

允许的类型：`feat`、`fix`、`docs`、`style`、`refactor`、`perf`、`test`、`build`、`ci`、`chore`。

示例：

```text
feat(auth): add jwt login
fix(api): handle empty result set
docs(github): clarify review checklist
```

建议使用英文描述，保持简短、明确。完整规则见 [Commit 规范](https://github.com/nynu-codelab/docs/blob/main/software/git/commit-convention.md)。

## Pull Request 要求

- 标题遵循 Commit 规范。
- 描述中写清变更内容、验证方式、影响范围和风险。
- 使用 `Closes #<issue-number>` 关联 Issue。
- 涉及 API、数据库、配置或部署变更时，必须说明兼容性和迁移方案。
- 不混入无关格式化、重构或依赖升级。
- 所有检查通过，至少一位 Reviewer 批准后才能合并；关键规范仓库还要求 `codelab-admin` 作为 Code Owner 批准。

详细流程见 [Pull Request 规范](https://github.com/nynu-codelab/docs/blob/main/software/github/pull-request.md)。

## Teams 与仓库权限

组织只维护三个 team，不按职能细分研发组：

- **software**：全体研发人员。所有代码仓库的默认读写权限授给这个 team；CODEOWNERS 中需要研发团队审批时使用 `@nynu-codelab/software`。
- **achievement**：成果中心成员，负责成果归档、竞赛、论文、专利、软著与企业合作相关仓库。
- **codelab-admin**：组织负责人与全栈开发组长，负责仓库权限、分支保护、规则集和组织级配置；关键规范仓库要求其 Code Owner 批准。具体成员与调整以飞书成员手册为准。

工作边界不靠 team 划分，而写在每个仓库的 `CODEOWNERS` 中：哪个仓库必须谁批准，以该文件为准——部署与 CI 配置归运维负责人，测试资产归测试负责人，业务代码归全栈开发负责人。需要按职能隔离某个仓库时，直接在该仓库授对应个人权限；不为单一职能预先建组。

## Code Review

Reviewer 重点检查：

- 方案是否解决正确的问题，范围是否可控。
- 逻辑、边界条件、异常处理和安全性。
- 测试是否覆盖关键路径和失败场景。
- API、数据库、配置和部署变更是否向后兼容。
- 文档、示例和 Release 说明是否同步更新。

作者应逐条回应 Review 意见。不同意时应说明技术理由，不以“已修改”代替解释。

### codelab-admin 自合并例外

GitHub 不允许 PR 作者批准自己的 Pull Request。`codelab-admin` 成员维护组织级配置时，可以使用规则集的 Pull Request bypass 合并自己的 PR，但必须同时满足：

- 所有必需 CI 状态检查通过，不得绕过检查。
- PR 描述中写明自审结论、验证命令和影响范围。
- 涉及安全、权限、分支保护或组织级规则的重大变更，应邀请另一位 `codelab-admin` 成员复核。
- 合并后如发现问题，立即回滚或提交修复 PR。

该例外只解决作者无法自我批准的问题，不改变其他仓库的 Review 要求。

## 测试与质量

- 新功能和缺陷修复必须补充对应测试，或说明无法自动测试的原因和手工验证步骤。
- 提交 PR 前至少执行项目定义的 `lint`、`test` 和 `build`。
- CI 失败不得合并。
- 测试、构建和发布命令写入项目 `README.md`，避免依赖个人环境知识。

技术方案、测试和发布规范见 [工程流程](https://github.com/nynu-codelab/docs/tree/main/software/engineering)。

## 文档

- 组织级技术规范、工具指南和协作规则维护在 `docs` 仓库。
- 项目特有的方案、接口、部署、测试和复盘文档应随项目版本化维护。
- 代码行为变化时同步更新 README、示例、接口文档和迁移说明。
- 不在 GitHub 复制飞书中的人事、考勤、奖惩和成员管理制度。

## 安全红线

- 不提交密码、API Key、Token、SSH Key、证书私钥或真实 `.env`。
- 不提交实验室或合作企业的内部数据。
- 示例配置只提交 `.env.example`，并保留空值或占位符。
- 发现凭据泄露时，先轮换或吊销凭据，再联系管理员处理历史记录。
- 代码漏洞、依赖告警、配置隐患可以直接开 Issue 公开讨论；凭据类问题先轮换再说明，流程见 [SECURITY.md](SECURITY.md)。

## 新人第一次贡献

1. 从 `good first issue` 或 `documentation` 标签中认领一个小任务。
2. 阅读对应项目的 `README.md` 和 `docs` 中的相关规范。
3. 创建规范分支，完成修改并本地验证。
4. 提交 PR，在描述中说明不清楚的地方。
5. 按 Review 意见修改，完成第一次合并。

## 获取帮助

- 技术问题先查 [docs](https://github.com/nynu-codelab/docs)。
- 项目问题在对应仓库创建 Issue。
- 账号、权限和组织问题通过飞书联系 `codelab-admin`。
- 安全问题和凭据泄露按 [SECURITY.md](SECURITY.md) 处理。
