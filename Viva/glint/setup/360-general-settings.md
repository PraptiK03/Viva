---
title: Microsoft Viva Glint 360 feedback program General Settings and User Roles setup
description: 360 feedback setup begins in the General Settings section of the admin dashboard. By default, Viva Glint admins have access to create and edit all Viva Glint programs, including 360s. A best practice, however, choose to create a unique User Role with exclusive 360 admin permissions. 
ms.author: JudithWeiner
author: JudyWeiner
manager: mbarry
audience: admin
f1.keywords: NOCSH
keywords: localization, supported languages, dashboard languages, unique 360 admin role, 360 user role permissions, granting 360 permissions
ms.collection:  
- m365initiative-viva
- selfserve 
search.appverid: MET150 
ms.topic: install-set-up-deploy
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 3/05/2025
---

# Microsoft Viva Glint 360 feedback program General Settings and User Roles setup

360 feedback setup begins in the General Settings section of the admin dashboard. By default, Viva Glint admins have access to create and edit all Viva Glint programs, including 360s. A best practice, however, choose to create a unique User Role with exclusive 360 admin permissions. And, in addition to any unique 360 admin role, other people in your organization need access to 360 feedback. Use this guidance to grant feedback permissions for other User Roles.

## Configure General Settings 
1. From the Viva Glint admin dashboard, select the **Configuration** symbol and then **General Settings**. 
1. Review selections that apply to all your Glint programs and confirm that 360 items are set up. 
1. [View, edit, or update the information](manage-general-settings.md).

   Focus on these items:

   |Section|Item to set up|Description|
   |-------|---------|---------|
   |**Company information**|**Top-level Manager (CEO**)|Confirm that the top-level Manager/CEO for your organization is selected. Manager Hierarchy is a critical piece of information used in 360s to determine feedback provider category assignments and 360 report access.|
   |**Engage Survey Details**| **Require Azure AD for links in survey emails** | Viva Glint Admins, 360 Admins, and 360 subjects must exist in and authenticate with Microsoft Entra ID to access 360 feedback items. Feedback providers have two access options based on the this access setting. Confirm whether this functionality is set to: <br><br> <ul><li>**Yes** to require all users to authenticate with Microsoft Entra ID, or </li> <li>**No** to allow feedback providers to give feedback without authenticating with Microsoft Entra ID</li></ul> <br> **Note:** This setting applies to all surveys and not just 360 feedback programs. [Learn more about survey access methods](understand-survey-access-methods.md)
   |**Features**|**Community Enabled**|Define if access to Viva Glint’s community is allowed |
   |**Features**|**Default Focus Area Privacy**|Set privacy level for users to search for, view, and comment on other users’ focus areas:<br><br><ul><li> **Publicly Visible** - Everyone in the organization </li><li> **Visible to Manager** - The user’s manager, up-level managers, or anyone configured with custom focus area access </li><li> **Visible to Manager and Directs** - The user’s manager, up-level managers, direct reports, or anyone configured with custom focus area access </li><li> **Visible to Manager and Full Team** - The user’s manager, up-level managers, everyone who reports up to the user, or anyone with custom focus area access to the manager </li></ul>|
   |**Localization**|**Supported Survey Languages**|Determines which survey languages are available for users to select in a 360 feedback program.|
   |**Localization**|**Supported Dashboard Languages**|Determines which dashboard languages are available to select in a 360 feedback program|

## Create a unique 360 admin role

> [!IMPORTANT]
> You can have more than one Viva Glint 360 admin, but the best practice is to limit your total number of unique 360 admins to just a few.

From the Viva Glint admin dashboard, select the **Configuration** symbol and then **User Roles** in the **Employees** section. 

1.	Select **+ New Role**.
1.	On the **Untitled Role** page that opens, name the User Role by selecting the **pencil symbol**. Choose a name easily identifiable for that role name. In this example, the role of "360 Admin" is being created.

    :::image type="content" source="../../media/glint/setup/360-unique-manager-role-2.png" alt-text="Screenshot of naming a unique 360 admin User Role.":::
   
1. Select **Permissions** and scroll down to the **Feedback** section of the page.
1. Enable **Access 360 feedback**.
1. Select **Manage Feedback** to enable users to modify existing 360 feedback programs.
1. Select **Create 360s** to enable users to create and modify 360 programs.
1. Select **Save Changes**.
1. In the **Confirm your changes to Permissions** dialog box which opens, select **Save Permissions**.

   :::image type="content" source="../../media/glint/setup/confirm-permissions.png" lightbox="../../media/glint/setup/confirm-permissions.png" alt-text="Screenshot of the Confirm your changes to Permissions dialog box.":::

## Grant program privileges

Your program configuration specifies which user groups have privileges. Use this procedure to grant user groups permissions to view 360s:

1. From the admin dashboard, select the **Configuration symbol** and then **360 Feedback Programs.**
1. Select the program to be edited.
1. From the Actions dropdown menu, select **Add/Edit Admin Access**. 
1. Use the Search box to see the available User Roles and select the one you want. The dropdown list under the Search box shows the User Roles that have Manage Feedback permission. In this case, select the user role name for each group you want to give privileges to.
1. To remove program privileges from a user role, hover over the User Role and select X.
1. The User Role name is added to the dropdown list. This role doesn't have permission for any program that is already live.
1. Select **Save Changes.**
    
## Assign 360 permission to all 360 participants

You must assign the Access 360 Feedback permission to all subjects, coaches, and raters so they can participate in 360 feedback cycles.
To assign permissions:
1. From the admin dashboard, select the **Configuration symbol"and then **User Roles**.
3. Select the User Role.
4. Select **Permissions.**
5. Select **Access 360 Feedback.**
6. Select **Save Changes.**

## Add members to a 360 User Role

To manually add a person to a new role, scroll down to the Search bar in the **All Members** section. Begin to type the name of the person you're searching for and then select it. Now you see your unique 360 User Role in **All Members**.

:::image type="content" source="../../media/glint/setup/all-members.png" alt-text="Screenshot of an employee name added to the All Members role list.":::
 
For more information on adding User Roles, [see this guidance](/../../viva/glint/setup/set-up-user-roles).

## Give subjects and feedback providers access to the feedback tab

Subjects and feedback provider participating in 360s need access to the **Feedback tab** on their Glint dashboard. It’s optional to grant feedback providers access to the Feedback tab. Access enables users to log in and view any open or historical requests to provide feedback to a 360 subject.

Subject use of the feedback tab includes the ability to:
- See all active feedback requests 
- Add or edit feedback providers 
- Complete their self-assessment 
- View who responded to their 360 cycle, if the admin provided this permission
- Review all completed feedback history

### Procedure to enable feedback tab access: 

1. From the **Configuration** page of your admin dashboard, select **User Roles** in the **Employees** section.
1. To grant permissions, select the name of the **User Role**. This role can be a previously created or newly created role just for 360s.
1. Choose **Permissions**.
1. **Access 360 Feedback** must be checked in addition to whatever other permissions the role is granted.




