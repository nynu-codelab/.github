<div align="center">

# NYNU CodeLab

A student engineering and research lab at Nanyang Normal University.

We build open-source software the way professional teams do — specification first,
review-gated pull requests, and CI on every change.

Nanyang, Henan, China · [Contribution guide](https://github.com/nynu-codelab/.github/blob/main/CONTRIBUTING.md) · [Security policy](https://github.com/nynu-codelab/.github/blob/main/SECURITY.md) · [Code of conduct](https://github.com/nynu-codelab/.github/blob/main/CODE_OF_CONDUCT.md)

</div>

---

## What we do

CodeLab is a lab for undergraduates who want to ship real software rather than finish
exercises. Members take a project from requirement to release inside the same pipeline a
professional team would use, and every artifact of that pipeline is public: the standards,
the review, and the tests.

## How we work

```text
requirement  →  technical design  →  interface contract  →  pull request
     →  CI  →  code review  →  merge  →  release  →  retrospective
```

Every non-trivial change arrives as a pull request against `main`, is validated by CI, and
is approved by a code owner before merge. Commit messages, branch names, issue labels and
pull request bodies follow one published convention, so review can focus on substance.

## Repositories

| Repository | What it is |
| --- | --- |
| [**docs**](https://github.com/nynu-codelab/docs) | Engineering and collaboration standards — Git, GitHub, code review, testing, release, CI/CD |
| [**codelab-web**](https://github.com/nynu-codelab/codelab-web) | Official website and recruitment management system (Spring Boot 3 · Vue 3 · MySQL · Redis) |
| [**.github**](https://github.com/nynu-codelab/.github) | Organization-wide collaboration defaults: issue and pull request templates, community health files, reusable workflows |
| [**lab-member-system-docs**](https://github.com/nynu-codelab/lab-member-system-docs) | Onboarding project briefs — a member management system specified end to end |

## Teams

| Team | Scope |
| --- | --- |
| `codelab-admin` | Organization owners and project leads — repository setup, permissions, security baseline |
| `software` | Software engineering members — all development repositories |
| `achievement` | Write access scoped to achievement and archive repositories |

## Joining

Recruitment runs through the [official website](https://github.com/nynu-codelab/codelab-web),
which manages the application and review workflow. New members start with the onboarding
brief in [`lab-member-system-docs`](https://github.com/nynu-codelab/lab-member-system-docs)
and the standards in [`docs`](https://github.com/nynu-codelab/docs) before their first pull
request.

## Disclaimer

This organization and its projects are maintained by the CodeLab student lab. They are not
official portals of Nanyang Normal University.

## License

Content and code are released under the license declared in each repository, unless stated
otherwise.
