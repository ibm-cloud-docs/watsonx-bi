---
copyright:
  years: 2025, 2026
lastupdated: "2026-02-20"

keywords: key concepts, create metrics
subcollection: watsonx-bi



---

{{site.data.keyword.attribute-definition-list}}


# Key concepts for metrics
{: #concepts}

Before you start creating metrics, it helps to understand a few foundational concepts that shape how {{site.data.keyword.wxbia_short}} works. {: #shortdesc}


## Metrics
{: #about_metrics}

Metrics are a calculation that are used to measure and monitor key areas of a business. {{site.data.keyword.wxbia_full}} uses metrics and the underlying enriched metadata that is used to define metrics, to answer your questions and provide insights.

In {{site.data.keyword.wxbia_short}}, metrics are assets stored in projects but defined in semantic data models through metric definitions. A metric definition contains measures and related attributes. After you create a metric definition, you must export it from the semantic data model into a project before it can be used in **Conversations**.

### Who can create metrics?
{: #metrics_role}

Metrics can be created by both the Analytics consumers and Data analysts. 

- Analytics consumers can create their own metrics or use ones made available to them.

- Data analysts can create, publish, govern, and assign metrics to Analytics consumers or to other Data analysts.

Although both roles follow the same creation steps, only Data analysts can publish metrics to the **Metrics catalog** and control access to them. Assigned metrics appear in the **Key metrics** panel in **Conversations**.

## Projects
{: #projects}

A project is a collaborative workspace where you work with data and other assets to accomplish a particular goal, such as creating metrics.  

You can choose an existing project to work in or create a new project from the **Data and Metrics** tab. Once you've identified a project to work in, select it from the project switcher on **Data and Metrics**. 

Create one project when you are working toward one defined business goal and using the same data sources and collaborators. For example, if you are exploring data for a single initiative such as sales forecasting, churn analysis, or inventory optimization, a single project keeps related assets together and might be easier to manage.Create multiple projects when your workstreams support different goals, require different collaborators or permissions, or need data isolation. 
{: tip}

You can now:

-  Create metrics on the **Metrics** tab

   This action starts the metric creation flow where you can add the data you want to ask about and prepare the data for use in conversations through metadata enrichment and data modeling in the semantic data model. 

- Upload a data file on the **Data sources** tab

  You can upload a file to quickly get started on asking questions about the data in the file. The data automatically undergoes metadata enrichment during the file upload process, preparing it for use in conversations. 

When asking questions in **Conversations**, choose the project in the list in the input box. Watsonx BI uses the enriched metadata and metrics in that project to generate answers.

## Assets
{: #assets_types}

An asset is an item that contains information about data, other valuable information, or code that works with data.

In {{site.data.keyword.wxbia_short}}, you work with assets in a project. You can view the types of assets in a project on the **Project > Assets** tab.

| Asset | Asset type |Description |
|-------|---------|--------------|
| Data asset | Data | Represents data that is accessed through a connection to a remote data source. Examples include Table, Metric, and Uploaded file. |
| Semantic data model | Data| Contains the structure of data through its relationships and calculations.Metrics are defined in semantic data models.|
| Connection| Data access| Contains the information to connect to a data source.|
| Metdata import| Data access | Imports asset metadata from a connection. |
| Metadata enrichment | Metadata enrichment| Enriches imported asset metadata.|
| Visualizations | Visualizations | A chart that visually represents a metric.
| Job| Job| Contains information about how to run the asset, including the environment definition, schedule, and notification options|
{: caption="Assets in {{site.data.keyword.wxbia_short}}" caption-side="bottom"}

## Metadata enrichment
{: #metadata_enrichment}

{{site.data.keyword.wxbia_short_cap}} uses the IBM watsonx.data intelligence for metadata import and enrichment. 

After you select data during the metric creation flow, watsonx BI enriches it with business context such as business terms, descriptions, and inferred relationships.

This enrichment process adds a semantic layer that helps AI understand context, making your data easier to use when generating answers or metrics.

## Semantic data model
{: #semantic_model}

A semantic data model describes  how data is structured, related, and calculated. It provides the meaning and context required for AI‑generated insights. For example, customer service data may include attributes such as Name, Location, and Product number, which can be linked to additional product attributes like category, price, or color.

In {{site.data.keyword.wxbia_short}}, a semantic data model is a type of asset where:

- You define metric definitions (collections of measures and attributes)

- You enrich and model data (relationships, filters, calculations)

- You prepare data that will later be exported to a project for use in Conversations

When you start creating metrics, a new semantic data model is automatically created for you. You can then select existing project data or add new data through a connection. 

At any time, you can access the semantic data model from the **Data and Metrics** tab.
{: note}

Data then goes through metadata enrichment, which allows business context to be added to the data. Once metadata enrichment is complete, you can use the enriched data to automatically generate metrics or build them manually. 

You can use the **Advanced mode** after metadata enrichment to open the semantic data model and use modelling tools to create relationships and calculations, define filters, and more. For more information, see [Data modeling in {{site.data.keyword.wxbia_short}}](/docs/watsonx-bi?topic=watsonx-bi-advanced_mode_model_data){: external}.

## Related links
{: #related}

- [An overview of creating metrics](/docs/watsonx-bi?topic=watsonx-bi-overview_metrics){: external}

- [Enriching data with metadata](/docs/watsonx-bi?topic=watsonx-bi-enrich){: external}

- [Data modeling in watsonx BI](/docs/watsonx-bi?topic=watsonx-bi-advanced_mode_model_data){: external}
