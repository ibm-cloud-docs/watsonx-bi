---
copyright:
  years: 2025
lastupdated: "2025-09-09"

keywords: adding users, BI community, members
subcollection: watsonx-bi



---

{{site.data.keyword.attribute-definition-list}}

# Adding users to the Cloud account 
{: #add_users_account}

As a Cloud account owner or Administrator, you can add people in your organization who need access to {{site.data.keyword.wxbia_full}} to the IBM Cloud account and then assign them the appropriate roles for their tasks. {: #shortdesc}

This is a two-step process:

1. Inviting users to the IBM Cloud account so that users can access the account in general. During this step, you will assign IAM roles to the users.

2. Adding users to the **BI community** in watsonx BI so that the invited users can use watsonx BI. During this step, you will assign collaborator roles. 

There are two types of roles that are required for {{site.data.keyword.wxbia_short}}: 

- [IAM roles](/docs/watsonx-bi?topic=watsonx-bi-managing_iam){: external} - provide Service and Platform level assignments, which determine access to service and platform resources and are set in the IBM Cloud account. 

- [Collaborator roles](/docs/watsonx-bi?topic=watsonx-bi-roles){: external} - determine what the user can do in {{site.data.keyword.wxbia_short}}. 

## Inviting users to the IBM Cloud account 
{: #invite_cloud_account}

1. Go to **Navigation Menu > Administration > Configurations and settings > Access (IAM)** and click **Invite users with Access (IAM)**. 

  You can also invite users directly from your IBM Cloud account by selecting **Manage > IAM > Users**. 

2. On the **IBM Cloud/Users/Invite users** page, enter the email addresses of the users that you want to invite. 

3. Choose how you want to assign access. If you have created an access group with predefined access policies, select **Access groups**. Otherwise, select **Access policy**. 

  If you selected [Access groups](/docs/account?topic=account-access-management-overview#access-groups-iam){: external}, follow these steps to invite members of an access group to the watsonx BI account. 

  a. Select one or more access groups and click **Add** to add the users to the selection.

  b. Click **Invite** under **Access summary**. 

  If you selected [Access policy](/docs/account?topic=account-access-management-overview#access-policies-concept){: external}, follow these steps to invite users to the watsonx BI account.

  a. Under **Service**, enter **watsonx BI** in the search field and select it.

  b. Under **Resources**, select **All resources**. 

  c. Under **Roles and actions**, specify the IAM access that you want to assign. 

  d. Review the selections and click **Add**.

  e. Click **Invite** under **Access summary**. 

The new users receive an email invitation to join the account. 

After the users accept the invitation, you can now add them to the watsonx BI community and assign them collaborator roles to provide the necessary permissions to use {{site.data.keyword.wxbia_short}}.

## Adding users to the watsonx BI community
{: #add_watsonxBI_community}

1. In watsonx BI, go to the **Navigation menu** and select **Administration > Configurations and settings > Manage BI community**.

2. Click **Add members** and choose if you want to add individual users or groups. 

3. Select the individual users or access groups and assign the relevant collaborator role. 

For more information about collaborator roles, see [Roles and permissions in {{site.data.keyword.wxbia_short}}](/docs/watsonx-bi?topic=watsonx-bi-roles){: external}.
