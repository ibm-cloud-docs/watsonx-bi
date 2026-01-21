---
copyright:
  years: 2024
lastupdated: "2024-04-26"

keywords:
subcollection: watsonx-bi



---

{{site.data.keyword.attribute-definition-list}}

# Use of AI in conversations 
{: #explainability}

The **AI** label in the user interface gives an overview of how AI works in **Conversations**. {{site.data.keyword.wxbia_full}} uses large language models (LLM) to answer your questions and provide recommendations, insights, and summaries for your business data. {: #shortdesc}

Administrators can choose the LLM that is used in {{site.data.keyword.wxbia_short}} conversations for users in their organization and can update selection at any time from the **Configuration and settings > Model settings** page. 

## How AI generates responses 
{: #ai_queries}

The selected LLM is used to respond to your BI questions.  It analyzes your input, along with the metrics and enriched metadata you have access to, to understand the underlying business logic. It then uses column titles, descriptions, sample values, SQL examples, and predefined instructions to identify the most relevant data. Based on this understanding, the LLM generates the appropriate query to retrieve the relevant information.

Using the returned data, the LLM produces a text-based answer, a visualization, or both. You can view each step of this process in the **AI steps** by clicking **Show AI steps** in the response.

The LLM also evaluates key metrics and helps surface changes in your business data. When you select a metric from the **Key metrics** panel, the AI can summarize and explain what has changed and why it might be important.

The name of the LLM used to generate each response appears in the **AI** label and within **AI steps** during conversations.

{{site.data.keyword.wxbia_short_cap}} uses LLMs that are hosted in IBM watsonx.ai and does not use your data to train the models.
{: note}


## Response generation process
{: #response_process}

1. Interpretation and analysis - {{site.data.keyword.wxbia_short}} interprets your question and analyzes its intent.

2. Context rephrasing  -  {{site.data.keyword.wxbia_short}} might rephrase the question based on the historical context of previous questions.

3. Key word extraction and identifing data source - {{site.data.keyword.wxbia_short}} pulls out key search terms from the question and identifies the data source that can answer the question.

4. SQL generation - {{site.data.keyword.wxbia_short}} generates a query to retrieve the most useful and accurate answer by using the following inputs:

 - The rephrased question and extracted key terms

 - Column labels, column descriptions, sample values in metrics, and enriched metadata

 - Asset labels and asset descriptions

 - General instructions

 - SQL examples

5. Response generation - {{site.data.keyword.wxbia_short}} uses the queried data, the rephrased question, and final phrasing instructions to generate a text response, visualization, or both.

For more information, see [Steps AI takes to respond](/docs/watsonx-bi?topic=watsonx-bi-steps_ai){: external}.

## Related links
{: #related_explainability}

- [Selecting the large language model for your account](/docs/watsonx-bi?topic=watsonx-bi-choose_llm_account){: external}
