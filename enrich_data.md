---
copyright:
  years: 2025, 2026
lastupdated: "2026-07-10"

keywords: enrichment, metadata enrichment, enrich, semantics
subcollection: watsonx-bi


---

{{site.data.keyword.attribute-definition-list}}


# Enriching data in watsonx BI
{: #enrich}

Metadata enrichment in {{site.data.keyword.wxbia_full}} uses generative AI to automatically add business context, descriptions, and semantic meaning to your data. Enriched metadata helps you understand, discover, and query data more effectively.{: #shortdesc}
 
Traditional or simple data might lack clear meaning or context. Metadata enrichment uses AI to analyze the data and adds a semantic layer of business context and instructions to the data, making it more insightful for users. It also generates context-aware descriptions for tables and columns, which consider the surrounding columns and the context of the table. 

Before you can ask questions about your data, the data must undergo metadata enrichment. Watsonx BI uses the following enriched metadata to answer questions. 

- Asset name 
- Asset description 
- Column name 
- Column description 
- Column identifier 
- Column data type, usage, aggregate, and nullable fields 
- Sampled columns 

While most of these might already be available in your data, asset and column names and descriptions are generated during the metadata enrichment process. For example, a column name might be abbreviated in your data. Enrichment can improve this by generating a meaningful name and description.

 Before enrichment | After enrichment|
 |-------|-------------|
 |Column name: cust_id <br><br>Description: none | Column name: Customer ID <br><br>Description: Unique identifier for each customer in the CRM system|
 {: caption="Enrichment example" caption-side="bottom"}

Watsonx BI automatically enriches your data during the [metric creation](/docs/watsonx-bi?topic=watsonx-bi-overview_metrics){: external} process. Metadata enrichment does not change your original data. 
{: note}

## Supported metadata enrichment providers
{: #supported_mde_providers}

Administrators can select between the following metadata enrichment providers in watsonx BI. The selection applies to all users in the account.

IBM watsonx BI enrichment

:   - Available in {{site.data.keyword.wxbia_short}} as a Service only
  
:   - Runs natively in {{site.data.keyword.wxbia_short}} 

:   - Optimized for faster discovery, enhanced semantic understanding, and accurate question answering

:   - Faster enrichment through sampling-based analysis
  
:   - Foundation for automatic metric generation
  
:   - Uses generative AI to add business context directly (no dependency on governance artifacts such as categories and business terms)

:  Use watsonx BI enrichment when you need fast setup, minimal configuration, and AI-driven insights without governance dependencies.

When watsonx BI enrichment is selected, governance artifacts such as categories and business terms are not applied during enrichment. Watsonx BI enrichment uses generative AI to enrich metadata and add business context directly, simplifying the process without relying on governance artifacts.
  

IBM watsonx.data intelligence enrichment

:   - Available in watsonx BI as a Service and watsonx BI on IBM Software Hub

:   - Requires watsonx.data intelligence 

:   - Provides governance, profiling, and classification

:   - Uses custom-defined governance artifacts such as business terms, categories, and data classes

:   - Used by default if you have watsonx.data intelligence provisioned in your account 

:  Use watsonx.data intelligence enrichment when you need enterprise data governance and classification, and deep profiling through full data analysis, which can take longer.

:  For more information, refer to watsonx.data intelligence documentation on [enriching data](https://dataplatform.cloud.ibm.com/docs/content/wsj/governance/metadata-enrichment.html?context=df&audience=wdp).

When watsonx.data intelligence is not available in the IBM Cloud account, watsonx BI will use its built-in enrichment for metadata enrichment. Enrichment provides governance, profiling, and classification capabilities. When watsonx.data intelligence enrichment is selected, governance artifacts such as categories and business terms are used to augment technical metadata with descriptive and meaningful names. 

### Comparing enrichment capabilities
{: #diff_enrichment}

The following table compares the enrichment capability of both enrichment providers.

| Capability | watsonx.data intelligence |  watsonx BI |
|-------|-------------|-----------------------|
| Profiling and sampling data | Creates a full data profile by querying data. Performs basic analysis such as row count, null count, and unique values. |Samples data and performs basic analysis such as row count, null count, and unique values.|
| Statistical analysis | Includes advanced univariate and bivariate statistics in addition to basic profiling.| Includes univariate and bivariate statistics.|
| Generating names and descriptions| Generates context-aware names and descriptions for columns and tables.|  Generates context-aware names and descriptions for columns and tables.|
|Metadata classification| Performs data class analysis, including governed data classes and BI-supplied classes such as temporal and geographic.| Performs its own data analysis focused on temporal and geographic classification.|
| Vector embeddings | Generates vector embeddings from data and metadata to improve question answering and data discovery.| Generates vector embeddings from data and metadata to improve question answering and data discovery.|
| Indexing data | Adds data to global search to make it discoverable across the platform.| Adds data to global search to make it discoverable across the platform.| 
{: caption="Comparing metadata enrichment" caption-side="bottom"}

### Choosing an enrichment provider
{: #choose_mde}

As an administrator, you can select the enrichment provider from the **Configuration and settings** page based your organization's requirements. 

You might not need to choose an enrichment provider. If watsonx.data intelligence is not available in your environment, watsonx BI enrichment is used automatically.
{: note}

To select the provider:

1. Go to **Configuration and settings > AI configuration**.

1. Select the enrichment provider. 

After you select an option, future enrichments for all users in the account run with the selected provider. 

Changing the enrichment selection affects future enrichments only. Existing enriched assets do not need to be enriched again.
{: note}

## Limitations
{: #limitations_mde}

**User interface differences**

- User interface differences in watsonx BI enrichment:

  - No page to review the enrichment results or view the progress of the enrichment job.

  - Watsonx BI enrichment does not create a metadata enrichment asset. This means that you cannot access watsonx BI enrichment results or the asset.

**Switching from watsonx.data intelligence to watsonx BI enrichment**

- Using enriched assets after deprovisioning watsonx.data intelligence

  When watsonx.data intelligence is deprovisioned, you cannot run enrichment again on previously enriched assets with it. You can continue to use those assets or re-enrich them with watsonx BI enrichment.

- Using imported projects 

  Imported projects that were enriched with watsonx.data intelligence are not compatible with environments that use the built-in watsonx BI enrichment. If your account now uses watsonx BI enrichment, assets enriched with watsonx.data intelligence are no longer supported. To continue using these assets, you must use watsonx.data intelligence for enrichment.

- Using samples 

  If you have samples that were installed prior to using watsonx BI enrichment, and you make changes to the semantic data model or metrics in the samples, you need to re-export metrics to use them in conversations.

**Re-enriching data using watsonx BI enrichment**

If you are using watsonx BI enrichment, to re-run enrichment, you have to manually re-import metadata. 

1. Go to **Navigation Menu > Projects > View all** projects and open the project with the data that needs to be re-enriched.

1. Go to the **Assets** tab and under **Data access**, click **Metadata import**.

1. Open the metadata import asset associated with the semantic data model and click **Reimport metadata**.

After metadata import is complete, enrichment starts automatically.

**Updating a semantic data model after switching to watsonx BI enrichment**

To update a semantic data model with new tables or columns when using watsonx BI enrichment, you need to reimport metadata. For more information, see [Adding data to an existing semantic data model](/docs/watsonx-bi?group=adding-data-to-an-existing-semantic-data-model){: external}.
