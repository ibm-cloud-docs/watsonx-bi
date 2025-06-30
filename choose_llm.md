---
copyright:
  years: 2025
lastupdated: "2024-04-26"

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

At the time of setting up watsonx BI, Administrators can choose the large language model (LLM) that will be used in watsonx BI conversations for users in their organization. {: #shortdesc}

As an Administrator, you can choose between the following:

- A combination of [Meta Llama 4](https://www.llama.com/docs/model-cards-and-prompt-formats/llama4/){: external} and IBM Granite-3-8b-instruct (Recommended)

- [IBM Granite-3-8b-instruct](https://www.ibm.com/docs/watsonx/w-and-w/2.2.0?topic=models-granite-30-8b-instruct-model-card){: external}

To work with simple BI queries, such as basic data retrieval and summarization, choose IBM Granite-3-8b-instruct. 

For complex, multi-step BI queries, choose the Meta Llama 4 and IBM Granite-3-8b-instruct option. 

## Changing the large language model
{: #change_llm}

Administrators change the LLM from **Navigation menu > Configuration and settings**. 

When you change the LLM, the change applies at the account level and to new conversations or queries. This means that the change applies to everyone that is a part of the Cloud account that has access to watsonx BI.

Users in the organization will be notified in the user interface when a change is made. Additionally, users can see the updated LLM name in the AI icon and the query generation step under **Steps taken by AI** when they ask their next question or start a new conversation.
