---
copyright:
  years: 2025, 2026
lastupdated: "2026-07-10"

keywords: review mde, review metadata enrichment, review enrichment
subcollection: watsonx-bi

---

{{site.data.keyword.attribute-definition-list}}


# Reviewing metadata enrichment 
{: #review}

You can review enrichment results to make sure the metadata that is applied is meaningful and accurate.  {: #shortdesc}

You can review enrichment, if you use:

- Watsonx.data intelligence for enrichment in watsonx BI as a Service

- Watsonx BI on IBM Software Hub

## Accessing the review enrichment page
{: #access_review}

You can open the **Review enriched data** page from the:

1. Metadata enrichment page during metric creation 

  This option is available only while you are still in the metadata enrichment workflow. After you move forward to the **Metrics overview** page, you can no longer access the review page from here.

2. Project view 

  a. Go to **Navigation menu > View all projects**.

  b. Select the project that contains the enriched asset. 
  
  c. Open the **Assets** page and locate the Metadata enrichment asset.

If you are using watsonx BI enrichment in watsonx BI as a Service, a page to review enrichment results is not currently available.
{: important}

## About the review enrichment page
{: #about_review}

When you open the enrichment results, you can view the enriched data at both the asset level and column level. A side panel also provides a summary of relevant information about the metadata enrichment.

The following indicators are used in the results tables and the details panels:

- A purple square for automatically assigned display names and for AI-generated descriptions that were automatically assigned

- A blue dot for accepted display-name or description suggestions, or for edited display names or descriptions 

- An AI label for AI-suggested descriptions 


## Reviewing enrichment at the asset level
{: #rev_asset}

On the **Assets** tab, review the following information that is used by watsonx BI for each data asset. 

By default, all of the information is shown on the tab but you can customize the view and show only the information that you need. Click the **Customize columns** icon and deselect all columns that you want to hide. You can also reorder the columns by clicking an entry and dragging it to a new position.
{: tip}

- Asset name (for relational data, also the table type is shown)

- Display name - You can edit the names and accept suggested names.

- Description - You can edit the descriptions and accept AI-suggested descriptions.



You can go to the columns of an asset by clicking the asset name or **View columns** in the context menu.

### Asset details
{: #asset_enrich}

Access an asset's enrichment details by clicking the asset name or by clicking **View asset details** in the context menu. On the **Details** tab in the side panel, you can find the following information:

Display name

:   The **Display name** initially contains an alternative name for the data asset that was found through fuzzy matching. Fuzzy matching expands the source name based on a predefined glossary to provide a name that is easy to understand. 

:   The expanded name might already be assigned because the confidence was high enough or it is a suggestion that you can accept. At any time, you can edit the display name.

Description

:   This section contains an AI-generated description, which might already be assigned because the confidence was high enough. Otherwise, it is a suggestion that you can accept. At any time, you can edit the description.



## Reviewing results at the column level
{: #rev_column}

On the **Columns** tab, review the following information for each column in a data asset:

By default, all information is shown on the tab. You can customize the view and show only the information that you need. Click the **Customize columns** icon and deselect all columns that you want to hide. If you want to check only the columns of a specific data asset, click the asset name on the **Assets** tab or click **View columns** from the context menu.
{: tip}

- Column name. A Key icon next to the name indicates that the column is assigned as primary key.

- Asset to which the column belongs and the context of that asset

- Display name. You can edit the names and accept AI-suggested names inline.

- Description. You can edit the descriptions and accept AI-suggested descriptions.



The **Columns** tab is empty until enrichment runs at least once.

### Column details
{: #col_details}

Access the column's enrichment details by clicking the column name or by clicking **View column details** from its context menu. On the **Details** tab in the side panel, you can find this information:

Display name

:   Based on the default enrichment objectives, which include **Expand metadata**, the **Display name** initially contains an alternative name for the column that was found through fuzzy matching. Fuzzy matching expands the source name based on a predefined glossary to provide a name that is easy to understand. 

:   The expanded name might already be assigned because the confidence was high enough or it is a suggestion that you can accept. At any time, you can edit the display name.

Description

:   This section can contain an AI-generated description for the column, based on the **Expand metadata** enrichment objective. The description might already be assigned because the confidence was high enough or it is a suggestion that you can accept. At any time, you can edit the description.
