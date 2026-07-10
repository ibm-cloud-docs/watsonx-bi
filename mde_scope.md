---
copyright:
  years: 2025, 2026
lastupdated: "2026-07-10"

keywords: enrichment, metadata enrichment, enrich, semantics
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


# Metadata enrichment scope and steps
{: #enrich_settings}

Metadata enrichment occurs at two levels in {{site.data.keyword.wxbia_short}}; the project and data asset levels. Any metrics that you build or generate are also enriched. {: #shortdesc}

Metadata enrichment settings for all projects, data assets, and metrics in watsonx BI are configured by default, which help ensure consistent use of the enrichment options.

The following steps take place during metadata enrichment:

1. Metadata import 

   Metadata is imported from the data tables that you added to the semantic data model and a metadata import asset is created. This import occurs during enrichment of an uploaded file or during the metric creation process when you select data from a connection. Imported metadata provides asset details, relationships, and a preview of the data.
   
2. Metadata enrichment 

  Depending on the enrichment provider selected for your account, the steps in each might be different.

   Watsonx.data intelligence enrichment

     :  - Data profiling and sampling

     :  - Statistical analysis

     :  - Assigning business terms and classifications 

     :  - Expanding metadata and generating names and descriptions

     :  - Expanding metadata 

     :  - Creating relationships between tables 

     :  - Processing of metadata enrichment to generate and store vector embeddings and index data

   :  For more information, refer to the watsonx.data intelligence documentation on [enriching data](https://dataplatform.cloud.ibm.com/docs/content/wsj/governance/metadata-enrichment.html?context=df&audience=wdp).

   Watsonx BI enrichment

    :  - Data profiling and sampling

    :  - Statistical analysis

    :  - Expanding metadata and generating names and descriptions

    :  - Creating relationships between tables 

    :  - Processing of metadata enrichment to generate and store vector embeddings and index data


