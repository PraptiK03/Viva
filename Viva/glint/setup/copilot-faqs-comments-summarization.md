---
title:  Microsoft 365 Copilot in Viva Glint-FAQs for comments summarization
description: Find answers to your specific inquiries about comments summarization and prompts for Copilot in Viva Glint.
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

## Filtering 

**Q: How can we differentiate between item (item label) and customized topics, which may or may not be Glint topics? What is the best practice for applying filters (for example: groups, topics, question labels)?**

**A:** Item labels and topics can sometimes be indistinguishable, such as the “Inclusion” item versus the general topic of inclusion. Viva Glint Copilot initially identifies item labels in the user prompt and filter comments based on those labels. Subsequently, Copilot summarizes comments that closely align with the topics identified in the user prompt. For instance, if the user requests Copilot to “summarize comments about inclusion” and there is an “Inclusion” item label, Copilot first filters comments about the Inclusion *item* and then summarizes comments discussing inclusion as a *topic*.

Copilot uses filters applied to the report—for example: item labels, topics, people attributes, —before summarizing. For this reason, the optimal way to ensure accurate interpretation of user intent is to **first apply all relevant filters** to a report. **After filtering, request Copilot to summarize non-Glint topics**. 

>For example, users can apply these filters to the comments report:
>- “Career” item label
>- “Compensation” Glint topic
>- “Negative” comment sentiment
>- “Engineering” department
>
>Now ask Copilot, “What are people saying about stock options?”, as stock options is not a Viva Glint topic. This approach enables Copilot to differentiate between various filters and incorporate custom topics from the user prompt.

<br>**Q: Can I ask about attributes that I don't have permissions (or access) to?**

**A:** No. Copilot in Viva Glint can't filter by any attributes that a user doesn't have acces to. 

<br>**Q: When does Copilot use all comments in its summarization ? When does Copilot summarize by a topic-based sampling? How is the sample size determined?**

>[!NOTE]
> Currently Copilot in Viva Glint can summarize and filter up to 8000 comments.

**A:** Use these examples to understand summarization analytics:

> **Scenario 1: The user asks about specific survey item labels or comment topics.** In this case, the prompt might be "Summarize comments from the career and empowerment items" or "Summarize comments about promotion". 
> - Copilot behavior:
>   - Copilot first filters comments based on the detected survey item labels from the user prompt, in addition to any filters already applied to the report. Next Copilot looks for comments with words tied most closely related to the survey item or the comment topic in the user prompt. 
>   - A workaround to ask Copilot to summarize all comments using stratified sampling (up to 8K comments) from specific items, is to apply the filters to the report first then ask Copilot to "Summarize all comments."
>     
> **Scenario 2: The user doesn't include specific survey item labels or comment topics in the prompts.** In this case, the prompt might be "Summarize all comments," "Summarize comments from the engineering team," or "Summarize employee recommendations from US employees".
> - Copilot behavior:
>   - Copilot first filters the comments based on the detected filters in the user prompts, perhaps demographic filters, prescriptive comments, or comment sentiments. These filters are in addition to the filters already applied to the report. 
>   - From the filtered comments, Copilot performs stratified sampling up to 8K comments, by either item or topic:
>     - If there is more than one topic with sufficient respondents, Copilot performs stratified sampling by topics. The sample contains comments for different topics in the same ratio as the population.
>     - If there are one or no topics with sufficient respondents of the filtered comments, Copilot performs stratified sampling by survey items. The sample contains comments for different survey items in the same ratio as the population.


## Summarization response 

**Q:Why is there a limit of 8000 comments, and what is the plan to expand this limit?**

**A:** Answer: The 8000 comments limit is due to the context window size limit of our LLM model. This limit may increase as upgrades roll out. Our sampling technique does, however, summarize comment *themes* that represent the top themes from the *entire* comment set. The recommended best practice is to focus on specific items or teams. This filtering reduces the total comment set size.

<br>**Q: Does Copilot recognize words that may have incorrect spelling? Does Copilot recognize similar words, specifically Merck acronyms? Is there a way to edit the acronyms?**

**A:** Copilot relies on the Large Language Model’s (LLM) ability to recognize and understand similar words, acronyms, and even misspelled words, based on the context the words are used in prompts. Currently there isn’t a way for customers to add or adjust acronyms. 

<br>**Q: Do we have the ability to customize sample prompts?**

**A:** This is not currently available.

<br>**Q: Can we compare the comments between a current survey and our last survey cycle?**

**A:** Copilot in Viva Glint doesn’t currently support comparing comments between survey cycles. We are considering this capability on the roadmap.

<br>**Q: Can we compare comments between different organizations, location, job levels, etc.?**

**A:** Copilot in Viva Glint doesn’t currently support comparing comments between employee groups. We are considering this capability on the roadmap. 

<br>**Q: Can the comment summary output pick up themes outside of Viva Glint standard topics?**

**A:** Yes.

<br>**Q: Can we add customized topics?**

**A:** This option isn't currently available.

<br>**Q: A prompt that reads "Tell me more about priorities" returns to no results. But "What do employees say about priorities" returns results. Why?**

**A:** Currently, Copilot in Viva Glint supports a specific set of comment summarization scenarios. To achieve this, our LLM received instructions with sample prompts matching the supported scenarios. These instructions and samples may not encompass all user prompts. If Copilot misinterprets user intent, please provide feedback via the thumb up/down button. Capturing user interactions allows for refinement of Copilot's ability to accurately interpret user intent. 

<br>**Q: Why would an admin user role be unable to receive a response to a question that a lower-level user role can?**

**A:** We use LLM to interpret the user prompt and intent, and because we don't cache the user prompt and Copilot response. Even for the same user prompt on the same comment set, LLM may interpret user intent differently or use different wordings in its response. 

<br>**Q: Does Copilot in Viva Glint learn from our prompts?**

**A:** No, not at this time.

<br>**Q: Why might answers change across the same user role, despite the data remaining the same?**

**A:** Because we don't cache user prompts and responses, the LLM model may use different wordings in its responses. 

<br>**Q: What determines when Copilot responds with...?**

**A:** 
1. **Sorry, I can't help with this."** Reasons for this response might be:
   - When our responsible AI policy is triggered.
   - When Copilot doesn't understand the user prompt
   - When Copilot determines that the user prompt is not related to comments summarization
   - When Copilot can't answer a user's specific request about comments because the LLM model doesn't allow it
   
2.	**An all-comments summary**
    - When the user doesn't ask about specific survey questions or comment themes in the prompt, Copilot summarizes all comments up to the 8K comment limit.
    - Apply filters to the reporting first, and then ask Copilot to "Summarize all comments" as a workaround to ask Copilot to summarize all comments from a specific item.
     
3.	**A subset of comments summary** 
  	- When a user asks about specific survey questions or comment themes.
   > For example, "Summarize comments from the career questions" or "Summarize comments about promotion". Copilot first uses the detected survey question label from the prompt to filter the comments to that item. Then Copilot looks for the most relevant 1000 comments related to the survey item or the comment theme mentioned in the user prompt. Apply filters to the reporting first, and then ask Copilot to "summarize all comments" as a workaround to ask Copilot to summarize all comments from a specific item.
  
<br>**Q: How does the algorithm define Diversity, Equity, and Inclusion-related or sensitive topics/attributes? Is it solely based on our attributes sent to Viva Glint? Is there a key term library?**

**A:** [Read this article about Copilot's responsible AI approach](https://www.microsoft.com/en-us/microsoft-365/blog/2024/02/13/making-our-generative-ai-products-safer-for-consumers/).


## Other resources for Copilot in Viva Glint

All customer-facing documentation is found on Microsoft Viva Glint Learn. [Start here](/viva/glint/copilot/copilot-admin-intro)

[General Copilot in Viva Glint FAQs](/viva/glint/setup/copilot-faqs) 

[Manager Guide](/viva/glint/setup/copilot-manager-quick-guide)

