---
title: Access the Viva Glint platform
description: Active Microsoft Viva Glint admin and dashboard users can access Viva Glint with a Microsoft Entra ID user account and an ACTIVE status in the Viva Glint app. Use this article to learn about supported internet browsers, access links, session time-outs, login troubleshooting, and dashboard experiences.
ms.author: aweixelman
author: AliciaWeixelman
manager: melissabarry
audience: admin
f1.keywords: NOCSH
keywords: platform, access, session, browser, glint access
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 02/10/2025
---

# Access the Viva Glint platform

Active Microsoft Viva Glint admin and dashboard users can access Viva Glint with a Microsoft Entra ID user account and an ACTIVE status in the Viva Glint app. Use this article to learn about supported internet browsers, access links, session time-outs, login troubleshooting, and dashboard experiences. 

> [!IMPORTANT]
> To successfully access Viva Glint, users must:
> - Exist in Entra with a Member Type of "Member" (not "Guest"). Learn more about how Microsoft 365 Global Administrators or Entra admins can [set up access to Viva Glint with Microsoft Entra ID](access-with-azure-ad.md).
> - Exist in the Viva Glint app with an "ACTIVE" employee status and membership to the Active Employees role.

## Select a supported browser

Viva Glint users can access surveys and dashboards with various internet browsers. Use this information to verify that your preferred browser is supported for accessing Viva Glint.

> [!IMPORTANT]
> All users must access Viva Glint from a browser that supports TLS 1.2, which includes the latest versions of Microsoft Edge, Google Chrome, Safari, and Mozilla Firefox.

|Browser  |Survey  |Dashboard|
|----------|-----------|------------|
|Microsoft Edge     |Supported       |Supported        |
|Google Chrome   |Supported       |Supported        |
|Safari     |Supported       |Supported        |
|Mozilla Firefox |Supported       |Supported        |
|iOS - Safari (Mobile)     |Supported       |Supported        |
|Android - Chrome (Mobile)|Supported       |Supported        |

> [!IMPORTANT]
> Internet Explorer isn't a supported browser.

## Access with a Microsoft Entra ID user account

Your Entra or other IT admins choose [authentication methods in Microsoft Entra ID](/entra/identity/authentication/concept-authentication-methods) for Viva Glint and other resources. For example: username and password + multifactor authentication with an app like Microsoft Authenticator. Select a link based on the region that your organization's Viva Glint tenant sits in and follow prompts to log in.

- US - [http://app.us1.glint.cloud.microsoft](http://app.us1.glint.cloud.microsoft)
- EU - [http://app.eu1.glint.cloud.microsoft](http://app.eu1.glint.cloud.microsoft)

## Session time-out

After 20 minutes of inactivity, you're prompted with an initial **"Are you still here?"** message. A Viva Glint session ends after another 10 minutes of inactivity.

:::image type="content" source="../../media/glint/setup/glint-inactive-session-message.png" alt-text="Screenshot of a message that appears when a user is inactive in their survey session.":::

## Login issues

If users experience login issues or repeated logouts when accessing Viva Glint, [review troubleshooting information](/viva/troubleshoot/glint/access/manager-access-issues?toc=%2Fviva%2Fglint%2Ftoc.json&bc=%2Fviva%2Fbreadcrumb%2Ftoc.json#unable-to-connect-to-the-glint-service) for common access problems.

## Dashboard experiences

Viva Glint Admins and dashboard users see different landing pages, or dashboards, in Viva Glint depending on their User Role and the role's settings. Learn more about [dashboard experiences for Viva Glint roles](/viva/glint/reports/dashboard-experiences).
