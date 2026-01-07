---
copyright:
  years: 2025
lastupdated: "2026-01-07"

keywords: data security, row-level security
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

# Implementing row-level security in semantic data models
{: #row_level_security}

In {{site.data.keyword.wxbia_full_notm}}, you can implement row-level security in the semantic data model by using a database table that defines which data each user is allowed to see. {: #shortdesc}

Let’s say, you need to secure data and dynamically filter it based on the user. You have a table in the database that lists values such as regions and products. The table includes columns product_id and user_email. 

You can take the following steps to secure data:
 
## Step 1. Determine the fields to use to secure data and map them
{: #determine_fields}

To control access, you can limit the list of products that a given user can see based on the user’s email ID. You can create a mapping between the user emails and product ids.

| User_email| Product_id |
|-------|-------------|
| user1@email.com | 101 |
| user1@email.com | 102 |
| user2@email.com | 101 |
| user2@email.com | 104|
{: caption="Table depicts mapping of user email to product ID" caption-side="bottom"}

## Step 2. Apply an embedded filter to the table
{: #apply_embedded_filter}

You can apply an [embedded filter](/docs/watsonx-bi?topic=watsonx-bi-model_filters) at the table or metric level to enforce this security.

Embedded filters can be created for a single column, or for multiple columns in a table. They are defined in a query subject and always apply to the query subject.


1. In a semantic data model tree, locate the table or metric that you want to add the filter to and from its menu, click **Filter**.

2. Enter a name for the filter and define the query subject or expression. For example:  

   ```
   product_id in ( #queryValue('rowLevelSecurityTable.product_id', 'rowLevelSecurityTable.user_email = ' + sq($account.personalInfo.email) )# )
   ```

3. Click **OK** to save. 

A **Filter** icon appears next to the table or metric that has the filter applied to it. 

In this example, the filter ensures that only the product_id values that are associated with the logged-in user's email are returned.

The **queryValue** retrieves a list of product_id values from the rowLevelSecurityTable. The **where** clause filters the table to match the current user's email.

The result is used to filter the main data table, restricting access to only the allowed products.

You can also apply a filter with an explicit email in the filter. However, this approach does not scale well and can be difficult to maintain as the number of users grows.

```
('user1@email.com' = #sq($account.personalInfo.email)# and geography_name_1 in ('Americas') ) or ('user1@email.com' <> #sq($account.personalInfo.email)# and geography_name_1 in ('Asia Pacific') )

```
This filter restricts the "Americas" region to user1@email.com, while all other users see "Asia Pacific". 

