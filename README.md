# Drupal 8 Workbench Moderation to Content Moderation Migration Concept

This repo is the install profile that creates a scenario to test migrating from WBM to CM in Drupal 8.4.

To easily install, see [https://github.com/josephdpurcell/drupal8_wbm2cm_concept-project](https://github.com/josephdpurcell/drupal8_wbm2cm_concept-project)

For the module that runs the migration, see [https://github.com/josephdpurcell/wbm2cm](https://github.com/josephdpurcell/wbm2cm).

## Developer Install

### Build the codebase

    composer install

This will create a docroot folder that contains Drupal and the drupal8_wbm2cm_concept profile

### Install WPS

    phing install

`phing install` assumes:

DB username: `root`  
DB pass: `<none>`  
DB host: `localhost`  
DB Name: `drupal8_wbm2cm_concept`

You can override the presets with `-Ddb.<option>=<value>`. For example, to
change the DB name:

    -Ddb.name=my_db_name

### Pull changes

If you make changes to the profile within the docroot directory and you want to
pull them back into the top-level directory so they can be committed to VCS, use
the `phing pull` command:

    phing pull

## Push changes

Alternately, you can push changes in the top-level down into the docroot with
`phing push`

    phing push

