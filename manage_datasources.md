---
copyright:
  years: 2026
lastupdated: "2026-09-24"

keywords: data sources, manage data sources, data source management

subcollection: watsonx-bi

---

{{site.data.keyword.attribute-definition-list}}

# Managing data sources (watsonx BI as a Service only)
{: #manage_data_sources}
[Cloud]{: tag-blue}

You can use the **Data sources** tab under **Data and Metrics** to add, view, and manage the data sources used for your metrics and analysis. The **Data sources** tab also shows enrichment status and provides tools to review and approve metadata generated during enrichment. {: #shortdesc}

The **Data sources** tab displays information about each data source such as:

- Data source name
- Data source type  
  - Uploaded file  
  - Data connection
- Enrichment status

Depending on the data source type, you can preview data, re-run enrichment, re-import metadata, review enrichment details, or delete the data source.

## Adding a data source
{: #add_ds}

1. Go to **Data and Metrics** > **Data sources**.

2. Add a data source by using one of the following options:

   - **[Add data from connection](/docs/watsonx-bi?topic=watsonx-bi-select){: external}**: Import data from an available connection to your database or data warehouse.
   - **[Upload file](/docs/watsonx-bi?topic=watsonx-bi-upload){: external}**: Add data from a local file.

   You cannot connect to Cognos Analytics data sources from the **Data sources** tab. To use a Cognos Analytics data source, go to the **Metrics** tab and click **Create metrics**. For more information, see [IBM Cognos Analytics](/docs/watsonx-bi?topic=watsonx-bi-cognos){: external}.{: important}


3. Select and add your data source.

4. After the data source is added, metadata enrichment starts automatically.

  The **Data sources** tab displays the current enrichment status so that you can monitor progress and confirm when enrichment is complete.


## Managing a data source
{: #manage_ds}

Open the context menu for a data source by clicking the options icon (three dots) next to the data source name.

| Action | Description |
| --- | --- |
| **Re-import** | Refresh the data source with the latest data from the source. This is useful when the underlying data has changed and you want to update your local copy. |
| **Re-enrich** | Run [metadata enrichment](/docs/watsonx-bi?topic=watsonx-bi-enrich){: external} again for the data source. This is useful if you want to update the business context metadata or if enrichment previously encountered errors.|
| **Preview** | Preview the contents of the data source to view a sample of the data and verify its contents before using it in metrics or conversations.|
| **View details** | Open the data source details page to review enrichment information and metadata.|
| **Delete** | Remove the data source from the project. This action might impact semantic data models or metrics that reference the deleted data source. |
| **Ask a question** | Ask a question directly against a data source to start analyzing the data immediately without creating a metric first.|
{: caption="Data source management options" caption-side="bottom"}

## Related tasks
{: #related_ds}

- [Uploading a file](/docs/watsonx-bi?topic=watsonx-bi-upload){: external}
- [Add data through a connection](/docs/watsonx-bi?topic=watsonx-bi-select){: external}
- [Enriching data in watsonx BI](/docs/watsonx-bi?topic=watsonx-bi-enrich){: external}
- [Creating metrics](/docs/watsonx-bi?topic=watsonx-bi-overview_metrics){: external}
