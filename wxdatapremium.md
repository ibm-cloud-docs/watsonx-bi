---
copyright:
  years: 2025
lastupdated: "2026-02-10"

keywords: watsonx.data premium
subcollection: watsonx-bi


---

{{site.data.keyword.attribute-definition-list}}

# IBM watsonx.data Premium
{: #wxdpremium}

IBM watsonx.data Premium is an open, hybrid, and governed lakehouse optimized for AI and analytics, which combines data from multiple sources. By integrating {{site.data.keyword.wxbia_short}} with watsonx.data Premium, you can use natural language to analyze your data from watsonx.data Premium to get actionable, easy to understand insights. {: #shortdesc}

This feature is available in IBM Software Hub versions 5.3 and higher. 
{: note}

## Prerequisites
{: #wxdpremium_prerequisites}

- A working {{site.data.keyword.wxbia_short}} environment on IBM Software Hub 5.3

- A working watsonx.data Premium environment

- A [role in your BI community](/docs/watsonx-bi?topic=watsonx-bi-roles-swh){: external}

To get familiar with watsonx BI, review these resources:

- [About watsonx BI's user interface](/docs/watsonx-bi?topic=watsonx-bi-user_interface){: external}

- [Key concepts in creating metrics](/docs/watsonx-bi?topic=watsonx-bi-concepts){: external}

- [An overview of creating metrics](/docs/watsonx-bi?topic=watsonx-bi-overview_metrics){: external}

## Accessing {{site.data.keyword.wxbia_short}} from watsonx.data Premium
{: #wxdpremium_accessing_wxBI}

You can use Business Intelligence tools directly in the watsonx perspective. 

After you are assigned a BI community role, you can use the **Connect to data**, **Create metrics**, and **Chat with data** tiles on the watsonx.data Premium home page to access watsonx BI. To do this, on the watsonx.data home page, select **Business intelligence** from the **Based on your interests** dropdown.

From this page, you can: 

- [Connect to data](/docs/watsonx-bi?topic=watsonx-bi-wxdpremium#connect_wxd_data)
- [Create metrics](/docs/watsonx-bi?topic=watsonx-bi-wxdpremium#create_metrics_wxd)
- [Chat with data](/docs/watsonx-bi?topic=watsonx-bi-wxdpremium#chat_data_wxd)

If you are new to {{site.data.keyword.wxbia_short}}, start your BI journey in the {{site.data.keyword.wxbia_short}} context by creating metrics. 

To generate accurate insights from watsonx.data Premium assets, metrics must be created first. 

During this process, {{site.data.keyword.wxbia_short}} uses metadata enrichment within its own context to prepare data for analysis. Even if your assets were already enriched in watsonx.data, defining metrics and enriching metadata in watsonx BI helps the AI understand your data and deliver accurate responses and insights.



Follow these integration steps to successfully access watsonx BI functionality within watsonx.data Premium.

## Creating metrics  
{: #create_metrics_wxd}

To create metrics within the Business Intelligence context, follow these steps:

1. From the watsonx.data home page, change the context to **Business Intelligence** by using the Experience switcher. You are now in the watsonx BI conversation interface.

1. Go to the **Data and Metrics** tab from the side panel and click the **+** icon next to the project list to create a project.

1. Go back to the watsonx.data context through the Experience switcher. 

1. Select the newly created project on the watsonx.data home page and select **Business intelligence** from the **Based on your interests** dropdown.

1. Click the **Create metrics** tile.

1. On the **Data and Metrics > Metrics** page, click **Create metrics**.

1. Enter the name of the semantic data model when prompted.

1. Add data by creating a new data connection. 

  Be sure to test the connection before proceeding.
  {: important}

1. Select data and click **Next** until you reach the **Metadata enrichment** page.

1. Metadata enrichment runs automatically.

  Metadata enrichment is a critical step in {{site.data.keyword.wxbia_short}}, which uses AI to transform raw data into a semantically rich dataset by adding business terms and descriptions. These enriched assets form the semantic data model, providing the business context that drives insights across {{site.data.keyword.wxbia_short}}.
 
1. [Review metadata enrichment](/docs/watsonx-bi?topic=watsonx-bi-review){: external} to ensure that the metadata applied is meaningful and accurate. Enrichment results open in a new tab. Changes save automatically.

1. Return to the **Metadata enrichment** page in watsonx BI and click **Next**. 

1. On the **Metrics overview** page, you can create metrics by:

  - [Generating them automatically](/docs/watsonx-bi?topic=watsonx-bi-generate_metrics){: external}  
  
  - [Building them manually](/docs/watsonx-bi?topic=watsonx-bi-advanced_mode){: external} 

14. Navigate back to the **Metrics overview** page after creating metrics. You can see your metrics and their enrichment status. 

  You can now do the following:

  a. [Try a metric in a conversation](/docs/watsonx-bi?topic=watsonx-bi-try_metrics){: external} 
   
  b. [Edit metrics](/docs/watsonx-bi?topic=watsonx-bi-edit_metrics){: external} 

  c. Use the [Advanced mode](/docs/watsonx-bi?topic=watsonx-bi-advanced_mode_model_data){: external} to make changes to the semantic data model

  d. [Add visualizations to metrics](/docs/watsonx-bi?topic=watsonx-bi-add_viz_metrics){: external}  
      
  e. [Publish metrics and visualizations](/docs/watsonx-bi?topic=watsonx-bi-publish_metrics){: external} to the **Metrics catalog** (Data analysts only)

  This is an iterative process. You can explore, adjust, and revisit these steps as needed.
  {: note}    

## Connecting to data
{: #connect_wxd_data}

You can also connect to data from watsonx.data and then create metrics in watsonx BI.

1. From the watsonx.data home page, change the context to **Business Intelligence** by using the Experience switcher. You are now in the watsonx BI conversation interface.

1. Go to the **Data and Metrics** tab from the side panel and click the **+** icon next to the project list to create a project.

1. Switch back to the watsonx.data context through the Experience switcher.

1. Select the newly created project on the watsonx.data home page and select **Business intelligence** from the **Based on your interests** dropdown.

1. Click the **Connect to data** tile.

1. Select a [{{site.data.keyword.wxbia_short}} supported connector](/docs/watsonx-bi?topic=watsonx-bi-supported_connectors_wxbi){: external} and enter the details. 

  Be sure to test the connection.
  {: important}

  After the connection is created, you will be redirected to the **Projects** page.

1. Go to the **Overview** tab, select **Business intelligence** from the dropdown list, and click the **Create metrics** tile. 

1. Enter a name for the semantic data model when prompted. 

1. Select **Existing data source** and choose the connection that you just created. 

  After creating a connection outside the Business Intelligence context, this option might take a few minutes to appear. If it doesn’t show up right away, refresh the page to continue.  

1. Select the tables and click **Next**.

1. Metadata enrichment runs automatically. [Review metadata enrichment](/docs/watsonx-bi?topic=watsonx-bi-review){: external} to ensure that the metadata applied is meaningful and accurate. 

1. Return to the **Metadata enrichment** page in watsonx BI and click **Next**. 

1. On the **Metrics overview** page, select **Build in advanced mode**. 

1. From the table context menu, select **Generate metric definition**. 

1. Save the semantic data model.

1. From the context menu of the newly created metric definition, select **Export metric definition**. 

1. Return to the **Metrics overview** page to monitor the enrichment status.

  If the metric enriches with a warning, click the **Advanced mode** link and go to the **Grid** tab to review the data. This can happen if the created connection was set with private credentials. In some cases, you might be prompted to enter your login details. After logging in, export the metric definition again and return to the **Metrics overview** page. 
  {: important}

1. After enrichment completes successfully, the metric is ready to be used. You can now do the following:

  a. [Try a metric in a conversation](/docs/watsonx-bi?topic=watsonx-bi-try_metrics){: external} 
   
  b. [Edit metrics](/docs/watsonx-bi?topic=watsonx-bi-edit_metrics){: external} 

  c. Use the [Advanced mode](/docs/watsonx-bi?topic=watsonx-bi-advanced_mode_model_data){: external} to make changes to the semantic data model

  d. [Add visualizations to metrics](/docs/watsonx-bi?topic=watsonx-bi-add_viz_metrics){: external}  
      
  e. [Publish metrics and visualizations](/docs/watsonx-bi?topic=watsonx-bi-publish_metrics){: external} to the **Metrics catalog** (Data analysts only)

  This is an iterative process. You can explore, adjust, and revisit these steps as needed.
  {: note}


## Chatting with data
{: #chat_data_wxd}

You can ask questions about data and metrics that you have access to that have been enriched in {{site.data.keyword.wxbia_short}}.  

1. On the watsonx.data home page, select your project and choose **Business intelligence** from the **Based on your interests** dropdown.

1. Click the **Chat with data** tile to open the **Conversations** tab in {{site.data.keyword.wxbia_short}}.

A new conversation is created that is scoped to the selected project. {{site.data.keyword.wxbia_short_cap}} will answer your questions based on the data in that project.



## Related links
{: #wxdpremium_resources}

- [Asking questions in natural language](/docs/watsonx-bi?topic=watsonx-bi-ask){: external}
- [Understanding metadata enrichment in watsonx BI](/docs/watsonx-bi?topic=watsonx-bi-concepts_enrichment){: external}
- [Optimizing data for AI](/docs/watsonx-bi?topic=watsonx-bi-best_practices){: external}
- [Known issues in watsonx BI on IBM Software Hub](/docs/watsonx-bi?topic=watsonx-bi-known_issues_software){: external}.
