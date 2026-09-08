# CodeLab .github

CodeLab Organization 的公共配置仓库，存放组织主页、Issue / PR 模板、社区健康文件与共享 GitHub Actions Workflow。

## Overview

`.github` 仓库是 Organization 级配置的唯一入口。GitHub 会自动把本仓库中的模板与社区健康文件应用到组织内所有仓库。

- 组织主页：`profile/README.md`，展示在 <https://github.com/nynu-codelab>
- Issue 模板：`ISSUE_TEMPLATE/`
- PR 模板：`PULL_REQUEST_TEMPLATE.md`
- 社区健康文件：`CONTRIBUTING.md` / `CODE_OF_CONDUCT.md` / `SECURITY.md` / `SUPPORT.md`
- 公共 Workflow：`workflows/`

## Structure

```text
.github/
├── profile/
│   └── README.md          # 组织首页
├── ISSUE_TEMPLATE/
│   ├── bug_report.yml
│   ├── feature_request.yml
│   ├── project_task.yml
│   └── config.yml
├── workflows/
│   ├── markdown-lint.yml  # Markdown 规范检查
│   └── pr-title-lint.yml  # PR 标题格式检查
├── PULL_REQUEST_TEMPLATE.md
├── CONTRIBUTING.md
├── CODE_OF_CONDUCT.md
├── SECURITY.md
├── SUPPORT.md
├── .markdownlint-cli2.yaml
└── README.md
```

## Usage

本仓库由 `codelab-admin` 团队维护。修改模板或健康文件后，通过 Pull Request 提交，经 Review 后合并到 `main`。合并后，改动会自动对所有仓库生效。

## Contributing

参见 [CONTRIBUTING.md](CONTRIBUTING.md)。

## License

[MIT](LICENSE)
