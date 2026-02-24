---
copyright:
  years: 2025
lastupdated: "2026-02-23"

keywords: choose llm, large language model
subcollection: watsonx-bi



---

{{site.data.keyword.attribute-definition-list}}


# Selecting the large language model for your account
{: #choose_llm_account}

At the time of setting up {{site.data.keyword.wxbia_full}}, Administrators can choose the large language model (LLM) that will be used in {{site.data.keyword.wxbia_short}} conversations for users in their organization. {: #shortdesc}

Administrators can update this selection at any time from the **Configuration and settings > Model settings** page. 

The selected LLM is used to respond to your BI questions.  It analyzes your input, identifies the key intent, and aligns it with your business data (such as column names, measures, or filters). Based on this understanding, the LLM generates the appropriate query to retrieve the relevant information.

Using the returned data, the LLM produces a text-based answer, a visualization, or both. You can view each step of this process in the **AI steps** by clicking **Show AI steps** in the response.

The LLM also evaluates key metrics and helps surface changes in your business data. When you select a metric from the **Key metrics** panel, the AI can summarize and explain what has changed and why it might be important.

The name of the LLM used to generate each response appears in the **AI** label and within **AI steps** during conversations.

{{site.data.keyword.wxbia_short_cap}} uses LLMs that are hosted in IBM watsonx.ai and does not use your data to train the models.
{: note}

## Available LLMs
{: #available_llms}

As an Administrator, you can choose from the following LLMs:

| LLM | Available in watsonx BI| 
|-------|---------|
|[IBM Granite-3-8b-instruct](https://www.ibm.com/docs/watsonx/w-and-w/2.2.0?topic=models-granite-30-8b-instruct-model-card){: external} | Software Hub 5.2.0 and later versions |

|[OpenAI gpt-oss-120b](https://www.ibm.com/docs/en/watsonx/saas?topic=models-third-party-foundation#gpt-oss){: external} and IBM Granite-3-8b-instruct| As a Service, Software Hub 5.2.2 and later versions|

|OpenAI gpt-oss-120b| As a Service|
|[Meta Llama 4](https://www.llama.com/docs/model-cards-and-prompt-formats/llama4/){: external} and IBM Granite-3-8b-instruct | As a Service|

|OpenAI gpt-oss-120b and IBM Granite-3-8b-instruct with [Chain of Thought](/docs/watsonx-bi?topic=watsonx-bi-choose_llm)[Preview]{: tag-teal}| As a Service|


Watsonx BI on Software Hub 5.2.1 and previous versions use IBM Granite-3-8b-instruct to respond to your questions. 
{: note}

## How model selection affects conversations
{: #model_selection}

While watsonx BI utilizes large language models for various tasks, this feature specifically controls which LLMs are used for SQL generation. You can choose the LLM based on your specific requirements for SQL generation performance and accuracy.

* **IBM Granite-3-8b-instruct**

  When you select only the Granite model, it is used for all language model tasks, including SQL generation. 
  
  Choose Granite-3-8b-instruct to work with simple BI queries, such as basic data retrieval and summarization.



* **OpenAI gpt-oss-120b and IBM Granite-3-8b-instruct**

  When you select the gpt-oss-120b and Granite combination, gpt-oss-120b is used specifically for SQL generation tasks, while Granite continues to be used for all other language model tasks.

  Choose this combination for advanced, configurable reasoning in complex BI queries.

* **OpenAI gpt-oss-120b**

  The gpt-oss-120b is used for SQL generation tasks and for all other language model tasks.

  Choose this option for advanced question interpretation and higher accuracy.

* **Meta Llama 4 and IBM Granite-3-8b-instruct**

  When you select Meta Llama 4 and Granite, Meta Llama 4 is used specifically for SQL generation tasks, while Granite continues to be used for all other language model tasks.

  Choose Meta Llama 4 and Granite for complex, multi-step BI queries. 

* **OpenAI gpt-oss-120b and IBM Granite-3-8b-instruct with Chain of Thought** [Preview]{: tag-teal}

  Chain of Thought with OpenAI gpt-oss-120b and Granite provides reasoning behind each response by breaking down complex questions into smaller steps. 
  
  OpenAI gpt-oss-120b is used specifically for SQL generation tasks, while Granite is used for all other language model tasks.

  Choose gpt-oss-120b and Granite with Chain of Thought to view reasoning for complex, multi-part BI queries.
  
  Chain of Thought was previously supported by Meta Llama 4 and Granite. This option is being discontinued. Administrators must reselect Chain of Thought with the new gpt‑oss‑120b model in **Configuration and settings > Model settings** to continue receiving accurate and supported responses. Users who previously enabled Chain of Thought with the Llama model will continue to receive responses for now. However, once Llama is fully discontinued, answer accuracy might be impacted until the model selection is updated.
  {: important}

  For more information, see [Chain of Thought reasoning](/docs/watsonx-bi?topic=watsonx-bi-choose_llm){: external}.


## Changing the large language model
{: #change_llm}

As an Administrator, you can change the LLM from **Navigation menu > Configuration and settings**. 

When you change the LLM, the change applies at the account level and to new conversations or queries. This means that the change applies to everyone that is a part of the account that has access to {{site.data.keyword.wxbia_short}}.

Users can see the updated LLM name in the AI icon in **Conversations**. Additionally, users can see the LLM being used in the query generation step under **AI steps** when they ask their next question or start a new conversation.

## Related links
{: #related_choose_llm}

- [Use of AI in conversations](/docs/watsonx-bi?topic=watsonx-bi-explainability){: external}

- [Steps AI takes to respond](/docs/watsonx-bi?topic=watsonx-bi-steps_ai){: external}

  
