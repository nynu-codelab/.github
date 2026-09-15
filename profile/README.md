<div align="center">

# NYNU CodeLab

A student engineering and research lab at Nanyang Normal University.

We build open-source software the way professional teams do — specification first,
review-gated pull requests, and CI on every change.

Nanyang, Henan, China

</div>

---

## What we do

CodeLab is a lab for undergraduates who want to ship real software rather than finish
exercises. Members take a project from requirement to release inside the same pipeline a
professional team would use, and every artifact of that pipeline is public: the standards,
the review, and the tests.

## Where the rules live

组织制度、协作规范与流程统一维护在飞书 CodeLab 共享文件夹（`工程规范` 目录），GitHub 上只保留代码、项目技术文档与表单骨架。

| 内容 | 位置 |
| --- | --- |
| 组织架构与成员制度 | 飞书《成员手册》 |
| 一条需求从提出到上线的完整链路 | 飞书《协作流程》 |
| Git、分支、Commit、Issue、PR、Code Review、工程流程 | 飞书《软件研发协作规范》 |
| 建仓库、权限、分支保护 | 飞书《仓库与权限规范》 |
| 安全基线与资产交接 | 飞书《工程安全基线与资产交接》 |
| 行为准则、安全策略与求助渠道 | 飞书《组织协作总则与行为规范》 |
| 接口文档、数据库设计、技术方案、测试用例、部署说明、复盘记录 | 各项目仓库 |

## How we work

```text
requirement  →  technical design  →  interface contract  →  pull request
     →  CI  →  code review  →  merge  →  release  →  retrospective
```

Every non-trivial change arrives as a pull request against `main`, is validated by CI, and
is approved by a code owner before merge. Commit messages, branch names, issue labels and
pull request bodies follow one published convention.

## Repositories

| Repository | What it is |
| --- | --- |
| [**codelab-web**](https://github.com/nynu-codelab/codelab-web) | Official website and recruitment management system (Spring Boot 3 · Vue 3 · MySQL · Redis) |
| [**lab-member-system-docs**](https://github.com/nynu-codelab/lab-member-system-docs) | Onboarding project briefs — a member management system specified end to end |
| [**.github**](https://github.com/nynu-codelab/.github) | Organization-wide collaboration defaults: issue and pull request templates, community health files, reusable workflows |

## Teams

| Team | Scope |
| --- | --- |
| `codelab-admin` | 队长与组织所有者 — repository setup, permissions, security baseline |
| `members` | CodeLab 全体成员 — all repositories |

## Joining

招新由实验室统一组织，具体安排以群内通知为准。加入后的第一步见飞书《成员手册》的「新人指引」：从新人入门项目仓库 [`lab-member-system-docs`](https://github.com/nynu-codelab/lab-member-system-docs) 开始。

## Disclaimer

This organization and its projects are maintained by the CodeLab student lab. They are not
official portals of Nanyang Normal University.

## License

Content and code are released under the license declared in each repository, unless stated
otherwise.
