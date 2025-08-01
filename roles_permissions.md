---
copyright:
  years: 2025
lastupdated: "2025-07-29"

keywords: roles, permissions, access
subcollection: watsonx-bi



---

{{site.data.keyword.attribute-definition-list}}


# Roles and permissions 
{: #roles}

Review the roles and permissions that you need for working with watsonx BI.{: #shortdesc}

IBM watsonx BI users require two types of roles:

- Roles assigned in watsonx BI, which are called Collaborator roles

- Service roles:

  - Roles assigned in IBM Cloud, which are called IAM roles, if you're using watsonx BI as a Service

  - Predefined roles, if you're using watsonx BI on IBM Software Hub

## Assigning collaborator roles
{: #collab_roles}

An Administrator can assign collaborator roles from the **Administration > Configurations and settings > Manage BI community** page.  These roles control access to the actions that can be taken in watsonx BI.

- **Analytics consumers**: Analytics consumers can ask questions about their data and monitor metrics that were assigned to them. Analytics consumers can create metrics but cannot give access to metrics, publish metrics to the **Metrics catalog**, or edit published metrics.

- **Data analysts**: Data analysts can create and publish metrics, assign metrics to Analytics consumers, and manage data. Writer role includes permissions for Viewer.

- **Administrator**: Administrators can add users and assign roles and other configuration tasks. Administrator role includes permissions for Reader and Writer.

To add members to the community:

1. From the **Navigation menu**, go to **Administration > Configurations and settings > Manage BI community** page.

2. Click **Add members** and choose if you want to add individual users or groups. 

3. Select the individual users or access groups and assign the relevant collaborator role. 

When you assign collaborator roles, the related service role automatically gets assigned. 

The IBM Cloud account owner or Administrator can modify the IAM Service and Platform roles, if required. For more information, see [IBM Cloud IAM roles](/docs/account?topic=account-userroles){: external}.
{: note}

The following table shows the actions that you can complete depending on your collaborator role.

Data analysts can give access to metrics in the **Metrics catalog** to individual users or user groups. To view the details of a user group that can access a metric, Data analysts need to have the **Viewer** IAM Platform role. 
{: important}

Action |Administrator | Data analyst | Analytics consumer
|---------------| -----|------|---------|
|**watsonx BI setup**|
|[Cloud]{: tag-blue} Change large language model | ✓ | x | x |
|Add or delete user groups | ✓ | x | x |
|Assign and modify roles | ✓ | x | x |
|**Conversations** |
|View, create, and delete chats| ✓ | ✓ | ✓ |
|View key metrics| ✓ | ✓ | ✓ |
|Open metric card | ✓ | ✓ | ✓ | 
|Pin metric from chat | ✓ | ✓ | ✓ |
|**Data and Metrics**|
|Create projects | ✓ | ✓ | ✓ |
|[Cloud]{: tag-blue} Import/export projects | ✓ | ✓ | ✓ |
|Create metrics | ✓ | ✓ | ✓ |
|[Cloud]{: tag-blue} Upload files | ✓ | ✓ | ✓ |
|Manage semantic data models | ✓ | ✓ | ✓ |
|Publish metrics to Metrics catalog | ✓ | ✓ | x |
|**Metrics catalog**|
|Access metrics in Metrics catalog | ✓ | ✓ | ✓ |
|Assign metrics to users | ✓ | ✓ | x |
|Pin metric to Key metrics from Metrics catalog | ✓ | ✓ | ✓ |
{: caption="Permissions by role for watsonx BI features" caption-side="bottom"}
