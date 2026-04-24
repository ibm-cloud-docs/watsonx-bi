---
copyright:
  years: 2025, 2026
lastupdated: "2026-04-24"

keywords: about watsonx BI
subcollection: watsonx-bi


---

{{site.data.keyword.attribute-definition-list}}

# IBM watsonx.data intelligence required for {{site.data.keyword.wxbia_short}}  
{: #data_intelligence_plans}

IBM watsonx.data intelligence is required to use {{site.data.keyword.wxbia_full_notm}}. {: #shortdesc}

Watsonx.data intelligence provides the data preparation and governance capabilities that {{site.data.keyword.wxbia_short}} relies on. These capabilities help ensure that data is understood, consistently defined, and accurately interpreted.

## How watsonx.data intelligence is used with {{site.data.keyword.wxbia_short}} 
{: #di_required}

Watsonx.data intelligence supports watsonx BI in the following ways:

- Import metadata 

  Imports metadata that represents data tables from remote data sources.

- Metadata enrichment

  Enhances structured data assets with metadata that describes the data, such as column meaning and relationships.

- Business vocabulary and governance

  Establishes a shared business vocabulary by using governance artifacts, including business terms, data classes, reference datasets, and classifications. Industry-specific vocabularies are also available through Knowledge Accelerators.

## Capacity Unit Hours (CUH) and plan usage
{: #compute_usage}

As an Administrator or Cloud account owner, when you provision watsonx.data intelligence to be used with watsonx BI, you can select one of the following plans:

- Trial
- Essentials
- Standard
- Premium 

Each plan has a specific amount of compute usage that is measured in Capacity Unit Hours (CUH). The CUH is used when you run metadata import and metadata enrichment jobs. 

### What happens when CUH is exhausted
{: #cuh_limit}

If you run out of CUH, watsonx BI continues to function, but metadata enrichment is limited.

You can still:

- Create metrics
- Work with semantic data models
- Analyze existing enriched data 
- Use a data source, such as an uploaded file, that is not enriched

However, jobs that depend on metadata enrichment cannot run without available CUH, including:

- Metadata import

- Metadata enrichment at the data source level (through a connection)

- Metadata enrichment at the metric definition level

- Metadata enrichment for newly uploaded files 

The impact of insufficient CUH depends on the workload:
 
Database through connection

:   If metadata enrichment of source data through a connection is skipped because of insufficient CUH, you can still create metrics manually. You can also update the semantic data model manually to add the required business context. 

:   For more information, see [Optimizing data for AI](/docs/watsonx-bi?topic=watsonx-bi-best_practices){:external} and [Teaching watsonx BI your business language](/docs/watsonx-bi?topic=watsonx-bi-teach_wxbi#add_context_semantic_model){: external}. 

Metric definitions

:   If metadata enrichment of metric definitions is skipped due to insufficient CUH, the metrics will still be created and exported to the project. However, response accuracy might be impacted because additional enriched context (such as sampling data values) is missing.


Uploaded files

:   When you upload a file, if metadata enrichment is skipped due to insufficient CUH, you can still ask questions against the file or use it as a source to create metrics manually. 

In scenarios where enrichment does not occur, response accuracy might be impacted if you use a data source or a metric that lacks enriched metadata.

To avoid enrichment failures, Administrators or Cloud account owners can upgrade the watsonx.data intelligence plan for the account. Depending on the plan, CUH usage is calculated monthly and resets at the end of the billing period. For information about how to check usage for your account, see [Viewing your usage](/docs/account?topic=account-viewingusage&interface=ui){: external}.

## Upgrading the watsonx.data intelligence plan (administrators only)
{: #upgrade_di_plan}

If CUH limits are affecting metadata import or enrichment, Administrators or the Cloud account owner can upgrade the watsonx.data intelligence plan to increase available CUH.

1. Log in to the [IBM Cloud account](https://cloud.ibm.com/login). 

2. Go to **Navigation Menu > Resource list**.

3. Select watsonx.data intelligence from **AI/Machine learning**. 

4. Go to the **Plans** tab and select the new plan and click **Upgrade**.
