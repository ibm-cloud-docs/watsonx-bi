---
copyright:
  years: 2025, 2026
lastupdated: "2026-02-09"

keywords: multi-fact metrics, multiple tables, calculate after aggregate
subcollection: watsonx-bi



---

{{site.data.keyword.attribute-definition-list}}


# Creating calculations for cross-metric queries
{: #multi_fact_metrics}

You can create calculations that help answer questions spanning multiple metrics. These calculations are based on a multi‑fact metric, which combines measures from different fact tables. Multi‑fact metrics are especially useful when you need to compare or analyze data across fact tables that share common dimensions. {: #shortdesc}

## Before you begin
{: #prereq_multi_fact}

Before you create a multi-fact metric or multi-fact calculation, ensure that:

- You have at least two fact tables in your semantic data model

- Measures are already defined in each fact table that you want to use

## Step 1: Create a metric definition from multiple fact tables
{: #create_multi_fact} 

To create a calculation which spans multiple metrics, you must first define a metric which contains measures from the multiple fact tables.

1. Open the semantic data model that you want to create the metric in from **Data and Metrics**. 

1. Go to **Advanced mode**.

1. In the semantic data model tree, select measures from the different fact tables and from the context menu, select **New > Metric definition**.

1. Specify the details for the metric definition, include the data scope and measure role.

1. Click **Done** to finish. 


## Step 2: Create a calculation from mult-fact metric definition 

1. Select the metric definition you just created and from the context menu, choose **New > Calculation**.

1. Define your calculation using the measures within the metric definition. For example,
`Sales_Target - Sales_Total`.

1. Select **Calculate after aggregation**.
  
   When **Calculate after aggregation** is selected, the calculation is performed after values are aggregated. This is required for multi‑fact metrics so that the results from each fact table are aggregated first and only then included in the calculation.
   {: important}

1. Select **OK** to save the calculation.

1. Select **Actions > Save** to save your semantic data model.

1. Select the metric definition and export it to make it available in conversations.


## Example: Variance from plan calculation
{: #example_variance}

Consider a scenario where you have:

- **Sales** fact table with a `Sale_Total` measure

- **Sales Target** fact table with a `Sales_Target` measure

- **Time** dimension that joins both fact tables

To create a `Variance from plan` calculation that shows the percentage of actual sales compared to target:

1. Create a metric definition using measures `Sale_Total` and `Sales_Target` measures from the **Sales** and **Sales Target** tables. 

1. Select the metric definition in the semantic model and create a calculation named `Variance from plan`. Use the expression:

   ```
   100 * Sale_Total / Sales_Target
   ```
   {: codeblock}

1. Select **Calculate after aggregation** and click **OK**.

   This metric will calculate the variance by first aggregating the sales totals and targets separately, then performing the division and multiplication to get the percentage variance.

1. Save the semantic data model and export the metric definition to the project.

When you ask a question in a conversation that uses this metric, {{site.data.keyword.wxbia_short}} uses the calculation you created and aggregates the expression according to the context of your question.

## Related links
{: #related_multi_fact}

- [Calculations](/docs/watsonx-bi?topic=watsonx-bi-calculations){: external}

- [Building metrics in the Advanced mode](/docs/watsonx-bi?topic=watsonx-bi-advanced_mode){: external}

- [Data modeling in watsonx BI](/docs/watsonx-bi?topic=watsonx-bi-advanced_mode_model_data){: external}
