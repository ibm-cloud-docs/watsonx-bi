---
copyright:
  years: 2025
lastupdated: "2026-01-07"

keywords: classifications
subcollection: watsonx-bi

---

{:codeblock: .codeblock}
{:note: .note}
{:pre: .pre}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:table: .aria-labeledby="caption"}
{:tip: .tip}
{:video: .video}
{:external: target="_blank" .external}
{:step: data-tutorial-type='step'}

# Classifications 
{: #classifications}

Classifications describe specific characteristics of the meaning of data. Much like tags or labels, you can create classifications to describe other characteristics of data or other governance items. {: #shortdesc}

In {{site.data.keyword.wxbia_short}}, predefined classifications are available in the [uncategorized category], which describe the sensitivity of the data: 

- Confidential: Confidential data is data that if compromised in some form, is likely to result in significant or long-term harm to the institution or individuals whose data it is.

- Personal information (PI)- Personal information (PI) is defined as any data that relates to an identified or identifiable individual. PI includes both identifiers, such as name or employee serial number, and any personal information that can be  associated with an individual, such as age, profession, preferences, net worth or mobile device location.

- Personally identifiable information (PII) - Personally identifiable information (PII) is defined as any data that might potentially identify a specific individual. Any information that can be used to distinguish one person from another can be considered PII.

- Sensitive personal information (SPI) - Sensitive personal data is defined as personal data that consists of information relating to an individual about racial or ethnic origin; political opinions; religious beliefs or other beliefs of a similar nature; trade union membership; physical or mental health or condition; sexual life; or any criminal or alleged criminal history of a person.

##  Creating a classification
{: #create_class}

To create classifications, you must have user permission for **Access governance artifacts**. Also, you must have one of these category collaborator roles in the primary category for the classification:

- Admin

- Owner

- Editor

- A custom role with the permission to create classifications

To create a business term: 

1. Go to **Navigation menu > Governance > Classifications**.

2. Click **Add classification > New classification**. 

   Classification names must be unique within a category.

3. Enter the details for the classification and click **Save as draft**.

4. (Optional) On the **Overview** tab, you can define relationships with other classifications. 

   You can select the main or Parent classification to which you want to assign the current classification. Or you can select the classifications that depend on the current classification.

5. Click **Publish**.

You can also import business terms from a CSV file. 

1. Go to **Navigation menu > Governance > Classifications**.

2. Click **Add classification > Import from file**. 

3. Upload the file and choose a method for merging imported and existing artifacts. 

4. On the **Task inbox** page, review the imported classification.

5. Click **Publish**.

