---
copyright:
  years: 2025, 2026
lastupdated: "2026-09-24"

keywords: re-run enrichment, re-enrich, rerun enrichment, reimport metadata, metadata enrichment

subcollection: watsonx-bi

---

{{site.data.keyword.attribute-definition-list}}


# Re-running metadata enrichment
{: #rerun_enrichment}

You can re-run metadata enrichment to update metadata and business context for your data assets. You can start the process from the **Data sources** page or from project assets.{: #shortdesc}


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

3. Click the menu (three dots) next to the data source name.

4. Select **Re-enrich metadata**.



You can monitor the enrichment status on this page as well.

## Re-enriching data from project assets 
{: #rerun_project}
[Software]{: tag-blue}
You can also re-run metadata enrichment from project assets. Use this option if you are using watsonx BI on IBM Software Hub.

1. Go to **Navigation menu > Projects > View all projects**.

1. Select the project that contains the data asset you want to re-enrich.

1. Open the **Assets** tab and under **Curation > Metadata Enrichments**, select the metadata enrichment asset.

1. Click **Start full enrichment**.
