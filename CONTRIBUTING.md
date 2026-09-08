# Contributing to CodeLab

欢迎参与 CodeLab 的项目。本文件定义了 CodeLab 统一的 Git 协作方式，所有仓库默认遵循。

## Git 工作流

分支模型：

```text
main         稳定分支，始终可运行
  └── develop    开发分支，集成分支
       ├── feature/*   新功能
       ├── fix/*       修复 Bug
       ├── docs/*      文档
       └── refactor/*  重构
```

### 基本流程

```text
Issue
  ↓ 创建分支
开发
  ↓ Commit
Push
  ↓ Pull Request
GitHub Actions（CI）
  ↓ Code Review
Merge
```

1. 在 GitHub 上创建 Issue，描述要做什么
2. 从 `develop` 创建分支：`feature/xxx`、`fix/xxx`、`docs/xxx`、`refactor/xxx`
3. 本地开发并 Commit
4. Push 到远程
5. 创建 Pull Request，关联 Issue
6. 等待 CI 通过，接受 Code Review
7. Review 通过后 Merge

## Commit Convention

格式：`type(scope): description`

| type | 含义 | 例子 |
| --- | --- | --- |
| `feat` | 新功能 | `feat(auth): add login page` |
| `fix` | 修复 Bug | `fix(api): fix null pointer on empty list` |
| `docs` | 文档 | `docs: update README` |
| `style` | 格式调整（不影响逻辑） | `style: format code with prettier` |
| `refactor` | 重构（不改功能） | `refactor: extract user service` |
| `perf` | 性能优化 | `perf: cache hot query results` |
| `test` | 测试 | `test: add unit tests for calculator` |
| `build` | 构建相关 | `build: bump spring boot to 3.3` |
| `ci` | CI 配置 | `ci: add python lint job` |
| `chore` | 杂项 | `chore: update .gitignore` |

建议使用英文写 commit message，保持简洁。

## 禁止事项

- 不允许直接向 `main` 提交（只能通过 PR 合并）
- 不要提交密码、API Key、token
- 不要提交 `.env`、`application-local.yml` 等含真实配置的文件
- 不要提交大型二进制文件（>10MB，请使用 Release 或对象存储）
- 不要提交个人 IDE 配置（`.idea/`、`.vscode/` 等，见 `.gitignore`）
- PR 必须经过至少一位 Review，`main` 分支强制要求
- CI 必须通过才能合并

## 代码规范

- 每个仓库遵循 `templates` 中对应模板的规范
- 代码必须有必要的注释和可读的命名
- 新功能必须有测试（单元测试或至少手动验证说明）

## 其他

- 有疑问先搜索 Issue 和 [docs](https://github.com/nynu-codelab/docs)
- 不确定怎么做时，在 PR 中直接提问，Reviewer 会帮你
- 新人第一次提交 PR 前，建议先做一个 `docs` 或 `test` 类型的小改动练手
