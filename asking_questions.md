---
copyright:
  years: 2026
lastupdated: "2026-01-07"

keywords: asking questions
subcollection: watsonx-bi



---

{{site.data.keyword.attribute-definition-list}}


# Asking questions in natural language
{: #ask}

Use natural language for the best results when you use {{site.data.keyword.wxbia_full}}. {{site.data.keyword.wxbia_short_cap}} attempts to understand your questions and queries based on the context of the whole sentence, including grammar, punctuation, and spelling. {: #shortdesc}

The more specific and explicit you are, the more likely that {{site.data.keyword.wxbia_short}} is going to understand and answer your question. 
{: tip}

When it is unable to interpret your question correctly or your question is ambiguous, you might find that slight alterations to how you ask the question can yield the correct result. 

For example, the following input might return a single number or the total number for each city.

> How many units were sold in Tokyo and Beijing?

You can clarify your intention by asking: 
  
> How many units were sold in Tokyo and Beijing by city?

Before you start conversing with {{site.data.keyword.wxbia_short}}, you can provide context for your business data by [adding business terms or glossaries](/docs/watsonx-bi?topic=watsonx-bi-business_terms){: external}. Use business terms to define specific terms like "S&S" and "TAM" and codifying that metadata into the semantic layer and the underlying definition of a metric.

## Types of questions you can ask
{: #type_questions}

### Descriptive questions
{: #descriptive}

Use descriptive questions to explore your data. These questions are typically the "What" and "Which" questions that summarize and describe your data. For example: 

- What are the product lines?

- Which product lines have revenue greater than planned revenue?

- What is the total planned revenue by calendar year and calendar month?

- What is the total revenue for each product line in each month?

- Which product line has the highest revenue?

### Diagnostic questions
{: #diagnostic}

Diagnostic questions can help you determine the reason behind changes in your data. For example:

- Is there a correlation between product size and revenue?

- What is driving revenue?

## Synonymous terms
{: #synonymous}

{{site.data.keyword.wxbia_short_cap}} understands most synonymous terms and phrases. For example, depending on your metric, the terms sales, revenue, and profit, might resolve to the same information. 

Synonymous terms also apply to many filters and aggregations. You can ask for "top 3 products", "best products", and "products with the most sales". You can also spell out words or use symbols when applicable. For example, "show sales greater than $1000", "show sales > 1k", or "show sales more than 1,000".

## Aggregating data
{: #aggregating}

Applying aggregations can add focus and create more compelling results and visualizations. You can use any aggregations that {{site.data.keyword.wxbia_short}} supports, including:

- total

- average

- maximum

- minimum

- count

- unique or distinct

{{site.data.keyword.wxbia_short_cap}} infers aggregation by using natural language:

- How many products were sold in 2025?

- What are the sales by region?

- How does planned revenue compare to sales revenue in Europe?

A metric might identify a default aggregation value for a column, for example, by using AVERAGE for weight. You can override this behavior by specifying the aggregation in the question:

- What is the weight per product? - This input uses the AI model's aggregation of AVERAGE to give the average weight for each product because the question doesn't explicitly identify how to aggregate the data.

- What is the total weight per product? - This input overrides the AI model's aggregation and uses SUM. When you ask for highest, lowest, least or most, the AI model might interpret your question as the maximum or minimum value rather than aggregating all values before it identifies which total is highest or lowest. You can clarify your intent by including "total" in the question:

- Which product has the highest total revenue?

## Filtering data
{: #filtering_data}

You can ask {{site.data.keyword.wxbia_short}} to filter by using words and associated synonyms. You can add filters for specific attributes, geographic items, temporal terms, and more. Some examples of how you can use filtering:

- Show the top 3 products by revenue in France.

- Which products have inventory > 500 in Q1 2025?

- How many units shipped more than a month after they were purchased last quarter?

- Show revenue in 2023 and 2024.

- What are the top 5 states by average inventory, excluding California.

While {{site.data.keyword.wxbia_short}} has a good understanding of common concepts, like country, region and city names, the ability to answer questions depends on your data. For example, when your data includes the product sales per country, asking "How do sales compare in Asia vs the Americas" might not return expected results if the data does not identify which countries are in each region. If such questions are common, consider adjusting your metric to include a region column.

## Follow-up questions
{: #followup}

After you ask a question, you can follow-up with other questions or clarification. {{site.data.keyword.wxbia_short_cap}} interprets your question in the context of the previous question asked. For example:

1. What is the total revenue for products sold in Canada?

2. What about in the US?

3. Break down the sales by product brand.

How you word your question determines whether it is a continuation of the previous question or a separate request. If {{site.data.keyword.wxbia_short}} is unable to determine that on its own, starting a new conversation clears the context.

