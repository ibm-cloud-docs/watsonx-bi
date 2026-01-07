---
copyright:
  years: 2025
lastupdated: "2026-01-07"

keywords:
subcollection: watsonx-bi



---

{:codeblock: .codeblock}
{:note: .note}
{:pre: .pre}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:table: .aria-labeledby="caption"}
{:tip: .tip}
{:video: .video}
{:external: target="_blank" .external}
{:step: data-tutorial-type='step'}

# Filters
{: #model_filters}

A filter specifies the conditions that rows must meet to be retrieved from tables that are used in a metric definition. {: #shortdesc}

There are two types of filters in semantic data models: 

- Embedded filters

- Selectable filters


## Embedded filters
{: #embedded}

You can create embedded filters to customize the data that is used in a metric definition. For example, you can filter out data that is irrelevant for certain geographies, time periods, product lines, and so on.

Embedded filters can be created for a single column, or for multiple columns in a table. They are defined in a query subject and always apply to the query subject.

### Creating an embedded filter
{: #create_embedded}

1. In a semantic data model tree, locate the table that you want to add filters to, and choose one of the following options:

- To create a filter for a single column in the table, from the column menu, click **Filter**.

- To create filters for multiple columns in a table, from the table context menu, click **Manage filters**. On the **Filters** tab, select the column for which you want to create the filter, and click **Add a filter**.

   The option via expression editor allows you to create a filter by using the expression editor. Specify the filter name, type its expression, and click **OK**. Next, you can either continue adding filters by using this option, or proceed to step 2.

2. Specify the filter values. The options to select values depend on the column data type.

   For columns with integer and decimal data types, you have two options to specify the values: Range and Individual items. When you choose Range, you can use the slider to specify the range values, or type the range start and end values. When you choose Individual items, select the check boxes that are associated with the values.

   You can enter decimal values only for columns with the decimal data type. When you try to enter a decimal value for a column with the integer data type, the decimal separator is cleared.
   {: tip}

- For columns with date and time (timestamp) data types, specify a range of values before, after, or between the selected date and time, or select individual values.

- For columns with text data types, select the check boxes that are associated with the values.

3. Click **OK** to save the filter.

   The effect of the filter is not automatically shown for the members in the semantic model panel. To see that effect, click **Refresh members** on the related column.
   {: note}

If you used the **Manage filters** option, you can continue creating filters for other columns in the table. The filters that you created are listed on the **Filters** tab.

After an embedded filter is created, the filter icon appears next to the column and table names in the semantic model panel and expression editor.

The filter icon on a table indicates that the table contains at least one embedded filter. You can see the embedded filters that a table contains in the table properties, on the ***Filters** tab.

### Embedded filters in a complex query
{: #complex_query}

Semantic data models have a setting that is called **Design mode**, which you can access in the **Properties** tab. The **Design mode** controls which filters are applied during queries. This setting is enabled by default.

Embedded filters have a property that is called **Usage**, which ties into the **Design mode** property for semantic data models. 

When an embedded filter is applied to a metric definition, there are four **Usage** values, which you can use to control when the filter is applied.

- Enabled - The filter is always applied.

- Disabled - The filter is not applied.

- Default - The filter is applied, unless the incoming query contains a filter that references the same columns (query items).

- Design mode - If the query says that it is in design mode then the filter is applied.

When the Design mode setting is toggled for the semantic data model, the design mode filters are executed in modeling. If Design mode is turned off, filters with a usage of design mode are ignored when a query is performed in modeling.

Filters that use Design mode are always executed in metadata enrichment and to generate suggested questions regardless of whether the semantic data model Design mode is on or off. Filters using Design mode are not used in conversations.
{: note}

### Managing embedded filters
{: #manage_embedded}

To edit or remove a filter on a single column or a table: 

1. From the column or table context menu, click **Properties**. 

2. On the **Filters** tab, click the filter name to expand the section.

3. Click the appropriate link. 

## Selectable filters
{: #selectable}

Selectable filters are pre-defined, optional filters. They exist as distinct objects and only apply to a query if they have been added to the query.

The filters suggest possible options to filter data in the semantic data model, but you can also view unfiltered data.

Selectable filters can be created inside a table or outside a table (at the root of the semantic data model).

### Creating a selectable filter
{: #create_selectable}

1. Open a semantic data model and decide what type of a selectable filter you want to create.

- To create a filter inside a table, from the table context menu, click **Filter**.

   The Filter option is also available for a folder inside the table, and for the table in the diagram.

- To create a filter outside a table, from the semantic data model context menu, click **Filter**.
   
    The Filter option is also available for a folder at the root of the semantic data model.

    The expression editor displays.

2. Type the filter name.

3. In the **Expression** panel, provide the filter expression by using the expression editor capabilities

4. Click **OK**.

The filter is added as a stand-alone entry in the semantic model panel with the filter icon before the filter name. 

Filters created at the folder-level are added to the applicable folder.

### Managing selectable filters
{: #manage_selectable}

To edit the filter, from the filter context menu, click **Edit filter**. 

To remove the filter, from the filter context menu, click **Remove**.


