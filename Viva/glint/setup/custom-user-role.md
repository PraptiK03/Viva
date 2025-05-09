---
title: User Roles with custom data access in Viva Glint
description: Microsoft Viva Glint custom access can override default access and meet access needs that specific enough to be tied to a user rather the User Role.
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: custom access,custom focus area access, custom admin access, custom direct report access, access to one or multiple populations 
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: install-set-up-deploy
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 04/14/2025
---

# User Roles with custom data access in Viva Glint

Microsoft Viva Glint custom access can override default access and meet access needs that specific enough to be tied to a user rather the User Role. For example, use custom access for HR Business Partners who serve unique combinations of employee groups in your organization.

## Grant custom survey access for a user

1. Select **Configuration** and then **People**.
2. Go to the User Role that needs custom access granted.
3. Search for or select a user.
4. On the user's profile, next to the survey name who needs access, select the **pencil** symbol to edit.

   > [!NOTE]
   > The person needs to be granted access to a survey program in a survey's Reporting section in order for it to appear on their user profile.

   :::image type="content" source="../../media/glint/setup/custom-access-dialog.png" alt-text="Screenshot of dialog that appears to let an admin edit a user's custom access.":::
    
5. Select **+ Population** and then **+ Add Filters**.
6. Select attributes and values that define the segment of employee data that this user should access and select **Done**.

   :::image type="content" source="../../media/glint/setup/custom-access-selection.png" alt-text="Screenshot of dialog with custom access attribute values selected.":::
   
7. Select **Save** to apply custom access for this user and survey program.

### Custom access to direct reports

For direct reports to have custom access, they need to identify them by "manager ID" and not "manager hierarchy." Using "manager hierarchy" can grant access to unintended users and block reporting access from intended users.

### Custom Admin and Focus Area access

> [!IMPORTANT]
> Users with customized Admin access can only see employee data for populations of users that they have access to. <br><br>
> For example, if a user has custom Admin access to Department = 'Sales' and 'Marketing,' they don't see Distribution Lists or users in People that have other Department values.

Users can have Focus Areas and admin access customized.

1. Select **Configuration** and then **People**.
3. Search for or select a user.
4. On the user's profile, next to *Admin Access* or *Focus Area Access*, select the **pencil** icon to edit.
5. Select attributes and values that define the segment of employee data that this user should have access to and select **Done**.

   :::image type="content" source="../../media/glint/setup/custom-focus-area-selection.png" alt-text="Screenshot of dialog with custom focus area access attribute values to be selected.":::

6. Select **Save**.

To grant custom access in bulk to multiple users for survey, Focus Area, and Admin access, see: [Advanced Configuration uploads](advanced-config-uploads.md#perform-a-managers_upload).

### Access to one or multiple populations

For survey, Focus Area, and Admin access, you can grant access to one or multiple populations, depending on how a user should see data in their reports. 
 - To give a user access to the overlap of different employee groups, add all attribute selections to one population.
 - To give a user access to multiple populations separately, add them as separate populations.

#### Example: 
For this manager to have access to the overlapping data between Cost Centers: 10010, 10414, 11140 and Departments: Support, Sales, and Marketing, select all values in one population:

:::image type="content" source="../../media/glint/setup/select-one-population.png" alt-text="Screenshot of dialog with cost center and department values selected in one population.":::

This access appears on their user profile as one population with values from both attributes:

:::image type="content" source="../../media/glint/setup/user-access-one-population.png" alt-text="Screenshot of user access with cost center and department values selected in one population.":::

But, to grant this user access to these employee groups *separately* -so they don't have access to only the overlap of these populations - add the attribute values selections in separate populations:

:::image type="content" source="../../media/glint/setup/select-two-populations.png" alt-text="Screenshot of dialog with cost center and department values selected in separate populations.":::

This access appears on their user profile as two populations, with values from each attribute:

:::image type="content" source="../../media/glint/setup/user-access-two-populations.png" alt-text="Screenshot of user access with cost center and department values selected in separate populations.":::



