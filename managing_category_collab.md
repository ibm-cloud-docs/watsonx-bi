---
copyright:
  years: 2025
lastupdated: "2026-02-24"

keywords: categories, category permissions
subcollection: watsonx-bi

---

{{site.data.keyword.attribute-definition-list}}

# Managing category access
{: #category-collab}

When you create a category, you can add collaborators and assign them roles in the category. The roles provide permissions to perform actions in the category. Subcategories inherit all collaborators with the same roles from their higher-level categories.
{: .shortdesc}

- [Required permissions](#permissions)
- [Predefined roles](#predefined)
- [Adding collaborators](#collaborators)
- [Changing collaborator roles](#change)
- [Deleting collaborators](#delete)

## Required permissions
{: #permissions}
You must have a role with the **Administer collaborators** or **Ownership** permission in the category to manage category collaborators:
- **Administer collaborators**
: Manage collaborators with any role except a role with **Ownership** permission. The default role that meets this criteria is the **Admin** role.
- **Ownership**
: Manage collaborators with any role. The default role that meets this criteria is the **Owner** role.

The users that you add as category collaborators must have one of these user permissions:
- **Access governance artifacts**
- **Manage governance categories**
- **Administer governance artifacts**

You can add a user group as a collaborator. If the group is assigned one of the required permissions, all its users have the group's role in the category. Otherwise, only those users who have one of the required permissions have the group's role in the category. The predefined user group, **All users**, includes all users who have one of the required user permissions for categories. 

The following restrictions apply to collaborators: 
- Updates to category collaborators or roles might take up to 20 minutes to take effect.
- Category requires at least one collaborator with an **Owner** role. The ownership of a category can only be changed by owners, or by a user with the **Administer governance artifacts** permission. To avoid a situation where the only owner is removed, you can add a group of users as owners of a category.

## Predefined roles
{: #predefined}
The predefined category collaborator roles provide permissions to perform certain actions. 

|Action                               |Viewer|Reviewer|Editor|Admin|Owner|
|----|----|----|----|----|----|
|View categories and artifacts        |✓|✓|✓|✓|✓|
|Export categories and artifacts      |✓|✓|✓|✓|✓|
|View draft artifacts                 | |✓|✓|✓|✓|
|Manage artifacts and draft artifacts | | |✓|✓|✓|
|Manage nonowner collaborators        | | | |✓|✓|
|Create, edit, or import subcategories| | | |✓|✓|
|Manage owner role                    | | | | |✓|
|Delete categories                    | | | | |✓|

You can't modify or delete predefined category roles.


## Adding collaborators
{: #collaborators}

You can assign one role or multiple roles to a collaborator. For example, if you want one person to both create artifacts and review them, you must assign that collaborator the roles of **Editor** and **Reviewer**.

The more roles that you assign to each collaborator, the longer categories take to load. For best results, assign each collaborator the role with the most permissions that they need in the highest level category that they belong to.

To add collaborators to a category:

1. Go to the **Access control** page for the category.
1. Click **Add collaborator**.
1. Select the users to add as collaborators, or user groups.
1. Select the category role or roles that you want to assign to each user.
1. Click **Add**.

The collaborators are added with their assigned roles to the category and all its subcategories.

## Changing collaborator roles
{: #change}

You can change the role for an individual category collaborator or a user group. You can change the role only in the category where the collaborator is assigned that role. You can't change the role of a collaborator in a subcategory that inherited that collaborator and role from a higher-level category. To see the category in which a collaborator is assigned a particular role, go to the category's **Access control** page, then click the Show inheritance icon.

A category must have at least one collaborator that is assigned a role with the ownership permission. If you are the only collaborator in a top-level category that has a role with the ownership permission, you cannot change your role.
{: .note}

To change the category role for a collaborator:
1. Go to the **Access control** page for the category.
1. Click the pencil icon next to the collaborator name, select one or more roles, and click **Save**.

The role applies to all subcategories of the category.

## Deleting collaborators
{: #delete}
You can remove collaborators from the category where they were added. You can’t remove collaborators from a category if they are inherited from higher-level categories.

To remove a collaborator from a category, click the trash icon next to the collaborator name. The collaborator is removed from the category and all its subcategories where they have the same role. The collaborator is not removed from any subcategories where the collaborator is assigned a different role.

For example, you might have one collaborator who is a **Viewer** in a category and one of its subcategories, but an **Editor** in a second subcategory. If you delete the collaborator from the category, the collaborator is deleted from the category and subcategory where they are a **Viewer**. However, the collaborator remains in the subcategory where they are an **Editor**.





