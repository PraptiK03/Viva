---
title: Survey hiring managers with Viva Glint
description: While Microsoft Viva Glint doesn't offer a survey template for hiring feedback, Viva Glint Administrators can use use existing Viva Glint features to gather sentiment.
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

While Microsoft Viva Glint doesn't offer a survey template for hiring feedback, Viva Glint Administrators can use use existing Viva Glint features to gather sentiment. Before setting up a survey, consider how often hiring managers have new hires, ideal survey reporting thresholds, and how easily your organizaton can add new attributes to employee data.

> [!IMPORTANT] 
> Viva Glint doesn't currently offer standard items related to the hiring manager experience and no External benchmarks are available.

## New attributes to include

For this kind of feedback, the respondent shifts from individual employees responding to questions on their company to hiring managers describing to their recruiter and new hire experiences. To reach out to hiring managers and include the right information in survey questions, [consider adding new attribtues](update-attributes.md): 

- **New hire start date:** To trigger surveys or create Distribution lists based on when new hires started.
- **New hire full name:** To let hiring managers know which new hires they're giving feedback for.
- **Hiring manager flag:** To add hiring managers to Distribution Lists.
- **Recruiter full name:** To let hiring managers know which recruiters they're giving feedback for.

## Survey type options

| Survey type | Timeframe | Survey access | Attributes | Question phrasing | Communications | Survey ubmissions |
|:----------|:-----------|:------------|:----------|:-----------|:------------|:------------|
| Always-On | Past month or quarter | [Attribute-based access](attribute-based-survey-access.md) <br> or <br> [Authentication with Entra](understand-survey-access-methods.md#authentication-with-microsoft-entra-id) | Hiring manager flag | General, with no references to specific new hires or recruiters | Sent by Viva Glint Admins (Always-On surveys don't include notifications) | Use the "Next survey available" option in [Program setup](program-set-up.md#define-the-basics) to determine how long users wait before submitting another survey |
| Always-On | As needed, when there are new hires or recruiters to gather feedback on | [Attribute-based access](attribute-based-survey-access.md) <br> or <br> [Authentication with Entra](understand-survey-access-methods.md#authentication-with-microsoft-entra-id) | Hiring manager flag <br> New hire full name <br> Recruiter full name | Specific, with references to hew hires or recruiters using attributes | Sent by Viva Glint Admins (Always-On surveys don't include notifications) | Use the "Next survey available" option in [Program setup](program-set-up.md#define-the-basics) to determine how long users wait before submitting another survey |
| Employee Lifecycle | As needed, when hiring managers are eligible based on "New hire start date" | [Attribute-based access](attribute-based-survey-access.md) <br> or <br> [Authentication with Entra](understand-survey-access-methods.md#authentication-with-microsoft-entra-id) <br> or <br> [Personalized link](understand-survey-access-methods.md#personalized-survey-link) | New hire date <br> Hiring manager flag <br> New hire full name <br> Recruiter full name | Specific, with references to hew hires or recruiters using attributes | Use Viva Glint survey invite and reminder notifications | Use the "Waiting period between surveys" option in [Program setup](program-set-up.md#define-the-basics) to determine how long users wait before submitting another survey |
| Recurring | Past month or quarter | [Attribute-based access](attribute-based-survey-access.md) <br> or <br> [Authentication with Entra](understand-survey-access-methods.md#authentication-with-microsoft-entra-id) <br> or <br> [Personalized link](understand-survey-access-methods.md#personalized-survey-link) | Hiring manager flag | General, with no references to specific new hires or recruiters | Use Viva Glint survey invite and reminder notifications | One submission per hiring manager per survey cycle |
| Recurring | Past month or quarter | [Attribute-based access](attribute-based-survey-access.md) <br> or <br> [Authentication with Entra](understand-survey-access-methods.md#authentication-with-microsoft-entra-id) <br> or <br> [Personalized link](understand-survey-access-methods.md#personalized-survey-link) | Hiring manager flag <br> New hire full name <br> Recruiter full name | Specific, with references to hew hires or recruiters using attributes | Use Viva Glint survey invite and reminder notifications | One submission per hiring manager per survey cycle  |

## Reporting considerations

## Confidentiality considerations

