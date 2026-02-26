---

copyright:
  years: 2025
lastupdated: "2026-02-26"

keywords: known issues, limitations, watsonx BI

subcollection: watsonx-bi

---

{{site.data.keyword.attribute-definition-list}}


# Known issues in {{site.data.keyword.wxbia_short}} on IBM Software Hub
{: #known_issues_software}

The following issues and limitations apply to {{site.data.keyword.wxbia_full}} on IBM Software Hub 5.2.0 and later versions. {: shortdesc}


## Connector filters
{: ki_connector}

**IBM Db2 connector doesn't appear when the watsonx BI filter is applied**
 
 Applies to: 5.3.0

 When you are in the **Add connection** flow and have the watsonx BI filter applied, the IBM Db2 connector doesn't appear in the list of Db2 connectors.

 Workaround:

 Clear the filters and then select the watsonx BI connector.

 When you clear the filter, you see other connectors that are available on IBM® Software Hub, including those that you cannot use with watsonx BI.
 {: note}

**The Connect to data option in the watsonx.data™ experience does not filter for watsonx BI connectors**

 Applies to: 5.3.0

 If you click **Connect to data** in the watsonx.data experience, you can see connection types that you cannot use with watsonx BI assets.

 Workaround:

 Create connections in the Business Intelligence experience.

## Metric generation
{: ki_metric_generation}

**Metadata enrichment failure during metric generation for export**
  
 Applies to: 5.3.0

 When you open a semantic model that was created during a previous metadata import step and try to export a metric definition from this model, the metadata enrichment job fails during the profiling step.

**Connections created outside of the Business Intelligence experience are unusable in metric generation**
  
 Applies to: 5.3.0

 When you try generating metrics from connections and projects that were created outside of the Business Intelligence experience, metric generation fails.

 Workaround: 

 Delete the connection and recreate it by using either the Create metric or the Connect to data tabs in the Business intelligence dropdown in watsonx.data.

## Visualizations
{: #ki_visualizations}

**Technical issue when asking questions against visualization in Key metrics**
  
 Applies to: 5.3.0

 After you pin a visualization to **Key metrics**, if you try to ask a question against the visualization, you might get the following response due to a technical issue: *Sorry, I encountered a technical issue on our end and can't answer your question. Try rephrasing your question or ask a different question.*

**Intermittent datasource loading issue on visualization tiles**
  
 Applies to: 5.3.0

 After you build and publish a custom visualization, a *Failed to load datasource* error message might display in the **Metrics catalog**.

 Workaround:

 The issue typically resolves itself after some time. Wait until your visualization appears in the **Metrics catalog**, then try to view the visualization tiles.

**Five minute wait before visualizations appear in the Metrics catalog**

 Applies to: 5.3.0

 After you publish visualizations, you might need to wait approximately 5 minutes before you can see them in the **Metrics catalog**.

## Imported projects
{: ki_imported_projects}

**Metrics from imported assets cannot be used**

 Applies to: 5.3.0
  
 If you import a project from the watsonx.data experience, the metrics in this project cannot be used with Business Intelligence tools.

**Database connection error on imported projects**
 
 Applies to: 5.3.0

 If you import a project, then switch to another account without logging in to the second account, you cannot update the credentials for the project.
  
 Workaround: 

 As the user who imported the project, you must enter your personal database credentials before you can share the project with other collaborators.

## Navigation menu
{: #ki_nav_menu}

**View all catalogs option is missing from the Navigation Menu**
 
 Applies to: 5.3.0

 When you click the **Navigation Menu** while you are in the watsonx.data experience, the **View all catalogs** option is not shown under the **Catalogs** dropdown.

## Experience issues
{: #ki_experience}

**Experience is not perserved during certain navigation**
 
 Applies to: 5.3.0

 Certain actions that you perform in the watsonx.data experience redirect you to the same page in the Business Intelligence experience. There is no immediate impact to being in a different experience, but you might encounter issues when performing other actions, such as rendering visualizations. The actions include:

 - Viewing imported projects
 - Clicking notifications
 - Previewing assets
 - Navigating to the **Metrics overview** page
 - Clicking **Home** in the **Metadata enrichment** view

 Workaround:

 Manually switch back to the watsonx.data experience by using the 9-dot switcher.

**Some tasks fail in projects that are created outside of the Business Intelligence experience**
 
 Applies to: 5.3.0

 If you try complete certain tasks for projects created outside of the Business Intelligence experience, these tasks fail. These tasks include:
 
 - Metadata enrichment
 - Metric creation
 - Metric publishing
 
 Workaround:

 Create metrics only in the **Data and Metrics** page. You can access this page by clicking **Create metrics** in watsonx.data when the **Business intelligence** dropdown is selected.



## Semantic data model creation
{: #ki_semantic_model}

**Semantic data model creation fails in shared projects for everyone besides the Administrative user**
 
 Applies to: 5.3.0
 
 If a project is shared with a user who has the project permission of Editor, and the Editor tries to create a semantic data model, the creation fails.

 Workaround: 

 As the Administrative user, you must create the semantic data model in your projects. Click **Create metrics** to create a semantic data model.

## Deleted files
{: #ki_deleted_files}

**Deleted files continue to display in the user interface**
 
 Applies to: 5.3.0

 If you delete files that were uploaded and enriched, then reload the **Data and Metrics** page, the files still display after they were deleted.

 Workaround: 

 Wait approximately 15 minutes after you delete the files, then refresh the **Data and Metrics** page. The files no longer display. 

**Overwrite file option appears when you reupload deleted files**
 
 Applies to: 5.3.0

 If you delete a set of files and later re-upload these same files, you get the option to overwrite the files, even though these files no longer exist in the platform assets page.

## File upload
{: #ki_file_upload}

**False error message during batch file upload**
 
 Applies to: 5.3.0

 When you upload 10 files at one time, the displayed status shows that the upload job failed, even if it the job actually succeeded.

 Workaround:
 To see whether the enrichment job succeeded or failed, view the enrichment job run metrics.

## Roles and permissions
{: #ki_roles}

**Loss of user permission**
 
 Applies to: 5.3.0

 Due to the introduction of new roles in IBM Software Hub Version 5.3.0, the roles of User, Data Steward, and Administrator no longer apply to watsonx BI users. If you had any of these roles, you might lose access to your watsonx BI community.

 Workaround: 
 A user with the role of Business Intelligence Administrator must add users by completing the [Post-upgrade setup for watsonx BI](https://www.ibm.com/docs/software-hub/latest?topic=upgrading-post-upgrade-setup).

**Analytics consumers are unable to create metrics**
  
 Applies to: 5.2.0 - 5.2.2; Fixed: 5.3.0
  
 Analytics consumers who use {{site.data.keyword.wxbia_short}} on IBM® Software Hub 5.2 are assigned the User role, which has no permissions. This causes a metadata import error during metric creation. 
  
 This issue does not impact Data analysts.

 Workaround:
  
 Data analysts can create and publish metrics and related visualizations to the **Metrics catalog**, and assign them to Analytics consumers.

**Certain predefined roles allow users to set up {{site.data.keyword.wxbia_short}} without being invited first**

 Applies to: 5.2.0 - 5.2.2; Fixed: 5.3.0

 Users added to IBM Software Hub with direct access to the User, Data steward, or Administrator role can access {{site.data.keyword.wxbia_short}} and complete setup without being invited to the {{site.data.keyword.wxbia_short}} community. 
  
 Removing such users from the {{site.data.keyword.wxbia_short}} community might also prevent them from accessing IBM Software Hub.

 Workaround: 

 Administrators must verify that users are added to the {{site.data.keyword.wxbia_short}} community and ensure continued access to IBM Software Hub after removal.

**Administrators can access all projects on Data and Metrics, regardless of permissions**
  
 Applies to: 5.2.0 - 5.2.2; Fixed: 5.3.0

 Administrators in watsonx BI can view all projects in the cluster on the **Data and Metrics** page, including those that they don't have access to. Creating metrics in inaccessible projects results in an error.

 Workaround:

 Administrators can view the projects that they explicitly have access to under **Navigation menu > Projects**.  

**User permission level misalignment**

 Applies to: 5.2.0 and later

 Users may have editor-level permissions at the Platform level but only read-only access in Projects. This misalignment allows users with Viewer role to modify project assets via the Platform user interface.

## Links to documentation
{: #ki_docs}

**Help links are not working**

 Applies to: 5.2.0 and later

 The main **Help** link and the **Documentation** link in the **Navigation menu** do not lead to product documentation.

 Workaround:
  
 Users can get product help through:

 - [Product documentation](https://cloud.ibm.com/docs/watsonx-bi) in IBM Cloud Docs
  
 - Documentation for [{{site.data.keyword.wxbia_short}} on IBM Software Hub 5.2](https://www.ibm.com/docs/software-hub/5.2.x?topic=services-watsonx-bi)









## Limitations
{: #limitations}

**Response feedback is not supported in watsonx BI on IBM Software Hub**

This feedback feature is only available in watsonx BI as a Service.

**All watsonx.data Premium assets must go through the watsonx.data metric creation flow**

Metadata enrichment in watsonx.data Premium does not prepare assets for use in watsonx BI. To use watsonx.data Premium assets in watsonx BI, you must go through the watsonx BI metric creation flow. If you import a project from the watsonx.data experience, any metrics in this project cannot be used with Business Intelligence tools.
