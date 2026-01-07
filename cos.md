---
copyright:
  years: 2025
lastupdated: "2026-01-07"

keywords: cloud object storage
subcollection: watsonx-bi


---

{{site.data.keyword.attribute-definition-list}}


# IBM Cloud Object Storage 
{: #cos}

IBM Cloud® Object Storage is a highly available, durable, and secure platform for storing unstructured data. Object storage is the most efficient way to store PDFs, media files, database backups, disk images, or even large structured datasets. {: #shortdesc}

The files that are uploaded into IBM Cloud Object Storage are called **objects**. They are organized into **buckets** that serve as containers for objects, and which can be configured independently from one another in terms of locations, resiliency, billing rates, security, and object lifecycle. 

{{site.data.keyword.wxbia_full}} requires an instance of IBM Cloud Object Storage for creating your first project and storing: 

- Projects

- Sampled data

- Metrics

- Uploaded data

- Metrics catalog

- Conversations 

As the IBM Cloud account owner or Administrator, you provision an instance of Cloud Object Storage. 

## New Cloud Object Storage instance
{: #new_cos}

To provision an instance of IBM Cloud Object Storage:

1. Log in to IBM Cloud.

2. On the homepage, select **Create resource**.

3. Search for the Object Storage tile and select it.

4. Select a plan and give the service instance a name.

   The Standard plan includes a Free Tier with 5GB of free monthly usage for 12 months.

You can now select this Cloud object storage instance when you provision {{site.data.keyword.wxbia_short}}. 

For more information, see [Getting started with IBM Cloud Object Storage](/docs/cloud-object-storage?topic=cloud-object-storage-about-cloud-object-storage){: external}.

## Managing Cloud Object Storage 
{: #manage_cos}

You can administer the Cloud Object Storage from the **Resource list > Storage** page in the IBM Cloud account.  

You can upload and download assets, manage buckets, and configure credentials, and other security settings for the Cloud Object Storage instance.

