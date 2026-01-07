---
copyright:
  years: 2025
lastupdated: "2026-01-07"

keywords: cognos analytics, cognos, FM package
subcollection: watsonx-bi



---

{{site.data.keyword.attribute-definition-list}}


# IBM Cognos Analytics
{: #cognos}

[Preview]{: tag-teal} IBM Cognos Analytics is a business intelligence platform that supports the entire analytics cycle. By integrating Cognos Analytics with {{site.data.keyword.wxbia_full_notm}}, the rich metadata from Cognos Analytics becomes accessible to AI, making it easier for you to get insights from your data. {: #shortdesc} 

{{site.data.keyword.wxbia_full_notm}} and Cognos Analytics integration requires the IBM Cognos Analytics connector.  

This feature is a Technology Preview feature. Technology Preview offers customers early access to product features, allowing them to explore functionality and share feedback during development. These features are provided for evaluation purposes and might not be fully functional or complete.
{: important}


## Prerequisites
{: #prereq}

- A working {{site.data.keyword.wxbia_short}} environment

- A working Cognos Analytics environment

- A Framework Manager package (also called FM package)

- For Cognos Analytics on Premises, you need to create and set up a [Satellite Connector](/docs/watsonx-bi?topic=watsonx-bi-satellite){: external}.

## Limitations
{: #limitations_ca}

- Only relational FM packages are supported
- Dimensionally modelled (DMR) objects are not supported
- Data modules, dynamic cubes, uploaded files, and OLAP sources (such as SAP) are not supported 

## Supported versions
{: #supported_version}

IBM Cognos Analytics 11.2.4 and later

## Connecting to an FM package
{: #connect_FM}

Before you start, select the project that you want to work in or create a new project. You can quickly create a new project from the **Data and Metrics** tab by clicking the '+' button next to the project switcher.
{: Requirement}

1. Go to the project view by clicking **Navigation Menu > View all projects** and select the project.  

2. Go to the **Assets** tab and click **New asset**. 

3. Select **Import metadata for data assets**.

   If you see the following message on the screen, you **Can't fetch information about platform assets catalog**. Close this notification to proceed to the next step.
   {: tip}

4. Define the details and click **Next**.

5. Under **Define goals**, select **Import asset metadata** and click **Next**.

6. Under **Select source and scope**, select **Connection**.

7. Choose an existing IBM Cognos Analytics connection or click **Create a new connection**. If you chose **Create a new connection**, follow steps 7a to 7c. Otherwise, skip to step 8. 

    **a.** Select IBM Cognos Analytics from the list of connectors and click **Next**.

    **b.** Enter the connection details. Make sure that you enter the Gateway URL in the format that is specified in the field: http://hostname:9300/bi/v1/disp 

   If you're connecting to Cognos Analytics on Premises, you need to enter the Gateway URL, Credentials, and select the Satellite Connector under Private connectivity.
   {: note}

    **c.** Test the connection, then click **Create**.

8. Select **Scope** and click **Select assets**.

9. Go to the **Team Content** folder, you can select the folder that the Framework Manager (FM) package is in or the FM package that you want to import and click **Select**.

   If you choose a folder, which contains more than one FM package, a separate semantic model for each package will be created. The semantic data model names are derived from the FM package name. 
   {: note}  

10. (Optional) Define the job details.

11. (Optional) Set advanced options.

12. Review the details, then click **Create**.

A metadata import process starts, which creates a semantic data model based on the metadata in the FM package. 

Each FM package included in the metadata import creates its own semantic model. FM packages that are based on linked and segmented models behave the same as packages created from a single model. 
{: note}

As the metadata import process runs, you can click the **View metrics** link in the **About this metadata import** panel to see the progress. 

Once the metadata import job is complete, you can work with the data. 

At any time, you can go to the project from **Navigation Menu > Projects > View all projects > select your project > Assets** to see the metadata import, semantic data model, and metric definition assets created in this process. 
{: tip}

## Next steps
{: #next_ca_steps}

1. Click **Home** and go to **Data and Metrics**. 

2. Open the semantic data model for the FM package that you imported.

3. Click **Advanced mode** on the **Metrics overview** page, to review the relationships and metric definitions in the view. 

      {{site.data.keyword.wxbia_full_notm}} automatically generates metric definitions from the Fact table in the FM package. Each metric definition is named after the first measure that is in the collection.

      The determinants that are defined in the model specify the attributes that will be included in the metric definition.  

      For example, a metric definition that is created from a Fact table, which has a grain of month, has attributes of the month determinant and those determinants that are above it. This is important as, without it, including attributes below the Fact grain can produce double counting and results in queries taking a long time. 

4. Choose the metric definition that you want to work with and from its menu, select **Export metric definition**. 
   
   When you export a metric definition, it creates or updates a metric and makes it available for use in {{site.data.keyword.wxbia_short}}. This process also allows the data in the metric definition to go through metadata enrichment, which is required to ask questions about the data.

5. Go to **Navigation Menu > Home > Conversations**. 

6. Select the project that you imported metadata to from the list next to the input box and enter your question. 

You can manage the semantic data model, create more metrics, and add visualizations to the metrics from the **Data and Metrics** tab. If you're a **Data analyst**, you can publish metrics and related visualizations to the **Metrics catalog** and assign them to Analytics consumers. 

For more information, see [Overview of creating metrics](/docs/watsonx-bi?topic=watsonx-bi-overview_metrics).

