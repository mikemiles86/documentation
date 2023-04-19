---
title: Integrated Composer
subtitle: Apply One-click Updates
description: Learn how to apply One-click updates with Integrated Composer.
tags: [composer, workflow]
contributors: [ari, edwardangert]
reviewed: "2022-12-13"
showtoc: true
permalink: docs/guides/integrated-composer/one-click-updates
contenttype: [guide]
innav: [false]
categories: [dependencies]
cms: [drupal, wordpress]
audience: [development]
product: [composer]
integration: [--]
---

This section provides information on how to apply One-click updates with Integrated Composer. 

You can apply one-click updates in the Site Dashboard or with Terminus.

## Site Dashboard

1. Go to the [Site Dashboard[(/guides/account-mgmt/workspace-sites-teams/sites#site-dashboard)], **Dev** tab, and click **Code**.

1. Click **Check Now**.

1. Switch your **Development Mode** from SFTP to **Git** if you have not done so already.

1. Click **Apply Updates** if updates are available.


## Terminus

Run the command below to apply available updates to your site development environment:

```bash{promptUser: user}
terminus upstream:updates:apply --updatedb --accept-upstream -- <site>.<env>
```

## More Resources

- [WordPress and Drupal Core Updates](/core-updates)

- [Upstream Updates with Terminus](/terminus/commands/upstream-updates-apply)
