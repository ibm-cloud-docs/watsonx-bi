---

copyright:
  years: 2025
lastupdated: "2025-10-31"

keywords: known issues, limitations, watsonx BI

subcollection: watsonx-bi

---

{{site.data.keyword.attribute-definition-list}}


# Known issues in {{site.data.keyword.wxbia_short}} on IBM Software Hub
{: #known_issues_software}

The following issues and limitations apply to {{site.data.keyword.wxbia_full}} on IBM Software Hub 5.2.0 and later versions. {: shortdesc}



- **Unable to upgrade watsonx BI service instances**
  Applies to: 5.2.1
  Fixed in: 5.2.2

  You cannot update an existing watsonx BI service instance.

  Workaround:

  Instead, you must uninstall the watsonx BI operator and service instance, upgrade the IBM Software HUb instance and watsonx BI dependencies, then reinstall the watsonx BI operation and deploy a service instance. For more information, see [Preparing to upgrade to IBM Software Hub 5.2.1](https://www.ibm.com/docs/software-hub/5.2.x?topic=bi-preparing-upgrade-version-521) when watsonx BI is installed.

- **Analytics consumers are unable to create metrics**
  Applies to: 5.2.0 and later
  
  Analytics consumers who use {{site.data.keyword.wxbia_short}} on IBM® Software Hub 5.2 are assigned the User role, which has no permissions. This causes a metadata import error during metric creation. 
  
  This issue does not impact Data analysts.

  Workaround:
  
  Data analysts can create and publish metrics and related visualizations to the **Metrics catalog**, and assign them to Analytics consumers.

- **Certain predefined roles allow users to set up {{site.data.keyword.wxbia_short}} without being invited first**
  Applies to: 5.2.0 and later

  Users added to IBM Software Hub with direct access to the User, Data steward, or Administrator role can access {{site.data.keyword.wxbia_short}} and complete setup without being invited to the {{site.data.keyword.wxbia_short}} community. 
  
  Removing such users from the {{site.data.keyword.wxbia_short}} community might also prevent them from accessing IBM Software Hub.


  Workaround: 

  Administrators must verify that users are added to the {{site.data.keyword.wxbia_short}} community and ensure continued access to IBM Software Hub after removal.

- **Home in the Navigation menu doesn't bring users back to Conversations**
  Applies to: 5.2.0
  Fixed in: 5.2.1

  The **Home** option in the **Navigation menu** doesn't bring users back to {{site.data.keyword.wxbia_short}} **Conversations**.

  Workaround:

  Manually change the URL to redirect to the **Conversations** page by replacing everything after '.com' and replace it with 'wxbi/conversation'.

- **Administrators can access all projects on Data and Metrics, regardless of permissions**
  Applies to: 5.2.0 and later

  Administrators in watsonx BI can view all projects in the cluster on the **Data and Metrics** page, including those that they don't have access to. Creating metrics in inaccessible projects results in an error.

  Workaround:

  Administrators can view the projects that they explicitly have access to under **Navigation menu > Projects**.  

- **Help links are not working**
  Applies to: 5.2.0 and later

  The main **Help** link and the **Documentation** link in the **Navigation menu** do not lead to product documentation.

  Workaround:
  
  Users can get product help through:
  
  - [Product documentation](https://cloud.ibm.com/docs/watsonx-bi) in IBM Cloud Docs
  
  - Documentation for [{{site.data.keyword.wxbia_short}} on IBM Software Hub 5.2](https://www.ibm.com/docs/software-hub/5.2.x?topic=services-watsonx-bi)


- **Unable to create new connections (intermittent issue)**
  Applies to: 5.2.0 and later
  Fixed in: 5.2.2

  Users might encounter an error when creating a new connection during the **Create metrics** process. This might happen when the session expires before the user clicks the **New connection** button on the **Connections** page.

  Workaround:

  Reload the page and log in again to be redirected to **Connections**. If the issue persists, users can contact [IBM Support](https://www.ibm.com/mysupport/s/?language=en_US) for help.

- **User permission level misalignment**
  Applies to: 5.2.0 and later

  Users may have editor-level permissions at the Platform level but only read-only access in Projects. This misalignment allows users with Viewer role to modify project assets via the Platform user interface.


## Limitations
{: #limitations}

- **Response feedback is not supported in watsonx BI on IBM Software Hub**

This feedback feature is only available in watsonx BI as a Service.
