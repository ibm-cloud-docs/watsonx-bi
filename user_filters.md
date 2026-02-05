---
copyright:
  years: 2025, 2026
lastupdated: "2026-02-05"

keywords:
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

# Manage data access with User filters
{: #user_filters}

User filters let you control which users or user groups can view specific data within a metric. Administrators and Data analysts can define conditions on a metric defintion in the semantic data model to ensure that users only see the data that they are permitted to access.
{: #shortdesc}

## User filter logic 
{: #user_filter_logic}

Users will only see values calculated from the rows that they are allowed to view.

If a user belongs to a user group that has multiple filters, all conditions must be true at the same time. This means the user will only see data that satisfies all filters in that group. For example:

  A group has filters for *year = 2013* **and** *year IN (2012, 2013)*.
  Only rows where **year = 2013** meet both conditions.

If a user belongs to multiple user groups, they can see any data allowed by **any** of the groups they belong to.Watsonx BI combines filters from different groups using **OR logic**. For example:

  User group A allows *year = 2013*
  User group B allows *year IN (2012, 2013)*

A user in both groups will see rows for **2012 and 2013** because the filters are combined using OR.


## Limitations
{: #user_filter_limitations}

- User filters apply only to metric definitions, not base tables. If multiple metric definitions use the same table, the filter must be applied to each definition individually.

- User filters must be re‑exported or re‑published after any modification for changes to take effect in the project or Metrics catalog.

- Users with **Editor** or **Admin** role in the project, can modify a user filter even if they are not the filter's owner.


## Adding a user filter
{: #add_user_filter}

To add user filters to a metric definition in a semantic data model:

1. In **Data and Metrics**, open the semantic data model that contains the metric definition that you want to update. 

2. In **Advanced mode**, select the metric definition and from its menu, choose **Manage user filters**.

3. Click **Add filter** if you don't have existing filters. 

4. Enter a name for the filter and then click **Add filter** to define the filter.

5. Select a table column and set the condition that determines which data values the filter applies to.

6. Select the users or user groups who should be allowed to view the data that meets the condition.

7. Save your changes and the semantic data model. 

8. Export the metric definition to apply the filter to the corresponding metric in the project. 

There are similarities in the **user and user group** settings interface between user filters and publishing metrics, but they serve different purposes. In user filters, these settings determine which data a user can see. During publishing, they control which users can access the metric in the **Metrics catalog**.
{: note}

## Removing a user filter
{: #remove_user_filter}

To remove a user filter from a metric definition in a semantic data model:

1. In **Data and Metrics**, open the semantic data model that contains the metric that you want to update. 

1. In **Advanced mode**, select the metric and from its menu, choose **Manage user filters**.

1. Click the (-) icon next to the user filter name. 

1. Confirm deletion. 

1. Save your changes and the semantic data model. 

1. Export the metric definition to apply the changes to the corresponding metric in the project. 

Removing a user filter restores full visibility of the data, and any metrics that depend on that data, for all users.
