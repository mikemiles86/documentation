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

Workspaces are a home base for your WebOps. There are two types of workspaces:

<TabList>

<Tab title="Personal Workspace" id="personal-workspace" active={true}>

The Personal Workspace displays tools for the sites you own, or are a team member of, your account plan, and billing for sites you own.  You have only one personal workspace. Learn more about workspaces in the [Accounts](/guides/account-mgmt/account) guide.

- Every Pantheon user is assigned one Personal Workspace. 
- All the sites you have created, as well as individual sites from other organizations you've been invited to collaborate on, will be in your Personal Workspace. 
- You can use a Personal Workspace for your own projects, and for visibility into sites from other organizations you are working with.
- WebOps collaboration features such as [Multidev](/guides/multidev) and [Custom Upstreams](/guides/custom-upstream) are not available in Personal Workspaces. To access these features, you need a [Professional Workspace](/guides/account-mgmt/workspace-sites-teams/workspaces#create-a-professional-workspace). 

</Tab>

<Tab title="Professional Workspace" id="professional-workspace">

Professional workspaces bring together users and sites to allow administrators to effectively manage a large number of sites. Keep in mind, you can be a member of multiple professional workspaces at the same time.

You can create a Professional Workspace as the home for an organization’s sites and the teams working on them. 

- Creating a Professional Workspace is free. 
- Access to the collaboration features below are available to sites owned by Gold Workspaces or above:
	- [Multidev](/guides/multidev)
	- [Custom Upstreams](/guides/custom-upstream)
	- [Autopilot](/guides/autopilot)
- You can create any number of Professional Workspaces. 
- You may be a member of more than one Professional Workspace, and can switch between your Personal and Professional Workspace at any time.

</Tab>

</TabList>

## Supporting Workspaces

If you have contracted with a [Pantheon Partner Agency](https://pantheon.io/plans/partner-program?docs) or have a Professional Workspace with a Gold Account Plan, you can add it to the site as a **Supporting Workspace**, which will give the members of that Workspace access to help build, launch, or maintain your site.

## Create a Professional Workspace

You can create as many workspaces as necessary. The following process will create a Professional Workspace with a free Silver Account Plan.

1. Click on your gravatar in the upper left corner, then select **Create New Workspace**.

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

To switch between workspaces, click your gravatar in the upper left to switch between workspaces:

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

Enterprise, Reseller, OEM, and EDU+ workspaces own sites. Registered Agencies, Pantheon Partners, Premier Pantheon Partners, Strategic Pantheon Partners, and EDU workspaces support sites. This is because an agency's role is to develop, service, and maintain a site on behalf of its owner. Read more about owning and supporting sites in [Workspaces, Sites, and Teams](/guides/account-mgmt/workspace-sites-teams).

### Can I add my own Agency as a Supporting Workspace to a client's site?

No. Only the owner of the site can add an agency as a Supporting Workspace. This action grants all members of the workspace access to the site. You should ask site owners to add your agency as a Supporting Workspace if you are providing services to the site.

### What privileges and roles are granted when adding a Supporting Workspace?

All members of the Supporting Workspace receive the role assigned on the site, regardless of their role in the Supporting Workspace.

### Can the site owner override privileges and access for team members of a Supporting Workspace?

Yes, but only for sites owned by Enterprise or EDU+ workspaces. Roles designated on the Site Team modal will override any roles assigned within the workspace.

### As an Agency, how many sandbox sites do members of a workspace receive?

Each member of a workspace can create up to 10 Sandbox sites. When the limit of 10 is reached, take a site live or delete unused sites to free up additional Sandbox slots.
