---
copyright:
  years: 2025, 2026
lastupdated: "2026-08-06"

keywords: re-run enrichment, re-enrich, rerun enrichment, reimport metadata, metadata enrichment

subcollection: watsonx-bi

---

{{site.data.keyword.attribute-definition-list}}


# Re-running metadata enrichment
{: #rerun_enrichment}

You can re-run metadata enrichment to update metadata and business context for your data assets. You can start the process from the Data sources page or from project assets.{: #shortdesc}


## Prerequisites
{: #prereq_reenrich}

You must have the Editor or Administrator role to perform this task.


## Re-enriching data from the Data sources page (recommended)
{: #rerun_datasources}

[Cloud]{: tag-blue}

You can re-run metadata enrichment directly from the **Data sources** page in watsonx BI. This option provides a faster way to manage enrichment without navigating to project assets.

The **Data sources** experience is available only in watsonx BI as a Service. If you are using watsonx BI on IBM Software Hub, use the project-based procedure.
{: important}

1. Go to **Data and Metrics > Data sources**.

2. Locate the data source that you want to update.

3. Click the options menu (three dots) next to the data source name.

4. Select an action from the menu. The available actions depend on the enrichment method configured for the data source: 

  - **Re-import metadata** 
  
    If only **Re-import metadata** is available, the data source uses watsonx BI enrichment. For data sources that use watsonx BI enrichment, reimporting metadata automatically triggers enrichment when the import completes.

  - **Re-import metadata** and **Re-enrich metadata** 
  
    If both **Re-import metadata** and **Re-enrich metadata** are available, the data source uses watsonx.data intelligence enrichment. You can reimport metadata, re-run metadata enrichment, or perform both actions as needed. 
    
    If source metadata changed, such as when tables or columns are added, removed, or updated, run **Re-import metadata** first and then run **Re-enrich metadata**. Otherwise, you can re-run metadata enrichment without importing metadata again. 

  You can monitor the enrichment status on this page as well.

## Re-enriching data from project assets 
{: #rerun_project}
[Software]{: tag-blue}
You can also re-run metadata enrichment from project assets. Use this option if you are using watsonx BI on IBM Software Hub.

### watsonx.data intelligence
{: #rerun_wxdata}

1. Go to **Navigation menu > Projects > View all projects**.

1. Select the project that contains the data asset you want to re-enrich.

1. Open the **Assets** tab and under **Curation > Metadata Enrichments**, select the metadata enrichment asset.

1. Click **Start full enrichment**.

### watsonx BI enrichment
{: #rerun_native}

1. Go to **Navigation menu > Projects > View all projects**.

1. Select the project that contains the data asset you want to re-enrich.

1. Open the **Assets** tab and under **Data access > Metadata imports**, select the metadata import asset.

1. Click **Reimport metadata**.

After metadata import is complete, enrichment starts automatically.
