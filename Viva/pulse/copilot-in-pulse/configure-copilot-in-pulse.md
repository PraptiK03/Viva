---
title: "Set up Microsoft 365 Copilot in Viva Pulse"
f1.keywords:
- NOCSH
ms.author: hasrivas
author: hasrivas
manager: alisaliddle
ms.date: 03/19/2025
audience: Admin
ms.topic: install-set-up-deploy
ms.service: viva-pulse
ms.collection: 
- viva-copilot
ms.localizationpriority: medium
search.appverid:
- MET150
description: "Learn how to configure and incorporate Microsoft 365 Copilot in Viva Pulse within your organization."
---

# Set up Microsoft 365 Copilot in Viva Pulse

Microsoft 365 Copilot in Viva Pulse is your everyday AI partner, empowering you to create relevant Pulse questions, requests, and helping you understand your report summaries, in ways that create value for you and your organization. Copilot gives users access to Large Language Model (LLM) technology with [Microsoft Responsible AI protections](https://www.microsoft.com/en-us/ai/responsible-ai). LLM is a type of AI that can process and produce natural language text. 

## Licensing requirements

By default, Copilot capabilities in Viva Pulse are enabled for all users who are assigned a premium Viva Pulse license, purchased as part of _Microsoft Viva Suite_ or _Microsoft Viva Workplace Analytics and Employee Feedback_ or assigned a Microsoft 365 Copilot license.

For details on Microsoft Viva plans and pricing, visit the [Employee Experience Platform Plans and Pricing page](https://www.microsoft.com/microsoft-viva/pricing).

## Control access to Copilot and AI Summarization services

Access to Copilot capabilities in Viva Pulse is manager through the [Viva feature access management platform](/viva/feature-access-management). Feature access management allows admins to create three types of access policies (tenant, users, and groups) for each feature through PowerShell commandlets. Policies provide a flexible and scalable approach to deployment.

Policy settings apply anytime a user signs in, allowing the user access to all enabled features. Because you can set multiple access policies--targeting the tenant, groups, and individual users--a user can be impacted by more than one policy. Individual user and group level policies always take priority over a tenant-level policy. For instructions, see [Control access to features in Viva](/viva/feature-access-management). Changes to Copilot may require 24 hours to take effect. 

| Pulse feature | Copilot in Viva Pulse State | Description |
|:-------------|:------------------:|:----------------------|
|**Report Summarization** |**Enabled**| This state enables Pulse authors to view a summary for their Pulse reports in-app and included as part of their notifications.|
| |**Disabled**|If you disable Copilot capabilities in Viva Pulse, report summaries won't be visible as part of Pulse reports nor as part of the notifications sent to the authors.|



## Access Copilot in Viva Pulse

Users can access Copilot in Viva Pulse as part of the generated reports. In the future, we'll be bringing newer Copilot capabilities to author new Pulse questions and requests, along with question recommendation based on your Pulse series, etc. 




