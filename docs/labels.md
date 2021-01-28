# Issue Labels

Labels or tags like `bug`, `security` or `rbac` (for
[role-based access control][rbac]) will help organizing and sorting all issues.
They can be set at issue creation, as part of a review, by a bot, or when working on it.

[rbac]: https://en.m.wikipedia.org/wiki/Role-based_access_control "See RBAC on Wikipedia"

Currently the project uses over thirty different labels.
This number may grow in the future.

See the [contributing](contributing) page for details on how to use those labels.

1. [Epics](#epics)
2. [Helpers](#helpers)
3. [Status](#status)
4. [Priority](#priority)
5. [Types](#types)
6. [GitHub](#github)

## Epics

An epic is an issue that points to a list of other issues,
thus enabling Agile processes.

In this project, an epic corresponds to a particular component or team.

| **Label**       | **Description**                                                       |
| --------------- | --------------------------------------------------------------------- |
| api 👽           | Issues or PRs related to GraphGL, ONIX, B2B, etc.                     |
| rbac 🛂          | Issues or PRs related to authorization, roles and permissions         |
| core 🐼          | Issues or PRs related to Panda Core, Composer, Bedrock or CP          |
| design 🎨        | Issues or PRs related to pandastic theme or assets like SCSS and SVGs |
| documentation 📝 | Improvements or additions to documentation                            |
| environments 👷  | Control CI/CD workflows and pipelines                                 |
| infra 🔧         | Issues or PRs related to infrastructure like Docker or dev scripts    |
| php ⚙️           | Issues or pull requests that update PHP code                          |

## Helpers

Issues can be tagged with one of the following helper labels.

| **Label**     | **Description**                                   |
| ------------- | ------------------------------------------------- |
| dontmerge ❌   | This pull request needs testing or refactoring    |
| duplicate ♻️   | This issue or pull request already exists         |
| enhancement 🎉 | New feature or request                            |
| epic 🔖        | Large user story linking to sub-tasks             |
| milestones 🚀  | Big things are happening here                     |
| todos ✅       | This issue contains a To-Do list of pending tasks |

## Status

An issue can have one of the following states.

| **Label**      | **Description**                                |
| -------------- | ---------------------------------------------- |
| blocker ⛔      | We cannot go live until this is fixed          |
| confidential 🛡️ | Kept secret for privacy or security reasons    |
| released ✈️     | Yay, we're going live!                         |
| wip 🚧          | This issue or pull request is work in progress |
| wontfix 🚫      | This will not be worked on                     |

## Priority

The priority label helps understanding the urgency of a task during sprint planning.

| **Label**  | **Description**                        |
| ---------- | -------------------------------------- |
| critical 🚑 | Please, fix me NOW!                    |
| high ‼️     | I'm having major priority              |
| medium ❗   | I'm having normal priority             |
| low ❕      | Don't worry, I'm having minor priority |

## Types

Type labels indicate the primary purpose of an issue.

| **Label**         | **Description**                                               |
| ----------------- | ------------------------------------------------------------- |
| breaking-change 💣 | Breaking backward compatibility                               |
| bug 🐛             | Something isn't working                                       |
| dependencies ⬆️    | Pull requests that update a dependency file                   |
| feature ✨         | Suggest an idea for Panda                                     |
| feedback 💬        | Tell us what you think about Panda                            |
| help wanted 🆘     | Extra attention is needed                                     |
| invalid ❎         | This doesn't seem right                                       |
| performance ⚡️     | Cache, Minify, CDN, Memory, Storage, Transmission speed, etc. |
| question ❓        | Further information is requested                              |
| security 🔒        | Dependency updates, code audits, system hardening, etc.       |

## GitHub

Labels can also be used for issues related to GitHub repos, team memberships, etc.

| **Label**               | **Description**                                              |
| ----------------------- | ------------------------------------------------------------ |
| area/github-integration | Third-party integrations, webhooks, or GitHub Apps           |
| area/github-management  | Issues or PRs related to GitHub Management                   |
| area/github-membership  | Requesting membership in a Panda GitHub Organization or Team |
| area/github-repo        | Creating, migrating or deleting a Panda GitHub Repository    |
| area/github-permissions | Permissions requests and problems                            |
| github_actions          | Pull requests that update Github_actions code                |
| good first issue        | Good for newcomers                                           |
