---
copyright:
  years: 2024
lastupdated: "2024-04-26"

keywords:
subcollection: watsonx-bi



---

{{site.data.keyword.attribute-definition-list}}

# Use of AI in conversations 
{: #explainability}

The **AI** label in the user interface gives an overview of how AI works in **Conversations**. {{site.data.keyword.wxbia_full}} uses large language models (LLM) to answer your questions and provide recommendations, insights, and summaries for your governed business data. {: #shortdesc}

Governed business data is data that has gone through different processes, policies, and standards to define the availability, quality, and security of the data. These processes and standards determine the intended use of the organization's data, data owners, and data security measures.
{: note}

## How AI generates responses 
{: #ai_queries}

To respond to your BI question, the LLM analyzes and helps interpret your input. It can then match the interpreted input to your business data (such as column names, measures, or filters) and generates a query to retrieve the matched information to respond to your input. 

The LLM generates a text-based response, visualization, or both based on the matched information to respond to your question. You can see each of these steps under **AI steps**. 

The LLM also monitors key metrics and helps to identify changes in the business data. When you click a metric in the **Key metrics** panel to open it, notice that the AI can summarize and help explain the identified changes in your metrics.

The selected LLM name that was used to respond to your queries displays in the **AI** label and **AI steps** in conversations.

{{site.data.keyword.wxbia_short_cap}} uses large language models (LLMs) that are hosted in IBM watsonx.ai and does not use your data to train the models.
{: note}

## Choosing the LLM
{: #cyom}

At the time of setting up {{site.data.keyword.wxbia_short}} as a Service, Administrators can choose the LLM that is used in conversations for users in their organization. 

Administrators can also change the LLM from **Configuration and settings > Model settings**. 

The ability to choose the large language model is not available in {{site.data.keyword.wxbia_short}} on IBM Software Hub 5.2.1 and prior versions. Watsonx BI on Software Hub 5.2.1 and previous versions use [IBM Granite-3-8b-instruct](https://www.ibm.com/docs/watsonx/w-and-w/2.2.0?topic=models-granite-30-8b-instruct-model-card){: external} to respond to your questions. 
{: important}

The following LLMs are available: 

- Combination of [OpenAI gpt-oss-120b](https://www.ibm.com/docs/en/watsonx/saas?topic=models-third-party-foundation#gpt-oss){: external} and IBM Granite-3-8b-instruct

- Combination of [Meta Llama 4](https://www.ibm.com/docs/watsonx/w-and-w/latest?topic=models-third-party-foundation#llama-4){: external} and IBM Granite-3-8b-instruct 

- [IBM Granite-3-8b-instruct](https://www.ibm.com/docs/watsonx/w-and-w/latest?topic=models-granite-30-8b-instruct-model-card){: external}

The LLM change applies at the account level and to new conversations or queries. This means that the change applies to everyone that is a part of the account that has access to {{site.data.keyword.wxbia_short}}.

The updated LLM name appears in the AI icon and the query generation step under **AI steps** in **Conversations**.  

