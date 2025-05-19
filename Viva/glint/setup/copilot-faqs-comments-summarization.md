---
title:  Microsoft 365 Copilot in Viva Glint FAQs for comments summarization
description: Find answers to your specific inquiries about comments summarization and prompts for Copilot in Viva Glint.
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: comment summarization, filtering comments summarization, Copilot in Viva Glint, responsible AI, FAQ
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
ms.date: 05/19/2025
---

# Microsoft 365 Copilot in Viva Glint FAQs for comments summarization

> [!NOTE]
> Not all items in the Microsoft Viva Glint Question Library are posed in question format. Question Library items can be statements for the survey taker to rate on a given scale. For this reason, the term "item" is used to refer to all contents of the Viva Glint Question Library.

## Filtering 

**Q: How can we distinguish between item labels and customized topics? What is a good practice for applying filters such as groups, topics, and question labels?** <br>
**A:** Item labels and topics can sometimes be indistinguishable. For example, the "Inclusion" survey *item* versus the *general topic* of inclusion. Copilot in Viva Glint initially identifies item labels in the user prompt and filters comments based on those labels. After Copilot summarizes comments that closely align with the topics identified in the user prompt, it filters comments about inclusion as a topic.

**Q: Can Copilot in Viva Glint summarize comments for attributes that a user doesn’t have access to?** <br>
**A:** No, Copilot in Viva Glint can’t filter or summarize comments based on attributes that a user can’t access.

**Q: When does Copilot in Viva Glint use all comments in its summarization? When does Copilot in Viva Glint summarize by a topic-based sampling? How is the sample size determined?** <br>
**A:** Use these examples to understand summarization analytics:

- **Scenario 1: The user asks about specific survey item labels or comment topics.** In this case, the prompt might be "Summarize comments from the career and empowerment items" or "Summarize comments about promotion." **Copilot in Viva Glint behavior:** In addition to any filters applied to the report, Copilot first filters comments based on the detected survey item labels from the user prompt. Next, Copilot looks for comments with words most closely related to the survey item or the comment topic in the user prompt.
- **Scenario 2: The user doesn't include specific survey item labels or comment topics in the prompts.** In this case, the prompt might be "Summarize all comments," "Summarize comments from the engineering team," or "Summarize employee recommendations from US employees." **Copilot in Viva Glint behavior:** Copilot first filters the comments based on the detected filters in the user prompts, such as demographic filters, prescriptive comments, or comment sentiments. These filters are in addition to the filters already applied to the report.

## Summarization response 

**Q: Why is there a limit of 8000 comments, and what is the plan to expand this limit?** <br>
**A:** The 8,000-comments limit is due to the context window size limit of our large language model (LLM). This limit may increase as upgrades roll out. Our sampling technique does, however, summarize comment themes that represent the top themes from the entire comment set. We recommend focusing on specific items or teams. This filtering reduces the total comment set size.

**Q: Why does my Copilot in Viva Glint summary sometimes show fewer than the maximum limit of 8,000 comments, even when my survey comments for a topic far exceed 8,000?** <br>
**A:** The capacity to process up to 8,000 comments was estimated based on an average comment length within a relevant timeframe. However, the actual amount of data included is constrained by the text processing limit of the AI system. Since comment lengths vary, fewer comments may fit within this limit. 

**How comments are selected:**

- Initially, comments most relevant to each topic are identified. 
- Subsequently, a number of comments from each topic are chosen based on the total comments for that topic. 
- As many comments pertain to multiple topics, the largest topic group tends to approximate the total number of comments displayed. 

**Q: What determines when Copilot in Viva Glint responds with…**

**“Sorry, I can't help with this."** Reasons for this response might be:
- When our [responsible AI policy](https://www.microsoft.com/ai/responsible-ai?ef_id=_k_2b3ce813d8b01157997a803234c87cf3_k_&OCID=AIDcmm1o1fzy5i_SEM__k_2b3ce813d8b01157997a803234c87cf3_k_&msclkid=2b3ce813d8b01157997a803234c87cf3) is triggered
- When Copilot doesn't understand the user prompt
- When Copilot determines that the user prompt is not related to comments summarization

**An “all-comments” summary:**
- When the user doesn't ask about specific survey questions or comment themes in the prompt, Copilot summarizes all comments up to the 8,000 comment limit.
- Apply filters to the reporting first and then ask Copilot to "Summarize all comments" as a workaround.

**A subset of comments summary:**
- A user asks about specific survey questions or comment themes.<br><br>
  For example, "Summarize comments from the career questions" or "Summarize comments about promotion":
  - Copilot first uses the detected survey question label to filter the comments to that item. Then, Copilot looks for the most relevant 1,000 comments related to the item, or the theme mentioned in the user prompt. 
  - We recommend that you apply filters to the report first. Then ask Copilot to "summarize all comments," as a workaround to ask Copilot to summarize all comments from a specific item.

**Q: Does Copilot in Viva Glint recognize words that may have incorrect spelling? Does Copilot in Viva Glint recognize similar words or acronyms? Is there a way to edit acronyms?** <br>
A: Copilot in Viva Glint relies on the Large Language Model (LLM) ability to recognize and understand similar words, acronyms, and misspelled words, based on the context the words are used in prompts. Currently there isn’t a way for customers to add or adjust acronyms.

**Q: Do we have the ability to customize sample prompts?** <br>
A: This capability is not currently available.

**Q: Can we compare the comments between a current survey and a past survey cycle?** <br>
A: Copilot in Viva Glint doesn’t currently support comparing comments between survey cycles. We're considering this capability on the roadmap.

**Q: Can we compare comments between different organizations, locations, job levels, etc.?** <br>
A: Copilot in Viva Glint doesn’t currently support comparing comments between employee groups. We're considering this capability on the roadmap.

**Q: Can the comment summary output pick up themes outside of Viva Glint standard topics?** <br>
A: Yes.

**Q: If I ask Copilot in Viva Glint for key topics, does it use the same topic model as Viva Glint today? If not, what does it train on?** <br>
A: Copilot in Viva Glint uses the same topic model as Viva Glint today and summarizes up to 10 top topics found in survey comments. If the user doesn’t specify the number of topics in the prompt, Copilot defaults to showing up to five topics in the response. Topics with comment respondents that fall below the confidentiality threshold are excluded. When there are only one or no Viva Glint topics with sufficient comment respondents, Copilot summarizes all the comments, and the LLM may highlight top themes from the comments that fall outside of Glint’s topic models. Glint topics show the percentage of comments, while LLM themes won’t.

**Q: Can we add customized topics?** <br>
A: This option isn't currently available.

**Q: A prompt that reads "Tell me more about priorities" returns no results. But "What do employees say about priorities?" returns results. Why?** <br>
A: Copilot in Viva Glint supports a specific set of comment summarization scenarios. To achieve this, our LLM received instructions with sample prompts matching the supported scenarios. These instructions and samples may not encompass all user prompts. If Copilot misinterprets your intent, provide feedback by using the thumb up/down feedback button. Alerting us to user interactions allows for refinement of Copilot's ability to accurately interpret user intent.

**Q: Why would an admin user role be unable to receive a response to a question that a lower-level user role can receive?** <br>
A: We use LLM to interpret the user prompt and intent and don't cache the user prompt and Copilot response. Even for the same user prompt on the same comment set, LLM may interpret user intent differently or use different wordings in its response.

**Q: Does Copilot in Viva Glint learn from our prompts?** <br>
A: No, not at this time.

**Q: Why might answers change across the same user role, despite the data remaining the same?** <br>
A: The LLM model may use different wordings in its response because we don’t cache user prompts and responses.

**Q: Can Copilot in Viva Glint generate a PowerPoint from the results?** <br>
A: Not yet, but it’s another feature we'd like to explore.

**Q: How does Copilot work with the sensitive comments flagging feature?** <br>
A: Quarantined comments are excluded from Copilot’s comment summarization. Copilot can summarize redacted comments, but the redacted words are excluded from Copilot’s summary. 

## Other resources for Copilot in Viva Glint

All customer-facing documentation is found on Microsoft Viva Glint Learn. [Start here](/viva/glint/copilot/copilot-admin-intro)

[General Copilot in Viva Glint FAQs](/viva/glint/setup/copilot-faqs) 

[Manager Guide](/viva/glint/setup/copilot-manager-quick-guide)

