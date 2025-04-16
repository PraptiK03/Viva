---
ms.date: 04/03/2024
title: "Customize and edit the Viva Connections home experience"
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
  - essentials-manage
  - Strat_SP_modern
  - M365-collaboration
  - m365initiative-viva-connections
  - highpri
search.appverid:
- SPO160
- MET150
description: "Learn how to customize and edit the Viva Connections home experience."
---

# Customize and edit the Viva Connections experience

The [Viva Connections](viva-connections-overview.md) desktop design serves as an experience that centers essential job tasks, personalized content, easy access to other Viva experiences, and better aligns with the mobile experience. [Learn more about the Connections desktop experience](https://techcommunity.microsoft.com/blog/viva_connections_blog/more-options-coming-soon-for-the-viva-connections-desktop-experience/3644419).

Elements of the Connections experience can be customized to fit your organization’s brand and the needs of your end users. Learn more about how to customize the banner, Dashboard content, and navigational links in Resources. Then, learn how to influence content in the  News reader. Finally, learn how to manage access and permissions.

> [!NOTE]
>
> - If your organization has a SharePoint home site, you can choose to use it as the default landing destination.
> - The Connections experience uses a similar permission model to SharePoint and can be managed from Microsoft Teams.
> - You must have member level permissions or higher to edit the new desktop experience.

## About the Connections experience

The Connections experience highlights news across your organization and provides easy access to the top tasks, tools, and resources that help people in your organization get their jobs done. Sections featured in Connections include Announcements, the  News reader, the Spotlight, Dashboard, Resources, and the Viva suite footer. Content for some of these elements can be filtered [using audience targeting to create a personalized experience](use-audience-targeting-in-viva-connections.md) for users in your organization.

> [!NOTE]
>
> - The news reader experience is being rolled out to users that replaces the current Feed experience across desktop, web, and mobile devices. This update is planned to roll out to all customers across all devices by the end of April 2025.
> - The Copilot powered news summary is currently only available through the desktop version of Microsoft Teams and is rolling out to users with a Microsoft 365 Copilot license.
> - Users are required to have a Microsoft Viva suite or Viva Communications and Communities license to utilize the announcements feature. See [Microsoft Viva plans and pricing](https://www.microsoft.com/microsoft-viva/pricing) for more info.

:::image type="content" source="../media/connections/edit-viva-home/vc3-at-a-glance-desktop.png" alt-text="Screenshot of the full page Connections experience." lightbox="../media/connections/edit-viva-home/vc3-at-a-glance-desktop.png":::

**Announcements:** Announcements from the organization display at the top of the Connections experience and convey time-sensitive information to users.

**Spotlight**: The spotlight dynamically displays content from the home site, news from SharePoint sites, or links to articles or sites. The [spotlight can be customized](manage-spotlight.md) to display up to 11 items.

**News reader:** [The News reader](news-reader.md) presents SharePoint news from organizational sites, boosted news, the user’s followed sites, frequent sites, and people the user works with in an immersive reader experience. It also includes the option for users to request an AI generated news summary, powered by Copilot, providing a quick overview of all the latest news information.

**Dashboard:** [The Dashboard](viva-connections-overview.md#connections-dashboard) is your users’s digital toolset. It brings together the tools your users need, enabling quick and easy access whether they are in the office or in the field.

**Resources:** [The Resources](viva-connections-overview.md#connections-resources) experience enables navigation across portals and destinations.

**Viva Suite footer:** Information and links to other Viva Suite apps licensed and enabled by your organization appear at the bottom of the experience.

**Navigational elements:** The navigational elements located in the top-right and top-left corners help viewers easily get to-and-from other landing pages and [other Viva experiences](https://support.microsoft.com/topic/introducing-microsoft-viva-3c1012cb-6c85-4d49-bd7f-b18a6e7873e0).

## Get started customizing the experience

> [!NOTE]
>
> - You must have member level permissions (or higher) to edit the new desktop experience.
> - If your organization has a SharePoint home site, you can choose to use it as the default Connections experience.

### How to edit the Connections desktop experience for the first time

If you already have Connections setup, editors who have site owner or member permissions to the SharePoint home site  automatically have owner or member permissions to the new Connections experience in Teams. People with member permissions or higher can see **Edit** buttons in the Connections experience.

If you're setting up Connections for the first time, only owners of the SharePoint root site can edit. When the home experience is edited for the first time, a special site container gets created on the backend. You want to assign (at least two) owners and members from this site to give permissions to others so they can edit the experience for the rest of the organization.

### How to switch between multiple Connections experiences

If your organization created [multiple Connections experiences](/viva/connections/viva-connections-overview#connections-allows-for-multiple-home-sites-across-multiple-experiences), you can switch between enabled and draft experiences from within Connections in order to edit them.

1. Navigate to the Connections app in Teams.

2. Select the **ellipsis** in the upper-right of your Connections experience.

3. Then select **Switch Experience**.

   :::image type="content" source="../media/connections/edit-viva-home/vc3-switch-experience.png" alt-text="Screenshot showing additional options with switch experience highlighted.":::

   > [!NOTE]
   >
   > Only users with edit privileges are able to see the Switch Experience option in the menu.

4. A list of created experiences display along with their status (enabled or draft). Select an **Experience** to switch to.

5. Select **Switch**.

   :::image type="content" source="../media/connections/edit-viva-home/vc3-switch-experience-list.png" alt-text="Screenshot showing three available experiences and their status.":::

> [!NOTE]
>
> Users are required to have a Microsoft Viva suite or Viva Communications and Communities license in order to create two or more experiences (up to 50). See [Microsoft Viva plans and pricing](https://www.microsoft.com/microsoft-viva/pricing) for more info.

#### Give permission to edit from Connections in Teams

If you're setting up Connections for the first time, navigate to the Connections app in Teams to assign owners and members who can edit the Connections desktop experience.

1. Navigate to the Connections app in Teams.

2. Select the **ellipsis** in the upper-right of your Connections experience.

3. Then select **Manage access**.

4. Select **Grant access**.

5. Under **Site Access** add users and select their level of permission from visitor, member, or owner.

6. Select **Add**.

#### Choose default cards for the intended audience

When you set up Connections for the first time in Teams, you're asked to choose a set of default cards. The default cards help you get started creating a dashboard and don’t need anything to get set-up. Default cards can be removed and edited after the initial selection.

| Card descriptions | Frontline worker  | Information worker  |
|:------------------- |:------------------- |:---------------|
| Audience description  | This audience consists of users who are customer-facing, or don’t work primarily at a desk with a computer. Sometimes these roles are referred to as essential workers. Popular roles for frontline workers are retail sales associates, nurses, line workers, and teachers. |This audience consists of users who usually get their work done from a desk using a computer. Popular roles for information workers are project managers, finance associates, administrative personnel, and business executives.  |
| Default cards    | Approvals, Assigned tasks, Shifts, and Top news. | Assigned tasks, Top news, Viva Learning, and Viva Topics. |

By default, cards will already be on the dashboard and require minimal setup. Edit and preview the dashboard until you're ready to share with others. To edit existing cards, select the pencil icon to **Edit** the card. In the property pane that opens to the right of your experience, choose your card size from the **Card size** drop-down list. For more information on available dashboard cards and their properties, see the article on [available dashboard cards in Connections](available-dashboard-cards.md)

You can also apply **Audience targeting** so cards are filtered to specific roles, regions, or departments. Learn more about [audience targeting for Connections](use-audience-targeting-in-viva-connections.md).

### Summary of customizable elements

:::image type="content" source="../media/connections/edit-viva-home/vc3-customizable-elements.png" alt-text="Screenshot of the full page Connections experience with labels that explain which parts can be edited." lightbox="../media/connections/edit-viva-home/vc3-customizable-elements.png":::

1. **App icon and label in the Teams app bar:** Customize the app name and label in the [Teams admin center](add-viva-connections-app.md).

2. **Entry point to secondary landing page:** A link to the preferred default desktop experience automatically displays here.

3. **Change the look:** Access the settings to [apply themes](#apply-a-theme-to-your-connections-experience) to reflect your organizational brand colors consistently across experiences.

4. **Announcements:** Create targeted, time-sensitive messages that display at the top of your Connections experience to members of your organization. Learn more about [using announcements in Connections](announcements-viva-connections.md).

5. **Banner image:** Upload a banner image and set the focal point to create a branded look consistent across desktop and mobile.

6. **Spotlight:** The banner dynamically displays content from the home site, news from SharePoint sites, or links to articles or sites. The spotlight can be customized to display up to 11 items.

7. **Dashboard:** Customize with [cards and content](create-dashboard.md) specific to roles, regions, departments, and popular tasks.

8. **Resources:** Create a list of navigational links and icons to useful sites and information.

### Summary of noncustomizable elements

:::image type="content" source="../media/connections/edit-viva-home/vc3-non-customizable-elements.png" alt-text="Screenshot of the full page Connections experience with labels that explain which parts can be further edited." lightbox="../media/connections/edit-viva-home/vc3-non-customizable-elements.png":::

9. **Shared Viva navigation:** Helps viewers navigate between Viva experiences. Viva apps will automatically display in this menu when Viva licenses are detected.

10. **News reader:** Content in the News tab presents news posts from the user's followed SharePoint sites, frequent sites, trending sites, home site, organizational news sites, and news posts published by people the user works with. Users with a Microsoft 365 Copilot license can also [summarize the top news stories using Copilot from their desktop using Microsoft Teams. For more information, see the article on the [News reader](news-reader.md).

11. **Scoped Search**: Users can search within Connections when using the search bar while in the Connections experience. As users type, the option to search for results within Connections (or Teams) displays.

12. **Ellipses menu:** Access more information about the Connections experience depending on your level of permissions.

13. **Viva navigational bar:** The Viva navigational bar provides an opportunity to discover [more Viva experiences](https://support.microsoft.com/topic/introducing-microsoft-viva-3c1012cb-6c85-4d49-bd7f-b18a6e7873e0) and gets automatically generated when Viva licenses are detected.

## Customize the app icon and label in the Teams app bar

> [!NOTE]
>
> Connections is part of the [tailored apps experience](/microsoft-365/frontline/pin-teams-apps-based-on-license). Frontline users who see the tailored app experience have Connections pinned in the first position in the Teams app bar on both mobile and desktop.
>
> If you don’t want the app prepinned, either [turn off tailored apps for frontline workers](/microsoft-365/frontline/pin-teams-apps-based-on-license), change the [app settings](/microsoftteams/teams-custom-app-policies-and-settings), or [edit how apps in Teams are managed](/microsoftteams/manage-apps).

Your organization’s Connections app can display a custom icon and label in the Teams app bar. This customization takes place in the Teams admin center, which requires Teams admin permissions or higher. It's recommended that you also apply app settings that [prepin and preinstall the app](/microsoftteams/teams-app-setup-policies). Doing so makes sure people in your organization can more easily discover the Connections app and start using it. Learn more about [customizing the Connections icon, label, and app settings](#customize-the-app-icon-and-label-in-the-teams-app-bar).

## Customize the banner image

Change the banner image in the header and set the focal point for the image. The banner image and focal point can only be set on the desktop app but is visible across desktop and mobile.

> [!NOTE]
>
> - The greeting is automatically generated and can't be customized.
> - Depending on your organization's license type, you might see more dynamic information displayed in the banner.
> - The banner image and focal point resize when viewed via the tablet and mobile app.

To change the banner image:

1. Start by selecting **Edit** and then select **Change image**.

2. Select the image you’d like to use and then select **Reposition**.

3. Once you're satisfied with the focal point, select **Set focal point** and then **Save**. There's no draft state for the banner image. It's displayed for all users when you select Save.

## Apply a theme to your Connections experience

Further customize your Connections experience and SharePoint home site by applying preexisting [SharePoint themes](https://support.microsoft.com/office/320b43e5-b047-4fda-8381-f61e8ac7f59b) or a [custom theme](/sharepoint/dev/declarative-customization/site-theming/sharepoint-site-theming-powershell) to reflect your organizational brand colors consistently across all instances of your desktop, tablet, and mobile experiences. Users can apply themes from within their Connections experience, or SharePoint home site. Only users who have permissions to edit the Connections experience can apply themes.

> [!NOTE]
>
> If you have never selected a theme for your home site, the default SharePoint theme is used for the home site and Connections experience.

1. Select the **ellipsis**, then select **Change the look**.

    :::image type="content" source="../media/connections/edit-viva-home/vc3-change-the-look.png" alt-text="Screenshot of the settings menu open with Change the look option highlighted.":::

2. Select **Theme**.

3. Make a selection from the list of available themes.

   - Themes from your organization can't be customized.
   - SharePoint themes from Microsoft can be customized.

   :::image type="content" source="../media/connections/edit-viva-home/vc3-themes.png" alt-text="Screenshot showing examples of organization created themes and Microsoft default themes.":::

   > [!NOTE]
   >
   > - If an end user has selected dark mode on their mobile or tablet device, the dashboard and other Connections components render in dark mode with the default color and won't apply the theme colors.
   > - Dark themes (has the property `isInverted=True`), won’t be applied to the mobile experience. If the dark theme is selected, mobile will continue showing Connections with the user’s selected mode (light or dark) and the default colors.

4. Select **Save**.

   The home site color theme reflects automatically in the Connections desktop experience.

   > [!NOTE]
   >
   > Using [accent colors under the app customization feature](/microsoftteams/customize-apps) will only apply to the app icon outline color on the Teams chrome, and won't apply all colors to the Connections experience. For consistency of theming, it's a best practice to set the accent color same as the theme primary color from SharePoint.
   >
   > :::image type="content" source="../media/connections/edit-viva-home/vc3-teams-chrome.png" alt-text="Screenshot showing how accent colors apply.":::

## Customize the dashboard

The [Connections dashboard](create-dashboard.md#edit-a-viva-connections-dashboard) provides fast and easy access to information and job-related tasks. Add and edit cards that help users quickly access the tools and resources they use in their day-to-day role. Cards on the dashboard can be targeted to users based on specific roles, regions, and interests. Edits (including audience targeting settings) made to cards on the dashboard are also automatically applied to the [Dashboard web part](use-dashboard-web-part-on-home-site.md) and [the mobile experience](viva-connections-overview.md#the-connections-mobile-experience).

> [!NOTE]
>
> - If your organization already has Connections set up, you’ll see your existing cards and settings displayed in the new home experience.
> - If your organization doesn’t already have Connections set up, you’ll see a set of default cards that need minimal configuration.  

### Learn more about adding partner cards and creating custom cards

In addition to the core set of dashboard cards, cards from partner solutions can be added to the card toolbox from the SharePoint store. [Learn more about partner cards](https://techcommunity.microsoft.com/blog/spblog/explore-and-deploy-sharepoint-framework-solutions-from-partners-in-sharepoint-mi/2645289) and [how to request them](available-dashboard-cards.md#add-a-partner-card-or-microsoft-app). Additionally, customers can create custom cards for the Connections dashboard by using the [SharePoint Framework (SPFx)](/sharepoint/dev/spfx/sharepoint-framework-overview) to create Adaptive Card Extensions (ACEs). Learn more about this framework and view the [ACE solution gallery](https://appsource.microsoft.com/product/office/WA200003929).

### Preview the dashboard before sharing with others

After creating or editing cards on the Dashboard, make sure you preview the experience for each audience. Select **Preview** in the top-right corner of the editing experience, then choose to preview the desktop or mobile view. What you see in preview mode approximates how the Dashboard displays for certain audiences and devices. When you apply audience targeting to cards, you can preview how different people view the Dashboard depending on the audience or device.

## How news is given priority in the News reader

News comes from multiple sources: Home sites, boosted news, news from org news sites, the user’s frequent sites, followed sites, trending sites, and news published by people the user works with. News content from organizational news sites is given priority in the news reader. Boosted and organizational news is put before any team news.

- **Promote important ‘official’ communications** - Use [News boost](https://support.microsoft.com/office/boost-news-from-organization-news-sites-46ad8dc5-8f3b-4d81-853d-8bbbdd0f9c83) to raise the visibility of crucial news posts from organizational news sites.

- **Publish from official news sources** - Like [organizational news sites](/sharepoint/organization-news-site) or [SharePoint home sites](/sharepoint/home-site).

- **Follow SharePoint sites within your organization** – Users will see news posts added to their own News tab made on followed SharePoint sites.

## Language and multilingual settings

The Connections experience can be set in more than one language. Learn more about how [different elements of the experience can be edited to display in more than one language](viva-connections-language.md) and [how to create a multilingual dashboard](create-multilingual-dashboard.md).

> [!NOTE]
>
> Connections desktop applies the users’ SharePoint preferred language but not the Microsoft Teams language setting. However, for the mobile app, Connections applies the device settings.

## Manage permissions

The permissions model for the new Connections landing experience is like the permissions in SharePoint. Certain levels of permission grant access to specific editing tools and the ability to manage permissions and sharing.

> [!NOTE]
> At least two people should be assigned Owner level permissions.

| Owner       | Member            | Visitor     |
|:------------------- |:-------------------|:---------------|
| Can edit content in the banner, Dashboard, and Resources. <br><br> Can add or remove owners, members, and visitors.| Can edit content in the banner, Dashboard, and Resources.  | Visitors are the end users in your organization. <br><br> They can view and interact with content but can’t edit content or share the page with others. |

If you already have Connections setup, editors who have site owner or member permissions to the SharePoint home site will automatically have owner or member permissions to edit the new Connections experience in Teams.

- People with member permissions *or higher*  can see the **Edit** buttons in the Connections experience.
- People with member permissions or higher can view permissions to the page by navigating to the ellipsis menu in the top-right and selecting **Manage permissions**.

If you're setting it up *for the first time*, only the SharePoint root site owners are able to edit the Connections experience in Teams. When the Connections experience is edited for the first time, a SharePoint site on the backend gets created. Assign owners and members from this site to give permissions to others so they can edit the experience for the rest of the organization. [Manage permissions from the Connections app in Teams](#give-permission-to-edit-from-connections-in-teams) to assign owner or member level permissions. Once permission levels are assigned, people with owner or member permissions can see the **Edit** buttons in the Connections experience.

### How to add, view, and edit permissions

If you have member permissions or higher, you can view who has permission to view and edit the Connections experience. Access permissions by navigating to the ellipsis menu (**...**) in the top-right corner and then select **Manage permissions**.

If you have owner permissions or higher, you can give access to new people and change the roles of the people who already have access. Select **Share** to give access to new people. Edit the roles of existing people by selecting the drop-down arrow and then select a new role. Changes are applied immediately.

## Help end users in your organization learn more

If your organization already has a SharePoint home site and you want to keep it as the landing experience for the Connections desktop experience, use the PowerShell command listed in the following section to use the SharePoint home site. Learn more about [setting up Connections in the Microsoft 365 admin center](set-up-admin-center.md).

> [!NOTE]
>
> For customers who already have Connections setup, your end users are automatically routed to the new Connections home experience in Teams if your organization decides to use the new design as the default experience. If your organization has a SharePoint home site, you can choose to keep it as the default home experience when the new experience is available.

## Choose the default landing experience for Connections desktop

If your organization already has a SharePoint home site and you want to keep it as the landing experience for the Connections desktop experience, use the PowerShell command listed in the following steps. If you decide to change the default experience from a home site back to the Connections home experience, run this command again using the `$false` parameter. To run this cmdlet, you must be a SharePoint admin.

1. [Download the latest SharePoint Online Management Shell](https://go.microsoft.com/fwlink/p/?LinkId=255251).

   > [!NOTE]
   > - If you installed a previous version of SharePoint Online Management Shell, go to Add or Remove programs and uninstall "SharePoint Online Management Shell".
   > - Run the command as a SharePoint Administrator.
   > - This command allows you to choose the default experience for the desktop app and doesn't affect the mobile experience.

2. Connect to SharePoint as a [SharePoint Administrator](/microsoft-365/admin/add-users/about-admin-roles#commonly-used-microsoft-365-admin-center-roles) in Microsoft 365. For more information, see the article on[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online).

3. Run `Set-SPOHomeSite -HomeSiteUrl <homesiteURL> -VivaConnectionsDefaultStart <$true/$false>`.

   - The parameter should be set to **`$false`** to use the new Connections desktop experience as the default landing experience.
   - The parameter should be set to **`$true`** to use a SharePoint home site as the default landing experience.

   **Example:**

   Contoso’s SharePoint home site URL is `https://contoso.sharepoint.com/sites/homeSite` in this example.

   **To set the default landing to the SharePoint home site:**

   `Set-SPOHomeSite -HomeSiteUrl "https://contoso.sharepoint.com/sites/homeSite" -VivaConnectionsDefaultStart $true`

   **To set the default landing to the new Connections desktop experience:**

   `Set-SPOHomeSite -HomeSiteUrl "https://contoso.sharepoint.com/sites/homeSite" -VivaConnectionsDefaultStart $false`

> [!NOTE]
>
> - It might take up to 15 minutes to see the updated default landing experience.
> - If you change the SharePoint home site to a different SharePoint home site, it might take up to a week for users in Connections to be directed to the new site. However, users can sign out and sign back in to clear the cache to view the new SharePoint home site sooner.

## Make the experience available to the end user

Once finished customizing your Connections experience, follow the steps to [enable the experience to make it visible to your audience](set-up-admin-center.md#step-5-enable-the-experience).

## Learn more

[More options coming soon for the Connections desktop experience](https://techcommunity.microsoft.com/blog/viva_connections_blog/more-options-coming-soon-for-the-viva-connections-desktop-experience/3644419)

[Overview: Viva Connections](viva-connections-overview.md)

[Use audience targeting in Viva Connections to personalize the experience](use-audience-targeting-in-viva-connections.md)
