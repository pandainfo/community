# Environment settings

## Environment settings[¶](environment-settings.md#environment-settings) <a id="environment-settings"></a>

In this step all **Panda** environment variables will be set.

Hint: Copy the provided `.env.example` file to `.env`, and adjust as needed.

This file will be respected by both [WP-CLI Dotenv](https://aaemnnost.tv/wp-cli-commands/dotenv/) and `docker-compose`.

* Development stages
* **Development**
* **Staging**
* **Production**
* Database settings
* `DB_NAME` – Database name
* `DB_USER` – Database user
* `DB_PASSWORD` – Database password
* `DB_HOST` – Database host
* `DB_PREFIX` – Database prefix

Optionally, you can define `DATABASE_URL` for using a [DSN](https://en.m.wikipedia.org/wiki/Data_source_name) instead of using the variables above

e.g. `mysql://user:password@db_host:3306/db_name`

It might be a good idea to not just generate passwords \(64 characters recommended\), but also the names of DBs and DB users, e.g.

```text
DB_NAME=panda-quaep7daiZai
DB_USER=panda-es0oopeiDohM
```

* Web settings
* `WP_ENV` - Set to environment \(`development`, `staging`, `production`\)
* `WP_HOME` - Full URL to WordPress home \([https://example.com](https://example.com/)\)
* `WP_SITEURL` - Full URL to WordPress including subdirectory \([https://example.com/wp](https://example.com/wp)\)
* Secret keys

Generate or regenerate keys and values for authentication salts in the `.env` file with [wp-cli-dotenv-command](https://github.com/aaemnnosttv/wp-cli-dotenv-command), or with this [online salts generator](https://roots.io/salts.html). Should the site be down, try [this](https://wordplate.github.io/salt/) or [that](https://api.wordpress.org/secret-key/1.1/salt/).

* `AUTH_KEY` – Secret key for login cookies
* `SECURE_AUTH_KEY` – Secret key for authorization cookies
* `LOGGED_IN_KEY` – Secret key for non-SSL authorization cookies
* `NONCE_KEY` – Secret key for intrusion prevention
* `AUTH_SALT` – Salt key for login cookies
* `SECURE_AUTH_SALT` – Salt key for authorization cookies
* `LOGGED_IN_SALT` – Salt key for non-SSL authorization cookies
* `NONCE_SALT` – Salt key for intrusion prevention

  Details can be found in [this article](https://wpdatatables.com/wordpress-salts-and-keys/).

* Website customization
* `WP_TITLE` – Every good story needs a good name
* `WP_ADMIN_USER` – Not calling superuser accounts `admin` or `administrator` is recommended
* `WP_ADMIN_PASSWORD` – Every good admin needs a good password
* `WP_ADMIN_EMAIL` – Setting an email address for the primary admin account is optional

 Last update: January 24, 2021

