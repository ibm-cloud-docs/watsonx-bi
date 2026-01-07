---
copyright:
  years: 2025
lastupdated: "2026-01-07"

keywords: governance, business terms
subcollection: watsonx-bi

---

{{site.data.keyword.attribute-definition-list}}


# Defining business logic with the semantic layer and governance
{: #governance}

{{site.data.keyword.wxbia_full_notm}} comes with a predefined governance framework that helps apply business meaning to your data through governance artifacts. This framework along with the metadata enrichment, which automatically analyzes and enhances technical metadata with more context, labels or descriptions, creates the **semantic layer** that helps activate information for AI. {: #shortdesc}

[Metadata enrichment](/docs/watsonx-bi?topic=watsonx-bi-enrich) takes place when you upload files or create metrics in a project. During metadata enrichment, {{site.data.keyword.wxbia_short}} uses IBM watsonx.data intelligence's capability to match technical metadata with predefined business concepts. Technical metadata is augmented with more descriptive and meaningful names, drawing from the predefined and your domain-specific business concepts.
{: note}

{{site.data.keyword.wxbia_short_cap}} includes:

- Predefined business terms, data classes, classifications, and reference data sets

- Industry-specific Knowledge Accelerator

Administrators can build a more robust semantic layer by establishing the organization's own business concepts in watsonx BI through governance artifacts in [categories](/docs/watsonx-bi?topic=watsonx-bi-categories). Much like folders, categories organize governance artifacts in a hierarchical structure.  

Administrators can add the following governance artifacts in {{site.data.keyword.wxbia_short}}: 

- [Business terms](/docs/watsonx-bi?topic=watsonx-bi-business_terms)

  Business terms implement a common enterprise vocabulary to describe the meaning of data.

- [Classifications](/docs/watsonx-bi?topic=watsonx-bi-classifications)

  Classifications describe specific characteristics of data. 

- [Data classes](/docs/watsonx-bi?topic=watsonx-bi-data_classes)

  Data classes classify data based on the structure, format, and range of values of the data.

- [Reference data](/docs/watsonx-bi?topic=watsonx-bi-reference_data)

  Reference data sets define standard values for specific types of data to classify data and measure consistency.


