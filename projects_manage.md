---
copyright:
  years: 2025
lastupdated: "2026-01-07"

keywords: add collaborators, projects
subcollection: watsonx-bi



---

{{site.data.keyword.attribute-definition-list}}


# Adding collaborators to a project
{: #managing_projects}

After you create a project, you can add collaborators to the project to work with the assets in the project.{: #shortdesc}

When you add a collaborator to a project, you specify the actions that the user can do by assigning a role.

These roles provide permissions for projects:

- Viewer: View the project

  Viewers cannot perform any of the following actions within that project:

  - Create metrics
  - Delete metrics
  - Delete semantic data models
  - Generate or build visualizations
  - Publish metrics and visualizations
  - Edit visualization
  - Delete visualization

- Editor: Control project assets

- Admin: Control project assets, collaborators, and settings

To add collaborators to your project:

1. Go to **Navigation Menu > View all projects** and select your project. 

2. From your project, click the **Access Control** page on the **Manage** tab.

3. Click **Add collaborators** then select **Add users**, **Add service IDs**, or **Add user groups**.

   - Users: Enter email addresses into the **Find users** field. 

   - Service IDs: In the **Find service IDs** field, search for the service name or description and select the one you want.

   - User groups: In the **Find groups** field, search for user groups and select the one you want.

4. Choose the role for the collaborators and click **Add**:

5. Select the access level and click **Add**.

When collaborators start using the shared project, they might be prompted to enter their personal credentials to the data source connection when they start a conversation or work with metrics in the semantic data model.
{: note}

