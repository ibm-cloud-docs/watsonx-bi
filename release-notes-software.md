---

copyright:
  years: 2025
lastupdated: "2026-04-23"

keywords: watsonx BI, release notes, what's new

subcollection: watsonx-bi

content-type: release-note

---



{{site.data.keyword.attribute-definition-list}}

# Release notes for watsonx BI on IBM Software Hub 
{: #my-service-relnotes}

Use these release notes to learn about the latest updates to watsonx BI that are grouped by date. Release notes are available for a minimum of three years.
{: #shortdesc}

## 22 April 2026
{: #subcollection-apr2226}
{: release-note}

The following fixes are included in watsonx BI on IBM Software Hub 5.3.1 patch 3.

**Security issues fixed in this patch**

This patch addresses the following Common Vulnerabilities and Exposures (CVE):

CVE-2026-4867, CVE-2026-22695, CVE-2026-22801, CVE-2026-25646, CVE-2026-33036, CVE-2026-33151, CVE-2026-33671, CVE-2026-33672, CVE-2026-33750, CVE-2026-33891, 

CVE-2026-33894, CVE-2026-33895, CVE-2026-33896

## 11 April 2026
{: #subcollection-apr0826}
{: release-note}

The following fixes are included in watsonx BI on IBM Software Hub 5.3.1 patch 2.

**Security issues fixed in this patch**

This patch addresses the following Common Vulnerabilities and Exposures (CVE):

CVE-2026-0540, CVE-2026-21932, CVE-2026-21933, CVE-2026-24842, CVE-2026-25639, CVE-2026-27942

CVE-2025-9086, CVE-2025-13601, CVE-2025-15467, CVE-2025-15599, CVE-2025-23419, CVE-2025-27821, CVE-2025-67735, CVE-2025-69419

CVE-2012-5783



## 25 March 2026
{: #subcollection-mar2526}
{: release-note}

The following new features and fixes are included in watsonx BI on IBM Software Hub 5.3.1 patch 1.

For more information about patches on IBM Software hub, see [Available patches on IBM Software Hub Version 5.3.1](https://www.ibm.com/docs/en/software-hub/5.3.x?topic=overview-available-patches-software-hub-version-531){: external}

**Security issues fixed in this patch**

This patch addresses the following Common Vulnerabilities and Exposures (CVE):

CVE-2026-25896

CVE-2025-15467

**New features in this patch**

This patch includes the following new features:

**OpenAI gpt-oss-120b large language model now available for all language-model-driven functions**

:   The OpenAI gpt-oss-120b large language model (LLM) is now available for SQL generation tasks and all other language‑model–driven functions within watsonx BI. If you are an Administrator, you can choose this LLM by going to **Configuration and settings > Model settings**.

:   The OpenAI gpt-oss-120b model provides advanced question interpretation, stronger semantic understanding, and higher accuracy across a wide range of queries.

:   For more information about the OpenAI gpt-oss-120b model, see [Configuring additional models in watsonx BI](https://www.ibm.com/docs/en/software-hub/5.3.x?topic=administering-configuring-additional-models){: external}.

**Conversation scopes now have descriptions**

:   The conversation scope list next to the input box in **Conversations** now includes descriptions (if applicable) for each item, such as projects, the **Metrics catalog**, and any files that you have uploaded.

:   You can now also open and preview any of these items in a new tab directly from the conversation scope, such as:

:  - Launching a project opens the data platform project view, including its assets.

:  - Launching an uploaded file opens the file view in a new tab for quick review.

:   These enhancements make it easier to choose the data that you want to focus your conversation on.

**Download responses and related data from a conversation**
:   You can now download responses and their associated components from a conversation, making it easy to save and share insights. Available download options include:

:  - Text response – The generated answer in .txt format

:  - Visualizations – Charts downloaded in .png format.

:  - Tabular data – Data tables downloaded in .csv format.

:  - Diagnostic information – Details such as AI steps, generated SQL, and response ID in .json format (available to Data analysts only).

:   For more information, see [Downloading responses and data from a conversation](/docs/watsonx-bi?topic=watsonx-bi-download_response){: external}.

**Provide custom instructions and context to guide AI behavior**

:   A new **AI instructions and context** field is available in the modelling experience, which you can use to add business logic and rules that the large language model (LLM) follows when interpreting and generating responses that are related to a metric. Use AI instructions in scenarios where consistent interpretation depends on rules, such as when:

:  - Your dataset uses business‑specific terminology that differs from column names

:  - You use standard calculation methods or rules, such as weighted averages or variance formulas

:  - Certain columns must always appear together for context

:  - You rely on default filters or display preferences

:  - You need to enforce organizational reporting standards, such as fiscal or seasonal time logic

:   For more information, see [Adding instructions and context for AI](/docs/watsonx-bi?topic=watsonx-bi-instructions_ai){: external}.


**Cognos Analytics data modules now supported as a data source and improved connection process**

:   You can now use Cognos Analytics data modules as a data source in watsonx BI. With this enhancement, you can create semantic data models metrics by using your existing data modules. You can use data modules that use uploaded files and database tables as data source. You cannot use data modules that use FM packages as a source.

:   The experience for connecting to Cognos Analytics and importing a package is also improved. You can now:

:   - Create and test a Cognos Analytics connection directly during data selection

:   - Choose either an FM package or a data module from your Cognos environment

:   - Automatically populate your semantic data model with Cognos metadata and governance rules

:   In addition, improved sync behavior helps semantic data models stay aligned with source changes. Updates to FM packages are applied automatically, while data modules prompt you to resync whenever changes are detected in the underlying source.

:   For more information, refer to [IBM Cognos® Analytics](/docs/watsonx-bi?topic=watsonx-bi-cognos){: external}.

**Apply user filters for row-level security**

:   User filters are now available to help protect sensitive data in metrics. Administrators and Data analysts can define conditions on a metric definition in the semantic data model to ensure that users see only the data they have permissions to access. When a user views a metric, the values are calculated only from the rows they’re allowed to see, based on the filters applied.

:   For more information, see [Manage data access with User filters](/docs/watsonx-bi?topic=watsonx-bi-user_filters){: external}.

## 15 December 2025
{: #subcollection-dec1525}
{: release-note}

Manage new roles for watsonx BI users through IBM Software Hub Access control

:   As a watsonx BI user, you can now use IBM Software Hub Access control to assign roles to your team that are specific to watsonx BI. You can assign the following roles to users or groups: Business Intelligence Administrator, Business Intelligence Analyst, or Business Intelligence Consumer.

:   For more information, see [Roles and permissions for watsonx BI](https://www.ibm.com/docs/en/SSNFH6_5.3.x?topic=administering-roles-permissions){: external}.

Configure flat file service to upload files to watsonx BI

:   You can configure flat file service to [upload files](/docs/watsonx-bi?topic=watsonx-bi-upload){: external} and use them as a source of data in **Conversations**. 

:   For more information, see [Configuring flat file service](https://www.ibm.com/docs/en/SSNFH6_5.3.x?topic=setup-configuring-flat-file-service){: external}.

Integrate with IBM watsonx.data™ Premium

:   You can now easily access watsonx BI from a tile in watsonx.data Premium. By combining watsonx.data Premium and watsonx BI, you can use business intelligence tools to get deeper insights into your structured and unstructured data. 

:   For more information, see [IBM watsonx.data Premium](/docs/watsonx-bi?topic=watsonx-bi-wxdpremium){: external}.

## 30 October 2025
{: #subcollection-oct3025}
{: release-note}

Integrate with the IBM Cognos Analytics FM package

:   You can now import metadata from relational FM packages into for use in conversations. By integrating Cognos Analytics with watsonx BI, the rich metadata from Cognos Analytics becomes accessible to AI, making it easier for you to get insights from your data. 

:   This feature is a Technology Preview feature. Technology Preview offers customers early access to product features, allowing them to explore functionality and share feedback during development. These features are provided for evaluation purposes and might not be fully functional or complete.
{: important}

:   For more information, see [IBM Cognos Analytics](/docs/watsonx-bi?topic=watsonx-bi-cognos){: external}.

Import and export projects

:   Get started quickly by importing projects to watsonx BI to create projects that already contain data and metrics. To import a project, you must have a local .zip file of a previously exported project.

:   For more information, see [Importing a project](/docs/watsonx-bi?topic=watsonx-bi-import_project){: external}.

Use sample data to explore watsonx BI

:   You can now use sample data in watsonx BI. Use the **Customer experience** sample data to explore the natural language interface, the types of questions you can ask, the structure of a metric definition, and the ways that sample data is modeled and optimized for AI.

:   For more information, see [Installing samples in watsonx BI](/docs/watsonx-bi?topic=watsonx-bi-using_samples){: external}.

Choose the large language model (LLM)

:   If you have the watsonx BI administrator role, you can now choose which LLM to use in your organization. You can choose from the following options:

:   - A combination of the new OpenAI gpt-oss-120b model and IBM Granite-3-8b-instruct - Recommended for complex, multi-step queries

:   - IBM Granite 3-8b-instruct - Recommended for working with simple queries, such as data retrieval and summarization

:   For more information, see [Choosing the large language model (LLM)](/docs/watsonx-bi?topic=watsonx-bi-choose_llm){: external}.

## 27 August 2025
{: #subcollection-aug2725}
{: release-note}

New way to navigate to watsonx BI

:   Watsonx BI is now part of a new experience called Business Intelligence. You can now launch watsonx BI by selecting Business Intelligence in the IBM Software Hub experience switcher menu. The Navigation Menu now displays menu options that are specific to watsonx BI.


## 30 June 2025
{: #subcollection-jun3025}
{: release-note}

Introducing watsonx BI on IBM Software Hub 5.2.0

:   IBM watsonx™ BI is a new service that is now available on IBM Software Hub 5.2.0.

:   Watsonx BI is a generative AI-powered business intelligence partner that uses natural language to analyze complex data, providing personalized insights and data-driven recommendations that are actionable and easy to understand. It works with the tools you already use and delivers intelligent, transparent answers tailored to your needs.

:   Use watsonx BI to:

:   - Get faster insights - Ask questions using natural language and receive answers through a simple, intuitive interface.

:   - Understand data more deeply - Uncover trends, understand causes, predict future outcomes and gain actionable strategies.

:   - Act with greater confidence -  Governed data and artificial intelligence (AI) ensure trusted models, transparency for all AI workflows (powered by IBM watsonx™), and security 
with insights that derive from a single source of truth via a centralized **Metrics catalog**. 

:   - Perform advanced data visualization interaction - Customize the look and feel of data visualizations with conversational and graphical interactions.

:   - Semantic automation - Automate data profiling, business term matching, and data modeling.

### Quick links
{: #quick_links_rel}

- [Installing watsonx BI](https://www.ibm.com/docs/SSNFH6_5.2.x/svc-bi/wxbi-install.html)

- [About the user interface](/docs/watsonx-bi?topic=watsonx-bi-user_interface)

- [Using conversations to get insights](/docs/watsonx-bi?topic=watsonx-bi-conv_overview)

- [Creating metrics for data analysis](/docs/watsonx-bi?topic=watsonx-bi-overview_metrics)
