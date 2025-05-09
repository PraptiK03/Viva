---
title: Link custom questions to Viva Glint benchmarks
description: As a Microsoft Viva Glint Administrator, associate custom questions with Glint benchmark suites so that users still have a point of comparison in reporting.
ms.author: aweixelman
author: AliciaWeixelman
manager: melissabarry
audience: admin
f1.keywords: NOCSH
keywords: benchmark mapping, benchmark linking, custom benchmark, question benchmark, map question, custom question
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: how-to
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 02/21/2025
---

# Link custom questions to Viva Glint benchmarks

As a Microsoft Viva Glint Administrator, associate custom questions with Viva Glint benchmark suites so that users still have a point of comparison in reporting.

## Question edits and mapping guidelines

To map custom questions to a Viva Glint benchmark suite, the question should be comparable to the Viva Glint standard version that carries a benchmark. For a custom question or edited duplicate of a Viva Glint standard question, always consider whether the question shares:

- Intent: the purpose and outcome.
- Referent: the subject of the question.

> [!IMPORTANT]
> Mapping Viva Glint standard question benchmarks to custom questions that don't share intent and referent isn't recommended. Learn more and review examples: [Question mapping](question-mapping.md).

## Link a question to a benchmark suite

Viva Glint Admins can map custom survey questions to benchmarks from the Question Library or from the Questions section of a survey program. Link custom or duplicated standard questions to benchmark suites.

> [!CAUTION]
> To pull the correct benchmark information into reports, [reapprove](preview-manage-enable-engage-programs.md#approve-a-program) all survey programs that use the question with an added or updated benchmark mapping. To view which survey programs use a question, go to the **Question Library**, select the question, and select the **Associated Programs tab**.

### Link a question in the Question Library

> [!NOTE]
> Organizations migrating from LinkedIn Glint to Viva Glint may see manually added benchmark values for custom questions and see a **Benchmark** warning tag. Use these steps to link eligible custom questions to Viva Glint standard question benchmarks to use automatic benchmarking.

To map a custom question to a benchmark suite in the Question Library:

1. Select **Configuration** from the admin dashboard and choose **Question Library** in the **Surveys** section.
2. For users in a migrated organization: 
    1. At the top of the page, a banner indicates how many questions aren't associated with a benchmark. Switch on the **Show only warnings** setting to filter to these questions.
    2. Select a question with the **Benchmark** warning tag.
3. Go to the **Benchmark** field (for migrated or nonmigrated organizations) in the question edit pane that appears.
4. Search for and select a Viva Glint standard question to apply its benchmark to your comparable, custom question.
5. Select **Save Changes** at the top of the edit pane.
  
   :::image type="content" source="../../media/glint/setup/question-lib-benchmark-warning.png" alt-text="Screenshot of the Question Library with a custom question flagged for benchmark mapping.":::

#### View benchmarks for a question

To view which benchmarks have a score available for a Viva Glint question:

1. Select **Configuration** from the admin dashboard and choose **Question Library** in the **Surveys** section.
2. Select a Viva Glint question.
3. Go to the **Benchmark** field in the edit pane that appears, 
4. Select the "x of y external benchmarks" link to view which benchmark suites have scores available for the question.
5. Select the "x custom questions" link to view which custom questions use the associated benchmarks.
  
   :::image type="content" source="../../media/glint/setup/view-benchmark-info.png" alt-text="Screenshot of benchmark information options available at the question level.":::

   > [!NOTE]
   > Benchmark suites in the "x of y external benchmarks" dialog are based on [external benchmark suites selected in General Settings](opting-into-external-benchmarks.md#selecting-external-benchmarks-after-admin-consent).

### Link a question in Program Setup

To map an existing custom question to a benchmark in the **Questions** section of a survey:

1. Select **Configuration** from the admin dashboard and then in Surveys, choose a survey.
2. Go to the **Questions** section of Program Summary and select a question.
3. Go to the **Benchmark** field in the question edit pane that appears.
4. Search for and select a Viva Glint standard question to apply its benchmark to your comparable, custom question.
5. Select **Save Changes** at the top of the edit pane.

### Link a duplicated question

To map a duplicated question to the original Viva Glint standard question in the Question Library or in a survey:

1. Select a question and choose the **Duplicate Question** option in the edit pane that appears.
2. Select an option in the benchmark associations dialog that appears:
    1. Yes, keep any inherited benchmarks, to keep benchmarks from the copied standard question, or
    2. No, remove all inherited benchmarks, to discard benchmark information when edits are made that change the question's meaning.
3. Select **Duplicate this question** in the dialog.

> [!NOTE]
> Mapping a copied question to a Viva Glint standard question only links it to external benchmark suites and doesn't map any internal benchmarks or trend from Viva Glint standard questions.
  
   :::image type="content" source="../../media/glint/setup/benchmark-association-dialog.png" alt-text="Screenshot of the dialog that appears to give the option to map or discard benchmark suites for copied questions.":::
