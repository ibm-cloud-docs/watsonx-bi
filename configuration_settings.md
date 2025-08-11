---
copyright:
  years: 2025
lastupdated: "2025-08-11"

keywords: configuration and settings
subcollection: watsonx-bi


---

{{site.data.keyword.attribute-definition-list}}



# Managing configuration and settings
{: #config_settings}

You can access **Configuration and settings** from **Navigation menu > Administration** and from the left-hand side panel in {{site.data.keyword.wxbia_full_notm}} to manage access to your {{site.data.keyword.wxbia_short}} instance through Manage BI community, manage storage, and set up sample data from here. Depending on your role and permissions, you might be able to make other configuration changes. {: #shortdesc}

Samples are currently not available in {{site.data.keyword.wxbia_short}} on IBM Software Hub. 
{: note}

## Manage BI community
{: #manage_bi_comm}

Use **Manage BI community** to add users or user groups that have been invited to your {{site.data.keyword.wxbia_short}} account. You can also manage users here by removing them or my modifying their roles. 

## Sample data [Cloud]{: tag-blue}
{: #sample_config}

You can explore {{site.data.keyword.wxbia_short}}'s features with a prebuilt sample. Each sample is optimized for AI and comes with prebuilt metrics that you can use right away to ask questions in **Conversations**. 

## Storage 
{: #storage}

An instance of storage is required to store the following:

- Projects

- Metrics

- Sampled data

- Uploaded files 

- Metrics catalog

- Your conversations

If you are using {{site.data.keyword.wxbia_short}} as a Service, you can use an existing instance or provision a new instance of IBM Cloud object storage in IBM Cloud. For more information, see [IBM Cloud Object Storage](/docs/watsonx-bi?topic=watsonx-bi-cos){: external}. 

If you're using {{site.data.keyword.wxbia_short}} on IBM Software Hub, see [Storage considerations](https://www.ibm.com/docs/en/software-hub/latest?topic=planning-storage-considerations).

## Access (IAM) Access control
{: #access_control}

To manage access to watsonx BI, you must first invite users to {{site.data.keyword.wxbia_short}} using the Access control or IBM Cloud Manage Access (IAM) tool. Once they accept the invitation, users can be added as members and you can assign them their collaborator roles. For more information, see: 

- [Adding users to the Cloud account](/docs/allowlist/watsonx-bi?topic=watsonx-bi-add_users_account){: external}, if you're using watsonx BI as a Service

- [Managing IBM Software Hub users](https://www.ibm.com/docs/en/software-hub/latest?topic=a-managing-users), if you're using {{site.data.keyword.wxbia_short}} on IBM Software Hub
