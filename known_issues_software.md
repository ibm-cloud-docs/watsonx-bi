---

copyright:
  years: 2025, 2026
lastupdated: "2026-06-18"

keywords: known issues, limitations, watsonx BI

subcollection: watsonx-bi

---

{{site.data.keyword.attribute-definition-list}}


# Known issues in {{site.data.keyword.wxbia_short}} on IBM Software Hub
{: #known_issues_software}

The following issues and limitations apply to {{site.data.keyword.wxbia_full}} on IBM Software Hub 5.2.0 and later versions. {: #shortdesc}


## Metadata enrichment
{: #ki_mde}

- **Metadata enrichment information appears at the wrong step**

  Applies to: 5.4.0

  Information about how long metadata enrichment takes appears at the **Select data** step, instead of the **Enrich metadata** step. No metadata enrichment occurs at the point where you select data.

## Connector filters
{: #ki_connector}

- **IBM Db2 connector doesn't appear when the watsonx BI filter is applied**
 
  Applies to: 5.3.0 and later

  When you are in the **Add connection** flow and have the watsonx BI filter applied, the IBM Db2 connector doesn't appear in the list of Db2 connectors.

  Workaround:

  Clear the filters and then select the watsonx BI connector.

  When you clear the filter, you see other connectors that are available on IBM® Software Hub, including those that you cannot use with watsonx BI.
{: note}

- **The Connect to data option in the watsonx.data™ experience does not filter for watsonx BI connectors**

  Fixed in: 5.4.0

  If you click **Connect to data** in the watsonx.data experience, you can see connection types that you cannot use with watsonx BI assets.

  Workaround:

  Create connections in the Business Intelligence experience.

## Metric generation
{: #ki_metric_generation}

- **Connections created outside of the Business Intelligence experience are unusable in metric generation**
  
  Fixed in: 5.4.0

  When you try generating metrics from connections and projects that were created outside of the Business Intelligence experience, metric generation fails.

  Workaround: 

  Delete the connection and recreate it by using either the Create metric or the Connect to data tab in the Business intelligence dropdown in watsonx.data.

## Conversations
{: #ki_conversations}

- **Missing AI reasoning and completion messages in conversations**

  Applies to: 5.4.0

  When you send multiple messages in an agentic conversation flow, some AI response messages might not appear in the conversation. Specifically, AI reasoning steps and completion messages might be missing, even though the initial message appears correctly. This issue occurs when the system cannot acquire the necessary lock to cache conversation messages.

- **False error message**

  After you generate metrics and close the **Try in conversation** window, an error message that states **Failed to delete the conversation** might appear.

## Visualizations
{: #ki_visualizations}

- **Five minute wait before visualizations appear in the Metrics catalog**

  Fixed in: 5.4.0

  After you publish visualizations, you must wait approximately 5 minutes before you can see them in the **Metrics catalog**.

- **Visualizations unable to load after pinning**

  Applies to: 5.4.0

  When you pin a visualization from the metrics catalog, the visualization may fail to load.

## Imported projects
{: #ki_imported_projects}

- **Visualizations not loading after project import**

  Applies to: 5.4.0

  When you import a project that had existing visualizations, the visualizations don't load properly.

- **Metrics from imported assets cannot be used**

  Applies to: 5.3.0 - 5.3.1

  Fixed in: 5.4.0

  If you import a project from the watsonx.data experience, the metrics in this project cannot be used with Business Intelligence tools.

- **Database connection error on imported projects**
 
  Applies to: 5.3.0 and later

  If you import a project, then switch to another account without logging in to the second account, you cannot update the credentials for the project.
  
  Workaround: 

  As the user who imported the project, you must enter your personal database credentials before you can share the project with other collaborators.

## Experience issues
{: #ki_experience}

- **Some actions redirect you to the Business Intelligence experience**

  Applies to: 5.4.0

  Certain actions that you perform in the watsonx.data experience redirect you to the same page in the Business Intelligence experience. There is no immediate impact to being in a different experience, but you might encounter issues when performing other actions, such as rendering visualizations. The actions include:

    - Clicking notifications

    - Previewing assets **Fixed in: 5.4.0**

  Workaround:

  Manually switch back to the watsonx.data experience by using the 9-dot switcher.

- **Some tasks fail in projects that are created outside of the Business Intelligence experience**
 
  Applies to: 5.3.0 and later

  If you try to complete certain tasks for projects that are created outside of the Business Intelligence experience, these tasks fail. These tasks include:

   - Metadata enrichment

   - Metric creation

  Workaround:

  Create metrics only in the **Data and Metrics** page. You can access this page by clicking **Create metrics** in watsonx.data when the **Business intelligence** dropdown is selected.

## Deleted files
{: #ki_deleted_files}

- **Deleted files continue to display in the user interface**

  Applies to: 5.3.0 and later

  If you delete files that were uploaded and enriched, then reload the **Data and Metrics** page, the deleted files are still displayed.

  Workaround:

  Approximately 15 minutes after you delete the files, refresh the **Data and Metrics** page. The files no longer display.

- **Overwrite file option appears when you reupload deleted files**

  Applies to: 5.3.0 and later

  If you delete a set of files and later reupload these same files, you have the option to overwrite the files, even though these files no longer exist in the platform assets page.

## File upload
{: #ki_file_upload}

- **False error message during batch file upload**

  Applies to: 5.3.0 and later

  When you upload 10 files at one time, the displayed status shows that the upload job failed, even if the job succeeded.

  Workaround:

  To see whether the enrichment job succeeded or failed, view the enrichment job run metrics.

## Roles and permissions
{: #ki_roles}

- **Changing multiple users' roles at one time fails if search bar isn't clear**

  Applies to: 5.4.0

  When you search for multiple users and try to change their roles at the same time, without clearing the search bar, the page loads indefinitely and the user roles remain unchanged.

  Workaround:

  If you want to change the roles of multiple users at one time, select the users whose roles you want to change, clear the search bar, and then select the users' new roles.

- **Loss of user permission**

  Applies to: 5.3.0 and later

  Due to the introduction of new roles in IBM Software Hub Version 5.3.0, the roles of User, Data Steward, and Administrator no longer apply to watsonx BI users. If you had any of these roles, you might lose access to your watsonx BI community.

  Workaround:

  A user with the role of Business Intelligence Administrator must add users by completing the [Post-upgrade setup for watsonx BI](https://www.ibm.com/docs/software-hub/latest?topic=upgrading-post-upgrade-setup).

- **User permission level misalignment**

  Applies to: 5.2.0 and later

  Users can be assigned editor-level permissions at the Platform level, while retaining read-only access within individual Projects. There is a known issue affecting user permission configurations across Platform and Project levels. This might lead to an unintended misalignment, where users invited to a Project with read-only permissions (Viewer role) can still modify project assets such as database connection details via Platform user interface.

## Links to documentation
{: #ki_docs}

- **Help links are not working**

  Applies to: 5.2.0 and later

  The main **Help** link and the **Documentation** link in the **Navigation menu** do not lead to product documentation.

  Workaround:

  Users can get product help through the following links

   - [Product documentation](https://cloud.ibm.com/docs/watsonx-bi) in IBM Cloud Docs
  
   - Documentation for [{{site.data.keyword.wxbia_short}} on IBM Software Hub 5.2](https://www.ibm.com/docs/software-hub/5.2.x?topic=services-watsonx-bi)
   - [Installing watsonx BI](https://www.ibm.com/docs/software-hub/latest?topic=services-installing-watsonx-bi)

   - [watsonx BI product documentation](https://cloud.ibm.com/docs/watsonx-bi)


## Limitations
{: #current_limitations}

- **Response feedback is not supported in watsonx BI on IBM Software Hub**

  This feedback feature is only available in watsonx BI as a Service.

- **All watsonx.data Premium assets must go through the watsonx.data metric creation flow**

  Metadata enrichment in watsonx.data Premium does not prepare assets for use in watsonx BI. To use watsonx.data Premium assets in watsonx BI, you must go through the watsonx BI metric creation flow. 

  If you import a project from the watsonx.data experience, any metrics in this project cannot be used with Business Intelligence tools.
