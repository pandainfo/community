# WP Client

<!-- Abbreviations used by MkDocs for building a glossary -->
<!-- https://squidfunk.github.io/mkdocs-material/reference/abbreviations/ -->
--8<-- "mkdocs/abbreviations.md"

!!! summary "Documentation"
    This is a step-by-step tutorial. Reading the Panda [installation notes](install.md) and our [WP Core docs](wp-core.md) is assumed.

[Click here to see the full documentation… :fontawesome-solid-paper-plane:](index.md){: .md-button }

## Introduction

!!! summary
    Panda can be controlled in various ways, one of it being the command-line client or CLI.

**WP Client** allows easy and automated maintenance of both database and server.

In detail the backend consists of the following key components:

* [x] Web server
  * [PHP server][PHP-server] for development
  * [Apache] or [Nginx] server for production
* [x] GUI dashboard or admin interface based on [WP Core](wp-core.md)
* [x] CLI client
* [x] REST API
* [x] SQL database

[PHP-server]: https://www.php.net/manual/en/features.commandline.webserver.php "PHP built-in web server"
[Apache]: https://httpd.apache.org/ABOUT_APACHE.html "Apache HTTP Server Project"
[Nginx]: https://nginx.org/en/ "Nginx HTTP and Proxy Server"

!!! hint
    It is recommended to use the CLI or the API instead of the GUI for scripts and regular tasks.

## Overview

!!! summary
    This tutorial covers the most important CLI commands.

!!! note ""
    See `wp help` or [wp.org][commands] for a full list of available commands.

[commands]: https://developer.wordpress.org/cli/commands/ "WP-CLI Commands"

> In this tutorial we will learn how to…

* [x] Get system information like the path of the `wp` binary or the `php.ini` file.
* [x] Manage environment variables and `.env` files, including secrets.
* [x] Install, update, and manage the core installation.
* [x] Read and set site options, including plugin and theme settings.
* [x] Perform database operations and connect to the MySQL console.
* [x] …and more.

## First steps

!!! summary
    Let us start with some basics: Command name, system information, and client updates.

### Command name

!!! note
    Before starting we need to know the exact path to the `wp` binary.<br>
    This document will use `wp` without path for better readability.

The command name may vary depending on our installation.

* [x] When using Composer

    `./vendor/wp-cli/wp-cli/bin/wp` (or the `./vendor/bin/wp` symlink)

* [x] When using Docker

    `docker exec wp-cli wp` (or `docker-compose exec wp-cli wp`)

* [x] For global or system-wide installations

    `wp`

### System information

!!! summary
    Whenever information about the current system is needed, the `wp cli info` or `wp --info` command is our friend.

The client will retrieve the following:

* [x] OS information
* [X] Shell information
* [X] PHP binary used
* [X] PHP binary version
* [X] `php.ini` configuration file used, which is typically different than web
* [X] WP CLI root dir, i.e. where the client is installed (if non-Phar install)
* [X] WP CLI global config, i.e. where the global config YAML file is located
* [X] WP CLI project config, i.e. where the project config YAML file is located
* [X] WP CLI version, i.e. the currently installed release

So in cases where changes to the `php.ini` are needed, the CLI shows us the path.

!!! info "Command"
    Display details about the current installation.

```bash
wp --info
```

!!! example
    The output might look as follows.

| **Name**                  | Value                                     |
| ------------------------- | ----------------------------------------- |
| **OS**                    | `Linux 5.4.0-44-generic`                  |
| **Shell**                 | `/bin/zsh`                                |
| **PHP binary**            | `/usr/local/bin/php`                      |
| **PHP version**           | `7.3.11`                                  |
| **php.ini used**          | `/etc/php/7.3/cli/php.ini`                |
| **WP-CLI root dir**       | `phar://wp-cli.phar/vendor/wp-cli/wp-cli` |
| **WP-CLI vendor dir**     | `phar://wp-cli.phar/vendor`               |
| **WP_CLI phar path**      | `/var/www/html`                           |
| **WP-CLI packages dir**   | `/home/redtux/.wp-cli/packages/`          |
| **WP-CLI global config**  | `/var/www/wp-cli.yml`                     |
| **WP-CLI project config** | `/var/www/wp-cli.yml`                     |
| **WP-CLI version**        | `2.4.0`                                   |

!!! note ""
    See `wp help cli` or [wp.org][cli] for more options.

[cli]: https://developer.wordpress.org/cli/commands/cli/ "wp cli <command>"

### Client updates

!!! info "Command"
    Check for updates.

```bash
wp cli check-update
```

> Success: WP-CLI is at the latest version.

!!! info "Command"
    Update the client to the latest release.

```bash
wp cli update --nightly --yes
```

!!! warning
    Phar files have self-updating powers. As shown below,
    this will not work when using Composer or Docker.

> Error: You can only self-update Phar files.

## Environment

!!! summary
    `wp dotenv` manages all environment variables defined in an `.env` file.

`./.env` is set as default. This can be changed by using the `--file` parameter.

!!! info "Command"
    List the content of the `.env.example` file.

```bash
wp dotenv list --file=.env.example
```

!!! example
    The output might look as follows.

| **Variable**        | Value                    |
| ------------------- | ------------------------ |
| `DB_HOST`           | *db*                     |
| `DB_PREFIX`         | *wp_*                    |
| `DB_ROOT_PASSWORD`  | *database_root_password* |
| `DB_NAME`           | *database_name*          |
| `DB_USER`           | *database_user*          |
| `DB_PASSWORD`       | *database_password*      |
| `DOCROOT`           | */var/www/htdocs*        |
| `WP_ENV`            | *development*            |
| `WP_HOME`           | *https://localhost*      |
| `WP_SITEURL`        | *https://localhost/wp*   |
| `WP_DEBUG_LOG`      | */var/log/debug.log*     |
| `WP_TITLE`          | *Panda-CMS*              |
| `WP_ADMIN_USER`     | *admin_user*             |
| `WP_ADMIN_PASSWORD` | *admin_password*         |
| `WP_ADMIN_EMAIL`    | *mail@example.com*       |
| `SFTP_HOST`         | *sftp.example.com*       |
| `SFTP_USER`         | *remote_user*            |
| `SFTP_PASSWORD`     | *remote_password*        |
| `AUTH_KEY`          | *generateme*             |
| `SECURE_AUTH_KEY`   | *generateme*             |
| `LOGGED_IN_KEY`     | *generateme*             |
| `NONCE_KEY`         | *generateme*             |
| `AUTH_SALT`         | *generateme*             |
| `SECURE_AUTH_SALT`  | *generateme*             |
| `LOGGED_IN_SALT`    | *generateme*             |
| `NONCE_SALT`        | *generateme*             |

!!! note ""
    See `wp help dotenv` or [wp-dotenv] for more options, and [phpdotenv] for further information.

[wp-dotenv]: https://aaemnnost.tv/wp-cli-commands/dotenv/ "WP-CLI Dotenv Command"
[phpdotenv]: https://packagist.org/packages/vlucas/phpdotenv "phpdotenv on Packagist"

## Core installation

!!! info "Command"
    Run Panda Core installation process and populate the database.

```bash
wp core install \
        --path=$DOCROOT/wp \
        --url=$WP_HOME \
        --title=Panda-CMS \
        --admin_user=$WP_ADMIN_USER \
        --admin_password=$WP_ADMIN_PASSWORD \
        --admin_email=$WP_ADMIN_EMAIL
```

!!! note ""
    See `wp help core` or [wp.org][core] for more options.

[core]: https://developer.wordpress.org/cli/commands/core/install/ "wp core install"

## Options and settings

!!! summary
    Configure Panda settings like site description, title, theme, URL, or mail server.

### Site title

!!! info "Command"
    Get the site name or title.

```bash
wp option get blogname
```

!!! quote "Output"
    Panda-CMS

!!! info "Command"
    Change the site name or title.

```bash
wp option update blogname "Panda"
```

!!! quote "Output"
    Success: Updated 'blogname' option.

### Site description

!!! info "Command"
    Update the site description.

```bash
wp option update blogdescription "Next Generation E-Commerce Platform"
```

!!! quote "Output"
    Success: Updated 'blogdescription' option.

### Time zone

!!! info "Command"
    Set the time zone.

```bash
wp option update timezone_string "Europe/Vienna"
```

!!! quote "Output"
    Success: Updated 'timezone_string' option.

### Time format

!!! info "Command"
    Set the time format.

```bash
wp option update time_format "H:i"
```

!!! quote "Output"
    Success: Updated 'time_format' option.

### Date format

!!! info "Command"
    Set the date format.

```bash
wp option update date_format "j. F Y"
```

!!! quote "Output"
    Success: Updated 'date_format' option.

### URL format

!!! hint
    In case you do not know what permanent links are and how to use them, see [Using Permalinks].

[Using Permalinks]: https://wordpress.org/support/article/using-permalinks/

!!! info "Command"
    Set the permalink structure to use the post title in the URL.

```bash
wp rewrite structure '/%postname%/'
```

!!! quote "Output"
    Success: Rewrite structure set.<br>
    Success: Rewrite rules flushed.

!!! info "Command"
    Display `.htaccess` permalink rewrite rules

```bash
wp rewrite list --format=csv
```

!!! note ""
    See `wp help rewrite` or [wp.org][rewrite] for more options.

[rewrite]: https://developer.wordpress.org/cli/commands/option/ "wp rewrite"

### Options help

!!! note ""
    See `wp help option` or [wp.org][option] for further assistance.

[option]: https://developer.wordpress.org/cli/commands/option/ "wp option"

## Database management

### List tables

!!! info "Command"
    List database tables.

```bash
wp db tables
```

### Display size

!!! info "Command"
    Display the size of all tables in human readable format.

```bash
wp db size --tables --human-readable
```

!!! example
    The output might look as follows.

| **Name**                | Size  |
| ----------------------- | ----- |
| `wp_commentmeta`        | 50 KB |
| `wp_comments`           | 99 KB |
| `wp_links`              | 33 KB |
| `wp_options`            | 2 MB  |
| `wp_postmeta`           | 50 KB |
| `wp_posts`              | 82 KB |
| `wp_term_relationships` | 33 KB |
| `wp_term_taxonomy`      | 50 KB |
| `wp_termmeta`           | 50 KB |
| `wp_terms`              | 50 KB |
| `wp_usermeta`           | 50 KB |
| `wp_users`              | 66 KB |

### Check integrity

!!! info "Command"
    Check database integrity.

```bash
wp db check
```

!!! quote "Output"
    Success: Database checked.

### DB optimization

!!! info "Command"
    Optimize the database running `mysqlcheck -optimize=true`.

```bash
wp db optimize
```

!!! quote "Output"
    Success: Database optimized.

### DB export

!!! info "Command"
    Export the database to an SQL file running `mysqldump`.

```bash
wp db export --porcelain
```

!!! hint
    The PROCESS privilege for the `DB_USER` is needed for this operation. Use:<br>
    `GRANT PROCESS ON *.* TO 'db_user'@'%';`

### DB import

!!! info "Command"
    Import a database dump from an SQL file.

```bash
wp db import <file>
```

### MySQL client

!!! info "Command"
    Open the SQL console using the `mysql` client.

```bash
wp db cli
```

### Database help

!!! note ""
    See `wp help db` or [wp.org][db] for further assistance.

[db]: https://developer.wordpress.org/cli/commands/db/ "wp db"

## Menus and navigation

### Theme menus

!!! info "Command"
    List available menu locations for the current theme.

```bash
wp menu location list
```

!!! example
    The output might look as follows.

| **Location** | Description             |
| ------------ | ----------------------- |
| `primary`    | Desktop Horizontal Menu |
| `expanded`   | Desktop Expanded Menu   |
| `mobile`     | Mobile Menu             |
| `footer`     | Footer Menu             |
| `social`     | Social Menu             |

### Menu creation

!!! info "Command"
    Create a new menu.

```bash
wp menu create "Panda Menu"
```

!!! quote "Output"
    Success: Created menu 2.

### Menu assignment

!!! info "Command"
    Assign the new menu to the primary menu location.

```bash
wp menu location assign panda-menu primary
```

!!! quote "Output"
    Success: Assigned location primary to menu panda-menu.

### Display menus

!!! info "Command"
    Gets a list of menus.

```bash
wp menu list
```

!!! example
    The output might look as follows.

| term_id | **Name**   | slug       | locations | count |
| ------- | ---------- | ---------- | --------- | ----- |
| 2       | Panda Menu | panda-menu | primary   | 0     |

### Custom menus

!!! info "Command"
    Add custom menu items to the navigation bar.

```bash
wp menu item add-custom panda-menu "🐼 Code" https://github.com/pandainfo/panda --porcelain
wp menu item add-custom panda-menu "📘 Docs" https://pandainfo.github.io/panda --porcelain
```

### List menu items

!!! info "Command"
    Get a list of items associated with a menu.

```bash
wp menu item list panda-menu
```

!!! example
    The output might look as follows.

| DB ID | Type   | **Title** | Link                               | Position |
| ----- | ------ | --------- | ---------------------------------- | -------- |
| 10    | custom | 🐼 Code    | https://github.com/pandainfo/panda | 1        |
| 11    | custom | 📘 Docs    | https://pandainfo.github.io/panda  | 2        |

### Menu help

!!! note ""
    See `wp help menu` or [wp.org][menu] for more options.

[menu]: https://developer.wordpress.org/cli/commands/menu/ "wp menu"
