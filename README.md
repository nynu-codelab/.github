# CodeLab .github

CodeLab 组织的公共配置仓库。这里只保留 GitHub 平台自身的运行部件：Issue / Pull Request 模板、社区健康文件与可复用工作流。

## 内容边界

本仓库**不承载制度、规范、流程或技术文档内容**。这些内容统一维护在飞书 CodeLab 共享文件夹（`工程规范` 目录）：

- [组织协作总则与行为规范](https://mcnccybqf361.feishu.cn/docx/CSUSdGzDGoFS31x2WLWciL4GnQg)
- [软件研发协作规范](https://mcnccybqf361.feishu.cn/docx/EynwdC2NmoXtccxMQBCc4Kkrnmh)
- [仓库与权限规范](https://mcnccybqf361.feishu.cn/docx/VER4dT8tbo4TEyxT3UNcmzj6nVg)
- [工程安全基线与资产交接](https://mcnccybqf361.feishu.cn/docx/Lwg6dna4Loa4TSxJHNyceK3DnWc)

制度与流程见飞书 [成员手册](https://mcnccybqf361.feishu.cn/docx/QcrBd22vFo1NfSxHNoEcZWHZnfF) 与 [协作流程](https://mcnccybqf361.feishu.cn/docx/VK2gdUejDoLZYyxrYZJcsuoJnPc)。

## Structure

```text
.github/
├── ISSUE_TEMPLATE/          # 表单骨架，新增 Issue 时自动出现
├── workflow-templates/      # Organization 可选工作流模板
├── .github/workflows/       # 本仓库自身的检查工作流
├── PULL_REQUEST_TEMPLATE.md # PR 表单骨架
├── CODEOWNERS               # 审批人名单
├── CONTRIBUTING.md          # 入口，指向飞书
├── CODE_OF_CONDUCT.md       # 入口，指向飞书
├── SECURITY.md              # 入口，指向飞书
├── SUPPORT.md               # 入口，指向飞书
├── .markdownlint-cli2.yaml
└── README.md
```

## 自动生效范围

GitHub 会默认读取本仓库的 Issue / PR 模板和社区健康文件。`.github/workflows/` 中的工作流只检查本仓库自身；其他仓库需要按需复制或调用工作流，`workflow-templates/` 提供可复用入口。

## 修改流程

本仓库由 `codelab-admin` 维护。修改默认模板或工作流时，通过 Pull Request 提交并完成 Review。

## License

[MIT](LICENSE)
