---
copyright:
  years: 2024
lastupdated: "2026-01-07"

keywords:
subcollection: watsonx-bi



---

{{site.data.keyword.attribute-definition-list}}


# Hiding items
{: #model_hiding_items}

You can hide items in the semantic data model panel  to provide an uncluttered view of metadata. {: #shortdesc}

When you hide columns that are referenced in a calculation, the data tree shows only the calculation column, but not the referenced columns. 

When you hide the identifier columns that are used as keys for joins, the keys are not exposed, but the joins are functional in the modeling interface.

The following read-only items can't be hidden by default:

* Packages 

  To work around this issue, create a folder in the semantic data model panel, and move your package with all its content into that folder. Then, hide the folder.

* Tables that are linked to the source semantic data model
  
  To work around this issue, in the semantic data model panel, from the table context menu,
  select **Break link**. The link is broken, and you can now hide the table.

## Steps
{: #hide_steps}

1. In the semantic data model panel, click the context menu for an item such as a table or column, and click **Hide from users**.

   You can also select multiple items to hide at once.
   
   To show the hidden items, click the context menu for the parent item, and then click **Show hidden items**.
   {: note}

2. Save the semantic data model.

The labels on the hidden items are grayed out in the semantic data model panel and in the diagram. Also, on the **General** tab of the item's properties, the **Hide from users** property is selected. 
