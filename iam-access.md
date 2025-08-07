---
copyright:
  years: 2025
lastupdated: "2025-08-06"

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

When you assign collaborator roles in {{site.data.keyword.wxbia_short}}, the related IAM Service role automatically gets assigned. 
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

Access groups expedite role assignments by grouping permissions for large numbers of users. You create a group and assign policies and rules to the group. When you assign a user to an access group, their access rights are determined by the group policies. All members of an access group have the same access permissions, and all members are updated when the group is edited.

Select **Configuration and settings > Access(IAM) > Access groups** to set up access groups for {{site.data.keyword.wxbia_short}}.

You can also indicate the access group when you invite users to the account.

## Assigning roles individually
{: #assign_individual}

Roles can be assigned to individual users. Select **Configuration and settings > Access(IAM) > Users > Assign access** for each user.

You can also indicate the access policy when you invite users to the account.
