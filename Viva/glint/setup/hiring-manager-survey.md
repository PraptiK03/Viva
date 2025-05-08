---
title: Survey hiring managers with Viva Glint
description: While Microsoft Viva Glint doesn't offer a survey template for hiring feedback, Viva Glint Administrators can use existing Viva Glint features to gather sentiment.
ms.author: aweixelman
author: AliciaWeixelman
manager: melissabarry
audience: admin
f1.keywords: NOCSH
keywords: hiring manager survey, recruiter survey, recruiter feedback, manager new hire feedback
ms.collection:  
- m365initiative-viva
- selfserve 
search.appverid: MET150 
ms.topic: install-set-up-deploy
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 05/08/2025
---

# Survey hiring managers with Viva Glint

While Microsoft Viva Glint doesn't offer a survey template for hiring feedback, Viva Glint Administrators can use existing Viva Glint features to gather sentiment. Before setting up a survey, consider how often hiring managers have new hires, ideal survey reporting thresholds, and how easily your organization can add new attributes to employee data.

> [!IMPORTANT] 
> Viva Glint doesn't currently offer standard items related to the hiring manager experience and no External benchmarks are available.

## New attributes to include

For this kind of feedback, the respondent shifts from individual employees responding to questions on their company to hiring managers describing to their recruiter and new hire experiences. To reach out to hiring managers and include the right information in survey questions, [consider adding new attributes](update-attributes.md#add-new-attributes-to-viva-glint) and making them [visible in reporting](update-attributes.md#update-custom-attribute-visibility): 

- **Hiring manager flag:** To add hiring managers to Distribution Lists.
- **New hire start date:** To trigger surveys or create Distribution lists based on when new hires started.
- **New hire full name:** To let hiring managers know which new hires they're giving feedback for.
  - Add separate **New hire first name** and **New hire last name** fields to add "Last, first" name formats into survey and question text.
- **Recruiter full name:** To let hiring managers know which recruiters they're giving feedback for.
  - Add separate **Recruiter first name** and **Recruiter last name** fields to add "Last, first" name formats into survey and question text.
 
> [!IMPORTANT] 
> To trigger surveys for the right users, populate "New hire start date" values for hiring manager records in employee data files. Hiring managers (not new hires) are the targeted respondents.

## Survey type options

| Survey type | Timeframe  | Helpful attributes for distribution lists and survey customization | Question phrasing | 
|:----------|:-----------|:------------|:----------|
| [Always-On](always-on-surveys.md) | Past month or quarter  | <ul><li>Hiring manager flag</li></ul> | General, with no references to specific new hires or recruiters | 
| [Always-On](always-on-surveys.md)  | As needed, when there are new hires or recruiters to gather feedback on | <ul><li>Hiring manager flag </li> <li>New hire full name </li> <li>Recruiter full name</li></ul> | Specific, with references to new hires or recruiters using attributes | 
| [Employee Lifecycle](program-summary-setup-lifecycle.md) | As needed, when hiring managers are eligible based on "New hire start date" | <ul><li>New hire date </li> <li>Hiring manager flag </li> <li>New hire full name </li> <li>Recruiter full name</li></ul>| Specific, with references to new hires or recruiters using attributes | 
| [Recurring](program-summary-overview.md) | Past month or quarter  | <ul><li>Hiring manager flag</li></ul> | General, with no references to specific new hires or recruiters | 
| [Recurring](program-summary-overview.md)  | Past month or quarter  | <ul><li>Hiring manager flag </li> <li>New hire full name </li> <li>Recruiter full name</li></ul> | Specific, with references to new hires or recruiters using attributes | 

### Communications

For Recurring and Employee Lifecycle surveys, use Viva Glint survey invite and reminder notifications in [Communications](program-summary-communications.md). Always-On surveys don't include a Communications section and Viva Glint Admins need to manage and send all notifications outside of the Viva Glint app.

### Survey access methods

If your organization chooses Employee Lifecycle or Recurring survey types for getting feedback from hiring managers, choose from Viva Glint's available survey access methods:

- [Attribute-based access](attribute-based-survey-access.md)  
- [Authentication with Entra](understand-survey-access-methods.md#authentication-with-microsoft-entra-id)  
- [Personalized link](understand-survey-access-methods.md#personalized-survey-link)

For Always-On surveys, which don't include Communications to deliver personalized links, choose from:

- [Attribute-based access](attribute-based-survey-access.md)  
- [Authentication with Entra](understand-survey-access-methods.md#authentication-with-microsoft-entra-id)  

> [!TIP]
> To ensure hiring managers are still with your organization and can access surveys via Entra authentication, only include Active users in [Distribution Lists](set-up-distribution-lists.md). 

## Confidentiality

Depending on how regularly your organization hires new employees, respondent counts may be small for a given month or quarter. Consider adjusting confidentiality for hiring manager surveys so that your users can effectively view and act on feedback.

- [How Viva Glint protects privacy](viva-glint-survey-privacy.md)
- [Manage Viva Glint confidentiality thresholds](manage-confidentiality-thresholds.md)

## Survey submissions 

Recurring surveys allow one submission per hiring manager per survey cycle and each survey cycle is a fixed point in time that can trend with other cycles. Always-On and Employee Lifecycle surveys, however, are ongoing and trend data on a rolling basis. Depending on Viva Glint Admins' selections in Program setup, users can respond multiple times in a single reporting timeframe.

To determine how long users wait before submitting another survey, use the "Next survey available" (Always-On) or "Waiting period between surveys" (Lifecycle) in [Program setup](program-set-up.md#define-the-basics). To let hiring managers respond as often as possible, lower this setting to one.

## Reporting

Viva Glint recurring surveys happen at definite points in time and trend based on each survey cycle. But scores for Employee Lifecycle and Always-On surveys trend differently because of their ongoing nature. If you choose Lifecycle or Always-On surveys to get hiring manager feedback, review how reporting functions for these survey types:

- [How data trends for ongoing surveys](/viva/glint/reports/trend-graph-lifecycle-survey)
- [How responses are counted in ongoing survey reporting](/viva/glint/reports/trend-graph-lifecycle-survey#understand-how-response-numbers-show-in-elc-reporting)

