---
copyright:
  years: 2025, 2026
lastupdated: "2026-07-10"

keywords: governance, business terms
subcollection: watsonx-bi

---

{{site.data.keyword.attribute-definition-list}}


## Using governance for business logic
{: #governance}

Governance artifacts add business meaning to your data and are used during metadata enrichment. {: #shortdesc}

Governance in watsonx BI is optional and only applies when you use:

- watsonx.data intelligence to enrich your data in watsonx BI as a Service 

- watsonx BI on IBM Software Hub where watsonx.data intelligence is a required dependency for metadata enrichment

If you use the built-in watsonx BI enrichment in watsonx BI as a Service, governance artifacts are not required or applied during enrichment.
{: important}

### Governance artifacts

Governance artifacts are organized into categories and can come from predefined content, knowledge accelerators, or custom definitions created by your organization. 

Watsonx BI does not automatically set up or manage a governance framework for your project. If you want to use governance artifacts, you must add and manage them manually in your watsonx BI.

{{site.data.keyword.wxbia_short_cap}} includes:

- Predefined business terms, data classes, classifications, and reference data sets

- Industry-specific Knowledge Accelerator

Administrators can build a more robust semantic layer by establishing the organization's own business concepts in watsonx BI through governance artifacts in categories. Much like folders, categories organize governance artifacts in a hierarchical structure.  

Administrators can add the following governance artifacts in {{site.data.keyword.wxbia_short}}: 

- Categories – Containers that organize governance artifacts into a hierarchical structure, similar to folders. Categories help manage ownership, visibility, and scope. 

- Business terms – Standardized definitions of business concepts, such as “revenue” or “customer.” These terms create a shared vocabulary for consistent interpretation of data. 

- Data classes – Definitions that classify data based on structure, format, or value patterns (for example, email address or account number). These are used during profiling and enrichment to identify column content. 

- Classifications – Labels that describe data sensitivity or governance characteristics, such as confidential or personal. These support policy enforcement and access control. 

- Reference data – Standardized sets of allowed values, such as country codes or status lists. These improve consistency and can help classify and validate data. 

For more information, see [Governance artifacts](https://dataplatform.cloud.ibm.com/docs/content/wsj/governance/governance.html?context=df&audience=wdp){: external}.

### How governance is applied
When governance artifacts are available, they can be applied during metadata enrichment to add business context, classifications, and relationships to your data. 

If governance artifacts are not configured, enrichment still runs but relies only on system-generated metadata without business-specific context.

By default, watsonx BI samples up to 1,000 rows for profiling and enrichment. You can adjust this sampling size if needed.





