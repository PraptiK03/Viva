---
title: Custom data access in Viva Glint
description: Microsoft Viva Glint offers custom data access for users who support unique groups of employees in your organization.
ms.author: aweixelman
author: AliciaWeixelman
manager: melissabarry
audience: admin
f1.keywords: NOCSH
keywords: custom survey access, custom access, custom data access export, user access, data access export
ms.collection:  
- m365initiative-viva
- selfserve 
search.appverid: MET150 
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 02/13/2025
---

# Custom data access in Viva Glint

Microsoft Viva Glint offers custom data access for users who support unique groups of employees in your organization. Users may need to have their default team access modified or are in a role so specific, access needs to be set at the user level. Use the guidance in this article to export, modify, and import custom data access. To make individual updates to users' custom data access, see: [Custom User Role setup in Viva Glint](custom-user-role.md).

## Export custom access

Use the custom access export as a Viva Glint Admin to audit users' data access.

1. From the Glint Admin dashboard, select the **Configuration** symbol and then in **Employees** choose **User Roles**.
2. In the top right corner of the **User Roles** page, select **Export**.
3. In **Export data** dialog that appears, make selections in the following fields.
   1. **Programs:** Select one survey program or choose **Select All**.
   2. **Roles:** Select one User Role or choose **Select All**.
   3. **Focus Areas:** Enable this setting to include Focus Area access only. Disable to include survey results access only.
   4. **Include Empty Data**: Enable this setting to include users with no data access.
   5. **Include Inactive Data**: Enable this setting to include active **and inactive users**.
  
      :::image type="content" source="../../media/glint/setup/export-access-dialog.png" alt-text="Screenshot of the Export data dialog with program, role, and data selections.":::  
      
6. Select **Export** after making selections.
7. A new dialog appears prompting you to **rename and save** the data to your device. By default, custom access files export to a compressed folder named: **Untitled.zip**.

## Custom access file

The custom data access export includes the following information:

|Column  |Description   |
|:----------|:-----------|
|user email     | Populated with users' email addresses.       |
|population     | The first population shows as 1. Each new population increases in number for each user. |
|access type   | <ul><li>The survey uuid of the program that users have customized access for, or</li> <li>"GOAL" when exporting Focus Area access for users.</li> </ul>      |
|other attributes    | Other columns in the export are based on your organization's attributes and values that are used to grant custom access. |

### Edit the access file

To prepare your exported custom access file for import to Advanced Configuration:

1. To retain leading zeros and data formats, use the [Text Import Wizard](https://support.microsoft.com/office/text-import-wizard-c5b02af6-fda1-4440-899f-f78bafe41857) to open files with a .csv extension.
2. Update the column labels in the exported file to the following columns:

   |Column  |Change to...   |
   |:----------|:-----------|
   |user email     | manager reference   |
   |population     | `no change to column label` |
   |add or remove     | `insert this as a new column` populate with "ADD" or "REMOVE" |
   |access type   | survey uuid values or "GOAL" already included in export, depending on Focus Areas selection |
   |other attributes    | `no change` To grant new access, add new columns and values based on employee data imported to Glint. |

   > [!NOTE]
   > To prevent upload errors, for attributes based on data uploaded to Glint make sure that column labels match your attribute setup exactly.
   
   > [!TIP]
   > To confirm which survey program a survey uuid is connected to, go to **Configuration** and select **Survey Programs**. Choose a survey and note the ID at the end of the URL in your web browser. This value is the survey uuid that appears in the **access type** column in the custom access export.
 
3. Edit values in the population column. The first population that a user has access to should be changed from a 1 to a 0, with each new population increasing in number.
   
   |Population value |Becomes...   |
   |:----------|:-----------|
   |1    | 0 |
   |2    | 1 |
   |3    | 2 |
   
5. To grant custom access for:
   - **Survey results**:
      - Populate the survey uuid column with the survey program's unique ID included in the access export file.
      - **To update a user's data access for all surveys that they have access to, leave the survey uuid column blank**.
   - **Focus Areas**:
      - Populate the survey uuid column with "GOAL".
   - **Admin permissions**:
      - Populate the survey uuid column with "ADMIN".
6. To grant custom access to manager or nonmanager hierarchy data, use this table as a guide.

   |Access  |Attributes to include in file  | Attribute values to include in file  |
   |:----------|:-----------|:------------|
   |Another active manager's team    | Manager Level 1       | Employee ID of the manager that another user should have access to |
   |Another inactive manager's team     | Fields for all manager levels in the inactive manager hierarchy <br><br>[Export users from the survey cycle](/viva/glint/setup/glint-data-apps#export_users_from_survey_cycle) to get all levels  | Employee IDs of the managers in all levels <br><br>[Export users from the survey cycle](/viva/glint/setup/glint-data-apps#export_users_from_survey_cycle) to get all IDs  |
   |A manager's direct reports only  | Manager ID field, with the label from your attribute setup <br> <br>Go to **People** and select **Manage User Attributes** in the **Actions** menu to view attribute labels.    | Manager IDs of each direct report, in separate rows |
   |A level in a nonmanager hierarchy    | Fields for all levels above and including the level the user should access    | Values for each level in each field |

7. Save your file in .csv format with a comma separator and UTF-8 encoding (Viva Glint accepts UTF-8 and UTF-8 with BOM encoding).

### Example

An HR business partner, user@contoso.com, oversees European Sales and Marketing teams for Contoso. To grant this user access to the right cut of data to view survey results, a Viva Glint Admin would fill in an access file with their location attribute Region = Europe and their hierarchy Team Level 1 = Marketing and Sales.

:::image type="content" source="../../media/glint/setup/custom-access-export-survey3.png" alt-text="Screenshot of a custom access export for a user with customized survey results access.":::

To apply the same custom access for creating Focus Areas, update the access type column for this user to "GOAL."

:::image type="content" source="../../media/glint/setup/custom-access-export-focus-area3.png" alt-text="Screenshot of a custom access export for a user with customized focus area access.":::

> [!IMPORTANT]
> Save your edited file as **.csv with a comma separator and UTF-8 or UTF-8 with BOM encoding**.

## Upload custom access in Advanced Configuration

After exporting and preparing a file, go to **Advanced Configuration** to upload users' custom data access.

1. From the Glint Admin dashboard, select the **Configuration** symbol and then in **Service Configuration**, choose **Advanced Configuration**.
2. In the **Advanced Configuration** menu, select **Uploads**.
3. In the **Upload type** dropdown menu, select **MANAGERS_UPLOAD**.
4. **Apply to**: Ignore, this setting is for retroactive uploads only.
5. **Incremental**:
   1. Enable this setting to append access to users in your file.
   2. Disable this setting to overwrite all access for users in your file. Users not included in the file aren't impacted.
6. **Use exact case from the file for First/Last name**: Ignore, this setting doesn't apply to access uploads.

   :::image type="content" source="../../media/glint/setup/adv-config-uploads.png" alt-text="Screenshot of the Advanced Configuration Uploads feature.":::

7. Drag and drop your .csv file or browse to choose it in the **Drag and drop to upload** section.
8. In the **Upload Job Details** page that appears, confirm that the **Uploaded Lines Summary** matches the changes in your file.
9. Select **Apply Upload to Database** to upload new values.
10. In the **Load import file into database?** dialog, select **Yes**.
11. Go to some users' profiles to confirm that customized access appears as expected.
   1. Select the **Configuration** symbol, then in **Employees**, choose **People**.
   2. Search for and select users to spot check.
