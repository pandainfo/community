# Boilerplate

## Boilerplate[¶](boilerplate.md#boilerplate) <a id="boilerplate"></a>

The organization of **Panda** follows the standards of similar projects.

```text
├── composer.json
├── config
│   ├── application.php
│   └── environments
│       ├── development.php
│       ├── staging.php
│       └── production.php
├── db
├── docker-compose.yml
├── log
│   ├── db
│   └── web
├── phpcs.xml
├── vendor
├── wp-cli.yml
└── htdocs
    ├── app
    │   ├── mu-plugins
    │   ├── plugins
    │   ├── themes
    │   └── uploads
    ├── index.php
    ├── wp-config.php
    └── core
```

The following list might help to better understand the exact project structure.

1. Settings of this composer package go into `composer.json`.
2. Environment settings are defined in `config`.
3. Databases can be stored locally in `db` during development.
4. Container settings can be found in `docker-compose.yml`.
5. Micro service events are mounted to `log` for persistency.
6. `phpcs.xml` describes the Panda Coding Standards.
7. Third party libraries end up in the `vendor` directory.
8. `wp-cli.yml` generates `wp-config.php` including plugin and core settings.
9. The docroot `htdocs` contains all data processed by the webserver.

 Last update: January 24, 2021

