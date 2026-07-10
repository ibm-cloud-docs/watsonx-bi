---
copyright:
  years: 2025, 2026
lastupdated: "2026-07-10"

keywords: about watsonx BI
subcollection: watsonx-bi


---

{{site.data.keyword.attribute-definition-list}}

# About {{site.data.keyword.wxbia_full_notm}}
{: #about}

{{site.data.keyword.wxbia_full}} is a generative AI-powered business intelligence partner that brings analytics to business users in your organization. {: #shortdesc}

{{site.data.keyword.wxbia_short_cap}} uses natural language to analyze complex data, providing personalized insights and data-aware recommendations that are easy to understand and actionable.

The {{site.data.keyword.wxbia_short}} service makes it easier and faster for Data analysts and Analytics consumers to make data-driven decisions with the following features:

Personalized and trusted insights

:   Get descriptive and diagnostic insights from your governed business data through a conversational experience. You can use suggested questions to dig deeper into your data.

Natural language interface

:   A natural language canvas where you can co-create insightful, data stories about the performance of your business with generative AI that is tuned specifically to your data and domain.

Personalized metrics

:   Track your most important metrics and get a summary of your business health.

Semantic automation

:   Automate data profiling, business term matching, and data modeling.


## Availability
{: #availability}

{{site.data.keyword.wxbia_full_notm}} is available as a Service and software deployment. 

- As a service on IBM Cloud in the Dallas (us-south) regional data center

- As software that can be installed from IBM Software Hub version 5.2 and higher

## Relationship between services
{: #relationship_services}

### Cloud Service Solutions platform
{: #service_platform}

{{site.data.keyword.wxbia_full_notm}} uses the cloud service platform, which lets you connect to your data and use it for analysis.

The platform provides the following core functionality:

- Security, compliance, and isolation
- Compute resources for running workloads
- Global search for assets across the platform
- The platform assets catalog for sharing connections across the platform
- Role-based user management within workspaces
- View compute usage from the Administration menu
- Connections to remote data sources
- Connection credentials that are personal or shared
- Sample assets and projects

For more information about the service platform and its capabilities, see:

- [Overview of IBM Software Hub](https://www.ibm.com/docs/en/software-hub/5.2.x?topic=overview){: external}

- [Documentation for Cloud Pak for Data as a Service](https://dataplatform.cloud.ibm.com/docs/content/wsj/getting-started/welcome-main.html?context=wxbi&audience=wdp){: external}

{{site.data.keyword.wxbia_full_notm}} on IBM Software Hub also uses IBM watsonx.data intelligence, a core platform service, to import and enrich metadata in watsonx BI. 

IBM watsonx.data intelligence provides ready-to-use vocabularies that help you quickly deploy data governance and analytics frameworks. It also uses generative AI to enhance technical metadata with additional context, labels, and descriptions.

### Service platform features
{: #service_platform_features}

You can access the following platform features from the **Navigation Menu** in {{site.data.keyword.wxbia_short}}.

#### Projects
{: #projects_service}

Core services on the platform are organized as a set of collaborative workspaces, called **Projects**, where you can work with your team or organization.

Each project has a set of members with roles that provide permissions to perform actions.

Users work with assets, which are the items in the project that contain metadata about data or data analysis.

In {{site.data.keyword.wxbia_short}}, to add the data that you want to ask questions about, you first need to create a project.

You can then create metrics. Watsonx BI uses metrics and enriched metadata to answer your questions.

#### Catalogs
{: #catalogs_metric}

The **Metrics catalog** is a centralized repository of published metrics, their metric definition details, and related visualizations. It provides a single source of truth for published metrics that are used across the organization.

Data analysts can publish metrics to the **Metrics catalog** and assign them to Analytics consumers.

As an Analytics consumer, you can browse the **Metrics catalog** to view the metrics that are available to you. Select ametric to view metric details and related visualizations. You can ask a question about a specific metric directly from the **Metrics catalog**.

You can also add metrics to your **Key metrics** panel from the **Metrics catalog** to monitor changes in your data.

#### Governance
{: #governance_features}

You can use the watsonx.data intelligence governance framework to apply business context to your data during metadata enrichment if:

- You use {{site.data.keyword.wxbia_short_cap}} on IBM Software Hub 
- You have an instance of watsonx.data intelligence provisioned in your IBM Cloud account

Watsonx.data intelligence is optional on watsonx BI as a Service and is not required for metadata enrichment. Watsonx BI has its own native enrichment, which does not rely on goverance to add business context to data.
{: note}

You can customize the existing governance framework in {{site.data.keyword.wxbia_short}} to meet your business context needs by implementing the following governance artifacts.

- **Categories** - Use categories to organize governance artifacts in a hierarchical structure similar to folders. You can use category roles to define ownership of artifacts, control their authoring, and restrict their visibility.

- **Business terms** - Use business terms to implement a common enterprise vocabulary to describe the meaning of data. You create business terms to help ensure clarity and compatibility among departments, projects, or products. Business terms are the core of your governance framework and typically form the bulk of your governance artifacts.

- **Data classes** - Data classes classify data based on the structure, format, and range of values of the data. You can create relationships with business terms to link data format with business meaning.

- **Classifications** - Classifications describe specific characteristics of the meaning of data. Predefined classifications describe the sensitivity of the data. You can create classifications to describe other characteristics of data or other governance items.

- **Reference data sets** - Reference data sets define standard values for specific types of data to classify data and measure consistency. They act as lookup tables that map codes and values. You can include a reference data set in the definition of a data class as part of the data matching criteria.
