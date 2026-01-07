---
copyright:
  years: 2025
lastupdated: "2026-01-07"

keywords: configuration and settings
subcollection: watsonx-bi


---

{{site.data.keyword.attribute-definition-list}}



# Managing configuration and settings for administrative users
{: #config_settings}

[Cloud account owners]{: tag-blue} [Account administrators]{: tag-blue}

Administrative users can access **Configuration and settings** from **Navigation Menu > Administration** and from the left-hand side panel in {{site.data.keyword.wxbia_full_notm}} to manage access to the {{site.data.keyword.wxbia_short}} instance through Manage BI community, manage storage, and set up sample data from here. Depending on your role and permissions, you might be able to make other configuration changes. {: #shortdesc}


## Manage BI community
{: #manage_bi_comm}

Use **Manage BI community** to add users or user groups that have been invited to your {{site.data.keyword.wxbia_short}} account. You can also manage users here by removing them or my modifying their roles. 

## Sample data 
{: #sample_config}

You can explore {{site.data.keyword.wxbia_short}}'s features with a prebuilt sample. Each sample is optimized for AI and comes with prebuilt metrics that you can use right away to ask questions in **Conversations**. 

Samples are not supported in {{site.data.keyword.wxbia_short}} on IBM Software Hub. 
{: note}

## Model settings
{: #model_settings_tab}

During the initial setup of {{site.data.keyword.wxbia_short}}, administrative users select the large language model (LLM) that will be used in conversations for all users in the account. 

They can also change the LLM from the **Model settings** tab under **Configuration and settings**. When the LLM selection changes, the change applies at the account level and to new conversations or queries. This means that the change applies to everyone that is a part of the account that has access to {{site.data.keyword.wxbia_short}}.

The ability to choose the LLM is not available in {{site.data.keyword.wxbia_short}} on IBM Software Hub 5.2.x. Watsonx BI on Software Hub 5.2.x uses [IBM Granite-3-8b-instruct](https://www.ibm.com/docs/watsonx/w-and-w/2.2.0?topic=models-granite-30-8b-instruct-model-card){: external} to respond to questions. 
{: note}


## Storage 
{: #storage}

An instance of storage is required to store the following:

- Projects

- Metrics

- Sampled data

- Uploaded files 

- Metrics catalog

- Conversations

If you are using {{site.data.keyword.wxbia_short}} as a Service, you can use an existing instance or provision a new instance of IBM Cloud object storage in IBM Cloud. For more information, see [IBM Cloud Object Storage](/docs/watsonx-bi?topic=watsonx-bi-cos){: external}. 

If you're using {{site.data.keyword.wxbia_short}} on IBM Software Hub, see [Storage considerations](https://www.ibm.com/docs/en/software-hub/latest?topic=planning-storage-considerations).

## Access (IAM) or Access control
{: #access_control}

To manage access to watsonx BI, you must first invite users to {{site.data.keyword.wxbia_short}} using the Access control or IBM Cloud Manage Access (IAM) tool. Once they accept the invitation, users can be added as members and you can assign them their collaborator roles. For more information, see: 

- [Adding users to the Cloud account](/docs/allowlist/watsonx-bi?topic=watsonx-bi-add_users_account){: external}, if you're using watsonx BI as a Service

- [Managing IBM Software Hub users](https://www.ibm.com/docs/en/software-hub/latest?topic=a-managing-users), if you're using {{site.data.keyword.wxbia_short}} on IBM Software Hub


