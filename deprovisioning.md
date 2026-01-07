---
copyright:
  years: 2025
lastupdated: "2026-01-07"

keywords: remove, delete, deprovision
subcollection: watsonx-bi


---

{{site.data.keyword.attribute-definition-list}}


# Deprovisioning {{site.data.keyword.wxbia_short}} as a Service
{: #deleting_wxbi}

IBM Cloud account owners can deprovision an instance of {{site.data.keyword.wxbia_full_notm}} as a Service from their IBM Cloud account.  {: #shortdesc}

As a Cloud account owner, when you deprovision a {{site.data.keyword.wxbia_short}} instance, all of the users that are a part of the Cloud account lose access to the service.
{: note}

1.	In your IBM Cloud account, go to the **Resource** list.
2.	Go to the {{site.data.keyword.wxbia_short}} instance in the **AI/Machine learning** list. 
3.	Click **Actions** and select **Delete**.
4.	Enter the phrase specified to confirm that you want to delete the resource and click **Delete**.

Data in {{site.data.keyword.wxbia_short}} is stored in the IBM Cloud Object Storage that is associated with your IBM Cloud account.  When you deprovision a {{site.data.keyword.wxbia_short}} instance, your {{site.data.keyword.wxbia_short}} data, which includes conversations, the Metrics catalog, and assets, remains stored in Cloud Object Storage. For information about managing your data in the Cloud Object Storage, see [Bucket management](/docs/cloud-object-storage?group=bucket-management){: external}. 
