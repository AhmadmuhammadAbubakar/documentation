---
title: Migrate a Custom Upstream to Drupal 9
subtitle: Deploy to Dev
description: 
cms: "Drupal 9"
categories: [develop]
tags: [code, launch, migrate, site, updates]
contributors: [wordsmither, michellecolon-pantheon]
layout: guide
permalink: docs/guides/drupal-9-hosted-createcustom/deploy-dev
anchorid: deploy-dev
editpath: drupal-9/drupal-9-hosted-createcustom/09-deploy-dev.md
reviewed: "2021-03-31"
---

Merge the code and files from the Multidev environment to the Dev environment.

1. Merge the `composerify` branch on the Custom Upstream into the `master` branch and push:

    ```bash{promptUser:user}
    git checkout master
    git merge composerify && git push origin master
    ```

1. Apply the upstream updates to your individual sites. This will only apply them to the Dev environment.

1. If you applied any site-specific code to individual sites' `ic-test` Multidev, merge that Multidev into the Dev environment.

  <Alert title="Note" type="info" >

  There is currently a platform bug which prevents Integrated Composer from being enabled until a change to `pantheon.yml` has been pushed to *each site*. Follow the steps below to complete the final deployment.

  </Alert>

1. After you push to Dev, you must push another change to `pantheon.yml`. You can either:

    - Add a comment in `pantheon.yml` at the end of the file, and that will trigger Composer

      Or

    - Use `echo` to do it for you:

     ```bash{promptUser:user}
     echo "\n# comment to trigger Composer\n" >> pantheon.yml
     ```

1. Make sure to push your changes up again.

1. Confirm that the Dev environment is working as expected.
