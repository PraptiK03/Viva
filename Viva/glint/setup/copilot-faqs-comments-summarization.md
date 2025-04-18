---
title:  Microsoft 365 Copilot in Viva Glint-FAQs for comments summarization
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
ms.date: 04/18/2025
---

Microsoft 365 Copilot in Viva Glint-FAQs for comments summarization

> [!NOTE]
> Not all items in the Microsoft Viva Glint Question Library are posed in question format. Question Library items can be statements for the survey taker to rate on a given scale. For this reason, the term "item" is often used to refer to the all contents of the Question Library, regardless of whether it's a question or statement.


**Q: How can we differentiate between item (item label) and customized topics, which may or may not be Glint topics? What is the best practice for applying filters (for example, groups, topics, question labels)?**

**A:** Item labels and topics can sometimes be indistinguishable, such as the “Inclusion” item versus the general topic of inclusion. Viva Glint Copilot initially identifies item labels in the user prompt and filter comments based on those labels. Subsequently, Copilot summarizes comments that closely align with the topics identified in the user prompt. For instance, if the user requests Copilot to “summarize comments about inclusion” and there is an “Inclusion” item label, Copilot first filters comments about the Inclusion *item* and then summarizes comments discussing inclusion as a *topic*.

Copilot uses filters applied to the report—for example: item labels, topics, people attributes, —before summarizing. For this reason, the optimal way to ensure accurate interpretation of user intent is to **first apply all relevant filters** to a report. **After filtering, request Copilot to summarize non-Glint topics**. 

>For example, users can apply these filters to the comments report:
>- “Career” item label
>- “Compensation” Glint topic
>- “Negative” comment sentiment
>- “Engineering” department
>
>Now ask Copilot, “What are people saying about stock options?”, as stock options is not a Viva Glint topic. This approach enables Copilot to differentiate between various filters and incorporate custom topics from the user prompt.


<br>**Q:**Can I ask about attributes that I don't have permissions (or access) to?**

**A:**No. Copilot in Viva Glint can't filter by any attributes that a user doesn't have acces to. 

<br>**Q: When does Copilot use all comments in its summarization ? When does Copilot summarize by a topic-based sampling? How is the sample size determined?**

>[!NOTE]
> Currently Copilot in Viva Glint can summarize and filter up to 8000 comments.

**A:** Use these examples to understand summarization analytics:

> **Scenario 1: The user asks about specific survey item labels or comment topics.** In this case the prompt might be "Summarize comments from the career and empowerment items" or "Summarize comments about promotion". 
> - Copilot behavior:
>   - Copilot first filters comments based on the detected survey item labels from the user prompt, in addition to any filters already applied to the report. Next Copilot looks for comments with words tied most closely related to the survey item or the comment topic in the user prompt. 
>   - A workaround to ask Copilot to summarize all comments using stratified sampling (up to 8k comments) from specific questions is to apply the question filters to the report first then ask Copilot to "summarize all comments". See scenario 2 for details. 
<br>
> **Scenario 2: The user doesn't include specific survey item labels or comment topics in the prompts.** In this case, "Summarize all comments", "Summarize comments from the engineering team", or "Summarize employee recommendations from US employees".
>- Copilot behavior:
>   - Copilot first filters the comments based on the detected filters in the user prompts, perhaps demographic filters, prescriptive comments, or comment sentiments. These filters are in addition to the filters already applied to the report. 
>   - Out of the filtered comments, Copilot performs stratified sampling up to 8K comments, by either item or topics:
>     - If there is more than one topic with sufficient respondents, Copilot performs stratified sampling by topics. The sample contains comments for different topics in the same ratio as the population.
>     - If there are one or no topics with sufficient respondents of the filtered comments, Copilot performs stratified sampling by survey items. The sample contains comments for different survey itemss in the same ratio as the population.


<br>**Q: **5.	How often does Copilot in Viva Glint update underlying models (functionalities)? Are there notes about new functionalities with each update? We'd like to expect and explain potential differences.?**

**A:**•	Glint continuously monitors Copilot’s reliability and performance to determine whether a new model update would address any existing issues or improve Copilot’s response quality and system performance. Glint sends out release notes about major feature updates which may or may not require model updates. 

<br>**Q: **

**A:**

<br>**Q: ?**

**A:**

<br>**Q: **

**A:**

<br>**Q: **

**A:**

<br>**Q: ?**

**A:**

