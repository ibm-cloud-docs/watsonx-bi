---
copyright:
  years: 2025
lastupdated: "2025-08-07"

keywords: review mde, review metadata enrichment, review enrichment
subcollection: watsonx-bi

---

{{site.data.keyword.attribute-definition-list}}


# Review enrichment
{: #review}

After metadata enrichment completes, you can review the enrichment results to make sure the metadata applied is meaningful and accurate. {: #shortdesc}

When you open the enrichment results, you can view the enriched data at both the asset level and column level. A side panel also provides a summary of relevant information about the metadata enrichment.

The following indicators are used in the results tables and the details panels:

- A purple dot for automatically assigned terms or data classes

- A purple square for automatically assigned display names and for AI-generated descriptions that were automatically assigned

- A blue dot for accepted display-name or description suggestions, or for edited display names or descriptions 

- An AI label for AI-suggested descriptions 


## Reviewing enrichment at the asset level
{: #rev_asset}

On the **Assets** tab, the following information is provided for each data asset in the scope of the metadata enrichment:

- Asset name (for relational data, also the table type is shown)

- Source information  

- Display name - You can edit the names and accept suggested names.

- Description - You can edit the descriptions and accept AI-suggested descriptions.

- Assigned business terms and the number of suggested terms

- Assigned classifications

- Assigned primary keys and the number of suggested ones

- Overall data quality score that was achieved in the enrichment

- Review status

- The status and the date and time of the last enrichment

By default, all of the information is shown on the tab but you can customize the view and show only the information that you need. Click the **Customize columns** icon and deselect all columns that you want to hide. 

You can also reorder the columns by clicking an entry and dragging it to a new position.

You can directly go to the columns of an asset by clicking the asset name or **View columns** in the context menu.

### Asset details
{: #asset_enrich}

Access an asset's enrichment details by clicking the asset name or by clicking **View asset details** in the context menu. On the **Details** tab in the side panel, you can find the following information:

- **Display name**

  The **Display name** initially contains an alternative name for the data asset that was found through fuzzy matching. Fuzzy matching expands the source name based on a predefined glossary to provide a name that is easy to understand. 

  The expanded name might already be assigned because the confidence was high enough or it is a suggestion that you can accept. At any time, you can edit the display name.

- **Description**

  This section contains an AI-generated description, which might already be assigned because the confidence was high enough. Otherwise, it is a suggestion that you can accept. At any time, you can edit the description.

- **Source**

  The **Source** section shows the connection and database for the connected asset. For files uploaded from a local system, the **Project** is shown in the **Source** column. 

- **Asset details**

  Asset details include the table type, the number of columns and rows in the asset, and its data format.

- **Asset owner**

  The asset owner is usually the user who added the asset to the project. 

- **Enrichment details**

  The enrichment details includes the list of enrichment objectives and the sampling method, which are set by default in {{site.data.keyword.wxbia_short}}. The enrichment details also includes the date when the asset was last enriched and a link to the corresponding job run.

### Governance
{: #governance_enrich}

Governance information for an asset includes the assigned and suggested business terms and assigned classifications, which are listed in the **Business terms** and **Classifications** columns of the results. For assigned terms, a purple dot indicates that at least one of the terms was automatically assigned.

Access detailed governance information for an asset by clicking the asset name, by clicking the **View more** link in the **Business terms** or **Classifications** column, or by clicking **View asset details** from its context menu. 

On the **Governance** tab in the side panel, you can manage business term and classification assignments.

- **Business terms** 

  Review assigned and suggested business terms. Each assigned or suggested term has a confidence score. You can click a term to see some of its properties: its description, its primary and secondary categories, hierarchical type relationships, and related classifications and data classes.

  You can also search for any business terms that are not listed as suggestions and assign them manually. Remove any assigned terms that you think are inaccurate. **Depending on your project settings, such negative feedback is considered in the next enrichment run. Business terms that you remove in bulk are treated differently from those that you remove individually.** If you remove a term from a single asset, that term is considered rejected. The removed term remains listed in the side panel and you can reassign it at any time. 

- **Classifications**

  Review assigned classifications. Depending on the project settings, classifications that are related to a business term are also assigned when the business term is automatically assigned. You can assign more classifications or remove the classifications that were assigned by the system and replace them with other ones. 

### Keys
{: #keys}

The **Keys** section displays the **Primary key** and **Relationships**. Enrichment uses profiling statistics and name similarities between columns to provide primary and foreign keys and to suggest or assign relationships between assets and columns. The default enrichment settings for key relationships are applied and this type of relationship analysis requires profiling.

In the **Primary key** section, for primary keys that were identified through primary key analysis, the number and percentage of unique values, the number and percentage of null values, and the number of analyzed columns is shown. This information is not available for a key that was picked and assigned manually without prior primary key analysis, or for suggested primary keys that result from in-depth key relationship analysis.

The **Relationships** section provides these views of the assigned relationships:

- Parent of tab: In relationships to the listed assets, the current asset provides the primary key.
- Child of tab: In relationships to the listed assets, the current asset provides the foreign key.

If a relationship analysis was run but no relationships are assigned yet, you can click the plus icon to view and work with the analysis results.

At any time, you can edit the assigned relationships by clicking the pencil icon.

### Data quality score
{: #data_quality_score}

A data quality score is displayed only if at least one data quality check was applied to the asset. Otherwise, a dash (—) is shown. 

### Review status
{: #rev_status}

Initially, the review status of all assets in the metadata enrichment is **Not reviewed**. After you review the enrichment results for an asset, you can select the asset and click **More > Mark as reviewed** to set the asset's review status to **Reviewed**.

You can reset the review status of an asset at any time. To change the review status, click **Mark as reviewed** or **Mark as not reviewed** from the asset's context menu. 

### Enrichment status
{: #enrich_status}

The enrichment status column can have these values:

- Not analyzed - Status applies to asset that was added after the last enrichment run.

- Finished - Enrichment for this asset is complete. This status is also shown if the enrichment happened outside the current enrichment asset, for example, if the asset was profiled manually before it was added to this enrichment.

- Failed - An error occurred during the enrichment.

- Canceled - The job run for the enrichment was canceled.

You can sort or filter the result list by enrichment status. For sorting, the primary sort order is by status. Ascending order is canceled, failed, and finished. Depending on the general sort order, assets with the status Not analyzed are displayed unordered at the top or the end of the list.

## Reviewing results at the column level
{: #rev_column}

On the **Columns** tab, the following information is provided for each column in a data asset:

- Column name. A Key icon next to the name indicates that the column is assigned as primary key.

- Asset to which the column belongs and the context of that asset

- Display name. You can edit the names and accept AI-suggested names inline.

- Description. You can edit the descriptions and accept AI-suggested descriptions.

- Assigned business terms and the number of suggested terms

- Assigned data class

- Assigned classifications

- Data quality score for this column

- Review status

The **Columns** tab is empty until enrichment runs at least once.

By default, all information is shown on the tab. You can customize the view and show only the information that you need. Click the **Customize columns** icon and deselect all columns that you want to hide. 

If you want to check only the columns of a specific data asset, click the asset name on the **Assets** tab or click **View columns** from the context menu.

### Column details
{: #col_details}

Access the column's enrichment details by clicking the column name or by clicking **View column details** from its context menu. On the **Details** tab in the side panel, you can find this information:

- **Display name**

  Based on the default enrichment objectives, which include **Expand metadata**, the **Display name** initially contains an alternative name for the column that was found through fuzzy matching. Fuzzy matching expands the source name based on a predefined glossary to provide a name that is easy to understand. The expanded name might already be assigned because the confidence was high enough or it is a suggestion that you can accept. At any time, you can edit the display name.

- **Description**

  This section can contain an AI-generated description for the column, based on the **Expand metadata** enrichment objective. This description might already be assigned because the confidence was high enough or it is a suggestion that you can accept. At any time, you can edit the description.

- The asset to which the column belongs in the **Source** section.

### Governance
{: #col_gov}

Governance information for a column includes assigned and suggested **Business terms**, assigned and suggested **Data classes**, and assigned **Classifications**. 

You can access detailed governance information for a column by clicking the column name, by clicking the **View more** link in the **Business terms**, **Data class**, or **Classifications** column, or by clicking **View column details** from the column context menu. 

You can manage business term, data class, and classification assignments in the **Columns** tab or on the **Governance** tab in the side panel.

- **Business terms**
  
  Review assigned and suggested terms. Each assigned or suggested business term has a confidence score. You can click a term to see some of its properties: its description, its primary and secondary categories, its hierarchical type relationships, and related classifications and data classes.

  Accept suggestions as required. You can also search for any business terms that are not listed as suggestions and assign them manually. Remove any assigned terms that you think are inaccurate. Such negative feedback is considered in the next enrichment run. Terms that you remove in bulk are treated differently from those that you remove individually. If you remove a term from a single column, that term is considered rejected. It is also listed in the side panel, and you can reassign it any time.

  Note that term assignments do not affect data class assignments. If a term that is associated with a data class is assigned to a column by AI or through name matching, the related data class is not automatically assigned as well.

- **Data class**

  Review the assigned data class and the suggested data classes. You can click a data class to see some of its properties: its description, its primary and secondary categories, the type of data matching, its parent and dependent data classes, and related classifications and data classes.

  The confidence score for assigning or suggesting a data class must at least equal the set threshold, which is set by default in {{site.data.keyword.wxbia_short}}. The set threshold takes precedence when data classes are assigned. It is not considered for suggestions. In addition to the confidence score, the priority of a data class is taken into account. 

  A dash (—) indicates that no data class was assigned during analysis.

  Several data classes are more generic identifiers that are detected and assigned at column level only. These data classes are assigned when a more specific data class could not be identified at a value level. Generic identifiers include the following data classes: Code, Identifier, Indicator, Quantity, and Text

  When you assign a data class manually, either a suggested data class or an entirely different one, terms that are associated with that data class are assigned in the next enrichment run. Term assignments, however, do not entail automatic assignment of associated data classes.

- **Classifications**

  Review assigned classifications. Depending on the project settings, classifications that are related to data class or a business term are also assigned when the data class or business term is automatically assigned. You can assign additional classifications or remove the classifications that were assigned by the system and replace them with other ones. 

- **Data quality score**

  A data quality score is displayed only if at least one data quality check was applied to the column. Otherwise, a dash (—) is shown. 

- **Review status**

  Initially, the review status of all columns in the metadata enrichment is **Not reviewed**. After you review the enrichment results for a column, you can click **More > Mark as reviewed** and set its review status to **Reviewed**. 

  Note that, for columns that are marked as reviewed, term assignments are not updated on reruns of an enrichment. 

  You can reset the review status of a column at any time. To change the review status, click **Mark as reviewed** or **Mark as not reviewed** from the column's context menu A column's review status is independent of the review status that its asset has. 
  
  When you do a bulk change of the review status, you might see a success message before the changes are actually complete depending on the volume of the requested changes. You might need to refresh the view several times before you see all changes applied.

  Filter the list of columns by review status to quickly find any columns that must be looked at.
