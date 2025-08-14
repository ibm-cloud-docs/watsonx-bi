---
copyright:
  years: 2024
lastupdated: "2024-04-26"

keywords:
subcollection: watsonx-bi



---

{{site.data.keyword.attribute-definition-list}}

# Use of AI in Conversations 
{: #explainability}

The **AI** label in the user interface gives an overview of how AI works in **Conversations**. {{site.data.keyword.wxbia_full}} uses large language models (LLM) to answer your questions and provide recommendations, insights, and summaries for your governed business data. {: #shortdesc}

Governed business data is data that has gone through different processes, policies, and standards to define the availability, quality, and security of the data. These processes and standards determine the intended use of the organization's data, data owners, and data security measures.
{: note}

To respond to your BI question, the LLM analyzes and helps interpret your input. It can then match the interpreted input to your business data (such as column names, measures, or filters) and generates a query to retrieve the matched information to respond to your input. 

The LLM generates a text-based response, visualization, or both based on the matched information to respond to your question. You can see each of these steps under **Steps taken by AI**. 

The LLM also monitors key metrics and helps to identify changes in the business data. When you click a metric in the **Key metrics** panel to open it, notice that the AI can summarize and help explain the identified changes in your metrics.

Administrators can choose the LLM that is used to answer questions. The following LLMs are available: 

Administrators can select LLMs in {{site.data.keyword.wxbia_short}} as a Service only. 
{: important}

- Combination of [Meta Llama 4](https://www.ibm.com/docs/watsonx/w-and-w/latest?topic=models-third-party-foundation#llama-4){: external} and IBM Granite-3-8b-instruct 

- [IBM Granite-3-8b-instruct](https://www.ibm.com/docs/watsonx/w-and-w/latest?topic=models-granite-30-8b-instruct-model-card){: external}

The selected LLM name displays in the **AI** label in **Conversations**. You can also view the LLM that was used to generate a query in response to your question under **Steps taken by AI** in the conversation.

When the LLM is changed by the Administrator, you receive a notification. Additionally, the updated LLM name appears in the AI label content and the query generation step under **Steps taken by AI**. 

{{site.data.keyword.wxbia_short_cap}} uses large language models (LLMs) that are hosted in IBM watsonx.ai and does not use your data to train the models.
{: note}

## Choosing the large languge model (LLM)
{: #cyom}

At the time of setting up {{site.data.keyword.wxbia_short}} as a Service, Administrators can choose the LLM that is used in conversations for users in their organization. 

As an Administrator, you can choose between the following:

- A combination of [Meta Llama 4](https://www.ibm.com/docs/watsonx/w-and-w/latest?topic=models-third-party-foundation#llama-4){: external} and IBM Granite-3-8b-instruct (Recommended)

- [IBM Granite-3-8b-instruct](https://www.ibm.com/docs/watsonx/w-and-w/latest?topic=models-granite-30-8b-instruct-model-card){: external}

The ability to choose the large language model is not available in {{site.data.keyword.wxbia_short}} on IBM Software Hub 5.2.0. Watsonx BI on Software Hub 5.2.0 uses [IBM Granite-3-8b-instruct](https://www.ibm.com/docs/watsonx/w-and-w/latest?topic=models-granite-30-8b-instruct-model-card){: external} to respond to your questions.
{: note}

Administrators can also change the LLM from **Configuration and settings > Model settings**. 

When the LLM is changed, the change applies at the account level and to new conversations or queries. This means that the change applies to everyone that is a part of the Cloud account that has access to {{site.data.keyword.wxbia_short}}.

All members in the account are notified when the LLM changes. The updated LLM name appears in the AI icon and the query generation step under **Steps taken by AI** in Conversations.  
