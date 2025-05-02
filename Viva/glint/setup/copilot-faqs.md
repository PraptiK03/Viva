---
title:  Microsoft 365 Copilot in Viva Glint-FAQs 
description: Scan commonly asked questions about the comments summarization tool in Microsoft Viva Glint.
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: comment summarization, language for comments summarization, Copilot in Viva Glint metrics, purchasing Copilot in Viva Glint
ms.collection:  
- m365initiative-viva
- selfserve
- viva-copilot
- magic-ai-copilot
search.appverid: MET150 
ms.topic: faq
ms.service: viva-glint
ms.localizationpriority: high
ms.custom: CELA-aapproved
ms.date: 05/01/2025
---

# Microsoft 365 Copilot in Viva Glint-FAQs 

## Foundational and enablement questions

**Q: Should we have concerns about bias in Copilot in Viva Glint? What metrics are used to measure performance?**

**A:** At Microsoft, our commitment to responsible AI is paramount. Copilot in Viva Glint aligns with our AI principles and undergoes rigorous internal stress testing. We ensure Copilot’s comment summarization remains free from undesirable content or behavior such as hate speech, incitement to violence, or misinformation. We're vigilant about protecting privacy and preventing the disclosure of sensitive information. Our ongoing evaluation process incorporates feedback from early adopters and customers, helping us continuously enhance Copilot's performance.

<br>**Q: What happens when a manager or a leader doesn't have access to a demographic attribute or group results and a prompt includes that demographic?**

**A:** When a manager or a leader doesn't have access to a specific demographic attribute or group results, Copilot can't find that attribute in the User's report filter, so is unable to use that attribute for filtering comments. Copilot is still able to summarize the comments but without filtering by that attribute.
Examples:
1. If a User asks to summarize comments from male employees but doesn't have access to the gender attribute or the male attribute value, Copilot summarizes **all** comments and provides a summary. The summary isn't specific to the attribute requested.
2. If a User requests a summary of comments using multiple filters (for example, Accounting department, Generation X) but lacks permission for one or more of the filters, Copilot generates a summary based **only** on the filters the User has permission to access. The summary excludes restricted filters.

<br>**Q: How often is the Large Language Model (LLM) updated for Copilot in Viva Glint?**

**A**: Copilot in Viva Glint uses the latest Open AI LLM model, GPT-4.0, trained with data up to October 2023. We don't use customer data to train the LLM model. While it currently relies solely on customer survey data without external references, engineering is continuously updated to ensure Copilot delivers accurate and relevant responses based on survey input.

<br>**Q: What’s the licensing for Copilot in Viva Glint?** **Is it part of the Copilot or Viva Glint licensing?**

**A:** Copilot in Viva Glint is separate from the Microsoft 365 Copilot license and is available with a Viva Glint or Microsoft Viva license.

<br>**Q: Is Copilot in Viva Glint included in the Viva Glint subscription or as part of Viva Suite?**

**A:** Copilot in Viva Glint is available for all Viva Glint customers with Microsoft Viva and Viva Glint licenses.
 
<br>**Q: If I have a Microsoft 365 Copilot license and a license for Viva Glint, does that augment the Copilot in Viva Glint responses by having more scope to ground responses in (e.g., an Excel sheet with data to correlate the survey responses with)?**

**A:** Currently, no.

<br>**Q: How is Copilot in Viva Glint enabled?**

**A:** Admins enable Copilot in Viva Glint within programs.
 
<br>**Q: What operational factors and settings allow for effective and responsible use of Copilot in Viva Glint?**

**A:** Viva Glint admins can enable or disable Copilot in Viva Glint for any role, in any survey program. Copilot in Viva Glint launches as **disabled** or **off** for all users by default.

<br>**Q: Is Copilot in Viva Glint proprietary in how it works or is it similar to Microsoft Copilot?**

**A:** Yes, Copilot in Viva Glint is proprietary in how it works.

## Current capabilities

<br>**Q: What features does enabling Copilot in Viva Glint provide access to?**

**A:** Through an interactive question and response format, users can request comment summarization across survey items, and filter attributes. Current functionality includes the ability to summarize, in English:
- All Comments
- Comments by Item
- Comments by Comment Sentiment
- Comments by Filter Attribute
- Prescriptive Comments
 
<br>**Q: What languages does Copilot in Viva Glint support for comment summarization?**

Copilot in Viva Glint comment summarization is available in all languages supported by Viva Glint. The user still needs to interact with Copilot in English. 
 
For the best feedback, encourage your employees to leave comments in their native language.

[Microsoft 365 Copilot currently supports these languages](https://support.microsoft.com/office/supported-languages-for-microsoft-copilot-94518d61-644b-4118-9492-617eea4801d8). Copilot in Viva Glint may not support all of the languages listed on this page. Support for all languages is on the roadmap. Your platform informs you of which languages are available for your programs.

<br>**Q: Can customers participate in multiple private previews and Microsoft 365 Copilot in Viva Glint?**

**A:** Yes, customers can enroll in multiple private previews by joining the Viva Customer Connection Program (VCCP), a prerequisite for any Viva private preview.
 
<br>**Q: Does Copilot in Viva Glint work retroactively on past surveys, including those migrated from LinkedIn Glint?**

**A:** Yes. Copilot in Viva Glint can analyze comment data from the previous two cycles within a program, including surveys migrated from LinkedIn Glint.
 
<br>**Q: Does Copilot in Viva Glint pull from the program level or generic settings for confidentiality thresholds?**

**A:** Copilot in Viva Glint aligns with the threshold configured on the dashboard or report being viewed.

<br>**Q: Can the end user see variables in summarization, based on the user's question or prompt?**

**A:** Yes, Copilot in Viva Glint shows attributes in its response so you can adjust them for your next prompt. For example, when filtering a particular tenure group or location, it shows what filter attributes are included in the summary provided.
 
<br>**Q: If I ask Copilot in Viva Glint for key topics, does it use the same topic model as Viva Glint today? If not, what did you train on?**

**A:** Copilot in Viva Glint uses the same topic model as Viva Glint today and summarizes up to 10 top topics found in the comments. Topics with comment respondents that fall below the confidentiality threshold are excluded. 

<br>**Q: How is random sampling determined? Is it inclusive of demographic data segmentation or is it stratified to be representative of the larger population?**

**A:** We perform stratified sampling by topics. The sample contains comments for different topics in the same ratio as the population. We don't sample by demographic data.
  
<br>**Q: What influences how Copilot describes demographics (e.g. ethnicity)?**

**A:** Copilot in Viva Glint uses the same demographic filters as available in Reporting in Viva Glint.

<br>**Q: How does Copilot in Viva Glint identify teams?** 

**A:** Team identification is based on the manager hierarchy within your employee data file.

<br>**Q: Is it possible to start a conversation in the dashboard to address comments (e.g., for a manager to acknowledge a comment and address it)?**

**A:** Currently, no.

<br>**Q: Does Copilot in Viva Glint have the ability to look across multiple surveys or just one at time?**

**A:** One at a time, for now. Additionally, Copilot in Viva Glint only reads Ad hoc and Recurring survey programs. We're looking to add the feature to employee lifecycle and always-on programs in the future.

<br>**Q: Can Copilot in Viva Glint generate a PowerPoint from the results?**

**A:** Not yet, but it’s another feature we'd like to explore.
 
<br>**Q: Can Copilot in Viva Glint recognize when some groups (based on attributes) have more of a negative or positive reactions to a certain question? Can it determine cultural bias or language/translation problems?**

**A:** Currently, Copilot in Viva Glint can’t detect potential biases between survey comments left in different languages. 

<br>**Q: Is there a given bank of emotions that Copilot in Viva Glint uses to describe sentiment?**

**A:** No.

## Understanding feedback

<br>**Q: How is feedback data calculated?**

**A:** Learn about [Microsoft Viva Glint's Narrative Intelligence](https://techcommunity.microsoft.com/discussions/results_and_action_taking_on_viva_glint/what-is-viva-glints-narrative-intelligence/3884799) and download the PDF to share with your leaders.

<br>**Q:** How does the algorithm define Diversity, Equity, and Inclusion-related or sensitive topics/attributes? Is it solely based on our attributes sent to Viva Glint? Is there a key term library?

**A:** [Read this article about Copilot's responsible AI approach](https://www.microsoft.com/microsoft-365/blog/2024/02/13/making-our-generative-ai-products-safer-for-consumers).

## Copilot roadmap

<br>**Q: Are new features planned for Microsoft 365 Copilot in Viva Glint?**

**A:** Yes! We let you know as soon as new features are available. All items mentioned as currently unavailable are on our list for consideration.

<br>**Q: Does Copilot in Viva Glint have any limitations?**

**A:** Currently, but under consideration for the future:
- Copilot in Viva Glint works on completed survey cycles for Recurring and Ad hoc programs only. It isn’t currently available for Employee Lifecycle, Always-On, or 360 feedback programs. 
- There must be at least one Recurring or Ad hoc program survey *administered* or *closed* on your Glint platform to use the feature. 
- Copilot in Viva Glint doesn’t take quantitative survey results into consideration. It can’t answer questions that require comparison scores between questions or employee groups. 
- Any AI can make mistakes misrepresenting the information it finds. If you encounter harmful, inappropriate, or inaccurate responses, immediately provide feedback or report a concern through our feedback button in Copilot in Viva Glint or in the Viva Glint app.
- Copilot in Viva Glint samples a subset of comments from each question proportionate to the overall comment count per question. The current limit for this feature is 8,000 comments.
- Copilot in Viva Glint doesn’t currently support cross-program filters.
- Copilot in Viva Glint doesn’t currently support plug-ins.

<br>**Q: What languages does Copilot in Viva Glint support for comment summarization?**

**A:** Copilot in Viva Glint comment summarization is available in most languages supported by Microsoft 365 Copilot. The admin still needs to interact with the program in English. To obtain the best feedback possible, encourage your employees to leave comments in their native language. [Microsoft 365 Copilot supports these languages](https://support.microsoft.com/office/supported-languages-for-microsoft-copilot-94518d61-644b-4118-9492-617eea4801d8)

> [!NOTE]
> Not all languages supported by Microsoft 365 Copilot are available for Viva Glint. Support for all these languages is on the roadmap. Your platform informs you of available languages.

 




