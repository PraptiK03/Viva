---
title: Set up the in-app Viva Pulse experience
description: "Set up the in-app Viva Pulse experience"
ms.reviewer: 
ms.author: hasrivas
author: hasrivas
manager: alisaliddle
audience: Admin
f1.keywords: NOCSH
ms.date: 12/19/2024
ms.topic: install-set-up-deploy
ms.service: viva-pulse
ms.localizationpriority: medium
ms.collection: m365initiative-viva-pulse  
search.appverid: MET150
---

# Set up the in-app Viva Pulse experience

The Viva Pulse in-app experience can be managed by users with the Viva Pulse admin role. If you're the Viva Pulse admin, you see a Manage tab next to the Home tab in the Viva Pulse header. You can manage all settings for the in-app Viva Pulse experience in the Manage tab. <br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RW1fCHB]

## Privacy settings

As an admin, you can set privacy options for your organization. This includes setting the minimum number of recipients required to send a pulse, the minimum number of responses required to see feedback once a pulse closes, adding a custom privacy policy statement, and choosing to turn off the collection of user diagnostic data.

### Minimum recipients required to send a pulse

All pulses require a minimum number of recipients to be added before they can be sent. Changing the default won't affect any currently deployed pulses. The minimum value allowed is 3 and maximum value allowed is 25. To update the minimum recipients required default value:

1. In the **Manage** tab, go to the **Privacy** tab.
2. Under the Minimum number of recipients and responses heading go to the Minimum recipients section, where you can select a value between 3 and 25 using either the carrot or typing in the value.
3. The value is autosaved.

### Minimum response required to see feedback

All pulses also require a minimum number of responses before authors can view feedback. Changing the default won't affect any currently deployed pulses. The minimum value allowed is 1 and maximum value allowed is equal to the current value of your Minimum recipients setting. To update the minimum responses required default value:

1. In the **Manage** tab, go to the **Privacy** tab.
2. Under the **Minimum number of responses required to see feedback** section,  you can select a value between 3 and 25 using either the carrot or typing in the value.
3. The value is autosaved.

### Customized privacy policy link

You can add your company’s privacy policy to be shown in the app in place of the Microsoft privacy statement. This change is reflected in three places: 

1. In the common navigation header (top right ellipses).
2. The 'Learn More' page, which appears when the author creates a new pulse during a new session.
3. Before starting pulse, when the respondent opens the pulse request to respond.

When the user clicks on **Privacy**, they're taken to your company’s privacy policy. To customize the privacy statement:

1. In the **Manage** tab, go to the **Privacy** tab.
2. In the search bar, copy and paste the link to your company's privacy policy site. 
3. The entry is autosaved.

### Diagnostic data

There are two types of data that we collect: Required Diagnostic Data (RDD) and Optional Diagnostic Data (ODD). By default, ODD and RDD are enabled. As an admin, you can go into the Admin Center in the Viva Pulse app and de-enable the collection of diagnostic data. Once collection of diagnostic data has been de-enabled, previously collected data for the tenant is still available, but additional data is no longer collected.

* Required Diagnostic Data: Telemetry collected to help us make product improvements and provide enhanced information to help us detect, diagnose, and remediate issues.
* Optional Diagnostic Data: Telemetry gathered to ensure the customers are secure, up to date, and performing as expected.

To turn off Required Diagnostic Data or Optional Diagnostic Data collection:

1. From the **Manage** tab, go to the **Privacy** tab.
2. Navigate to the **Required diagnostic data** and **Optional diagnostic data** section.
3. To turn off data collection for either Required Diagnostic Data or Optional Diagnostic Data, use the toggles associated with **Required Diagnostic Data** or **Optional Diagnostic Data**.
4. The update is autosaved.

### Data sharing

Viva Pulse survey results for the Copilot impact template is automatically shared to the [Microsoft Copilot Dashboard](/viva/insights/org-team-insights/copilot-dashboard). In the Microsoft Copilot Dashboard, leaders can analyze usage metrics that map sentiment data collected by Viva Pulse to workplace patterns data collected by Viva Insights. The individual Copilot impact sentiment is not joined to behavioral metrics in Insights Advanced Analytics in Workbench.

Data export of Copilot impact Pulse survey results to populate the Microsoft Copilot Dashboard may fail due to (1) system failure or (2) the Insights license did not complete provisioning in your tenant yet. As an admin, you can retry the data export for the Copilot impact Pulses to the Copilot Dashboard by selecting the retry button to retry all the failed Copilot impact Pulse data exports in your tenant.

If you do not see the section in the data sharing tab to retry the data export failures to the Copilot Dashboard, then all the Copilot impact Pulses were successfully exported to the Copilot Dashboard. If you are consistently seeing data export failures after retrying, ensure that the Insights license completed provisioning in your tenant.

To retry data export failures to the Microsoft Copilot Dashboard:

1. In the **Manage** tab, go to **Data sharing** tab.
2. Under the **Retry data export to Microsoft Copilot Dashboard** section, select the **Retry** button.

## Customization

> [!IMPORTANT]
> Customization administration is available only to those tenant administrators who are trying to access Viva Pulse with a premium license. If you are trying to access Viva Pulse with your Microsoft 365 Copilot subscription, you will not have access to the customization administration experience. 

### Customize Pulses

Customization is turned on by default, but as an admin, you can control whether feedback authors can add their own questions to existing stock templates or edit existing stock questions through granular access controls. To make any customization configurations, see [Granular access controls](./granular-access-controls.md).

### Customize your organization’s policy statement

As an admin, you can also set customization options for your organization, which includes an option to add a link to internal guidance and policies governing appropriate survey questions, which are shown to users during survey creation.

You can use this link to remind employees of internal policies and guidelines for writing survey questions within your organization. When the feedback author clicks on the link while customizing a survey, they are taken to your company’s internal policy.

1. In the **Manage** tab, go to the **Customization** tab.
2. Under the **Customized organizational policy statement** section, in the text box labeled **Link to organization’s policy statement**, type or paste a link to your company’s internal policy statement to be shown in the customization flow in place of the Microsoft policy statement.
3. The value is autosaved.

## Notifications

> [!IMPORTANT]
> Notification administration is available only to those tenant administrators who are trying to access Viva Pulse with a premium license. If you are trying to access Viva Pulse with your Microsoft 365 Copilot subscription, you will not have access to the notifications administration experience.

An employee’s ability to manage their email notifications preferences is default turned on, but as an admin, you can control whether the employee can manage their email notification preferences. Once the default is turned off, employees can't manage their email notification preferences and will receive all of Viva Pulse’s email notifications. You can also change the notification channels that users receive notifications from. To make any notification configurations:

1. In the **Manage** tab, navigate to the **Notifications** tab.
2. To turn on or turn off email notification preferences, use the toggle associated with **Allow users to opt out of emails**.
3. To update where users receive notifications, use the toggle associated with the preferred channel (Teams Activity Feed, Chatbot, Email).
4. The update is autosaved.

## Viva resources

> [!IMPORTANT]
> Viva resources administration is available only to those tenant administrators who are trying to access Viva Pulse with a premium license. If you are trying to access Viva Pulse with your Microsoft 365 Copilot subscription, you will not have access to the Viva resources administration experience.

Viva Pulse reports show recommended learning content for users to learn more about specific Pulse topics. These learning resources are sourced from LinkedIn Learning and can be viewed in the Viva Learning app. If your users are not subscribed to LinkedIn Learning or do not use Viva Learning, they will not be able to access those resources, even though the resources are shown. For example, a learning video might be displayed, but it will not play for those users. In this case, you may want to disable the display of these learning resources. To make any learning resource configurations:

1. In the **Manage** tab, navigate to the **Viva Resources** tab.
2. To turn on or turn off Viva Learning videos, use the toggle associated with **Viva Learning**.
3. The update is autosaved.

## Delete user data

As an admin, you can delete a user’s past Pulse requests and responses on the user’s behalf. Deletion of a user’s data is a hard deletion, and no record of the user’s data remains. You can only delete one user’s data at a time, and there's no limit as to how many times a user’s data can be deleted. To delete a user’s data:

1. In the **Manage** tab, navigate to the **Delete user data** tab.
2. Search for the user that requested their data be deleted by using the search bar and select that user in the populated options.
3. Select **Delete user data**.
4. Select **Delete user data** again in the confirmation box.
5. You see a status message in the deletion log that says **‘Pending’**. Deletions can take up to a few minutes.
6. Once the deletion is successful, the status of the deletion changes to **‘Deleted’**.
7. If the deletion was unsuccessful, then the status of the deletion changes to **‘Not Deleted’**. In this instance, please try the deletion again.

### Survey deletion

As an admin, you can delete any past and current Pulse surveys in your organization. This is different from template deletion by a content admin, where the content admin can delete a template so that users cannot use that template to send Pulse surveys in the future. Deletion of a Pulse survey is a hard deletion and no record of either the survey or the survey responses will remain. You can delete multiple surveys at a time by searching for an author’s name, and there is no limit as to how many surveys can be deleted. To delete a survey:

1. In the **Manage** tab, navigate to the **Survey deletion** tab.
2. Search for the author’s name in the search bar and select that user in the populated options.
3. Select the Pulse surveys you want to delete and click **Delete selected surveys**.
4. Select **Delete** in the confirmation popup.
5. You see a status message in the deletion log that says **‘In progress’**. Survey deletions can take up to a few minutes.
6. Once the deletion is successful, the status of the deletion changes to **‘Deleted’**.
7. If the deletion was unsuccessful, then the status of the deletion changes to **‘Not deleted’**. In this instance, try the deletion again.
