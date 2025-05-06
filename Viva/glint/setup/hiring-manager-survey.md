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
ms.date: 05/06/2025
---

# Survey hiring managers with Viva Glint

While Microsoft Viva Glint doesn't offer a survey template for hiring feedback, Viva Glint Administrators can use existing Viva Glint features to gather sentiment. Before setting up a survey, consider how often hiring managers have new hires, ideal survey reporting thresholds, and how easily your organization can add new attributes to employee data.

> [!IMPORTANT] 
> Viva Glint doesn't currently offer standard items related to the hiring manager experience and no External benchmarks are available.

## New attributes to include

For this kind of feedback, the respondent shifts from individual employees responding to questions on their company to hiring managers describing to their recruiter and new hire experiences. To reach out to hiring managers and include the right information in survey questions, [consider adding new attributes](update-attributes.md): 

- **New hire start date:** To trigger surveys or create Distribution lists based on when new hires started.
- **New hire full name:** To let hiring managers know which new hires they're giving feedback for.
- **Hiring manager flag:** To add hiring managers to Distribution Lists.
- **Recruiter full name:** To let hiring managers know which recruiters they're giving feedback for.

## Survey type options

| Survey type | Timeframe | Survey access | Attributes | Question phrasing | Communications |
|:----------|:-----------|:------------|:----------|:-----------|:------------|
| [Always-On](always-on-surveys.md) | Past month or quarter | [Attribute-based access](attribute-based-survey-access.md) <br> or <br> [Authentication with Entra](understand-survey-access-methods.md#authentication-with-microsoft-entra-id) | <ul><li>Hiring manager flag</li></ul> | General, with no references to specific new hires or recruiters | Sent by Viva Glint Admins (Always-On surveys don't include notifications) |  
| [Always-On](always-on-surveys.md)  | As needed, when there are new hires or recruiters to gather feedback on | [Attribute-based access](attribute-based-survey-access.md) <br> or <br> [Authentication with Entra](understand-survey-access-methods.md#authentication-with-microsoft-entra-id) | <ul><li>Hiring manager flag </li> <li>New hire full name </li> <li>Recruiter full name</li></ul> | Specific, with references to hew hires or recruiters using attributes | Sent by Viva Glint Admins (Always-On surveys don't include notifications) |
| [Employee Lifecycle](program-summary-setup-lifecycle.md) | As needed, when hiring managers are eligible based on "New hire start date" | [Attribute-based access](attribute-based-survey-access.md) <br> or <br> [Authentication with Entra](understand-survey-access-methods.md#authentication-with-microsoft-entra-id) <br> or <br> [Personalized link](understand-survey-access-methods.md#personalized-survey-link) | <ul><li>New hire date </li> <li>Hiring manager flag </li> <li>New hire full name </li> <li>Recruiter full name</li></ul>| Specific, with references to hew hires or recruiters using attributes | Use Viva Glint survey invite and reminder notifications | 
| [Recurring](program-summary-overview.md) | Past month or quarter | [Attribute-based access](attribute-based-survey-access.md) <br> or <br> [Authentication with Entra](understand-survey-access-methods.md#authentication-with-microsoft-entra-id) <br> or <br> [Personalized link](understand-survey-access-methods.md#personalized-survey-link) | <ul><li>Hiring manager flag</li></ul> | General, with no references to specific new hires or recruiters | Use Viva Glint survey invite and reminder notifications | 
| [Recurring](program-summary-overview.md)  | Past month or quarter | [Attribute-based access](attribute-based-survey-access.md) <br> or <br> [Authentication with Entra](understand-survey-access-methods.md#authentication-with-microsoft-entra-id) <br> or <br> [Personalized link](understand-survey-access-methods.md#personalized-survey-link) | <ul><li>Hiring manager flag </li> <li>New hire full name </li> <li>Recruiter full name</li></ul> | Specific, with references to hew hires or recruiters using attributes | Use Viva Glint survey invite and reminder notifications |

## Confidentiality

Depending on how regularly your organization hires new employees, respondent counts may be small for a given month or quarter. Consider adjusting confidentiality for hiring manager feedback so that your users can effectively view and act on feedback.

- [How Viva Glint protects privacy](viva-glint-survey-privacy.md)
- [Manage Viva Glint confidentiality thresholds](manage-confidentiality-thresholds.md)

## Survey submissions and reporting

Recurring surveys allow one submission per hiring manager per survey cycle and each survey cycle is a fixed point in time that can trend with other cycles. Always-On and Employee Lifecycle surveys, however, are ongoing and trend data on a rolling basis. Depending on Viva Glint Admins' selections in Program setup, users can respond multiple times in a single reporting timeframe.

- [How data trends for ongoing surveys](/viva/glint/reports/trend-graph-lifecycle-survey)
- [How responses are counted in ongoing survey reporting](/viva/glint/reports/trend-graph-lifecycle-survey#understand-how-response-numbers-show-in-elc-reporting)

To determine how long users wait before submitting another survey, use the "Next survey available" (Always-On) or "Waiting period between surveys" (Lifecycle) in [Program setup](program-set-up.md#define-the-basics) 

