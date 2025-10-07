---
copyright:
  years: 2025
lastupdated: "2025-10-07"

keywords: choose llm, large language model
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

# Choosing the large language model (LLM) 
{: #choose_llm}

At the time of setting up {{site.data.keyword.wxbia_full}}, Administrators can choose the large language model (LLM) that will be used in {{site.data.keyword.wxbia_short}} conversations for users in their organization. {: #shortdesc}

The ability to choose the large language model is not available in {{site.data.keyword.wxbia_short}} on IBM Software Hub 5.2.x. Watsonx BI on Software Hub 5.2.x uses [IBM Granite-3-8b-instruct](https://www.ibm.com/docs/watsonx/w-and-w/2.2.0?topic=models-granite-30-8b-instruct-model-card){: external} to respond to your questions. 
{: note}

As an Administrator, you can choose between the following:

- A combination of [OpenAI gpt-oss-120b](https://www.ibm.com/docs/en/watsonx/saas?topic=models-third-party-foundation#gpt-oss){: external} and IBM Granite-3-8b-instruct

  Choose the OpenAI gpt-oss-120b and IBM Granite-3-8b-instruct option for advanced, configurable reasoning in complex BI queries.

- A combination of [Meta Llama 4](https://www.llama.com/docs/model-cards-and-prompt-formats/llama4/){: external} and IBM Granite-3-8b-instruct (Recommended)

  Choose the Meta Llama 4 and IBM Granite-3-8b-instruct option for complex, multi-step BI queries. 

- [IBM Granite-3-8b-instruct](https://www.ibm.com/docs/watsonx/w-and-w/2.2.0?topic=models-granite-30-8b-instruct-model-card){: external}

  Choose IBM Granite-3-8b-instruct to work with simple BI queries, such as basic data retrieval and summarization.

## Changing the large language model
{: #change_llm}

Administrators change the LLM from **Navigation menu > Configuration and settings**. 

When you change the LLM, the change applies at the account level and to new conversations or queries. This means that the change applies to everyone that is a part of the account that has access to {{site.data.keyword.wxbia_short}}.

Users can see the updated LLM name in the AI icon in **Conversations**. Additionally, users can see the LLM being used in the query generation step under **Steps taken by AI** when they ask their next question or start a new conversation.
