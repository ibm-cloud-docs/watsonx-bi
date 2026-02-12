---
copyright:
  years: 2025
lastupdated: "2026-02-11"

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
    
## Supported visualizations
{: #supp_chart_types}

Here are some of the visualization types that you might see under **Change chart**. Each visualization has its own strengths and displays data differently. 

### Area 
{: #chart_area}

An area chart emphasizes the magnitude of change over time.

Area charts are like line charts, but the areas below the lines are filled with colors or patterns. An area chart stacks the results for each column or item and the total of all results is easily seen.

For example, an area visualization is excellent for looking at revenue over time across several products.

### Bar
{: #chart_bar}

A bar visualization compares values by one or more columns, such as sales for products or sales for products each month.

Bar visualizations use horizontal data markers that are arranged in groups to compare individual values and can show change over a specific time period or compare and contrast two or more columns in a time period or over time. 

### Box plot
{: #chart_box}

Box plot visualizations are used to identify outliers and compare distributions.

A box plot can show the median, quartiles, outlier, and extreme values for a variable. The inter-quartile range is the difference between the 75th and 25th percentiles and corresponds to the length of the box. The middle line is the 50th percentile.

Above and under each box, whiskers give additional information about the spread of the data.

Far out values are represent by adding "o" signs beyond the whiskers.

The mean score in a box plot is presented by a "+" sign.

### Column
{: #chart_column}

Much like a bar chart, a column visualization compares values by one or more columns such as sales for products each month.

Column visualizations use vertical data markers that are arranged in groups to compare individual values. A column visualization shows change over a specific time period or can compare and contrast two or more columns in a time period or over time.

### Crosstab
{: #chart_crosstab}

A crosstab can show relationships between three or more columns or rows. Crosstabs show data in rows and columns with information summarized at the intersection points.

### Heatmap
{: #chart_heatmap}

Heat map visualizations show the relationship between two variables through color. Most often, dark colors represent high-value data points and light colors represent low-value data points.

### Line
{: #chart_line}

Line visualizations show trends over time.

A line visualization can compare trends and cycles, infer relationships between variables, or show how a single variable is performing over time.

### List
{: #chart_list}

List visualizations create an overview of data in a hierarchical way. You can use a list visualization as a filter widget.

### Packed bubble
{: #chart_packed}

Packed bubble visualizations display data in a cluster of circles.

A packed bubble visualization uses sizable plotted points, also known as bubbles, to show the relationship between two data sets. The size of the bubble corresponds to the value or proportion of data. There is no positional axis and the bubbles are arranged in a random cluster.

Packed bubble visualizations help convey data that contains many groups and categories. Most often, the bubbles are arranged in a hierarchical order, with larger bubbles placed at the center and smaller bubbles place along the outside.

### Pie
{: #chart_pie}

Pie visualizations highlight proportions. Each slice shows the relative relationship of each part to the whole. The larger the size of a slice, the higher the percentage of the whole it represents. Pie charts are suitable to use with both nominal and categorical data sets.

### Point
{: #chart_point}

A point visualization show trends over time and is like a line chart without the connecting lines.

Point visualizations can compare trends and cycles, infer relationships between variables, or show how a single variable is performing over time.

Data values are plotted vertically.

### Radar
{: #chart_radar}

Radar visualizations are used to compare multiple quantitative variables. The radar visualization shows which variables have similar or outlier values.

Radar visualizations also show which variables score high or low in a data set, which is useful to display performance. For example, you can use a radar visualization to compare competitor profiles, such as the number of employees, revenue, profit, current stock price, and customer satisfaction.

### Spiral
{: #chart_spiral}

A spiral visualization shows you the key drivers, or predictors, for a given target. The closer the driver is to the center, the stronger that driver is.

### Word cloud
{: #chart_word}

A word cloud visualization displays text-based visualization of a column. The text height represents the scale. The name itself is the different members of the column.
