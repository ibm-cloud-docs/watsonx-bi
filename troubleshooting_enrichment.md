---
copyright:
  years: 2025, 2026
lastupdated: "2026-05-14"

keywords: monitor enrichment, enrichment error, enrichment warnings
subcollection: watsonx-bi


---

{{site.data.keyword.attribute-definition-list}}


# Metadata enrichment errors or warnings 
{: #troubleshoot_enrichment}



When you create metrics, you might encounter metadata enrichment errors or warnings. These indicate that the enrichment process was incomplete or encountered issues. {: #shortdesc}

- Errors must be resolved by rerunning enrichment

- Warnings can be ignored but doing so might reduce query accuracy

Metadata enrichment is essential because the process not only expands metadata, assigns business terms, generates contextual asset and column names and descriptions, but also computes vectors. Vectors help AI understand semantic relationships between queries and actual data values in a structured and mathematical way. Without these vectors, filters in queries (the WHERE clause of a query) might fail to match the correct data if exact values aren't specified in a question.

## Impact of ignored warnings
{: #ignoring_warnings}

Ignoring enrichment warnings can lead to:

- Incorrect filters - Filters in queries (WHERE clauses) might not match the correct data. 

  For example, asking for “americas” when the column contains “North America” and “South America” might return no results unless vectors suggest the correct values.

- Case and format mismatches - If your data uses specific formats, queries that use other variations might fail.

  For example, asking for "surgeries" when the data contains the term "SURGERY" might not return any results. 

To improve query accuracy when warnings remain unresolved, add descriptive column metadata to the semantic data model. Include example values or format details. The LLM uses this metadata as context when it generates queries.


## Common metadata enrichment errors and warnings
{: #common_mde_messages}

| **Message** | **Impact** | **Action** |
|-------------|-----------|--------------------------|
| Unable to retrieve data values to process enriched metadata. | Metadata enrichment could not be completed because data values were not retrieved. | You need to resolve this error before proceeding. Click **Try again** to rerun enrichment. |
| Unable to retrieve data values to compute and write vectors to Cloud Object Storage. | Enrichment completed with a warning that data values could not be retrieved to compute and write vectors to Cloud Object Storage. This issue impacts accuracy for filter search.| Click **More details** and rerun enrichment.|
| Unable to compute and write vectors to Cloud Object Storage. | Enrichment completed with a warning that vectors could not be computed and stored to Cloud Object Storage.  This issue impacts accuracy for filter search. |Click **More details** and rerun enrichment. |
| Unable to write vectors to Cloud Object Storage. | Enrichment completed with a warning that Vectors were computed but not saved. This issue impacts accuracy for filter search. | Click **More details** and rerun enrichment. |
| Unable to compute and write some vectors to Cloud Object Storage. | Enrichment completed with a warning that only some vectors were computed and written to Cloud Object Storage. This issue might impact accuracy for filter search. | Click **More details** and rerun the step. |
