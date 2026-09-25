---
copyright:
  years: 2025, 2026
lastupdated: "2026-09-24"

keywords: review mde, review metadata enrichment, review enrichment
subcollection: watsonx-bi

---

{{site.data.keyword.attribute-definition-list}}


# Reviewing metadata enrichment 
{: #review}

Review enrichment results to ensure that the metadata applied to your data is accurate and meaningful. Metadata enrichment generates business context that helps watsonx BI understand your data and return more accurate responses in conversations. {: #shortdesc}

## Accessing enrichment results
{: #access_review}

The location where you review enrichment results depends on your deployment.    

### watsonx BI as a Service
{: #wxbi_enrich}

Review enrichment results from the **Data sources** tab.

1. Go to **Data and Metrics > Data sources**.
1. Locate the data source that you want to review.
1. Click the data source to view details or from the menu, click **View details**.

The data source details page displays enrichment status and column-level metadata generated during enrichment.

### watsonx BI on IBM Software Hub
{: #wxbi_onprem_enrich}

You can open the **Review enriched data** page from the following locations:

-  Metadata enrichment page during metric creation 

  This option is available only while you are still in the metadata enrichment workflow. After you move forward to the **Metrics overview** page, you can no longer access the review page from here.

- Project view 

  1. Go to **Navigation menu > View all projects**.

  1. Select the project that contains the enriched asset. 
  
  1. Open the **Assets** page and locate the metadata enrichment asset.

## Reviewing enrichment in watsonx BI as a Service
{: #about_review_saas}

After enrichment completes, open the data source details page to review the generated metadata before it is used in conversations.

The Column enrichment section shows:

- Enrichment status
- Metadata source indicators
- Column-level metadata
- Approval status

Expand **Review and approve enrichment** to view the meaning of each metadata indicator. Each metadata value displays a status that identifies its source and behavior during re-enrichment.

User-set

:   Metadata that you added or modified. User-set metadata:

:   - Is always used in conversations.
:   - Isn't overwritten during re-enrichment.

AI-suggested

:   Metadata generated automatically during enrichment. AI-suggested metadata:

:   - Is used in conversations.
:   - Can be updated during re-enrichment unless it is approved or manually updated.

Not set

:   No metadata is available for the field. Add metadata to provide additional business context for the data.

### Reviewing column metadata
{: #review_column_saas}

Review the metadata generated for each column and confirm that it accurately reflects your business terminology.

You might see the following metadata:

| Metadata     | Description                                                      |
| ------------ | ---------------------------------------------------------------- |
| Display name | A business-friendly name for the column.                         |
| Description  | A description of the column's business meaning.                  |
| Represents   | The type of business concept represented by the column. For example, a date, time, or a geographic location. |
| Usage        | Defines how a column is used in analysis. A column can be categorized as an attribute for describing and grouping data, a measure for calculations and metrics, or an identifier for uniquely identifying and linking records.   |
| Aggregation  | Defines how values in the column are summarized in analysis. Examples include Sum, Average, and Count. Aggregation helps ensure that metrics and query results are calculated correctly. |


### Approving metadata
{: #approve_metadata_saas}

Review AI-generated metadata before approving it for use in conversations.

1. Open the data source details page.

1. In the Column enrichment section, review the generated metadata.

1. Approve metadata by using one of the following methods:

   - To approve a single metadata value, click **Approve** next to the value.

   - To approve multiple rows, select the rows and click **Approve**.

After metadata is approved, the approved values are used in conversations. Re-enrichment doesn't overwrite approved metadata.

To modify metadata before approval, click the **Edit** icon next to the value, update the field, and then click **Approve**.

## Reviewing enrichment in watsonx BI as a Software
{: #about_review_onprem}

When you open the enrichment results, you can view the enriched data at both the asset level and column level. A side panel also provides a summary of relevant information about the metadata enrichment.

The following indicators are used in the results tables and the details panels:

- A purple square for automatically assigned display names and for AI-generated descriptions that were automatically assigned

- A blue dot for accepted display-name or description suggestions, or for edited display names or descriptions 

- An AI label for AI-suggested descriptions 


### Reviewing enrichment at the asset level
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



### Reviewing results at the column level
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
