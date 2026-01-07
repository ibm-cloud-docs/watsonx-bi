---
copyright:
  years: 2025
lastupdated: "2026-01-07"

keywords: generating visualizations, conversations
subcollection: watsonx-bi



---
{{site.data.keyword.attribute-definition-list}}


# Generating visualizations in conversations
{: #visualizations}

{{site.data.keyword.wxbia_full_notm}} generates a visualization when you ask for one or when it might be better suited to help you quickly see trends and comparisons in your data. {: #shortdesc}

You can ask {{site.data.keyword.wxbia_short}} to create a visual of your data and use the visualization as a metric. For example, the following inputs can generate a visualization along with related insights:  

- Show sales by region 

- Show top 5 products by sales

{{site.data.keyword.wxbia_short_cap}} generates a visualization that best describes your data in the canvas. However, if other charts are available for your data, the **Change chart** icon in the visualization is enabled. Click **Change chart** to change the visualization to a different chart type.

You can pin a visualization that was generated in response to your question to **Key metrics**. Pinning a generated visualization allows you to monitor changes in that data without having to ask {{site.data.keyword.wxbia_short}} to regenerate the visualization. 

After a visualization is pinned to **Key metrics**, you can click the visualization and use **Ask a question** to get insights.

When you use **Ask a question** to get insights for a pinned visualization, {{site.data.keyword.wxbia_short}} analyzes all of your data to generate a response. The answer might not come from the same project that created the visualization, even if you select that project in the data scope. This is because the original project might not contain the information that is needed to answer your follow-up question.
{: important}

## Customize visualizations by using natural language
{: #customize_viz}

You can customize certain properties of a visualization, conversationally.

For example, when you ask AI to generate a visualization, you can enter an input like "Show product line with revenue and set the chart title as *My new visualization*."

You can even change a visualization property after the visualization generates by asking AI to implement the change you want to make. For example, "Hide the yAxis gridline" hides the gridline that is on the y-axis of the chart.

Properties that you can change with natural language:

- **Change chart title**

  Example inputs: 

  - Show top selling products for 2025 and set the chart title to "Top sellers". 
  - Change the chart title to "Top selling products".

- **Set background color**

  By default the background color for all visualizations is White. 

  Example inputs:

  - Show product line and revenue and set the background color to green
  - Change the background color to green.

- **Set border color**

  The default border color in visualizations is transparent. 

  Example inputs:

  - Set the chart border color as blue.

- **Show or hide legend**

  By default, the legend is shown in visualizations.

  Example inputs:

  - Hide the legend in the chart.
  - Show the legend in the chart.

Depending on the visualization you're working with, you can also ask AI to:

- **Show or hide axis labels**

  Labels provide context for the data in the visualization. By default, labels are always shown on both axes. 
  
  Example inputs:

  - Hide the labels in the x-axis.
  - Hide the xAxis labels.

- **Show or hide axis title**

  The title of both axes in a visualization is shown by default. You can ask the AI to hide the title for one or both axes.

  Example inputs: 

  - Hide xAxis title. 
  - Hide x-axis title.
  - Hide the title for both axes. 

- **Show or hide gridlines**

  You can ask the AI to hide gridlines for one or both axes. By default, the visualization always shows gridlines. 

  Example inputs:

  - Hide gridlines in the chart.
  - Don't show gridlines.

- **Show tick marks**

  Tick marks are small lines on the axes, which indicate the measurement scale or intervals. By default, tick marks are shown in visualizations.

  Example inputs:

  - Hide tick marks on the x-axis.
  - Add tick marks to the y-axis.
  - Show product line with revenue and hide the tick marks on the x-axis.

- **Adjust label font size** 
  
    You can adjust the label font size in visualizations. The values for font size are:
    
    - xsmall
    - small
    - medium
    - large
    - xlarge
    
    By default, the font size is set to medium. 

    Example inputs:

    - Use xlarge as the label size for xAxis.
    - Change the label size to small.

- **Bar width**

  For charts with bars, you can set the bar width. The values for bar width are: 
  
    - xsmall
    - small
    - medium
    - large
    - xlarge
  
  By default, bar width is set to medium. 

  Example inputs:

  - Change the bars to small size.
  - Make the bars small.
  
- **Change element color**

    Elements represent the data values in the charts. For example, lines in a line chart and bars in a bar chart are elements. 

    By default, the elements in visualizations are set to blue color. 

    Example inputs:

    - Set the element color to pink.
    - Change the element color to green.
    
