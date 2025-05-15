---
title: Viva Glint employee attribute fundamentals
description: Learn how Viva Glint uses data about the people in your organization to convert survey feedback into insightful and action-oriented information to improve employee engagement.
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: standard attributes, custom attributes, functional attributes, time zones, languages
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: concept-article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 05/08/2025
---

# Viva Glint employee attribute fundamentals

Attributes are data about the people in your organization. Attributes are used to convert feedback into insightful and action-oriented intelligence to improve employee engagement and achieve business goals.

Attribute column headers (labels) are unique to your organization. For example, your HR information system (HRIS) may include "Employee ID," while another company has "Work ID." The labels in Microsoft Viva Glint guidance are examples only. Choose name labels that match your organization's HRIS.

## Standard attribute types

- **Required attributes**: These fields are required for each user in your Employee Data File.
- **Recommended attributes**: Custom data for your organization that can include fields that are converted into derived values (or buckets), like Tenure.

> [!NOTE]
> Attributes that are used to derive other fields are required for all future uploads. For example, if Viva Glint uses Hire Date to create Tenure groups, Hire Date is required in all uploads.

### Attributes by item and survey type

| **Attribute** | **Description/Notes** | **Required for Engagement surveys** | **Required for Employee Lifecycle surveys** |
|---|---|---|---|
| **Status** | Must always be fully capitalized ACTIVE or INACTIVE.<br>An employee on temporary leave should have their status updated to INACTIVE and then returned to ACTIVE upon return. | Yes | Yes |
| **First name** | Appears in email invites and reminders (can be the legal first name, preferred first name, or whichever is in your HRIS). | Yes | Yes |
| **Last name** | Employee’s legal last name field from your HRIS. | Yes | Yes |
| **Employee ID** | Each employee has a unique ID. Don't use blanks or spaces. | Yes | Yes |
| **Email address** | Each employee should have a unique email address. Don't include extra spaces.<br>If an employee doesn't have an email address, copy the employee’s unique ID into the email field. | Yes | Yes |
| **Personal email address** | To contact exiting employees, include personal email address. | No | Recommended |
| **Time zone** | See [Time zones](#time-zones) | No | No |
| **Language** | See [Language](#languages) | No | No |
| **Manager ID** | Providing the employee ID of the manager for each employee allows automatic build-out of a manager hierarchy. | Highly recommended | Highly recommended |
| **Hire date** | Used to derive tenure buckets.<br>Viva Glint standard values: <1 Year, 1-2 Years, 2-4 Years, 4-6 Years, 6-10 Years, 10-15 Years, 15-20 Years, 20+ Years.* | No | Yes, to trigger Employee Lifecycle Onboarding surveys |
| **Birth year** | Used to derive age group buckets.<br>Viva Glint standard values: <25, 25-29, 30-34, 35-39, 40-44, 45-49, 50-54, 55-59, 60-64, 65-69, and 70+ | No | No |
| **End date** | Employee’s termination date. | No | Yes, for triggering Employee Lifecycle Exit surveys |

*Tenure values for new Viva Glint customers after January 13, 2024. Before this date: 0-1 Year, 1-2 Years, 2-3 Years, 3-4 Years, 4-5 Years, 5-7 Years, 7+ Years.

## Date attributes

Date information, like Hire date or Term date, can be crucial for collecting feedback from employees as they start at or leave your organization. To use dates to trigger surveys and create distribution lists, ensure that all dates are formatted correctly and consistently in the employee data uploaded to Viva Glint.

### Format dates in Microsoft Excel

If your organization sends data files in Excel format, ensure that:

- The cells that contain dates have a Text format in Excel, **not** Custom or Date formats.
- Your organization selects the date format that is included in uploaded files during attribute setup.
- Your organization completes derivation selections in attribute setup, which transform dates into Viva Glint's preferred format: yyyy/mm/dd.

To reformat dates and the cell format in Excel, see the [resolution steps to correct an incorrectly configured date](/viva/troubleshoot/glint/data-file-upload/fix-upload-derivation-errors?toc=%2Fviva%2Fglint%2Ftoc.json&bc=%2Fviva%2Fbreadcrumb%2Ftoc.json#the-date-format-is-incorrectly-configured). 

If a date's format is correct (for example, mm/dd/yyyy), but the cell format needs to be updated to Text, follow these steps:

1. In Excel, select the date column.
2. Choose the **Data** option the ribbon at the top of the file.
3. Choose the **Text to Column**s option.
4. In the Text Wizard dialog that appears, select **Delimited** and then choose **Next**.
5. In the **Delimiters** section, choose **Tab** and select **Next**.
6. In the Column data format section, choose **Text** and select **Finish**.

## Custom attributes

Use custom attributes to see which groups of employees are more engaged than others and use this information to develop action plans to improve engagement. Your organization can include up to 100 custom attributes; required and hierarchy attributes don't contribute to the 100 custom attribute limit. Include attributes in your employee data file header row with labels that match your HRIS.

- The more attributes you provide, the more ways data can be sliced and diced to provide richer insights and alerts. 
- Attributes that are too specific don't meet the minimum confidentiality threshold of five to appear in reporting, so avoid them.

### General Data protection Regulation (GDPR) compliance for attributes

Confidentiality around employee data is of the highest priority for Microsoft Viva Glint. Using [EU General Data Protection Regulation (GDPR) guidelines](/compliance/regulatory/gdpr), we apply these privacy protection standards globally to ensure that every person’s data is handled with the utmost confidentiality and integrity.

## Optional system attributes

Optional system attributes are values that indicate how and when communications are sent to an employee, such as time zone and language.

|Optional System Attribute  |Description  |
|----------|-----------|
|Survey Language     |The language for employee surveys and emails.      |
|Dashboard Language|The language for users' dashboards.  |
|User Timezone|The time zone in which survey communications are sent.  |
|Personal Email|Users' personal email addresses that can be used to survey exiting employees. Select Company and Personal Email in the Communications section of your survey program.  |

> [!IMPORTANT]
> Send language and time zone values exactly as they appear in related tabs in the following articles:
> - [Viva Glint supported languages](supported-languages.md)
> - [Viva Glint supported time zones](supported-time-zones.md)
> 
> Users with blank or invalid values receive and access surveys/emails/dashboards in your organization's default selection in General Settings.

### Time zones

Global companies often include a time zone attribute column in their employee data to trigger emails in employees’ time zones. To find valid time zone values, see: [Viva Glint supported time zones](supported-time-zones.md). Before a survey launches, ensure that all employees have a valid value attached to their records.

### Languages

To find language values that trigger survey emails in an employee’s preferred language, see: [Viva Glint supported languages](supported-languages.md). Ensure that you include a Language column in your employee data. Before a survey launches, ensure that all employees have a valid value attached to their records.

If you also supply language values to indicate users’ dashboard languages (for users who view reports), include a separate column (example: Dashboard Language).

> [!NOTE]
> Dashboards don't support languages that are read from right to left.

### Recent language changes

On April 10 2025, some supported languages for Viva Glint changed. Some languages are deprecated, and potential replacements are noted in the following table. These languages receive no updates after April 10, 2025 and are only available in the platform through August 2025. To keep any custom translations, [export translated content](language-translations.md) before the end of August 2025. After August 2025, if deprecated languages are used, users are directed to your organization's default language.

| Current language  | Current language code | Potential alternative language | Potential alternative code |
|:----------|:-----------|:------------|:------------|
| Austrian (German)   | de_AT                 | German  | de_DE  | 
| Chinese (Hong Kong) | zh_HK  | Chinese (Traditional) or Chinese (Simplified) | zh_TW or zh_CN  |
| Bengali             | bn_BD                | Bangla  | bn_IN  | 
| Armenian            | hy_AM   | None  | None  | 
| Haitian Creole      | fr_HT  | None  | None  | 
| Northern Sotho      | ns_ZA   | None | None  | 
| Sinhala             | si_LK   | None | None  | 
| Swahili             | sw_KE   | None | None  | 
| Welsh               | cy_GB  | None  | None  | 
| Xhosa               | xh_ZA  | None  | None  |

## Next step
Learn about Viva Glint organizational hierarchy fundamentals, including a Viva Glint calculated Manager Hierarchy and other hierarchy groups.

> [!div class="nextstepaction"]
> [Viva Glint organizational hierarchy fundamentals](hierarchy-fundamentals.md)
