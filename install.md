# Getting started

* Update dependencies for required packages

  `composer update`

  At first use the output will look like the following:

  ```bash
  Loading composer repositories with package information
  Updating dependencies (including require-dev)
  Package operations: 24 installs, 0 updates, 0 removals
    - Installing composer/installers (v1.9.0): Loading from cache
    - Installing roots/wordpress-core-installer (1.1.0): Loading from cache
    - Installing aaemnnosttv/wp-cli-dotenv-command (v2.0.0): Downloading (100%)
    - Installing roave/security-advisories (dev-master 425be18)
    - Installing roots/wp-password-bcrypt (1.0.0): Loading from cache
    - Installing roots/wp-config (1.0.0): Loading from cache
    - Installing roots/wordpress (5.5.1): Loading from cache
    - Installing roots/bedrock-autoloader (1.0.3): Loading from cache
    - Installing oscarotero/env (v2.1.0): Loading from cache
    - Installing symfony/polyfill-ctype (v1.18.1): Loading from cache
    - Installing phpoption/phpoption (1.7.5): Loading from cache
    - Installing vlucas/phpdotenv (v4.1.8): Loading from cache
    - Installing roots/bedrock (1.14.2): Loading from cache
    - Installing wpackagist-theme/astra (2.5.5): Downloading (100%)
    - Installing wpackagist-theme/generatepress (2.4.2): Downloading (100%)
    - Installing wpackagist-theme/hueman (3.6.1): Loading from cache
    - Installing wpackagist-theme/online-shop (3.0.3): Loading from cache
    - Installing wpackagist-theme/twentytwenty (1.5): Loading from cache
    - Installing wpackagist-plugin/jetpack (8.9): Downloading (100%)
    - Installing wpackagist-plugin/salt-shaker (1.2.7): Downloading (100%)
    - Installing wpackagist-plugin/theme-check (20200731.1): Loading from cache
    - Installing wpackagist-plugin/woocommerce (4.5.1): Downloading (100%)
    - Installing wpackagist-plugin/amp-wp (1.5.11): Downloading (100%)
    - Installing squizlabs/php_codesniffer (3.5.6): Loading from cache
  Writing lock file
  Generating optimized autoload files
  8 packages you are using are looking for funding.
  Use the `composer fund` command to find out more!
  ```

  Note: The first run might take a while, as we need to download and install all required packages for this project, including WordPress Core, plugins, and themes.

* Start containers and services

  `COMPOSE_DOCKER_CLI_BUILD=1 docker-compose up --build -d`

  ```bash
  Creating network "panda_default" with the default driver
  Creating volume "panda_web_conf" with local driver
  Creating volume "panda_web_data" with local driver
  Creating volume "panda_web_vendor" with local driver
  Creating db ... done
  Creating web ... done
  Creating wp-cli ... done
  ```

* Show container logs

  `docker-compose logs -f`

* Show webserver access log

  `tail -f log/web/apache2/access.log`

* Show webserver error log

  `tail -f log/web/apache2/error.log`

* Show debug log

  `tail -f htdocs/app/debug.log`

  Hint: Try `multitail` for colored output of multiple logs.

* Display all `composer` commands

  `composer list`

* Show PHP version

  `docker-compose exec web php --version`

  ```bash
  PHP 7.3.11 (cli) (built: Oct 25 2019 02:28:50) ( NTS )
  Copyright (c) 1997-2018 The PHP Group
  Zend Engine v3.3.11, Copyright (c) 1998-2018 Zend Technologies
  ```

* Show PHP info

  `docker-compose exec web php --info`

* Show WP-CLI info

  `docker-compose run wp-cli wp --info`

  ```bash
  Starting db ... done
  Starting web ... done
  OS:     Linux 5.4.0-44-generic #48-Ubuntu SMP Tue Aug 11 06:38:48 UTC 2020 x86_64
  Shell:
  PHP binary:     /usr/local/bin/php
  PHP version:    7.3.11
  php.ini used:
  WP-CLI root dir:        phar://wp-cli.phar/vendor/wp-cli/wp-cli
  WP-CLI vendor dir:      phar://wp-cli.phar/vendor
  WP_CLI phar path:       /var/www/html
  WP-CLI packages dir:
  WP-CLI global config:   /var/www/wp-cli.yml
  WP-CLI project config:  /var/www/wp-cli.yml
  WP-CLI version: 2.4.0
  ```

* Create unique salts for enhanced security

  `docker-compose run wp-cli wp dotenv salts regenerate`

* Install new plugin

  `composer require wpackagist-plugin/wp-security-hardening`

  ```bash
  Using version ^1.1 for wpackagist-plugin/wp-security-hardening
  ./composer.json has been updated
  Loading composer repositories with package information
  Updating dependencies (including require-dev)
  Package operations: 1 install, 0 updates, 0 removals
    - Installing wpackagist-plugin/wp-security-hardening (1.1.2): Loading from cache
  Writing lock file
  Generating optimized autoload files
  8 packages you are using are looking for funding.
  Use the `composer fund` command to find out more!
  ```

* Install new theme

  `composer require wpackagist-theme/hueman`

  ```bash
  Using version ^3.6 for wpackagist-theme/hueman
  ./composer.json has been updated
  Loading composer repositories with package information
  Updating dependencies (including require-dev)
  Package operations: 1 install, 0 updates, 0 removals
    - Installing wpackagist-theme/hueman (3.6.1): Loading from cache
  Writing lock file
  Generating optimized autoload files
  8 packages you are using are looking for funding.
  Use the `composer fund` command to find out more!
  ```

* Show installed themes

  `docker-compose run wp-cli wp theme list`

  ```bash
  Starting db ... done
  Starting web ... done
  +-----------------+----------+--------+---------+
  | name            | status   | update | version |
  +-----------------+----------+--------+---------+
  | hueman          | inactive | none   | 3.6.1   |
  | online-shop     | inactive | none   | 3.0.3   |
  | twentyeleven    | inactive | none   | 3.5     |
  | twentyfifteen   | inactive | none   | 2.7     |
  | twentyfourteen  | inactive | none   | 2.9     |
  | twentynineteen  | inactive | none   | 1.7     |
  | twentyseventeen | inactive | none   | 2.4     |
  | twentysixteen   | inactive | none   | 2.2     |
  | twentyten       | inactive | none   | 3.1     |
  | twentythirteen  | inactive | none   | 3.1     |
  | twentytwelve    | inactive | none   | 3.2     |
  | twentytwenty    | active   | none   | 1.5     |
  +-----------------+----------+--------+---------+
  ```

* Use new theme

  `docker-compose run wp-cli wp theme activate hueman`

  ```bash
  Starting db ... done
  Starting web ... done
  Success: Switched to 'Hueman' theme.
  ```

* Get details of an installed theme

  `docker-compose run wp-cli wp get twentysixteen --fields=name,title,version`

  ```bash
  +---------+----------------+
  | Field   | Value          |
  +---------+----------------+
  | name    | Twenty Sixteen |
  | title   | Twenty Sixteen |
  | version | 1.2            |
  +---------+----------------+
  ```

* Get the status of a theme

  `docker-compose run wp-cli wp theme status twentysixteen`

  ```bash
  Theme twentysixteen details:
       Name: Twenty Sixteen
       Status: Active
       Version: 1.2
       Author: the WordPress team
  ```

* Access wp shell

  `docker-compose run wp-cli wp shell`

  ```bash
  Starting db ... done
  Starting web ... done
  wp> help
  wp> exit
  ```

* Stop containers and services

  `docker-compose down -v --remove-orphans`

* Delete all local database instances

  `sudo rm -rfv db/*`
