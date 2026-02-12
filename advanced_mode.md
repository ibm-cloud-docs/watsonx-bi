---
copyright:
  years: 2025, 2026
lastupdated: "2026-02-11"

keywords: build metrics, building, manual, metric definitions
subcollection: watsonx-bi



---

{{site.data.keyword.attribute-definition-list}}


# Building metrics in the Advanced mode
{: #advanced_mode}

You can build metrics manually by creating metric definitions in the semantic data model. A metric definition is a logical collection of measures and attributes that define a metric. {: #shortdesc}

## Building metrics manually
{: #build_manual} 

After you start the metric creation process from **Data and Metrics** and [select the data](/docs/watsonx-bi?topic=watsonx-bi-select){: external} that you want to work with, the data undergoes [metadata enrichment](/docs/watsonx-bi?topic=watsonx-bi-enrich){: external}. Upon completion of enrichment, click **Next** to proceed. 

Follow these steps when you get to the **Metrics overview** page.

1. On the **Metrics overview** page, click **Build metrics in Advanced mode**. You're now in the semantic data model. 

2. Review the semantic data model and make necessary adjustments. 

   You can view all of the measures along with their properties and attributes, relationships between tables that were generated during enrichment, and calculations. 

   Ensure that meaningful names, descriptions, and identifiers are assigned to each column. These fields help AI find and retrieve data when answering your questions. For more information, see [Optimizing data for AI](/docs/watsonx-bi?topic=watsonx-bi-best_practices){: external}. 
   {: tip}

3. In the semantic data model tree, select one or more measures.

4. Right-click on one of your selections and select **New > Metric definition**.  

5. Enter a name for the metric definition and add optional details such as a description, screen tip, and comments to easily find the metric definition. You can also add custom guidance that explains your business logic, rules, and interpretation in the **AI instructions and context** field. This helps AI understand questions more effectively and generate accurate SQL during analysis.

   Ensure that the metric definition has a unique name. 
   {: important}

6. On the **Data scope** tab, review the list of the measures and attributes. By default, all of the attributes are selected. Deselect the attributes that you want to exclude from the metric definition. 

   Make sure that the selected attributes are related to the measure you initially selected.
   {: tip}

7. On the **Measure role** tab, use the dropdown on the right to select and associate each measure with other measures to define them as targets and actuals.

8. Select the arrow beside each measure to specify if their sentiment is positive (up arrow), negative (down arrow) or neutral (right arrow).



9. Click **Done**.

10. Click **Actions > Save** to save your semantic data model. 

11. Select the metric definition that you just created in the semantic data model tree and click **Export metric definition**. 

    The metric definition exports to the project and creates a metric that can be used in conversations.

12. (Optional) You can now go back to the **Metrics overview** page and: 

    a. [Add visualizations](/docs/watsonx-bi?topic=watsonx-bi-add_viz_metrics){: external} to one or more of these metrics. 
    
    b. Select a metric and [try it in a conversation](/docs/watsonx-bi?topic=watsonx-bi-try_metrics) to ensure it can answer questions about your data. You can go back to the **Advanced mode** to adjust its metric definition, if necessary. 
    
    c. (Data analysts only) [Publish metrics and visualizations](/docs/watsonx-bi?topic=watsonx-bi-publish_metrics){: external} to the **Metrics catalog** and assign them to Analytics consumers. 

13. From the **Navigation menu**, go to **Home > Conversations** to ask questions about your data.
