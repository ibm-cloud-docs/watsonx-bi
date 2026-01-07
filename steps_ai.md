---
copyright:
  years: 2024
lastupdated: "2026-01-07"

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

# Steps taken by AI to respond
{: #steps_ai}

For each response generated in {{site.data.keyword.wxbia_short}}, you can view the steps the AI has taken to understand and answer your question. You can view the progress of these steps in real-time while the AI is working on your query. {: #shortdesc}

This feature not only identfies the data source chosen and query generated to answer your question but also allows you to confirm that the AI understood your query accurately. If you notice that the AI did not understand your query, you can stop the response generation process without waiting for {{site.data.keyword.wxbia_short}} to complete the steps and try rephrasing your question. 

During response generation, expand the **Generating response** dropdown to view the progress of the steps and details in each completed step. After a response has been generated, you can expand **Show AI steps** under any response to see a step-by-step explanation.

## Step 1: Interpretation
{: #interpretation}

In the first step, the AI analyzes your question, interprets it, and rephrases it, if necessary. If you're in a conversation already, AI considers the context of the previous question. 

## Step 2: Finding data source
{: #find_datasrc}

The AI finds and matches the data in your question to your enriched business data (such as column names, measures, or filters). Once a data source is found, you can see the data asset name and can access it from the given link. 

You can also see the measures and columns that were identified and used to answer your question. 

### Using other data assets
{: #change_data_asset}

When the AI finds other data assets that might be able to answer your question, an **Edit** icon becomes available next to the data asset name that allows you to choose a different data asset. 

You cannot choose a different data asset if your original question was a suggested question.
{: note}

Select a different data asset and click **Ask again**. AI answers the same question that you asked before but uses the new data asset to answer your question. 

To avoid getting unexpected results, select a data asset that aligns with the topic of your question. For example, if you asked about sales but select a data asset that only has HR-related data, you might get an inaccurate response. 
{: tip}

## Step 3: Query generation
{: #query_gen}

AI then generates a query that can help it find the most useful and accurate answer. You can view the generated query in this step and check for accuracy. 

You can also see the measures and columns that were used to generate the query to answer your question.

### Using other measures and columns
{: #change_measure_colmn}

When AI finds other measures and columns that might be able to answer your question, an **Edit** icon is available next to **Data referenced**. Click the **Edit** icon to explore other angles of your data.

You cannot choose different measures and columns if your original question was a suggested question.
{: note}

The measures and columns that were used to answer your question are listed in a table and automatically selected. Other measures and columns that are available to answer your question are also listed in the table. Data that has a background color:

- Green - means that these measures and columns are a close match to the data in your question 

- Blue -  means that these measures and columns were considered to answer your question

- White - means that these measures and columns were ignored and not considered to answer your question 

To change the measures and columns and ask your question again:

1. Deselect the ones that are automatically selected.

2. Select new measures and columns and click **Ask again**.

To avoid getting unexpected results, select measures and columns that align with the topic of your question. Let's say you asked about Revenue for Canada and {{site.data.keyword.wxbia_short}} chose the measure Revenue and column Country to answer your question. If you choose Expenses as a measure and Product color as a column instead, the response might not be aligned with the question you asked. 
{: tip}

## Step 4: Response generation
{: #resp_gen}

Based on the query, AI then generates a response in natural language. This can be either in text format or a visualization. 
