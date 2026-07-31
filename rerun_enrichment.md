---
copyright:
  years: 2025, 2026
lastupdated: "2026-07-31"

keywords: re-run enrichment, re-enrich, rerun enrichment, reimport metadata, metadata enrichment

subcollection: watsonx-bi

---

{{site.data.keyword.attribute-definition-list}}


# Re-running metadata enrichment
{: #rerun_enrichment}

You can re-run enrichment to update the metadata for your data assets. You must have the Editor or Administrator role to perform this task.{: #shortdesc}

## Re-running enrichment with watsonx.data intelligence
{: #rerun_wxdata}

1. Go to **Navigation menu > Projects > View all projects**.

1. Select the project that contains the data asset you want to re-enrich.

1. Open the **Assets** tab and under **Curation > Metadata Enrichments**, select the metadata enrichment asset.

1. Click **Start full enrichment**.

## Re-running enrichment with watsonx BI enrichment
{: #rerun_native}

For native enrichment or watsonx BI enrichment, re-enrichment is triggered by reimporting metadata.

1. Go to **Navigation menu > Projects > View all projects**.

1. Select the project that contains the data asset you want to re-enrich.

1. Open the **Assets** tab and under **Data access > Metadata imports**, select the metadata import asset.

1. Click **Reimport metadata**.

After metadata import is complete, enrichment starts automatically.
