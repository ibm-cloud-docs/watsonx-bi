---
copyright:
  years: 2025
lastupdated: "2026-01-07"

keywords: roles, permissions, access
subcollection: watsonx-bi



---

{{site.data.keyword.attribute-definition-list}}


# Roles and permissions in watsonx BI
{: #roles}

Review the roles and permissions that you need for working with {{site.data.keyword.wxbia_short}}.{: #shortdesc}

{{site.data.keyword.wxbia_short_cap}} users require two types of roles:

- Roles assigned in {{site.data.keyword.wxbia_short}}, which are called collaborator roles

- Service roles:

  - IAM roles, if you're using [{{site.data.keyword.wxbia_short}} as a Service](#collab_roles) 

  - Predefined roles, if you're using [{{site.data.keyword.wxbia_short}} on IBM Software Hub](/docs/watsonx-bi?topic=watsonx-bi-roles-swh)

## Assigning collaborator roles
{: #collab_roles}

An Administrator can assign collaborator roles from the **Navigation Menu > Administration > Configurations and settings > Manage BI community** page. These roles control access to the actions that can be taken in {{site.data.keyword.wxbia_short}}.

- **Analytics consumers**: Analytics consumers can ask questions about their data and monitor metrics that were assigned to them. Analytics consumers can create metrics but cannot give access to metrics, publish metrics to the **Metrics catalog**, or edit published metrics.

- **Data analysts**: Data analysts can create and publish metrics, assign metrics to Analytics consumers, and manage data. Writer role includes permissions for Viewer.

- **Administrator**: Administrators can add users and assign roles and other configuration tasks. Administrator role includes permissions for Reader and Writer.

To add members to the watsonx BI community and assign collaborator roles:

1. Open the **Navigation menu** and go to **Administration > Configurations and settings > Manage BI community**.

2. Click **Add members** and choose if you want to add individual users or groups. 

3. Select the individual users or access groups and assign the relevant collaborator role. 





The following table shows the actions that you can complete depending on your collaborator role.



Action |Administrator | Data analyst | Analytics consumer
|---------------| -----|------|---------|
|**{{site.data.keyword.wxbia_short}} setup**|
|Change large language model | ✓ | x | x |
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
|Upload files | ✓ | ✓ | ✓ |
|Manage semantic data models | ✓ | ✓ | ✓ |
|Publish metrics to Metrics catalog | ✓ | ✓ | x |
|**Metrics catalog**|
|Access metrics in Metrics catalog | ✓ | ✓ | ✓ |
|Assign metrics to users | ✓ | ✓ | x |
|Pin metric to Key metrics from Metrics catalog | ✓ | ✓ | ✓ |
{: caption="Permissions by role for {{site.data.keyword.wxbia_short}} features" caption-side="bottom"}

