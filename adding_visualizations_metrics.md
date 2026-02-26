---
copyright:
  years: 2025, 2026
lastupdated: "2026-02-26"

keywords: adding visualizations, visualizations, metrics
subcollection: watsonx-bi



---

{{site.data.keyword.attribute-definition-list}}

# Adding visualizations to metrics
{: #add_viz_metrics}

You can visualize your metrics by adding visualizations to them. Visualizations can help you quickly see how your data is trending, compare data points, determine relationships between key data points, and more. {: #shortdesc}

You can add visualizations to your metrics by generating them automatically or building them manually from scratch. 

## Generating visualizations for metrics
{: #generate_viz}

1. From the **Data and Metrics** tab, open the semantic model with the metrics for which you want to create visualizations.

2. On the **Metrics overview** page, click the menu icon next to the metric you want to work with and select **Generate visualizations**.

3. Select the visualizations that best represent the metric and click **Next**. 


## Building visualizations for metrics
{: #build_viz}

1.  From the **Data and Metrics** tab, open the semantic model with the metrics for which you want to create visualizations.

2. On the **Metrics overview** page, click the menu icon next to the metric you want to work with and select **Build visualizations**.

3. Enter the required fields on the **Chart type**, **Chart fields**, **Metric details**, and **Chart properties** tabs:   

   - On the **Chart type** tab, select the chart you want to use to represent the metric. 

   - The **Chart fields** tab is where you select the data that appears in different parts of the visualization. As you select data and populate fields on this tab, a visualization builds.  
    
   The **Values** field is a required field on this tab. Click the field context menu to see actions you can perform such sorting, applying a filter, and summarizing the data item. 
{: important}

   - On the **Metric details** tab, add a name for your metric and a chart title. The metric name is used to identify the metric in the **Metrics catalog**. The chart title displays in the metric when it is added to **Key metrics** on the **Conversations** tab.

   - On the **Chart properties** tab, you can change the properties from their defaults to customize how the visualization appears.

4. Click **Save**. 

### Supported visualizations
{: #supported_viz}

Visualizations communicate comparisons, relationships, and trends. They emphasize and clarify numbers. To choose a visualization type, consider what you want the visualization to illustrate.

The visualizations that you can choose from, when building a visualization, include:

Area 

:   An area chart emphasizes the magnitude of change over time. An area chart stacks the results for each column or item and the total of all results is easily seen. For example, an area visualization is excellent for looking at revenue over time across several products.

Bar

:   A bar chart compares values by one or more columns, such as sales for products or sales for products each month. Bar charts use horizontal data markers that are arranged in groups to compare individual values and can show change over a specific time period or compare and contrast two or more columns in a time period or over time. 

Box plot

:   Box plot visualizations are used to identify outliers and compare distributions. A box plot can show the median, quartiles, outlier, and extreme values for a variable. 

Bubble

:   Use a bubble visualization to show relationships among columns that contain numeric values, such as revenue and profit. A bubble visualization uses data points and bubbles to plot measures anywhere along a scale. One measure is plotted along each axis. The size of the bubble represents a third measure. Use bubble visualizations to represent financial data or any data where measure values are related.

Bullet

:   Use bullet charts to show measures that need to be compared against a target value. Bullet visualizations compare an actual measure (the bullet) to targeted measure (the target). Bullet visualizations also relate the compared measures against colored regions in the background that provide more qualitative measurements, such as good, satisfactory, and poor. 

Column

:   Much like a bar chart, a column visualization compares values by one or more columns such as sales for products each month. Column visualizations use vertical data markers that are arranged in groups to compare individual values. A column visualization shows change over a specific time period or can compare and contrast two or more columns in a time period or over time.

Crosstab

:   A crosstab can show relationships between three or more columns or rows. Crosstabs show data in rows and columns with information summarized at the intersection points.

Driver analysis

:   A driver analysis visualization shows you the key drivers, or predictors, for a target. The closer the driver is to the right, the stronger that driver is.

Dual axis line

:   Use a dual-axis line visualization to display relationships between two data sets. Each line in the visualization represents one y-axis. This visualization technique allows you to display two different data sets in one visualization. Each y-axis uses its own scale. Using this technique, you can compare different metrics or measures that each have different scales or units. When users view the data side-by-side, it is easier for them to understand patters and correlations in the data.

Heat map

:   Heat map visualizations show the relationship between two variables through color. Most often, dark colors represent high-value data points and light colors represent low-value data points.

Hierarchy bubble

:   Use a hierarchy bubble visualization when you want to show relationships among columns that contain values, such as net loss. It is similar to the bubble visualization but the bubbles are tightly packed instead of spread over a grid. The bubbles use nesting to represent the hierarchy. 

KPI

:   Use a KPI visualization to display a key performance indicator (KPI) that contains two related measures, such as revenue and planned revenue. A KPI visualization compares a base value to a target value and shows the variance between the two measures.

Line

:   Line visualizations show trends over time. A line visualization can compare trends and cycles, infer relationships between variables, or show how a single variable is performing over time.

Line and column

:   Use a line and column visualization to highlight relationships between multiple data series by combining bars and lines with one visualization.

List

:   List visualizations create an overview of data in a hierarchical way. You can use a list visualization as a filter widget.

Marimekko

:   A marimekko visualization is similar to a stacked column visualization. It shows data through varying heights and includes an added dimension of data through varying column widths. The width of the columns is based on the value that is assigned to the width field. Individual segment height is a percentage of the respective column total value.

Network

:   Use a network visualization when you want to see the connections among columns in your data asset. A network visualization is a good choice to show connections, networks, and points of intersection.Network visualizations display a set of nodes, represented by symbols, and links, represented by paths, to show the relationship between entities or items.

Packed bubble

:   Packed bubble visualizations display data in a cluster of circles. A packed bubble visualization uses sizable plotted points, also known as bubbles, to show the relationship between two data sets. The size of the bubble corresponds to the value or proportion of data. There is no positional axis and the bubbles are arranged in a random cluster. Packed bubble visualizations help convey data that contains many groups and categories.

Pie

:   Pie visualizations highlight proportions. Each slice shows the relative relationship of each part to the whole. The bigger the size of a slice, the higher the percentage of the whole it represents. Pie charts are suitable to use with both nominal and categorical data sets.

Point

:   A point visualization show trends over time and is like a line chart without the connecting lines. Point visualizations can compare trends and cycles, infer relationships between variables, or show how a single variable is performing over time.

Radar

:   Radar visualizations are used to compare multiple quantitative variables. The radar visualization shows which variables have similar or outlier values. Radar visualizations also show which variables score high or low in a data set, which is useful to display performance. 

Radial

:   In a radial visualization, each bar appears in a circle with longer bars that represent larger values. Each bar starts at 12 noon and goes in a clockwise direction for positive values and counterclockwise for negative values. Radial visualizations, also known as dial charts or speedometer charts, show information as reading on a dial. The radial visualization is valid only with one category.

Scatter

:   Scatter visualizations use data points to plot two measures anywhere along a scale, not only at regular tick marks. Scatter visualizations are useful for exploring correlations between different sets of data.

Spiral

:   A spiral visualization shows you the key drivers, or predictors, for a given target. The closer the driver is to the center, the stronger that driver is.

Stacked bar

:   Use a stacked bar visualization to compare the proportional contributions for each item to the total, such as sales for products and sales for products each month. A stacked bar visualization can show change over a specific time period or compare the proportional contributions for each item to the total. 

Stacked column

:   Use a stacked column visualization to compare the proportional contributions for each item to the total, such as sales for products and sales for products each month. A stacked column visualization can show change over a specific time period or can compare the proportional contributions for each item to the total. 

Sunburst

:   A sunburst visualization is used to illustrate how underlying data predicts a chosen target and highlights key insights.

Table

:   Use a table to show detailed information from your database, such as product lists and customer lists. A table shows data in rows and columns. Each column shows all the values for a data item in the database or a calculation based on data items in the database.

Tree map

:   Use a tree map visualization to identify patterns and exceptions in a complex data asset. Treemaps show relationships among large numbers of components by using size and color coding in a set of nested rectangles.

Word cloud

:   A word cloud visualization displays text-based visualization of a column. The text height represents the scale. The name itself is the different members of the column.  
