---
copyright:
  years: 2025
lastupdated: "2025-06-26"

keywords: cognos analytics, cognos, FM
subcollection: watsonx-bi



---

{:codeblock: .codeblock}
{:note: .note}
{:pre: .pre}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:table: .aria-labeledby="caption"}
{:tip: .tip}
{:video: .video}
{:external: target="_blank" .external}
{:step: data-tutorial-type='step'}

# Connecting to Cognos Analytics 
{: #cognos}

IBM Cognos Analytics is a business intelligence platform that supports the entire analytics cycle. By integrating Cognos Analytics with IBM watsonx BI, the rich metadata from Cognos Analytics becomes accessible to AI, making it easier for you to get insights from your data. {: #shortdesc}
 
IBM watsonx BI and Cognos Analytics integration requires the IBM Cognos Analytics connector. 

## Prerequisites
{: #prereq}

- A working watsonx BI environment.

- A working Cognos Analytics environment.

- A Framework Manager package (also called FM package) that was created in IBM Cognos Framework Manager. 

- For Cognos Analytics on Premises, you need to create and set up a [Satellite Connector](/docs/watsonx-bi?topic=watsonx-bi-satellite).

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

As the metadata import process runs, you can click the **View metrics** link in the **About this metadata import** panel to see the progress. 

Once the metadata import job is complete, you can work with the data. 

Use the breadcrumbs to navigate to the project. Under the **Asset** tab, you can see the semantic data model that was just created and the metadata import asset.

## Next steps
{: #next_ca_steps}

Once you connect to your FM package in Cognos Analytics, you can ask questions about the imported metadata. 

1. Click the semantic data model asset to open it.

2. Review the relationships and metric definitions in the view. 
   
   IBM watsonx BI automatically creates metric definitions from the Fact table in the FM package. Each metric definition is automatically named after the first measure that is in the collection.

3. Choose the metric definition that you want to work with and from its menu, select **Export and enrich metric**. 
   
   Exporting and enriching a metric definition creates or updates a metric and makes it available for use in watsonx BI. This process also allows the data in the metric definition to go through metadata enrichment, which is required to ask questions about the data.

4. Use the breadcrumbs to navigate to the project. You can now see a metric definition and metadata enrichment asset in the **Assets** tab.

5. Go to **Navigation Menu > Home > Conversations**. 

6. Select the project that you imported metadata to and enter your question. 

At any time, you can go to the **Data and Metrics** tab to manage the semantic data model, create more metrics, and add visualizations to the metrics. If you're a **Data analyst**, you can publish metrics and related visualizations to the **Metrics catalog** and assign them to Analytics consumers. 

For more information, see [Overview of creating metrics](/docs/watsonx-bi?topic=watsonx-bi-overview_metrics).
