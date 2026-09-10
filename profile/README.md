# NYNU CodeLab

CodeLab 是南阳师范学院面向本科生设立的科研与工程实践实验室。GitHub 组织用于承载代码、技术文档、工程规范与协作流程；成员管理、组织制度和日常沟通由飞书负责。

## 仓库导航

| 仓库 | 用途 | 入口 |
| --- | --- | --- |
| `docs` | 技术文档与协作规范，GitHub 上相关内容的唯一来源 | <https://github.com/nynu-codelab/docs> |
| `.github` | 组织主页、默认 Issue / PR 模板、安全与支持说明 | <https://github.com/nynu-codelab/.github> |
| `codelab-web` | 实验室官方网站 | <https://github.com/nynu-codelab/codelab-web> |
| `lab-member-system-docs` | 新人入门项目题目与成果提交入口 | <https://github.com/nynu-codelab/lab-member-system-docs> |

组织不维护"复制即用"的项目模板。新项目按规范从零搭建，一致性由分支保护、CODEOWNERS 和 CI 检查保证——提交不合规时由 CI 直接指出要改什么。

## 开始协作

1. 阅读 [CONTRIBUTING.md](https://github.com/nynu-codelab/.github/blob/main/CONTRIBUTING.md)，了解统一协作流程。
2. 按任务类型阅读 [docs](https://github.com/nynu-codelab/docs) 中的 Git、GitHub、测试、发布和技术栈规范。
3. 新建仓库时按 [仓库规范](https://github.com/nynu-codelab/docs/blob/main/codelab-admin/repository.md) 与 [新仓库权限配置](https://github.com/nynu-codelab/docs/blob/main/codelab-admin/repository-setup.md) 配好权限、CODEOWNERS、分支保护、安全开关和标准检查工作流。
4. 通过 Issue、分支、Pull Request、CI 和 Code Review 完成交付。

## 统一工作流

```text
Issue
  -> 创建分支
  -> 开发与本地验证
  -> Commit
  -> Push
  -> Pull Request
  -> GitHub Actions
  -> Code Review
  -> Merge
  -> Release
```

## 工程底线

- 不直接向受保护的 `main` 分支提交代码。
- 每个 PR 只解决一个明确问题，并关联对应 Issue。
- Commit 与 PR 标题使用 Conventional Commits 格式。
- CI、测试和 Code Review 通过后才能合并。
- 不提交密码、Token、`.env`、真实数据库连接串或企业敏感数据。
- 技术方案、接口、部署、测试与复盘文档随项目版本化维护。

## 平台边界

| 平台 | 负责内容 |
| --- | --- |
| 飞书 | 组织架构、角色职责、入组与权限、会议、考勤、奖惩、成果与保密制度 |
| GitHub | 代码、Issue、Pull Request、Code Review、CI/CD、Release、技术方案、接口、部署与复盘文档 |

`CodeLab 成员手册`（组织架构、入组与权限、会议、考勤、奖惩、成果与保密制度）在飞书知识库维护，以飞书版本为唯一权威；GitHub 侧不复制这些内容。

## 安全

不要在公开 Issue 中报告安全漏洞或泄露凭据。处理方式见 [SECURITY.md](https://github.com/nynu-codelab/.github/blob/main/SECURITY.md)。
