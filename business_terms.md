---
copyright:
  years: 2026
lastupdated: "2026-01-07"

keywords: business terms, glossary, 
subcollection: watsonx-bi

---

{{site.data.keyword.attribute-definition-list}}


# Business terms
{: #business_terms}

Administrators can add business terms, that represent your organization's terminology, to the semantic layer in {{site.data.keyword.wxbia_full}}. {: #shortdesc}

Business terms are standardized definitions of business concepts so that your data is described in a uniform and easily understood way across your organization. 

Business terms can describe the contents of the data, the sensitivity of the data, or other aspects of the data, such as the subject or purpose of the data. You can assign one or more business terms to individual columns in relational data sets, to other governance artifacts, or to data assets.

You can use business terms to:

- Show that columns with different column names have the same type of data

- Translate technical or obscure column names to terminology that makes sense and has an accessible definition

- Link assets that have similar data

- Define relationships with other terms

For example, suppose your company has data that includes personal identification numbers from people in many different countries. The columns that contain personal identification numbers are named with abbreviations of the country-specific terms, for example: "SSN" for US Social Security Numbers, "SIN" for Canadian Social Insurance Numbers, "UID" for Indian Unique Identification Numbers, and so on. You can create a business term named "Personal identification number" and assign it to all of the columns that contain personal identification numbers, to show that the "SSN", "SIN", and "UID" columns contain the same type of information and what that information means. 

## Predefined business terms or glossary in {{site.data.keyword.wxbia_short}} 
{: #predefined_terms}

{{site.data.keyword.wxbia_full_notm}} comes with predefined business terms in the Knowledge accelerator artifact and the Business Analytics category. These business terms act as metadata to enrich data assets so that AI can better understand your data and provide accurate responses to your questions. 

To view pre-defined business terms, go to the **Navigation Menu** and open **Governance > Business Terms**.

The predefined business terms have a hierarchy defined. Some of the business terms are identified by tags such as *concept*. For each of these concept terms, there is a set of business terms that describe the various properties related to the concept. 

For example, the concept of **Person** has related terms Age, Passport Number, First Name and Last Name. These property terms are related to the relevant concept term through the **Is Part Of** relationship. 

Some of the terms have predefined relationships with the relevant data classes to assist with Term Assignment in metadata enrichment. In addition, where appropriate, these terms have relationships with the standard IBM watsonx.data intelligence classifications of Personal Information, Personally Identifiable Information, and Sensitive Personal Information.

Click a business term under **Governance > Business Terms** to view the associated tags, relationships, and related artifacts.

For more information, see the related IBM watsonx.data intelligence topic, [Business terms](https://dataplatform.cloud.ibm.com/docs/content/wsj/governance/dmg16.html?context=df&audience=wdp){: external}.

## Business terms in metadata enrichment 
{: #terms_mde}

Business terms can be automatically assigned to or suggested for a column during metadata enrichment.

Assigned and suggested business terms have a confidence score attached to them. Terms are assigned or suggested when the confidence level exceeds the minimum confidence level thresholds for a term to be assigned or suggested. The default setting for assignment threshold is 60% and suggestion threshold is 50%. 

In {{site.data.keyword.wxbia_short}}, business term assignment uses the following methods:

- Machine learning: A built-in supervised machine learning model is used to assign terms. By default, the built-in model is trained with assets from the project.

- Data-class-based assignments: Terms are assigned based on the data class assignment for a column. Appropriate linkage between data classes and terms is a prerequisite for quality results here.

- Name matching: Terms are assigned based on the similarity between a term and the name of the asset or column.

- Gen AI based term assignment: Domain-specific business terms are assigned and suggested by using IBM Slate 30m encoding model. The AI model takes into account names and descriptions of assets and columns, and semantically matches terms with that metadata. This means that terms can be assigned even if they aren't exact matches.

## Adding business terms
{: #adding_terms}

Before you add a business term, you need to decide the meaning that the term represents, where it fits in the category structure, and its relationships with other artifacts.

To create, edit, or delete business terms, you must have permissions to **Access governance artifacts**. Additionally, you must have one of these category collaborator roles in the primary category for the business term:

- Admin

- Owner

- Editor

- A custom role with the permission to create, edit, or delete business terms

To create a business term: 

1. From the **Navigation Menu**, open **Governance > Business Terms**.

2. Click **Add business term > New business term**.

3. Enter the details for the business term and click **Save as draft**.

4. (Optional) On the **Overview** tab, you can define relationships among business terms, synonyms, or other business terms.

5. Click **Publish**.

You can also import business terms from a CSV file. 

1. From the **Navigation Menu**, open **Governance > Business Terms**.

2. Click **Add business term > Import from file**. 

3. Upload the file and choose a method for merging imported and existing artifacts. 

4. On the Task inbox page, review the imported business terms.

5. Click **Publish**.

You can edit custom properties for a business term in the details section. 
