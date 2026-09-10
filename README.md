# CodeLab .github

CodeLab 组织的公共配置仓库：组织主页、Issue / PR 模板、社区健康文件、CODEOWNERS 与共享 GitHub Actions workflow。

## 这是什么

`.github` 是 Organization 级特殊仓库，GitHub 会自动把其中的模板与社区健康文件作为组织内所有仓库的默认值：

- 组织主页：`profile/README.md`，展示在 <https://github.com/nynu-codelab>
- Issue 模板：`ISSUE_TEMPLATE/`
- PR 模板：`PULL_REQUEST_TEMPLATE.md`
- 社区健康文件：`CONTRIBUTING.md` / `CODE_OF_CONDUCT.md` / `SECURITY.md` / `SUPPORT.md`
- 共享 workflow 模板与本仓库 CI：`.github/workflows/`
- 审批线：`.github/CODEOWNERS`

## 目录结构

```text
.github/
├── .github/
│   ├── CODEOWNERS              # 审批线：默认 software，workflows 归 codelab-admin
│   └── workflows/
│       ├── markdown-lint.yml   # Markdown 规范检查（CI）
│       └── pr-title-lint.yml   # PR 标题 Conventional Commits 检查（CI）
├── profile/
│   └── README.md               # 组织主页
├── ISSUE_TEMPLATE/
│   ├── bug_report.yml
│   ├── feature_request.yml
│   ├── project_task.yml
│   └── config.yml
├── PULL_REQUEST_TEMPLATE.md
├── CONTRIBUTING.md
├── CODE_OF_CONDUCT.md
├── SECURITY.md
├── SUPPORT.md
├── .markdownlint-cli2.yaml
├── .gitignore
├── LICENSE
└── README.md
```

## 怎么维护

权限模型与全组织一致（见 [docs 协作规范](https://github.com/nynu-codelab/docs)）：

| Team | 权限 | 职责 |
| --- | --- | --- |
| codelab-admin | Maintain | 仓库设置、分支保护、workflow 改动审批 |
| software | Write | 推分支、开 PR、默认审批人 |

改动流程：

1. 从 `main` 切分支：`docs/*`、`chore/*`、`ci/*`
2. 走 Pull Request，标题遵循 Conventional Commits（`type(scope): description`）
3. CI（Markdown Lint、PR Title Lint）通过并完成 review 后，squash 合并到 `main`
4. 模板与社区健康文件合并后自动对全组织生效；`.github/workflows/` 改动按 CODEOWNERS 由 `codelab-admin` 审批

协作细节（分支模型、commit 规范、禁止事项）见 [CONTRIBUTING.md](CONTRIBUTING.md)。

## License

[MIT](LICENSE)
