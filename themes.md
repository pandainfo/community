# Welcome to pandastic

<!-- Abbreviations used by MkDocs for building a glossary -->
<!-- https://squidfunk.github.io/mkdocs-material/reference/abbreviations/ -->
--8<-- "mkdocs/abbreviations.md"

!!! summary
    In this tutorial we show how to change or update themes for Panda.

## About

!!! info
    :calling: A lightweight mobile-first theme called [pandastic].

* [x] Requires at least WP 4.5
* [x] Tested up to WP 5.5
* [x] Requires PHP 5.6 or later
* [x] [AGPLv3](LICENSE.md) (or later)

[pandastic]: https://github.com/pandainfo/pandastic "Pandastic on GitHub"

## Description

!!! hint
    :construction_worker: Custom theme: `pandastic`, developed by Pablo Hörtner <redtux@pm.me>

!!! note ""
    This theme is part of the **[Panda](https://github.com/pandainfo/panda)** project,
    aiming to build the Next Generation E-Commerce Platform.

`pandastic` is a lightweight but powerful WP theme based on [Bootstrap] and [_s].

It includes support for WooCommerce and for Infinite Scroll in Jetpack.

> **You have the choice…**

1. `pandastic` can be used as parent theme for a customized child theme.
2. `pandastic` can be forked in order to create your awesome new theme.

For smaller customizations a child theme is recommended,
facilitating `pandastic` updates without overwriting any changes.

In any case we want to encourage you to contribute your improvements back to `pandastic`.

## Features

!!! summary
    :tada: Well-commented Multipurpose Templates

!!! quote ""
    We provide several pre-styled ready-to-use elements and models for any purpose.

`pandastic` page templates, widgets and layout elements are fully customizable.

> **Our feature list Or: What you get…**

| **Support**                   | **Feature tag**     | **Feature description**                  |
| ----------------------------- | ------------------- | ---------------------------------------- |
| :negative_squared_cross_mark: |                     | Camera Carousal                          |
| :negative_squared_cross_mark: |                     | Gallery Section Lightbox                 |
| :negative_squared_cross_mark: | `svg`               | Vector Illustrations                     |
| :negative_squared_cross_mark: | `custom-fonts`      | SVG Fonts, Font Awesome & [Google Fonts] |
| :negative_squared_cross_mark: | `custom-forms`      | Customizable Contact Forms               |
| :white_check_mark:            | `bootstrap`         | Developer-friendly Bootstrap Theme       |
| :white_check_mark:            | `cross-browser`     | Cross Browser Support (see below)        |
| :white_check_mark:            | `custom-404`        | HTTP 404 Error Page Template             |
| :white_check_mark:            | `custom-background` | Customizable Background                  |
| :white_check_mark:            | `custom-footer`     | Footer Template                          |
| :white_check_mark:            | `custom-header`     | Header Template                          |
| :white_check_mark:            | `custom-logo`       | Customizable Logo                        |
| :white_check_mark:            | `custom-menu`       | Customizable Menus And Navigation Bars   |
| :white_check_mark:            | `custom-search`     | Search Page Template                     |
| :white_check_mark:            | `custom-templates`  | Custom Page Templates & Layout Elements  |
| :white_check_mark:            | `featured-images`   | Customizable Featured Images             |
| :white_check_mark:            | `flexbox`           | CSS Flexible Box Layout                  |
| :white_check_mark:            | `human-readable`    | Clean Well-structured HTML5 & CSS3 Code  |
| :white_check_mark:            | `mobile-first`      | 100% Responsive Web Design               |
| :white_check_mark:            | `sass`              | Syntactically Awesome Style Sheets       |
| :white_check_mark:            | `scss`              | Sassy CSS & Compiled CSS                 |
| :white_check_mark:            | `threaded-comments` | Customizable Threaded Comments           |
| :white_check_mark:            | `translation-ready` | Translations powered by [GNU gettext]    |
| :white_check_mark:            | `ultra-minimal`     | Minify HTML, CSS & JS Resources          |

[Google Fonts]: https://fonts.google.com/ "Free Font Files by Google"

The last two major releases of all major browsers will be automatically tested and fully supported.

* [x] Chrome and Chromium
* [x] Firefox and Firefox ESR
* [x] Internet Explorer
* [x] Opera
* [x] Safari

[GNU gettext]: https://www.gnu.org/software/gettext/manual/gettext.html

!!! hint "We :heart: humans! :robot:"
    No need to reinvent the wheel. :wink:

Reusing pre-built, preselected, curated, modular & well-integrated components saves time and money.

Now we can focus on things that matter without loosing our freedom, creativity, or flexibility.

## Installation

!!! Hint
    :keyboard: While the dashboard can be used for theme installation,
    using the [WP CLI](wp-cli.md) is recommended.

!!! note ""
    :construction: When using Panda, adding new themes via GUI is disabled by default, so you will need to manually enable it.

1. When using the *Dashboard*, go to *Appearance > Themes* and click the *Add New* button.
2. Click *Upload Theme* and *Choose File*, then select the `pandastic.zip` file.
3. Click *Install Now*.
4. Click *Activate* to use our `pandastic` theme right away.

## Customization

Theme customization options are located at *Appearance > Customize*.

The currently available options are:

| **Menu**               | Description                                       |
| ---------------------- | ------------------------------------------------- |
| *Background Image*     | Add a background header image                     |
| *Colors*               | Adjust site-wide colors                           |
| *Pages & Posts*        | Adjust the style of page and post featured images |
| *Site Identity > Logo* | Add a logo image                                  |

!!! example
    To change website colors through the GUI customizer,
    go to *Appearance > Customize > Colors*.

!!! note ""
    For further customization creating a child theme is recommended.

The `inc` directory contains several code snippets to be used in our theme templates.

| **Snippet**                  | **Template**                  | **Description**          |
| ---------------------------- | ----------------------------- | ------------------------ |
| `inc/custom-header.php`      | `header.php`                  | custom header            |
| `inc/template-tags.php`      | `tags.php`                    | custom tags              |
| `inc/template-functions.php` | `functions.php`               | custom functions         |
| `assets/js/navigation.js`    | `assets/js/custom.js`         | responsive dropdown menu |
| `assets/css/layouts/`        | `assets/css/style.scss`       | sidebar layout samples   |
| `inc/woocommerce.php`        | `assets/css/woocommerce.scss` | WooCommerce overrides    |
|                              |                               |                          |

## Development

!!! info "Command"
    The `pandastic` starter code was generated using the WP CLI.

```bash
export WP_THEME="pandastic"
wp scaffold _s "$WP_THEME" --theme_name="$WP_THEME" --author="$WP_TITLE" --author_uri="$WP_HOME" --sassify --woocommerce --activate
```

!!! quote "Output"
    Success: Created theme 'pandastic'.
    Success: Switched to 'pandastic' theme.

## Requirements

`pandastic` requires the following dependencies for theme development:

* [Composer]
* [Node.js]
* [WPGulp]

## Quick start

To start, we need to clone or download this repository.

!!! note
    Skip the following for contributions to `pandastic`.
    These step are only required when forking our project.

We might want to change the name of this project from
`pandastic` to something else like `another-awesome-theme`.

For this we will need to do a six-step find and replace
on the current project's name in all the templates.

1. Search for `'pandastic'` (inside single quotations) to capture the text domain and replace with: `'another-awesome-theme'`.
2. Search for `pandastic_` to capture all the functions names and replace with: `another-awesome-theme_`.
3. Search for `Text Domain: pandastic` in `style.css` and replace with: `Text Domain: another-awesome-theme`.
4. Search for <code>&nbsp;pandastic</code> (with a space before it) to capture DocBlocks and replace with: <code>&nbsp;Another_Awesome_Theme</code>.
5. Search for `pandastic-` to capture prefixed handles and replace with: `another-awesome-theme-`.
6. Search for `_PANDA_` (in uppercase) to capture constants and replace with: `ANOTHER_AWESOME_THEME_`.

Then, we should update the stylesheet header in `style.css`
and the links in `footer.php` with our project's information,
and rename `pandastic.pot` from the `languages` directory to use the theme's slug.

Finally, we need to update this readme, add some new awesome features, adopt the copyright, etc.

## Dev setup

To start using all the development tools that come with `pandastic`
we need to install the necessary Node.js and Composer dependencies.

!!! info "Command"
    Install [Composer] dependencies.

```bash
composer install
```

!!! info "Command"
    Install [Node.js] dependencies.

```bash
npm install
```

## CLI commands

`pandastic` comes packed with CLI commands tailored for WP theme development :

!!! info "Command"
    List available tasks.

```bash
gulp --tasks
```

* `composer lint:wpcs` : checks all PHP files against [PHP Coding Standards](https://developer.wordpress.org/coding-standards/wordpress-coding-standards/php/).
* `composer lint:php` : checks all PHP files for syntax errors.
* `composer make-pot` : generates a .pot file in the `languages/` directory.
* `npm run compile:css` : compiles SASS files to css.
* `npm run compile:rtl` : generates an RTL stylesheet.
* `npm run watch` : watches all SASS files and recompiles them to css when they change.
* `npm run lint:scss` : checks all SASS files against [CSS Coding Standards](https://developer.wordpress.org/coding-standards/wordpress-coding-standards/css/).
* `npm run lint:js` : checks all JavaScript files against [JavaScript Coding Standards](https://developer.wordpress.org/coding-standards/wordpress-coding-standards/javascript/).
* `npm run bundle` : generates a .zip archive for distribution, excluding development and system files.

## Getting help

[Click here to see the full documentation… :fontawesome-solid-paper-plane:](index.md){: .md-button }

!!! help
    :closed_book: See the [Theming Bootstrap] and [Child Themes] docs for further information.

!!! note "See also"
    :book: Reading the Panda [installation notes](install.md) and our [WP Core docs](wp-core.md) is assumed.

## Authors

* **Pablo Hörtner** - _Initial work_ - [🐼 Team panda!](https://github.com/orgs/pandainfo/teams/panda)

See also the [AUTHORS](AUTHORS.md) page and the
[full list of contributors](https://github.com/pandainfo/pandastic/contributors)
who participated in this project.

## Credits

!!! hint "Powered by"
    :battery: `pandastic` is powered by the following projects.

| **Project**         | Copyright notice                                     | License            |
| ------------------- | ---------------------------------------------------- | ------------------ |
| **[Bootstrap]**     | &copy; 2011-2020 [Bootstrap Authors] & [Twitter]     | [MIT]              |
| **[jQuery]**        | &copy; 2005-2020 [jQuery Authors] and [OpenJS]       | [MIT]              |
| **[normalize.css]** | &copy; 2012-2020 Nicolas Gallagher and Jonathan Neal | [MIT]              |
| **[Popper]**        | &copy; 2016-2020 [Federico Zivolo]                   | [MIT]              |
| **[Underscores]**   | &copy; 2012-2020 [automattic]                        | [GPLv2] (or later) |
| **[WPGulp]**        | &copy; 2016-2020 [Ahmad Awais]                       | [GPLv2] (or later) |

!!! check "Thank you! :heart:"
    A big thanks to all authors and contributors, and to the whole free software community.

## Changelog

### 0.2.0 - 2020-11-09

* 🚚 Rename project from `_panda` to `pandastic` due to NPM and Composer restrictions
* 👥 Add a code of conduct
* 👥 Add `AUTHORS` and `mailmap` files to list contributors
* 🔒 Add a security policy for reporting severe bugs and vulnerabilities
* 👷 Add GitHub templates for creating issues and pull requests
* 👷 Add CI workflows for automatic building and testing with GitHub Actions
* 🔒 Fix security issues due to old lodash.template

### 0.1.0 - 2020-10-31

* :tada: Initial release

[_s]: https://github.com/Automattic/_s "Underscores on GitHub"
[AGPLv3]: LICENSE.md "GNU Affero General Public License, Version 3"
[Ahmad Awais]: https://github.com/ahmadawais "Ahmad Awais on GitHub"
[automattic]: https://github.com/Automattic "Automattic on GitHub"
[Bootstrap]: https://github.com/twbs/bootstrap "Bootstrap framework on GitHub"
[Bootstrap Authors]: https://getbootstrap.com/docs/4.5/about/team/ "Founding team and core contributors"
[Composer]: https://getcomposer.org/ "A Dependency Manager for PHP"
[Federico Zivolo]: https://github.com/FezVrasta "Federico Zivolo on GitHub"
[GPLv2]: https://www.gnu.org/licenses/gpl-2.0.html "GNU General Public License, Version 2"
[jQuery]: https://github.com/jquery/jquery "jQuery framework on GitHub"
[jQuery Authors]: https://github.com/jquery/jquery/blob/master/AUTHORS.txt "jQuery Authors on GitHub"
[MIT]: https://opensource.org/licenses/MIT "The MIT License"
[Node.js]: https://github.com/nodejs/node "Node.js JavaScript runtime on GitHub"
[normalize.css]: https://necolas.github.io/normalize.css/ "normalize.css on GitHub"
[OpenJS]: https://openjsf.org/ "OpenJS Foundation"
[Popper]: https://github.com/popperjs/popper-core "Popper on GitHub"
[Theming Bootstrap]: https://getbootstrap.com/docs/4.3/getting-started/theming/ "Customize Bootstrap 4 using Sass variables"
[Twitter]: https://about.twitter.com/ "About Twitter, Inc."
[Underscores]: https://underscores.me/ "A Starter Theme for WordPress"
[Child Themes]: https://developer.wordpress.org/themes/advanced-topics/child-themes/ "WP Theme Developer Handbook"
[WPGulp]: https://github.com/ahmadawais/WPGulp "WPGulp on GitHub"
