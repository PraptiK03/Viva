---
ms.date: 08/12/2024
title: "Overview: Viva Connections"
ms.reviewer: evanatkin
ms.author: evanatkin
author: AtkinE
manager: elizapo
audience: Admin
f1.keywords:
- NOCSH
ms.topic: overview
ms.service: viva-connections
ms.localizationpriority: high
ms.collection:
  - essentials-navigation
  - essentials-overview
  - Strat_SP_modern
  - M365-collaboration
  - m365initiative-viva-connections
  - intro-overview
  - highpri
search.appverid:
- SPO160
- MET150f
ms.custom: intro-overview
description: "Learn how to use Viva Connections to engage and unite your organization."
---

# Overview of Viva Connections

Microsoft Viva Connections is your gateway to a modern user experience and is designed to keep everyone engaged and informed. Connections is a customizable app that can be accessed through Microsoft Teams or the web from your desktop, mobile, or table device.

Connections gives different roles in your organization a personalized landing page where users can discover:

- [Helpful tools to complete tasks](#connections-dashboard);
- [SharePoint news from organizational sites, boosted news, user followed sites, frequent sites, and from people the user works with](#connections-news-reader);
- [Resources in the form of links provided by the organization](#connections-resources); and
- Other Viva apps your organization is licensed for.

:::image type="content" source="../media/connections/viva-connections-overview/desktop-mobile-compare.png" alt-text="Screenshot of the Connections app on desktop and mobile." lightbox="../media/connections/viva-connections-overview/desktop-mobile-compare.png":::

Use the [quick guide to set up Connections](set-up-admin-center.md) or get [more detailed guidance on how to plan, build, and launch](plan-viva-connections.md).

**Connections is:**

- A user experience app in Microsoft Teams that allows organizations to create unique experiences for different audiences like information workers, frontline workers, educators, researchers, or students.

- A gateway to other Viva apps and services with the ability to curate specific content and tools by providing easy access to resources, tools, relevant news, announcements, and popular destinations.

- Built on existing capabilities in Microsoft 365 like SharePoint, Teams, and [Microsoft Entra](/azure/active-directory/fundamentals/new-name).

- Easily accessed through the desktop, tablet, or mobile versions of the Microsoft Teams app, through your company’s SharePoint home site, or by using the [Viva Suite home](https://viva.cloud.microsoft/) website.

- Able to give users a consistent experience by being accessible through the desktop Teams app, a SharePoint home site, or via the [Viva Suite home](https://viva.cloud.microsoft/) website. Refer to the section in this article on the [Connections desktop experience](#the-connections-desktop-experience) for more detail.

- Accessing Connections through the Teams app on a mobile or tablet device provides a more compact experience and uses tabs to make it easier to scroll through content. Refer to the section in this article on the [Connections mobile experience](#the-connections-mobile-experience) for more detail.

- Learn more about [Microsoft Viva](https://www.microsoft.com/microsoft-viva) and [Viva licensing](https://www.microsoft.com/microsoft-viva/pricing).

> [!NOTE]
>
> - A home site isn't a requirement for setting up Connections, but some organizations might choose to use a home site in addition to Connections to provide a secondary landing experience that’s more focused on organizational content. [Learn more about home sites and how they complement Connections](#how-sharepoint-home-sites-and-connections-work-together).

## Components to Connections

Connections is composed of three primary components - the  News reader, the dashboard, and resources. All components can be accessed from the desktop, tablet, or mobile versions of the Microsoft Teams app, through your company’s SharePoint home site, or by using the [Viva Suite home](https://viva.cloud.microsoft/) website.

| Component | Description |
| :------------------- | :------------------- |
| **Spotlight** | At the top of connections experience, the spotlight dynamically displays content from the home site, news from SharePoint sites, or links to articles or sites. The spotlight can be customized to display up to 11 items.|
| **News reader** | The News reader provides users with SharePoint news from across the organizational sites, boosted news, user’s followed sites, frequent sites, and people the user works with presented as news cards in a neat and easy to access immersive reader experience. Users can easily Like interesting news and Save content for later. Users with a Microsoft 365 Copilot license can access a Copilot powered news summary from the desktop version of Microsoft Teams; providing an AI generated summary of top news items to provide a quick overview of all the latest information. The news reader can be accessed from the News tab at the top of the connections experience.|
| **Dashboard** | [The dashboard](create-dashboard.md) is your user's digital toolset that brings together the resources your users need whether they are in the office or in the field. The dashboard uses dynamic cards that users can interact with to do things like clock in for a shift, access training materials, review paystub information, or book a shuttle. It can also be used as a [web part on SharePoint home sites](use-dashboard-web-part-on-home-site.md). <br><br> Cards in the Connections dashboard are based on [adaptive cards](https://adaptivecards.io/) and the [SharePoint Framework (SPFx)](/sharepoint/dev/spfx/sharepoint-framework-overview). They provide a low-code solution to bring your line-of-business apps into the dashboard. In addition, Connections desktop combined with SharePoint home sites can also be further customized and extended using [SPFx web parts and extensions](/sharepoint/dev/spfx/viva/overview-viva-connections).|
| **Resources** | The Connections resources experience enables way finding across popular destinations. Organizations can curate a list of useful links that appear to users such as health benefits, important forms, and department websites.|

### Connections Spotlight

The spotlight sits at the top of the Connections experience and displays content from the home site, news from SharePoint sites, or links to articles or sites, providing a steady stream of information. Users can select links and news stories as they cycle through or use the navigation controls to scroll through the banner. If no items are available to display, this section collapses.

:::image type="content" source="../media/connections/viva-connections-overview/spotlight.png" alt-text="Screenshot of the spotlight at the top of the Connections experience." lightbox="../media/connections/viva-connections-overview/spotlight.png":::

For more information on customizing the Spotlight, see the article on [managing the spotlight](manage-spotlight.md).

### Connections News reader

> [!NOTE]
>
> - The news reader experience is being rolled out to users that will replace the current Feed experience across desktop, web, and mobile devices. This update is planned to roll out to all customers across all devices by the end of April 2025.
> - The Copilot powered news summary is currently only available through the desktop version of Microsoft Teams and is rolling out to users with a Microsoft 365 Copilot license.

Additional news can be accessed from the News tab. Here, users can access their personalized news feed with relevant information ranging from organizational and industry news, boosted news, the users frequent and followed sites, trending sites, and news published by people the user works with. News will be displayed on cards with options to like and save posts for later. A Copilot powered news summary provides an AI generated summary of top news items in a user’s feed to provide a quick overview of all the latest information.

:::image type="content" source="../media/connections/viva-connections-overview/news-tab.png" alt-text="Screenshot showing off content available from within the news tab." lightbox="../media/connections/viva-connections-overview/news-tab.png":::

For more information on the News reader, see the article on the [news reader in Connections](news-reader.md).

### Connections dashboard

The Connections dashboard enables you to create a curated experience using dashboard cards that give your users' access to their most critical content and tools. These cards are designed to enable quick task completion either by interacting with a card directly or by opening a quick view in the dashboard. Think of the Connections dashboard as a digital tool set for your users.

:::image type="content" source="../media/connections/viva-connections-overview/dashboard-overview.png" alt-text="Screenshot of the dashboard in the Connections experience." lightbox="../media/connections/viva-connections-overview/dashboard-overview.png":::

The Connections dashboard is available as a Teams app for desktop, tablet, and mobile (iOS, Android) platforms, by accessing Connections using the [Viva Suite website](https://viva.cloud.microsoft/), and as a [web part on SharePoint sites](/viva/connections/use-dashboard-web-part-on-home-site). The web part can be integrated into a SharePoint home site, which then is exposed as part of the Connections for desktop experience in Teams.

#### Anatomy of a dashboard

A dashboard is made of medium-sized and large-sized cards which users can interact with to get information or complete a task.

**Users can select cards or click the buttons on cards to do things like:**

- Displaying a quick view with more information or an input form
- Navigating to a SharePoint page
- Accessing a Teams app
- Integrate with partner apps, services, and other Viva apps

Some cards can also reflect dynamic content that refreshes based on a user action or other event. For example, users can see new tasks assigned or required training courses when they open the dashboard. As the users mark the tasks as complete, the card updates to reflect their new number of tasks.

The dashboard experience has been designed to be consistent across mobile platform and desktop, but there are some differences:

|**Element**  |**Mobile Experience** (Smartphone & Tablet) |**Desktop Experience** (Desktop & Web)  |
|---------|---------|---------|
|Dashboard  |     Displays as the default tab in the Connections app in Teams.    | It's prominently displayed in the desktop app and can be added to your SharePoint sites [as a web part](use-dashboard-web-part-on-home-site.md).   |
|Dashboard layout   | Fixed in portrait mode. Card sizes can be medium (which shows two cards on one row) or large (which shows one card on a row). Users can [reorder, show, or hide the cards](https://support.microsoft.com/office/753e0607-0bfd-4712-ad7e-18490dd565a2#bkmk_customize-viva-connections-mobile-dashboard) on their dashboard (These settings won't carry over to their desktop or tablet experience).       |     Can be portrait or landscape with varying numbers of cards on each row depending on whether the web part is used in a one, two, or three column page section layout.     |
|Card UI     |  Native       |    HTML based     |
|Card order     |     Same as in Desktop    |  Same as in Mobile       |
|Card reflow    |   Same as in Desktop      |   Same as in Mobile      |
|How many cards are shown     |  All cards without audience targeting plus audience-targeted cards where the viewer is part of the targeted audience.       |   The number of cards to show can be specified in the Dashboard web part settings, but which cards are shown might vary depending on audience targeting. Users can expand the number of cards show by selecting "See all."     |

#### Dashboard authoring

The dashboard can be authored directly in the Connections app in Teams desktop. If you're using a home site, the dashboard can also be authored from the SharePoint home site.

:::image type="content" source="../media/connections/new-dashboard-creation.png" alt-text="Image showing how to edit a Connections Dashboard." lightbox="../media/connections/new-dashboard-creation.png":::

The layout of the dashboard, including the size of the cards (which can be individually set as medium or large) can be customized. The layout of the cards might look different depending on whether the dashboard is being viewed on mobile, desktop, or in the dashboard web part. Users with edit permissions can preview how the dashboard appears to users viewing on a mobile device or desktop.

For more information on customizing the dashboard, see the article on [creating and editing a dashboard](create-dashboard.md).

#### Dashboard cards

The Connections dashboard comes with a set of built-in cards, but is also designed to enable Software as a Service (SaaS) providers, system integrators, and in-house development teams to create their own cards to meet the needs of the organization.

:::image type="content" source="../media/connections/dashboard-cards.png" alt-text="Image showing Dashboard cards." lightbox="../media/connections/dashboard-cards.png":::

Cards in the Connections Dashboard are based on adaptive cards and the [SharePoint Framework (SPFx)](/sharepoint/dev/spfx/viva/get-started/build-first-sharepoint-adaptive-card-extension). They provide a low-code solution to bring your line-of-business apps into the Dashboard.

[Learn more about the available dashboard cards.](available-dashboard-cards.md)

Discover [more card options from partner services](https://cloudpartners.transform.microsoft.com/resources/viva-app-integration)

### Connections resources

Resources are navigational links that can be set up and customized both from the Teams app and web experience for Connections. Once set up, these resources are displayed on the desktop, web, and mobile experiences of Connections. They include customized links from any URL, whether it's external to your organization or internal to organization. Links can be further customized by applying audience targeting to each link.

Organizations with a [SharePoint home site](home-site-plan.md) that created a [global navigation bar](sharepoint-app-bar.md) can also provide users with links to resources. The global navigation bar can only be accessed outside SharePoint by users through the Connections app on Microsoft Teams by selecting the organizations logo on the Teams app rail. Links from the Global Navigation bar can also be [imported into the Resources section](edit-resources.md#import-sharepoint-links) of Connections.

> [!NOTE]
>
> Up to 48 resource links can be created in the Resources section.

:::image type="content" source="../media/connections/viva-connections-overview/resources-overview.png" alt-text="Screenshot of the resource section within the Connections experience." lightbox="../media/connections/viva-connections-overview/resources-overview.png":::

In the mobile app, users can view resources by selecting the **Resources** tab. This type of functioning provides users with a familiar navigation structure and allows them to open sites, pages, news, and more—right from their mobile devices.

For more information, see the article on [editing the resource section](edit-resources.md).

## Connections mobile and desktop experiences

The desktop and mobile experiences are centered around the three main components of the dashboard, News reader, and resources sections. Users accessing Connections from the desktop app in Teams, SharePoint home page, or the [Viva Suite home website](https://viva.cloud.microsoft/) features all three components at-a-glance, in addition to announcements, spotlight, and the Viva Suite footer.

Accessing Connections from a tablet or mobile device features a more compact experience for the three components and uses tabs to make it easier to scroll through content.

### The Connections desktop experience

Users can access Connections via Teams, their organization's SharePoint home page, or the [Viva Suite home website](https://viva.cloud.microsoft/), thus providing a consistent experience through multiple entry points.

:::image type="content" source="../media/connections/edit-viva-home/vc3-at-a-glance-desktop.png" alt-text="Screenshot of the Connections desktop experience." lightbox="../media/connections/edit-viva-home/vc3-at-a-glance-desktop.png":::

**Key capabilities of the desktop experience:**

- **Access to the rest of the Viva suite:** The desktop experience of the connections app offers easy discovery and navigation to all the Viva modules that the user is licensed for, bringing together the connection, insight, growth, and purpose pillars of Microsoft Viva.

- **Accessible from the web:** Users can access Connections on the web can be accessed from your company’s SharePoint home site or from the [Viva Suite home](https://viva.cloud.microsoft/) website, without needing the Microsoft Teams app.

- **Navigation between other Viva experiences:** Navigational elements located in the top-right and top-left corners, navigational elements help viewers easily get to-and-from other landing pages and [other Viva experiences](https://support.microsoft.com/topic/introducing-microsoft-viva-3c1012cb-6c85-4d49-bd7f-b18a6e7873e0).

- **Announcements**: [Important time-sensitive notices](announcements-viva-connections.md) targeted to users within the organization appear at the top of the Connections experience.

- **Company resources and way finding**: The desktop experience provides users the ability to navigate to important resources using links curated by your organization and the important sites your organization frequently engages with. This navigation panel appears when users select the branded app icon in Teams, and surfaces elements shared with the [SharePoint global navigation](sharepoint-app-bar.md).

- **Access specific tools based on roles**: Throughout the Connections experience, [content can be targeted to specific audiences](use-audience-targeting-in-viva-connections.md) to ensure they have the right tools at the right time.

- **Stay updated on news personalized to the viewer**: Users can access the News tab to check their personalized news feed. In addition, the Spotlight on the Home tab cycles through news pulled from selected SharePoint sites, or links pinned by experience owners.

- **Easily share content**: Content consumed within Teams can be easily shared into chats or channels, making collaboration easier.

#### Accessing Connections from Microsoft Teams, SharePoint, or the Viva Suite home

**From the Connections app in Microsoft Teams**: Select the **Connections app** from the Microsoft Team’s app bar.

:::image type="content" source="../media/connections/viva-connections-overview/access-vc-teams.png" alt-text="Screenshot of accessing Connections from Microsoft Teams." lightbox="../media/connections/viva-connections-overview/access-vc-teams.png":::

**From your organization's SharePoint home site**: Select **Go to Connections** from your organization's intranet or home site.

:::image type="content" source="../media/connections/viva-connections-overview/access-vc-sp.png" alt-text="Screenshot of accessing Connections from SharePoint." lightbox="../media/connections/viva-connections-overview/access-vc-sp.png":::

**From the Viva Suite home website**: Select the **Connections card** from the spotlight on the [Viva Suite home site](https://viva.cloud.microsoft/).

:::image type="content" source="../media/connections/viva-connections-overview/access-vc-home.png" alt-text="Screenshot of accessing Connections from Viva Home." lightbox="../media/connections/viva-connections-overview/access-vc-home.png":::

### The Connections mobile experience

The experience in the Connections mobile app is anchored around three key concepts: the dashboard, the news reader, and resources.

:::image type="content" source="../media/connections/viva-connections-overview/mobile-dashboard.png" alt-text="Screenshot showing the dashboard tab on the Connections mobile app." lightbox="../media/connections/viva-connections-overview/mobile-dashboard.png":::

For more detailed information, see the article on [Connections on mobile devices](https://support.microsoft.com/office/753e0607-0bfd-4712-ad7e-18490dd565a2).

## Curated experiences

Connections gives you and your content creators the tools to provide a curated experience. A curated experience is one in which the user sees content chosen by a site owner or author. For example, a site owner controls the content used on the site and whether the content is audience targeted. [Audience targeting](use-audience-targeting-in-viva-connections.md) is accomplished using [Microsoft Entra ID](/azure/active-directory/fundamentals/new-name) groups for card-level targeting in the dashboard and menu-item targeting in the global navigation.

- **Home site (optional)**: A home site isn't required for Connections, but can be used as a secondary landing destination for organizational content and news. A site owner controls the layout of the home site, the elements used on that site, and targeting  content to specific audiences.

- **News reader**: By using audience targeting, you can show news content to specific groups of people. This is useful when you want to present information that is relevant only to a particular group of people. For example, you can target news stories about a specific project to only team members and stakeholders of the project. The news reader will then display all news based on the user’s frequented and followed SharePoint sites.<br><br>News that is posted across the organization will also be featured in the spotlight at the top of the experience and can be customized to include links to other sites or information.

- **Dashboard**: A dashboard author controls the curation of the dashboard and can target each card on the dashboard to specific audiences using existing Microsoft Entra ID groups. This allows dashboard authors to create different experiences for each group. And because Viva Connection uses Microsoft Entra ID groups, authors benefit from dynamic group memberships to reduce administrative overhead. Authors can easily preview what the dashboard looks like across devices and audiences.

- **Resources**: The list of sites on the resources experience in mobile is controlled by a resource author who generates links for the organization and enables audience targeting so that users in different groups see relevant navigation items.

## Branding

Matching your organizational brand is integral to your users' connection with your company's values and goals. The branding you apply in Teams to the Connections desktop app – including your logo and colors – is automatically applied to the mobile app. For information on how to apply your branding in an app, review [how to customize apps in Microsoft Teams](/microsoftteams/customize-apps). The desktop app offers an opportunity for further branding by [customizing the banner image](edit-viva-home.md#customize-the-banner-image) and [customizing the theme](edit-viva-home.md#apply-a-theme-to-your-connections-experience).

> [!NOTE]
> Organization branding in the Connections app is currently disabled for users on mobile and desktop who have enabled dark mode under their Microsoft Teams Appearance and Accessibility settings.

## Localization

Connections is available in most major languages used in Microsoft 365. Learn more about [how to set up the Connections mobile experience in a specific language](viva-connections-language.md) and [how to create a dashboard in more than one language](create-multilingual-dashboard.md).

- **Dashboard:** Content can be set by dashboard authors to support multiple languages.

- **News reader:** The content is available in the format in which it was authored, and SharePoint news posts display author-translated posts in the user’s preferred language.

- **Resources:** Content follows the site's default language.

## Extensibility

Many components to the Connections experience can be customized. The [SharePoint Framework](/sharepoint/dev/spfx/sharepoint-framework-overview) (SPFx) is the recommended SharePoint customization and extensibility model for developers because of the tight integration between SharePoint, Microsoft Teams, and Microsoft Connections. The SPFx is the only extensibility and customization option for Connections. [Learn more about Connections extensibility](/sharepoint/dev/spfx/viva/overview-viva-connections).

## How SharePoint home sites and Connections work together

Connections and home sites are two complementary methods to creating powerful user experiences that can be viewed on the web and in Teams. A [SharePoint home site](home-site-plan.md) is a user experience that serves as a landing destination, news hub, and the main entry-point to your organization’s intranet. Both Connections and home site experiences are designed to unite and empower your organization and automatically integrate with each other to form a cohesive and branded experience.

Use Connections as the primary destination where users access job-specific tools and news and home sites as a secondary source of organizational news and industry news, events, and resources. Connections is where individuals get access to curated content based on their role, and the home site is where they can find more organizational-focused resources.

### Shared functionality

:::image type="content" source="../media/connections/viva-connections-overview/shared-functionality.png" alt-text="Screenshot of a Venn diagram that displays the similarities and differences between Connections and home sites." lightbox="../media/connections/viva-connections-overview/shared-functionality.png":::

Both share many common capabilities like news roll ups, navigation, and partner extensibility to ensure these solutions work together. Both types of experiences share basic functionality, like the ability to use audience targeting, distribute organizational news, industry news, and [share the same permissions model](edit-viva-home.md) to make it easy for editors to access and manage.

### Connections automatically detects home sites

For organizations that already have a home site (or know they want one in the future) the home site is automatically detected by Connections, and a prominent link will display at the top-right of the desktop experience. Users can easily navigate between both – so you don’t have to choose one over the other.

:::image type="content" source="../media/connections/viva-connections-overview/home-site-detected.png" alt-text="Screenshot of Connections detecting the home site." lightbox="../media/connections/viva-connections-overview/home-site-detected.png":::

### Connections allows for multiple home sites across multiple experiences

Depending on the size of your organization and the information to communicate, you might decide to create a separate experience for each audience you wish to target. Organizations are able to set multiple home sites by using multiple Connections experiences, creating a targeted experience that is content specific for that group of users (for example, a dashboard and resources with a frontline worker focus). This article provides some [scenarios where you’d want to create more Connections experiences](/viva/connections/set-up-admin-center#scenarios-for-creating-additional-viva-connections-experiences).

> [!NOTE]
>
> - SharePoint home sites are now set in the Microsoft admin center and can be set up when you create a Connections experience that builds off an intranet portal.
> - You must have an Enterprise (E), Frontline (F), or Academic (A) license type to create a Connections experience.
> - Users with a Microsoft 365 subscription (E, F, or A license) are limited to creating and using one experience. If you want to create or use two or more experiences (up to 50), then every user in your tenant must have a Microsoft Viva Suite or Viva Communications and Communities license. See [Microsoft Viva plans and pricing](https://www.microsoft.com/microsoft-viva/pricing) for more info.

### You can choose the default landing experience

Unless specified, Connections is the default experience for the desktop app in Teams. When Connections is the default, a link to the home site displays in the top-right corner to ensure easy navigation between the two experiences. We recognize that some organizations with a home site want the home site to be the default experience. When the home site is the default experience, a link to Connections will display in the top-right corner. [Learn more about choosing the default experience](edit-viva-home.md#choose-the-default-landing-experience-for-connections-desktop).

## Step-by-step guidance to prepare for Connections

There are several options to learn more about how to get Connections for your organization.

| Option                  | Description        | Time to complete|
| :--------------------- | :--------------------|:----------------------:|
| [Quick guide](set-up-admin-center.md) | Use the quick guide to get a high-level overview of how to get Connections | 10 minutes |
| [Plan, build, and launch guidance](viva-connections-setup-overview.md) | Get more detailed guidance that focus on tasks in the plan, build, and launch phases.   | 30 minutes           |
| [Learning path](/training/paths/viva-connections-get-started/)    | Get in-depth guidance that includes fictitious business stories and examples. Complete knowledge checks to confirm learnings.       | Two hours            |

## More resources

Join the discussion and see the latest events in the [Connections Community](https://techcommunity.microsoft.com/category/VivaConnection).

[Learn how to plan, build, and launch a home site](home-site-plan.md)

[Connections adoption resources](https://adoption.microsoft.com/viva/connections)

[Connections guidance for end users](https://support.microsoft.com/office/your-intranet-is-now-in-microsoft-teams-8b4e7f76-f305-49a9-b6d2-09378476f95b)

Learn more about [creating and editing a dashboard](create-dashboard.md)