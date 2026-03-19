---
copyright:
  years: 2025, 2026
lastupdated: "2026-03-19"

keywords: adding users, BI community, members, administrators
subcollection: watsonx-bi



---

{{site.data.keyword.attribute-definition-list}}

# Enabling administrators to set up watsonx BI
{: #assign_admins}

Users other than the IBM Cloud account owner can be administrators of watsonx BI. 

In most cases, the Cloud account owner completes the initial watsonx BI setup and then assigns the **Administrator** role to additional users from **Administration > Configurations and settings > Manage BI community**. When an existing user is assigned the **Administrator** role, watsonx BI automatically applies the required access policies. Administrators can then manage the service in the same way as the account owner, without needing to manually configure IBM Cloud access.

However, if the Cloud account owner wants to delegate the **initial provisioning and setup of watsonx BI** to another user, additional steps are required. In this **first administrator** scenario, the account is not yet configured for watsonx BI. Along with the **Administrator** role, the user must be granted specific access policies before they can provision and set up the service.

The following table lists the minimum access policies required for administrators to be able to set up watsonx BI:

| Service | Resources |Role |
|-------|-------------|------|
|All Identity and Access enabled services| All | Administrator|
|All Account Management services | All | Administrator | 
|Resource group only | All resource groups in the account| Administrator|
|Cloud Object Storage| All | Manager, Administrator|
|watsonx BI| All | Manager|

This capability gives account owners and Administrators the flexibility to initialize and configure watsonx BI so other users in the account can onboard quickly.

For information about provisioning and setting up watsonx BI, see [Provisioning watsonx BI](/docs/watsonx-bi?topic=watsonx-bi-getting-started){: external}.

## Related links
{: #related_setup}


- [Provisioning watsonx BI](/docs/watsonx-bi?topic=watsonx-bi-getting-started){: external}
  
- [Adding users to the Cloud account](/docs/watsonx-bi?topic=watsonx-bi-add_users_account){: external}

- [Managing IAM access for watsonx BI as a Service](/docs/watsonx-bi?topic=watsonx-bi-managing_iam){: external}

