---
copyright:
  years: 2025
lastupdated: "2026-01-07"

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

# Metadata enrichment
{: #enrich}

Metadata enrichment in {{site.data.keyword.wxbia_full}} uses generative AI with IBM watsonx.data intelligence to understand your data on a deeper level.  {: #shortdesc}
 
Traditional or simple data might lack clear meaning or context. Metadata enrichment uses AI to analyze the data and adds a semantic layer of well-defined business context such as business terms, descriptions, and categories to the data. Enrichment adds additional instructions to your data, making it more insightful for the users. 

Watsonx.data intelligence uses the pre-defined governance artifacts and the domain-specific glossary concepts that you upload to augment technical metadata with more descriptive and meaningful names. 
 
Metadata enrichment also generates context-aware descriptions for tables and columns, which consider the surrounding columns and the context of the table. 

To ask questions about your data in {{site.data.keyword.wxbia_short}}, your data first needs to be enriched. You can enrich data during the [metric creation](/docs/watsonx-bi?topic=watsonx-bi-overview_metrics){: external} process. 

Metadata enrichment does not change your original data. 
{: note}

## Metadata enrichment scope
{: #enrich_settings}

Metadata enrichment occurs at two levels in {{site.data.keyword.wxbia_short}} the project and data asset levels. Any metrics that you build or generate are also enriched. 

Metadata enrichment settings for all projects, data assets, and metrics in {{site.data.keyword.wxbia_short}} are configured by default, which help ensure consistent use of the enrichment options. 

The categories in the governance framework that contain business terms, data classes, and classifications are applied to the data during enrichment.

### Enrichment settings for projects
{: #mde_projects}

Thresholds are automatically configured in {{site.data.keyword.wxbia_short}} for the following settings. You don't need to change these settings to run enrichment. 

- Profiling and primary key analysis

- Expand metadata

- Term and classification assignment

- Advanced profiling settings

- Basic quality analysis

- Data quality output

- Key relationships

You can view the default settings on the project **Manage > Tools > Metadata enrichment** page.

For more information, see [Metadata enrichment default settings](https://dataplatform.cloud.ibm.com/docs/content/wsj/governance/enrichment-settings.html?context=df&audience=wdp). 

### Enrichment objectives for data assets and metrics
{: #mde_assets}

The default metadata enrichment objectives for data assets and metrics include:

#### Profile data
{: #profile}

Profiling data provides basic statistics about the asset content, assigns and suggests data classes, and suggests primary keys. This type of profiling makes some approximations for certain metrics like frequency distribution and uniqueness. 

Data classes describe the contents of the data in the column. For example, city, account number, or credit card number are data classes. Data classes can be used to mask data with data protection rules or to restrict access to data assets with policies. In addition, they can contribute to term assignments if a corresponding data class to business term link exists.

The confidence score for a data class to be assigned or suggested must at least equal the default threshold that is set in {{site.data.keyword.wxbia_short}}.

Single-column primary keys are suggested based on profiling statistics. If primary key and foreign key constraints are already defined in your data and this information is included in the metadata import, these keys are automatically assigned.

#### Expand metadata
{: #expand}

Expanding metadata semantically enriches the asset and column metadata with fuzzy matching and generative AI. The names that exist in the source are expanded based on the collected metadata and a predefined glossary by using fuzzy matching. 

Generative AI provides descriptions based on the expanded names, surrounding columns, and the context of the data assets. AI-generated descriptions help to understand the content especially when column or data asset descriptions are missing in the data source. The assignment and suggestion thresholds are defined in the default enrichment settings.
      
You can also create custom abbreviations, by uploading CSV files or adding them manually when you create business terms, to extend the business vocabulary used in **Expand metadata**. 

#### Assign terms and classifications
{: #assigned_terms}

This scope assigns and suggests business terms and classifications for tables and columns, which are used as a starting point to create the semantic data model. 

Assigned and suggested business terms have a confidence score attached to them. Terms are assigned or suggested when the confidence level exceeds the default minimum confidence level thresholds for a term to be assigned or suggested. The default setting for assignment threshold is 60% and suggestion threshold is 50%. 





## Steps in metadata enrichment
{: #enrich_steps}

The following steps take place during metadata enrichment:

1. Metadata import 

   Metadata is imported from the data tables that you added to the semantic data model and metadata import (MDI) assets are created.

2. Metadata enrichment 

   During metadata enrichment, a Metadata enrichment (MDE) asset is created based on the following default objective:  

   - Profiling of data 

   - Assigning business terms and classifications 

   - Expanding metadata 

   - Creating relationships between tables 

3. Processing of metadata enrichment 

   During this step, {{site.data.keyword.wxbia_short}} generates and stores vector embeddings for sample values captured during enrichment. These sample values are then used for search and matching filter values in conversations.
   
For more information, refer to the watsonx.data intelligence documentation on [enriching data](https://dataplatform.cloud.ibm.com/docs/content/wsj/governance/metadata-enrichment.html?context=df&audience=wdp).
