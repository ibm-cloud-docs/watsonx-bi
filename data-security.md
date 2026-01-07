---
copyright:
  years: 2026
lastupdated: "2026-01-07"

keywords:
subcollection: watsonx-bi

---

{{site.data.keyword.attribute-definition-list}}


# Securing your data in {{site.data.keyword.wxbia_short}} as a Service
{: #security}

{{site.data.keyword.wxbia_full}} uses the cloud service platform which lets you connect to your data, govern it, find it, and use it for analysis. The cloud service platform offers data security mechanisms, such as encryption and protects sensitive customer and corporate data, both in transit and at rest. {: #shortdesc}

To use {{site.data.keyword.wxbia_short}} as a Service, you need to have a secure [IBM Cloud Object Storage](/docs/cloud-object-storage?topic=cloud-object-storage-getting-started-cloud-object-storage) instance. The IBM Cloud account owner or Administrator, can provision an instance of Cloud Object Storage to the IBM Cloud account. Cloud object storage stores data assets from your projects (including your anything that you connect to or upload), conversations, and the **Metrics catalog**. 

The IBM Cloud Identity and [Access Management (IAM)](/docs/cloud-object-storage?topic=cloud-object-storage-iam-overview) service securely authenticates users and controls access to Cloud Object Storage. 

{{site.data.keyword.wxbia_short_cap}} does not support context-based restrictions. Context-based restrictions give account owners and Administrators the ability to define and enforce access restrictions for resources based on the context of access requests.
{: note}

For more information, see [Data security](https://dataplatform.cloud.ibm.com/docs/content/wsj/getting-started/security-data.html?context=cpdaas&audience=wdp&locale=en#configuring-cloud-object-storage).

