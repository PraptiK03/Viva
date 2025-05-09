---
ms.date: 03/17/2025
title: "Viva Engage setup requirements"
description: "Guidance for setting up licensing and installation of Viva Engage for an organization."
ms.reviewer: ethli
ms.author: donnabouldin
author: v-rgrace
manager: elizapo
audience: Admin
f1.keywords:
- NOCSH
ms.topic: install-set-up-deploy
ms.service: viva-engage
ms.localizationpriority: medium
ms.collection:  
- M365initiative-viva
- highpri
- essentials-get-started
search.appverid:
- MET150
---
# Viva Engage setup requirements

This article describes top-level setup procedures for admins and users of Viva Engage, including configuration on its supported surfaces including Microsoft Teams and mobile. To perform Microsoft Viva Engage setup tasks, you must have Engage administrator permissions.

## Set up Core Service Plan licensing for Viva Engage

As a foundational component of Microsoft Viva Engage, the Core Service Plan provides features and capabilities to promote engagement and collaboration in your organization.

**If you *don't* enforce Viva Engage licensing**, users can still access the Viva Engage Core experience.

**If you *do* enforce Viva Engage licensing**, users access the Viva Engage Core experience, but each user must have the following:

- a Microsoft 365 license.
- a Viva Engage Core Service Plan.

## Premium experience

Your organization can use premium Viva Engage experiences if your tenant owns either of these plans:

- Microsoft Viva Suite
- Microsoft Viva Employee Communications and Communities

>[!NOTE]
>Viva Engage licenses aren't required for admins to configure Viva Engage core or premium.

Unlike Viva Engage users, Engage administrators (also called Yammer administrators in Microsoft Entra ID) don't require a Viva Engage Core or premium license to access the [Engage website](https://engage.cloud.microsoft), the Engage admin center, or legacy network admin center.

Other Viva Engage admin roles can also administer premium features without being assigned a premium license.

|Service plan |Enables |Comes with this product |
|-------------------|---------|-------|
|**Viva Engage Core or Yammer enterprise**|Engage core experiences and the Answers in Viva core experiences <br> *Example:* Communities, storyline |Microsoft 365|
|**Viva Employee Communities and Communications**|Engage premium experiences <br> *Example:* Leadership corner, AMAs (Ask Me Anything), storyline announcements, delegation, analytics, and campaigns |Microsoft Viva Suite, Microsoft Viva Employee Communications and Communities |
|**Viva Engage Knowledge**|[Answers in Viva premium experience](/viva/engage/eac-answers-overview-set-up#licensing) |Microsoft Viva Suite and Microsoft Viva Employee Communications and Communities |

## Configure and review privacy and security settings

The Engage admin (Yammer administrator) can manage data, privacy, and security settings in Viva Engage. For details, see [Overview of security & compliance](/viva/engage/manage-security-and-compliance/security-and-compliance).

## Set up Viva Engage

Where you set up Viva Engage is a matter of preference.

Engage admins (Yammer administrators in Microsoft Entra ID) can use the Microsoft 365 admin center for initial setup. To control some Viva features, such as Copilot in Viva Engage, you must use [Microsoft 365 feature access management](/viva/feature-access-management).

The Engage admin center provides most Viva Engage settings and customization options.

The Microsoft 365 admin center supports the following tasks:

- Assign [Engage and Answers admins](eac-key-admin-roles-permissions.md).
- Pin Viva Engage in Teams.
- Manage other settings in Viva Engage.

## Install Viva Engage in Teams

The Microsoft Teams admin can deploy and pin the app for all users, or for particular departments, through a [Teams app setup policy](/microsoftteams/teams-app-setup-policies).

Setup policies allow users to easily set up Viva Engage themselves, using the following steps:

1. Open Teams on the web or in a desktop client.
2. From the left rail in Teams, select **Apps**.
3. Search for Viva Engage.
4. Select the Viva Engage app, and then select **Add**. The app is added to all your Teams clients, including mobile.

## Install or access Viva Engage on other surfaces

Using the following links, you can direct users to other installation options:

- [Install the Viva Engage desktop app](https://support.microsoft.com/office/install-the-viva-engage-desktop-app-66ccb412-ca1d-4e43-872c-9705abf11b1b)
- [Install Viva Engage on your iOS or Android phone](https://support.microsoft.com/office/set-up-viva-engage-on-your-mobile-phone-e52e65ad-14fa-4db9-b8f7-80fe3f6e25a7)
- [Access Viva Engage on the web](https://engage.cloud.microsoft.com/)

## Customize the Viva Engage appearance in the Teams store

Customizing the Viva Engage app is a good choice for companies that tailor their network branding to fit their corporate identity. From the Teams app store, you can customize the appearance for the following Viva Engage properties:

- app name
- app description
- app icons
- accent color

> [!NOTE]
> Currently, customizations don't affect the Viva Engage app branding that appears _within_ the Viva Engage Experience. Learn more about [customizing details of an app](/MicrosoftTeams/customize-apps#customize-details-of-an-app).

## Support adoption of Viva Engage

Review the contents of the [Viva Engage Adoption page](https://adoption.microsoft.com/en-us/viva/engage/) to help you get started, train and engage your organization, build champions, and to secure your environment.

>[!NOTE]
>If you’re setting up the premium Viva Engage experience, make sure to assign admin roles specific to Viva Engage to ensure usage and successful adoption of its many premium features.

### See also

[Manage administrator roles and permissions in Viva Engage](eac-key-admin-roles-permissions.md)
[Manage licenses in Microsoft 365](/Viva/engage/manage-engage-licenses-microsoft-365)
