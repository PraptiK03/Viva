---
title: "Set up Answers in Viva"
description: "Overview and setup of Answers in Viva, including licensing, technical requirements, and data management."
ms.reviewer: davidchang
ms.author: donnabouldin
author: v-rgrace
manager: elizapo
ms.date: 01/13/2025
audience: Admin
f1.keywords:
- NOCSH
ms.topic: install-set-up-deploy
ms.service: viva-engage
ms.localizationpriority: high
ms.collection:  
- M365initiative-viva
- highpri
search.appverid:
- MET150
---

# Set up Answers in Viva

**Answers in Microsoft Viva** is a new experience for people in large organizations to ask and answer questions from one another. Use the feature in the Viva Engage Teams app, on the **Answers** tab, and on the **Communities** tab in communities of which the user is a member.

The Answers feature enables users to ask and get questions answered, connect with subject matter experts, and promote their learning process. Natural language processing helps match questions with available answers, and the experience rewards people who contribute to Answers.

## Licensing

The Viva Engage Knowledge service plan is part of the following licenses:

- Microsoft Viva Suite license
- Microsoft Viva Employee Communications license
- Microsoft Viva Employee Communities license

Users with the Viva Engage Knowledge service plan have access to the Answers experience. They can ask and answer questions in communities and on the **Answers** tab. Users can also find related questions, and receive rewards and recognition.  

Users without the Viva Engage Knowledge service plan don't have the full Answers experience. Those users can ask questions, and view, vote, and respond to questions from communities in which they’re a member. When their name is mentioned in Answers, they receive notifications to those questions and can visit those threads.

For more information about permissions, see [Manage admin roles in Viva Engage](eac-key-admin-roles-permissions.md).

## Technical requirements

By default, the Answers experience is enabled for networks where Viva Engage is enabled, and for all users of Viva Engage services. For the best Answers experience, we recommend that all organizations [install the Viva Engage app in Microsoft Teams](/viva/engage/setup#installing-viva-engage).

## Compliance and Answers data

By default, a group in Microsoft 365 backs up your Answers data. This group follows your organization’s default data [retention policies](/microsoft-365/compliance/retention-policies-yammer). The Answers backing group activates when a user posts the first question in the group or creates a question attachment. All Microsoft 365 Global admins are owners of the backing group, which is labeled *Group for Answers in Viva Engage – DO NOT DELETE.*

Backing group owners should ensure that Answers remains compliant with network policies. *Avoid accidental deletion of the backing group.* Admins can export group data before deleting the backing group in Microsoft 365. **Deletion of the Answers data backing group stops Answers from working.**

>[!NOTE]
> You can recover a soft delete within 30 days. A hard delete produces *permanent* data loss.

You can find Answers data in [eDiscovery](/viva/engage/manage-security-and-compliance/overview-of-ediscovery), so you can identify and deliver electronic information that can be used as evidence in legal cases.

### General Data Protection Regulation (GDPR)

For a GDPR user data export, verified Viva Engage admins and Engage admins can follow the [Viva Engage GDPR export guidance](/Viva/engage/eac-as-manage-data). Answers data is bundled with Viva Engage data. To comply with GDPR data subject requests, you can erase all information about a Viva Engage user. Learn [how to manage GDPR data subject requests in Viva Engage](./manage-security-and-compliance/gdpr-requests-in-viva-engage-enterprise.md).

## Configure the Answers experience

> [!NOTE]
> You must be a Microsoft 365 Global admin to configure Answers and Answers-related options.

Answers is enabled by default. You can hide Answers from view in the Viva Engage, which allows users to access Answers content only through existing links. If you hide Answers, users can't contribute to threads or navigate the Answers experience.

1. [Go to the Viva Engage admin center](admin-howto-access-admin-center-in-ve.md).

1. On the **Feature management** tab, select **Answers** to open Answers configuration.

1. Use the **Enable Answers** toggle to enable or disable Answers for your organization.

>[!NOTE]
> If Answers is disabled, the backing group complies with the default data [retention policies](/microsoft-365/compliance/retention-policies-viva-engage) set by your organization, *unless Answers uses a unique policy*.

## Option: Show Viva Engage experience

Answers resides within Viva Engage. Organizations that aren't ready to start using all the Viva Engage features can use a limited Answers-focused experience. Doing so hides other Viva Engage features such as storylines, communities, and leadership. You can still access hidden Viva Engage content through existing links, but users can't navigate to Viva Engage features other than Answers.

To use this feature, the network must have two or fewer Engage communities.

1. [Go to the Viva Engage admin center](admin-howto-access-admin-center-in-ve.md).

1. On the **Feature management** tab, select **Answers** to open Answers configuration.

1. Switch **Show Engage Experience** on or off for your organization.
This option is disabled if Answers is turned off, or if the tenant has more than two active communities.

:::image type="content" source="../media/engage/admin/answers-eac-show-exp-off.png" lightbox="../media/engage/admin/answers-eac-show-exp-off.png" alt-text="Screenshot shows that Answers must be enabled to turn off the Show Engage Experience setting.":::

> [!NOTE]
> If the Viva Engage Experience is hidden, the backing group respects the [data retention policies](/microsoft-365/compliance/retention-policies-yammer?view=o365-worldwide&preserve-view=true) set by your organization. The admin can still export and manage their data.

## Option: Enable AI-suggested topics

Users with the Viva Engage Knowledge service plan see AI-suggested topics in Answers. Viva Engage admins control this feature. When a user posts a question on Answers, generative AI returns up to three relevant topics for the user to include with their post.

1. [Go to the Viva Engage admin center](admin-howto-access-admin-center-in-ve.md).

1. On the **Feature management** tab, select **Answers** to open Answers configuration.  

1. Switch **Enable AI-suggested topics** on or off for your organization.

   :::image type="content" source="../media/engage/admin/ea-answers-ai-2.png" lightbox="../media/engage/admin/ea-answers-ai-2.png" alt-text="Screenshot shows AI-suggested topics turned off.":::

## Option: Enable rewards and recognition

When users contribute to Answers in Viva, they can earn and collect up to five different badges. Badges are available and visible to anyone in the organization who has a Viva Engage Knowledge service plan. This feature requires Answers to collect user data, such as votes from fellow employees, which count toward badges.

1. [Go to the Viva Engage admin center](admin-howto-access-admin-center-in-ve.md).

2. On the **Feature management** tab, select **Rewards and recognition**.

   [![Screenshot shows the interface for Answers badges settings in the Viva Engage admin center.](/Viva/media/netnew/badges-settings.png)](/Viva/media/netnew/badges-settings.png#lightbox)

3. Configure badges by selecting from these options:

   - **On** enables badges for the organization.

   - **User Preference** enables badges for the organization while allowing individuals to opt out. The end user can turn off badges in Viva Engage by selecting the ellipses (`...`) button on the right of their **Achievements and awards** page.
   - **Disabled** turns off badges in Answers in Viva. If you switch this control from **On** to **Disabled**, all badges earned by users are deleted and unrecoverable. Answers stops collecting user data for badges.

   [![Screenshot shows the Viva Engage interface where users can turn off Answers badges.](/Viva/media/netnew/badges-turn-off.png)](/Viva/media/netnew/badges-turn-off.png#lightbox)

## See also

[Administrator scenarios for Answers in Viva Engage](/viva/engage/eac-answers-admin-scenarios)

[Answers in Viva: Frequently asked questions (FAQ)](/viva/engage/eac-answers-faq)

[Manage administrator roles in Viva Engage](/viva/engage/eac-key-admin-roles-permissions)
