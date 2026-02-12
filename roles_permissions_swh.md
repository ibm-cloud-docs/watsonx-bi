---
copyright:
  years: 2025
lastupdated: "2026-02-12"

keywords: roles, permissions, software hub
subcollection: watsonx-bi



---

{{site.data.keyword.attribute-definition-list}}

# Roles and permissions for {{site.data.keyword.wxbia_short}} on IBM Software Hub
{: #roles-swh}

As a {{site.data.keyword.wxbia_short}} user in IBM Software Hub, you have different permissions based on your assigned role. 
{: #shortdesc}

## {{site.data.keyword.wxbia_short}} roles

At the platform level, {{site.data.keyword.wxbia_short}} users have three role options: **Business Intelligence Administrator**, **Business Intelligence Analyst**, and **Business Intelligence Consumer**. These roles correspond to the {{site.data.keyword.wxbia_short}} service-level roles of **Administrator**, **Data analyst**, and **Analytics consumer**, respectively.

At the service level, {{site.data.keyword.wxbia_short}} users have the following access to features:

**Conversations**
:   All users can perform all actions.

**Data and Metrics**
:   All users can perform most actions. Analytics consumers cannot publish metrics to the Metrics
catalog.

**Metrics catalog**
:   All users can perform most actions. Analytics consumers cannot assign metrics to users.

The following table shows permission based on assigned role.

| Permission                          | Business Intelligence Administrator | Business Intelligence Analyst | Business Intelligence Consumer |
|------------------------------------|-------------------------------------|--------------------------------|--------------------------------|
| Access catalogs                    | ✓                                   | ✓                              | x                              |
| Access governance artifacts        | ✓                                   | ✓                              | x                              |
| Add catalog assets to projects     | ✓                                   | ✓                              | x                              |
| Add vaults                         | ✓                                   | x                               | x                              |
| Administer platform                | ✓                                   | x                               | x                               |
| Analyze data                       | ✓                                   | ✓                              | x                               |
| Consume data                       | ✓                                   | ✓                              | ✓                              |
| Create deployment spaces           | ✓                                   | ✓                              | ✓                              |
| Create projects                    | ✓                                   | ✓                              | ✓                              |
| Drill down to issue details        | ✓                                   | x                               | x                               |
| Manage asset discovery             | ✓                                   | ✓                              | ✓                              |
| Manage catalogs                    | ✓                                   | x                               |  x                              |
| Manage data protection rules       | ✓                                   | ✓                              |   x                             |
| Manage data quality SLA rules      | ✓                                   | x                               |   x                             |
| Manage glossary                    | ✓                                   | x                               |   x                             |
| Manage governance categories       | ✓                                   | x                               |   x                             |
| Manage service                     | ✓                                   | x                               |  x                              |
| Manage user groups                 | ✓                                   | x                               |   x                             |
| Manage users                       | ✓                                   | x                               |   x                             |
| Manage vaults and secrets          | ✓                                   | x                               |   x                             |



## Assigning user roles in {{site.data.keyword.wxbia_short}} on IBM Software Hub

You must have the **Business Intelligence Administrator** role to assign roles to other users. You can assign roles when you add a new user or assign different roles to an existing user. 

When you assign a role to a user in the BI community, the user's role is automatically updated to include the equivalent role at the platform level. For example, if you assign a user the role of **Analytics consumer**, in IBM Software Hub, they receive the role of **Business Intelligence Analyst**.

Use only the existing roles in the BI community. Do not create any new roles for your users or groups.
{: note}

**Complete the following steps if you are adding users to IBM Software Hub for the first time:**

1. First, connect an identity provider by going to **IBM Software Hub > Navigation menu > Access control > Identity provider configuration.**

1. Choose which type of identity provider you want to add and provide the required information.

1. Make sure that the users you want to add are in your connected identity provider. Then, click **Users > Add users** to add individual users or **User groups > New user group** to add multiple users with the same role.

1. Provide the required information and assign each user or group the role of **User**.

1. The invited users must accept the invitation to IBM Software Hub. After they accept the invitation, you can proceed to configure user roles in the BI community.

**Complete the following steps if you already have existing users in IBM Software Hub**

1. In the **Business Intelligence** perspective, click **Settings > Configuration and settings** to open the **Manage BI community** tab.

1. Click **Add members** then either **Add users** or **Add groups**.

1. Select the users that you want to add and assign them a role.

**Complete the following steps to assign new roles to an existing user in the BI community:**

1. In the **Business Intelligence** perspective, click the **Settings > Configuration and settings** to open the **Manage BI community** tab.

1. Click the name of the user whose role you want to change and assign the new role.
