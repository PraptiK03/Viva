---
ms.date: 02/14/2025
title: "Use announcements in Viva Connections"
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
description: "Use announcements in Viva Connections"
---

# Use announcements in Viva Connections

Announcements allow you to create, manage, and schedule time-sensitive messages in Connections to users in your organization, all from your Connections experience.

:::image type="content" source="../media/connections/announcements-viva-connections/display-announcement-in-connections-for-mobile.png" alt-text="Screenshot that shows what an announcement in Viva Connections looks like on a mobile device."lightbox="../media/connections/announcements-viva-connections/display-announcement-in-connections-for-mobile.png":::

> [!NOTE]
>
> - Users are required to have a Microsoft Viva suite or Viva Communications and Communities license to utilize the announcements feature. See [Microsoft Viva plans and pricing](https://www.microsoft.com/microsoft-viva/pricing) for more info.
> - Only email-enabled security groups are supported.
> - You must have edit permissions or higher to your organization’s SharePoint home site or Viva Connections to author and manage announcements.
> - Announcements are unavailable in GCC, GCC High, and DoD environments. For more information, see the [list of platform features in Viva Connections](/office365/servicedescriptions/office-365-platform-service-description/office-365-us-government/office-365-us-government#platform-features).


## When to use announcements

Announcements are the best way to communicate targeted, time-sensitive information in the Connections app. Some examples include:

- To remind users of a specific role about upcoming deadlines, like time sheets, application deadlines, etc.
- To share details about open enrollment benefits with a link to your organization’s Human Resources website.
- To send a specific call to action for new users, such as reminders of required security trainings, morale events, etc.

> [!IMPORTANT]
>
> For emergencies such as a safety hazard, it’s recommended to use multiple modes of communication.

### Best practices for using and writing announcements

- Announcements aren’t designed for life-threatening emergencies.
- Keep messages short with a clear call to action. Provide a link to more information for more complex topics.
- Use audience targeting to specify which audiences need to receive the announcement to ensure the highest engagement possible.
- Use announcements sparingly so that users understand their importance. Sending them too frequently can cause users to disregard the notifications.
- Allow users to dismiss announcements for less-urgent topics or when there are several high priority announcements active at the same time.
- The delivery time increases with the size of the targeted audience. Sending an announcement to a group of 50 users might take a few minutes but sending one to 100,000 users can take several hours.

## Manage announcements from the announcements page

You can view, create, and manage all announcements (active, scheduled, drafts, and expired) from the Announcements page from your Connections experience or SharePoint home site.

:::image type="content" source="../media/connections/announcements-viva-connections/announcements-page.png" alt-text="Screenshot of the announcements page with multiple announcements visible." lightbox="../media/connections/announcements-viva-connections/announcements-page.png":::

**To access the announcements page in Connections:**

1. Select the **ellipsis** (![Screenshot of the ellipsis icon](../media/connections/connections-ellipsis-settings.png)) in the upper-right of the Connections experience.

2. Select **Manage announcements** from the list.

3. The announcements page opens where users can select **+ New announcement** to begin drafting an announcement.

**To access the announcements page from the SharePoint home site:**

1. Select the **Settings icon** (![Screenshot of the SharePoint Settings icon](../media/connections/announcements-viva-connections/SharePoint-settings-icon.png)) in the upper-right of SharePoint to open settings.

2. Select **Manage Viva Connection**.

3. Select **Manage Announcements**.

4. The announcements page opens where users can select **+ New announcement** to begin drafting an announcement.

### Create a new announcement

When creating a new announcement, you can choose up to 10 audiences to send to, set an expiration date, schedule a future send date, provide a link to users for more information, and allow users to dismiss the announcement.

1. From the Announcement page, select **+ New Announcement**.

> [!NOTE]
>
> You can also create a new announcement from your SharePoint home site by selecting **+ New**, then select **Announcement** to begin creating your announcement.

2. Add a **title** and **message**.

3. Select up to 10 audiences to distribute the announcement to. Audiences can be Microsoft Entra groups, Microsoft 365 Groups, or Microsoft Entra dynamic groups.

4. To schedule the message, enable **Scheduling** and enter the **date** and **time** the announcement should be set (Scheduling is off by default and the scheduling date and time fields only display if scheduling is enabled).

5. Select an **end date and time** (up to two weeks from posting) for the announcement to expire. Expired announcements won't display to users.

    :::image type="content" source="../media/connections/announcements-viva-connections/create-announcement-details.png" alt-text="Screenshot of the announcement details pane with numbered callouts" lightbox="../media/connections/announcements-viva-connections/create-announcement-details.png":::

> [!NOTE]
>
> At any time while creating your announcement, you can select **Save as draft** to save the announcement as a draft and work on it later from the announcement page.

6. Under **More options**, you can **add a link** to more information. Enter a URL and label for the link.

7. To allow users to dismiss the announcement after viewing, enable the **Allow users to dismiss setting**.

    :::image type="content" source="../media/connections/announcements-viva-connections/create-announcement-more-options.png" alt-text="Screenshot of the announcment details pane showing the add a link and allow users to dismiss fields." lightbox="../media/connections/announcements-viva-connections/create-announcement-more-options.png":::

8. Select **Next** to review the details of your announcement.

9. Select **Send announcement** when you're ready to send.

    If the announcement is scheduled for a future date, send announcement will instead become **Schedule announcement**.

> [!NOTE]
>
> Once an announcement is sent, message details and end date can still be edited.

   :::image type="content" source="../media/connections/announcements-viva-connections/schedule-announcement.png" alt-text="Screenshot of the announcement review page." lightbox="../media/connections/announcements-viva-connections/schedule-announcement.png":::

### Edit an active, scheduled, or draft announcement

1. Access the **Announcements** page.

2. Select the **pencil** icon next to the announcement you want to edit.

    :::image type="content" source="../media/connections/announcements-viva-connections/edit-announcement.png" alt-text="Screenshot of the announcement page with the edit icon highlighted." lightbox="../media/connections/announcements-viva-connections/edit-announcement.png":::

3. Make any desired changes in the **Announcement details**, then select **Next**.

4. Choose to send, schedule, or save as draft to apply your edits.

### Delete an announcement

1. Access the **Announcements** page.

2. Select the **trashcan** icon next to the announcement you want to delete.

> [!NOTE]
>
> Deleted announcements can’t be recovered.

   :::image type="content" source="../media/connections/announcements-viva-connections/delete-announcement.png" alt-text="Screenshot of the announcement page with the delete icon highlighted." lightbox="../media/connections/announcements-viva-connections/delete-announcement.png":::

3. When prompted, choose **Yes, delete**.

4. If the announcement was active, users won’t be able to view it, but might still be accessible through a Teams notification.

## How announcements display in Connections

Announcements sent to users appear differently depending on if they're accessing their Connections experience from a mobile, tablet, or desktop device.

> [!NOTE]
>
> For details on how announcements display for frontline workers, see the section on [Teams Channel announcements in Viva Connections](#announcements-for-frontline-workers).

### How announcements display on mobile and tablet devices

**In the Teams mobile app**: Users get a Teams notification displayed on the lock screen of their mobile device alerting them of a new announcement  ([Teams notifications must be enabled by the user](https://support.microsoft.com/office/1cc31834-5fe5-412b-8edb-43fecc78413d)).

   :::image type="content" source="../media/connections/announcements-viva-connections/announcement-mobile-lockscreen.png" alt-text="Screenshot showing the lock screen of a mobile phone with an announcement displayed." lightbox="../media/connections/announcements-viva-connections/announcement-mobile-lockscreen.png":::

Users can also see the announcement appear under the **Activity** tab in Microsoft Teams. Selecting the announcement opens it in the Connections app on the Teams mobile app.

   :::image type="content" source="../media/connections/announcements-viva-connections/announcement-mobile-activity.png" alt-text="Screenshot of the Activity tab in Teams mobile showing an announcement." lightbox="../media/connections/announcements-viva-connections/announcement-mobile-activity.png":::

**From the Connections app in Teams mobile**: Announcements display at the top of the Connections mobile experience.

   :::image type="content" source="../media/connections/announcements-viva-connections/display-announcement-in-connections-for-mobile.png" alt-text="Screenshot of an announcement displaying in the Connections app in Teams mobile." lightbox="../media/connections/announcements-viva-connections/display-announcement-in-connections-for-mobile.png":::

### How announcements display on desktop

When users [access their Connections experience](https://support.microsoft.com/office/8b4e7f76-f305-49a9-b6d2-09378476f95b#bkmk_access_connections_desktop) through SharePoint, Microsoft Teams, or the Viva Home suite, announcements display above the news spotlight.

   :::image type="content" source="../media/connections/announcements-viva-connections/announcement-desktop.png" alt-text="Screenshot of an announcement in Viva Connections." lightbox="../media/connections/announcements-viva-connections/announcement-desktop.png":::

When in Microsoft Teams, the announcement also appears in the **Activity** tab. Selecting the announcement opens it within the Connections experience.

   :::image type="content" source="../media/connections/announcements-viva-connections/announcement-desktop-activity.png" alt-text="Screenshot of an announcement displaying on the Activities tab in Microsoft Teams." lightbox="../media/connections/announcements-viva-connections/announcement-desktop-activity.png":::

## Announcements for frontline workers

The following section covers topics related to sending announcements to Frontline workers. Learn how to:

- Use @mentions in a Teams channel to send an announcement in Connections to Frontline workers.

- Target announcements to Frontline workers based on job attributes (location, title, etc.).

- How to map Frontline attributes to workers

- How to enable regional filtering.

- How to filter announcements based on Frontline worker attributes.

### How @ messages in a Teams channel display as an announcement in Connections for frontline workers

Frontline managers can communicate important updates to Frontline workers in Connections by using their Teams channel. Adding an @mention in the Teams channel message displays it to Frontline workers as an announcement in Connections across desktop and mobile experiences.

Frontline workers can then select the link within the Connections announcement to be redirected to the Teams channel where the announcement was made.

A Teams channel announcement is displayed in the Connections experience only if:

- The user is assigned a Microsoft 365 F1 or F3 license; and

- Channel mentions are enabled under the Teams channel notification settings; and

- The Teams channel announcement is tagged with an @mention and is unread.

For more information, see [sending an announcement to a channel in Microsoft Teams](https://support.microsoft.com/office/8f244ea6-235a-4dcc-9143-9c5b801b4992).

> [!NOTE]
>
> - If you have authentication issues, disable the **Limited-access user permission lockdown mode** under site collection features from your SharePoint site. Learn more about [enabling or disabling site collection features](https://support.microsoft.com/office/a2f2a5c2-093d-4897-8b7f-37f86d83df04).
> - Vanity domains aren't supported. Contact your organization's support team for more information.
> - An update to an existing Teams Channel announcement won't display in Viva Connections. Users need to follow the link from the original announcement in Viva Connections to view the Teams Channel announcement.
> - Teams Channel announcements that are deleted and then undone show as unread.

### Target announcements to frontline audiences based on department, location, and job title

Managers can now send targeted announcements based on a user’s department, location, and job title to frontline workers on a time-sensitive basis using Regional filtering.

Before Regional filtering can be enabled, Dynamic Teams at Scale (DTAS) and your organizations Hierarchy needs to be set up within the Teams admin center in order for the proper information to be available to filter.

> [!NOTE]
>
> - It's recommended to set up DTAS and your Hierarchy configuration before using this feature to avoid users receiving an error.
> - After DTAS and your Hierarchy are configured, regional filtering must be enabled in Connections.

#### Map frontline attributes in the admin center

There's some preliminary configuration required before regional filtering can be enabled in Connections.

1. First, your organization needs to set up DTAS within the [Teams admin center](https://admin.teams.microsoft.com/).

2. If DTAS is set up for your organization, you need to set up your frontline operational hierarchy through a CSV file uploaded to the Teams admin center. The CSV file enables you to map your organization’s structure of frontline teams and locations to a hierarchy.

3. After the hierarchy is in place, you'll be able to map your frontline attributes to the Microsoft Entra ID attributes that represent your organization’s departments and job titles.

4. Your final step is to enable regional filtering in Viva Connections.

For more information, see the article on [deployment of frontline dynamic teams at scale](/microsoft-365/frontline/deploy-dynamic-teams-at-scale).

##### To get started creating your CSV hierarchy file

1. In the left navigation of the [Teams admin center](https://admin.teams.microsoft.com/), choose **Teams > Manage frontline teams**.

2. Go to the **Operational hierarchy tab**.

3. Choose **Get Started**. The **Operational hierarchy** pane opens, and from here, you can upload your hierarchy CSV file or download a CSV template to create one.

4. Select **Download the CSV template** to create your file.

5. After creating the file, return to the **Operational hierarchy tab**.

6. Choose **Get Started** and upload your CSV file.

For more information, see the article about [deploying your frontline operational hierarchy](/microsoft-365/frontline/deploy-frontline-operational-hierarchy).

##### To map frontline attributes

Map your attributes on the Map frontline attributes page of the [deploy frontline dynamic teams](/microsoft-365/frontline/deploy-dynamic-teams-at-scale?view=o365-worldwide&preserve-view=true) experience. Select the Microsoft Entra attribute for **Department** and **Job title** that best represents the departments and job titles in your organization. You can map one or both attributes.

For more information, see the article on [setting up for targeted communications for your frontline](/microsoft-365/frontline/set-up-targeted-communications).

##### Enable Regional filtering

After the DTAS and Hierarchy service is configured in Microsoft Teams, enable **Regional filtering** within the Announcements page in Viva Connections (or from your SharePoint home site).

**To enable from Viva Connections:**

1. After accessing the announcements page, select **Settings** in the upper-right corner of the page.

2. In the Settings pane, select the toggle to enable **Regional filtering**.

   :::image type="content" source="../media/connections/announcements-viva-connections/target-announcement-enable.png" alt-text="Screenshot of the regional filtering option in settings." lightbox="../media/connections/announcements-viva-connections/target-announcement-enable.png":::

3. Select **Save** to save your changes.

**To enable from a SharePoint home site**:

1. After accessing the announcements page, select **Settings** in the upper-right corner of the page.

2. In the Settings pane, select the toggle to enable **Regional filtering**.

3. Select **Save** to save your changes.

#### Filter announcement by Frontline worker properties

After location, department, and role values have been set up in Microsoft Teams, and regional filtering is enabled in Viva Connections, owners and members will see options to filter their announcement based on the new set of frontline worker properties created in Microsoft Teams.

To create an announcement filtered by frontline worker properties, follow the steps for [creating your announcement](/viva/connections/announcements-viva-connections#create-a-new-announcement) up to selecting your audience:

1. Select **Filter by property**.

2. Select from three properties to enable announcement filtering based on the following variables:

- **Location**: enter a location in the text field to filter down based on available choices or select the drop-down arrows to choose multiple locations from a list of available options. Up to 10 locations can be selected.

- **Department**: enter a department in the text field to filter down based on available choices or select the drop-down arrows to choose multiple departments from a list of available options.

- **Job title**: enter a job title in the text field to filter down based on available choices, or select the drop-down arrows to choose multiple job titles from a list of available options.

   :::image type="content" source="../media/connections/announcements-viva-connections/target-announcement-properties.png" alt-text="Screenshot of the Viva Pulse properties." lightbox="../media/connections/announcements-viva-connections/target-announcement-properties.png":::

3. Continue creating your announcement until you're ready to send.
