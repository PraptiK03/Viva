---
title: Overview of People Skills
ms.author: bhaswatic
author: bhaswatic
manager: elizapo
ms.reviewer: chrisarnoldmsft
ms.date: 04/29/2025
audience: admin
ms.topic: overview
ms.service: viva-learning
search.appverid: MET150
ms.collection:
  - enabler-strategic
  - m365initiative-viva-learning
ms.localizationpriority: medium
description: An introduction to People Skills, an AI-powered service providing skills-based experiences.
---

# Overview of People Skills


> [!NOTE]
> This feature is currently in preview. Preview features or services are in development, may not be available to all customers, and are made available on a "preview" basis so you can get early access and send us feedback.

People Skills is an AI-driven service that infers personalized skill profiles for your users mapped to a customizable, built-in taxonomy. This service provides a data layer that fuels the Skills agent, and enhances Microsoft 365 Copilot, Microsoft 365, and Viva services with contextualized information about the people in your organization.  

People Skills:

- Equips leaders with critical workforce skill insights to prepare and accelerate their AI transformation.
- Empowers employees with personalized skill profiles to help them connect with others and grow their careers.


## Licensing  

People Skills comes with your Microsoft 365 Copilot or Viva Suite licenses. It doesn't need a separate license. The People Skills inference engine coverage includes all users in your organization company with an assigned Microsoft 365 Copilot or Viva license. Skills inferencing isn't included in the Viva Communications and Communities (C&C) offer.

Users with the Microsoft 365 base licenses also get access to an improved skills experience and can search skills from your taxonomy and manually add them using the Microsoft 365 Profile editor. 

> [!NOTE]
> Customers with the base Skills Microsoft 365 plan don't receive AI-powered skill inferences or suggestions, but can manually curate their own skills. Customers with Microsoft 365 Copilot or Viva licenses get access to the full People Skills experience, including AI-powered skill inferences.

Contact your Microsoft representative if you have questions on licensing or access.  

## Where does People Skills data appear?

People Skills data appears in Microsoft 365 for employees, leaders, and organizations:  

- [Skills in the Microsoft 365 profile card: ](https://support.microsoft.com/office/explore-what-you-can-do-with-your-skills-0e8dd61c-89b9-42de-8e4d-7c606806cf40)Users can view and manage their skills with others directly from the profile card in Microsoft 365 to share their skills and learn more about others.
- [Skills in Microsoft 365 Copilot:](https://support.microsoft.com/office/explore-what-you-can-do-with-your-skills-0e8dd61c-89b9-42de-8e4d-7c606806cf40) If you use Microsoft 365 Copilot, shared skills surface in people related queries in Copilot to help form connections and find people with the skills you need.
- **Skills in Org Explorer and People Companion**:  Tools like [Org Explorer](https://support.microsoft.com/office/explore-what-you-can-do-with-your-skills-0e8dd61c-89b9-42de-8e4d-7c606806cf40) and [People Companion](/microsoft-365-apps/companions/people) help users quickly find the right person based on their shared skills data.
- **Skills in Viva Learning:** Users can now manage skills they want to develop within Viva Learning, and receive personalized course recommendations based on those skills.
- [Skills in Copilot Analytics (Viva Insights):](https://go.microsoft.com/fwlink/?linkid=2320729) The Skills landscape report allows organizational analysts to discover top skills in their workforce, assess their distribution across groups, identify potential gaps, and explore related skill insights.
- **Skills for Leaders in Microsoft 365 Copilot**: Copilot enables leaders to ask targeted or broad questions about their team’s skills and receive instant, data-driven answers.  
- **Skills Agent** (coming soon): The Skills agent helps employees and leaders explore, manage, and use organizational skills for personal growth and strategic planning. 

People Skills AI inferencing and experiences are based on a user's Microsoft 365 Copilot, Microsoft 365, Office 365, and Viva plan. Read more about [licensing in People Skills](#licensing). 


## Inference engine 

The People Skills inference engine uses Microsoft 365 profile and activity signals from the Microsoft Graph to create personalized skill profiles for users in your organization. Profile and activity signals include documents, emails, chats, and meetings.


:::image type="content" source="../media/skills/skills-workflow-graphic.png" alt-text="Diagram showing the People Skills inferencing engine using collaboration, role data, AI, user-confirmed skills in an organizational context." lightbox="../media/skills/skills-workflow-graphic.png":::


**[Microsoft Graph](/graph/overview) and AI Graph**: Includes data from user profiles, job titles, collaboration signals, and documents; and key phrases from emails, meetings, and documents.

- **Microsoft Skills Graph**: Provides a base skills taxonomy and semantic descriptions for skills 
  - **Microsoft 365 User Profiles**: Offers information on job titles and top contacts. 
  - **Custom data and Third-party systems**: Organizations can import their own custom skills or import existing skills data from third-party systems.  

The inference engine uses the latest OpenAI LLM models and a proprietary inferencing approach with relevant Microsoft Graph data. The skill inferencing engine associates users with a representative set of skill names based on the sources available to People Skills to keep their profiles fresh and relevant. The inferred skills are based on the context of the source signals and inferencing methodologies. They aren't intended to be a comprehensive reflection of a person’s capabilities.

The skill inferencing engine operates under following constraints: 

- We currently only infer skills from Microsoft 365 sources. We don't use user activity in other line of business applications.  
- People Skills uses large language models. The skills assigned to users are skills most closely matched in the taxonomy for the user profile and activity. For example, if a user creates a document on front end development, we might tag the user with front end development, web development, React, or Angular based on the closest content match.
- Inferences are sometimes impacted by the name and description uploaded by customer administrators.

- Read [AI transparency in People Skills](https://support.microsoft.com/office/ai-transparency-in-skills-c54f3ded-58bf-44dd-9fa1-6cbe49fba106) to learn how we use the inferencing data. 

People Skills also provides a framework for tagging sensitive skills that administrators don't want the inference engine to capture. We continue to share more details on how to tag skills as AI-restricted. 

> [!NOTE]
> We'll share instructions on managing skills inferencing and visibility controls before People Skills general availability.  

## User Profile Application (UPA) Skills 

If your organization depends on skills data that appears in About Me on the Microsoft 365 profile card and editor (formerly in Delve), or on the skills field in the UPA API or Graph API, those skills are hidden from the Microsoft 365 profile card and editor when you deploy People Skills, and replaced with this new experience. 

People Skills migrates shared UPA user skills data to this new experience at a future date. 

When you deploy People Skills, skills from these other sources continue to be accessible to your users to edit. They can edit using the SharePoint user profile editor and surface in some experiences, such as Microsoft 365 Copilot chat and people search. 

We'll update this article with more information on handing your requirements for existing dependencies. 

## Responsible AI 

Read about [AI transparency in People Skills](https://support.microsoft.com/office/ai-transparency-in-skills-c54f3ded-58bf-44dd-9fa1-6cbe49fba106).
