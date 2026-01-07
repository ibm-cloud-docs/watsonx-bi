---
copyright:
  years: 2025
lastupdated: "2026-01-07"

keywords: roles, permissions, access, iam
subcollection: watsonx-bi



---

{{site.data.keyword.attribute-definition-list}}


# Managing IAM access for {{site.data.keyword.wxbia_short}} as a Service
{: #managing_iam}

## Assigning IAM access roles 
{: #access_iam}

As the IBM Cloud account owner or Administrator, you can assign IAM roles to individual users or access groups on IBM Cloud using **Manage > Access (IAM)**. The IAM role assignments provide Platform or Service level permissions for IBM Cloud. {: #shortdesc}

Any of the IAM Platform roles of Viewer, Editor, and Administrator can be assigned to most users who work with {{site.data.keyword.wxbia_short}}. For more information about IAM access, see [IAM access](https://cloud.ibm.com/iam/overview){: external}.

You have two options for assigning IAM roles. You can assign roles to individual users or you can create access groups to expedite role assignment.

When you assign or update collaborator roles in {{site.data.keyword.wxbia_short}}, the related IAM Service role automatically gets assigned. 
{: important}

**Required roles for Analytics consumers**

- IAM Service role: Reader

**Required roles for Data analysts**

- IAM Service role: Writer
- IAM Platform role: Viewer

**Required roles for Administrators**

- IAM Platform role: Administrator
- IAM Service role: Manager

## Working with access groups
{: #access_grps}

IAM access groups are created and managed entirely on IBM Cloud. 

Access groups expedite role assignments by grouping permissions for large numbers of users. You create a group and assign policies and rules to the group. When you assign a user to an access group, their access rights are determined by the group policies. All members of an access group have the same access permissions, and all members are updated when the group is edited.

### Creating an access group 
{: #create_access_grps}

To create an access group: 

1. From {{site.data.keyword.wxbia_short}} as a Service, go to **Administration > Access (IAM)** and click the **IBM Cloud Manage Access (IAM)** link. 

2. In the right-hand panel of your IBM Cloud account, go to **Manage access > Access groups** to see a list of available groups. All accounts have the default Public Access group, which contains all users and Service IDs in the account.

3. Click **Create** to create a new access group. Enter the name and a description. Access group names must be unique. A description helps you remember the purpose of the access group.

4. Create the group.

5. Click **Access > Assign access** to add access policies to the group.

  a. For Service, select watsonx BI and click **Next**.

  b. For Resources, select **All resources** for the scope and click **Next**.

  c. For **Roles and actions**, select the access that you want to assign to this group.
  
  e. Review the parameters, then click **Add**.
  
6. In the **Access summary** panel, click **Assign**.

### Adding users to an access group
{: #add_users_access_grps}

To add users to an access group:

1. From {{site.data.keyword.wxbia_short}} as a Service, go to **Administration > Access (IAM)** and click the **IBM Cloud Manage Access (IAM)** link. 

2. In the right-hand panel of your IBM Cloud account, go to **Manage access > Access groups** to see a list of available groups. All accounts have the default Public Access group, which contains all users and Service IDs in the account.

3. Select the access group that you want to populate with users.

4. Checkmark one or more users to add as members of the access group and click **Add users**.

After creating an IAM access group, a user group is also created in watsonx BI. User groups make it easier to manage a large number of users with similar access requirements when adding users to the watsonx BI community.

You can assign Viewer, Editor or Admin roles to user groups when you add collaborators to projects and spaces.

If a member of the group leaves, the IBM Cloud account administrator can remove the user from the group rather than looking at all of the assets the user has access to.

## Assigning roles individually
{: #assign_individual}

IAM Roles can be assigned to users individually. 

1. From {{site.data.keyword.wxbia_short}} as a Service, go to **Administration > Access (IAM)** and click the **IBM Cloud Manage Access (IAM)** link. 

2. In the right-hand panel of your IBM Cloud account, go to **Users** to see a list of available users.

3. Click the menu icon for the user that you want to assign access and click **Assign access**. 

4. Select **Access policy**:

  a. Under **Service**, enter **watsonx BI** in the search field and select it.

  b. Under **Resources**, select **All resources**. 

  c. Under **Roles and actions**, specify the IAM access that you want to assign to these individual users.

  d. Review the selections and click **Add**.

5. In the **Access summary** panel, click **Assign**. 

