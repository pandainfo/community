# WP Client

## WP Client[¶](wp-client.md#wp-client) <a id="wp-client"></a>

[Click here to see the full documentation… ]()

### Introduction[¶](wp-client.md#introduction) <a id="introduction"></a>

Summary

Panda can be controlled in various ways, one of it being the command-line client or CLI.

**WP Client** allows easy and automated maintenance of both database and server.

In detail the backend consists of the following key components:

*  Web server
* [PHP server](https://www.php.net/manual/en/features.commandline.webserver.php) for development
* [Apache](https://httpd.apache.org/ABOUT_APACHE.html) or [Nginx](https://nginx.org/en/) server for production
*  GUI dashboard or admin interface based on [WP Core](wp-core.md)
*  CLI client
*  REST API
*  SQL database

Hint

It is recommended to use the CLI or the API instead of the GUI for scripts and regular tasks.

### Overview[¶](wp-client.md#overview) <a id="overview"></a>

Summary

This tutorial covers the most important CLI commands.

See `wp help` or [wp.org](https://developer.wordpress.org/cli/commands/) for a full list of available commands.

> In this tutorial we will learn how to…

*  Get system information like the path of the `wp` binary or the `php.ini` file.
*  Manage environment variables and `.env` files, including secrets.
*  Install, update, and manage the core installation.
*  Read and set site options, including plugin and theme settings.
*  Perform database operations and connect to the MySQL console.
*  …and more.

### First steps[¶](wp-client.md#first-steps) <a id="first-steps"></a>

Summary

Let us start with some basics: Command name, system information, and client updates.

#### Command name[¶](wp-client.md#command-name) <a id="command-name"></a>

Note

Before starting we need to know the exact path to the `wp` binary.  
 This document will use `wp` without path for better readability.

The command name may vary depending on our installation.

*  When using Composer

  `./vendor/wp-cli/wp-cli/bin/wp` \(or the `./vendor/bin/wp` symlink\)

*  When using Docker

  `docker exec wp-cli wp` \(or `docker-compose exec wp-cli wp`\)

*  For global or system-wide installations

  `wp`

#### System information[¶](wp-client.md#system-information) <a id="system-information"></a>

Summary

Whenever information about the current system is needed, the `wp cli info` or `wp --info` command is our friend.

The client will retrieve the following:

*  OS information
*  Shell information
*  PHP binary used
*  PHP binary version
*  `php.ini` configuration file used, which is typically different than web
*  WP CLI root dir, i.e. where the client is installed \(if non-Phar install\)
*  WP CLI global config, i.e. where the global config YAML file is located
*  WP CLI project config, i.e. where the project config YAML file is located
*  WP CLI version, i.e. the currently installed release

So in cases where changes to the `php.ini` are needed, the CLI shows us the path.

Command

Display details about the current installation.

Example

The output might look as follows.

| **Name** | Value |
| :--- | :--- |
| **OS** | `Linux 5.4.0-44-generic` |
| **Shell** | `/bin/zsh` |
| **PHP binary** | `/usr/local/bin/php` |
| **PHP version** | `7.3.11` |
| **php.ini used** | `/etc/php/7.3/cli/php.ini` |
| **WP-CLI root dir** | `phar://wp-cli.phar/vendor/wp-cli/wp-cli` |
| **WP-CLI vendor dir** | `phar://wp-cli.phar/vendor` |
| **WP\_CLI phar path** | `/var/www/html` |
| **WP-CLI packages dir** | `/home/redtux/.wp-cli/packages/` |
| **WP-CLI global config** | `/var/www/wp-cli.yml` |
| **WP-CLI project config** | `/var/www/wp-cli.yml` |
| **WP-CLI version** | `2.4.0` |

See `wp help cli` or [wp.org](https://developer.wordpress.org/cli/commands/cli/) for more options.

#### Client updates[¶](wp-client.md#client-updates) <a id="client-updates"></a>

Command

Check for updates.

> Success: WP-CLI is at the latest version.

Command

Update the client to the latest release.

```text
wp cli update --nightly --yes
```

Warning

Phar files have self-updating powers. As shown below, this will not work when using Composer or Docker.

> Error: You can only self-update Phar files.

### Environment[¶](wp-client.md#environment) <a id="environment"></a>

Summary

`wp dotenv` manages all environment variables defined in an `.env` file.

`./.env` is set as default. This can be changed by using the `--file` parameter.

Command

List the content of the `.env.example` file.

```text
wp dotenv list --file=.env.example
```

Example

The output might look as follows.

| **Variable** | Value |
| :--- | :--- |
| `DB_HOST` | _db_ |
| `DB_PREFIX` | _wp\__ |
| `DB_ROOT_PASSWORD` | _database\_root\_password_ |
| `DB_NAME` | _database\_name_ |
| `DB_USER` | _database\_user_ |
| `DB_PASSWORD` | _database\_password_ |
| `DOCROOT` | _/var/www/htdocs_ |
| `WP_ENV` | _development_ |
| `WP_HOME` | [_https://localhost_](https://localhost/) |
| `WP_SITEURL` | [_https://localhost/wp_](https://localhost/wp) |
| `WP_DEBUG_LOG` | _/var/log/debug.log_ |
| `WP_TITLE` | _Panda-CMS_ |
| `WP_ADMIN_USER` | _admin\_user_ |
| `WP_ADMIN_PASSWORD` | _admin\_password_ |
| `WP_ADMIN_EMAIL` | [_mail@example.com_](mailto:mail@example.com) |
| `SFTP_HOST` | _sftp.example.com_ |
| `SFTP_USER` | _remote\_user_ |
| `SFTP_PASSWORD` | _remote\_password_ |
| `AUTH_KEY` | _generateme_ |
| `SECURE_AUTH_KEY` | _generateme_ |
| `LOGGED_IN_KEY` | _generateme_ |
| `NONCE_KEY` | _generateme_ |
| `AUTH_SALT` | _generateme_ |
| `SECURE_AUTH_SALT` | _generateme_ |
| `LOGGED_IN_SALT` | _generateme_ |
| `NONCE_SALT` | _generateme_ |

See `wp help dotenv` or [wp-dotenv](https://aaemnnost.tv/wp-cli-commands/dotenv/) for more options, and [phpdotenv](https://packagist.org/packages/vlucas/phpdotenv) for further information.

### Core installation[¶](wp-client.md#core-installation) <a id="core-installation"></a>

Command

Run Panda Core installation process and populate the database.

```text
wp core install \
        --path=$DOCROOT/wp \
        --url=$WP_HOME \
        --title=Panda-CMS \
        --admin_user=$WP_ADMIN_USER \
        --admin_password=$WP_ADMIN_PASSWORD \
        --admin_email=$WP_ADMIN_EMAIL
```

See `wp help core` or [wp.org](https://developer.wordpress.org/cli/commands/core/install/) for more options.

### Options and settings[¶](wp-client.md#options-and-settings) <a id="options-and-settings"></a>

Summary

Configure Panda settings like site description, title, theme, URL, or mail server.

#### Site title[¶](wp-client.md#site-title) <a id="site-title"></a>

Command

Get the site name or title.

Command

Change the site name or title.

```text
wp option update blogname "Panda"
```

Output

Success: Updated 'blogname' option.

#### Site description[¶](wp-client.md#site-description) <a id="site-description"></a>

Command

Update the site description.

```text
wp option update blogdescription "Next Generation E-Commerce Platform"
```

Output

Success: Updated 'blogdescription' option.

#### Time zone[¶](wp-client.md#time-zone) <a id="time-zone"></a>

Command

Set the time zone.

```text
wp option update timezone_string "Europe/Vienna"
```

Output

Success: Updated 'timezone\_string' option.

#### Time format[¶](wp-client.md#time-format) <a id="time-format"></a>

Command

Set the time format.

```text
wp option update time_format "H:i"
```

Output

Success: Updated 'time\_format' option.

#### Date format[¶](wp-client.md#date-format) <a id="date-format"></a>

Command

Set the date format.

```text
wp option update date_format "j. F Y"
```

Output

Success: Updated 'date\_format' option.

#### URL format[¶](wp-client.md#url-format) <a id="url-format"></a>

Hint

In case you do not know what permanent links are and how to use them, see [Using Permalinks](https://wordpress.org/support/article/using-permalinks/).

Command

Set the permalink structure to use the post title in the URL.

```text
wp rewrite structure '/%postname%/'
```

Output

Success: Rewrite structure set.  
 Success: Rewrite rules flushed.

Command

Display `.htaccess` permalink rewrite rules

```text
wp rewrite list --format=csv
```

See `wp help rewrite` or [wp.org](https://developer.wordpress.org/cli/commands/option/) for more options.

#### Options help[¶](wp-client.md#options-help) <a id="options-help"></a>

See `wp help option` or [wp.org](https://developer.wordpress.org/cli/commands/option/) for further assistance.

### Database management[¶](wp-client.md#database-management) <a id="database-management"></a>

#### List tables[¶](wp-client.md#list-tables) <a id="list-tables"></a>

Command

List database tables.

#### Display size[¶](wp-client.md#display-size) <a id="display-size"></a>

Command

Display the size of all tables in human readable format.

```text
wp db size --tables --human-readable
```

Example

The output might look as follows.

| **Name** | Size |
| :--- | :--- |
| `wp_commentmeta` | 50 KB |
| `wp_comments` | 99 KB |
| `wp_links` | 33 KB |
| `wp_options` | 2 MB |
| `wp_postmeta` | 50 KB |
| `wp_posts` | 82 KB |
| `wp_term_relationships` | 33 KB |
| `wp_term_taxonomy` | 50 KB |
| `wp_termmeta` | 50 KB |
| `wp_terms` | 50 KB |
| `wp_usermeta` | 50 KB |
| `wp_users` | 66 KB |

#### Check integrity[¶](wp-client.md#check-integrity) <a id="check-integrity"></a>

Command

Check database integrity.

Output

Success: Database checked.

#### DB optimization[¶](wp-client.md#db-optimization) <a id="db-optimization"></a>

Command

Optimize the database running `mysqlcheck -optimize=true`.

Output

Success: Database optimized.

#### DB export[¶](wp-client.md#db-export) <a id="db-export"></a>

Command

Export the database to an SQL file running `mysqldump`.

Hint

The PROCESS privilege for the `DB_USER` is needed for this operation. Use:  
 `GRANT PROCESS ON *.* TO 'db_user'@'%';`

#### DB import[¶](wp-client.md#db-import) <a id="db-import"></a>

Command

Import a database dump from an SQL file.

#### MySQL client[¶](wp-client.md#mysql-client) <a id="mysql-client"></a>

Command

Open the SQL console using the `mysql` client.

#### Database help[¶](wp-client.md#database-help) <a id="database-help"></a>

See `wp help db` or [wp.org](https://developer.wordpress.org/cli/commands/db/) for further assistance.

### Menus and navigation[¶](wp-client.md#menus-and-navigation) <a id="menus-and-navigation"></a>

Command

List available menu locations for the current theme.

Example

The output might look as follows.

| **Location** | Description |
| :--- | :--- |
| `primary` | Desktop Horizontal Menu |
| `expanded` | Desktop Expanded Menu |
| `mobile` | Mobile Menu |
| `footer` | Footer Menu |
| `social` | Social Menu |

Command

Create a new menu.

```text
wp menu create "Panda Menu"
```

Output

Success: Created menu 2.

Command

Assign the new menu to the primary menu location.

```text
wp menu location assign panda-menu primary
```

Output

Success: Assigned location primary to menu panda-menu.

Command

Gets a list of menus.

Example

The output might look as follows.

| term\_id | **Name** | slug | locations | count |
| :--- | :--- | :--- | :--- | :--- |
| 2 | Panda Menu | panda-menu | primary | 0 |

Command

Add custom menu items to the navigation bar.

```text
wp menu item add-custom panda-menu "🐼 Code" https://github.com/pandainfo/panda --porcelain
wp menu item add-custom panda-menu "📘 Docs" https://pandainfo.github.io/panda --porcelain
```

Command

Get a list of items associated with a menu.

```text
wp menu item list panda-menu
```

Example

The output might look as follows.

| DB ID | Type | **Title** | Link | Position |
| :--- | :--- | :--- | :--- | :--- |
| 10 | custom | 🐼 Code | [pandainfo/panda](https://github.com/pandainfo/panda) | 1 |
| 11 | custom | 📘 Docs | [https://pandainfo.github.io/panda](https://pandainfo.github.io/panda) | 2 |

See `wp help menu` or [wp.org](https://developer.wordpress.org/cli/commands/menu/) for more options.

 Last update: January 24, 2021

