# Contributing

Thanks for your interest in contributing to Panda!

As you might have expected,
contributions are welcome.

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
[code-of-conduct]: CODE_OF_CONDUCT.md

## Some hints

* Check existing issues to verify that the [bug][bug issues] or [feature request][feature request issues] has not already been submitted.
* Open an issue if things are not working as expected.
* Open an issue to propose a significant change.
* Open a pull request to fix a bug.
* Open a pull request to fix documentation about a command.
* Open a pull request if a member of the Panda team has given the ok after discussion in an issue.
* Add installation instructions specifically for your OS/package manager inside `./docs/install/`.

[bug issues]: https://github.com/panda/pandainfo/issues?q=is%3Aopen+is%3Aissue+label%3Abug
[feature request issues]: https://github.com/panda/pandainfo/issues?q=is%3Aopen+is%3Aissue+label%3Aenhancement

## Submitting a pull request

1. Fork and clone the repository
1. Create a new branch: `git checkout -b my-branch-name`
1. Make your change, add tests, and ensure tests pass
1. Submit a pull request: `gh pr create --web`

## Guidelines

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
