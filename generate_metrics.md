---
copyright:
  years: 2025, 2026
lastupdated: "2026-06-22"

keywords: generate metrics, auto-generate metrics, automatic metrics
subcollection: watsonx-bi


---

{{site.data.keyword.attribute-definition-list}}


# Generating metrics automatically 
{: #generate_metrics}

[Preview]{: tag-teal} Metrics define business logic that answers data questions consistently across conversations. You can generate metrics automatically from your data and semantic model.
{: #shortdesc}

This feature is a Technology Preview feature in {{site.data.keyword.wxbia_short}}. Technology Preview offers customers early access to product features, allowing them to explore functionality and share feedback during development. These features are provided for evaluation purposes and might not be fully functional or complete.
{: important}

## Overview
{: #overview_generate_metrics}

Watsonx BI analyzes your data and semantic data model to create metrics that reflect real business logic. The generation experience differs depending on your environment:

- Watsonx BI as a Service: Generate metrics by providing a business question and a SQL query

- Watsonx BI on Software Hub: Generate metrics from the enriched metadata in the semantic data model

In both environments, you can use the **Advanced mode** to refine metrics and create more. 

## Generating metrics in watsonx BI as a Service
{: #question_sql}

In watsonx BI as a Service, you can generate metrics automatically by providing a business question that needs to be answered and the corresponding SQL query. 

Providing a question and SQL pair anchors metric generation in a real business scenario, which improves both accuracy and relevance. The SQL defines the exact logic used to answer the question, while the question captures the analytical intent. Together, they remove ambiguity in how metrics are created.

This approach to generating metrics allows Data analysts to generate metrics without relying on manual or advanced modeling techniques. Instead of defining relationships, calculations, and the semantic data model manually, watsonx BI extracts these elements directly from the SQL.

By validating the SQL against the data, watsonx BI ensures that generated metrics align with the actual data structure and values. This validation reduces errors and increases trust in metric outputs. 

Watsonx BI also identifies additional relevant columns and relationships that can strengthen the answer. As a result, generated metrics are more complete, context-aware, and better suited for answering questions in conversations.

To generate metrics automatically using this approach, follow these steps.

1. On the **Data and Metrics** tab, select a project or create a new one by clicking the '+' button next to the project list. 

1. Click **Create metrics**. 

1. Enter a unique name for the semantic data model.

1. [Select your data](/docs/watsonx-bi?topic=watsonx-bi-select){: external}.

1. Click **Next** to continue to **Metadata enrichment**. 

  During [metadata enrichment](/docs/watsonx-bi?topic=watsonx-bi-enrich){: external}, business context-based metadata is added to your data to prepare it for use in conversations and metrics. 
    
  No changes are made to your original data during enrichment. 

1. Click **Next** after enrichment completes to go to the **Metrics overview** page. 

1. Click **Generate metrics**. 

1. Enter a business question and corresponding SQL query, then click **Generate**.

  - Watsonx BI validates the SQL against the dataset

  - One or more metrics are generated to answer the question

  - Additional relevant columns and relationships are included automatically

1. Review the metrics generated from your questions and SQL queries, then select the ones you want to add to the project. 

  You can also view any questions and SQL queries that could not be used to generate metrics. You can review the reasons and update your inputs.

1. The selected metrics display on the **Metrics overview** page. 

  You can now [try each metric in a conversation](/docs/watsonx-bi?topic=watsonx-bi-try_metrics){: external} to confirm it answers your data question.
   
  You can also do the following:

  - [Add visualizations to metrics](/docs/watsonx-bi?topic=watsonx-bi-add_viz_metrics){: external}  
   
  - Use the [Advanced mode](/docs/watsonx-bi?topic=watsonx-bi-advanced_mode_model_data){: external} to make changes to the semantic data model (such as create new relationships, calculations, and more) and [edit metrics](/docs/watsonx-bi?topic=watsonx-bi-edit_metrics){: external}

  - [Publish metrics and visualizations](/docs/watsonx-bi?topic=watsonx-bi-publish_metrics){: external} to the **Metrics catalog** and specify access permissions (Data analysts only)
    
### Limitations
{: #limitations_metrics}

- The business question and SQL are not validated against each other.

- SQL query must match identifiers in the semantic data model.

- Results depend on the clarity of the questions and SQL queries. Ambiguous questions or poorly structured SQL might lead to weak or inaccurate metrics. 
 
### Troubleshooting metric generation
{: #troubleshoot_metrics}

**SQL identifiers do not match identifiers in semantic data model**

For metric generation to work correctly, the table names and column names in the SQL must match the identifiers that are in the semantic data model. 

If column or table names contain spaces, they are typically converted to underscore-separated names (for example, order date becomes order_date). If identifiers do not match, SQL validation can fail or metrics might not be generated correctly.

You can use the **Advanced mode** to view the system-generated SQL with the correct identifiers.

1. Open the semantic data model in **Advanced mode**.

2. Right-click a table.

3. Select **Show query information**.

This option displays a simple `SELECT` statement that includes the table and column identifiers in the correct format. You can use this SQL as a reference when building your question–SQL pair. This method is especially useful for uploaded files.

## Generating metrics in watsonx BI on IBM Software Hub
{: #metrics_swh}

When you generate metrics in watsonx BI on IBM Software Hub, it creates metric definitions and automatically exports them to the project for use in **Conversations**.

1. On the **Data and Metrics** tab, select a project or create a new one by clicking the '+' button next to the project list. 

1. Click **Create metrics**. 

1. Enter a unique name for the semantic data model. 

1. On the **Select data** page, [select your data](/docs/watsonx-bi?topic=watsonx-bi-select){: external}. 

1. Click **Next** to continue to **Metadata enrichment**. 

   During [metadata data enrichment](/docs/watsonx-bi?topic=watsonx-bi-enrich){: external}, business context-based metadata is added to your data to prepare it for use in conversations and metrics. 
    
   No changes are made to your original data during enrichment. 

1. Click **Next** to go to the **Metrics overview** page, then click **Generate metrics**. 

   You can generate metrics here only when the semantic data model has no existing metrics. To add more metrics, use the **Advanced mode**.
   {: note}

1. Select the metrics that you want to use. You can preview details before selecting. 

1. Open the [Advanced mode](/docs/watsonx-bi?topic=watsonx-bi-advanced_mode_model_data){: external} to review the semantic data model.  

   Make sure that meaningful names, descriptions, and identifiers are assigned to each column. These fields help AI find and retrieve data when it answers your questions. 
   {: tip}

1. Save any changes made to the semantic data model.

1. If you edited a metric definition, click the menu icon for the metric definition and select **Export metric definition**. 

   Exporting a metric definition automatically enriches the metric definition, creates a metric or updates an existing one, and makes the metric available for use in conversations. 

1. (Optional) Go back to the **Metrics overview** page and: 

   - [Add visualizations](/docs/watsonx-bi?topic=watsonx-bi-add_viz_metrics) to one or more of these metrics. 
    
   - [Try a selected metric](/docs/watsonx-bi?topic=watsonx-bi-try_metrics) in a conversation to ensure that it can answer questions about your data. You can go back to the **Advanced mode** to adjust its metric definition, if necessary.  
    
   - (Data analysts only) [Publish metrics and related visualizations](/docs/watsonx-bi?topic=watsonx-bi-publish_metrics){: external} to the **Metrics catalog** and assign them to Analytics consumers. 

You can go back to the **Converations** page to ask questions about your data.

## Generating metrics in Advanced mode
{: #metrics_advanced}

In both environments, you can generate additional metrics after the initial generation by using the **Advanced mode**.

1. Open the **Advanced mode** from the **Metrics overview** page.

2. Select the measures that you want to use, right-click, and select **Generate metric definitions**. 

   New metric definitions are generated and displayed in the semantic data model. 

3. Save the semantic data model. 

4. Export the metric definitions that you want to use in conversations.

5. Go to the **Metrics overview** page if you want to: 

   - Add visualizations to the newly-created metrics

   - Try a metric in a conversation

   - Publish the metrics and related visualizations to the **Metrics catalog** (Data analysts only)

6. Go to **Navigation menu > Home > Conversations** to ask questions about your data.
