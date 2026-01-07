---
copyright:
  years: 2025
lastupdated: "2026-01-07"

keywords:
subcollection: watsonx-bi

---

{{site.data.keyword.attribute-definition-list}}


# Reference data
{: #reference_data}

Reference data sets define standard values for specific types of data to classify data and measure consistency. {: #shortdesc}

Reference data sets act as lookup tables that map codes and values. Some reference data sets are standardized by organizations, such as the International Organization for Standardization (ISO). Reference data can be hierarchical or mapped across related sets.

Reference data helps you, for example, define a standard set of values for certain fields. It can be useful to create a standard definition of country codes and use this reference data to ensure that country code fields comply. Different designations such as “US”, “USA”, “United States”, and "America" can all be resolved to the same reference data value. As a result you can get much more consistent data.

The predefined reference data sets in {{site.data.keyword.wxbia_short}} provide physical and sovereign locations and can be found in the Locations category:

- Physical locations: Physical location is the geographical location of the data asset.

- Sovereign locations: Sovereign location is the governing body that has jurisdiction over the data asset.

An example of a physical location is Tokyo and its sovereign location is Japan.

## Creating reference data
{: #create_reference}

A reference data set consists of a number of reference data values, where each reference data value must at least have a code and its value defined. 

When you design a reference data set, you need to decide what format of values to use, which code-value pairs constitute the set, and if the set should be related to any other existing sets. You can import the already existing reference data sets and modify them to suit your needs, or create a new reference data set manually.

To create reference data, you must have user permission for **Access governance artifacts**. Additionally, you must have one of these category collaborator roles in the primary category for reference data:

- Admin
- Owner
- Editor
- A custom role with the permission to create reference data sets

To create reference data: 

1. From the **Navigation Menu**, open **Governance > Reference data**.

2. Click **Add reference data set > New reference data set**. 

3. Enter the details for the reference data set. Note, reference data set names must be unique within a category.

4. Under **Add Columns**, create the columns for the reference data set. If you didn't upload a CSV file, you need to provide details for each column. 

5. Review the information under **Review** and click **Create**.

You can also import reference data from a CSV file. 

1. From the **Navigation Menu**, open **Governance > Reference data**.

2. Click **Add reference data set > Import from file**. 

3. Upload the file and choose a method for merging imported and existing artifacts. 

For more information, see the related IBM watsonx.data intelligence topic, [Reference data](https://dataplatform.cloud.ibm.com/docs/content/wsj/governance/reference_data_sets.html?context=df&audience=wdp){: external}.
