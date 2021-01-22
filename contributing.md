# Contributing

Thanks for your interest in contributing to Panda!

As you might have expected,
contributions are welcome.

1. [Collaboration policy](#collaboration-policy)
2. [Organization](#organization)
3. [Code of Conduct](#code-of-conduct)
4. [Key concepts](#key-concepts)
5. [Kanban](#kanban)
6. [User stories](#user-stories)
7. [Epics](#epics)
8. [Milestones](#milestones)
9. [Issues workflow](#issues-workflow)
10. [Feature requests](#feature-requests)
11. [Bug reports](#bug-reports)
12. [Merge requests](#merge-requests)
13. [Writing Documentation](#writing-documentation)
14. [Some hints for newbies](#some-hints-for-newbies)
15. [Submitting a pull request](#submitting-a-pull-request)
16. [Coding guidelines](#coding-guidelines)
17. [Resources](#resources)

## Collaboration policy

> 💁🐼 Contributing to Panda is not different from other projects.

Our **collaboration policy** communicates how best to work together on this project. Basically, only a few basic rules need to be observed.

* [x] **1. Respect and solidarity come first!** Our code of conduct explains community standards that need to be taken into account when interacting with this project.
* [x] **2. Comrade, we need you!** There are many ways to contribute; no need to be a technician or developer. Every help and every feedback is appreciated.
* [x] **3. Consider talking before acting!** When contributing to this project we first discuss the proposed changes in the team via new issue, email, or any other method.
* [x] **4. Issues can be everything!** No matter whether bugs, tasks, or ideas to be discussed – the issue tracker is the best place to add things that need to be improved or solved in this project.

In case you are contributing to this project for the first time, it would be nice if you could briefly introduce yourself, telling us about your interest in the project and related experiences.

> <3 **Thanks a lot for your interest in contributing to Panda!** <3

## Organization

Visit [Team panda!] for details.

This project is organized as follows:

> **[Roadmap] > [Milestones] > [Epics] > [Issues]**

[Team panda!]: https://github.com/orgs/pandainfo/teams/panda
[Roadmap]: https://github.com/pandainfo/panda/projects/2 "Panda Roadmap"
[Milestones]: https://github.com/pandainfo/panda/milestones "Panda Milestones"
[Epics]: https://github.com/pandainfo/panda/issues?q=is%3Aissue+label%3Aepic "Panda Epics"
[Issues]: https://github.com/pandainfo/panda/issues "Panda Issues"

An issue can be a [feature request] or enhancement formulated as a user story, a [bug report], or a proposed patch submitted as a [pull request].

[feature request]: https://github.com/pandainfo/panda/issues/new?assignees=redtux&labels=enhancement&template=feature-request.md&title= "Create a new feature request"
[bug report]: https://github.com/pandainfo/panda/issues/new?assignees=redtux&labels=bug&template=bug-report.md&title= "Create a new bug report"
[pull request]: https://github.com/pandainfo/panda/pulls?q=is%3Apr "Show pull requests"

Not only code contributions
but also help with docs, e.g.
translations, proofreading,
etc. is highly appreciated.

We accept pull requests for bug fixes and features,
and welcome discussing the approach in an issue.

We would also love to hear about ideas for new features as issues.

Contributions to this project are released under the [AGPLv3 license][license].

Please note that this project adheres to a [Contributor Code of Conduct][code-of-conduct].
By participating in this project you agree to abide by its terms.

[license]: LICENSE.md
[code-of-conduct]: code-of-conduct.md

## Code of Conduct

Our Code of Conduct has been adapted from the [Contributor Covenant], version 2.0,
available at [https://www.contributor-covenant.org/version/2/0/code_of_conduct/][CoC-version].

The Contributor Covenant was created by [Coraline Ada Ehmke] in 2014 and is released under the [CC BY 4.0][cc-by-4.0] license.

For answers to common questions about their Code of Conduct, please see [https://www.contributor-covenant.org/faq][CoC-FAQ].

[Contributor Covenant]: http://contributor-covenant.org "A Code of Conduct for Open Source Projects"
[CoC-version]: https://www.contributor-covenant.org/version/2/0/code_of_conduct/ "Contributor Covenant CoC version 2.0"
[Coraline Ada Ehmke]: https://where.coraline.codes/
[cc-by-4.0]: https://creativecommons.org/licenses/by/4.0/legalcode "Creative Commons Attribution 4.0 International Public License"
[CoC-FAQ]: https://www.contributor-covenant.org/faq "Contributor Covenant: Frequently Asked Questions"

## Key concepts

Our development workflow consists of several basic [Agile](https://en.m.wikipedia.org/wiki/Agile_software_development) principles.

In accordance with the [Agile Manifesto] we value:

* ***Individuals and interactions** over processes and tools*
* ***Working software** over comprehensive documentation*
* ***Customer collaboration** over contract negotiation*
* ***Responding to change** over following a plan*

[Agile Manifesto]: http://agilemanifesto.org/ "Manifesto for Agile Software Development"

Team members should be more or less familiar with these concepts:

* [x] [Kanban system](https://en.m.wikipedia.org/wiki/Kanban_(development))
* [x] [DevOps toolchain](https://en.m.wikipedia.org/wiki/DevOps_toolchain)
* [x] [CI](https://en.m.wikipedia.org/wiki/Continuous_integration)/[CD](https://en.m.wikipedia.org/wiki/Continuous_delivery)
* [x] [Application lifecycle management](https://en.m.wikipedia.org/wiki/Application_lifecycle_management)
* [x] [User stories](https://en.m.wikipedia.org/wiki/User_story)
* [x] [Issues](https://en.m.wikipedia.org/wiki/Software_project_management#Issue)
* [x] [Bug reports](https://www.mediawiki.org/wiki/How_to_report_a_bug)
* [x] [Feature requests](https://en.m.wikipedia.org/wiki/Software_feature)
* [x] [Epics](https://en.wiktionary.org/wiki/epic)
* [x] [Semantic Versioning](https://semver.org/) (MAJOR.MINOR.PATCH)
* [x] [Release cycles](https://en.m.wikipedia.org/wiki/Software_release_life_cycle)
* [x] [Milestones](https://en.m.wikipedia.org/wiki/Milestone_(project_management))

## Kanban

Project management for Panda development is based on a methodology called Kanban.

Originating in the automotive industry, Kanban has been introduced to the IT industries by [David J. Anderson](https://web.archive.org/web/20100110013417/http://www.agilemanagement.net/Articles/hidden/Biography.html) over ten years ago.

The initial Kanban project management system has been pioneered in Japan, being developed by Taiichi Ohno as part of the [Toyota Production System](https://en.m.wikipedia.org/wiki/Toyota_Production_System).

TPS or Toyotism is a production model and management theory that followed the paradigm of Fordism-Taylorism in the post-war period.

Taylorism and Fordism emerged from the efficiency movement in the decade between 1905 and 1915 and remained the predominant mode of production worldwide until the late 1970s.

The Toyota system – with Kanban at its heart – has been developed between 1948 and 1975, revolutionizing the modern mode of production. It became predominant in the era of post-fordism and neoliberal globalization in the 1980's.

Both paradigms – Fordism-Taylorism and Toyotism – aim to maximize efficiency and output while identifying and eliminating waste in all areas of the economy and society.

Toyota's Taiichi Ohno identifies seven wastes in a typical manufacturing workflow, called [Muda](https://en.m.wikipedia.org/wiki/Muda_(Japanese_term)#Toyota's_(Ohno's)_Seven_Forms_of_Waste) in Japanese.

* [x] Overproduction (largest waste)
* [x] Waiting
* [x] Transportation
* [x] Overprocessing
* [x] Inventory
* [x] Motion
* [x] Defects (broken products)
* [x] Underutilized workforce

Based on the wording of Lean Production and Lean Manufacturing coming – from the automotive industry as well –, we sometimes speak of Lean Methods, Lean Management, Lean IT, Lean Development, Lean Services, Lean Maintenance, etc.

At the end of the twentieth century terms like Just-in-Time production (JIT), Short-cycle manufacturing (SCM), or Continuous-flow manufacturing (CFM) have been in use for similar philosophies.

The continuous improvement process - called [Kaizen](https://en.m.wikipedia.org/wiki/Kaizen) in Japanese - is an essential part of Kanban.

The main idea behind Kanban is to minimize the lead time or workload between releases (see [value chain](https://en.wikipedia.org/wiki/Value_chain) and [supply chain](https://en.wikipedia.org/wiki/Supply_chain)) by keeping the number of work in progress (i.e. tasks processed in parallel) low – and to maximize the number of deployments and releases by using CI/CD automation.

The progress is visualized and prioritized on the Kanban board. Each task or user story is represented by a post-it note on a whiteboard.

The Kanban board is split into various columns representing the status of an issue.

* **To do** means this issue still needs to be worked on. (This can be a new issue or an older issue coming from the backlog.)
* **In progress** means somebody is already working on the issue. (This can be analyzing, bug fixing, reviewing, or even rejecting.)
* **Done** means just that. (Somebody took care and created a PR. Someone else did a review and closed the issue.)

## User stories

Each major task is broken down into a manageable number of smaller tasks.

The smallest entity is an issue – representing a simple user story.

The user story informs other team members or external contributors about the who, what, and why of an issue making use of signal words, keywords and tags.

> As administrator I want to have permission to lock or delete standard user accounts.

From this example all contributors should recognize on the spot that

1. The user type is the admin role.
2. The task is the implementation of permission handling.
3. The goal is locking or deleting an existing user.

Try to clarify your request or user story with code examples and sketches such as

* screenshots with manual markings
* [mockups](https://en.m.wikipedia.org/wiki/Mockup#Software_engineering) (see: [mock object](https://en.m.wikipedia.org/wiki/Mock_object))
* [scribbles or doodles](https://en.m.wikipedia.org/wiki/Doodle)

## Epics

Epics are like chapters
Depending on the estimated workload a task can be divided into several sub-tasks. Such big issues are called epics.

Think of an epic as a large user story (like our role-based security example) represented by an issue with the label `epic`.

This issue or ticket should include a checklist of linked sub-tasks needed to be completed in order to close the epic.

Each issue or epic in turn needs to be linked to a Kanban project.

According to the nature of the issue and the team that will be working on it, this can be

* api
* core
* design
* documentation
* environment

## Milestones

A milestone defines the chunk of work planned for the next major release. It shows the big picture of what needs to be done to bring our project to the next level.

Think of milestones as anchors or markers for our major goals.

The four-weeks lasting period between milestones is called a sprint.

## Issues workflow

It is considered best practice to search the issue tracker for similar entries before submitting a new issue. There is a good chance that someone else already had the same issue, change request or feature proposal.

Showing support with an emoji at the respective comment is appreciated as much as taking part in the discussion.

Tags or labels like `bug`, `security` or `rbac` (for [role-based access control](https://en.m.wikipedia.org/wiki/Role-based_access_control)) will help organizing and sorting our issues. They can be set at issue creation, as part of a review, or when working on it.

Currently we use 21 different labels. This number may grow in the future.

Most issues will have labels for at least one of the following types:

* `api`
* `bug`: *Something isn't working.* This label is for bug reports, i.e. for issues that report undesirable or incorrect behavior.
* `confidential`: *Kept secret for privacy or security reasons.* This label is for confidential data. The content of the issue or comments contains references to private user information, such as private repository paths, and its contents should remain confidential indefinitely. This is usually primarily used for `security` or production issues.
* `core`
* `customer`: *Subscribers may get quicker support.* This label is for issues that were reported by paying **Panda Supporters' Edition** subscribers, indicating higher priority. This label should be accompanied by either the `bug` or `feature` label.
* `dependencies`: *Pull requests that update a dependency file.* This label shall be used when updating manifest files for Python pip, npm, PHP Composer, Ruby Bundler, Docker, etc.
* `documentation`: *Improvements or additions to documentation.* This label is for issues and PRs/MRs that only require a documentation change, to differentiate from those coupled with a feature change. This label can be used for epics, issues, and merge requests related to product documentation.
* `duplicate`: *This issue or pull request already exists.* Duplicates should be closed with an explanatory note and a link pointing to the original issue.
* `enhancement`: *New feature or request.* This label can refine an issue that has the `feature` label. This is for issues that propose improvements to existing features.
* `environments`: *Control CI/CD workflows and pipelines.* This label is for issues about [environments and deployments](https://docs.gitlab.com/ee/ci/environments.html).
* `epic`: *Large user story linking to sub-tasks.* This label is for task checklists of linked issues.
* `feature`: *Suggest an idea for Panda.* This label is for any issue (feature request or PR/MR) that contains work to support the implementation of a feature and/or results in an improvement in the user experience.
* `feedback`: *Tell us what you think about Panda.* This issue type is meant to give general feedback or to just leave a note.
* `design`
* `github_actions`: *Pull requests that update Github_actions code.*
* `good first issue`: *Good for newcomers.* This label will be set automatically.
* `help wanted`: *Extra attention is needed.* This label indicates that work on an issue is stuck.
* `invalid`: *This doesn't seem right.*
* `milestones`: *Big things are happening here.* This label is for issues related to the [Milestones feature](https://docs.gitlab.com/ce/user/project/milestones/) on issues and merge requests.
* `php`: *Pull requests that update PHP code.*
* `production::blocker`: *We cannot go live until this is fixed.* This label is for issues that block the deployment to production.
* `question`: *Further information is requested.* This label indicates that we are waiting for input by the reporter.
* `security`: *Dependency updates of insecure libraries, code audits, system hardening.* This label is for issues related to the security of Panda or its dependencies. It is asked to report severe vulnerabilities responsibly per GPG encrypted mail, via Signal, or through another secure channel.
* `todos`: This label is for issues related to the [To-Do list feature](http://doc.gitlab.com/ce/workflow/todos.html). To-Do lists offer a dashboard with a chronological list of items that are waiting for input.
* `wontfix`: *This will not be worked on.*

## Feature requests

To request a change to the way Panda works, opening an issue is enough. The team will regularly discuss new feature requests, and consider the top three suggestions.

## Bug reports

Everybody knows: Bugs are unfortunate, but a reality in software. As we cannot fix what we do not know about, we kindly ask everybody to report generously.

If you are not sure whether something is a bug or not, feel free to file a bug anyway.

**If you believe that reporting your bug publicly poses a security risk to our users, please contact us via email.**

## Merge requests

Our team loves merge requests from everyone. By participating in this project, readers agree to abide by our code of conduct.

NB: It should be noted that _merge requests_ here are equivalent to what others may call _pull requests_.

Merge requests are a place to propose changes made to a project, and to discuss those changes with others.

Interested parties can even contribute by directly pushing commits to a proper development branch if they want to.

Merge requests are the preferred method for code review and change management in this project. By this an assigned team member can be asked to merge two branches – development and feature branch.

After a review and discussion process the `git merge` command successfully will be the final action that is requested of the assignee, therefore the name of this approach.

Merge requests lead to higher-quality code by involvement of as many team members as possible, both checking code quality and assuring compliance with coding standards.

1. It must be ensured that any install or build dependencies are removed before the end of the layer when performing a build.
2. The `README.md` file and the respective documentation must be updated with details of relevant changes. This includes new environment variables, exposed ports, useful file locations and container parameters.
3. The version number in any sample files, in the environment variables, in the `README.md` file, etc. must be increased to the new version that this merge request would represent. The version scheme used is SemVer.
4. A Merge request may be completed with the `git merge` command by the contributors themselves – given the permission, a so-called [Sign-off], from at least one team member. By signing off contributors or the respective team member indicate that the original contributor accepts the [Developer's Certificate of Origin][DCO], thus certifying that no portion of the patch has been taken from a third pary without permission, and that the commit can be published and legally redistributed under the license terms of this project.

    ```bash
    $ git commit --signoff
    ```

    ```bash
    Signed-off-by: Pablo Hörtner <redtux@pm.me>
    ```

5. In case such a permission is missing for any reason contributors may request another team member to review the patch and merge it for them.

[Sign-off]: https://gerrit-review.googlesource.com/Documentation/user-signedoffby.html "Signed-off-by Lines"
[DCO]: https://developercertificate.org/ "Developer's Certificate of Origin, Version 1.1"

## Writing Documentation

Documentation improvements are very welcome. Contributions can be made directly here or at [**Panda Docs**](https://github.com/pandainfo/panda/tree/master/docs).

## Some hints for newbies

* Check existing issues to verify that the [bug][bug issues] or [feature request][feature request issues] has not already been submitted.
* Open an issue if things are not working as expected.
* Open an issue to propose a significant change.
* Open a pull request to fix a bug.
* Open a pull request to fix documentation about a command.
* Open a pull request if a member of the Panda team has given the ok after discussion in an issue.
* Add installation instructions specifically for your OS/package manager to [install](install.md).

[bug issues]: https://github.com/panda/pandainfo/issues?q=is%3Aopen+is%3Aissue+label%3Abug
[feature request issues]: https://github.com/panda/pandainfo/issues?q=is%3Aopen+is%3Aissue+label%3Aenhancement

## Submitting a pull request

1. Fork and clone the repository
1. Create a new branch: `git checkout -b my-branch-name`
1. Make your change, add tests, and ensure tests pass
1. Submit a pull request: `gh pr create --web`

## Coding guidelines

* Please follow the [PSR-2 Coding Style Guide](https://www.php-fig.org/psr/psr-2/).
* Ensure that the current tests pass.
* If you add new features or code, include the respective tests where relevant.
* Send a coherent commit history, making sure each individual commit in your pull request is meaningful.
* You may need to [rebase](https://git-scm.com/book/en/v2/Git-Branching-Rebasing) to avoid merge conflicts.
* If you are changing or adding to the behaviour or public API, you may need to update the docs.
* Please remember that Panda follows the [SemVer](https://semver.org) standard for versioning.

## Resources

* [How to Contribute to Open Source](https://opensource.guide/how-to-contribute/)
* [Using Pull Requests](https://help.github.com/articles/about-pull-requests/)
* [GitHub Help](https://help.github.com)
