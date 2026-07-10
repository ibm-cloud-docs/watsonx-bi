---
copyright:
  years: 2025, 2026
lastupdated: "2026-07-10"

keywords: configuration and settings
subcollection: watsonx-bi


---

{{site.data.keyword.attribute-definition-list}}



# Managing configuration and settings for administrative users
{: #config_settings}

[Cloud account owners]{: tag-blue} [Account administrators]{: tag-blue}

Administrative users can access **Configuration and settings** from **Navigation Menu > Administration** to manage access to the {{site.data.keyword.wxbia_short}} instance. You can also manage the BI community and storage, and set up sample data from here. Depending on your role and permissions, you might be able to make other configuration changes. {: #shortdesc}


## Manage BI community
{: #manage_bi_comm}

Use **Manage BI community** to add users or user groups that were invited to your {{site.data.keyword.wxbia_short}} account. You can also manage users here by removing them or my modifying their roles. 

## Sample data 
{: #sample_config}

You can explore {{site.data.keyword.wxbia_short}}'s features with a prebuilt sample. Each sample is optimized for AI and comes with prebuilt metrics that you can use immediately to ask questions in **Conversations**. 

Samples are not supported in {{site.data.keyword.wxbia_short}} on IBM Software Hub. 
{: note}

## Model settings or AI configuration
{: #model_settings_tab}

{{site.data.keyword.wxbia_short}} uses a large language model (LLM) to power conversations and generate insights for all users in the account. 

Administrative users can view the model configuration on the **Configuration and settings > Model settings** page if you use watsonx BI on IBM Software Hub. If you use watsonx BI as a Service, Administrators can view the model configuration on the **Configuration and settings > AI configuration** page. 

The model that is used depends on your deployment type and version.

In {{site.data.keyword.wxbia_short}} as a Service, the model is OpenAI gpt-oss-120b with Chain of thought (CoT) reasoning. In {{site.data.keyword.wxbia_short}} on IBM Software Hub, the available model depends on your version. For more information about models, see [Understanding the large language model (LLM) in your account](/docs/watsonx-bi?topic=watsonx-bi-choose_llm_account){: external}.
{: note}

Administrative users can also choose the metadata enrichment provider on this page. For more information, see [Enriching data in watsonx BI](/docs/watsonx-bi?topic=watsonx-bi-enrich){: external}.


## Storage 
{: #storage}

An instance of storage is required to store the following:

- Projects

- Metrics

- Sampled data

- Uploaded files 

- Metrics catalog

- Conversations

If you are using {{site.data.keyword.wxbia_short}} as a Service, you can use an existing instance or provision a new instance of IBM Cloud Object Storage in IBM Cloud. For more information, see [IBM Cloud Object Storage](/docs/watsonx-bi?topic=watsonx-bi-cloud-object-storage){: external}. 

If you're using {{site.data.keyword.wxbia_short}} on IBM Software Hub, see [Storage considerations](https://www.ibm.com/docs/en/software-hub/latest?topic=planning-storage-considerations).

## Access (IAM) or Access control
{: #access_control}

To manage access to watsonx BI, you must first invite users to {{site.data.keyword.wxbia_short}} by using the Access control or IBM Cloud Manage Access (IAM) tool. After invited users accept the invitation, they can be added as members and you can assign them their collaborator roles. For more information, see: 

- [Adding users to the Cloud account](/docs/allowlist/watsonx-bi?topic=watsonx-bi-add_users_account){: external}, if you're using watsonx BI as a Service

- [Managing IBM Software Hub users](https://www.ibm.com/docs/en/software-hub/latest?topic=a-managing-users), if you're using {{site.data.keyword.wxbia_short}} on IBM Software Hub
