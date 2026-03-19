---
copyright:
  years: 2025, 2026
lastupdated: "2026-03-18"

keywords: format data, currency, percentage

subcollection: watsonx-bi

---

{{site.data.keyword.attribute-definition-list}}

# Formatting data 
{: #format_data}

You can choose a format type, such as Percent or Currency, for metric columns in the semantic data model. When you set format types in the semantic model, watsonx BI will reflect those formats in the generated conversational responses.{: #shortdesc}

Insights, such as those generated with visualizations, do not support formatting.
{: note}


## Supported format options
{: #supported_data_formatting}

Watsonx BI currently supports the following format types for metric columns and calculated columns. 

Currency

:   Supported options:

:   - Currency - Specifies the currency to be used. 

:   - Number of decimal places - Specifies the number of digits to be displayed to the right of the decimal point. 

:   - Use thousands separator - Specifies whether the grouping delimiter will be applied as defined by the Group Size property. The default value is inherited from the user's content language.


:   Example: $12,000,000.00 with 2 decimals and thousands separator


Percent

:   The Percent format type is supported but additional options are not supported.

:   Ensure that the original data is in a ratio form. Applying the Percent format type multiplies values by 100 and adds a percent sign. If your data is already scaled and multiplied by 100, don’t assign the Percent format type. Doing so might result in inaccurate values for that column.

## Applying formats
{: #applying_format}

1. Open the semantic data model that contains the metric columns you want to format from **Data and Metrics**. 

1. Click the menu icon for a metric column and select **Format data**.

   For a column that represents a monetary value, select **Currency**. You can choose the currency (symbol or ISO as configured), set the number of decimal places, and use the thousands separator.

   For each column that represents a ratio, select **Percent**. Make sure that the source data is a ratio such as 0.125, not 12.5.

1. Click **OK** to apply the formatting.

1. Save the semantic data model, then export the metric definition. 

After the metric definition enriches successfully, you can ask a question in **Conversations** and confirm that values appear with the correct currency symbol or percent sign, decimal places, and thousands separators.


## Formatting for calculated columns
{: #format_calculated_columns}

Watsonx BI supports formatting for calculated columns, which are computed on the fly. Formatting for these columns follows these rules:

- Supported types: Currency and Percent

- Inference: An LLM infers the appropriate format based on the calculation.

- Conflicts: If the calculation mixes incompatible formats (for example, multiple different currencies), watsonx BI will not apply formatting to avoid incorrect results.

- Best practice: Keep calculations semantically meaningful and consistent in units. If you mix currencies, convert to a single currency before or within your calculation.


