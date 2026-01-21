---

copyright:
  years: 2025
lastupdated: "2026-01-21"

keywords: watsonx BI, release notes, what's new, watsonx BI as a Service

subcollection: watsonx-bi

content-type: release-note

---



{{site.data.keyword.attribute-definition-list}}

# Release notes for {{site.data.keyword.wxbia_short}} as a Service (on IBM Cloud)
{: #my-service-relnotes_saas}

Use these release notes to learn about the latest updates to {{site.data.keyword.wxbia_full}} that are grouped by date. Release notes are available for a minimum of three years.
{: shortdesc}

## 21 January 2026
{: #subcollection-jan2226}
{: release-note}

### OpenAI gpt-oss-120b large language model now available as an independent model option

The OpenAI gpt‑oss‑120b large language model (LLM) is now available as a standalone option in watsonx BI as a Service. Administrators can choose this LLM on the **Configuration and settings > Model settings**. 

This LLM is used for SQL generation tasks as well as all other language‑model–driven functions within watsonx BI.

Selecting this LLM provides advanced question interpretation, stronger semantic understanding, and higher accuracy across a wide range of queries.




## 15 January 2026
{: #subcollection-jan1526}
{: release-note}

### IBM watsonx.data intelligence required for watsonx BI as a Service
{: #data_intelligence}

IBM watsonx BI as a Service requires an IBM watsonx.data intelligence plan to be active in the IBM Cloud account. 

As part of an initial, limited‑time introductory promotion, watsonx.data intelligence was included with watsonx BI; this promotion has since expired, and clients are now required to explicitly select and activate a watsonx.data intelligence plan. IBM Cloud accounts without an active watsonx.data intelligence plan will not be able to provision watsonx BI.

Cloud account owners must have an active watsonx.data intelligence plan or purchase a watsonx.data intelligence plan and activate it. Cloud account owners can choose from any watsonx.data intelligence plan, including Trial, Essentials, Standard, or Premium. 

For existing watsonx BI users, the service checks whether a watsonx.data intelligence plan is available. If one is not found, users are guided to [provision a plan](/docs/watsonx-bi?topic=watsonx-bi-getting-started){: external} or asked to contact the Cloud account owner for assistance before continuing to use watsonx BI.

To check if the Cloud account has an active watsonx.data intelligence plan:

1. Log into the [IBM Cloud account](https://cloud.ibm.com/login). 

2. Click **Resource list** and expand the **Analytics** section and check if watsonx.data intelligence is listed as an existing resource. 


## 3 December 2025
{: #subcollection-dec325}
{: release-note}

### Chain of Thought reasoning
{: #cot}

Chain of Thought reasoning is now available with Meta Llama 4 and IBM Granite-3-8b-instruct. Available as a Technology Preview feature in watsonx BI as a Service, it delivers step-by-step reasoning for complex or multi-part questions, providing structured answers and visibility into how queries are built.

Technology Preview offers customers early access to product features, allowing them to explore functionality and share feedback during development. These features are provided for evaluation purposes and might not be fully functional or complete.
{: important} 

You can view reasoning steps, chosen data sources, intermediate calculations, and generated SQL, helping you understand the AI’s decision-making process.

Administrators can choose Meta Llama 4 and IBM Granite-3-8b-instruct with Chain of Thought from **Configuration and settings > Model settings** page.

For more information, see [Chain of Thought reasoning](/docs/watsonx-bi?topic=watsonx-bi-choose_llm){: external}. 

### IBM watsonx BI remote Model Context Protocol (MCP) server now available for queries
{: #mcp}

You can now use the IBM watsonx BI remote MCP server, a Model Context Protocol (MCP) compliant service that seamlessly connects AI agents with data in watsonx BI, enabling intelligent data and insight retrieval. 

For more details about remote MCP server, see [IBM watsonx BI remote Model Context Protocol (MCP) server](/docs/watsonx-bi?topic=watsonx-bi-remote_mcp){: external}.




## 14 August 2025
{: #subcollection-aug1425}
{: release-note}

### Introducing {{site.data.keyword.wxbia_short}} as a Service on IBM Cloud
{: #1.0.0}

{{site.data.keyword.wxbia_full}} is a new service that is now available on IBM Cloud.

{{site.data.keyword.wxbia_short_cap}} is a generative AI-powered business intelligence partner that uses natural language to analyze complex data, providing personalized insights and data-driven recommendations that are actionable and easy to understand. It works with the tools you already use and delivers intelligent, transparent answers tailored to your needs.

Use {{site.data.keyword.wxbia_short}} to:

:   **Get faster insights**

:    Ask questions using natural language and receive answers through a simple, intuitive interface.

:   **Understand data more deeply**

:   Uncover trends, understand causes, predict future outcomes and gain actionable strategies.

:   **Act with greater confidence**

:   Governed data and artificial intelligence (AI) ensure trusted models, transparency for all AI workflows (powered by IBM watsonx™), and security 
with insights that derive from a single source of truth via a centralized **Metrics catalog**. 

:   **Perform advanced data visualization interaction**

:   Customize the look and feel of data visualizations with conversational and graphical interactions.

:   **Semantic automation**

:   Automate data profiling, business term matching, and data modeling.

### Quick links
{: #quick_links_rel_saas}

- [About the user interface](/docs/watsonx-bi?topic=watsonx-bi-user_interface)

- [Using conversations to get insights](/docs/watsonx-bi?topic=watsonx-bi-conv_overview)

- [An overview of creating metrics](/docs/watsonx-bi?topic=watsonx-bi-overview_metrics)
