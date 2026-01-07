---
copyright:
  years: 2025
lastupdated: "2026-01-07"

keywords:
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

# Installing samples in {{site.data.keyword.wxbia_short}}
{: #using_samples}

You can choose one of the following prebuilt samples to familiarize yourself with {{site.data.keyword.wxbia_short}}. Each sample is optimized for AI and comes with prebuilt metrics that you can use right away to ask questions in **Conversations**. {: #shortdesc}

- [Cloud]{: tag-blue} [Go sales](/docs/watsonx-bi?topic=watsonx-bi-go_sales){: external}

- [Cloud]{: tag-blue}[Software]{: tag-blue} [Customer experience](/docs/watsonx-bi?topic=watsonx-bi-cust_exp){: external}

These samples are a great way to explore: 

- {{site.data.keyword.wxbia_short_cap}}'s natural language interface through conversations, including types of questions you can ask for each sample data

- The structure of a metric definition 

- How sample data was modeled and optimized for AI

You'll be prompted to load a sample when you first setup {{site.data.keyword.wxbia_short}}. 

If you choose not to load sample data at the time of setup, you won't be able to access them later. Only Cloud account owners and Administrators can access sample data from **Configuration and settings** at any time. 
{: note}

During the sample setup, {{site.data.keyword.wxbia_short}} automatically creates a similarly-named project for the sample. 

## Using sample data 
{: #using_sample}

After the sample setup is complete, you can navigate to:  

- **Conversations** to ask questions about the sample data

- **Data and Metrics** to view the associated semantic data model and metric definitions

**Samples in Conversations**
{: #sample_conv}

When you're in **Conversations**, you can set the scope of the conversation to just the sample project, that was created at the time of setup, and ask questions about the data in the sample. You can do this by selecting the sample project name from the list next to the input box and entering your question. 

The conversation will remain scoped to the sample data until you change it from the input box list. 

**Samples in Data and Metrics**
{: #sample_data_metrics}

The **Data and Metrics** tab is where you can create metrics, access semantic data models, and upload files. 

You can access the semantic data model for your sample data on the **Metrics** tab to see how the data was set up and modeled. 

Modifying metric definitions or the semantic data model might cause unexpected results in conversations.
{: attention}

1. On the **Data and Metrics > Metrics** tab, select the sample project name in the list at the top of the page.

2. Open the sample semantic data model.

You are now on the **Metrics overview** page. You can see the sample metric in the **Metrics overview** panel. Click the metric's menu icon and select **View details** to see the scope of the metric and other details.

On the **Metrics overview** page, click **Advanced mode** to view more details such as the  measures, columns, and data tables used in the metric definition, relationships between the tables used, filters applied, calculations, and more. 

Check the column properties. Each one should have a Name, Description, and an Identifier. These properties help AI in retrieving information to answer your question.  
{: tip}

## Next steps
{: #next_sample}

Review these topics for more details about each sample, including examples of questions you can ask against each data set.

- [Go sales](/docs/watsonx-bi?topic=watsonx-bi-go_sales)

- [Customer experience](/docs/watsonx-bi?topic=watsonx-bi-cust_exp) 
