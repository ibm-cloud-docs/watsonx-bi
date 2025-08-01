---
copyright:
  years: 2025
lastupdated: "2025-08-01"

keywords: about watsonx BI
subcollection: watsonx-bi


---

{{site.data.keyword.attribute-definition-list}}

# Feature differences between watsonx BI deployments
{: #diff}

IBM watsonx BI as a Service and IBM watsonx BI software have some differences in features and implementation.  {: #shortdesc}

Watsonx BI as a Service is an IBM Cloud service. Watsonx BI is also available as software that you must install and maintain on [IBM Software Hub](https://www.ibm.com/docs/software-hub/latest?topic=overview).

## Platform differences
{: #platform_differences}

While IBM watsonx BI as a Service and IBM watsonx BI software share a common code base, they differ in the following key ways:

 | Features | As a Service | Software | 
   |-------|-------------|-----------|
   |Software, hardware, and installation	 | IBM watsonx BI is managed on IBM Cloud. Software updates are automatic. Scaling of compute resources and storage is automatic. |You provide and maintain hardware. You install, maintain, and upgrade the software. See [Software requirements](https://www.ibm.com/docs/en/software-hub/5.2.x?topic=services-watsonx-bi).|
   | Storage | You can provision an IBM Cloud Object Storage service instance to provide storage. See [IBM Cloud Object Storage service](/docs/watsonx-bi?topic=watsonx-bi-cos){: external}. | You provide persistent storage on a Red Hat OpenShift cluster. See [Storage considerations](https://www.ibm.com/docs/en/software-hub/latest?topic=planning-storage-considerations). |
   | User management	 | You add users and user groups and manage their account roles and permissions with IBM Cloud Identity and Access Management. See [Managing IAM access for watsonx BI as a Service](/docs/watsonx-bi?topic=watsonx-bi-managing-iam-access-for-watsonx-bi-as-a-service){: external}. | You can add users and create user groups from the **Administration** menu. Use your SAML SSO or LDAP provider for identity and password management. See [Managing users](https://www.ibm.com/docs/en/software-hub/latest?topic=a-managing-users). |
   | Cost | You buy watsonx BI at the appropriate plan level. | You buy a software license based on the services that you need. See [Licenses and entitlements](https://www.ibm.com/docs/en/software-hub/latest?topic=planning-licenses-entitlements). |
   {: caption="{Platform differences}" caption-side="bottom"}

## User interface differences
{: #interface_differences}

The key differences in the user interface of both deployments are:

Navigation menu 

: The Navigation menu in watsonx BI as a Service is tailored for cloud-based account management. The Administration section includes account management options, billing and usage, and access management through IAM.

Conversely, the Navigation menu in watsonx BI software, reflects on-premises options for platform such as the Service catalog and storage volumes. 

Help icon 

: The Help icon in watsonx BI as a Service takes you to the product documentation. 

The same icon in watsonx BI software opens the Assist me feature for in-product context-sensitive help and guidance.

Perspective switcher

: In watsonx BI software, the perspective switcher allows you to toggle between different experiences. This switcher is useful if your environment includes multiple solutions on IBM Software Hub.

This user interface component is not available in watsonx BI as a Service. 

## Features differences 
{: #feature_differences}

While the core functions in both deployments are effectively the same, the following features are not available in watsonx BI software:


- Choose your large language model (LLM)
- Use of sample datasets
- Upload file 
- Import and export project
- Use Framework packages to integrate with Cognos Analytics 
- Provide feedback for generated responses in conversations
