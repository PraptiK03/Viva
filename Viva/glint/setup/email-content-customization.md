---
title: Customize Viva Glint survey email content
description: Customize Microsoft Viva Glint email content for survey invites, reminders, and survey results notifications in the Communications section of Program Setup.
ms.author: aweixelman
author: AliciaWeixelman
manager: mbarry
audience: admin
f1.keywords: NOCSH
keywords: email, reminder, invite, custom email, results notification, email communications for approved programs
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: how-to
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 04/18/2025
---

# Customize Viva Glint survey email content

Customize Microsoft Viva Glint email content for survey invites, reminders, and survey results notifications in the Communications section of Program Setup. Optionally, set up a custom email sending domain and a company logo for survey emails. To understand how to enable/disable emails, and for more information about Communications setup, see [Communications setup in Program Summary](program-summary-communications.md).

> [!IMPORTANT]
> Always-On survey programs don't have a Communications section for setup.

## Custom sending domains and branding (optional)

Your Microsoft 365 global admin can configure a custom sending domain for your organization in the [Microsoft 365 admin center](https://go.microsoft.com/fwlink/?linkid=2264234). Choose from different survey email branding options in the Microsoft Entra admin center or Viva Glint app. Both are optional steps to further customize communications for your organization.

- [Set up a custom sending domain in the Microsoft 365 admin center](/microsoft-365/admin/email/select-domain-to-use-for-email-from-microsoft-365-products)
- **Custom branding options:**
  - In [Microsoft Entra admin center](https://entra.microsoft.com): To [add your organization's logo](/entra/fundamentals/how-to-customize-branding) to Viva Glint survey emails, set up the **Sign-in form** > **Banner logo.** 
  - In the Viva Glint app: Go to **General settings** to manage [Custom branding](custom-branding.md).

> [!NOTE]
> - Custom sending domains configured in the Microsoft 365 admin center can impact other Microsoft 365 products. See [Set up a custom sending domain](/microsoft-365/admin/email/select-domain-to-use-for-email-from-microsoft-365-products) for a full list.
> - Viva Glint teams have access to limited email delivery metrics. Using a custom sender domain gives your organization direct access to your email delivery data.
> - [Send an email preview](#preview-emails) to see your organization's customized logo. The preview in the email setup pane in the platform always displays the Viva Glint logo. 

## Email sections

To edit email content, go to the **Communications** section of **Program Summary** in your desired survey program. Select the **pencil icon** to edit a communication. In the edit panel that appears, select the **pencil icon** to edit content. Viva Glint survey invites and reminders contain multiple editable sections:

:::image type="content" source="../../media/glint/setup/glint-email-invite-sections.png" alt-text="Screenshot of editable survey email sections in Viva Glint.":::

Add your customizations to each section and select **Save Changes**.

> [!CAUTION]
> - Hyperlinks and HTML aren't supported content in Viva Glint customized emails. These items can cause email delivery or blocking issues.
> - Viva Glint Admins can add links as plain text; for example: `www.microsoft.com`.
>   - Some versions of Microsoft Outlook automatically convert a plain text link into a clickable link. To prevent creating issues with links, ensure that the plain text URL is less than or equal to 100 characters, or create a shortened link.

### Email macros

Macros in Viva Glint emails allow your organization to add placeholders that pull in information from your employee data and from Viva Glint. Customize your message by including Departments, Manager Names, or the estimated to complete a survey in email. To add a macro, select the **plus sign icon** in each email sections and choose a macro from the dropdown menu.

:::image type="content" source="../../media/glint/setup/glint-email-macros.png" alt-text="Screenshot of macros available to add to email text.":::

## Manage language translations

Any edits made to email text in English need to be made to all other survey languages.

In the email edit panel, after customizing English content, use the **Language** dropdown menu to select other survey languages and add translations to each survey section. Select **Save Changes** in the top right to save all of your edits.

:::image type="content" source="../../media/glint/setup/glint-email-language-dropdown.png" alt-text="Screenshot of the Language dropdown in the email edit pane.":::

### Use the program content import

Use this [translation guidance](language-translations.md) to import updated translations for emails after modifying English text.

## Survey End Results Notification email

The Survey End Results Notification email is designed to notify managers that their results are ready for review in Viva Glint dashboards. It contains several sections, including some that link to more resources. 

Sections that can be easily customized: Button Text, Greeting, Main Title, Preview Text, Subject Title, Tip Titles, Tip Descriptions

**Avoid customizing links and icons**.

These results notification email sections support multiple paragraphs to break up and emphasize important text:
- Description
- Main Title
- Tip 1 Description
- Tip 2 Description
- Tip 3 Description

:::image type="content" source="../../media/glint/setup/glint-survey-results-notification.png" alt-text="Screenshot of the Survey End Results Notification email.":::

## Preview emails

After customizing emails, use the Viva Glint [preview option](preview-manage-enable-engage-programs.md) to send yourself a sample of the survey invite email.

> [!TIP]
> For email previews in other languages, select a User Role to **Preview As** who uses assigned the language code that you want to see. Learn more in the **Language** section in [Viva Glint employee attribute fundamentals](attribute-fundamentals.md).

### Preview email communications for Approved cycles

Admins can easily send preview communications from an Approved program cycle. Any communication set up on the Communications page in Program Summary can be viewed.

1. From your admin dashboard, select **Survey Programs**.
2. On the **Survey Programs** page, select the survey program you want to review communications for.
3. In the **Upcoming and Live** tab on the survey program page, select a cycle and then use the ellipses to display the dropdown menu. Select **Preview**.

> [!IMPORTANT]
> A survey must be in **Approved** status for it to be listed as Upcoming or Live.

   :::image type="content" source="../../media/glint/setup/preview-email-steps.png" alt-text="Screenshot of how to preview email communications from Upcoming and Live cycles.":::

1. In the Select Preview for [Survey Name] window that opens, select from **Survey Start**, **Survey Reminders**, **Survey End** to define which previews to send.
2. In the **Select a Recipient** box, search for your name or whoever you want to send the previews to.

   :::image type="content" source="../../media/glint/setup/comms-preview-selection.png" alt-text="Screenshot of how to choose and send email previews.":::

   Example email preview:

   :::image type="content" source="../../media/glint/setup/example-email-preview.png" alt-text="Screenshot of an example preview email.":::


> [!NOTE]
> To allow for easier email review, previews for surveys that require authentication via Entra don't include an Entra link behind the Provide Feedback button.
