# NYNU CodeLab

CodeLab 是面向本科生的科研与工程实践实验室，聚焦软件工程、AI / Agent、计算机视觉与嵌入式硬件，以真实项目驱动学习，以规范工程流程培养成员。

## 实验室定位

- 以本科生为主体，教师指导、学长带新
- 项目驱动：真实课题、科技竞赛与企业合作项目
- 工程规范：统一 Git 工作流、Code Review、CI/CD
- 成果导向：代码、论文、专利、软件著作权、竞赛奖项

## 四个研发部门

| 部门 | 定位 | 主要方向 |
| --- | --- | --- |
| 软件研发部 | 应用与全栈开发 | Java / Python / TypeScript、Vue / React、Spring Boot、FastAPI |
| 算法研发部 | AI 与视觉算法 | AI / Agent、计算机视觉、工业视觉 |
| 硬件研发部 | 嵌入式与无人机 | 树莓派、嵌入式、无人机 |
| 成果中心 | 成果转化与归档 | 论文、专利、软件著作权、竞赛、企业合作 |

## 技术方向

Java · Python · TypeScript · Vue / React · Spring Boot · FastAPI · AI / Agent · Computer Vision · Docker · Docker Compose · GitHub Actions · GHCR / Harbor · Linux

## 项目方向

- 软件工程实践
- AI / Agent 开发
- 计算机视觉
- 工业视觉
- 无人机
- 树莓派 / 嵌入式
- 科技竞赛
- 企业合作项目

## 科研成果

> 论文、专利、软件著作权等成果由成果中心统一登记与展示（建设中）。

## 企业合作

实验室与行业企业开展合作项目，以真实需求锻炼成员的工程能力。合作项目由成果中心对接与归档，代码仓库仅对相关成员开放。

## 科技竞赛

实验室鼓励成员参加学科竞赛，由成果中心统筹报名、组队与备赛，参赛项目沉淀为实验室可复用的项目资产。

## 如何参与

1. 加入 CodeLab，阅读 [handbook](https://github.com/nynu-codelab/handbook) 了解实验室运行方式
2. 根据兴趣选择部门，获得对应角色
3. 阅读 [docs](https://github.com/nynu-codelab/docs) 学习工具与规范
4. 加入项目，使用 [templates](https://github.com/nynu-codelab/templates) 创建代码仓库
5. 通过 Pull Request 协作，代码 Review 后合并

## 协作方式

| 平台 | 职责 |
| --- | --- |
| 飞书 | 组织架构、日常沟通、知识库、项目管理 |
| GitHub | 代码、Issue、Pull Request、Code Review、CI/CD、Release、项目技术文档 |

## 协作规范（必读）

CodeLab 成员在 GitHub 上的统一协作方式：要做什么、怎么做、能做什么不能做什么。

**要做什么（Git 工作流）**

```text
Issue → 创建分支（feature/*、fix/*、docs/*、refactor/*）→ 开发 → Commit
  → Push → Pull Request → GitHub Actions（CI）→ Code Review → Merge
```

**怎么做（操作指南）**

- Git 入门与常用命令：[docs/git/overview](https://github.com/nynu-codelab/docs/blob/main/git/overview.md)
- 分支模型：[docs/git/branching](https://github.com/nynu-codelab/docs/blob/main/git/branching.md)
- Commit 规范：[docs/git/commit-convention](https://github.com/nynu-codelab/docs/blob/main/git/commit-convention.md)
- Issue / Pull Request / Code Review：[docs/github](https://github.com/nynu-codelab/docs/tree/main/github)
- 贡献总则：[CONTRIBUTING](https://github.com/nynu-codelab/.github/blob/main/CONTRIBUTING.md)

**能做什么、不能做什么**

- 能：按分支模型开发、Commit 遵循规范、PR 关联 Issue、Review 通过后合并
- 不能：直接向 `main` 提交、提交密钥 / `.env` / 大型二进制 / 个人 IDE 配置、未经 Review 合并
- 安全问题不要公开创建 Issue，联系实验室管理员：[SECURITY](https://github.com/nynu-codelab/.github/blob/main/SECURITY.md)
