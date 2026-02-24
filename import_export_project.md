---
copyright:
  years: 2025
lastupdated: "2026-02-24"

keywords: import project,copy project
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

# Importing and exporting a project
{: #import_project}

You can create a project that already has assets by importing a project from the **Data and Metrics** page. {: #shortdesc}

You can import or export a project only from **Data and Metrics**. The import and export project options are not available on the **Projects** page in {{site.data.keyword.wxbia_short}}.

You can't export and import a project between {{site.data.keyword.wxbia_short}} software and {{site.data.keyword.wxbia_short}} as a Service. 


## Prerequisites
{: #prereq_import}

You need a local .zip file of a previously exported project to import it. Importing a project from a local file is a method of copying a project. 

Other requirements include:

- Project size must be less than 500 MB
- You must have at least the Editor role in the project
- The project must contain the minimum viable components

### Preparing a project for export

Before you export a project, verify that your project contains:

**Active connections**
: Ensure that all data source connections are properly configured.

**Complete metadata** 
: Run metadata imports to ensure that all data assets are up-to-date.

**Semantic data models** 
: Verify that semantic data models are properly configured and linked to metadata imports.
: Make sure that the semantic data model isn't empty. Empty semantic data models cannot be imported.


## Exporting a project
{: #project_export}

When you export a project, the system creates a .zip file that contains all project assets, their relationships, and supporting metadata.

To export a project, follow these steps:

1. On the **Data and Metrics** tab, click **Export or import project** next to the project switcher. 

2. Select **Export project**.

3. Select a project to export and click **Export**.

The exported project is now available as a .zip file. 


## Importing a project
{: #steps_import}

Complete the following steps to import a project:

1. On the **Data and Metrics** tab, click **Export or import project** next to the project switcher.

2. Select **Import project**.

3. Enter a name for the project and upload the .zip file that contains the exported project. 

4. Click **Import**.

After the project imports successfully, you can immediately start using the data in the project on the **Data and Metrics** page. 

If the project contains metadata enrichment assets and metrics, you can start asking questions about the data in the project.

It can take a few minutes for metrics to show up on the **Data and Metrics** page after import. 
{: note}

## Verifying import success
{: #verify_import}

After you import a project, verify that all components were imported correctly.

### Immediate verification

Immediately after you import your project:

1. Go to **Data and Metrics** and verify that the project appears in the project switcher.
2. Check that all data source connections are listed.
3. Verify that tables and data objects appear in the data tree.
4. Confirm that semantic data models are available.

### Delayed verification

Some components might take a few minutes to fully initialize:

- Metrics
- BI visualizations
- Enrichment data

### Relationship verification

The import process automatically reconstructs all relationships between assets:

- Semantic data models are linked to their metadata imports.
- Data assets are connected to their physical constraints.
- BI visualizations reference their underlying semantic data models.
- All usage dependencies are preserved.

If you encounter issues with relationships, check the connection credentials first, as missing credentials can prevent proper relationship reconstruction.


## Managing credentials after import
{: #credentials}

Connection credentials are handled differently depending on the connection type.

**Shared connections**
:    Shared connections include their credentials in the export, so they are automatically available after import. No additional action is required for shared connections.

**Personal connections**
:    Personal connections do not include credentials in the export for security reasons. After you import a project that has personal connections, you must reenter credentials when you first access data from those connections.

To enter credentials for a personal connection:

1. Go to **Data and Metrics**.
2. Try to access data from the connection, for example expand a table or run a query.
3. When prompted, enter your credentials for the data source.
4. Click **Connect** to save the credentials.

Your credentials are stored securely and associated with your user account only.

### Updating connection credentials

If you need to update credentials for any connection after import:

1. Go to **Data and Metrics**.
2. Click the connection in the data tree.
3. Select **Edit connection**.
4. Update the credentials as needed.
5. Click **Save**.

Test the connection after you update credentials to ensure proper access to the data source.
