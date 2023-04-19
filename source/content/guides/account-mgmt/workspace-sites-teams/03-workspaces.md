---
title: Workspaces, Sites, and Teams
subtitle: Workspaces
description: Learn how to use and manage workspaces.
tags: [workspaces, sites, teams]
contributors: [wordsmither, michellecolon-pantheon]
showtoc: true
permalink: docs/guides/account-mgmt/workspace-sites-teams/workspaces
editpath: docs/guides/account-mgmt/workspace-sites-teams/03-workspaces.md
reviewed: "2022-09-19"
contenttype: [guide]
innav: [false]
categories: [organizations]
cms: [--]
audience: [sysadmin]
product: [--]
integration: [--]
---

Workspaces are a home base for your WebOps. 

## Workspace Tools

The navigation bar on the left contains several additional tabs to help you manage your sites:

- **Sites:** Add a new site, view sites you're a team member of, and check how many free sites you have remaining.

  - **Create New Site:** Start the process of creating a new site on Pantheon. New sites will appear under the Sites tab.

  - **Migrate Existing Site:** Start a guided migration to add a site. If you’re importing a site from your local environment, follow our [manual migration process](/migrate-manual).  For information about migrating a site from a competitor, or other migration scenarios, refer to [Migrate Sites to Pantheon](/guides/guided/) on our [Get Started](/get-started) page.

- **Team*:** Create a new workspace.

- **Autopilot:** [Autopilot](/guides/autopilot) is Visual Regression Testing (VRT) for every WordPress and Drupal Site within your workspace.

- **Support:** View details of an open support request or create a new support request. Our chat-based support is available 24-hours a day.

- **Custom Upstreams*:** Create a new workspace-specific [Custom Upstream](/guides/custom-upstream) using a GitHub or Bitbucket repository. Custom Upstreams allow you to use an external repository as a template for your site.

- **Settings:** Modify the workspace name, logo, billing information, and if your Organization is configured for it, billing terms and instructions for your team.

\* Not available in Personal Workspaces.

<Alert title="Note" type="info" >

<Partial file="dashboard-login-session-length.md" />

</Alert>

## Supporting Workspaces

If you have contracted with a [Pantheon Partner Agency](https://pantheon.io/plans/partner-program?docs) or have a Professional Workspace with a Gold Account Plan, you can add it to the site as a **Supporting Workspace**, which will give the members of that Workspace access to help build, launch, or maintain your site.

## Create a Professional Workspace

You can create as many workspaces as necessary. The following process will create a Professional Workspace with a free Silver Account Plan.  To upgrade a Workspace to Gold, see [Workspace Plans](/guides/account-mgmt/plans/workspace-plans).

1. Click the [Workspace Switcher](/guides/account-mgmt/workspace-sites-teams/workspaces#switch-between-workspaces) in the upper left corner, then select **Create New Workspace**.

1. Enter the information, upload a logo (optional), and click **Continue**.

1. Invite team members or skip this step by clicking **Continue**.

## Switch Between Workspaces

If you're a member of multiple [Organizations](/guides/account-mgmt/workspace-sites-teams/workspaces), you can stay logged in, and switch between Workspaces to work on personal projects or to work between Organizations.

Click the Workspace Switcher (the icon in the upper left) to switch between Workspaces:

![Workspace switcher shows a personal and Agency workspace](../../../images/dashboard/new-dashboard/workspaces-selector.png)


## Retrieve the Workspace UUID

Every entity (user, workspace, product, and site) is assigned a UUID which is internal to Pantheon. The UUID is found within the URL for the entity and resembles the following:

```none
de305d54-75b4-431b-adb2-eb6b9e546014
```

You can also use [Terminus](/terminus) to find the UUID of your workspaces:

```bash{promptUser: user}
terminus org:list
```


## Platform Email Notifications

<Partial file="pantheon-email-notifications.md" />


## Switch Between Workspaces

If you're a member of multiple workspaces, you can stay logged in, and switch between workspaces to work on different projects.

To switch between workspaces, click the icon in the upper left to switch between workspaces:

![Workspace switcher shows a personal and Agency workspace](../../../../images/dashboard/new-dashboard/workspaces-selector.png)

## Customize a Workspace

You can customize the following for a workspace:

- The name and icon of the workspace.

- Payment and terms of service information for Sites built in your workspace.

- [Upgrade](/guides/account-mgmt/workspace-sites-teams/workspaces#account-plans) a Silver Account Plan to a Gold Account Plan.

To customize a Professional Workspace, go to the workspace you wish to customize, then click the **Settings** tab.

## Delete a Workspace

Workspaces cannot be deleted.

## FAQ

### How do we add new sites to a Professional Workspace?

Refer to [Sites](/guides/account-mgmt/workspace-sites-teams/) for more information.

### Why do login attempts fail for all users across my workspace simultaneously?

Any large agency that has multiple developers who login frequently via username/password will trigger failed logins for everyone else who works on the site. This occurs despite everyone using the right password and even when one user logs in and out successfully 3 times.

As a workaround, we recommend following development best practice workflows by [authenticating via SSH key for passwordsless access](/ssh-keys).

### Why can't I access Multidev on my site when the Supporting Workspace can use it?

Only workspace team members and administrators of a Supporting Workspace with Multidev can use this feature. Site team members who are associated with the site but not the professional workspace can access Multidev environments via the unique URL, will not be able to commit code to them.

### Why can't my Agency workspace own a site?

Enterprise, Reseller, OEM, and EDU+ workspaces own sites. Registered Agencies, Pantheon Partners, Premier Pantheon Partners, Strategic Pantheon Partners, and EDU workspaces support sites. This is because an agency's role is to develop, service, and maintain a site on behalf of its owner. 

### Can I add my own Agency as a Supporting Workspace to a client's site?

No. Only the owner of the site can add an agency as a Supporting Workspace. This action grants all members of the workspace access to the site. You should ask site owners to add your agency as a Supporting Workspace if you are providing services to the site.

### What privileges and roles are granted when adding a Supporting Workspace?

All members of the Supporting Workspace receive the role assigned on the site, regardless of their role in the Supporting Workspace.

### Can the site owner override privileges and access for team members of a Supporting Workspace?

Yes, but only for sites owned by Enterprise or EDU+ workspaces. Roles designated on the Site Team modal will override any roles assigned within the workspace.

### As an Agency, how many sandbox sites do members of a workspace receive?

Each member of a workspace can create up to 10 Sandbox sites. When the limit of 10 is reached, take a site live or delete unused sites to free up additional Sandbox slots.
