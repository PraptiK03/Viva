---
ms.date: 11/08/2024
title: "Create and edit a Viva Connections dashboard"
ms.reviewer: evanatkin
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
  - highpri
search.appverid:
- SPO160
- MET150
description: "Learn how to edit the Viva Connections dashboard from Teams and SharePoint, how to apply audience targeting, and how SSO works with some dashboard cards."
---

# Edit a Viva Connections dashboard

The Viva Connections dashboard provides fast and easy access to information and job-related tasks. Content on the dashboard can be customized and then targeted to users in specific roles, markets, and job functions. It consists of cards that engage viewers with existing Microsoft Teams apps, Viva apps and services, partner apps, custom solutions using the SharePoint Framework (SPFx) framework, internal links, and external links.

![Screenshot that shows a Dashboard example for desktop and mobile.](../media/connections/vc-dashboard-flw.png)

The Connections dashboard can be edited from within your Connections experience.  

![Diagram of how to create a Viva Connections Dashboard.](../media/connections/viva-dashboard-step.png)

> [!NOTE]
>
> - You're asked to select your primary audience to generate a set of default dashboard cards for when setting up your experience for the first time.
> - Operators or members should limit the number of dashboard cards to about 20 for the best viewing experience.
> - Operator or member permissions are required to edit the Connections dashboard.
> - Users are able to customize their dashboard in Viva Connections on [desktop](https://support.microsoft.com/office/3da30f39-684a-4bde-bb81-2e1407d59b52#bkmk_desktop_customize_dashboard) and [mobile](https://support.microsoft.com/office/753e0607-0bfd-4712-ad7e-18490dd565a2#bkmk_customize-viva-connections-mobile-dashboard) by reordering, hiding, and showing cards. These changes only affect the experience for the user.

1. From within your Connections experience, select **Edit** in the dashboard section.

2. Select **+ Add a card**.

3. Select **Edit** (pencil icon) for each card to edit properties like the label, icon, image, and audience targeting settings where applicable.

4. Select **Delete** (trash can icon) to remove cards.

5. [Preview the experience](use-audience-targeting-in-viva-connections.md#preview-your-connections-dashboard-to-see-how-it-displays-for-different-audiences) on all devices to ensure usability before publishing or republishing.

6. **Publish** or **Republish** when you're done to share the edits with others.

## Change the dashboard settings

The dashboard details contain settings for your dashboard, page versioning, and controls for the Editor and enabling user customization on their personal dashboard view.

> [!NOTE]
>
> Some settings are only available to the Connections experience owner.

1. From Connections, select **Edit**.

2. Select **Dashboard details** above the dashboard.

    :::image type="content" source="../media/connections/create-dashboard/dashboard-details-expanded.png" alt-text="Screenshot showing the Dashboard details button"  lightbox="../media/connections/create-dashboard/dashboard-details-expanded.png":::

3. In the Dashboard details pane, you can add a thumbnail and description to show in search results:

    - **Change Thumbnail**: Select to add an image to be shown in search results.

    - **Description**: Enter a description in the text field to be shown in search results.

4. The **Editor** can be toggled off or on. When enabled, the editor checks spelling and grammar (Enabled by default).

5. **Allow users to rearrange and hide dashboard cards** can be enabled or disabled (Enabled by default):
    - If enabled, users see the **Customize** button on their dashboard, which enables them to show or hide unused dashboard cards, reorder their dashboard card view, and add their own cards.

    - Changes users make to their dashboard are only seen by that user. Any updates or changes to the dashboard by an owner or member of the experience will override the user’s personal changes.

> [!NOTE]
>
> Disabling user customization resets all user dashboard views to what the organization created. This includes removing any dashboard cards the user added to their dashboard.
>
> For more information how end users can customize their dashboard, see the relevant sections in the [dashboard](https://support.microsoft.com/office/3da30f39-684a-4bde-bb81-2e1407d59b52#bkmk_desktop_customize_dashboard) and [mobile](https://support.microsoft.com/office/753e0607-0bfd-4712-ad7e-18490dd565a2#bkmk_mobile_customize_dashboard) articles.

   :::image type="content" source="../media/connections/create-dashboard/dashboard-details-pane.png" alt-text="Screenshot of the dashboard details pane with numbered callout corresponding to steps three through five." lightbox="../media/connections/create-dashboard/dashboard-details-pane.png":::

6. When finished making your changes, select the **X** to close the Dashboard details pane.

### Edit the dashboard from your SharePoint home site

If your organization has a [SharePoint home site](home-site-plan.md), you can set up and edit the dashboard from the SharePoint home site or in Microsoft Teams. You need [edit permissions](/sharepoint/customize-sharepoint-site-permissions) for the SharePoint home site to make changes.

> [!NOTE]
> Images are an important aspect to making your cards rich and inviting. If you're a SharePoint admin, we recommend enabling a Content Delivery Network (CDN) to improve performance for getting images. Consider when storing images that /siteassets is by default a CDN source when Private CDN is enabled while /style library is the default source when the Public CDN is enabled. [Learn more about CDNs](/office365/enterprise/content-delivery-networks).

1. From the SharePoint home site, select the **Settings** gear at the top-right of the page.

2. Select **Manage Viva Connections**.

3. Select the **+ Create dashboard** or **View dashboard** button.

4. Select **+ Add a card**.

5. Select the type of card you want to add from the dashboard card toolbox and then use the instructions within this article to set up each type of card. As you’re building the dashboard, you can preview its appearance in mobile and desktop for different audiences.

6. When you're done adding cards and [applying targeting to specific audiences](use-audience-targeting-in-viva-connections.md), **Preview** the experience to ensure an ideal viewing experience.

7. Once you’re satisfied with how the dashboard looks in preview, select **Publish** or **Republish** at the top-right of your dashboard to make it available for use on your home site, in Teams, and in the Teams mobile app.

### Use the Dashboard web part for Viva Connections

Once a dashboard is authored and published in your Connections experience, you can use the Dashboard web part to display it on any section of your SharePoint site. If your organization has a SharePoint home site, you can set up and edit the dashboard from the SharePoint home site, Microsoft Teams, or the [Viva home site](https://viva.cloud.microsoft/).

> [!NOTE]
>
> - After editing content on the dashboard, it might take several minutes until the new content is available in the Dashboard web part.
> - For best results, we recommend placing the Dashboard web part in a right vertical section.

![Screenshot of the Viva Connections Dashboard web part highlighted in the Connections site.](../media/connections/vc-dashboard-web-part.png)

When added, the Dashboard web part automatically populates with the cards from the existing dashboard on your site. You can set the maximum number of cards you want to display. [Learn how to use the Dashboard web part](/sharepoint/use-dashboard-web-part-on-home-site).

## Customize your dashboard with cards and audience targeting

Further customize your dashboard by adding various cards meant to help users perform specific tasks. Add another layer of customization with audience targeting and build a unique dashboard experience with content for specific groups within your organization.

For a list of available dashboard cards, along with a description of the tool and steps for setting up, refer to the article on [Available dashboard cards in Viva Connections](available-dashboard-cards.md).

For more information on audience targeting and aspects of your Connections experience it can be applied to, see the article on [applying audience targeting to dashboard cards](use-audience-targeting-in-viva-connections.md#apply-audience-targeting-to-cards-in-the-dashboard).

## How URLs and single sign-on works

For some cards, you'll use links to URLs. Depending on the location of the content, links to URLs might display content in Microsoft Teams or elsewhere and [Single sign-on (SSO)](/azure/active-directory/manage-apps/what-is-single-sign-on) behavior can differ. Get more information about how links to URLs and SSO behave depending on the location of the content you're linking to.

> [!NOTE]
> When SSO isn't supported, users are asked to enter their sign-in credentials.

| Opens URL to… | On Teams mobile | On Teams desktop |
| :------------------- | :------------------- |:---------------|
| Teams App | Teams apps (like Shifts, Approvals, or Kudos) open within Teams and user doesn’t need to authenticate again. | Teams apps (like Shifts, Approvals, or Kudos) open within Teams and user doesn’t need to authenticate again. |
| Forms  | Forms open within Teams, user is asked to sign-in on the first time, and user doesn’t need to authenticate again if they stay signed in. | Forms open within Teams, user is asked to sign-in on the first time, and user doesn’t need to authenticate again if they stay signed in. |
| Viva Engage | Viva Engage opens within Teams, user is asked to sign-in on the first time and user doesn’t need to authenticate again if they stay signed in. | Opens a web browser session and the user might need to reauthenticate depending on browser and machine settings. |
| PowerApps  | PowerApps opens within Teams, user is asked to sign-in on the first time and user doesn’t need to authenticate again if they stay signed in. | Opens a web browser session and the user might need to reauthenticate depending on browser and machine settings. |
| Power Portals  | Power portals open within Teams, user is asked to sign-in on the first time and user doesn’t need to authenticate again if they stay signed in. | Opens a web browser session and the user might need to reauthenticate depending on browser and machine settings. |
| Stream   | Stream opens within Teams, user is asked to sign-in on the first time and user doesn’t need to authenticate again if they stay signed in. | Opens a web browser session and the user might need to reauthenticate depending on browser and machine settings. |
| External Links  | Web view opens within Teams and the user might need to authenticate again (depending on the site.)  | Opens a web browser session and the user might need to reauthenticate depending on browser and machine settings. |

## More resources

[Step-by-step guide to setting up Viva Connections](set-up-admin-center.md)

[Learn more about how to plan a dashboard](plan-viva-connections.md#step-1-plan-for-viva-connections)

[Design your own dashboard card with the card designer](use-card-designer.md)

[Available dashboard cards in Viva Connections](available-dashboard-cards.md)
