---
copyright:
  years: 2026
lastupdated: "2026-01-07"

keywords: calculations, modeling
subcollection: watsonx-bi



---

{{site.data.keyword.attribute-definition-list}}


# Calculations
{: #calculations}

Calculations allow you to answer questions that cannot be answered by the source columns. {: #shortdesc}

Semantic data models support the following types of calculations:

- Stand-alone calculations
  
  These types of calculations live outside of a table in a semantic data model. Stand-alone calculations can refer to columns in any table in the semantic data model. You can move a stand-alone calculation into a folder to better organize items in the semantic data model.

- Embedded calculations

  These types of calculations, also referred to as table calculations, reside within a table in a semantic data model. Embedded calculations can refer only to columns in the same table.

You can create basic arithmetic calculations, and more complex, custom calculations. 

## Creating basic calculations
{: #basic_calculations}

You can create basic arithmetic calculations for columns with numeric data types.

The expression for these calculations is predefined, and you need to only select the proper mathematical operator, and in some cases, a constant value. For example, you can create a column *Revenue* by multiplying values for *Quantity* and *Unit price*.

1. In the semantic data model tree, right-click one or two columns that you want to use in the calculation.

  For calculations that are based on two columns, use control-click to select the columns. The columns can be in two different tables. The column that was selected first is used as the first operand in the calculation.

  You can also create the calculations at the folder level.

2. Click **Create calculation**.
 
3. Specify the calculation name by overwriting the automatically generated name.

4. Define the expression. 

  If your calculation is based on one column, choose the required operator and specify the constant value.

  If your calculation is based on two columns, ensure that the order of columns is correct, and choose the required operator. If the order of columns is incorrect, click **Cancel**, and start the calculation again by selecting the columns in the proper order.



5. Click **OK** to finish the calculation, or click **Use calculation editor** to view the calculation expression, or to modify it.

A calculation based on one column is created as an embedded calculation. The calculation is added at the top of the list of columns in the table. You can move it to a folder inside the same table.

A calculation based on two columns can be created as an embedded or stand-alone calculation. If the columns are from the same table, an embedded calculation is created and added at the top of the list of columns in the table. If the columns are from different tables, a stand-alone calculation is created and added at the top of the semantic data model tree, outside of any table. You can move this calculation to a semantic model folder.

## Creating custom calculations
{: #custom_calculations}

To create a custom calculation, you must define your own expression using the expression editor.

The expression editor provides functions and operators to create your expressions. It also includes function examples and documentation, and can validate the expressions. 

Custom calculations can be based on one column or multiple columns from different tables.

1. In the semantic data model tree, right-click the semantic model name, a table name, or a folder name, and click **Calculation**.

  You can also create calculations from the **Relationships** or **Custom tables** view.
  {: note}
  
2. Specify the calculation name in the **Expression editor**. 

3. Define the expression for your calculation in the **Expression** box by using the expression editor capabilities.

  - To enter a function for your expression, type the first character of the function name, and select the function from the drop-down list of suggested functions. For example, the following expression can be used to concatenate a person's first and last name and create a calculated column called *Name*:

  ```
   concat ( [Sales target (query)].[Sales staff].[First name], 
   [Sales target (query)].[Sales staff].[Last name] )
   ```
   {: codeblock}

  - To add table columns to your expression, drag one or more columns from the semantic data model tree to the **Expression** box. The column name is added where you place the cursor in the Expression editor.

  You can also double-click the column in the semantic data model tree, and the column name appears in the Expression editor.

4. Click **Validate** to check if the expression is valid. The calculation will be created even if the expression is not valid, but it won't be usable.



5. Click **OK**.

A calculation based on one column is created as an embedded calculation. The calculation is added at the top of the list of columns in the table. You can move it to a folder inside the same table.

A calculation based on two columns can be created as an embedded or stand-alone calculation. If the columns are from the same table, an embedded calculation is created and added at the top of the list of columns in the table. If the columns are from different tables, a stand-alone calculation is created and added at the top of the semantic data model tree, outside of any table. You can move this calculation to a semantic model folder.
