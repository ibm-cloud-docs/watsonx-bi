---
copyright:
  years: 2024
lastupdated: "2025-06-26"

keywords: roles, permissions, access
subcollection: watsonx-bi



---

{{site.data.keyword.attribute-definition-list}}


# Roles and permissions 
{: #roles}

Review the roles and permissions that you need for working with watsonx BI.{: #shortdesc}

IBM watsonx BI users require two types of roles:

- Roles assigned in watsonx BI, which are called Collaborator roles


- Roles assigned in IBM Software Hub, which are the predefined roles

## Assigning collaborator roles
{: #collab_roles}

An Administrator can assign collaborator roles from the **Administration > Configurations and settings > Manage BI community** page.  These roles control access to the actions that can be taken in watsonx BI.

- **Reader**: Analytics consumers (or business users) can ask questions about their data and monitor metrics that were assigned to them. Analytics consumers can create metrics but cannot give access to metrics, publish metrics to the **Metrics catalog**, or edit published metrics.

- **Writer**: Data analysts can create and publish metrics, assign metrics to Analytics consumers, and manage data. Writer role includes permissions for Viewer.

- **Administrator**: Administrators can add users and assign roles and other configuration tasks. Administrator role includes permissions for Reader and Writer.

To add members to the community:

1. From the **Navigation menu**, go to **Administration > Configurations and settings > Manage BI community** page.

2. Click **Add members** and choose if you want to add individual users or groups. 

3. Select the individual users or access groups  and assign the relevant collaborator role. 

When you assign collaborator roles, the related  service role automatically gets assigned. 



The following table shows the actions that you can complete depending on your collaborator role.



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
|Create metrics | ✓ | ✓ | ✓ |
|Manage semantic data models | ✓ | ✓ | ✓ |
|Publish metrics to Metrics catalog | ✓ | ✓ | x |
|**Metrics catalog**|
|Access metrics in Metrics catalog | ✓ | ✓ | ✓ |
|Edit metrics in Metrics catalog | ✓ | ✓ | x |
|Assign metrics to users | ✓ | ✓ | x |
|Pin metric to Key metrics from Metrics catalog | ✓ | ✓ | ✓ |
{: caption="Permissions by role for watsonx BI features" caption-side="bottom"}





### Working with access groups
{: #access_grps}

Access groups expedite role assignments by grouping permissions for large numbers of users. You create a group and assign policies and rules to the group. When you assign a user to an access group, their access rights are determined by the group policies. All members of an access group have the same access permissions, and all members are updated when the group is edited.

Select **Configuration and settings >  Access control > Access groups** to set up access groups for watsonx BI.

You can also indicate the access group when you invite users to the account.

### Assigning roles individually
{: #assign_individual}

Roles can be assigned to individual users. Select **Configuration and settings >  Access control > Users > Assign access** for each user.

You can also indicate the access policy when you invite users to the account.
