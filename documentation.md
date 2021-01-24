# Documentation

## Documentation[¶](documentation.md#documentation) <a id="documentation"></a>

### Panda Docs[¶](documentation.md#panda-docs) <a id="panda-docs"></a>

Contributions to docs, translations, proofreading, etc. is always welcome.

This project uses

* [Markdown](https://www.markdownguide.org/) for easy content creation,
* [MkDocs](https://www.mkdocs.org/) with some plugins for website generation,
* [Read the Docs](https://readthedocs.org/) for automated versioning, hosting, and search API.

The easiest way to preview Panda's documentation is using Docker.

GNU/Linux & Unix

```text
docker run --rm -it -p 8000:8000 -v ${PWD}:/docs squidfunk/mkdocs-material
```

Windows

```text
docker run --rm -it -p 8000:8000 -v "%cd%":/docs squidfunk/mkdocs-material
```

See the fancy [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/) documentation for details.

Settings for [Read the Docs](https://readthedocs.org/) can be changed in `.readthedocs.yml`.

### Docs layout[¶](documentation.md#docs-layout) <a id="docs-layout"></a>

The Panda documentation follows a common structure.

```text
.
├── AUTHORS
├── CODE_OF_CONDUCT.md
├── mkdocs.yml
├── docs
│   ├── AUTHORS -> ../AUTHORS
│   ├── CODE_OF_CONDUCT.md -> ../CODE_OF_CONDUCT.md
│   ├── documentation.md
│   ├── index.md -> ../README.md
│   ├── LICENSE.md -> ../LICENSE.md
│   └── requirements.txt
├── LICENSE.md
└── README.md
```

The meaning of the files is probably self-explaining.

```text
mkdocs.yml    # The docs configuration file
docs/
    index.md  # The documentation homepage
    ...       # Other markdown pages, images and other files
```

### Docs management[¶](documentation.md#docs-management) <a id="docs-management"></a>

This list contains useful commands for taking care of Panda's documentation.

On some systems we need to replace `python` with `python3` and `pip` with `pip3 --user`. We should avoid using `sudo`. In some cases the following might help.

```text
sudo ln -sv /usr/bin/pip3 /usr/local/bin/pip
```

* Update the Python package manager.

  ```text
  pip install --upgrade pip setuptools wheel
  ```

* Get required Python packages.

  ```text
  pip install -r requirements.txt
  ```

* Start the live-reloading docs server.
* Build the documentation site.
* Print this help message.

### MkDocs installation[¶](documentation.md#mkdocs-installation) <a id="mkdocs-installation"></a>

To get familiar with all required packages, installing one by one might be a helpful alternative.

* Install the MkDocs package.
* Install the MkDocs Material theme.

  ```text
  pip install mkdocs-material
  ```

* Install the MkDocs Material extensions.

  ```text
  pip install mkdocs-material-extensions
  ```

* Install the [PyMdown](https://facelessuser.github.io/pymdown-extensions/) extensions.

  ```text
  pip install pymdown-extensions
  ```

* Install the [Awesome Pages](https://github.com/lukasgeiter/mkdocs-awesome-pages-plugin) plugin.

  ```text
  pip install mkdocs-awesome-pages-plugin
  ```

* Install the [Last Update](https://github.com/timvink/mkdocs-git-revision-date-localized-plugin) plugin.

  ```text
  pip install mkdocs-git-revision-date-localized-plugin
  ```

* Install the [Minify HTML and JS](https://github.com/byrnereese/mkdocs-minify-plugin) plugin.

  ```text
  pip install mkdocs-minify-plugin
  ```

### Getting help[¶](documentation.md#getting-help) <a id="getting-help"></a>

The following links provide further information for various operating systems.

* [Introduction to Read the Docs](https://opensource.com/business/16/8/introduction-read-docs)
* [Write the Docs Community](https://www.writethedocs.org/origin-story/)
* [MkDocs Installation](https://www.mkdocs.org/#installation)
* [Python Tools](https://packaging.python.org/guides/tool-recommendations/)
* [Pipenv](https://pipenv.pypa.io/en/latest/)
* [Homebrew Python](https://formulae.brew.sh/formula/python@3.8)
* [Package Managers](https://packaging.python.org/guides/installing-using-linux-tools/)
* [Python for Windows](https://docs.python.org/3/using/windows.html)

 Last update: January 24, 2021

