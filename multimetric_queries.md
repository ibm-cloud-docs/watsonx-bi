---
copyright:
  years: 2025, 2026
lastupdated: "2026-03-12"

keywords: multi-fact metrics, multiple tables, calculate after aggregate
subcollection: watsonx-bi



---

{{site.data.keyword.attribute-definition-list}}


# Asking questions across multiple data assets
{: #multiasset_queries}

You can ask a single natural‑language question that uses multiple data assets at the same time. With this multi‑asset query capability, watsonx BI can retrieve data from one asset, use that result to build a new query, and return a combined answer.{: #shortdesc} 

`Example: For the product with the most revenue, how many returns did it have?`

In this case, watsonx BI uses both the **Revenue** asset and the **Returns** asset to answer the question.

## How multi-asset queries work
{: #multiasset_process}

When you submit a question, such as the example provided, watsonx BI:

1. Parses the intent, entities, and operations in your question.

2. Identifies which assets are required, such as 'Revenue' for ranking and 'Returns' for comparison.

3. Queries the 'Revenue' asset to find the product with the highest revenue.

4. Uses the returned product value to build a second query to the 'Returns' asset to find the total returns.

5. Generates an answer with a visualization and an explanation of which assets and models were used.

The data assets and SQL that are used to answer the question display in the **AI steps** panel. 

## Prerequisites 
{: #prereq_multiasset}

Multi‑asset queries require:

- Chain of Thought model to be enabled.

- All referenced assets to exist in the same container, such as a project or catalog.

## Supported scenarios
{: #supported_multiasset}

Multi‑asset queries work well when you want to:

- Display independent visualizations, such as *Show the top 5 products by revenue and top 5 by returns*.

- Filter using one asset while displaying another, such as *For the product with the most revenue, how many returns did it have?*.

## Limitations
{: #multiasset_limitations}

With the multi-asset query capability, the large language model (LLM) has the optional ability to fetch the results of a query and use those results to create a new query with static filter values. Watsonx BI does not directly join multiple assets.

Instead, watsonx BI builds independent queries against different assets and lets the LLM use the results of one query to build the next query.

However, a maximum of 10 filter values is currently supported per filter. When a question requires more than 10 filter values, watsonx BI cannot apply a single filter across multiple data assets. Instead, it runs separate queries for each asset and displays the results together.


## Example questions
{: #multiasset_examples}

Try asking questions such as:

- *For the product with the highest revenue, how many returns did it have last quarter?*

- *Show revenue and returns by product category.*

- *Which stores had revenue growth but increasing return rates?*

- *What is the return count for the top 10 SKUs by revenue in 2025?*
