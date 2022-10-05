# Development tools

* [ITK Dev's own documentation](https://docs.itkdev.dk/) – read it and
  contribute
* [ITK-dev docker setup](https://github.com/itk-dev/devops_itkdev-docker) –
  makes life with Docker a little easier
* [Remote commands](https://github.com/rimi-itk/remote-commands) – makes some
  tasks a little easier

**Pro tip**: Always learn the full command before using the shortcut.

## Examples

```sh
itkdev-docker-compose
itkdev-docker-compose drush --uri=$(itkdev-docker-compose url)
```

### Fetch database from staging site

<https://github.com/itk-dev/devops_itkdev-docker#usage>

```sh
# ~/.ssh/config
…
Host stgdeltag.srvitkstgweb01.itkdev.dk
  HostName srvitkstgweb01.itkdev.dk
…
```

```sh
# .env.local (in project directory)
…
REMOTE_HOST=stgdeltag.srvitkstgweb01.itkdev.dk
# Note use of itkdev-docker-compose-server (cf. https://github.com/itk-dev/devops_itkdev-docker-server)
REMOTE_DB_DUMP_CMD='cd /data/www/stgdeltag_srvitkstgweb01_itkdev_dk/htdocs && itkdev-docker-compose-server exec phpfpm vendor/bin/drush sql:dump --extra-dump=--no-tablespaces --structure-tables-list="cache,cache_*,advancedqueue,history,search_*,sessions,watchdog"'
…
```

```sh
itkdev-docker-compose sync:db
```

**Exercise**: Syncronize files from the staging site.

### Sign in to staging site

<https://github.com/rimi-itk/remote-commands#shortcuts>

```sh
# ~/.ssh/config
…
Host stgdeltag.srvitkstgweb01.itkdev.dk
  HostName srvitkstgweb01.itkdev.dk
  # @see https://github.com/rimi-itk/remote-commands#configuration
  DRUPAL_DRUSH_CWD /data/www/stgdeltag_srvitkstgweb01_itkdev_dk/htdocs
  DRUPAL_DRUSH_ROOT /app
  # Note: We cannot use itkdev-docker-compose-server here due to a clash between drush and itkdev-docker-compose-server with the “root” option.
  DRUPAL_DRUSH_DRUSH docker-compose --env-file .env.docker.local --file docker-compose.server.yml exec phpfpm vendor/bin/drush
…
```

```sh
remote-drupal-drush stgdeltag.srvitkstgweb01.itkdev.dk user:login
```

[Remote commands support completions (on the hostname)!](https://github.com/rimi-itk/remote-commands#completions)

```sh
# Talk to the database
remote-drupal-drush stgdeltag.srvitkstgweb01.itkdev.dk sql:cli
```

It also works with the [Symfony
Console](https://symfony.com/doc/current/components/console.html):

```sh
# ~/.ssh/config
…
Host nsek.dmzwebstgitk03.itkdev.dk
  HostName dmzwebstgitk03.dmz.aarhuskommune.dk
  SYMFONY_CONSOLE_ROOT /data/www/nsek_dmzwebstgitk03_itkdev_dk/htdocs
  SYMFONY_CONSOLE_CONSOLE itkdev-docker-compose-server exec phpfpm bin/console
…
```

```sh
remote-symfony-console nsek.dmzwebstgitk03.itkdev.dk …
```

## Drupal

### [Masquerade](https://www.drupal.org/project/masquerade)

```sh
itkdev-docker-compose composer require drupal/masquerade --dev
itkdev-docker-compose drush --uri=$(itkdev-docker-compose url) pm:enable masquerade
itkdev-docker-compose drush --uri=$(itkdev-docker-compose url) user:login /masquerade
# or
# itkdev-docker-compose drush --uri=$(itkdev-docker-compose url) user:login /admin/people
```

### [Coffee](https://www.drupal.org/project/coffee)

```sh
itkdev-docker-compose composer require drupal/coffee --dev
itkdev-docker-compose drush --uri=$(itkdev-docker-compose url) pm:enable coffee
itkdev-docker-compose drush --uri=$(itkdev-docker-compose url) user:login /admin/config/user-interface/coffee
```
