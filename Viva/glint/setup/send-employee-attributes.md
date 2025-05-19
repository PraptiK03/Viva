---
title: Set up attributes in Viva Glint
description: Set up attributes in Microsoft Viva Glint to create a mapping of fields to expect in your employee data files transmitted to Viva Glint.
ms.author: aweixelman
author: AliciaWeixelman
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: Attribute setup, edit attribute, data import, derived attribute, data import
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: install-set-up-deploy
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 05/19/2025
---

# Set up attributes in Viva Glint

Set up attributes in Microsoft Viva Glint to create a mapping of fields to expect in your employee data files transmitted to Viva Glint. To set up required, custom, hierarchy, and derived attributes, use the decisions made in the [Employee attribute template](create-employee-attribute-template.md) as a guide.

> [!NOTE]
> Before starting, confirm that the attribute selections in your Employee attribute template are **final**. Viva Glint Admins can't edit, file format, date attribute formats, or add new hierarchies/hierarchy levels after initial setup is complete. 

## Attribute setup in Viva Glint

To set up attributes Viva Glint, your uploaded file must contain a finalized attribute header row and at least one row of employee data. Use the in-platform, four-step attribute setup process to create a mapping to import employee data.

> [!CAUTION]
> The Viva Glint Admin who sets up or changes attributes needs to save changes in the **default language for your organization**. Confirm that the default language (often English) is selected in the **Language** dropdown menu in Viva Glint. Setting up or editing attributes in a different language resets the expected language for Viva Glint data ingestion and causes upload errors.

Learn more about how to set up attributes in Viva Glint with this video and the following instructions:  

> [!VIDEO bb2646bc-ce4a-407d-8400-ec43bc5514de]

## 1. Upload dataset

1. From the admin dashboard, select **Configuration**.
2. In **Employees,** select **People**.
3. Choose **Get Started** and select **New User Schema or Attribute Updates** to begin the four-step setup process.

   :::image type="content" source="../../media/glint/setup/import-choice.png" alt-text="Screenshot of the import option selection screen, including the New User Schema or Attribute Updates option.":::

4. Upload finalized attributes in your selected format. This file format determines the format for all future uploads. Select **Continue.**
  
   :::image type="content" source="../../media/glint/setup/setup-step1.png" alt-text="Screenshot of step 1 to upload your attributes in a finalized file layout.":::

## 2. Preview employee data fields

Check that the attribute names and values appear as expected.

:::image type="content" source="../../media/glint/setup/setup-step2.png" alt-text="Screenshot of step 2 to preview uploaded attributes.":::

1. Verify that:
     - All attributes are present in the preview.
     - Attribute values shown for preview data display in the correct column.
     - The total count of "data fields found" displayed above the preview matches the number of attributes in the file.
2. If dates are included in your file, select the **There are date fields** checkbox and then choose your **date format** from the dropdown menu.

     > [!CAUTION]
     > - All attributes that include dates must follow the same format.
     > - Viva Glint transforms incoming dates to Viva Glint's preferred format, yyyy/mm/dd, upon upload.
     > - Complete date selection in this step and Derived attribute setup in the next step to import dates in a format that's usable for Distribution lists and survey triggers. 

3. After finished previewing, select **Continue**.

## 3. Set up attributes

Map your uploaded and confirmed attributes to Viva Glint fields. This setup is divided into three sections:

### Required attributes

Select your attribute from the dropdown for each required attribute:

- First Name
- Last Name
- Email
- Employee ID
- Status

:::image type="content" source="../../media/glint/setup/setup-step3-required.png" alt-text="Screenshot of step 3 to map required attributes.":::

### Derived attributes

Viva Glint calculates attributes based on data sent in your employee attribute file. Decide whether to include tenure groups based on hire date or age groups based on birth year.

|Derived Field   |Based On   |Derived Values|
|----------|-----------|------------|
|Tenure* |Hire Date   |<1 Year, 1-2 Years, 2-4 Years, 4-6 Years, 6-10 Years, 10-15 Years, 15-20 Years, 20+ Years|
|Age Grouping     |Birth Year       |<25, 25-29, 30-34, 35-39, 40-44, 45-49, 50-54, 55-59, 60-64, 65-69, 70+       |

\* Tenure values for new Viva Glint customers after January 13, 2024. Before this date: 0-1 Year, 1-2 Years, 2-3 Years, 3-4 Years, 4-5 Years, 5-7 Years, 7+ Years.

> [!IMPORTANT]
> - To avoid duplicated attribute errors, don’t include derived attributes like Tenure in your employee data file. Viva Glint creates these fields.
> - Age Grouping derivations can be based on Birth Year, but not full Birth Date. Include **Birth Year** in your employee data to create Age Grouping.

1. Select the section with the desired attribute.
2. Select the desired attribute from the dropdown menu.
3. Select **Continue**.

:::image type="content" source="../../media/glint/setup/new-derived-attribute2.png" alt-text="Screenshot of step 3 to map derived attributes.":::

### Optional System Attributes

Map attributes in your employee data to Viva Glint language, time zone, and personal email fields to indicate how and when to communicate with employees. Choose to enable any of the following fields by selecting the checkbox and choosing a field from your file in the **Sync From** dropdown menu:

|Viva Glint Field   |Description  |
|----------|-----------|
|Survey Language     |The language for employee surveys and emails.    |
|Dashboard Language|The language for user dashboards.  |
|User Timezone|The time zone in which survey communications are sent.  |
|Personal Email|Users' personal email addresses that can be used to survey exiting employees. Select Company and Personal Email in the Communications section of your survey program.  |

:::image type="content" source="../../media/glint/setup/setup-step3-optional.png" alt-text="Screenshot of step 3 to map optional system attributes.":::

> [!IMPORTANT]
> Send language and time zone values exactly as they appear in related tabs in the following articles:
> - [Viva Glint supported languages](supported-languages.md)
> - [Viva Glint supported time zones](supported-time-zones.md)
> 
> Users with blank or invalid values receive and access surveys/emails/dashboards in your organization's default selection in General Settings.
>
> See [Recent language changes](attribute-fundamentals.md#recent-language-changes) for changes to supported languages and codes effective April 10, 2025.

### Hierarchy groups

Select your attributes from the dropdown menu for each hierarchy group.

- To have Viva Glint create a Manager Hierarchy, map your manager ID field from your employee data to Manager ID.
- To add more levels to a hierarchy, select **+ Add Level**.
- To add a new hierarchy group, select **+ Add Hierarchy Group**.
- To rename the hierarchy label, select the **pencil** symbol.
- To delete a group or level, select the **trash can** symbol.

  :::image type="content" source="../../media/glint/setup/hierarchy-setup.png" alt-text="Screenshot of step 3 to map hierarchy group attributes." lightbox="../../media/glint/setup/hierarchy-setup.png":::

## 4. Review

Review a summary of all selections made in attribute setup and use the **Go Back** option to make any corrections before moving forward. The review step includes:

- Summary
- User Attributes
- Removed User Attributes
- Required Attributes Mapping
- Derived Attributes Mapping
- Optional System Attributes Mapping
- Hierarchy Groups Mapping

:::image type="content" source="../../media/glint/setup/setup-step4-review.png" alt-text="Screenshot of step 4 to review uploaded attribute mapping.":::

> [!NOTE]
> Viva Glint allows for up to 100 User Attributes. Required, optional system, and hierarchy attributes don't count toward this limit.

## 5. Choose how you want to import data

1. Choose between these two options:

   :::image type="content" source="../../media/glint/setup/setup-step5-choose-import.png" alt-text="Screenshot of step 5 to confirm attribute and data import options.":::

   |Option  | Description  |Use case|
   |:----------|:-----------|:------------|
   |1    |Save attributes and import employee data. Viva Glint creates an attribute mapping and imports all employee data in the file uploaded for attribute setup. Any admin users set up in the platform but not included in the file are **deactivated and lose access to Viva Glint.**      | Select this option if the employee data in your file is complete and finalized and doesn't contain test or partial data.        |
   |2    |Save attributes and discard employee data. Viva Glint creates an attribute mapping only and doesn't import any employee records from the file uploaded for attribute setup.  |Select this option to set up attributes based on your header row only and import employee data later.        |

   > [!CAUTION]
   > Employee data can't be deleted in bulk. Use the **Save attributes and discard employee data** option for initial setup if your file's column labels are finalized but employee data isn't.

2. Select **Save**.

## Update attributes after initial setup

To add new attributes or rename attributes after your initial setup, use [Update attributes in Viva Glint](update-attributes.md) guidance.

## Next step
After setting up your attributes in Viva Glint, choose a data upload method and upload your employee data.

> [!div class="nextstepaction"]
> [Choose a data upload method](choose-upload-method.md)
