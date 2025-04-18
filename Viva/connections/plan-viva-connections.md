---
ms.date: 01/30/2025
title: "Plan Viva Connections for your organization"
ms.reviewer: 
ms.author: evanatkin
author: AtkinE
manager: elizapo
audience: Admin
f1.keywords:
- NOCSH
ms.topic: how-to
ms.service: viva-connections
ms.localizationpriority: high
ms.collection:
  - Strat_SP_modern
  - M365-collaboration
  - m365initiative-viva-connections
search.appverid:
- SPO160
- MET150
description: "Build a team of stakeholders to align the primary use cases for your user experience strategy, then plan for each component of the experience"
---

# Plan Microsoft Viva Connections for your organization

In the planning phase, build a team of stakeholders to align the goals and primary use cases for your organization's user experience strategy, then start by planning for each component of the experience. Consider success metrics and adoption tactics to ensure Connections meets the needs of your organization and users.

> [!NOTE]
>
> - You must have an Enterprise (E), Frontline (F), or Academic (A) license type to create a Connections experience.
> - Users with a Microsoft 365 subscription (E, F, or A license) are limited to creating and using one experience. If you want to create or use two or more experiences (up to 50), then every user in your tenant must have a Microsoft Viva Suite or Viva Communications and Communities license. See [Microsoft Viva plans and pricing]( https://www.microsoft.com/microsoft-viva/pricing) for more info.
> - You must have SharePoint admin permissions to access the Microsoft 365 admin center.
> Connections is available on mobile and tablet devices in GCC, GCC High, and DoD environments with limited features. For more information, see the [list of service availability](/office365/servicedescriptions/office-365-platform-service-description/office-365-us-government/office-365-us-government#service-availability-for-each-plan).

The following steps marked with an asterisk (*) are optional or might only apply to customers who use SharePoint home sites to complement the Connections experience.

## Step 1: Plan for Connections

Connections is designed to help users complete high-priority tasks and easily access important information. This experience can be built over time as your organization adapts and scales. Organizations can use an [existing SharePoint intranet home site](set-up-admin-center.md#build-from-an-existing-intranet-portal) (if available), or create a [standalone Connections experience](set-up-admin-center.md#create-a-connections-experience).

Connections is composed of three main components – the [dashboard, the news reader, and resources](viva-connections-overview.md#components-to-connections):

> [!NOTE]
>
> The news reader experience is being rolled out to users that will replace the current Feed experience across desktop, web, and mobile devices. This update is planned to roll out to all customers across all devices by the end of April 2025.

- **Dashboard**: The dashboard is your user’s digital toolset. It brings together the tools your users need, enabling quick and easy access whether they are in the office or in the field.

- **News Reader**: Found on the News tab, the News reader pulls SharePoint news from organizational sites, boosted news, user’s followed sites, frequent sites, and people users work with in an immersive reader experience.

- **Resources**: Resources provide links to the most popular destinations at your organization. Create your own links or import them from a SharePoint home site (if available), or create links targeted to [specific audiences](edit-resources.md).

The three components making up your Connections experience are featured across desktop and mobile devices, but display differently. For more information, see the section in this article to [learn more about the differences between the desktop and mobile experience](viva-connections-overview.md#connections-mobile-and-desktop-experiences).

## Step 2: Consider using a SharePoint home site to complement the experience* (optional)

A Connections experience can be created without a [SharePoint home site](home-site-plan.md) (a communication site that has special capabilities), but providing one can complement the user experience. A SharePoint home site acts as the front door to your organization’s intranet and a gateway to other popular portals that are relevant to the entire organization. [Some organizations use a SharePoint home site to complement the Connections experience](viva-connections-overview.md#how-sharepoint-home-sites-and-connections-work-together) and extend the experience to the web. If you decide not to create a SharePoint home site now, an [existing Connections experience can have a SharePoint home site](set-up-admin-center.md#setting-a-home-site-after-setting-up-a-standalone-connections-experience) added to it at any time.

### Create a SharePoint home site for your organization* (optional)

A [SharePoint home site](home-site-plan.md) is a SharePoint communication site that acts as a front door to your organization’s intranet. Once a SharePoint home site is set, the news posted from that site is prioritized across the intranet.

A SharePoint home site can be set in the [Connections Admin Center](set-up-admin-center.md#how-to-access-viva-connections-in-the-microsoft-admin-center) when creating a new experience, or assigned to an existing SharePoint home site. Having a SharePoint home site also allows you to take advantage of the SharePoint app bar.

For more information, see how to [plan, build, and launch a SharePoint home site for your organization](home-site-plan.md).

### Set up global navigation in the SharePoint app bar* (optional)

> [!NOTE]
> Users need a SharePoint home site to take advantage of the SharePoint app bar.

Once you have a SharePoint home site, you can set up the SharePoint app bar to improve navigation to intranet resources through global navigation, and personalized content like sites, news, files, and lists. Links from the Global Navigation bar can also be [imported into the Resources section](edit-resources.md#import-sharepoint-links) of your Connections experience.

For more information, see the [introduction to the SharePoint app bar](sharepoint-app-bar.md).

### Review, prioritize, and modernize content to align with key scenarios and tasks* (optional)

After defining the key scenarios and tasks in the planning phase, prepare for Connections by ensuring priority content is located on modern SharePoint communication sites and team sites. Both [modern and classic sites](https://support.microsoft.com/office/5725c103-505d-4a6e-9350-300d3ec7d73f) can be used, but only modern sites appear in the Microsoft Teams app. Classic sites open in a separate browser window.

If you have many SharePoint sites, make sure you focus on sites, pages, and content that are relevant to the Connections experience. Sites and content that are unrelated to key tasks and scenarios can be modernized later.

**Sites that should be reviewed and prioritized**:

- Sites that dashboard cards link to.

- Sites that are displayed in global navigation.

- Sites that frequently publish organizational news.

- Sites that help users complete the most important day-to-day tasks or access important information.

**Resources to help you modernize**:

- Use the [SharePoint modernization scanner](/sharepoint/dev/transform/modernize-scanner) to create a dashboard that helps you determine modernization readiness.

- Learn more about how to [transform classic sites to modern sites](/sharepoint/dev/transform/modernize-userinterface-site-pages), or consider [creating new modern sites using SharePoint site templates](https://support.microsoft.com/office/39382463-0e45-4d1b-be27-0e96aeec8398).

- See the article on [healthy portal guidance for high-traffic sites](/sharepoint/portal-health) for more guidance on how best practices and recommendations for popular sites that are expected to get a high amount of traffic.

## Step 3: Plan the dashboard

Start by identifying the key scenarios that Connections needs to support and identify owners of those user experiences. Common scenarios include view paystubs and vacation hours, submit help tickets, catch up on news, check daily lunch menus, find people in a directory, and shift management. For more information, see the [full list available dashboard cards](available-dashboard-cards.md). If your organization has a specific need that calls for a custom card, consider using the [card designer](use-card-designer.md) to build your own.

These scenarios can be [targeted to specific audiences](use-audience-targeting-in-viva-connections.md) using Microsoft 365 Groups. Consider which groups of users need access to specific resources.

| General | For information workers   | For frontline workers  |
| :------------------- | :------------------- |:-------------------|
| - View pay and benefits <br> - Submit a ticket to the help desk <br> - Access lunch and café options <br> - Catch up on news and announcements | - Find people and team information <br> - Complete required training <br> - View company holidays | - View and manage shifts <br> - Access time sheets and popular forms <br> - View workplace policies and resources |

Collaborate and align with business groups that manage these experiences to determine the best design. Review the [Adoption center's best practices from successful Connections customers](https://adoption.microsoft.com/files/viva/connections/Adoption-Recommended-Practices-for-Viva-Connections.pdf) for more information on common scenarios and how to identify user experiences that result in lasting adoption.

### Planning process

As you work with business owners and key stakeholders to align your Connections design strategy, answer the following questions for each task:

- Who is the audience?

- What do users need to accomplish or learn?

- What tools or technology do they use today?

- What tools or technology do you want visitors to use to accomplish their key tasks?

- What information needs to be promoted?

### Design with your audience in mind

As a best practice, it's important to make decisions that are rooted in specific tasks for certain audiences:

- Consider using a common framework for scenario planning that starts by selecting a certain role or audience "In my role as a...".

- Then, narrow down the objective in "I need to...".

- Next, consider the ideal tool or process to meet the objective in "So that I...".

- Lastly, script out what success looks like in "I know this is successful when...".

For example, create a table like the following to list business scenarios that you want to address with cards in the dashboard:

|In my role as...|I need to...|So that...|I know this is successful when...|
|:-------------------|:---------------|:-----------|:------------------------------------|
|Full time user |Easy access to benefit and payroll information |I can quickly check important information without needing help from HR |Requests for help with benefits and payroll to the HR team are reduced  |
|Frontline worker |Clock in and out from a mobile device |I can create efficiencies in my workflow |Schedules and breaks are managed from Connections |
|People manager |Welcome and onboard new team members |I can grow and develop talent |I spend less time managing standard onboarding functions |
|Sales representative| Access specific product training materials while on a mobile device |Can quickly resolve customer issues|Most customer issues get resolved in real-time|
|HR specialist |Promote the use of the self-service benefits |I can spend more time working with users on unique benefits questions and scenarios|All of my user interactions are about individual critical scenarios|

Keep in mind that not every task should be turned into a card on the Dashboard. Focus on tasks that are the most impactful to your users that can be executed within a short amount of time.

### Examples of different dashboard designs

The dashboard should focus on the most important tasks. Tasks that are specific to certain audiences should be targeted to make sure users only see cards that are relevant to their day-to-day jobs.

For example, the following mobile dashboards are designed around different worker roles and the dashboard cards that more closely relate to their roles.

| **Information workers**   | **Frontline workers**  |
|-----------------------|--------------------|
| ![Image of the Connections dashboard designed for frontline workers.](../media/connections/plan-viva-connections/dashboard-information-worker.png) |  ![Image of the Connections dashboard designed for information workers.](../media/connections/plan-viva-connections/dashboard-frontline.png) |

### Content for planning Dashboards

- [Create and customize a dashboard](create-dashboard.md).

- Review the [dashboard cards available](available-dashboard-cards.md), or use the [card designer to build your own](use-card-designer.md).

- Review the [permissions model for Connections](edit-viva-home.md#manage-permissions).

- Use existing [Microsoft 365 Groups](https://support.microsoft.com/office/learn-about-microsoft-365-groups-b565caa1-5c40-40ef-9915-60fdb2d97fa2) or create news groups if needed so that you can quickly create cards and [target them to specific audiences](/viva/connections/create-dashboard#apply-audience-targeting-to-cards).

## Step 4: Get ready for the news reader

> [!NOTE]
>
> The news reader experience is being rolled out to users that will replace the current Feed experience across desktop, web, and mobile devices. This update is planned to roll out to all customers across all devices by the end of April 2025.

The news reader presents SharePoint news from organizational sites, boosted news, user’s followed sites, frequent sites, and people users work with in an immersive reader experience. This gives content publishers a reliable method of distributing important news and information, while keeping frontline workers, information workers, and hybrid workers alike engaged and informed on important news and announcements.

Audience targeting can be used to show news content to specific groups of people if you want to present information that is relevant only to a particular group of people. For example, you can target news stories about a specific project to only team members and stakeholders of the project. For more information, see the article on [audience targeting](use-audience-targeting-in-viva-connections.md#apply-audience-targeting-to-news-posts-that-display-in-the-news-reader).

Users can access their news from the news tab on the Connections experience. For more information, see the article on [the News reader in Connections](news-reader.md).

## Step 5: Plan the resources

Resources are the navigational links to portals and other popular destinations. Resources should be the most important and popular portals for your target audience and can be targeted to specific audiences.

Organizations with a [SharePoint home site](home-site-plan.md) that created a [global navigation bar](sharepoint-app-bar.md) can also provide users with links to resources. The global navigation bar can only be accessed outside SharePoint by users through the Connections app on Microsoft Teams by selecting the organizations logo on the Teams app rail. Links from the Global Navigation bar can also be [imported into the Resources section](edit-resources.md#import-sharepoint-links) of the Connections experience.

For more information, see the article on [editing resources](edit-resources.md). For more information on SharePoint navigation, see the introduction to [SharePoint information architecture](/sharepoint/information-architecture-modern-experience).

## Step 6: Create an adoption plan

Planning for change and helping users adopt new resources are different for every organization. Use the considerations and best practices here as a starting point to creating an adoption plan that fits your organization’s needs. Include considerations for change management and training materials for end-users in your plan.

### Adoption considerations

- Users can access Connections from [Microsoft Teams, SharePoint, and the Viva Suite home](viva-connections-overview.md#accessing-connections-from-microsoft-teams-sharepoint-or-the-viva-suite-home) on desktop or mobile devices.

- Use [early adopters and champions](https://adoption.microsoft.com/roles/champion/) to extend their enthusiasm to the rest of the organization.

- Plan to engage with users where they typically meet and share information (for example, if your organization already meets in Teams, plan to post in channels.)

- Determine where questions about Connections should go, and who should answer them. Consider using [Viva Engage](https://support.microsoft.com/office/join-and-create-a-community-in-yammer-56aaf591-1fbc-4160-ba26-0c4723c23fd6), a [SharePoint site](https://support.microsoft.com/office/create-a-site-in-sharepoint-4d1e11bf-8ddc-499d-b889-2b48d10b1ce8), or [Teams channels](https://support.microsoft.com/office/create-a-channel-in-teams-fda0b75e-5b90-4fb8-8857-7e102b014525) to allow users to ask questions or see commonly asked questions.

- Learn more about adoption, best practices, and get communication templates in the [Viva adoption center](https://adoption.microsoft.com/viva/).

### Change management considerations

- Start by creating awareness and interest in multiple channels to appeal to different audiences. Consider common spaces for on-site users like the break room or conference rooms. For remote workers and the rest of the organization, plan to post announcements in Teams, Viva Engage, and SharePoint.

- Make sure different audiences of end-users can easily understand how this new tool helps improve their day-to-day work.

- Create opportunities for users to ask questions, get help, and see live demonstrations. Consider setting up weekly training sessions or office hours during the first month of adoption. Use champions where possible.

- Reinforce change by creating incentives for using the new tools.

- Clearly explain how to use Connections on desktop and mobile devices, how to engage with the Dashboard, the Feed, and Resources, and where to view the latest news and announcements.

- Create specialized guidance for different audiences like frontline workers or hybrid workers.

### Training considerations

- Use training to help raise awareness about how to use Connections on [desktop](https://support.microsoft.com/office/3da30f39-684a-4bde-bb81-2e1407d59b52) and [mobile](https://support.microsoft.com/office/753e0607-0bfd-4712-ad7e-18490dd565a2) devices.

- Showcase different ways to connect and engage with cards on the dashboard.

- Consider providing different training guidance for different audiences.

- Highlight popular links that can be found in the Resource tab when on a mobile device.

## Step 7: Consider success metrics

Part of the planning process includes determining which metrics will be used to measure how effective Connections is in bringing your organization together and keeping specific audiences informed.

- **Use the analytics feature within Connections:** Use [analytics](viva-connections-analytics.md) to understand how and when users engage with components of the Connections experience, the content types users engage with, and the platforms used to access Connections.

- **High-level view of usage across M365 apps:** Use [Microsoft 365 usage analytics](/microsoft-365/admin/usage-analytics/usage-analytics) to access a prebuilt dashboard that contains several prebuilt reports that focus on adoption of Microsoft 365 apps, usage, communication, and collaboration.

- **Site or page level data:** Get [site level](https://support.microsoft.com/office/2fa8ddc2-c4b3-4268-8d26-a772dc55779e) and [page level](https://support.microsoft.com/office/e3186199-ccc8-4445-9162-bb1bcec8b7ee) usage reports in SharePoint to gauge engagement and learn more about when users access content and what devices they're using.

- **Get direct feedback from users:** Usage analytics aside, you can ask users directly about their overall satisfaction. Consider [creating a card on the Dashboard that links to a Microsoft Form](https://support.microsoft.com/office/4ffb64cc-7d5d-402f-b82e-b1d49418fd9d) where you can ask users to rate satisfaction and provide feedback.

## Step 8: Plan for maintenance over time

As your business grows and evolves, you'll likely identify new scenarios that can be supported by Connections. Over time, you might decide to retire cards on the dashboard or rearrange global navigation in resources.

Additionally, users will share feedback that can be used to improve the experience. Each of these scenarios requires time to implement and to communicate as needed. Plan to have a point-person, or team of people, who can manage these tasks over time.  

- **Dashboard:** Once the [owner or member](edit-viva-home.md#manage-permissions) has designed and tested the experience, the dashboard will only need to be updated to support new scenarios or retire old scenarios.

- **Feed:** Content is dynamically displayed and aggregated from SharePoint news posts and Viva Engage.  

- **Resources:** Like the dashboard, once links to sites have been established, the Resources will only need updates as needed.

## Next, build and customize Connections for your organization

After you meet requirements (for customers who want a SharePoint home site), have a plan for the dashboard, and are prepared to help users adopt Connections, it's time to [move on to the build phase](build-viva-connections.md).
