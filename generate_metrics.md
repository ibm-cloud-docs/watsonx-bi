---
copyright:
  years: 2025
lastupdated: "2026-01-07"

keywords:
subcollection: watsonx-bi



---

{{site.data.keyword.attribute-definition-list}}


# Generate metrics automatically 
{: #generate_metrics}

[Preview]{: tag-teal} You can generate metrics automatically in the metric creation process. {: #shortdesc}

When you generate metrics, {{site.data.keyword.wxbia_full_notm}} creates metric definitions and automatically exports them to the project for use in **Conversations**.

This feature is a Technology Preview feature in {{site.data.keyword.wxbia_short}} as a Service. 
{: note}

To generate metrics automatically, follow the steps listed in [Overview of creating metrics](/docs/watsonx-bi?topic=watsonx-bi-overview_metrics){: external}. 

When you get to the **Metrics overview** page:

1. Click **Generate metrics**.  

2. Select the metrics that you want to use. You can click the menu for a metric to view its details first. 

3. Click the [Advanced mode](/docs/watsonx-bi?topic=watsonx-bi-advanced_mode_model_data) to review the semantic data model.  

   Ensure that meaningful names, descriptions, and identifiers are assigned to each column. These fields help AI find and retrieve data when answering your questions. 
   {: tip}

4. If you made changes to the semantic data model, click **Save** to save your changes. If you edited a metric definition, click the menu icon for the metric and select **Export metric definition**. 

   Exporting a metric definition automatically enriches the metric definition, creates a metric or updates an existing one, and makes the metric available for use in conversations. 

5. (Optional) Go back to the **Metrics overview** page and: 

   - [Add visualizations](/docs/watsonx-bi?topic=watsonx-bi-add_viz_metrics) to one or more of these metrics. 
    
   - [Try a selected metric](/docs/watsonx-bi?topic=watsonx-bi-try_metrics) in a conversation to ensure it can answer questions about your data. You can go back to the **Advanced mode** to adjust its metric definition, if necessary. 
    
   - (Data analysts only) [Publish metrics and related visualizations](/docs/watsonx-bi?topic=watsonx-bi-publish_metrics){: external} to the **Metrics catalog** and assign them to Analytics consumers. 

5. From the **Navigation menu**, go to **Home > Conversations** to ask questions about your data.

## Generating metrics in Advanced mode
{: #generate_metrics_advanced}

You can only generate metrics once from the **Metrics overview** page. To generate more metrics: 

1. Go to the **Advanced mode**. 

2. Select the measures you want to use, right-click and select **Generate metric definitions**. 

   New metric definitions are generated and display in the semantic data model. 

3. Save the semantic data model. 

4. Export the metric definitions that you want to use in conversations.

5. Go to the **Metrics overview** page if you want to: 

   - Add visualizations to the newly-created metrics

   - Try a metric in a conversation

   - Publish the metrics and related visualizations to the **Metrics catalog** (Data analysts only)

6. Go to **Navigation menu > Home > Conversations** to ask questions about your data.

