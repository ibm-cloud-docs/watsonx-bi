---
copyright:
  years: 2025
lastupdated: "2026-02-24"

keywords: import project, export project
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

# Understanding project import and export

Before you import or export a project, familiarize yourself with the structure and components of {{site.data.keyword.wxbia_short}} projects. A project includes assets, configuration files, and relationships that combine to allow analysis, modeling, and visualization.
{: .shortdesc}

Create one project when you are working toward one defined business goal and using the same data sources and collaborators. Create multiple projects when your workstreams support different goals, require different collaborators or permissions, or need data isolation. For example, if you are exploring data for a single initiative such as sales forecasting, churn analysis, or inventory optimization, a single project keeps related assets together and is typically easier to manage.
{: tip}

A complete project consists of:

- **Core infrastructure**:
:   - Connections with credentials
:   - Project settings

- **Data layer**:
:   - Data assets
:   - Physical constraints
:   - Metadata imports

- **Processing layer**:
:   - Key analysis areas and results
:   - Metadata enrichment areas

- **Analytics layer**:
:   - Semantic data models
:   - Business intelligence visualizations
:   - Term assignment models

- **Attachments**:
:   - Physical files for each asset type
:   - Verification status tracking

- **Relationships**:
:   - Usage dependencies
:   - Parent-child hierarchies
:   - Constraint references
:   - Cascading delete behaviors



## Project components
Projects are made up of different components. Some components are required for any projects that you import, while others can be included but are not necessary.


**Required components**
:  - Connections
:  - Data assets
:  - Metadata import
:  - Metadata enrichment areas
:  - Physical constraints
:  - Key analysis areas and results
:  - Semantic data models
:  - Project settings

**Optional components:**
:   - Term assignment models
:   - Job run tracking 
:   - Job run attachments
:   - Business intelligence visualizations

Jobs cannot be imported.
{: .note}


## Assets
{: #assets}

An asset is an item that contains information about data, other valuable information, or code that works with data. Assets in projects include data assets, semantic data models, visualizations, and others.

For more information, see [Assets](/docs/watsonx-bi?topic=concepts){: external}.

## Exported file contents

When you export a project as a .zip file, it contains the following items:

- [Root-level files](#root-files)
- [An `/assets/` directory](#assets-directory)
- [An `/assettypes/` directory](#asset-types-directory)

### Root-level files
{: #root-files}

The following files are present at the root level:

**project.json**
:   A file that contains project metadata, such as:
    :   - Project name, description, and type.
    :   - Generator information, such as `watsonx BI`.
    :   - Storage configuration, including GUID and type.
    :   - Creation and update timestamps.
    :   - Project GUID and URL.
    :   - Deployment source and version.

**assetrelationships.json** 
:   A file that contains complete relationship graphs, including:
    :   - All asset relationships and their bidirectional endpoints.
    :   - Relationship types.
    :   - Asset IDs, types, and hrefs for each relationship end.
    :   - Timestamps and user IDs for relationship creation and updates.
    :   - Translated display names for relationships.

**deflate.log** 
:   - An export operation log file.

### `/assets/` directory
{: #assets-directory}

The `/assets/` directory contains actual asset data files that are organized by type and ID.

Asset files contain:

- Semantic data models
- Data assets
- Bivariate files
- Saved business intelligence questions
- Vector store files
- Subdirectories, identified by connection or catalog
- Business intelligence-specific subdirectories

### `/assettypes/` directory
{: #asset-types-directory}

The `/assettypes/` directory contains JSON schema definitions for all asset types. Asset types exist in the following categories:

Each asset type JSON file contains:

- A description.
- An array of searchable fields with types.
- Defined relationship types.
- A duplicate detection strategy.
- Fields that are indexed for search.
- A schema version number.
- The scope of the asset, whether global or project-specific.
- Information about whether the asset can be decorated.

Assets core asset types, business intelligence asset types, extended asset types, and advanced asset types.

Core asset types are the foundation of projects, which include the essential components that are required for data connectivity, modeling, and processing. Core assets types provide the structural backbone that enables all other {{site.data.keyword.wxbia_short}} functions. Core asset types include:
- Database connection definitions.
- Data asset schema with fields, relationships, and localization.
- Semantic data model schema with BI-specific fields. 
- Constraint definitions.
- Import configuration schema. 
- Enrichment area schema. 
- Job definition schema. 
- Job execution schema. 

Business intelligence asset types are designed for interactive analytics, conversational AI, and visualization capabilities within {{site.data.keyword.wxbia_short}}. Business intelligence asset types enable users to ask natural language questions, generate insights, create visualizations, and maintain context across analytical sessions, forming the user-facing intelligence layer of the platform. Business intelligence asset types include:
- Business intelligence question schema. 
- Vector store schema. 
- Business intelligence visualization schema. 
- Visualization reference schema. 
- Conversation schema. 

Extended asset types provide advanced data governance, profiling, and analytical capabilities that enhance the core {{site.data.keyword.wxbia_short}} functions. Extended asset types are useful for data quality initiatives, deeper analytical exploration, and better understanding of data characteristics and relationships. Extended asset types include:
- A term assignment schema. 
- An assignment profile schema. 
- A bivariate analysis schema. 
- Key analysis results. 
- Analysis area definitions. 
- A data profiling schema. 
- A column metadata schema. 

Advanced asset types extend {{site.data.keyword.wxbia_short}} capabilities by integrating with broader IBM components and aiding in complex data science and engineering workflows. Advanced assets types help you build data and AI pipelines, integrate with enterprise data platforms, and are used in advanced use cases that require machine learning, custom scripting, or complex data transformations. Advanced asset types include: 
- IBM Watson machine-learning assets, such as models, deployments, experiments, and pipelines.
- Data integration assets, such as flows, jobs, and components.
- Logical and physical model assets.
- Notebook and script assets.
- Document and library assets.
- Environment and specification assets.
















