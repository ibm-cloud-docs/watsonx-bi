---
copyright:
  years: 2025
lastupdated: "2026-01-07"

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

You can't export and import a project between {{site.data.keyword.wxbia_short}} software and {{site.data.keyword.wxbia_short}} as a service. 
{: important}


## Prerequisites
{: #prereq_import}

You need a local ZIP file of a previously exported project to import it. Importing a project from a local file is a method of copying a project. 

Other requirements include:

- Project size must be less than 500 MB
- You must have at least the Editor role in the project

To export a project, follow these steps:

1. On the **Data and Metrics** tab, click the **Export or import project** button next to the project switcher. 

2. Select **Export project**.

3. Select a project to export and click **Export**.

The exported project is now available as a ZIP file. 

An exported project that contains uploaded files cannot be imported. 
{: important}

## Steps to import a project
{: #steps_import}

1. On the **Data and Metrics** tab, click the **Export or import project** button next to the project switcher.

2. Select **Import project**.

3. Enter a name for the project and upload the ZIP file that contains the exported project. 

   Exported projects that contain uploaded files are not supported. Remove any uploaded files from the local ZIP file before you upload the file for import. You can add uploaded files to the project after import. For more information, see [Upload a file](/docs/watsonx-bi?topic=watsonx-bi-upload){: external}.
   {: note}

4. Click **Import**.

After the project imports successfully, you can immediately start using the data in the project on the **Data and Metrics** page. 

If the project contains metadata enrichment assets and metrics, you can start asking questions about the data in the project.

It can take a few minutes for metrics to show up on the **Data and Metrics** page after import. 
{: note}

## Entering credentials
{: #credentials}

As you work with the data in the imported project, you might be prompted to enter your personal credentials to the data source connection.
