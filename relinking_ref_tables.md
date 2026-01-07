---
copyright:
  years: 2025
lastupdated: "2026-01-07"

keywords: relink reference tables
subcollection: watsonx-bi



---

{{site.data.keyword.attribute-definition-list}}


# Relinking referenced tables
{: #model_relink_tables}

You can change the references of tables to point to different tables in a semantic data model. {: #shortdesc}

1. In the semantic data model panel, or on the **Relationships** or **Custom tables** tab, click the table context menu.

2. Select **Relink**.

   If the semantic data model is based on another semantic data model, the **Relink** dialog box includes the current and the source semantic data models.

   If the semantic data model is based on another type of data source, such as an uploaded file, only the semantic data model panel is available in the **Relink** dialog box.

2. Expand the semantic data model, and if applicable, the source tree.

3. Select the table that you want to be the new target table, and click **Relink**.

  The table reference is changed.
