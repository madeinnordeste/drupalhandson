# Drupal Hands On

## Enviroment

### Using [ddev](https://ddev.readthedocs.io/en/stable/) start enviroment:

  ```bash
  ddev start
  ```

### Confirm settings sync

in web/sites/settings.ddev.php confirm sync config:

  ```php
  if (empty($settings['config_sync_directory'])) {
    $settings['config_sync_directory'] = '../config/sync';
  }
  ```



### Load database dump

  ```bash
  cp DATABASE.sql web/ && \
  ddev drush sql-drop -y && \
  ddev drush sqlc < DATABASE.sql && \
  rm web/DATABASE.sql
  ```

### Navigate to site

Navigate to http://drupal-hands-on.ddev.site/


### Admin user

  username: admin

  password: admin
