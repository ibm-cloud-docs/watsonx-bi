---

copyright:
  years: 2025
lastupdated: "2026-02-06"

keywords: watsonx BI, release notes, what's new, watsonx BI as a Service

subcollection: watsonx-bi

content-type: release-note

---






{{site.data.keyword.attribute-definition-list}}

# Release notes for {{site.data.keyword.wxbia_short}} as a Service (on IBM Cloud)
{: #my-service-relnotes_saas}

Use these release notes to learn about the latest updates to {{site.data.keyword.wxbia_full}} that are grouped by date. Release notes are available for a minimum of three years.
{: shortdesc}

## 5 February 2026
{: #subcollection-feb526}
{: release-note}


Model update for Chain of Thought reasoning

:   Chain of Thought reasoning will now use **OpenAI gpt‑oss‑120b** instead of **Meta Llama 4** large language model (LLM). This update ensures improved quality and consistency in Chain of Thought reasoning.

:   Administrators must reselect Chain of Thought with the new gpt‑oss‑120b model in **Configuration and settings > Model settings** to continue receiving accurate and supported responses.

:   Users who previously enabled Chain of Thought with the Llama model continue to receive responses for now. However, after Llama is fully discontinued, answer accuracy might be impacted until the model selection is updated.

:   If Administrators do not switch to Chain of Thought with GPT, users will automatically be moved to an LLM that does not support Chain of Thought when the current model is discontinued.

Provide custom instructions and context to guide AI behavior

:   A new **AI instructions and context** field is available in the modelling experience, which allows you to add business logic and rules that the large language model (LLM) follows when interpreting and generating responses that are related to a metric. 

:   Use AI instructions in scenarios where consistent interpretation depends on rules, such as when:

:    - Your dataset uses business‑specific terminology that differs from column names

:    - You use standard calculation methods or rules, such as weighted averages or variance formulas

:    - Certain columns must always appear together for context

:   - You rely on default filters or display preferences

:   - You need to enforce organizational reporting standards, such as fiscal or seasonal time logic

:   For more information, see [Adding instructions and context for AI](/docs/watsonx-bi?topic=watsonx-bi-instructions_ai){: external}.


Download responses and related data from a conversation

:   You can now download responses and their associated components from a conversation, making it easy to save and share insights. Available download options include:

:    - Text response – The generated answer in .txt format

:    - Visualizations – Charts downloaded in .png format.

:    - Tabular data – Data tables downloaded in .csv format.

:    - Diagnostic information – Details such as AI steps, generated SQL, and response ID in .json format (available to Data analysts only). 

:   For more information, see [Downloading responses and data from a conversation](/docs/watsonx-bi?topic=watsonx-bi-download_response){: external}. 


Expand and collapse the Conversations panel

:   You can now expand or collapse the **Conversations** panel to create more space for your active chat. Previously, this panel was fixed and could not be collapsed.

Conversation scope list improved with descriptions

:   The conversation scope list next to the input box in **Conversations** now includes descriptions (if applicable) for each item, such as projects, the **Metrics catalog**, and any files that you have uploaded. 

:   You can now also open and preview any of these items in a new tab directly from the conversation scope. For example:

:    - Launching a project opens the data platform project view, including its assets.

:    - Launching an uploaded file opens the file view in a new tab for quick review.

:   These enhancements make it easier to choose the data that you want to focus your conversation on. 

Improved look and feel of the welcome message

:   The welcome message in **Conversations** now has an improved look and feel. You can still click any of the suggested questions to start exploring your data, just like before.


## 21 January 2026
{: #subcollection-jan2226}
{: release-note}

OpenAI gpt-oss-120b large language model now available as an independent model option

:   The OpenAI gpt‑oss‑120b large language model (LLM) is now available as a stand-alone option in watsonx BI as a Service. Administrators can choose this LLM on the **Configuration and settings > Model settings**. 

:   This LLM is used for SQL generation tasks and all other language‑model–driven functions within watsonx BI.

:   Selecting this LLM provides advanced question interpretation, stronger semantic understanding, and higher accuracy across a wide range of queries.


## 15 January 2026
{: #subcollection-jan1526}
{: release-note}

IBM watsonx.data intelligence is required for watsonx BI as a Service

:   IBM watsonx BI as a Service requires an IBM watsonx.data intelligence plan to be active in the IBM Cloud account. 

:   As part of an initial, limited‑time introductory promotion, watsonx.data intelligence was included with watsonx BI; this promotion has since expired, and clients are now required to explicitly select and activate a watsonx.data intelligence plan. IBM Cloud accounts without an active watsonx.data intelligence plan will not be able to provision watsonx BI.

:   Cloud account owners must have an active watsonx.data intelligence plan or purchase a watsonx.data intelligence plan and activate it. Cloud account owners can choose from any watsonx.data intelligence plan, including Trial, Essentials, Standard, or Premium. 

:   For existing watsonx BI users, the service checks whether a watsonx.data intelligence plan is available. If one is not found, users are guided to [provision a plan](/docs/watsonx-bi?topic=watsonx-bi-getting-started){: external} or asked to contact the Cloud account owner for assistance before continuing to use watsonx BI.

:   To check whether the Cloud account has an active watsonx.data intelligence plan:

:    1. Log into the [IBM Cloud account](https://cloud.ibm.com/login). 

:    2. Click **Resource list** and expand the **Analytics** section and check if watsonx.data intelligence is listed as an existing resource. 


## 3 December 2025
{: #subcollection-dec325}
{: release-note}

Chain of Thought reasoning

:   Chain of Thought reasoning is now available with Meta Llama 4 and IBM Granite-3-8b-instruct. Available as a Technology Preview feature in watsonx BI as a Service, it delivers step-by-step reasoning for complex or multi-part questions, providing structured answers and visibility into how queries are built.

:   Technology Preview offers customers early access to product features, allowing them to explore functionality and share feedback during development. These features are provided for evaluation purposes and might not be fully functional or complete.
{: important} 

:   You can view reasoning steps, chosen data sources, intermediate calculations, and generated SQL, helping you understand the AI’s decision-making process.

:   Administrators can choose Meta Llama 4 and IBM Granite-3-8b-instruct with Chain of Thought from **Configuration and settings > Model settings** page.

:   For more information, see [Chain of Thought reasoning](/docs/watsonx-bi?topic=watsonx-bi-choose_llm){: external}. 

IBM watsonx BI remote Model Context Protocol (MCP) server now available for queries

:   You can now use the IBM watsonx BI remote MCP server, a Model Context Protocol (MCP) compliant service that seamlessly connects AI agents with data in watsonx BI, enabling intelligent data and insight retrieval. 

:   For more details about remote MCP server, see [IBM watsonx BI remote Model Context Protocol (MCP) server](/docs/watsonx-bi?topic=watsonx-bi-remote_mcp){: external}.


## 14 August 2025
{: #subcollection-aug1425}
{: release-note}

Introducing {{site.data.keyword.wxbia_short}} as a Service on IBM Cloud

:   {{site.data.keyword.wxbia_full}} is a new service that is now available on IBM Cloud.

:   {{site.data.keyword.wxbia_short_cap}} is a generative AI-powered business intelligence partner that uses natural language to analyze complex data, providing personalized insights and data-driven recommendations that are actionable and easy to understand. It works with the tools you already use and delivers intelligent, transparent answers tailored to your needs.

:   Use {{site.data.keyword.wxbia_short}} to:

:    **Get faster insights**

:    Ask questions using natural language and receive answers through a simple, intuitive interface.

:    **Understand data more deeply**

:    Uncover trends, understand causes, predict future outcomes, and gain actionable strategies.

:    **Act with greater confidence**

:    Governed data and artificial intelligence (AI) help ensure trusted models, transparency for all AI workflows (powered by IBM watsonx™), and security with insights that derive from a single source of truth through a centralized **Metrics catalog**. 

:    **Perform advanced data visualization interaction**

:    Customize the look and feel of data visualizations with conversational and graphical interactions.

:    **Semantic automation**

:    Automate data profiling, business term matching, and data modeling.
