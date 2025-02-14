---
title: "Administrator scenarios for Answers in Viva Engage"
description: "Describes administration of Answers in Viva Engage for the Microsoft 365 Global admin, Engage admin, and Answers admin."
ms.reviewer: vfurlong
ms.author: donnabouldin
author: v-rgrace
manager: elizapo
ms.date: 12/17/2024
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva-engage
ms.localizationpriority: high
ms.collection:  
- M365initiative-viva
- highpri
search.appverid:
- MET150
---

# Administrator scenarios for Answers in Viva Engage

Administration of Answers requires either an Engage admin or Answers admin role.

>[!NOTE]
>The Microsoft 365 Global administrator can designate an Answers admin by [adding a Knowledge manager in Microsoft Entra ID](/azure/active-directory/fundamentals/active-directory-users-assign-role-azure-portal?context=%2Fazure%2Factive-directory%2Froles%2Fcontext%2Fugr-context). Knowledge managers are Answers admins and have elevated permissions over end users. For more information, see [Manage admin roles in Viva Engage](/Viva/engage/eac-key-admin-roles-permissions).

## Update information panel

### Provide guidance using the information panel

The Answers admin or Engage admin can use the information panel to provide guidance to employees on how to use Answers within the organization. By default, the information panel is only visible to administrators. After an admin saves and publishes the information panel, all other employees with access to Answers can see the information panel.

**Admin view**<br/>
:::image type="content" source="../media/engage/admin/ans-info-pan-admin1.png" lightbox="../media/engage/admin/ans-info-pan-admin1.png" alt-text="Screenshot of the information panel with guidelines option.":::

**End user view**<br/>
:::image type="content" source="../media/engage/admin/ans-info-pan-end-user.png" lightbox="../media/engage/admin/ans-info-pan-end-user.png" alt-text="Screenshot of how the information panel looks to end users.":::

### Edit the information panel

1. Select the edit icon from the top left corner of the information panel.
1. Enter the content specific to your organization.
1. Select **Save and publish** to allow all Answers users access to the information panel content.

:::image type="content" source="../media/engage/admin/ans-info-pan-admin2.png" lightbox="../media/engage/admin/ans-info-pan-admin2.png" alt-text="Screenshot of the info panel editing options.":::

### Reset the information panel  

1. Select the edit icon from the top left corner of the information panel.
1. Select **Reset** from the bottom-left corner.  

:::image type="content" source="../media/engage/admin/ans-info-pan-admin3.png" lightbox="../media/engage/admin/ans-info-pan-admin3.png" alt-text="Screenshot showing the info panel reset option.":::

## Manage topics in Answers

Use topics to organize and curate Engage knowledge. Answers topics also help you stay on top of new questions about topics you follow or subscribe to. [Learn more about using topics in Viva Engage](https://support.microsoft.com/office/use-topics-and-hashtags-in-viva-engage-98c0a0bb-aad0-45d3-88f1-4f6d12bb1772). 

>[!NOTE]
>Viva Topics will be retired in 2025. As part of that change, Viva Engage returns to a simplified topics experience and won't use Viva Topics or Lightweight Topics. During this transition, topics in Engage will be migrated to see the latest topics experience with the enablement of Answers and deletion of topics. Migrations are planned to complete in Spring 2025. Learn more about [Setting up Answers](/Viva/engage/eac-answers-overview-set-up#technical-requirements), and the [Viva Topics retirement](/microsoft-365/topics/changes-coming-to-topics?view=o365-worldwide&amp&preserve-view=true;WT.mc_id=M365-MVP-9501). 

## Bulk Remove topics

To remove a topic or multiple topics at once, applicable admins can:

1. Go to the Discover more topics page in Answers. 
2. Search by topic name, or filter by "All" to browse topics.  
3. Select the ellipsis icon on a topic to show edit and remove topics. 
4. Use the check box to select multiple topics to delete. 
5. When you remove the topic, the topic and all applications of the topic are removed. This action can't be undone.

## View Global Answers analytics

As an Answers admin, you can access Global Answers analytics:
1. Select the analytics icon from the top navigation bar of Viva Engage.
1. Go to the **Global Answers analytics** tab. The analytics dashboard provides an overview and relevant insights about knowledge sharing activity across Answers in Viva.

For more information about how to manage analytics in the [Viva Engage admin center](/Viva/engage/eac-overview), see [View and manage analytics in Viva Engage](/Viva/engage/analytics).

:::image type="content" alt-text="Screenshot of the Global Answers analytics dashboard in Viva Engage." source="/viva/media/engage/admin/global-answers-analytics.png" lightbox="/viva/media/engage/admin/global-answers-analytics.png":::

The following metrics are available for Global Answers analytics:

| Metric | Description |
|---|---------|
|**Total time saved for your organization**|Time the organization has saved based on question-and-answer usage|
|**Total questions**|Number of questions asked by users|
|**Question views**| Views across all questions|
|**Total answers**| Number of answers provided by users|
|**Total best answers**|Answers marked as best answer|
|**Answer rate**|The ratio of questions that have answers to total questions|
|**Best answer rate**| The ratio of questions with best answers to total questions|
|**Median time to first answer**|The median time it takes for a question to receive its first answer|
|**Median time to best answer**|The median time it takes for a question to receive its first best answer|
|**Median questions asked per user**|The median number of questions asked by each user|
|**Median questions viewed per user**| The median number of questions viewed by each user|
|**Median answers per user**| The median number of answers provided by each user|
|**Median best answers per user**| The median number of best answers provided by each user|
|**Top questions across your organization**|A table of the top questions with the most views, votes, reactions, and answers across your org|
|**User engagement distribution**|A distribution of all users split by active engagements (ask, answer, vote, reactions, comments) and passive engagements (question views)|
|**Global time saved** |Time saved across the organization. Based on Viva Engage research, this total shows that each question-and-answer pair saves people an average of 15 minutes. As more people discover existing answers to their questions, the organization saves more time.|

>[!NOTE]
> Analytics aren't live. They're updated every 24 hours.

## See also

[Answers in Viva: Frequently asked questions (FAQ)](/Viva/engage/eac-answers-faq)

[Key admin roles and permissions in Viva Engage](/Viva/engage/eac-key-admin-roles-permissions)

[View and manage analytics in Viva Engage](/Viva/engage/analytics)
