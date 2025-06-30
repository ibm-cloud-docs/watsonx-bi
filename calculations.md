---
copyright:
  years: 2025
lastupdated: "2025-06-26"

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

You can create basic arithmetic calculations, and more complex, custom calculations. The expression for these calculations is predefined, and you need to only select the proper mathematical operator, and in some cases, a constant value. For example, you can create a column *Revenue* by multiplying values for *Quantity* and *Unit price*.
