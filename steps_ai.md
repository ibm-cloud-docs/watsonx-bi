---
copyright:
  years: 2024
lastupdated: "2026-01-19"

keywords:
subcollection: watsonx-bi



---

{:codeblock: .codeblock}
{:note: .note}
{:pre: .pre}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:table: .aria-labeledby="caption"}
{:tip: .tip}
{:video: .video}
{:external: target="_blank" .external}
{:step: data-tutorial-type='step'}

# Steps AI takes to respond
{: #steps_ai}

For each response generated in {{site.data.keyword.wxbia_short}}, you can view the steps the AI has taken to understand and answer your question. You can view the progress of these steps in real-time while the AI is working on your query. {: #shortdesc}

This feature not only identfies the data source chosen and query generated to answer your question but also allows you to confirm that the AI understood your query accurately. If you notice that the AI did not understand your query, you can stop the response generation process without waiting for {{site.data.keyword.wxbia_short}} to complete the steps and try rephrasing your question. 

During response generation, expand the **Generating response** dropdown to view the progress of the steps and details in each completed step. After a response has been generated, you can expand **Show AI steps** for any response to see a step-by-step explanation.

## Step 1: Interpretation
{: #interpretation}

In the first step, the AI analyzes your question, interprets it, and rephrases it, if necessary. If you're in a conversation already, AI considers the context of the previous question. 

## Step 2: Finding data source
{: #find_datasrc}

The AI finds and matches the data in your question to your enriched business data (such as column names, measures, or filters). Once the relevant data source is found, you can view the associated data asset name and access it through the provided link. As part of this process, the AI also extracts key search terms from your question to improve the accuracy of the match.

You can also see the specific measures and columns that were identified and used to generate the answer to your question.

### Using other data assets
{: #change_data_asset}

When the AI identifies additional data assets that might be able to answer your question, an **Edit** icon becomes available next to the data asset name. This option allows you to choose a different data asset, if needed. 

You cannot choose a different data asset if your original question was a suggested question.
{: note}

To use another data asset, click the **Edit** icon, select the new data asset, and click **Ask again**. The AI answers the same question that you asked before but uses the new data asset to generate a response 

To avoid getting unexpected results, select a data asset that aligns with the topic of your question. For example, if you asked about sales but select a data asset that only has HR-related data, you might get an inaccurate response. 
{: tip}

## Step 3: Query generation
{: #query_gen}

AI then generates a query to retrieve the most useful and accurate answer by using the following inputs:

- The rephrased question and extracted key terms

- Column labels, column descriptions, sample values in metrics, and enriched metadata

- Asset labels and asset descriptions

- General instructions

- SQL examples

You can review the generated query in this step to verify its accuracy.

You can also view the specific measures and columns that were identified and used to generate the query for your question.

### Using other measures and columns
{: #change_measure_colmn}

When AI finds additional measures and columns that might help answer your question, an **Edit** icon is available next to **Data referenced**. Click this icon to explore other angles of your data.

You cannot choose different measures and columns if your original question was a suggested question.
{: note}

The measures and columns used to answer your question appear in a table and are automatically selected. Additional measures and columns that could also be used are listed in the same table. Their background colors indicate how they were evaluated:

- **Green** - Close match to the data in your question 

- **Blue** -  Considered by the AI to answer your question but not selected

- **White** - Ignored by the AI and not considered to answer your question 

To change the measures and columns and ask your question again:

1. Deselect the ones that are automatically selected.

2. Select new measures and columns and click **Ask again**.

To avoid getting unexpected results, select measures and columns that align with the topic of your question. Let's say you asked about Revenue for Canada and {{site.data.keyword.wxbia_short}} chose the measure Revenue and column Country to answer your question. If you choose Expenses as a measure and Product color as a column instead, the response might not be aligned with the question you asked. 
{: tip}

## Step 4: Response generation
{: #resp_gen}

Based on the generated query, the AI produces a natural‑language response, which can appear as text, a visualization, or both.
