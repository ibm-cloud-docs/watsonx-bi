---

copyright:
  years: 2025
lastupdated: "2025-08-11"

keywords: known issues, limitations, watsonx BI

subcollection: watsonx-bi

---

{{site.data.keyword.attribute-definition-list}}


# Known issues in {{site.data.keyword.wxbia_short}} as a Service 
{: #known_issues_cloud}

The following issues and limitations apply to {{site.data.keyword.wxbia_full}} as a Service.  {: shortdesc}

- **Users encounter an error after launching the watsonx BI service from the IBM Cloud catalog**
  
  You might encounter one of the following issues after launching the watsonx BI instance from the IBM Cloud catalog. 

  - Error - Your IBM watsonx BI apps weren't created.

  - You are navigated to the dataplatform home page (https://dataplatform.cloud.ibm.com/home2?context=cpdaas) where there are no links to watsonx BI.

  Workaround:

  - If you encounter the error, Your IBM watsonx BI apps weren't created, you can manually modify the URL to have **context=wdp** or **context=cpdaas**.

  - If you are navigated to the platform home page, re-launch the service or navigate directly to https://dataplatform.cloud.ibm.com/wxbi/conversations.

- **Continous loading state displays in Advanced mode after selecting a metric definition**

  You might encounter this issue if you imported a project, opened a semantic data model from this project from the **Data and Metrics** tab, and selected a metric definition. 

  Workaround:

  You can refresh the page and click the **Grid** tab in the semantic data model before selecting a metric definition.

- **Transferring an IBM Cloud account  that you own requires you to manually add the new owner as an Administrator**

When you transfer ownership of an IBM Cloud account after a watsonx BI instance has been set up, you need to add the new account owner as an Administrator to the:

-  watsonx BI community on **Configurations and settings > Manage BI community**



- **The Sources panel for FM package-based semantic data models does not display details**
  
  In semantic data models that are created from Cognos Analytics FM packages, The **Sources** panel does not display the package details. 
    
  This does not affect your ability to work with the data in these semantic data models. However, it might cause issues if, for example, you remove a table from the semantic data model and want to add it back in later but cannot access it through the **Sources** panel. 
    
  Workaround: 

  In the example scenario, if you have not yet saved the semantic data model, you can click **Undo** to revert the change. If you have already saved the semantic data model, you can re-import the FM package to restore the removed table.
  

## Limitations
{: #limitations_cloud}

- Import and export project does not support local files (.csv, .xls, .xlsx, or .tsv)

- Metrics created from a local file (.csv, .xls, .xlsx, or .tsv) cannot be published to the **Metrics catalog**. 

- Metrics and visualizations that are created from an imported Cognos Analytics Framework Manager package cannot be published to the **Metrics catalog**.
