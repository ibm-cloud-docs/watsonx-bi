---
copyright:
  years: 2025, 2026
lastupdated: "2026-07-10"

keywords: choose llm, large language model, foundation model, AI model
subcollection: watsonx-bi



---

{{site.data.keyword.attribute-definition-list}}


# Understanding the large language model in your account
{: #choose_llm_account}

{{site.data.keyword.wxbia_full}} uses a large language model (LLM) or foundation model to power conversations and generate insights from your business data. {: #shortdesc}

Administrators can view the model configuration on the **Configuration and settings > Model settings** page.

In watsonx BI as a Service, the model is OpenAI gpt-oss-120b with [Chain of thought](/docs/watsonx-bi?topic=watsonx-bi-choose_llm). In Software Hub, the available model depends on your version and administrators can select a model at any time on the **Configuration and settings > Model settings** page.
{: note}

The LLM responds to your BI questions by analyzing your input, identifying intent, and aligning it with your business data (such as column names, measures, or filters). It then generates the appropriate query to retrieve relevant information.

Using the returned data, the LLM produces a text-based answer, a visualization, or both. You can view each step of this process in the **AI steps** by clicking **Show AI steps** in the response.

The LLM also evaluates key metrics and helps surface changes in your business data. When you select a metric from the **Key metrics** panel, the AI can summarize and explain what changed and why it might be important.

The name of the model used to generate each response appears in the **AI** label and within **AI steps** during conversations.

{{site.data.keyword.wxbia_short_cap}} uses models that are hosted in IBM watsonx.ai and does not use your data to train the models.
{: note}

## Supported LLMs
{: #available_llms}

| LLMs | Available in {{site.data.keyword.wxbia_short}}| 
|-------|---------|
|[IBM Granite-3-8b-instruct](https://www.ibm.com/docs/watsonx/w-and-w/2.2.0?topic=models-granite-30-8b-instruct-model-card){: external} | Software Hub 5.2.0 and later versions |
|[OpenAI gpt-oss-120b](https://www.ibm.com/docs/en/watsonx/saas?topic=models-third-party-foundation#gpt-oss){: external} and IBM Granite-3-8b-instruct| Software Hub 5.2.2 and later versions|
|OpenAI gpt-oss-120b with [Chain of thought](/docs/watsonx-bi?topic=watsonx-bi-choose_llm)| As a Service|
{: caption="Supported LLMs" caption-side="bottom"}


## How the model affects conversations 
{: #model_selection}

While {{site.data.keyword.wxbia_short}} uses LLMs for various tasks, this feature specifically controls which models are used for SQL generation. The following table lists the supported LLMs and their capabilities.

IBM Granite-3-8b-instruct [Software]{: tag-blue} 

:   When you select the Granite model, it is used for all language model tasks, including SQL generation. 
  
:   Use Granite-3-8b-instruct to work with simple BI queries, such as basic data retrieval and summarization.

OpenAI gpt-oss-120b and IBM Granite-3-8b-instruct [Software]{: tag-blue} 

:   When you select the gpt-oss-120b and Granite combination, gpt-oss-120b is used specifically for SQL generation tasks, while Granite continues to be used for all other language model tasks.

:   Use this combination for advanced, configurable reasoning in complex BI queries.

OpenAI gpt-oss-120b with Chain of thought [Cloud]{: tag-blue}  

:   Chain of thought (CoT) with OpenAI gpt-oss-120b provides reasoning behind each response by breaking down complex questions into smaller steps. In this combination, OpenAI gpt-oss-120b is used for SQL generation tasks and all other language model tasks.

:   For more information, see [Chain of thought reasoning](/docs/watsonx-bi?topic=watsonx-bi-choose_llm){: external}.


## Changing the LLM 
{: #change_llm}

As an Administrator, you can change the LLM in watsonx BI on IBM Software Hub from **Navigation menu > Configuration and settings**.

When you change the model, the change applies at the account level and to new conversations or queries. This means that the change applies to everyone that is a part of the account with access to {{site.data.keyword.wxbia_short}}.

Users can see the updated LLM name in the AI icon in **Conversations**. Additionally, users can see the model that is being used in the query generation step under **AI steps** when they ask their next question or start a new conversation.

## Related links
{: #related_choose_llm}

- [Use of AI in conversations](/docs/watsonx-bi?topic=watsonx-bi-explainability){: external}

- [Steps AI takes to respond](/docs/watsonx-bi?topic=watsonx-bi-steps_ai){: external}

  
