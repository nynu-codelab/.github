# CodeLab .github

CodeLab Organization 的公共配置仓库，维护组织主页、默认 Issue / PR 模板、社区健康文件和 GitHub 工作流。

## 内容边界

本仓库只负责 GitHub 平台配置和协作入口，不维护实验室人事、组织制度或成员管理内容。技术与协作规范的唯一来源是 [docs](https://github.com/nynu-codelab/docs)。

## Structure

```text
.github/
├── profile/
│   └── README.md                    # 组织主页
├── ISSUE_TEMPLATE/
│   ├── bug_report.yml               # 缺陷
│   ├── feature_request.yml          # 功能建议
│   ├── project_task.yml             # 项目任务
│   ├── documentation.yml            # 文档任务
│   ├── technical_debt.yml           # 技术债
│   └── config.yml                   # Issue 模板配置
├── workflow-templates/              # Organization 可选工作流模板
├── .github/workflows/               # 本仓库自身的检查工作流
├── PULL_REQUEST_TEMPLATE.md
├── CODEOWNERS
├── CONTRIBUTING.md
├── CODE_OF_CONDUCT.md
├── SECURITY.md
├── SUPPORT.md
├── .markdownlint-cli2.yaml
└── README.md
```

## 自动生效范围

GitHub 会默认读取本仓库的 Issue / PR 模板和社区健康文件。`.github/workflows/` 中的工作流只检查本仓库自身；其他仓库需要按需复制或调用工作流，`workflow-templates/` 提供可复用入口。

## 修改流程

本仓库由 `codelab-admin` 维护。修改默认模板、协作规则或安全策略时，通过 Pull Request 提交并完成 Review。

## 规范入口

- 组织协作总则：[CONTRIBUTING.md](CONTRIBUTING.md)
- 技术文档与协作规范：[docs](https://github.com/nynu-codelab/docs)
- 项目模板：[templates](https://github.com/nynu-codelab/templates)
- 安全问题：[SECURITY.md](SECURITY.md)

## License

[MIT](LICENSE)
