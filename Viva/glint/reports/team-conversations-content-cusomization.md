---
title: Customize Microsoft Viva Glint Team Conversations email content
description: Customize Microsoft Viva Glint email content for Team Conversations introductory messages and reminders in the Communications section of Program Setup.
ms.author: aweixelman
author: AliciaWeixelman
manager: mbarry
audience: admin
f1.keywords: NOCSH
keywords: start email, reminder, team conversations
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: how-to
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 05/13/2025
---

# Customize Microsoft Viva Glint Team Conversations email content

Customize Microsoft Viva Glint email content for Team Conversations introductory messages and reminders in the **Communications** section of **Program Summary**. Optionally, set up a custom email sending domain and a company logo for emails. For more information about Team Conversations setup and emails, see [Admin setup for Viva Glint Team Conversations](team-conversations-administrator-setup.md).

## Custom sending domains and branding (optional)

Your Microsoft 365 global admin can configure a custom sending domain for your organization in the [Microsoft 365 admin center](https://go.microsoft.com/fwlink/?linkid=2264234). Choose from different email branding options in the Microsoft Entra admin center or Viva Glint app. Both are optional steps to further customize communications for your organization.

- [Set up a custom sending domain in the Microsoft 365 admin center](/microsoft-365/admin/email/select-domain-to-use-for-email-from-microsoft-365-products)
- **Custom branding options:**
  - In [Microsoft Entra admin center](https://entra.microsoft.com): To [add your organization's logo](/entra/fundamentals/how-to-customize-branding) to Viva Glint survey emails, set up the **Sign-in form** > **Banner logo.** 
  - In the Viva Glint app: Go to **General settings** to manage [Custom branding](/viva/glint/setup/custom-branding).

> [!NOTE]
> - Custom sending domains configured in the Microsoft 365 admin center can impact other Microsoft 365 products. See [Set up a custom sending domain](/microsoft-365/admin/email/select-domain-to-use-for-email-from-microsoft-365-products) for a full list.
> - Viva Glint teams have access to limited email delivery metrics. Using a custom sender domain gives your organization direct access to your email delivery data.

## Email sections

To edit email content, go to the **Communications** section of your desired survey program. Select the **pencil icon** to edit a given Team Conversations email. In the edit panel that appears, select the **pencil icon** to edit content.

Viva Glint Conversation Start, reminders, and summary notifications contain multiple editable sections:

:::image type="content" source="../../media/glint/setup/glint-tc-sections.png" alt-text="Screenshot of editable Team Conversations start email sections in Viva Glint.":::

Add your customizations to each section and select **Save Changes** to save all of your edits.

> [!NOTE]
> The Body Text section of Team Conversations emails supports multiple paragraphs to break up and emphasize important messages.

> [!CAUTION]
> Hyperlinks and HTML aren't supported content in Viva Glint customized emails. These items can cause email delivery or blocking issues.

### Email macros

Macros in Viva Glint emails allow your organization to add placeholders that pull in information from your employee data and from Viva Glint. Include Departments, Manager Names, or other Team Conversations information to further customize for your managers. To add a macro, select the **plus sign icon** in email sections and choose a macro from the dropdown menu.

:::image type="content" source="../../media/glint/setup/glint-tc-macros.png" alt-text="Screenshot of macros available to add to Team Conversation email text.":::

## Manage language translations

Any edits made to email text in English need to be made to all other survey languages. Use this guidance to manage Team Conversations email translations:

### Use the program content import

Use this [translation guidance](/viva/glint/setup/language-translations) to import updated translations for emails after modifying English text.

### Use the language dropdown

In the email edit pane, after customizing English content, use the **Language** dropdown menu to select other survey languages and add translations to each section. Select **Save Changes** in the top right to save all of your edits.

:::image type="content" source="../../media/glint/setup/glint-email-language-dropdown.png" alt-text="Screenshot of the Language dropdown in the email edit pane.":::

>[!IMPORTANT]
>Unlike for *invite* and *reminder* emails, it's not possible to use a dual language template for the **results notification email.** For creating results notification emails in dual languages, all languages must be added to the email body section individually and saved. 
