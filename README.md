# Drupal Hands On

## Enviroment

### Using [ddev](https://ddev.readthedocs.io/en/stable/) start enviroment:

  ```bash
  ddev start
  ```

### Confirm settings sync

in web/sites/settings.ddev.php for example, confirm sync config:

  ```php
  if (empty($settings['config_sync_directory'])) {
    $settings['config_sync_directory'] = '../config/sync';
  }
  ```

### Install dependencies
  ```bash
  ddev composer install
  ```

### Load database dump

  ```bash
  cp DATABASE.sql web/ && \
  ddev drush sql-drop -y && \
  ddev drush sqlc < DATABASE.sql && \
  ddev drush cr && \
  rm web/DATABASE.sql
  ```

### Navigate to site

Navigate to http://drupal-hands-on.ddev.site/


### Admin user

  username: admin

  password: admin
