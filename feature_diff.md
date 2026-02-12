---
copyright:
  years: 2025
lastupdated: "2026-02-10"

keywords: about watsonx BI
subcollection: watsonx-bi


---

{{site.data.keyword.attribute-definition-list}}

# Feature differences between {{site.data.keyword.wxbia_short}} deployments
{: #diff}

{{site.data.keyword.wxbia_full}} as a Service and {{site.data.keyword.wxbia_full_notm}} on IBM Software Hub have some differences in features and implementation.  {: #shortdesc}

{{site.data.keyword.wxbia_short_cap}} as a Service is an IBM Cloud service. {{site.data.keyword.wxbia_short_cap}} is also available as software that you must install and maintain on [IBM Software Hub](https://www.ibm.com/docs/software-hub/latest?topic=overview).

## Platform differences
{: #platform_differences}

While {{site.data.keyword.wxbia_short}} as a Service and {{site.data.keyword.wxbia_short}} on IBM Software Hub share a common code base, they differ in the following key ways:

 | Features | As a Service | Software | 
   |-------|-------------|-----------|
   |Software, hardware, and installation	 | IBM {{site.data.keyword.wxbia_short}} is managed on IBM Cloud. Software updates are automatic. Scaling of compute resources and storage is automatic. |You provide and maintain hardware. You install, maintain, and upgrade the software. See [Software requirements](https://www.ibm.com/docs/en/software-hub/5.2.x?topic=services-watsonx-bi).|
   | Storage | You can provision an IBM Cloud Object Storage service instance to provide storage. See [IBM Cloud Object Storage service](/docs/watsonx-bi?topic=watsonx-bi-cos){: external}. | You provide persistent storage on a Red Hat OpenShift cluster. See [Storage considerations](https://www.ibm.com/docs/en/software-hub/latest?topic=planning-storage-considerations). |
   | User management	 | You add users and user groups and manage their account roles and permissions with IBM Cloud Identity and Access Management. See [Managing IAM access for {{site.data.keyword.wxbia_short}} as a Service](/docs/watsonx-bi?topic=watsonx-bi-managing_iam). | You can add users and create user groups from the **Administration** menu. Use your SAML SSO or LDAP provider for identity and password management. See [Managing users](https://www.ibm.com/docs/en/software-hub/latest?topic=a-managing-users). |
   | Cost | You buy {{site.data.keyword.wxbia_short}} at the appropriate plan level. | You buy a software license based on the services that you need. See [Licenses and entitlements](https://www.ibm.com/docs/en/software-hub/latest?topic=planning-licenses-entitlements). |
   {: caption="{Platform differences}" caption-side="bottom"}

## User interface differences
{: #interface_differences}

The key differences in the user interface of both deployments are:

: **Navigation Menu**

: The **Navigation Menu** in {{site.data.keyword.wxbia_short}} as a Service is tailored for cloud-based account management. The Administration section includes account management options, billing and usage, and access management through IAM.

: Conversely, the **Navigation Menu** in {{site.data.keyword.wxbia_short}} software, reflects on-premises options for platform such as the Service catalog and storage volumes. 

: **Help icon**

: The Help icon in {{site.data.keyword.wxbia_short}} as a Service takes you to the product documentation. 

: The same icon in {{site.data.keyword.wxbia_short}} software opens the Assist me feature for in-product context-sensitive help and guidance.

: **Perspective switcher**

: {{site.data.keyword.wxbia_short_cap}} on IBM Software Hub has its own perspective called Business Intelligence. A perspective switcher in the header of the software allows you to toggle between different experiences. This switcher is useful if your environment includes multiple solutions on IBM Software Hub.

: This user interface component is not available in {{site.data.keyword.wxbia_short}} as a Service. 

## Features differences 
{: #feature_differences}

While the core functions in both deployments are effectively the same, the following features are not available in {{site.data.keyword.wxbia_short}} on IBM Software Hub:

- Choose your large language model (LLM) does not support Meta Llama 4 and Granite combination
- Use of Go Sales sample data
- Provide feedback for generated responses in conversations

In IBM Software Hub versions 5.3 and higher, {{site.data.keyword.wxbia_short}} can be accessed from IBM watsonx.data Premium. This feature is not available in {{site.data.keyword.wxbia_short}} as a Service.
