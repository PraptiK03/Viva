---
title: Set up and manage Viva Glint Distribution Lists
description: Distribution lists are how admins define which employees within an organization should receive a survey or permissions to view results.
ms.author: JudithWeiner
author: JudyWeiner
manager: mbarry
audience: admin
f1.keywords: NOCSH
keywords: distribution lists, attribute rules, delete distribution lists, exclude distribution lists
ms.collection:  
- m365initiative-viva
- selfserve 
search.appverid: MET150 
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 03/11/2025
---

# Set up and manage Viva Glint Distribution Lists

Microsoft Viva Glint Distribution Lists define which employees in your organization are eligible for a survey. Refine lists using employee attributes uploaded to Viva Glint, upload a file of users, use date-based lists, and edit or delete lists over time.

> [!NOTE]
> To set up Distribution Lists, complete [attribute setup](/../../viva/glint/setup/send-employee-attributes) and [upload data to the Viva Glint system.](/../../viva/glint/setup/upload-employee-attributes)

## Set up a Distribution List 

To set up a new Distribution List:

1. Select **Configuration** and in the **Employees** section select **Distribution Lists**. The Distribution List page displays all existing lists and their number of members.

   :::image type="content" source="../../media/glint/setup/distro-list-overview.png" alt-text="Screenshot of the Distribution List window.":::

1. Select **+ New Distribution List**. 

   :::image type="content" source="../../media/glint/setup/distro-list-add-new.png" alt-text="Screenshot of Distribution List setup steps.":::
   
1. To replace the "Untitled Distribution List...," add a unique name to the list default name. If another list already uses that name, an error message appears.

## Add users to a Distribution List

There are multiple ways for Viva Glint Admins to add users to a list, including:

- [Attribute rules](#use-attribute-rules-to-add-users) that automatically add users based on employee data imported to Viva Glint
- [Search and select](#search-for-and-add-individual-users) individual users
- [File imports](#import-users) to add multiple users that don't share an attribute value
- [A blended approach](#use-a-blended-approach-to-add-users) that combines attribute rules and the search + add feature

### Use attribute rules to add users

To automatically add users to a list based on their attribute values in data imported to Viva Glint:

1. Select **Configuration** and in the **Employees** section, select **Distribution Lists**.
2. Select the list that should have an attribute rule added.
3. Select **Add/Edit Employees** and in the **Choose a way to add employees** dialog, select **Attribute Rules.**
4. In the **Add Attribute Rules** edit pane that appears:
   1. Select **I want to filter all active employees by these populations:** to include active users only.
   2. Select **+ New Population** and then **+ Add Filters**.
   3. Choose attributes and values to include employees who match this data in your imported employee files.
      
      > [!TIP]  
      > For an Exit survey, enable **Include Inactive Employees** and consider contacting them via their [personal email](attribute-fundamentals.md#optional-system-attributes).
  
   5. To exclude users, hover over their name in the **Included** section and select **Exclude**.
   6. To remove someone from the **Excluded** list, hover over their name in the **Excluded** section and select **Remove**.
4. Confirm your list and select **Save Changes**.

### Add users manually

Add individual users with the **+ Search for an employee to add** feature or import a file of users to update a list in bulk.

#### Search for and add individual users

To manually add individual users:

1. Select **Configuration** and then choose **Distribution Lists**.
2. Select the Distribution List that you need to add employees to.
3. Enter a name or email address in the **+ Search for an employee to add** field at the bottom of the list.
4. Select the user from search results to add them to the list.

#### Import users

> [!CAUTION]
> Importing users to an attribute rule-base list removes attribute rules from the list.

To import a file of users to a list:

1. From the admin dashboard, select **Configuration** and then choose **Distribution Lists**.
2. Select the Distribution List that you need to add employees to.
3. Select **Add/Edit Employees**.
4. From the **Choose a way to add employees** dialog, select **Import**.
   
   :::image type="content" source="../../media/glint/setup/dl-choose-add-method.png" alt-text="Screenshot of the choose a way to import employees dialog for distribution lists.":::
   
5. In the **Import employees to distribution list** dialog, select **Download CSV** in the **Download your current employee list to modify** section. 
6. Use the downloaded file as a template and add employee email addresses in the email column. Include the header row, which is labeled differently when there are or aren't users in the list. Both column labels import successfully:
   1. The header row label in the template file is **email** when there are already users in the **Distribution List**.
   2. The header row label in the template file is **Employee Email** when there are no users in the **Distribution List**.
7. After adding all email address values, save the file as .csv or .xlsx.
8. In the **Import employees to distribution list** dialog, drag and drop or browse to choose the file (maximum size 550 MB, maximum row count 10,000).
9. To keep any existing users in the list, select **Preserve the employees already in the distribution list**.
    
    :::image type="content" source="../../media/glint/setup/dl-import-preserve.png" alt-text="Screenshot of distribution list import dialog with the preserve employees in the list option selected.":::
   
10. Select **Import File**.
11. The **Confirm your import** window displays. If the correct number of employees to be added and removed are correct, select **Confirm Import**.

#### Export users

1. From the admin dashboard, select **Configuration** and then choose **Distribution Lists**.
2. Select the Distribution List that you need to add employees to.
3. Select **Add/Edit Employees**.
4. From the **Choose a way to add employees** dialog, select **Import**.
   
   :::image type="content" source="../../media/glint/setup/dl-choose-add-method.png" alt-text="Screenshot of the choose a way to import employees dialog for distribution lists.":::
   
5. In the **Import employees to distribution list** dialog, select **Download CSV** in the **Download your current employee list to modify** section.

### Use a blended approach to add users

If your organization needs to add most users to a list based on attribute rules, but also needs to add a few users manually, consider a blended approach.

1. Set up a new list and add an [attribute rule](#use-attribute-rules-to-add-users) for it.
2. When users need to be added manually, add them with the **[Search and add user](#search-for-and-add-individual-users)** feature in the list.
3. The **Membership Type** in **Distribution Lists** shows as "Attribute Rules, Manual."

> [!CAUTION]
> Importing users to an attribute rule-base list removes attribute rules from the list. Use only the Search and add feature to manually add users to a list that uses a blended membership method.

## Use date-based lists

Viva Glint Employee Lifecycle surveys use exit and hire dates in your employee data to automatically trigger Exit and Onboarding surveys. Use date-based distribution lists to include all eligible users based on ranges of dates tied to exit and hire date information.

To set up a date-based list:

1. [Set up a list](#set-up-a-distribution-list)
2. [Use attribute rules to add users](#use-attribute-rules-to-add-users)
3. Select a date attribute, usually exit or hire date
4. Select a day range related to the date that employees are eligible.
5. When selecting a number of days before and after a date, consider:
   - How often your organization uploads employee data
   - How quickly new and termed employee data is updated in your HR information system
   - The Response Window in a survey's Program Setup (the number of days a user has to complete a survey, usually 14 days)

For example, to ensure that users have enough time to respond to a 30-day onboarding survey, a Viva Glint Admin can choose to make users eligible 30 days to 50 days after their hire date. This setup allows users to receive invites and respond with enough time based on this organization's bi-monthly import of employee data. 

:::image type="content" source="../../media/glint/setup/dl-day-range-onboard.png" alt-text="Screenshot of a Viva Glint date-based distribution list for a a 30-day onboarding survey.":::

## View how a list is populated

On the **Distribution Lists** page, the **Membership Type** column defines if that list is populated manually, by attribute rules, or both. 

- **Attribute Rules**: The list uses attribute rules to add users based on their attribute values in imported employee data
- **Manual**: The list uses a file of users imported to the list or the **Search and add user** feature to add new users
- **Attribute Rules, Manual**: The list uses attribute rules and the **Search and add user** feature to add users.
  
## Edit a list

Editing a Distribution List is a global change and affects any program using that list. To modify: 

1. Select the Distribution List you want to modify. 
1. Select  **Add/Edit Employees**  or  **Edit Attribute Rules** if there are filters available. 
1. Make the necessary changes and select **Save Changes**. 

## Delete a list

Viva Glint Admins can delete lists by hovering over the list and selecting the **Delete** option. A **Delete Distribution List** dialog opens with a list of survey programs that use the list. 

:::image type="content" source="../../media/glint/setup/delete-distribution-list.png" alt-text="Screenshot of Delete Distribution List slider window.":::

To delete the Distribution List, remove it from the Distribution section of the program.

1. Select **Configuration** and then select **Survey Programs**.
2. **Select the survey.**
3. Select **Distribution** and remove the list.
4. Repeat this process for all survey programs that use the list.
5. Return to **Distribution Lists** and select the **Delete** option for the list.
6. In the **Are you sure?** dialog that appears, select **Yes, I'm sure.**

:::image type="content" source="../../media/glint/setup/confirm-delete-distro-list.png" alt-text="Screenshot of Are you sure window to confirm deletion of a Distribution List.":::

> [!NOTE]
> Deleting a Distribution List is a permanent action. The data of the members of that list isn't deleted.

