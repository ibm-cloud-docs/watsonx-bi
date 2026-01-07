---
copyright:
  years: 2025
lastupdated: "2026-01-07"

keywords: adding users, BI community, members
subcollection: watsonx-bi



---

{{site.data.keyword.attribute-definition-list}}

# Adding users to the Cloud account 
{: #add_users_account}

As a Cloud account owner or Administrator, you add the people in your organization who need access to {{site.data.keyword.wxbia_full}} to the IBM Cloud account and then assign them the appropriate roles for their tasks. {: #shortdesc}

This is a two-step process:

1. Add administrative and non-administrative users to the IBM Cloud account so that they can access the account in general. During this step, you can set up access groups to simplify permissions and role assignment, and assign IAM roles to the users. 

2. Add users to the BI community in watsonx BI so that the invited users can use watsonx BI based on their role. During this step, you will assign collaborator roles. 

There are two types of roles that are required for {{site.data.keyword.wxbia_short}}: 

- [IAM roles](/docs/watsonx-bi?topic=watsonx-bi-managing_iam){: external} - provide Service and Platform level assignments, which determine access to service and platform resources and are set in the IBM Cloud account. 

- [Collaborator roles](/docs/watsonx-bi?topic=watsonx-bi-roles){: external} - determine what the user can do in {{site.data.keyword.wxbia_short}}. 


## Inviting users to the IBM Cloud account 
{: #invite_cloud_account}

### Before you begin
{: #prereq_invite}

Set up access groups to simplify user access policies, role assignment in watsonx BI, and access to projects. For more information, see [Managing IAM access for watsonx BI as a Service](/docs/watsonx-bi?topic=watsonx-bi-managing_iam){: external}. 

### Steps
{: #steps_invite}

1. Go to **Navigation Menu > Administration > Configurations and settings > Access (IAM)** and click **Invite users with Access (IAM)**. 

  You can also invite users directly from your IBM Cloud account by selecting **Manage > IAM > Users**. 

2. On the **IBM Cloud > Users > Invite users** page, enter one or more email addresses that are separated by commas, spaces, or line breaks. The limit is 100 email addresses. The settings apply to all the email addresses.

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

If you invited users as part of an access group, you can immediately add the access group to the watsonx BI community and to a project. If you invited users individually, you need to wait for the users to accept the invitation before you can add them to the watsonx BI community or to projects.
{: important}

## Adding users to the watsonx BI community
{: #add_watsonxBI_community}

1. In watsonx BI, go to the **Navigation Menu** and select **Administration > Configurations and settings > Manage BI community**.

2. Click **Add members** and choose if you want to add individual users or groups. 

3. Select the individual users or access groups and assign the relevant collaborator role. 

For more information about collaborator roles, see [Roles and permissions in {{site.data.keyword.wxbia_short}}](/docs/watsonx-bi?topic=watsonx-bi-roles){: external}.
