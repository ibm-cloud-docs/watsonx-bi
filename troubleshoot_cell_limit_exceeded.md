---
copyright:
  years: 2026
lastupdated: "2026-04-15"

keywords: cell limit exceeded, 10000000 cells, exceeded after reading rows, query service local execution, local execution engine
subcollection: watsonx-bi

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}

# Why do I get a cell limit exceeded error?
{: #troubleshoot-cell-limit-exceeded}
{: troubleshoot}
{: support}

When you run metadata enrichment, submit a query, or create a visualization, watsonx BI might display an error if the amount of data exceeds the cell limit.{: #shortdesc}

You might see an error message similar to the following:

> The cell limit of 10000000 has been exceeded after reading 625001 rows.

This error can occur when {{site.data.keyword.wxbia_short}} query service must process part of a request locally. If the amount of fetched data becomes too large, the operation can exceed the cell limit. 

This cell limit is enforced to help prevent locally executed operations from exhausting the memory and disk resources required to complete the request.

## Resolving the error
{: #resolve_cell_limit}

Try one or more of the following actions to reduce the amount of data processed locally:

- Add filters to reduce the volume of data in the request.

  For example, restrict the query to a smaller subset such as a specific year or country, like `year = 2025` and `country = 'Mexico'`.

- For metric definition enrichment, add [design mode filters](/docs/watsonx-bi?topic=watsonx-bi-model_filters#complex_query){: external}.

  Design mode filters limit the data that is used during enrichment and during queries that originate from the modeling user interface.
 
- For metadata enrichment of source data, reduce the number of sampled rows in the [enrichment settings](docs/watsonx-bi?topic=watsonx-bi-enrich#mde_projects){: external}.

  Sampling fewer rows can lower the amount of data that must be processed locally and help avoid the limit.
