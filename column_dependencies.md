---
copyright:
  years: 2025
lastupdated: "2026-01-07"

keywords: column dependencies, columns, 
subcollection: watsonx-bi



---

{{site.data.keyword.attribute-definition-list}}


# Defining and creating column dependencies 
{: #column_dependencies}


When you're working with tables in a semantic data model, column dependencies help define how columns relate to each other. This is important because it ensures that when you aggregate data, the same value isn't counted more than once. {: #shortdesc}

Column dependencies are created automatically when the source tables are added to the semantic data model. If you create a calculated column using the existing columns, it is added to the dependency automatically.

However, if you pull in a new column from the **Source** panel, it is not automatically linked, and this can cause a validation error. In this case, you need to manually update the column dependencies to specify how the new column fits in.

Column dependencies are not inherited for custom tables. Any table object is considered independent, and if necessary, requires its own explicitly defined column dependencies to prevent double counting.
{: note}

## Defining column dependencies
{: #define_column_dependencies}

Define column dependencies to ensure that the fact data is aggregated correctly. You don't need to define column dependencies for all tables, just the ones where double-counting is likely to take place. 

The column dependency groups are related to each other in a hierarchy group in an order from coarse to fine granularity.
{: note}

1. Open an existing semantic data model that is based on a source that contains tables with repeated data at different levels of granularity.

2. Identify the attribute and columns that might cause double-counting. For example, the table can contain data at the month, quarter, and year level.

  Verify whether column properties and data formats are properly specified. For example, change the **Usage** property to **Attribute**, or assign the data format of **Currency** to measure columns. 
  
  Save the semantic data model after you make changes.

3. From the table context (right-click) menu, select **Specify column dependencies**.

  The **Column dependencies** view opens.

4. Drag the attribute columns that you identified in step 2, such as Year, Quarter, Month, and Day from the semantic data model panel to the **Column dependencies** view.

5. Click the group icon for a grouped column, and draw a line from the highest level attribute to the left of the next level attribute. Group the columns in a logical order to create a hierarchy group.

  Repeat this action for each level until the hierarchy is complete from coarse to fine granularity.

6. Drag any related attributes or measures, such as Quarter (caption), Month (caption), Sales target, and Date and Revenue, inside the related attribute area.

  Each column from the table must be in one group. Otherwise, validation warnings are shown.
  {: note}

  You can view the groups in the Horizontal view or Vertical view.

7. Verify, and if needed, modify the column dependency settings. For more information, see Configuring column dependencies.

8. Save the semantid data model.

## Configuring column dependencies
{: #configure_column_dependencies}

After you define a column dependency group and a hierarchy group, you can configure the column dependency settings for individual columns.

- Unique or Repeating 

  This setting specifies whether each row value is unique or repeating. Typically, all levels except for the lowest level in a hierarchy have repeating keys. Unique means that the key doesn’t repeat for any row in the data.

- Dependent or Independent 

  This setting specifies whether the parent level value is required to identify the key of the current level. For example, a month key that is defined as a number in the range 1 - 12, requires the parent level keys to identify which year and quarter the key belongs to. Conversely, a month key that is defined as 20190101 doesn’t require the parent keys to identify it because the month (01), quarter (01), and year (2019) values are included in the key.

- Minimum, Maximum, and Group by, or Average 

  This setting specifies if the SQL must be generated with the Min, Max, Avg, or Group by clause when aggregating the data. Minimum is the default setting. Use Minimum, Maximum, or Average for data attributes where there is more than one value for a particular key. For example, the key value of YOW might have the airport name values of Macdonald Cartier Airport, Ottawa International Airport, Ottawa/Macdonald–Cartier International Airport, or Macdonald–Cartier International Airport. In this case, select the Minimum or Maximum setting to prevent double-counting.

  When the data attributes don't repeat, which means that they are consistent throughout the data for each key, the Group by setting can be used. This setting doesn’t apply to measures.

  For measures, you might want to use the Average setting when the numeric values are similar. For example, when the values are 1000001, 1000002, and 1000003.

  If the column dependency is set to Minimum or Maximum, changing the column Usage property from identifier or attribute to measure, or the opposite, doesn't affect the column dependency. However, if the column dependency is set to Group by (identifiers or attributes) or Average (measures) changing this property sets the column dependency to Minimum.

To configure the column dependencies: 

1. Open the table **Column dependencies** view.

2. Inside the columns, click the icons that represent the different column dependency settings, and adjust the settings as required. For example, click the Unique Unique icon or Repeating Repeating icon setting icon.

3. Save the semantic data model. 
