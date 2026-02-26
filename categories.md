---
copyright:
  years: 2025, "2026"
lastupdated: "2026-02-26"

keywords: categories
subcollection: watsonx-bi

---

{{site.data.keyword.attribute-definition-list}}


# Categories
{: #categories}

Categories organize governance artifacts in a hierarchical structure similar to folders. You can group your governance artifacts in categories to make them easy to find and manage. For example, you can create a category for each business unit, subject area, or geographical area. {: #shortdesc}

Categories can be organized in a hierarchy based on their meaning and relationships to one another. A category can have subcategories, but a subcategory can have only one direct parent category. By default, all users who have permission to access governance artifacts can view categories and their artifacts. 

The following predefined categories are available in {{site.data.keyword.wxbia_full_notm}}:

- **[uncategorized]** category -  Contains other predefined governance artifacts (predefined data classes and classifications). The [uncategorized] catagory can be only a primary category for governance artifacts and its artifacts are always visible to all users. This category can't have subcategories and can't be renamed or deleted. By default, [uncategorized] has these category collaborators: 

   - The platform admin user, with the Owner role. The Owner can change the default category collaborators and their roles.

   - The All users group, with the Viewer role.

- **Business Analytics** category - Contains predefined business terms. The Business Analytics category can be only a primary category for governance artifacts and its artifacts are always visible to all users. By default, the Locations category has these category collaborators:

   - The platform admin user, with the Owner role. The Owner can change the default category collaborators and their roles.
   
   - The All users group, with the Viewer role.

- **Locations** category - Contains predefined reference data sets. The Locations category can be only a primary category for governance artifacts and its artifacts are always visible to all users.
By default, the Locations category has these category collaborators:

   - The platform admin user, with the Owner role. The Owner can change the default category collaborators and their roles.
   
   - The All users group, with the Viewer role.

You can also find the Knowledge Accelerator under categories in {{site.data.keyword.wxbia_short}}, which include a sample grouping of personal information terms. Knowledge Accelerators offer pre-created, extensive, curated glossaries to improve data classification and other governance operations. 

For more information on categories, see [Categories for governance artifacts](https://dataplatform.cloud.ibm.com/docs/content/wsj/governance/categories.html?context=df&audience=wdp){: external} (related topic for IBM watsonx.data intelligence).  

## Creating a category
{: #create_category}

Whether you can create or manage a category depends on the level of the category, your user permissions, and on your role within the primary category. You must have access to the **Manage governance categories** permission to create a category.

### Limitations
{: #limitations_category}

- The combination of the category path plus its name must be unique.

- Category names cannot contain the ">>" characters because these are used to specify the hierarchy path, for example, **primary category >> subcategory**.

- You cannot create a subcategory to the [uncategorized] category.

- The maximum number of categories that a user can be assigned to (either directly, or via the user group) is 10000. If you assign more categories to the user, some of them and their associated artifacts might not be displayed correctly.

### Steps to create a category
{: #steps_category}
  
To create a primary category:

1. From the **Navigation Menu**, choose **Governance > Categories**.  

2. Click **Add category > New category**.

3. Add a name and optional description.

4. In the **Advanced settings** section, choose whether to allow reporting on governance artifacts metadata. If this setting is on, the reporting administrator can enable reporting on metadata for governance artifacts in this category and all its subcategories, and store such metadata in an external database.

5. Click **Create**.

You can also import a category from a CSV file. 

1. From the **Navigation Menu**, open **Governance > Categories**.

2. Click **Add category > Import from file**. 

3. Upload the file and choose a method for merging imported and existing artifacts. 

4. On the **Task inbox** page, review the imported category and click **Publish**.

When you create a primary category, it has these users by default:

- The user who creates the category, with the Owner role

- The Public access group, with the Viewer role

You can add or remove collaborators in the **About this category** pane or on the **Access control** tab.

For more information about adding and removing collaborators, see [Managing access to a collaborator](/docs/watsonx-bi?topic=watsonx-bi-category-collab){: external}.
