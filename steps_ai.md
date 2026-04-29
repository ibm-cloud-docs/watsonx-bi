---
copyright:
  years: 2024, 2025, 2026
lastupdated: "2026-04-29"

keywords: AI steps, explanation, reasoning
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

For each response generated in {{site.data.keyword.wxbia_short}}, you can view the steps the AI has taken to understand and answer your question. You can also view the progress of these steps in real-time while the AI is working on your query. {: #shortdesc}

This feature not only identfies the data source chosen and query generated to answer your question but also allows you to confirm that the AI understood your query accurately. If you notice that the AI did not understand your query, you can stop the response generation process without waiting for {{site.data.keyword.wxbia_short}} to complete the steps and try rephrasing your question. 

## AI steps
{: #response_steps}

When a response is generating in {{site.data.keyword.wxbia_short}}, you can view the reasoning steps that are in progress. You can also click **Reasoning...** to view more details about how AI is deriving the answer. 

After the response is generated, you can view the reasoning steps and explanation by clicking **Show AI steps**. 

Depending on the large language model (LLM) selected by your organization, reasoning steps and explanation can include: 

- An interpretation of the question and how the LLM decided to answer. 

- The data source that the AI chose to answer the question. The LLM picks the best asset it thinks can answer the question, but the option is available to select an alternate asset if other choices were found.

  You might see a repetition of this step if the LLM decides that the asset chosen cannot answer the question effectively and goes back to find other assets that can. 

- Specific measures and columns that were identified and used to generate the answer to your question.

- Intermediate calculations and filters that feed into the reasoning.

- The exact SQL that was generated and executed. 

- Live data for the query, which allows you to see the same logic replayed on the current data state. This means that the live data might differ from the original data used if the underlying data has changed. You can download this data as a CSV file. 


### Using other data assets
{: #change_data_asset}

When the AI identifies additional data assets that might be able to answer your question, an **Edit** icon becomes available next to the data asset name. This option allows you to choose a different data asset, if needed. 

You cannot choose a different data asset if your original question was a suggested question.
{: note}

To use another data asset, click the **Edit** icon, select the new data asset, and click **Ask again**. The AI answers the same question that you asked before but uses the new data asset to generate a response 

To avoid getting unexpected results, select a data asset that aligns with the topic of your question. For example, if you asked about sales but select a data asset that only has HR-related data, you might get an inaccurate response. 
{: tip}

### Using other measures and columns
{: #change_measure_column}

If you are using an LLM without Chain of Thought, when it finds additional measures and columns that might help answer your question, an **Edit** icon is available next to **Data referenced**. Click this icon to explore other angles of your data.

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
