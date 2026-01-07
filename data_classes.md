---
copyright:
  years: 2025
lastupdated: "2026-01-07"

keywords: data classes
subcollection: watsonx-bi

---

{{site.data.keyword.attribute-definition-list}}


# Data classes
{: #data_classes}

Data classes classify data based on the structure, format, and range of values of the data. {: #shortdesc}

Data classes help to describe the domain of the data values present within a column in a structured data asset. For example, City or Postal codes can be data classes.

Data classes are used during metadata enrichment to increase the accuracy of business term assignment recommendations. They can be seen as a syntactic counterpart to the semantic business terms. Data classes are automatically assigned to matching data columns during profiling in metadata enrichment and are shown on the **Profile** tab in metadata enrichment results.

Predefined data classes are available in the [uncategorized] category but you can also create data classes by defining matching criteria with an expression or a reference data set. 

When you create custom data class artifacts, you can use matching data to specify how to classify data automatically. You can also add related artifacts like classifications and business terms, which are then suggested during enrichment when a data class is assigned to a column in a data asset.

For more information, see the related IBM watsonx.data intelligence topic, [Data classes](https://dataplatform.cloud.ibm.com/docs/content/wsj/governance/data_classes.html?context=df&audience=wdp){: external}.

## Creating a data class
{: #create_data_class}

To create a data class, you must have user permission for **Access governance artifacts**. Additionally, you must have one of these category collaborator roles in the primary category for data classes:

- Admin
- Owner
- Editor
- A custom role with the permission to create data classes

To create a data class: 

1. From the **Navigation Menu**, open **Governance > Data classes**.

2. Click **Add data class > New data class**. Data class names must be unique within a category.

3. Enter the details for the data class and click **Save as draft**.

4. (Optional) On the **Overview** tab, you can enable data matching for this data class and define relationships between business terms, classifications, and other data classes.

5. Click **Publish**.

You can also import business terms from a CSV file. 

1. From the **Navigation Menu**, open **Governance > Data classes**.

2. Click **Add data class > Import from file**. 

3. Upload the file and choose a method for merging imported and existing artifacts. 

4. On the Task inbox page, review the imported data class.

5. Click **Publish**.

## Relationships between data classes
{: #relationship_data_class}

You can use hierarchies to create relationships between data classes. You can define the following relationships to other data classes within the same category:

- Parent data class

- Dependent data classes

The parent data class is used to organize the data class in parent-children relationships. It also acts as a kind of "pre-filter" if the automatic data matching method is used. If a parent data class has a matching data method, the data matching methods for the children data classes will only be evaluated if the data matching method for the parent data class returns a positive match. This means that if you define a parent data class it has an impact on the criteria used by the data classification process to decide whether the data class should be assigned to a data field or not.

## Relationships with business terms and classifications
{: #relationship_terms_class}

You can define relationships between a data class and business terms and classifications. The classifications and business terms that you add are suggestions for columns to which the data class is assigned.

When you add relationships between data classes and business terms, those business terms are automatically assigned to assets when their related data classes are assigned during metadata enrichment. For example, a data class **Email address** can be related to a business term **Contact method**. When the metadata enrichment process detects a column that matches the data class **Email address**, both the data class **Email address** and the business term **Contact method** are assigned. 

However, a data class is not automatically assigned when one of its related business terms is assigned to a column.
