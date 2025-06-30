---
copyright:
  years: 2025
lastupdated: "2025-06-26"

keywords: build metrics, building, manual, metric definitions
subcollection: watsonx-bi



---

{{site.data.keyword.attribute-definition-list}}


# Building metrics in the Advanced mode
{: #advanced_mode}

You can build metrics manually by creating metric definitions in the semantic data model. A metric definition is a logical collection of measures and attributes that define a metric. {: #shortdesc}

## Building metrics manually
{: #build_manual} 

1. On the **Data and Metrics** tab, select a project and click **Create metrics**. 

2. A new semantic data model is created for you. Enter a unique name for the semantic data model. 

3. On the **Select data** page, [select the data](/docs/watsonx-bi?topic=watsonx-bi-select){: external} you want to work with. You can connect to your remote data with an existing connection or create a new connection. 

4. Click **Next** to continue. Your data now undergoes enrichment, which adds a layer of business context metadata to prepare your data for use in conversations and metrics. 

   No changes are made to your original data during enrichment. 
   {: note}

5. Review your metadata enrichment results and return to the enrichment page in watsonx BI. Click **Next** to continue. 

6. On the **Metrics overview** page, click **Build metrics in Advanced mode**. You're now in the semantic data model. 

7. Review the semantic data model and make necessary adjustments. 

   You can view all of the measures along with their properties and attributes, relationships between tables that were generated during enrichment, and calculations. 

   Ensure that meaningful names, descriptions, and identifiers are assigned to each column. These fields help AI find and retrieve data when answering your questions. 
   {: tip}

8. In the semantic data model tree, select one or more measures.

9. Right-click on one of your selections and select **New > Metric definition**.  

10. Name your metric definition and add optional details such as a description, screen tip, and comments to easily find the metric definition. 

11. On the **Data scope** tab, review the list of the measures and attributes and deselect the attributes you want to exclude from the metric definition.

   Select attributes that are related to the measure you initially selected.
   {: tip}

12. On the **Measure role** tab, use the dropdown on the right to select and associate each measure with other measures to define them as targets and actuals.

13. Select the arrow beside each measure to specify if their sentiment is positive (up arrow), negative (down arrow) or neutral (right arrow).

14. (Optional) On the **Time grain** tab, select time periods (years, months, or days) to specify the number of time periods that will be included in the metric. 

15. (Optional) On the **Time reference** tab under **Available**, select a time reference you want to include in the metric and click the right arrow to move it to the **Selected** section. You can also change the **Default time reference**. 

16. Click **Actions > Save** to save your semantic data model. 

17. Select the metric definition that you just created in the semantic data model tree and click **Export metric definition**. 

    The metric definition exports to the project and creates a metric that can be used in conversations.

18. (Optional) You can now go back to the **Metrics overview** page and: 

    a. [Add visualizations](/docs/watsonx-bi?topic=watsonx-bi-add_viz_metrics){: external} to one or more of these metrics. 
    
    b. Select a metric and [try it in a conversation](/docs/watsonx-bi?topic=watsonx-bi-try_metrics) to ensure it can answer questions about your data. You can go back to the **Advanced mode** to adjust its metric definition, if necessary. 
    
    c. (Data analysts only) [Publish metrics and visualizations](/docs/watsonx-bi?topic=watsonx-bi-publish_metrics){: external} to the **Metrics catalog** and assign them to Analytics consumers. 

19. From the **Navigation menu**, go to **Home > Conversations** to ask questions about your data.
