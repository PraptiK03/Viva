---
title: Access Viva Glint raw survey responses
description: Admins can export employee data and raw data from Viva Glint programs.
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: Microsoft Viva Glint, raw data, extreme circumstance, DSR, raw data export
ms.collection: 
 - m365initiative-viva
 - selfserve
 - essentials-compliance
 - essentials-security
search-appverid: MET150
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.custom: CELA-approved
ms.date: 3/14/2025
---

# Access Viva Glint raw survey responses

In Microsoft Viva Glint, "raw survey responses" refers to unaggregated survey responses that are directly tied to a survey taker. 

## Who has access to raw survey responses?

By default, Viva Glint’s in-product reporting does not include raw survey responses and is reported in the aggregate. However, your organization may choose to make some surveys “identifiable,” meaning survey responses are directly linked to the survey taker. If a survey is identifiable, survey takers are informed before taking the survey. Learn more about [Viva Glint confidentiality and reporting](viva-glint-survey-privacy.md).

While raw survey responses are not included in Viva Glint default reporting, Viva Glint Administrators can export them unless export is disabled. Even when export of raw survey responses is disabled, your organization may still access raw survey responses if it determines that certain Extreme Circumstances exist. Learn more about the [Extreme Circumstances exception](#exception-for-extreme-circumstances). 

## Configuring raw survey response export

By default, raw survey responses are exportable for each new survey program, but Viva Glint admins can opt out of raw survey response exports. When setting up each Viva Glint program, the Viva Glint admin decides whether raw survey response exports are available. 

Admins can configure the Export Raw Survey Responses control at any time during a survey program, but the change only applies to future survey cycles. Closed cycles permanently conform to the setting established when the cycle launched. That is, if export was disabled when a survey cycle launched, enabling it later doesn't retroactively allow export of raw survey responses.

## Disabling export of raw survey responses permanently limits your access to this data

> [!CAUTION]
> Disabling export of raw survey responses means that:
> - Your organization permanently loses the ability to access these raw survey responses unless you determine that certain Extreme Circumstances exist. Learn more about the [Extreme Circumstances exception](raw-data-extreme-circumstances.md). 
> - If your organization leaves Viva Glint, you aren't able to take these raw survey responses with you.
> - You aren't able to (and Microsoft isn't able to facilitate) transfer of these raw survey responses to a third party, such as an alternative survey platform or data analytics consultant.  

## Exception for Extreme Circumstances

Even when export of raw survey responses is disabled, you can still identify a survey taker if your organization determines that Extreme Circumstances exist. 

### What does Extreme Circumstances mean? 

Extreme Circumstances exist if your organization determines that disclosure of a survey taker’s identity is necessary to investigate, prevent, or take action regarding illegal activities, suspected fraud, or situations involving potential threats to the safety of a person, or to otherwise comply with the law.

If your organization determines that Extreme Circumstances exist, you can make an Extreme Circumstances disclosure request, and Microsoft will identify the survey taker.

### Who determines whether Extreme Circumstances exist?

Your organization is solely responsible for determining whether Extreme Circumstances exist. Microsoft doesn't independently evaluate Extreme Circumstances disclosure requests. If your organization attests that Extreme Circumstances exist, Microsoft provides the requested identity of the survey taker.

[Learn how to make an Extreme Circumstances disclosure request](raw-data-extreme-circumstances.md).

## Responding to Data Subject Requests (DSRs) when export of raw survey responses is disabled

In some jurisdictions, Viva Glint users may have certain rights related to their personal data, including the rights to access, correct, delete, and restrict processing. Because raw survey responses are linked (or linkable) to identifiable survey takers, they are considered personal data. [Learn more about DSRs](/compliance/regulatory/gdpr-data-subject-requests).

If you need to provide a survey taker with their raw survey responses to fulfill a DSR, you can do so even if export of this data has been disabled. Viva Glint allows admins to send a survey taker’s raw survey responses directly to the survey taker without accessing or viewing this data. Learn how to [respond to DSRs in Viva Glint](raw-data-request-response.md).

## Configure raw survey response exports

By default, export of raw survey responses is enabled for each new Viva Glint survey program. However, the Viva Glint admin can disable export using a control in the Confidentiality section of Program Setup.

1.	Select Survey Programs in the Survey section.
2.	Select the survey and then Program Setup on the Program Summary page.
3.	Find the Confidentiality section of the Program Setup page.
4.	Here you find a control entitled “Enable Raw Survey Response Export.” 
5.	By default, the control is set to YES, meaning export is enabled.
6.	To disable export of raw survey responses, set the control to NO.

> [!NOTE]
> You cannot enable export of raw survey responses when a program is in Approved status. To enable raw survey response export, ensure Approved is set to NO. 

Opting out of response exports occurs within the **Confidentiality** section of *Program Setup*. Program Summary is accessible from the *Survey Programs* configuration page of the admin dashboard. 

1. Select **Survey Programs** in the **Survey** section.
1. Select the survey and then **Program Setup** on the *Program Summary* page.
2. The default setting for **Enable Export of Raw Survey Responses** is **YES**. Toggle to **NO** to opt out of raw survey response exports. [Read more about the confidentiality statement](viva-glint-survey-privacy.md).

## Export raw survey responses

If export is enabled for a survey program, you can export raw survey responses for Recurring, Ad Hoc, Employee Lifecycle, and Always-On surveys.

### Export raw survey responses for Recurring and Ad Hoc surveys

1.	Go to the **Configuration** page and select **Survey Programs.**
2.	Select your survey program and go to the **Completed cycles** tab.
3.	On the row with the appropriate cycle, select the ellipses (three dots) and then **Export Raw Survey Responses.**
1. In the export panel that appears:
   1. Select attributes to include in the Export Options section. Choose from: Survey Cycle ID, Survey Sent Date, Comments, Comment Topics, Sensitive Comment Flag, and Use question's description instead of UUID.
   1. Select attributes from your organization in the Attributes section.
   2. After making all selections, select **Export.**
5.	Your CSV file downloads to your device. Larger files take more time to generate. You receive an email when your file is ready to download.

### Export raw survey responses for Employee Lifecycle and Always-On surveys

1.	Go to the **Configuration** page and select **Survey Programs.**
2.	Select your survey program and then the **Actions** menu.
3.	Choose **Export Raw Survey Responses.**
1. In the export panel that appears:
   1. Select a Start Date and End Date in the Date Range section.
   1. Select a date type:
      1. The date the participant started the survey (which matches Reports).
      2. The date the participant completed the survey.
   1. Select attributes to include in the Export Options section. Choose from: Survey Cycle ID, Survey Sent Date, Comments, Comments Topics, Sensitive Comments Flag, and Use question's description instead of UUID. Survey Start Date is also available for Always-On surveys.
   2. Select attributes from your organization in the Attributes section.
   3. After making all selections, select **Export.**
5.	The CSV file downloads to your device. Larger files take more time to generate. You receive an email when your file is ready to download.

## Raw survey response file layout and content

The fields included in your Viva Glint raw survey response exports varies. Variation is based on the attributes that your organization sends, export selections, and the items included in your survey. The following columns are always included, with a field for every survey item:

|Field Label  |Description   |Value Format|
|----------|-----------|------------|
|Survey Cycle Creation Date   |The date and time that surveys were generated for users.       |YYYY-MM-DD hh:mm:ss|
|Survey Cycle Completion Date|The date and time the survey was completed by each user.    |YYYY-MM-DD hh:mm:ss|
|Survey Cycle Title|The name of the survey cycle.  |\<Month> \<Year> \<Program name> Survey|
|ItemText1  |Full text of survey item or question UUID. |Numeric response value.|
|ItemText2  |Full text of survey item or question UUID. |Numeric response value.|
|ItemText3  |Full text of survey item or question UUID. |Numeric response value.|

### Partial, blank, and termed employee response handling

- Partially completed surveys that participants don't submit aren't included in raw response exports.
- Blank surveys with no question responses or comments aren't included in raw response exports.
- Surveys submitted by terminated employees are included in raw response exports. Consider your organization's [data deletion settings](manage-general-settings.md#user-data) and how they affect terminated employee response data.

> [!NOTE]
> - The export option is only available to admins.
> -	The export option is only enabled for a survey cycle if the raw survey response export was enabled for the selected survey program before the survey went live.

> [!CAUTION]
> Once a survey is live, the choice to enable or disable raw survey response export can't be changed for that survey.
