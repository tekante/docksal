# Overriding default PHP/MySQL/etc. settings

<a name="configuration"></a>
## Altering PHP and MySQL configuration

The following configuration files are mounted inside the respective containers and can be used to override the default settings:

- `.docksal/etc/php5/php.ini` - PHP settings overrides
- `.docksal/etc/php5/php-cli.ini` - command line PHP settings overrides
- `.docksal/etc/mysql/my.cnf` - MySQL settings overrides

Copy [examples/.docksal](../examples/.docksal) into the `/.docksal` folder in your project repo and modify as necessary.

<a name="php-versions"></a>
## Using different PHP versions

Switching PHP versions is done via the `blinkreaction/drupal-cli` docker image tags.

To switch to a different image tag:

- open the `docker-compose.yml` file
- replace the `cli` service `image` property as necessary (see list of available tags below)
- run `fin up`

Available PHP versions:

- `5.6` (`image: docksal/cli:stable`) - default
- `7.0` (`image: docksal/cli:php7`) - experimental

<a name="mysql-versions"></a>
## Using different MySQL versions

Switching MySQL versions is done via the `blinkreaction/drupal-mysql` docker image tags.

To switch to a different image tag:

- open the `docker-compose.yml` file
- replace the `db` service `image` property as necessary (see list of available tags below)
- run `fin up`

Available MySQL versions:

- `5.5` (`image: docksal/mysql:5.5`)
- `5.6` (`image: docksal/mysql:5.6`) - default.
- `5.7` (`image: docksal/mysql:5.7`)