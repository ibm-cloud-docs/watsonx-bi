---
copyright:
  years: 2025
lastupdated: "2026-01-07"

keywords: response generation
subcollection: watsonx-bi



---

{{site.data.keyword.attribute-definition-list}}


# Understanding how {{site.data.keyword.wxbia_short}} generates a response
{: #answering_questions}

When you ask {{site.data.keyword.wxbia_short}} a question, it analyzes and interprets your question, identifies relevant data sources, and determines the best way to respond to the question (a text response or visualization). {: #shortdesc}

{{site.data.keyword.wxbia_short_cap}} uses your input and the data that you have access to in the form of metrics and the enriched metadata, to understand the business logic. It then uses column titles, descriptions, samples values, and SQL examples, and instructions to find the most relevant data to generate a context-aware response.

## Response generation process
{: #response_process}

1. Interpretation and analysis - {{site.data.keyword.wxbia_short}} interprets your question 

2. Context rephrasing  -  {{site.data.keyword.wxbia_short}} might rephrase the question based on the historical context of previous questions 

3. Key word extraction - {{site.data.keyword.wxbia_short}} pulls out key search terms from the question

4. SQL generation - {{site.data.keyword.wxbia_short}} uses the following to convert your question into SQL:

  - Rephrased question and key terms

  - Column labels, column descriptions, sample values in metrics, and enriched metadata

  - Asset labels and asset descriptions

  - General instructions 

  - SQL examples 

5. Response generation - watsonx BI uses queried data, the rephrased question, and final phrasing instructions to generate a text response or visualization

