# Language settings

<!-- Abbreviations used by MkDocs for building a glossary -->
<!-- https://squidfunk.github.io/mkdocs-material/reference/abbreviations/ -->
--8<-- "mkdocs/abbreviations.md"

!!! summary
    In this quick tutorial we will learn how to install, activate, and manage language packages for Panda.

## Show active language

!!! info "Command"
    Get the current default language.

```bash
wp language core list --status=active
```

!!! example
    The output might look as follows.

| **Language** | **English name**        | **Native name**         | **Status** | **Update** |
| ------------ | ----------------------- | ----------------------- | ---------- | ---------- |
| en_US        | English (United States) | English (United States) | active     | none       |

## Install new languages

!!! info "Command"
    Install the German core language packages.

```bash
wp language core install de_AT de_CH de_CH_informal de_DE de_DE_formal
```

!!! quote "Output"
    Success: Installed 5 of 5 languages.

## List installed languages

!!! info "Command"
    List installed core language packages.

```bash
wp language core list --status=installed
```

!!! example
    The output might look as follows.

| **Language**   | **English name**               | **Native name**       | **Status** | **Updated**         |
| -------------- | ------------------------------ | --------------------- | ---------- | ------------------- |
| de_AT          | German (Austria)               | Deutsch (Österreich)  | installed  | 2020-09-13 17:09:13 |
| de_CH          | German (Switzerland)           | Deutsch (Schweiz)     | installed  | 2020-09-09 20:03:38 |
| de_CH_informal | German (Switzerland, Informal) | Deutsch (Schweiz, Du) | installed  | 2020-09-09 20:03:47 |
| de_DE          | German                         | Deutsch               | installed  | 2020-10-22 11:22:21 |
| de_DE_formal   | German (Formal)                | Deutsch (Sie)         | installed  | 2020-10-22 11:23:04 |

## Switch default language

!!! info "Command"
    Set German as default language.

```bash
wp site switch-language de_DE
```

!!! quote "Output"
    Success: Language activated.

## Install theme language

!!! info "Command"
    Install the German language packages for the Twenty Twenty theme.

```bash
wp language theme install twentytwenty de_CH de_CH_informal de_DE de_DE_formal
```

!!! quote "Output"
    Success: Installed 4 of 4 languages.

## Install plugin language

!!! info "Command"
    Install the German language packages for WooCommerce.

```bash
wp language plugin install woocommerce de_CH de_CH_informal de_DE de_DE_formal
```

!!! quote "Output"
    Success: Installed 4 of 4 languages.

## Update language packages

!!! info "Command"
    Update all core language packages if needed.

```bash
wp language core update
```

!!! quote "Output"
    Success: Translations are up to date.

!!! info "Command"
    Update all plugin language packages if needed.

```bash
wp language plugin --all update
```

!!! quote "Output"
    Success: Translations are up to date.

!!! info "Command"
    Update all theme language packages if needed.

```bash
wp language theme --all update
```

!!! quote "Output"
    Success: Translations are up to date.

## Getting help

[Click here to see the full documentation… :fontawesome-solid-paper-plane:](index.md){: .md-button }

!!! note "See also"
    Reading the Panda [installation notes](install.md) and our [WP Core docs](wp-core.md) is assumed.

!!! note ""
    See `wp help language` or [wp.org][language] for more options, and [wp-languages.github.io] for further information.

[language]: https://developer.wordpress.org/cli/commands/language/ "wp language"
[wp-languages.github.io]: https://wp-languages.github.io/ "Composer WP language packs"
