---
title: Duplicate or delete surveys in Viva Glint
description: As your company’s data controllers, Microsoft Viva Glint Administrators can duplicate or delete surveys.  
ms.author: Judithweiner
author: JudyWeiner
manager: mbarry
audience: admin
f1.keywords: NOCSH
keywords: delete survey, duplicate survey, copy survey, remove survey, delete data
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: how-to
ms.service: viva-glint 
ms.localizationpriority: high 
ms.date: 03/04/2025
---

# Duplicate or delete surveys in Viva Glint

As your company’s data controllers, Microsoft Viva Glint Administrators can duplicate or delete surveys.

> [!NOTE]
> Viva Glint admins must have [Advanced Configuration access enabled](understand-advanced-configuration.md#grant-access-to-an-existing-admin-user) to delete survey data.

## Duplicate a survey

Survey duplication copies all survey settings and translations from the selected survey program. To duplicate a survey in Viva Glint, follow this process:

1.  Select **Survey Programs** from your admin **Configuration** page. 
1.  Use the search box or go to the **Survey Programs** list to identify the survey to duplicate.
1.  Use the three dots to display the dropdown menu. Choose **Duplicate**.
1.  You're directed to the **Program Summary** for the copied survey program, which is automatically named **[Survey Name] Copy**.

## Delete survey data

Survey deletion is available for all nonactive surveys. This feature deletes every data entity directly related to the survey, including overall survey configuration, items/questions, reports, responses, etc. The action doesn't delete distribution lists or any roles related to the survey. 

> [!IMPORTANT]
> Viva Glint admins must have [Advanced Configuration access enabled](understand-advanced-configuration.md#grant-access-to-an-existing-admin-user) to delete survey data.

> [!CAUTION]
> Survey data deletion in Viva Glint is an irreversible process. Perform this action only when confident that the data of the survey is not required anymore. 

To delete survey data from Viva Glint, follow this process:

2.  Select **Survey Programs** from your admin **Configuration** page. 
1.  Use the search box or navigate to the **Survey Programs** list to identify the survey that data should be deleted from. 
1.  Select the three dots to reveal the dropdown menu. Choose **Delete**.
1.  A **Survey Delete** confirmation box asks for confirmation and displays the following message: **This will permanently delete all data associated with this program.** If you aren't sure that should happen, select **No, I am not sure**, otherwise **Confirm the action**. 
1.  Once the delete action is completed, return to the **Survey page** to verify that the survey doesn't appear in the **Survey Programs list**.

> [!NOTE]
> If a survey is listed in the Disabled status section in Survey Programs, enable the survey before deleting it. To enable, hover over the right of the survey, select the ellipsis, and choose "Enable."
