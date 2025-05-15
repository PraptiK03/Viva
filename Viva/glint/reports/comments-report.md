---
title: Use Viva Glint's Comments report 
description: The Comments report is your window into Viva Glint's Narrative Intelligence technology, which helps managers interpret comment data by highlighting important topic areas, sentiment analysis, and keywords. 
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: representative comments, prescriptive comments, exporting comments, sharing commments, saving comments, choosing benchmark, filtering comments, redacting comments, quarantining comments, narrative intelligence
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: how-to
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 4/21/2025
---

# Use Viva Glint’s Comments report 

The Comments report is your window into Microsoft Viva Glint's Narrative Intelligence technology, which helps managers interpret comment data by highlighting important topic areas, sentiment analysis, and keywords. 
Reviewing comments allows managers to gain further insights into their results. Comments provide helpful context around scores you're exploring. When a comment count is present, select it to view it and interact with Viva Glint’s full Narrative Intelligence experience. Comments are available by demographic group or survey item. 

Read [*Narrative Intelligence:  Enable true understanding of employee feedback*](https://techcommunity.microsoft.com/discussions/results_and_action_taking_on_viva_glint/what-is-viva-glints-narrative-intelligence/3884799) to learn how individual comments are surfaced and calculated.

## Access the Comments dashboard

The Comments report is accessed from the Viva Glint dashboard by selecting the **Reports** tab and then **Comments**.

The Comments report is divided into sections. **Overview** displays by default.

:::image type="content" source="../../media/glint/reports/comments-overview.png" alt-text="Screenshot of Comments Overview default sections."

- **Comments:** Total number of comments, defined by number of commenters and percentage of respondents
- **Comment Sentiment:** A bar graph indicating overall positive, negative, and neutral sentiments
- **Topics:** Topics mentioned most often, including the number of mentions

### View the Questions section
This section can be viewed in grid or table view and includes:
- Top questions by volume
- Top questions by positive sentiment
- Top questions by negative sentiment

### View the Keywords section
This section can also be viewed in keyword or table view. Keywords are words and phrases that occur most frequently across comments. 
- The color of each keyword indicates the aggregated sentiment or favorability of related comments:
	- Blue = positive
	- Grey = neutral
	- Red = negative
- The *size* of a keyword reflects the volume of related comments.
- Hover over a keyword for more information about sentiment or favorability.
- Select a keyword to view all related comments.

### View the Topics section (or Topics cloud)
Topics are a high-level summary of comments, which generate deeper insight. This section may be viewed as a forced, directed view (cloud view), or a table view. 
- The color of a topic bubble indicates the aggregated sentiment or favorability of related comments.
  - Blue = positive
  - Grey = neutral
  - Red = negative
  - Gray lines, connecting bubbles, indicate related topics. The thicker the line, the stronger the relationship.
- The *size* of a topic bubble reflects the volume of related comments.
  
Hover over a topic bubble for more information about sentiment or favorability. Select it to reveal a slider window with all related comments. 

## Incorporate Copilot into your Comments report

Copilot in Viva Glint allows users to explore employee comments with natural language queries or suggested prompts. Copilot in Viva Glint brings the AI revolution into your employee engagement programs. [Read about using Copilot in the Comments report](/../../viva/glint/reports/incorporate-copilot).

## Add sections to the Comments report
In the **Comments** section, you can view all comments or see them by category. 

There are two ways to add sections:
- Select the **+ Add section** button, or
- Use the **More** dropdown menu and choose **+ Add Section**

Select sections by scrolling through the tabs in the slider window. Add or delete sections at any time. 
- Select the **+ button** to add the section.
- If a **right-facing arrow** displays, choose it to filter by attributes. Then select **Add**.

## Prescriptive and representative comments

Viva Glint suggests using both prescriptive and representative comments when reviewing your Comments report.

- **Prescriptive comments** are identified by **Narrative Intelligence**, which offers specific actionable suggestions for improvement in a Focus Area. You can access deep insights from Narrative Intelligence. Continuous listening as part of ongoing conversations, and developing Focus Areas with your teams lead to identifying the most appropriate actions to improve employee engagement and business goals.

- **Representative Comments** represent overall themes are isolated and shown together. You only need to read a few to get a sense of the whole.

## Redact and quarantine comments

You may redact terms flagged as Personally Identifiable Information (PII) or as profanity:
- Select **Redact All Terms** to replace all PII and profanity with five-pound signs (#####).
- Select **Un-Redact All** to replace ##### with the original comments.
- Use the **vertical ellipses** next to an individual comment to select **Redact** or **Un-Redact**.

To redact or quarantine, follow this process:
1. Select the **ellipses** next to the comment. 
2. By selecting **Quarantine**, the comment is visible only to admins with **Manage Sensitive Comments** capability. Comments may be unquarantined. 

> [!IMPORTANT]
> See [Flag sensitive comments in Viva Glint](/viva/glint/setup/glint-sensitive-comments) for a deeper dive into this information.
 
## Mixed Comments analysis

Our platform classifies every comment as positive, negative, neutral, or mixed. *Mixed* indicates both positive and negative sentiment in the same comment. From this data, a histogram of "red", "grey", and "blue" is generated. 
- A negative comment is red.
- A positive comment is blue.
- A neutral comment is grey.
- *Mixed comments* count as half of a blue and half of a red comment. 

## Export, save, or share from the Comments report

Selecting this dropdown menu allows you to perform multiple functions: Export report to PowerPoint, Export report to PDF, Export report to spreadsheet, Export report to Images, Export Comments to XLSX Spreadsheet, Save, Save As, and Share.

>[!NOTE]
> Managers with multinational teams can export and read all comments in their preferred languages offline, to easily dig deeper into the comments. For Comment reports generated in less than ten seconds, the file downloads automatically in a browser. Reports that require a longer generation, send an email link to the user to inform them that the file is ready to download.

## Best Practices for Using Comments
 
- Optimize survey design: Limit the number of items presented per survey and focus on topics. The comments section of each item allows employees to provide detail, color, explanation, and nuance to their answers. From comment summarization, analytics can mine deep insights.  
- Explore comments **after** reviewing scores 
- Consider related topics: Review how topics connect to each other in the bubble visualization for a new way to gain a deeper understanding of the intention. 
- Take action from Prescriptive Comments
- Beware of comment bias: It's natural to take comments personally, however, resist the urge. Survey comments tend to be more negative than positive. 
- Explore different populations: Filter by different attributes to see what your key populations are talking about. 
- Review keywords
- Explore Representative Comments: Viva Glint isolates a short list of comments that are representative of overall themes. Read just a few to get a sense of the whole.



 
