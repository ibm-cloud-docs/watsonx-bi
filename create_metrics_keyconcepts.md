---
copyright:
  years: 2025
lastupdated: "2026-02-05"

keywords: key concepts, create metrics
subcollection: watsonx-bi



---

{{site.data.keyword.attribute-definition-list}}


# Key concepts in creating metrics
{: #concepts}

Here are some key concepts that you need to know before you start creating metrics. {: #shortdesc}


## Metrics
{: #about_metrics}

Metrics are a calculation that are used to measure and monitor key areas of a business. {{site.data.keyword.wxbia_full}} uses metrics and the underlying enriched metadata that is used to define metrics, to answer your questions and provide insights.

Metrics are a type of asset that are stored in projects but are defined in semantic data models through metric definitions. A metric definition is a collection of measures and related attributes. Once created, a metric definition has to be exported from the semantic data model to the project before it can be used in conversations. 

Metrics can be created by both the Analytics consumers and Data analysts. 

If you're a Data analyst, you can publish metrics to the **Metrics catalog**, and assign them to Analytics consumers and other Data analysts in the organization. Assigned metrics display in the **Key metrics** panel in **Conversations**. 

If you're an Analytics consumer, you can create metrics for yourself or a Data analyst can create them for you. 

The process to create metrics is the same for both Analytics consumers and Data analysts, except that Data analysts can publish the metrics that they've created, govern their access, and assign them to other users.

## Projects
{: #projects}

A project is a collaborative workspace where you work with data and other assets to accomplish a particular goal, such as creating metrics.  

You can choose an existing project to work in or create a new project from the **Data and Metrics** tab. Once you've identified a project to work in, select it from the project switcher on **Data and Metrics**. 

You can now:

-  Create metrics on the **Metrics** tab

   This action starts the metric creation flow where you can add the data you want to ask about and prepare the data for use in conversations through metadata enrichment and data modeling in the semantic data model. 

- Upload a data file on the **Data sources** tab

  You can upload a file to quickly get started on asking questions about the data in the file. The data automatically undergoes metadata enrichment during the file upload process, preparing it for use in conversations. 

You can also use projects to set the scope of a conversation. When asking questions in **Conversations**, select the project you want to use from the list next to the input box. {{site.data.keyword.wxbia_full_notm}} uses the enriched metadata and metrics in the selected project to answer your questions.

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

{{site.data.keyword.wxbia_short_cap}} uses the IBM watsonx.data intelligence  for metadata import and enrichment. 

After you start the create metrics flow and select the data you want to work with, the data undergoes metadata enrichment. 

During metadata enrichment, data is enriched with metadata that adds a semantic layer of business meaning to your data in the form of business terms, descriptions, data classes, and relationships. 

Metadata enrichment provides business context for the data, making it easier for AI to understand and retrieve your data to answer your questions. 

## Semantic data model
{: #semantic_model}

A semantic data model describes the structure of data through its relationships and calculations, and provides meaning and context for the data. For example, a customer service data source might contain attributes such as Name, Location, and Product number. This data can represent the customer's name, their city or region, and the product they purchased. The Product number can further be associated with attributes such as product category, price, and colour. 

In {{site.data.keyword.wxbia_short}}, a semantic data model is a type of asset. Metrics are defined in the semantic data model through **metric defintions**. A metric definition is a collection of related measures and attributes. 

This metric definition must be exported to the project before it can be used by {{site.data.keyword.wxbia_short}} to answer your questions. 

When you start creating metrics, a new semantic data model is automatically created for you, where you can then select data from the project that you want to work with or add new data through a connection. 

At any time, you can access the semantic data model from the **Data and Metrics** tab.
{: note}

Data then goes through metadata enrichment, which allows business context to be added to the data. Once metadata enrichment is complete, you can use the enriched data to automatically generate metrics or build them manually. 

You can use the **Advanced mode** after metadata enrichment to open the semantic data model and use modeling tools to create relationships and calculations, define filters and navigation paths, and more. For more information, see [Data modeling in {{site.data.keyword.wxbia_short}}](/docs/watsonx-bi?topic=watsonx-bi-advanced_mode_model_data){: external}.

## Related links
{: #related}

- [An overview of creating metrics](/docs/watsonx-bi?topic=watsonx-bi-overview_metrics){: external}

- [Enriching data with metadata](/docs/watsonx-bi?topic=watsonx-bi-enrich){: external}

- [Data modeling in watsonx BI](/docs/watsonx-bi?topic=watsonx-bi-advanced_mode_model_data){: external}
