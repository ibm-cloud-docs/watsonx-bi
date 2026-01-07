---
copyright:
  years: 2025
lastupdated: "2026-01-07"

keywords:
subcollection: watsonx-bi



---

{{site.data.keyword.attribute-definition-list}}


# Object properties
{: #model_object_prop}

You can view and modify the semantic data model, table, column, and folder properties in the modeling interface. {: #shortdesc}

The properties can be accessed from the semantic data model, table, column, or folder context menu, or by using the **Properties** icon in the application bar. 

Some properties, such as **Label** and **Identifier**, are available for all objects in the semantic data model, while other properties are available only for certain types of objects.

For example, **Member display list** is available only for semantic data models, **Item list** only for tables, and **Aggregate** only for columns. 

You can view and modify the following properties on the **General** tab of the **Properties** pane.

- **Label**: Specifies the item's name that is displayed in the user interface. This property applies to all items. You can't change the label for members. To change the label for a semantic data model, use the **Save as** option. 

Ensure each asset and column has a unique label or a name. Labels are one of the factors that are used by the AI to understand questions and the context of your data when generating query statements. 
{: tip}

- **Hide from users**: Use this property to hide items, such as tables, columns, packages, or folders, in a semantic data model. The hidden items are grayed out in the modeling interface. 

- **Expression**: Shows the underlying expression for a column. Click **View or edit** to open the expression editor where you can modify the expression.

- **Usage**: This property applies to columns, and specifies the intended use for the column data. 

  The initial property value is based on the type of data that the column represents in the source. You need to verify that the property is set correctly. 
    
  For example, if you import a numeric column that participates in a relationship, the **Usage** property is set to **Identifier**. You can change this property.

  The following Usage types are supported:

    - **Identifier**: Represents a column that is used to group or summarize data in a Measure column with which it has a relationship. It can also represent an an index, date, or time column type. For example, Invoice number, or Invoice date.

    - **Measure**: Represents a column that contains numeric data that can be grouped or summarized, such as Product Cost.

    - **Attribute**: Represents a column that is not an Identifier or a Measure, such as Description.

- **Aggregate**: This property applies to columns, and defines the type of aggregation that is applied to a summary column. 

  For example, if the **Aggregate** property value of the Quantity column is **Total**, and the column is grouped by Product Name in a report, the Quantity column in the report shows the total quantity of each product. Aggregated data improves query performance and helps to retrieve data faster.

  The default type of aggregation is inherited from the source. When modifying this property, you can select values that the source does not provide, such as average or maximum. To know which aggregate value is required, you must understand what your data represents. For example, if you aggregate Part number, the aggregate values that apply are count, count distinct, maximum, and minimum.

  The following aggregation types are supported:

    - None (no aggregation is set up for a column)
    - Average
    - Count
    - Count distinct
    - Maximum
    - Minimum
    - Total

- **Data type**: The column data type is inherited from the source and can't be modified in the semantic data model.

- **Represents**: Use this property to specify whether a column includes the date or time, or geographic location type of data.

    - **Geographic location**: The values include Continent, Sub Continent, Country, Region, State Province, County, City, Postal code, Street Address, Position, Latitude, and Longitude.

    - **Time**: The values include Date, Year, Quarter, Season, Month, Week, Day, Hour, Minute, and Second.

- **Lookup reference**: This column property is used to create a semantic data model for relative date analysis.

- **Members**: Use this column property to enable or disable displaying relational members in the data tree. 

  The following settings are available:

    - **Automatic**: Members can be expanded in the data tree. Sorting is enabled, and members are sorted by the current column. Sort order is **Ascending**. This is the default setting.

    - **Enabled**: Members can be expanded in the data tree. You can select the column to sort by, and set the sort order to **Ascending** or **Descending**. The members that are shown in the data tree don't dynamically adjust to the changed sort order. Use the **Refresh members** action from the column context menu for the sort order to be reflected in the data tree.

    - **Disabled**: Members can't be expanded in the data tree. Previously shown members are removed, and new members can't be loaded for the column.

- **Members display limit** - This semantic data model property is used to specify the maximum number of members to load in the data tree nodes for each fetch request.

- **Description** - Use this property to specify information about the semantic data model, table, column, or folder. The description is used by AI to retrieve data when answering questions in **Conversations**. 

- **Comments**: Use this property to specify optional information about the semantic data model, table, column, or folder. Applies to all items in the semantic data model. The comment is available only within the semantic data model environment.

- **Screen tip**: Use this property to specify an optional short description of the table or column. Applies to all items in the semantic data model. The screen tip appears when you pause your pointer over the table or column name in the modeling environment.

## Advanced properties
{: #object_adv_props}

The following properties are specified in the **Advanced** section on the **Properties > General** tab:

- **Identifier**: This property uniquely identifies objects. It is used, either by itself or in conjunction with parent object identifiers, to generate SQL queries in expressions. The property is created automatically for a semantic data model and all its objects. For tables and columns, the property value is inherited from the data source. The property can be modified for all objects except for folders and the semantic data model itself. To change the semantic data model identifier, save it under a different name.   

Ensure each column has an identifier. Identifiers are one of the factors that are used by the AI to understand questions and the context of your data when generating query statements. 
{: tip}

When changing this property, ensure that:
    
- The first character is a letter or an underscore (_).

- The subsequent characters are letters, digits, or underscores (_), without spaces.

On the source tables, you cannot change the column identifier because at least one instance of that identifier is needed as a reference to the data source. While tables capture this reference in the background, columns do not. If you want to change the identifier for a column, for example if you are trying to create a more cryptic identifier, the recommended approach is to make copies of the columns, hide the original columns, and rename the identifiers of the copies.

- **Technical data type**: This property reflects how the column is defined in the database. For example, for a column with the **Data type** of Text, the **Technical data type** might be char(5), nvarchar(200), or varchar(10).

- **Usage**: This property applies to tables. It controls how the query engine should understand and process the table, and its child objects, in a query. The **Usage** property has the following settings:

    - **Automatic**: This setting informs the query engine that the table is an ordinary table, and requires no special processing. This is the default setting.

    - **Bridge**: The bridge table is used to remove the many-to-many relationships between tables by setting the many side of the relationship to the bridge table. By default, the query engine understands tables that are at the many end of relationships to be fact tables. The bridge table is not a fact table. So for the query engine to understand the role of the table and properly generate the query, the bridge table **Usage** property must be set to **Bridge**.

        The bridge table can be defined either in the database or in the semantic data model. However, it is preferable to create bridge tables in the database.

    - **Summary**: This setting summarizes the values in the table. When the table is used in a report or dashboard, the data retrieved from the table is already summarized, columns with the **Usage** property set to **Measure** are aggregated, and all other columns are used as grouping columns.

        Summary tables, such as unions, joined views, excepts, intersects, and SQL-based tables can be modeled in reports and semantic data models. It is more efficient to model these tables in the semantic data model. The tables are modeled once, there is only one possible point of failure, and the generated numbers are consistent.

- **Item list**: Use this property to specify the SQL generation type for a table. Depending on the setting for this property, the generated query SQL includes all or only selected columns. This property applies to tables only. 

- **Data cache**: Use this property to enable data caching and specify the cache expiry options for tables in the semantic data model. 

- **Source**: This property applies to all objects in the semantic data model. For a table or column, it shows the source name and path.

- **Supports NULL values**: Specifies whether a column supports null values. By default, this property value is inherited from the source. You can change this value.

- **User max suggested questions**: Use this property to specify the number of suggested questions that you want to generate when you export a metric definition. The default value is 10 and the maximum is 100. Suggested questions might  display at various points in a conversation. The questions displayed are based on the assets in the conversation's current scope, and can be asked to generate further insight.
