---
title: Add custom branding for your organization in the Viva Glint app
description: Use custom branding to apply a unique dashboard and survey experience for your organization.
ms.author: aweixelman
author: AliciaWeixelman
manager: melissabarry
audience: admin
f1.keywords: NOCSH
keywords:  multiple Viva Glint experiences, custom branding
ms.collection:  
- m365initiative-viva
- selfserve 
search.appverid: MET150 
ms.topic: how-to
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 04/11/2025
---

# Add custom branding for your organization in the Viva Glint app

Use custom branding to apply a unique dashboard and survey experience for your organization. Custom branding that Viva Glint Administrators add in Microsoft Viva Glint overrides any [custom themes](/microsoft-365/admin/setup/customize-your-organization-theme) your organization sets up in the Microsoft 365 admin center. If there’s no custom theme set up in the Microsoft 365 admin center or in the Viva Glint app, the app uses standard Viva Glint branding.

To add custom branding:

1. From the admin dashboard for your organization, select **Configuration** and in **Service Configuration**, choose **General Settings**.
2. In the **Company Information** section, go to **Custom Branding** and select **Manage custom branding**.

   :::image type="content" source="../../media/glint/setup/manage-branding.png" alt-text="Screenshot of the Viva Glint custom branding management section in General Settings.":::

3. In the **Custom Branding** pane that appears:
   1. Switch the **Use custom branding** toggle to **On**.
   2. In the **Logo options** section, update the following fields.
      1. **Custom logo**: Add your logo, which must be .jpg, .jpeg, or transparent .png file and less than or equal to 10 kilobytes.
      1. **Use custom logo in live survey header**:
         - Select the checkbox to display your company's logo in the survey header for survey takers.
         - Clear the checkbox to display the Viva Glint logo in the survey header for survey takers.
      1. **Target URL:** Optionally, add a link that directs users to a specified site or page when they select your custom logo.
         - If blank, the target URL in your organization’s [custom theme](/microsoft-365/admin/setup/customize-your-organization-theme) in the Microsoft 365 admin center is used.
         - If your organization doesn’t have a target URL specified in a custom theme, the logo directs users to the Office 365 homepage.
   3. In the Color options section, update and view the following fields.
      1. **Navigation bar color:** Add a hex color code for the background color of the navigation bar that appears at the top of the platform for dashboard users and Viva Glint Admins.
      2. **Text and icon color:** Add a hex color code for the text and icons that appear on the navigation bar that appears at the top of the platform for dashboard users and Viva Glint Admins.
      3. **Accent color:** Add a hex color code for accent buttons, links, and other elements in the platform.
      4. **Preview:** Use the preview displayed to see how your selected colors appear in Viva Glint.
      5. **Reset colors to default:** Select this option to revert to your organization’s [custom theme](/microsoft-365/admin/setup/customize-your-organization-theme) in the Microsoft 365 admin center.
         
         :::image type="content" source="../../media/glint/setup/custom-brand-pane-setup.png" alt-text="Screenshot of the Viva Glint custom branding edit pane with all settings complete.":::

> [!NOTE]
> Keep [usability standards](/windows/apps/design/signature-experiences/color#usability) related to contrast, lighting, and color blindness in mind when adding custom branding. Warnings display when the minimum color contrast ratio (`4:5:1`) isn’t met.

## Custom branding examples

Review Contoso's custom branding examples for their survey header, dashboard navigation bar, and survey email.

### Survey header

:::image type="content" source="../../media/glint/setup/custom-brand-survey.png" alt-text="Screenshot of a Viva Glint custom branded survey header.":::

### Navigation bar

:::image type="content" source="../../media/custom-nav-menu.png" alt-text="Screenshot of a Viva Glint custom branded navigation bar with a company logo.":::

### Survey email

:::image type="content" source="../../media/glint/setup/custom-brand-invite.png" alt-text="Screenshot of a Viva Glint email with a custom branded logo.":::

