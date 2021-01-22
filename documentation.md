# Documentation

## Panda Docs

Contributions to docs, translations, proofreading, etc. is always welcome.

This project uses

* [Markdown] for easy content creation,
* [MkDocs] with some plugins for website generation,
* [Read the Docs] for automated versioning, hosting, and search API.

[Markdown]: https://www.markdownguide.org/
[MkDocs]: https://www.mkdocs.org/ "MkDocs - Project documentation with Markdown"

The easiest way to preview Panda's documentation is using Docker.

=== "GNU/Linux & Unix"

    ```bash
    docker run --rm -it -p 8000:8000 -v ${PWD}:/docs squidfunk/mkdocs-material
    ```

=== "Windows"

    ```cmd
    docker run --rm -it -p 8000:8000 -v "%cd%":/docs squidfunk/mkdocs-material
    ```

See the fancy [Material for MkDocs] documentation for details.

[Material for MkDocs]: https://squidfunk.github.io/mkdocs-material/

Settings for [Read the Docs] can be changed in `.readthedocs.yml`.

[Read the Docs]: https://readthedocs.org/

## Docs layout

The Panda documentation follows a common structure.

```bash
.
├── AUTHORS
├── CODE_OF_CONDUCT.md
├── mkdocs.yml
├── docs
│   ├── AUTHORS -> ../AUTHORS
│   ├── CODE_OF_CONDUCT.md -> ../CODE_OF_CONDUCT.md
│   ├── documentation.md
│   ├── index.md -> ../README.md
│   ├── LICENSE.md -> ../LICENSE.md
│   └── requirements.txt
├── LICENSE.md
└── README.md
```

The meaning of the files is probably self-explaining.

```bash
mkdocs.yml    # The docs configuration file
docs/
    index.md  # The documentation homepage
    ...       # Other markdown pages, images and other files
```

## Docs management

This list contains useful commands for taking care of Panda's documentation.

On some systems we need to replace `python` with `python3`
and `pip` with `pip3 --user`.
We should avoid using `sudo`.
In some cases the following might help.

```bash
sudo ln -sv /usr/bin/pip3 /usr/local/bin/pip
```

* Update the Python package manager.

    ```bash
    pip install --upgrade pip setuptools wheel
    ```

* Get required Python packages.

    ```bash
    pip install -r requirements.txt
    ```

* Start the live-reloading docs server.

    ```bash
    mkdocs serve
    ```

* Build the documentation site.

    ```bash
    mkdocs build
    ```

* Print this help message.

    ```bash
    mkdocs --help
    ```

## MkDocs installation

To get familiar with all required packages,
installing one by one might be a helpful alternative.

* Install the MkDocs package.

    ```bash
    pip install mkdocs
    ```

* Install the MkDocs Material theme.

    ```bash
    pip install mkdocs-material
    ```

* Install the MkDocs Material extensions.

    ```bash
    pip install mkdocs-material-extensions
    ```

* Install the [PyMdown] extensions.

    ```bash
    pip install pymdown-extensions
    ```

* Install the [Awesome Pages] plugin.

    ```bash
    pip install mkdocs-awesome-pages-plugin
    ```

* Install the [Last Update] plugin.

    ```bash
    pip install mkdocs-git-revision-date-localized-plugin
    ```

* Install the [Minify HTML and JS] plugin.

    ```bash
    pip install mkdocs-minify-plugin
    ```

[PyMdown]: https://facelessuser.github.io/pymdown-extensions/
[Awesome Pages]: https://github.com/lukasgeiter/mkdocs-awesome-pages-plugin "MkDocs Awesome Pages on GitHub"
[Last Update]: https://github.com/timvink/mkdocs-git-revision-date-localized-plugin "MkDocs Last Update on GitHub"
[Minify HTML and JS]: https://github.com/byrnereese/mkdocs-minify-plugin "MkDocs Minify on GitHub"

## Getting help

The following links provide further information for various operating systems.

* [Introduction to Read the Docs]
* [Write the Docs Community]
* [MkDocs Installation]
* [Python Tools]
* [Pipenv]
* [Homebrew Python]
* [Package Managers]
* [Python for Windows]

[Introduction to Read the Docs]: https://opensource.com/business/16/8/introduction-read-docs
[Write the Docs Community]: https://www.writethedocs.org/origin-story/
[MkDocs Installation]: https://www.mkdocs.org/#installation
[Python Tools]: https://packaging.python.org/guides/tool-recommendations/ "Python tool recommendations"
[Pipenv]: https://pipenv.pypa.io/en/latest/ "Python Dev Workflow for Humans"
[Homebrew Python]: https://formulae.brew.sh/formula/python@3.8 "Python3.8 Homebrew Formula"
[Package Managers]: https://packaging.python.org/guides/installing-using-linux-tools/ "Installing pip using Linux Tools"
[Python for Windows]: https://docs.python.org/3/using/windows.html "Using Python on Windows"
