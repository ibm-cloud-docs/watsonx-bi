---

copyright:
  years: 2025
lastupdated: "2025-08-07"

keywords: known issues, limitations, watsonx BI

subcollection: watsonx-bi

---

{{site.data.keyword.attribute-definition-list}}


# Known issues in {{site.data.keyword.wxbia_short}} on IBM Software Hub
{: #known_issues_software}

The following issues and limitations apply to {{site.data.keyword.wxbia_full}} on IBM Software Hub 5.2.0. {: shortdesc}

- **Analytics consumers are unable to create metrics**
  
  Analytics consumers who use {{site.data.keyword.wxbia_short}} on IBM® Software Hub 5.2 are assigned the User role. The User role in IBM Software Hub has no permissions that are assigned to it. Analytics consumers who start the metric creation process will run into a metadata import error, which prevents them from creating metrics. 
  
  This issue does not impact Data analysts.

  Workaround:
  
  Data analysts can create and publish metrics and related visualizations to the **Metrics catalog**, and assign them to Analytics consumers.

- **Certain predefined roles allow users to set up {{site.data.keyword.wxbia_short}} without being invited first**

  Any user that is added to IBM Software Hub and has direct access to the User, Data steward, or Administrator role can access {{site.data.keyword.wxbia_short}} and go through the setup experience without being invited to the {{site.data.keyword.wxbia_short}} community. Removing such a user from the {{site.data.keyword.wxbia_short}} community can also prevent them from accessing IBM Software Hub.

  Workaround: 

  Administrators must check to ensure that users are added to the {{site.data.keyword.wxbia_short}} community and that, when users are removed from the {{site.data.keyword.wxbia_short}} community, that they continue to have access to IBM Software Hub.

- **Home in the Navigation menu doesn't bring users back to Conversations**

  The **Home** option in the **Navigation menu** doesn't bring users back to {{site.data.keyword.wxbia_short}} **Conversations**.

  Workaround:

  Users can manually change the URL to redirect them back to the watsonx BI **Conversations** page. Change the URL by removing all content that appears in the URL after .com and replace it with wxbi/conversations.

- **Administrators can access all projects on Data and Metrics, regardless of permissions**

  Users with the Administrator role in watsonx BI can view all projects in the cluster on the **Data and Metrics** page, including those that they don't have access to. Administrators who try to create metrics in a project that they don't have access to will encounter an error.

  Workaround:

  Administrators can view the projects that they explicitly have access to under **Navigation menu > Projects**.  

- **Help links are not working**

  The main **Help** link and the **Documentation** link in the **Navigation menu** do not take users to the product documentation.

  Workaround:
  
  Users can get product help through:
  
  - [Product documentation](https://cloud.ibm.com/docs/watsonx-bi) in IBM Cloud Docs
  
  - Documentation for [{{site.data.keyword.wxbia_short}} on IBM Software Hub 5.2](https://www.ibm.com/docs/software-hub/5.2.x?topic=services-watsonx-bi)


- **Unable to create new connections (intermittent issue)**

  Users might encounter an error when they try to create a new connection during the **Create metrics** process. This is an intermittent issue and might occur when the session expires before the user clicks the **New connection** button on the **Connections** page.

  Workaround:

  Users can reload the page and after logging in, will be redirected to the **Connections** page. They can then try to create a new connection again. If the issue persists, users can contact [IBM Support](https://www.ibm.com/mysupport/s/?language=en_US) for help.

- **User permission level misalignment**
   
  Users can be assigned editor-level permissions at the Platform level, while retaining read-only access within individual Projects. There is a known issue affecting user permission configurations across Platform and Project levels. This might lead to an unintended misalignment, where users invited to a Project with read-only permissions (Viewer role) can still modify project assets such as database connection details via Platform user interface.


## Limitations
{: #limitations}

- **Importing and exporting project is not currently supported**

At this time, users cannot import or export projects.

- **Samples are not fully supported**

The prebuilt sample data, Go sales and Customer experience, are not fully supported in this release and are not functional.
